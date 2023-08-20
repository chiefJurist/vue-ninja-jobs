<template>
    <h1>Job Details Page</h1>
    <p>The job id is {{ id }}</p>
</template>

<script>
    export default {
        data(){
            return{
                //'this.$route.params' references the route parameter while ".id" is the name we gave the path in the router
                id: this.$route.params.id
            }
        }
    }
</script>

<style>

</style>