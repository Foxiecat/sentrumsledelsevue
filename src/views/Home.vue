<template>
<div id="home">
    <Header />
    <router-view />
    <Companies v-bind:companies="company" />

</div>
</template>

<script>
// @ is an alias to /src
import Header from "../components/layout/header"
import Companies from "../components/companies"

export default {
    name: 'Home',
    components: {
        Header,
        Companies
    },
    data() {
        return {
            company: [{
                    id: 1,
                    title: "Komplett",
                    lastUpdated: 4,
                    branch: "Electro"
                },
                {
                    id: 2,
                    title: "Mat Butikk",
                    lastUpdated: 10,
                    branch: "Mat"
                }
            ]
        }
    }
}
</script>

<style scoped>
table,
th,
td {
    border: 1px solid black;
    padding: 5px;
}
</style>
