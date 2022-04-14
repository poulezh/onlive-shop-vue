<template>
	<div class="e-catalog">
		<h1>Catalog</h1>
		<div class="e-catalog__list">
			<e-catalog-item />
		</div>

	</div>
</template>

<script>
import eCatalogItem from './e-catalog-item.vue'

export default {
	name: 'e-catalog',
	components:{
		eCatalogItem
	},
	props:{},
	data() {
		return{}
	},
	computed: {}
}
</script>
<style lang="scss">
.e-catalog{
	&__list{
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		align-items: center;
	}

}

</style>