<template>
    
<div class="col-xs-6" id="app">
  <div class="form-group">
    <label for="make">Year</label>
    <select class="form-control" name="year" id="year" v-model="year">
      <option :value="null" disabled selected>Select year</option>
      <option v-for="option in year_options" v-bind:value="option.id" v-bind:key="option.id">{{option.text}}</option>
    </select>
  </div>
  <div class="form-group">
      
    <label for="model">Select your unit</label>
    <select class="form-control" name="unit" id="unit" v-model="unit">
         
      <option v-for="option in unit_options[year]" v-bind:value="option.id" v-bind:key="option.id">{{option.text}}</option>
    </select>
  </div>
</div>
</template>

<script>
export default {
    data(){
        return{

    year: null,
    unit: null,
    year_options: [
      {
        text: "2014",
        id: 1
      },
      {
        text: "2015",
        id: 2
      },
      {
        text: "2016",
        id: 3
      },
    ],
    unit_options: {
      1: [
        {
          text: "unit-1",
          id:10
        },
        {
          text: "unit-2",
          id:11
        },
        {text: "unit-3",
          id:12
        },
        {text: "unit-4",
          id:13
        },
        {text: "unit-5",
          id:14
        },
        {text: "unit-6",
          id:15
        },
      ],
      2: [
        {
          text: "unit-1",
          id:20
        },
        {
          text: "unit-2",
          id:21
        },
        {text: "unit-3",
          id:22
        },
        {text: "unit-4",
          id:23
        },
        {text: "unit-6",
          id:25
        },
      ],
      3: [
        {
          text: "unit-1",
          id:30
        },
        {
          text: "unit-2",
          id:31
        },
        {text: "unit-3",
          id:32
        },
        {text: "unit-4",
          id:33
        },
        {text: "unit-5",
          id:34
        },
        
      ]
    },
  }
  }
    }

</script>