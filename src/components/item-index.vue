<template>
  <div class="container my-5">
    <div class="d-flex flex-wrap">
      <div v-for="item in items" :key="item.name">
        <item-card-vue :item="item"></item-card-vue>
      </div>
      
    </div>
  </div>
</template>

<script>
import {Item} from "@/module/item";
import itemCardVue from "./item-card.vue";

export default {
  name : 'item-index',
  components : {
    itemCardVue
  },
  data(){
    return{
      items : [
          new Item("Model 3", "Tesla", "$48,490", "2020-10-4", "model3"),
          new Item("Model X", "Tesla", "$89,990", "2017-08-08", "modelx"),
          new Item("Model Y", "Tesla", "$48,190", "2020-02-02", "modely"),
          new Item("Cayenne", "Porsche", "$67,500", "2017-12-20", "cayenne"),
          new Item("Macan", "Porsche", "$52,100", "2019-07-12", "macan"),
          new Item("Camry", "Toyota", "$24,425", "2015-06-29", "camry"),
          new Item("Accord", "Honda", "$24,800", "2018-10-02", "accord"),
          new Item("Civic", "Honda", "$20,650", "2015-04-04", "civic"),
          new Item("CX-5", "Mazda", "$26,940", "2012-11-03", "cx-5"),
          new Item("GLE Coupe-5", "Mercedes-Benz", "$76,500", "2020-02-05", "gle-coupe"),
          new Item("CLA", "Mercedes-Benz", "$37,850", "2019-06-09", "cla"),
          new Item("GLA 250", "Mercedes-Benz", "$37,280", "2017-05-02", "gla-250"),
          new Item("RX 350", "Lexus", "$45,175", "2015-01-01", "rx-350"),
          new Item("NX 300", "Lexus", "$37,510", "2018-09-12", "nx-300"),
          new Item("Urus", "Lamborghin", "$218,000", "2021-08-16", "urus"),
          new Item("Aventador", "Lamborghin", "$393,695", "2020-09-11", "aventador"),
          new Item("A3", "Audi", "$33,500", "2019-05-08", "a3"),
          new Item("X3", "BMW", "$43,000", "2018-03-11", "x3"),
          new Item("2 Series", "BMW", "$37,500", "2019-01-15", "2series"),
          
          
      ]
    }
  }
}
</script>