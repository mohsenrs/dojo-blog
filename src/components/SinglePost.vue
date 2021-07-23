<template>
  <div class="single-post">
    <b>{{ post.id }}</b>
    <h4>{{ post.title }}</h4>
    <p>{{ snippet }}</p>
    <hr />
  </div>
</template>

<script>
import { computed } from '@vue/runtime-core';
export default {
  props: ['post'],
  setup(props) {
    const snippet = computed(() => {
      return props.post.body.substring(0, 100) + '.....';
    });

    return { snippet };
  },
};
</script>

<style></style>
