<template>
  <v-app style="background-color: #353535; overflow: auto">
    <v-app-bar
      app
      color="#ebebeb"
      dark
    >
    <span class="animation-p"> Hello World!!</span>
    </v-app-bar>

    <v-main>
      <Content/>
    </v-main>
  </v-app>
</template>

<script>
import Content from './components/Content';

export default {
  name: 'App',

  components: {
    Content,
  },

};
</script>

<style lang="scss" scoped>
.animation-p {
  animation-duration: 40s;
  color: #353535;
  font-size: 25px;
  animation-name: slidein;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  margin-bottom: 0px;
  &:before {
    content: "😄";
  }
  cursor: pointer;
  &:active {
    &:before {
      content: "😡";
    }
    animation-play-state: paused;
  }
}

@keyframes slidein {
  from {
    margin-left: 10px;
  }

  50% {
    margin-left: calc(100% - 190px);
  }

  to {
    margin-left: 10px;
  }
}
</style>
