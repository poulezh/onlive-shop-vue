<template>
  <div class="e-catalog">
    <h1>Catalog</h1>
    <div class="e-catalog__list">
      <e-catalog-item 
	  	v-for="product in products"
		:key="product.article"
		v-bind:product_data="product"
		@sendDataToParent="showChildArticleControle"
	  />
    </div>
  </div>
</template>

<script>
import eCatalogItem from "./e-catalog-item.vue";

export default {
  name: "e-catalog",
  components: {
    eCatalogItem,
  },
  props: {},
  data() {
    return {
      products: [
        {
          image: "1.jpg",
          name: "T-shirt 1",
          price: 111,
          article: "T1",
          available: true,
          category: "Мужские",
        },
        {
          image: "2.jpg",
          name: "T-shirt 2",
          price: 222,
          article: "T2",
          available: true,
          category: "Женские",
        },
        {
          image: "3.jpg",
          name: "T-shirt 3",
          price: 333,
          article: "T3",
          available: false,
          category: "Женские",
        },
        {
          image: "4.jpg",
          name: "T-shirt 4",
          price: 444,
          article: "T4",
          available: true,
          category: "Мужские",
        },
        {
          image: "5.jpg",
          name: "T-shirt 5",
          price: 555,
          article: "T5",
          available: false,
          category: "Женские",
        },
        {
          image: "6.jpeg",
          name: "T-shirt 6",
          price: 666,
          article: "T6",
          available: true,
          category: "Женские",
        },
      ],
    };
  },
  computed: {},
  methods:{
	  showChildArticleControle(data){
		  console.log(data);
	  }

  }
};
</script>
<style lang="scss">
.e-catalog {
  &__list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
  }
}
</style>