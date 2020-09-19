<template>
  <section>
    <h1 class="title">{{title}}</h1>
    <p class="content">{{content}}</p>
  </section>
</template>


<script>
export default {
  name: "Posts",
  props: {
    title: String,
    content: String,
  },
};
</script>


<style lang="stylus"></style>