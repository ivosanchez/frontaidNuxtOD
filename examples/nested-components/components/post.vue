<template>
  <div class="main">
    <h1 class="title">
      {{ title }}
    </h1>
    <slot />
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>
h1{
  font-family: Oxygen;
}
.main {
  font: 15px Oxygen, Arial;
  border: 1px solid rgb(41, 228, 24);
  background: rgba(26, 233, 33, 0.2);
  padding: 0 10px;
}
.title {
  font-size: 16px;
  font-weight: bold;
  margin: 10px 0
}
</style>
