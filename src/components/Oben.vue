<template>
  <div id="oben">
    <div id="header">
      <div id="logo">
         <a href="index.html" style="text-decoration: none;">
        <img src="../assets/logo.png" width="20">
        </a>
      </div>
      <div id="rate">Rates</div>
      <div id="prize">5,01€</div>
    </div>
    <div id="überblick">
      <div id="services">Services</div>
      <div id="rates">Rates</div>
      </div>
    <div v-for="anbieter in anbieterList"><anbieter :anbietername="anbieter.anbietername" :tarif="anbieter.tarif" :tarifbeschreibung="anbieter.tarifbeschreibung"
    :anbieterbeschreibung="anbieter.anbieterbeschreibung" 
    :bild="anbieter.bild"/></div>
  <div id="fooder">
  <a href="index.html" style="text-decoration: none;">
  <img src="../assets/trips.png" width="90">
  </a>
  </div>
  </div>
</template>

<script>
import anbieter from "./anbieter.vue";
export default {
  props: {
    msg: String
  },
  components: {
    anbieter
  },
  data() {
    return{
    anbieterList: [
      { anbietername: "DB", anbieterbeschreibung: "Schienenverkehr", 
        tarif: "0,20€", tarifbeschreibung: "per kilometer", 
        bild: require('../assets/logo2.png')},
      { anbietername: "Car2Go", anbieterbeschreibung: "Carsharing",
        tarif: "0,19€", tarifbeschreibung: "per minute",
        bild: require('../assets/logo3.png')},
      { anbietername: "Flixbus", anbieterbeschreibung: "Fernbus",
        tarif: "0,05€", tarifbeschreibung: "per kilometer",
        bild: require('../assets/logo4.png')},
      { anbietername: "BlaBlaCar", anbieterbeschreibung: "Sharing",
        tarif: "0,05€", tarifbeschreibung: "per kilometer",
        bild: require('../assets/logo5.png')},
      { anbietername: "myTaxi", anbieterbeschreibung: "Chauffeur",
        tarif: "2,35€", tarifbeschreibung: "per kilometer",
        bild: require('../assets/logo6.png')}
    ]
  }
 }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
#oben {
  width: 265px;
  height: 70px;
  padding-top: 119px;
  margin: auto;
  z-index: 10;
}
#header {
  display: grid;
  grid-template-columns: 33% 33% 33%;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.2), 0 0px 0px 0 rgba(0, 0, 0, 0.19);
  margin-bottom: 10px;
}
#logo {
  margin-top: 10px;
  margin-bottom: 5px;
  margin-left: -30px;
}
#rate {
  font-size: 13px;
  font-weight: 1000;
  margin-top: 12px;
  margin-bottom: 5px;
}
#prize {
  font-size: 13px;
  font-weight: 1000;
  margin-top: 12px;
  text-align: right;
  margin-bottom: 5px;
  margin-right: 10px;
  color: #1673FF;
}

#überblick {
  display: grid;
  grid-template-columns: 25% 25%;
  margin-bottom: 5px;
  font-size: 13px;
}
#services{
margin-left: 20px;
}
#rates{
margin-left: 155px;
text-align: right;
}

#fooder {
margin-top: -20px;
float: right;
}


</style>
