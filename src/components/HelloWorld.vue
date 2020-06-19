<template>
<div>
  <input type='checkbox' @click='checkAll()' v-model='isCheckAll'> Check All

  <!-- Checkboxes list -->
  <ul>
    <li v-for = "lang in langsdata" v-bind:key='lang'>
     <input type='checkbox'  v-model='languages' @change='updateCheckall()'>{{ lang }}
    </li>
  </ul>

  <!-- Print -->
  <input type='button' @click='printValues()' value='Print Selected Values'>

  <br>
  Selected items : {{ selectedlang }}
  </div>
</template>

<script>
  export default {
    data() {
      return {
        isCheckAll: false,
    langsdata: ["PHP","Vue.js","AngularJS","jQuery","JavaScript"],
    languages: [],
    selectedlang: ""
      }
    },
    checkAll: function(){

      this.isCheckAll = !this.isCheckAll;
      this.languages = [];
      if(this.isCheckAll){ // Check all
        for (var k in this.langsdata) {
          this.languages.push(this.langsdata[k]);
        }
      }
    },
    updateCheckall: function(){
      if(this.languages.length == this.langsdata.length){
         this.isCheckAll = true;
      }else{
         this.isCheckAll = false;
      }
    },
    printValues: function(){
      this.selectedlang = "";
      // Read Checked checkboxes value
      for (var k in this.languages) {
         this.selectedlang += this.languages[k]+", "; 
      }
    }
  }
</script>
  


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
