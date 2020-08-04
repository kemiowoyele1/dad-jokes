<template>
<nuxt-link  :to="'jokes/' + id" >
 <div class="joke">
        <p>{{ joke }}</p>
    </div>
</nuxt-link>
   
</template>
<script>
export default {
    name: "joke",
    props: ["joke", "id"]
}
</script>
<style scoped>
.joke{
    padding: 1rem;
    border: 1px dotted #ccc;
    margin: 1rem 0;
    background-color: rgb(196, 38, 64);
    border:inset 2px 2px 5px rgb(88, 2, 38);
    color: thistle;
}
</style>