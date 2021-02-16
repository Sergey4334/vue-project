/* eslint-disable vue/valid-template-root */
<template>
  <div id="app">
    <h1>{{first}}</h1>
    <h2>{{od.age}}</h2>
    <a v-bind:href="lik">Link</a>
    <a :[attrKey]="lik">Link</a>
    <template v-if="msgIsVisile === 1">
    <div class="msg">some msg!</div>
    </template>
    <template v-else-if="msgIsVisile === 2">
      <div class="msg">else if msg!</div>
    </template>
    <template v-else>
      <div class="msg">regrat msg!</div>
    </template>
    <div v-show="isVisileShow">W show text</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    HelloWorld,
  },
  data: () => ({
    first: 'Serhii',
    od: {
      age: 20,
    },
    lik: 'http://google.com',
    attrKey: 'href',
    msgIsVisile: 2,
    isVisileShow: true,
  }),
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
