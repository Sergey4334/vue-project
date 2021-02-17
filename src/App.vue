/* eslint-disable vue/valid-template-root */
<template>
  <div id="app">
    <h1  class="title">Hello World</h1>
    <HelloWorld :title="title" @ochacheCouter="oCouterComp"/>
    <input type="text" v-model="text"/>
    <h3>I text value: <i>{{text}}</i></h3>
    <div class="check">
      <input type="checkbox" v-model="check" />
      <h3>I text checkbox value: <i>{{check}}</i></h3>

      <input type="checkbox" v-model="checkArr" value="o" />
      <input type="checkbox" v-model="checkArr" value="two" />
      <input type="checkbox" v-model="checkArr" value="three" />
      <h3>I text checkbox value: <i>{{checkArr}}</i></h3>
    </div>
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
    title: 'Some title',
    text: '',
    check: false,
    checkArr: [],
  }),
  methods: {
    oCouterComp(value) {
      console.log('click App.vue:', value);
    },
  },
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
