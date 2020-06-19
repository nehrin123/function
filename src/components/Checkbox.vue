<template>
    <div>
        <div class="container">
            <input type="checkbox" id="1" value="unit-1" v-model="checkedNames">
            <label for="unit 1">Unit-1</label>

            <input type="checkbox" id="2" value="unit-2" v-model="checkedNames">
            <label for="unit 2">Unit-2</label>

            <input type="checkbox" id="3" value="unit-3" v-model="checkedNames">
            <label for="unit 3">Unit-3</label>

            <input type="checkbox" id="4" value="unit-4" v-model="checkedNames">
            <label for="unit 4">Unit-4</label>

            <input type="checkbox" id="5" value="unit-5" v-model="checkedNames">
            <label for="unit 5">Unit-5</label>

            <input type="checkbox" id="6" value="unit-6" v-model="checkedNames">
            <label for="unit 6">Unit-6</label>
            
        </div>
        
       
        <span>Checked names: {{ checkedNames }}</span>       
        </div>
  
</template>

<script>
export default {
    data(){
        return{
            checkedNames:[],
            
        }
}
}
</script>
<style scoped>
input{
  margin: 3em;
}
</style>