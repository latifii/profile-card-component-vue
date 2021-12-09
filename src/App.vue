<template>
  <CardMain />
</template>

<script>
import CardMain from "./components/CardMain.vue";

export default {
  name: "App",
  components: {
    CardMain,
  },
};
</script>

<style>
:root {
  /*  Primary */
  --primary-white: #fff;
  --primary-dark-cyan: hsl(185, 75%, 39%);
  --primary-very-dark-desaturated-blue: hsl(229, 23%, 23%);
  --primary-dark-grayish-blue: hsl(227, 10%, 46%);

  /*  Neutral */

  --neutral-dark-gray: hsl(0, 0%, 59%);
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  /* font-size: 10px; */
  /* 10px / 16px = 0.625 = 62.5% */
  /* Percentage of user's browser font-size setting */
  font-size: 62.5%;
}
body {
  position: relative;
  max-width: 100vw;
  height: 100vh;
  background-color: var(--primary-dark-cyan);
  background-image: url(./assets/bg-pattern-top.svg),
    url(./assets/bg-pattern-bottom.svg);
  background-position: right calc(47vw + 15%) bottom calc(65vh - 15vw),
    left calc(40vw + 25%) top calc(72vh - 15vw);
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
}
#app {
  font-family: "Kumbh Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
