<template>
<div id="anbieter">
<div id="anbieterbild">
<img :src="bild" width="50" />
</div>
<div id="anbietername">
{{anbietername}} 
<br>
<div id="anbieternameinfo">
{{anbieterbeschreibung}}
</div>
</div>
<div id="anbietertarif">
{{tarif}}
<br>
<div id="anbieternameinfo">
{{tarifbeschreibung}}
</div>
</div>
</div>

</template>

<script>
export default {
  props: {
    anbietername: String,
    anbieterbeschreibung: String,
    tarif: String,
    tarifbeschreibung: String,
    bild: String
  }
};
</script>


<style>

#anbieter{
display: grid;
grid-template-columns: 33% 33% 33%;
padding-top: 10px;
padding-bottom: 5px;
}

#anbietername{
font-weight: 1000;
font-size: 11px;
margin-top: 10px;
text-align: left;
}

#anbieternameinfo{
font-weight: 300;
font-size: 11px;
}

#anbietertarif{
font-weight: 1000;
font-size: 11px;
margin-top: 10px;
text-align: right;
margin-right: 10px;
}


</style>
