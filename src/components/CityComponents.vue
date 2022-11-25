<script>
export default {
  name: "CityComponent",
  props:[
    "key",
    "name",
    "country_name",
    "country_code",
    "state_name",
    "state_code",
    "latitude",
    "longitude",
  ]
};
</script>
<template>

</template>
<style>
.city { 
  padding: 2px; 
  white-space: nowrap; 
  width: 350px; 
  height: 350px; 
  border-style: solid; 
  border-radius: 5px; 
  border-color: grey; 
} 
 
h1 { 
  overflow: hidden; 
  text-overflow: ellipsis; 
} 
</style>