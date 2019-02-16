<template>
<div id="oben">
<div id="header">
<div id="logo">
<img src="../assets/logo.jpeg" width="50">
</div>
<div id="noti">
Du bist eingestiegen!
</div>
</div>
<a href="index.html" style="text-decoration: none;"> <banner/>
</a>
<anbieter anbieter_name="Test" tarif="test2"/>



</div>
</template>

<script>
import banner from "./banner.vue";
import anbieter from "./anbieter.vue";
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: {
    banner,
    anbieter
  }
  
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
#oben{
width: 260px;
height: 70px;
padding-top: 150px;
margin: auto;
z-index: 10;
}
#header{
display: grid;
grid-template-columns: 50% 50%;
padding-bottom: 20px;
}
#logo{
padding: -50px;
}
#noti{
width: 100px;
height: 50px;
border-style: solid;
border-color: black;
}
#anbieter{
margin-top: 10px; 
height: 50px;
border-bottom: solid black;
}
</style>
