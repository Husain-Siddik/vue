<template>
  <div>
    <h1>{{ title}}</h1>
    <div >
      <span>Now you see me:-{{ name }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name : "extra-bold",
  components: {},

  data() {
    return {
      title: "Hello",
      name: "rony",
      users: [],
    };
  },

  computed() { },

  mounted() {
    //lifecycle hook
    //computed
    //watch
    //emit
    //props / how to pass props to a componenet
  },

  created() { },

  methods: {
    checkInputValue() {
      this.title = `welcome ${this.name}`;
      console.log("name=> ", this.name);
      //this.name = "constant name"
    },
  },
};
</script>
<style scoped>
div {
  background-color: beige;
}
</style>
