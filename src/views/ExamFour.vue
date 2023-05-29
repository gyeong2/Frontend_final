<template>
    <h1>ExamFour</h1>
    <table>
        <tr><td>index</td><td>value</td></tr>
        <tr v-for="table in tables" v-bind:key="table.id">
            <td>{{ table.id }}</td>
            <td>{{ table.value }}</td>
        </tr>
    </table>
    <div>
        <p>ExamFourChild</p>
        <input type="text" v-model="value" />
        <button type="button" v-on:click="addTable">전달 </button>
    </div>
</template>

<script>
export default {
    name: 'ExamFourChild',
    data() {
        return{
            tables: [
               
            ], 
            lastId: 0
        }
    },
    methods: {
        addTable: function() {
            this.tables.push(({id: this.lastId++, value: this.value}))
            this.value = "";
        }
    }
}
</script>

<style scoped>
h1 { border-bottom: 1px solid gray; }
div { padding: 30px; margin: 30px auto; width: 400px;
  border: 1px solid #ccc; background-color: rgb(255, 255, 215); }
table { border-collapse: collapse; margin: auto; width: 70%; }
tr:nth-child(1) { background-color: #eee; text-align: center; }
td { border: 1px solid gray; padding: 6px; width: 10px; }
tr { width: 30px; }
input { margin: 5px; }
</style>