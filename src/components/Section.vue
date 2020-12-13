<template>
  <section :class="color" :id="id">
    <div class="flex column justify-center align-center ">
      <h1>{{ title }}</h1>
      <span class="underline"></span>
    </div> 
  </section>
</template>

<script>
export default {
  props: {
    color: String,
    title: String,
    id: String,
  },
}
</script>

<style scoped>
  section {
    min-height: calc(100vh - 60px);
  }
  h1 {
    color: rgba(245, 245, 245, 0.829);
    margin-bottom: 2px;
  }
  .underline {
    width: 50px;
    height: 2.5px;
    background-color: #FF4A57;
  }
</style>