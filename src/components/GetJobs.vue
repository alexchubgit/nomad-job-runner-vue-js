<template>
    <button @click="getJobs">Show jobs</button>

    <div v-for="item in post" :key="item.idjob">
        <h2>{{ item.idjob }} - {{ item.job }}</h2>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            post: []
        }
    },
    methods: {
        getJobs() {
            fetch('http://localhost:8000/jobs').then(response => response.json())
                .then(data => this.post = data)
        }
    },
    mounted() {
        this.getJobs()
    }
}
</script>

