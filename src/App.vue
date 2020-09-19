<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello, world" />
  <Posts title="A SINGLE post.." content="Lorem ipsum dolor something something." />
  <Posts
    title="SUPA FAST"
    content="Lorem ipsum dolor something something. Lorem ipsum dolor something something. Lorem ipsum dolor something something. Lorem ipsum dolor something something."
  />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Posts from "./components/Posts.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Posts,
  },
};
</script>
