<template>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
        <router-link :to="{name: 'JobDetails', params: {id: job.id}}">
            <h2>{{ job.title }}</h2>
        </router-link>
    </div>
</template>

<script>
    //Here we fetch the data from the json server and populate the "jobs" property with it
    export default {
        data(){
            return{
                jobs: []
            }
        },
        mounted(){
            fetch('http://localhost:3000/jobs')
            //fetching the response
            .then((res)=> res.json())
            //fetching the actual data and populating the "jobs" property
            .then((data)=> this.jobs = data)
            //catching errors
            .catch(err => console.log(err.message))
        }
    }
</script>

<style>
    .job h2{
        background: #f4f4f4;
        padding: 20px;
        border-radius: 10px;
        margin: 10px auto;
        max-width: 600px;
        cursor: pointer;
        color: #444;
    }
    .job h2:hover{
        background: #ddd;
    }
    .job a{
        text-decoration: none;
    }
</style>