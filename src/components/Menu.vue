<template>
  <div class="menu">
    <ul>
      <li v-for="item in items" :key="item.component">
        <a href="#" @click="changeItem(item)">{{item.text}}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
  data: () => ({}),
  methods: {
    changeItem(item) {
      this.$emit('changeItem', item)
    },
  },
}
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css?family=Poppins:100,200,300,400,500,600,700,800,900');
.menu {
  display: flex;
  place-items: center;
  justify-content: center;
  font-family: 'Poopins', sans-serif;
  font-weight: 600;
  background: #fff;

  ul {
    padding: 0;
    margin: 0;
    margin: 10px 0;
  }

  li {
    list-style: none;
    display: inline-block;
    padding: 10px;

    a {
      text-decoration: none;
      border: 1px #000 solid;
      padding: 10px 20px;
      text-transform: uppercase;
      color: #000;
    }
    a:hover {
      background: gray;
      color: #fff;
      border: 1px #fff solid;
    }
  }
}
</style>
