<template>
  <div class="e-catalog-item">
    <img class="e-catalog-item__image" :src="require ('../assets/images/' + product_data.image)" alt="" />
    <p class="e-catalog-item__name">{{product_data.name}}</p>
    <p class="e-catalog-item__price">Price: {{product_data.price}} р</p>
    <button 
		class="e-catalog-item__btn btn" 
		@click="sendDataToParent"
		>Add to cart
	</button>
  </div>
</template>

<script>
export default {
  name: "e-catalog-item",
  props: {
    product_data: {
      type: Object,
      default() {
        return {};
      }
    }
  },
  data() {
    return {};
  },
  computed: {},
  methods: {
	  sendDataToParent(){
		  // передаем в родителя по клику данные
		this.$emit( 'sendDataToParent', this.product_data.article)  
	  }
  }
};
</script>
<style lang="scss">
$padding: 8px;
$margin: 8px;

$radius: 4px;

.e-catalog-item {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 #e0e0e0;
  padding: $padding * 2;
  margin-bottom: $margin * 2;
  	&__image{
		  width: 100px;
	  }
}
</style>