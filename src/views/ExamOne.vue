<template>
    <h1>ExamOne</h1>
    <p>201914006</p>
    <p>김경이</p>
    <p>{{ time }}</p>
</template>

<script>
export default {
    name: 'ExamOne',
    data(){
        return {
           time: new Date() 
        }
    }
    
}
</script>
