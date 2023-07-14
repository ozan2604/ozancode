<template>
  <div id="app">
    <div class="box" :style="{backgroundColor : color}"></div>
    <div class="box2" :style="customStyle"></div>
    <div class="box3" :style="[customStyle , {witdh: yukseklik + 'px'}]"></div>
    
    <hr>
    <input type="text" v-model="color">
    <input type="text" v-model="height">
    
  </div>
</template>
<script>
export default {
  data() {
    return {
      color:"green",
      height: 100
      }
  
  },
  computed : {
        customStyle: function(){
          return{
            backgroundColor: this.color,
            height : this.height + "px"
          }
        }

      }
}
</script>
<style >
.box{
  width: 100px;
  height: 100px;
  background-color: gray;
  display: inline-block;
  margin-right: 5px;
}

.box2{
  width: 150px;
  height: 150px;
  background-color: gray;
  display: inline-block;
  margin-right: 5px;
}
.box3{
  width: 200px;
  height: 200px;
  background-color:gray;
  display: inline-block;
  margin-right: 5px;
}
.greeen{
  background-color: green;
}
.blue{
  background-color: blue;
}
.red{
  background-color: red;
}


</style>
