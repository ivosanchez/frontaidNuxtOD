<template>
  <main>
    <h1
      v-html="content.index.title"></h1>

    <div
      v-html="content.index.content"></div>
  </main>
</template>

<script>
  import conf from '../conf';

  export default {
    head() {
      return {
        title: this.content.title
      };
    },
    async asyncData({$content}) {
      const content = await $content(conf.CONTENT).fetch();
      return {content};
    },
  };
</script>

<style scoped>
  *{
    outline: 2px dashed gainsboro;
  }
  main{
    background: rgba(209, 13, 6, 0.8);
  }
</style>

