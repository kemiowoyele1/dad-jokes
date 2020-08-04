<template>
    <header class="header">
        <h1 class="tjtle">
            Dad jokes
        </h1>
        <ul>
            <li>
                <nuxt-link to="/">Home</nuxt-link>
            </li>
               <li>
                <nuxt-link to="/jokes">Jokes</nuxt-link>
            </li>
               <li>
                <nuxt-link to="/about">About</nuxt-link>
            </li>
        </ul>
    </header>
</template>
<script>
export default {
      name: "AppHeader"
}
</script>
<style scoped>
.header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
    padding-bottom: 1rem;
    border-bottom: 10px ridge rgb(20, 8, 92);
}
.header .title{
    font-size: 3rem;
    color: #526488;
}

.header ul{
    display: flex;
}

.header a {
    display: inline-block;
    background: #333;
    color: #fff;
    padding: 0.3rem 1rem;
    margin-right: 0.5rem;
}

</style>