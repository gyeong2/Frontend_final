<template>
    <h1>ExamThree</h1>
    <select v-model="color">
        <option>yellow</option>
        <option>green</option>
        <option>red</option>
        <option>blue</option>
    </select>
    <div calss="box" v-bind:class="color">
        <p>ExamThree</p>
    </div>
</template>

<script>
export default {
    name: 'ExamThreeChild', 
    data() {
        return {
            color: "yellow"
        };
    }
}
</script>

<style scoped>
  div.box { display: inline-block; padding: 100px; margin: 10px; width: 200px;
        border: 1px solid gray; }
  select { padding: 5px; font-size: 15pt; width: 150px; margin: 10px; }
  .yellow { background-color: #ffa; }
  .green { background-color: #bfb; }
  .blue { background-color: #bbf; }
  .red { background-color: #fbb; }
</style>

