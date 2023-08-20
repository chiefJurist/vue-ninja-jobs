<template>
    <h1>Job Details Page</h1>
    <p>The job id is {{ id }}</p>
</template>

<script>
    export default {
        //Accepting the route parameter as a prop. This is from "params: {id: job.id}}"
        props: ['id'],
        //data(){
        //    return{
        //        id: this.$route.params.id
        //    }
        //}
    }
</script>

<style>

</style>