<template>
    <nav>
        <router-link to="/">Home</router-link> |
        <router-link :to="{name: 'About'}">About</router-link> |
        <router-link :to="{name: 'Jobs'}">Jobs</router-link>
    </nav>

    <button @click="backward">Go back</button>
    <button @click="redirect">Redirect</button>
    <button @click="forward">Go Forward</button>
    <router-view/>
</template>


<script>
    export default{
        methods: {
            //Going backward by one page
            backward(){
                this.$router.go(-1)
            },
            //Going forward by one page
            forward(){
                this.$router.go(1)
            },
            //Redirecting to the home page
            redirect(){
                this.$router.push({name: 'Home'})
            }
        }
    }
</script>


<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }

    nav {
        padding: 30px;
    }

    nav a {
        font-weight: bold;
        color: #2c3e50;
        text-decoration: none;
        padding: 10px;
        border-radius: 4px;
    }

    nav a.router-link-exact-active {
        color: white;
        background: crimson;
    }

    button{
        margin: 0 15px;
        padding: 10px;
        border: none;
        border-radius: 5px;
    }
</style>
