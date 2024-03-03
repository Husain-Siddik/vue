<template>
  <div>
    <h1>this component have filter </h1>
    <p>{{ template | uppercase }}</p>
  </div>
</template>

<script>
export default {
  name: "filtersComponent",
  data (){
    return{
      template : 'a simple text'
    }
  },
  filters : {
    // capitalize: function (value) {
    // if (!value) return ''
    // value = value.toString()
    // return value.charAt(0).toUpperCase() + value.slice(1)
    //       }

    uppercase : function (value) {
     if (!value) return ''
      return  value.toUpperCase()
    }
  }
  
};
</script>

<style lang="postcss" scoped></style>
