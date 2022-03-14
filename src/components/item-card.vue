<template>
  <div class="card m-2" style="width: 18rem;">
    <div class="card-body">
      <img :src="imgSrc" class="card-img-top" />
      <h5 class="card-title pt-2">{{item.name}}</h5>
      <p class="card-text">Category: {{item.category}}</p>
      <p class="card-text">Price: {{item.price}}</p>
      <p class="card-text">Date: {{item.data}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "item-card",
  props: {
    item: Object,
  },
  computed: {
    imgSrc(){
      
      const img = "/img/" + this.item.img + ".jpg";
      return img;
    }
  }
};
</script>