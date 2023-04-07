<template>
    <button @click="getCompanies">Show companies</button>

    <div v-for="item in post" :key="item.idcompany">
        <h2>{{ item.idcompany }} - {{ item.company }}</h2>
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
        getCompanies() {
            fetch('http://localhost:8000/companies').then(response => response.json())
                .then(data => this.post = data)
        }
    },
    mounted() {
        this.getCompanies()
    }
}
</script>

