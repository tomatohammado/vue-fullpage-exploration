<template>
  <div id="app">
    <ul id="menu">
      <li data-menuanchor="week-1" class="active"><a href="#week-1">Week 1</a></li>
      <li data-menuanchor="week-2"><a href="#week-2">Week 2</a></li>
      <li data-menuanchor="week-3"><a href="#week-3">Week 3</a></li>
    </ul>


    <full-page :options="options" id="fullpage">
      <div class="section">
        <h3>Section 1</h3>
      </div>
      <div class="section">
        <div class="slide">
           <h3>Slide 2.1</h3>
        </div>
        <div class="slide">
           <h3>Slide 2.2</h3>
        </div>
        <div class="slide">
           <h3>Slide 2.3</h3>
        </div>
      </div>
      <div class="section">
         <h3>Section 3</h3>
      </div>
    </full-page>

  </div>
</template>

<script>
  import FullPage from './components/FullPage.vue'
  import fullPageMixin from './fullPageMixin'

export default {
  name: 'app',
  mixins: [fullPageMixin],
  components: {
    FullPage
  },
  data() {
    return {
      options: {
        scrollBar: false,
        menu: '#menu',
        navigation: true,
        anchors: ['week-1', 'week-2', 'week-3']
      },
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
