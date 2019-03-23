<template>
  <div id="app">
    <Menu :items="samples" @changeItem="changeItem"/>
    <component :is="component"></component>
  </div>
</template>

<script>
import Menu from './components/Menu.vue'
import Sample1 from './samples/Sample1.vue'
import Sample2 from './samples/Sample2.vue'
import Sample3 from './samples/Sample3.vue'
import Sample4 from './samples/Sample4.vue'
import Sample5 from './samples/Sample5.vue'
import Sample6 from './samples/Sample6.vue'

export default {
  name: 'App',
  components: { Menu, Sample1, Sample2, Sample3, Sample4, Sample5, Sample6 },
  data: () => ({
    samples: [
      { component: 'Sample1', text: 'Menu 1' },
      { component: 'Sample2', text: 'Menu 2' },
      { component: 'Sample3', text: 'Smoke 1' },
      { component: 'Sample4', text: 'Smoke 2' },
      { component: 'Sample5', text: 'Layers' },
      { component: 'Sample6', text: 'Movie Card' },
    ],
    component: Sample6,
  }),
  methods: {
    changeItem(item) {
      this.component = item.component
    },
  },
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
</style>
