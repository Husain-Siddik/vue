<template>
    <div>
      <ul id="example-1">
        <li v-for="(item, i) in items" :key="i" >
          index={{i}}, Message={{ item.message }} - <span @click="deleteItem(i)">delete</span>
        </li>
        <li>{{ users }}</li>
      </ul>
            <filters/>
    </div>
</template>

<script>
import filters from '@/components/filters.vue';
export default {

  name : "profile-new",
  // jehetu component add hoise seheto componenets er modde aita add kora dorkar
  components: {
        filters,
  },

  data() {
    return {
      title: "Hello",
      name: "rony",
      users: [],

      items: 
      [
      { id: "1", message: 'Foo' },
      { id: "2",message: 'Bar' },
      { id: "3",message: 'alpha' },
      { id: "4", message: 'beta' },
      { id: "5", message: 'delta' }
    ]
    };
  },

  computed:{},

  mounted(){
    //lifecycle hook
    //computed
    //watch
    //emit
    //props / how to pass props to a componenet
  },
  methods: {
    checkInputValue() {
    //   this.title = `welcome ${this.name}`;
    //   console.log("name=> ", this.name);
      //this.name = "constant name"
    },
    deleteItem(i){
      //console.log(this.items[i]);
      console.log(i);
      console.log(this.items.splice(i,1));
      this.users.push(i);
      //this.items.splice(i, 1)
    },
  },
};
</script>

 
 
