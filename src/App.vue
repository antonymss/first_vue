<template>
  <div class="app">
    <post-form @create="createPost"/>
    <post-list :posts="posts"  />
  </div>
</template>

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  components: {
    PostList,
    PostForm,
  },
  data() {
    return {
      posts: [
        { id: 1, title: "JS", body: "description" },
        { id: 2, title: "JS 2", body: "description" },
        { id: 3, title: "JS 3", body: "description" },
      ],
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
    },
  },
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}
</style>