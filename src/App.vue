

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
import { onMounted, reactive } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import Posts from "./components/Posts.vue";

// http://localhost:8888/tailwind/wp-json/wp/v2

export default {
  name: "App",
  components: {
    HelloWorld,
    Posts,
  },
  data: () => ({
    posts: {
      title: "test",
      content: "testing",
    },
  }),
  setup() {
    const posts = reactive({ posts: [] });

    onMounted(() => {
      fetch("http://localhost:8888/tailwind/wp-json/wp/v2/posts")
        .then((res) => {
          if (res.status !== 200) {
          } else {
            return res.json();
          }
        })
        .then((res) => {
          posts.posts.push(res);
        });
    });
  },
};
</script>
