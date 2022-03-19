<template>
  <div>
    <button @click="addLike">like</button>
    <button @click="addDislike">dislike</button>
    <div>
      количество лайков:<strong>{{ likes }}</strong>
    </div>
    <div>
      количество дизлайков:<strong>{{ dislikes }}</strong>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      likes: 0,
      dislikes: 10,
    };
  },
  methods: {
    addLike() {
      this.likes += 1;
    },
    addDislike() {
      this.dislikes += 1;
    },
  },
};
</script>
<style>
</style>