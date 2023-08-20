<template>
    <h1>{{job.title}}</h1>
    <p>The job id is {{ id }}</p>
    <p>{{ job.details }}</p>
</template>

<script>
    export default {
        props: ['id'],
        //Storing the fetched data from mounted below in a property
        data(){
            return{
                job: null
            }
        },
        //Fetching the details of each job
        mounted(){
            fetch('http://localhost:3000/jobs' + this.id)
            //fetching the response
            .then((res)=> res.json())
            //fetching the actual data and populating the "jobs" property
            .then((data)=> this.job = data)
            //catching errors
            .catch(err => console.log(err.message))
        }
    }
</script>

<style>

</style>