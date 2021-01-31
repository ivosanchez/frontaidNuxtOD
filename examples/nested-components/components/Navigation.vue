<template>
  <nav>
    <ul>
      <li>
        <nuxt-link to="/">{{ content.index.title }}</nuxt-link>
      </li>
      <li
        v-for="page in content.pages" :key="page.title">
        <nuxt-link :to="page.path">{{ page.title }}</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
import conf from '../conf';

export default {
  data() {
    return {content: null};
  },
  async fetch() {
    this.content = await this.$content(conf.CONTENT).fetch();
  },
};
</script>

<style scoped>




  nav ul {
    display: flex;
    justify-content: space-between;
    outline: 1px dashed darkblue;
    background: rgba(189, 189, 94, 0.87) ;
    list-style: none;
    text-transform: uppercase;
    padding: .3rem;
    font-family: 'Optician Sans', 'Ubuntu', sans-serif;
    outline: 1px solid blue;
    border-radius: 5px ;

  }




</style>
