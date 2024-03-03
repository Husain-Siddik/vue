<template>
    <div class="loop ">
        <h2> this is from loop component</h2>
        <h3 v-if="seen">this will bew seen when seen is true on button click</h3>
        <button v-on:click="showhide()" >Hide</button>
        <hr>
        <h3>there are a listed item:-- </h3>
        <button v-on:click="showit()"> hide  them-</button>
        <div v-if="seen2">
            <ul class="li">
                <!-- list item useing for in loop -->
                <li v-for="item in items" :key="item.message">
                    {{item.message }}
                </li>
            
            </ul>
            <ul class="li">
                <!-- list item useing  index for in loop -->
                <li v-for="(item,index) in items" :key="item.message">
                    {{ index }}--{{ item.message }}
                </li>
            
            </ul>
        </div>
        <hr>
        <!-- function er valu null, undefined,  false,  hole disable hobe -->
        <button v-bind:disabled="isButtonDisabled">Button</button><br>
        <!--  class add kora  -->
        <button  v-bind:class ="idClass.class" >dayna milky added id</button>
        <br> 
        

    </div>
</template>


<script>
export default {
  name: "loop-1st",
  data() {
    return {
      seen: true,
      seen2: true,
      selected:'',
      dynamicId: "koa",
      items: [{ message: "Foo" }, { message: "Bar" }],
      idClass: {
        id: "container",
        class: "wrapper",
      },
    };
  },
  methods: {
    showhide() {
      // this way toggle item easyly
      this.seen = !this.seen;
    },
    showit() {
      this.seen2 = !this.seen2;
    },
    isButtonDisabled() {},
  },
};
</script>
<style>
.loop {
  background-color: darkcyan;
  height: auto;
  width: 50%;
  padding: 40px;
  text-transform: capitalize;
}
</style>

