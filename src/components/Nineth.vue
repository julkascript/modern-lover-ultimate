<template>
  <div class="container">
    <h1 class="happy-title">
      💌💜
      <p class="message" v-html="messages[hearts]"></p>
      🎉🎉
    </h1>
    <button @click="bubbly()" class="bubbly-button">Click me</button>
    <div class="hearts-container">
      <p v-show="hearts > 0">💜</p>
      <p v-show="hearts > 1">💙</p>
      <p v-show="hearts > 2">🤎</p>
      <p v-show="hearts > 3">🖤</p>
      <p v-show="hearts > 4">💚</p>
      <p v-show="hearts > 5">💛</p>
      <p v-show="hearts > 6">🧡</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Nineth",
  data() {
    return {
      hearts: 0,
      messages: [
        "Happy 7 months, bae!",
        "I love you!",
        "I care for you!",
        "You hot af, grill ;)",
        "*hugs you*",
        "Damn shortie ^^",
        "Sheeesh, that's my girl",
        "Yuli loves ya"
      ],
    };
  },
  methods: {
    bubbly() {
      if (this.hearts === 7) {
        this.hearts = 0;
      } else {
          this.hearts++;
      }
    },
  },
  computed: {},
};
</script>

<style scoped>
.container {
  display: flex;
  width: 60%;
  margin: 0 auto;
  padding: 2rem;
  border-radius: 9px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: rgb(250, 173, 186);
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

.message {
    padding-left: 1rem;
    padding-right: 1rem;
}

.hearts-container {
  display: flex;
  justify-content: space-evenly;
  width: 40%;
}

.happy-title {
  margin-bottom: 2rem;
  display: flex;
}

.bubbly-button {
  margin-bottom: 2rem;

  font-family: "Helvetica", "Arial", sans-serif;
  display: inline-block;
  font-size: 1em;
  padding: 1em 1.5em;
  -webkit-appearance: none;
  appearance: none;
  background-color: #ff0081;
  color: #fff;
  border-radius: 9px;
  border: none;
  cursor: pointer;
  position: relative;
  transition: transform ease-in 0.1s, box-shadow ease-in 0.25s;
  box-shadow: 0 2px 25px rgba(255, 0, 130, 0.5);
}
.bubbly-button:focus {
  outline: 0;
}
.bubbly-button:before,
.bubbly-button:after {
  position: absolute;
  content: "";
  display: block;
  width: 140%;
  height: 100%;
  left: -20%;
  z-index: -1000;
  transition: all ease-in-out 0.5s;
  background-repeat: no-repeat;
}
.bubbly-button:before {
  display: none;
  top: -75%;
  background-image: radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, transparent 20%, #ff0081 20%, transparent 30%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, transparent 10%, #ff0081 15%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%);
  background-size: 10% 10%, 20% 20%, 15% 15%, 20% 20%, 18% 18%, 10% 10%, 15% 15%,
    10% 10%, 18% 18%;
}
.bubbly-button:after {
  display: none;
  bottom: -75%;
  background-image: radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, transparent 10%, #ff0081 15%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%),
    radial-gradient(circle, #ff0081 20%, transparent 20%);
  background-size: 15% 15%, 20% 20%, 18% 18%, 20% 20%, 15% 15%, 10% 10%, 20% 20%;
}
.bubbly-button:active {
  transform: scale(0.9);
  background-color: #e60074;
  box-shadow: 0 2px 25px rgba(255, 0, 130, 0.2);
}
.bubbly-button.animate:before {
  display: block;
  animation: topBubbles ease-in-out 0.75s forwards;
}
.bubbly-button.animate:after {
  display: block;
  animation: bottomBubbles ease-in-out 0.75s forwards;
}

@keyframes topBubbles {
  0% {
    background-position: 5% 90%, 10% 90%, 10% 90%, 15% 90%, 25% 90%, 25% 90%,
      40% 90%, 55% 90%, 70% 90%;
  }
  50% {
    background-position: 0% 80%, 0% 20%, 10% 40%, 20% 0%, 30% 30%, 22% 50%,
      50% 50%, 65% 20%, 90% 30%;
  }
  100% {
    background-position: 0% 70%, 0% 10%, 10% 30%, 20% -10%, 30% 20%, 22% 40%,
      50% 40%, 65% 10%, 90% 20%;
    background-size: 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%;
  }
}
@keyframes bottomBubbles {
  0% {
    background-position: 10% -10%, 30% 10%, 55% -10%, 70% -10%, 85% -10%,
      70% -10%, 70% 0%;
  }
  50% {
    background-position: 0% 80%, 20% 80%, 45% 60%, 60% 100%, 75% 70%, 95% 60%,
      105% 0%;
  }
  100% {
    background-position: 0% 90%, 20% 90%, 45% 70%, 60% 110%, 75% 80%, 95% 70%,
      110% 10%;
    background-size: 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%;
  }
}
</style>