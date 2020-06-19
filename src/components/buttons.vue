<template>
  <div>
    <div class = "dropdown">
      
    </div>
    <b-form-group label="Using options array:">
      <template v-slot:label>
        <b>Choose your flavours:</b><br>
        <b-form-checkbox
          v-model="allSelected"
          @change="toggleAll"
        >
        {{ allSelected ? 'Un-select All' : 'Select All' }}
        </b-form-checkbox>
      </template>
      <b-form-checkbox-group
        id="flavours"
        v-model="selected"
        :options="flavours"
        name="flavours" 
      ></b-form-checkbox-group>
    </b-form-group>
    
   <div>
      Selected: <strong>{{ selected }}</strong><br>
      All Selected: <strong>{{ allSelected }}</strong><br>
     
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        selected: [], // Must be an array reference!
        flavours: ['Orange', 'Grape', 'Apple', 'Lime', 'Very Berry'],
        allSelected: false,
      }
    },
    methods: {
      toggleAll(checked) {
        this.selected = checked ? this.flavours.slice() : []
  }
    },
  }
</script>
  


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
