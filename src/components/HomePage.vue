<template>
  <div class="container">
    <h1 class="title">n + y</h1>
    <div class="star-box-container">
      <div id="star-box">
        <div id="stars"></div>
        <div id="stars2"></div>
        <div id="stars3"></div>
        <img class="anime-img" src="@/assets/images/niya-anime.png" alt="" />
      </div>
      <svg class="arrows">
        <path class="a1" d="M0 0 L30 32 L60 0"></path>
        <path class="a2" d="M0 20 L30 52 L60 20"></path>
        <path class="a3" d="M0 40 L30 72 L60 40"></path>
      </svg>
      <div id="star-box">
        <div id="stars"></div>
        <div id="stars2"></div>
        <div id="stars3"></div>
        <img class="anime-img" src="@/assets/images/yuli-anime.png" alt="" />
      </div>
    </div>
    <div class="texts-container">
      <div class="text-box">
        <h3 class="text-box-name-title">niya</h3>
        <p>
          The supreme leader of Russia. Do not approach unless you have a solid
          reason.
        </p>
        <p class="text-box-feature">
          <strong>Favorite animal:</strong> your mom.
        </p>
      </div>
      <div class="text-box">
        <h3 class="text-box-name-title">yuli</h3>
        <p>Your dad. Therefore this can mean only one thing though...</p>
        <p class="text-box-feature"><strong>Favorite animal:</strong>keks.</p>
      </div>
    </div>
    <CSS />
  </div>
</template>

<script>
import CSS from "./CSS.vue"
export default {
    name: 'HomePage',
    components: {
      CSS
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@200&display=swap');
.container {
  width: 90%;
  margin: 0 auto;
}

.title {
  color: whitesmoke;
  text-shadow: 1px 1px black;
  font-size: 3rem;
  margin-top: 4rem;
  margin-bottom: 3rem;
  justify-content: center;
  display: flex;
}

#star-box {
  height: 400px;
  width: 300px;
  display: flex;
  justify-content: center;
  border-radius: 22px;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  overflow: hidden;
  cursor: pointer;
}

.anime-img {
  max-width: 100%;
  max-height: 100%;
}

.star-box-container {
  width: 100%;
  display: flex;
  justify-content: space-around;
}

.texts-container {
  margin-top: 6rem;
  display: flex;
  justify-content: space-around;
  padding-bottom: 3rem;
}

.text-box {
  display: flex;
  flex-direction: column;
  width: 30%;
  padding: 1.5rem;
  background-color: rgb(245, 240, 240);
  border-radius: 11px;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

.text-box-name-title {
  margin-bottom: 1rem;
}

.text-box-feature {
  margin-top: 1rem;
}

.text-box-feature strong {
  padding-right: 0.4rem;
}

@media only screen and (max-width: 850px) {
  #star-box {
    height: 300px;
    width: 200px;
  }
}

@media only screen and (max-width: 620px) {
  #star-box {
    height: 250px;
    width: 150px;
  }
}

@media only screen and (max-width: 500px) {
  #star-box {
    height: 250px;
    width: 150px;
  }
  .container {
    width: 100%;
    margin: 0 auto;
  }
  .text-box {
    width: 27%;
  }
  .version {
    padding-right: 1rem;
  }
}
</style>