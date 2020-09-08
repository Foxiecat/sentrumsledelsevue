<template>
<!--<div>
    <table v-bind:key="company" v-for="company in companies">
        <tr>
            <td>{{ company.title }} <button on:click="companyAbout">O</button></td>
            <td>{{ company.lastUpdated }}</td>
            <td>{{ company.branch }}</td>
        </tr>
    </table>
</div>-->

<div style="width: 600px">
    <vue-table-dynamic :params="params" ref="table"></vue-table-dynamic>
</div>
</template>

<script>
import VueTableDynamic from 'vue-table-dynamic'
// import CompanyItem from "./CompanyItem"

export default {
    name: "Companies",
    components: {
        VueTableDynamic
    },
    props: ["companies", "company"],
    data() {
        return {
            params: {
                data: [
                    ['Index', 'Navn', 'Sist Oppdatert', 'Bransje'],
                    [1, `Komplett`, '4', 'Electro'],
                    [2, 'Mat Butikk', '10', 'Grocery Store'],
                    [3, '63788d', 'a8c325', 'aab418'],
                    [4, 'hf7y8c', '4rghjk', 'cgnhik']
                ],
                header: 'row',
                border: true,
                stripe: true,
                enableSearch: true
            }
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

div {
    display: inline-block;
}
</style>
