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

export default {
  name: 'App',
  components: { Menu, Sample1, Sample2, Sample3 },
  data: () => ({
    samples: [
      { component: 'Sample1', text: 'Menu1' },
      { component: 'Sample2', text: 'Menu2' },
      { component: 'Sample3', text: 'Smoke' },
    ],
    component: Sample3,
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
