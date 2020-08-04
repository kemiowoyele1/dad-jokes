<template>
    <div>
        <h2>{{ joke }}</h2>
        <hr>
        <small> joke ID = {{ $route.params.id}}</small>
         <nuxt-link class="back" to="/jokes">Back to jokes</nuxt-link>
       
        </div>
</template>
<script>
import axios from "axios";
export default {
    data() {
        return{
            joke: {} 
        }
    },
    async created(){
        const config = {
            headers: {
                Accept: 'application/json'
            }
        };
        try {
     const res = await axios.get(`
     https://icanhazdadjoke.com/j/${this.$route.params.id}`,
      config);
     this.joke = res.data.joke; 
        }
        catch (err){
            console.log(err);
        }
    },
         head(){
        return {
            title: this.$route.params.id,
            meta:[
                {
                    hid: "description",
                    name: "description",
                    name: "description",
                    content: "Best place for corny dad jokes"
                }
            ]
        };
         }
}
</script>
<style scoped>
.back{
   background-color: rgb(255, 36, 36);
   border: 2px solid grey;
   display: block;
   width: fit-content;
   padding: 10px;
   border-radius: 10px;
   margin-top: 15px;
   float: right;
}
</style>