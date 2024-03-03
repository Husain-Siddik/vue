<template>
    <div>
        <extra/>
        <hr>
        <h1>{{name }}</h1>
        <button v-on:click="greet"> click here...</button>
        <button v-on:click="printit"> click</button>
        <p>{{ count }}</p>
        <button v-on:click ="countPlus" >Count counter</button>
        <br><br>
        <p>input field</p><br>
        <input type="text" v-model="Text1"><br>
        <p> you type this bro  {{ Text1 }}</p>
        <hr>
        <loop/>
 
    </div>
</template>

<script>
import extra from "@/components/extra.vue";
import loop from "@/components/loop.vue";
export default {
  name: "Contact-ext",
  components: { extra,loop },
  data() {
    return {

      title: "Hello",
      name: "rony",
      users: [],
      count : 0,
      Text1: '',


    };
  },
  methods: {
    greet(){
        console.log('tunirma');
    },
     printit(){
        console.log('print it');

    },
    countPlus(){
        this.count++
    }
    

  },
  computed() {},
  created() {},
  mounted() {console.log(this .user.push('Text1'));},
};
</script>
