<template>
    <nav>
        <!--the "to" attribute is similar to the "href" attribute-->
        <!--Router links have classes that ebable styling
        -->
        <router-link to="/">Home</router-link>
        <!--You can data-bind the "to" attribute as seen below. This is useful when yo decide to change the path-->
        <router-link :to="{name: 'about'}">About</router-link>
    </nav>
    <!--This "<router-view/>" is where our router will be injected-->
    <router-view/>
</template>

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
</style>
