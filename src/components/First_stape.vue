<template>
    <div id="first-step">
        <!-- active color er man data ay dewa ace  -->
        <h1 v-bind:style="{ color: activeColor}" >this code is first step</h1>
        <p>{{ text }}</p>
        <input type="text" v-model="Text4"><br>
        <P class="colorChange"> typed from input box -- {{ Text4 }}</p>
       <hr>
       <a v-bind:href="link"> google</a>
       <!-- bind  shortcut -->
       <a :href="link"> GOOGLE</a> <br>
       <!-- <a href="https://www.google.com/">google</a> -->

       <!-- DYNAMICALLY CLASS ADD -->
       <!-- <div>
        <button >click to change</button> <br> <br>
       <p v-bind:class="{active: isActive}">Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores, consequuntur neque nostrum illum dolores quam recusandae soluta ducimus magnam nulla tenetur tempore doloribus similique possimus impedit accusantium consequatur maxime deserunt?</p>
       </div> -->
       <!--  dynamically class binding is not okay -->
       <div>
        <input type="text" >
        <p>class :---</p>
        <p v-bind:class="[activeClass, errorClass]"> dynamicaly class added</p>
       </div>

    </div>
</template>

<script>
export default {
    name: 'first-stape',
    props: {
        text: String,

    },
    data(){
        return{
            Text4: 'kolim',
            activeColor: 'red' ,
            link : 'https://www.google.com/',
            activeClass: 'active',
            errorClass: 'text-danger'

        }
    },
    methods:{
        inputtext(){
              

        }

    }
}
       
</script>

<style scoped>
#first-step {
    color: beige;
    background-color: darkgreen;
    padding: 30px;
};



</style>
