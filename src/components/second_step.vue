<template>
  <div class="second">
    <div v-bind:id="dynamicId">
      <h4>this is second-step component</h4>
      <div v-for="post in posts"  v-bind:key="post.id"  v-bind:title="post.title">
        
    {{ korim }}
          
      </div>
      <div>
        <alert-box>
  Something bad happened.
</alert-box>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "second_step",
  props: {
    text: String,
  },
  data() {
    return {
      dynamicId: "second",
      posts: [
        { id: 1, title: "My journey with Vue" },
        { id: 2, title: "Blogging with Vue" },
        { id: 3, title: "Why Vue is so fun" },
      ],
      korim :'akkas',
    };
  },
};
</script>
<style></style>
