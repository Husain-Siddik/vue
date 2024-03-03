<template>
  <div class="about">
    <h1>This is an about page</h1>
    <extra/>
    <First_stape text="this props pass by child element"/>
    <second_step/>
    
  </div>
</template>
<script>
// @ is an alias to /src
import extra from '@/components/extra.vue'
import First_stape from '@/components/First_stape.vue'
import second_step from '@/components/second_step'


export default {
  name: 'extra-use',
  components: {
    extra,
    First_stape,
    second_step,
  
  },
  data (){ return{
     

  }}
  ,
}
</script>
