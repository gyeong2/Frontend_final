<template>
    <h1>ExamTwo</h1>
    <table>
        <tr><td>ID</td><td>이름</td><td>나이</td><td></td></tr>
        <tr v-for="(table, index) in tables" v-bind:key="table.id"> 
            <td>{{ table.id }}</td> 
            <td> {{ table.name }} </td>
            <td>{{ table.age }}</td>
            <td><button type="button" v-on:click="deleteTable(index)">삭제</button></td>
        </tr>
    </table>
</template>

<script>
export default {
    name: 'ExamTwo',
    data(){
        return {
            tables: [
                {id: 101, name: "홍길동", age: 16},
                {id: 102, name: "임꺽정", age: 18}, 
                {id: 103, name: "장길산", age: 19},
                {id: 104, name: "이몽룡", age: 17}
            ],
            name: "", age:"",
            lastId: 104
        }
    },
    methods: {
        deleteTable(index) {
        if (confirm("삭제하시겠습니까?"))
            this.tables.splice(index, 1);
        }
    }
}
</script>

<style scoped>
h1 { border-bottom: 1px solid gray; }
div { padding: 30px; margin: 30px auto; width: 400px;
  border: 1px solid #ccc; box-shadow: 3px 3px 3px #aaa; }
table { border-collapse: collapse; margin: auto; width: 60%; }
tr:nth-child(1) { background-color: #eee; text-align: center; }
td { border: 1px solid gray; padding: 6px; }
td:nth-child(1) { text-align: center; width: 30px; }
button { padding: 0.3em 1.5em; }
</style>
