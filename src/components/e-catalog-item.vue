<template>
	<div class="e-catalog-item">
		<p>item one</p>
		<p>Price: 100</p>
		<button>Pay</button>

	</div>
</template>

<script>
export default {
	name: 'e-catalog-item',
	props: {},
	data (){
		return{}
	},
	computed: {}
}
</script>
<style lang="scss">
$padding: 8px;
$margin: 8px;

$radius: 4px;

 .e-catalog-item{
	 flex-basis: 25%;
	 box-shadow: 0 0 8px 0 #e0e0e0;
	 padding: $padding*2;
	 margin-bottom: $margin*2;
 }

</style>