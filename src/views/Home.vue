<template>
  <div class="home">
    <PostList :posts="posts" />
  </div>
</template>

<script>
import { ref } from '@vue/reactivity';
import PostList from '../components/PostList.vue';
export default {
  name: 'Home',
  components: { PostList },
  setup() {
    const posts = ref([
      { title: 'soosis', body: 'lorem ipsum', id: 1 },
      { title: 'soosis22', body: 'lorem ipsum', id: 2 },
    ]);
    return { posts };
  },
};
</script>
