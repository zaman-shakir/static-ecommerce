<script>
import Products from '$lib/components/products.json';
console.log(Products);
let price = 14.99;
</script>

<!--
<div class="flex flex-col md:flex-row gap-2 xl:gap-5">
	<a
		class="w-full  rounded-lg p-4 text-xl font-bold text-center  transition-all duration-300"
		href="/"
	>

		<div class="flex flex-col items-center">
            <img
			class="w-48 sm:w-56 lg:w-64 xl:w-72 rounded-lg shadow-lg h-[143px]"
			src="https://daisyui.com/images/stock/photo-1550258987-190a2d41a8ba.jpg"
			alt="Burger"
		    />
            <div class="mt-2">
                <div class="">
                    Product name - $99
                </div>
            </div>
            <div class="btn btn-active mt-2"> Add to Cart</div>
            </div>
	</a>

</div> -->
<!-- Links.svelte -->
<!-- <div class="flex flex-col md:flex-row gap-2 xl:gap-5"> -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-5">
        {#each Products.item.slice(0, 6) as product, index}
    <a
    class="w-full  rounded-lg p-4 text-xl font-bold text-center  transition-all duration-300"
    href="/"
    >

    <div class="flex flex-col items-center">
        <img
        class="w-48 sm:w-56 lg:w-64 xl:w-72 rounded-lg shadow-lg h-[143px]"
        src={product.image_link}
        alt="Burger"
        />
        <div class="mt-2">
            <div class="">
                {product.title} - ${price}
            </div>
        </div>
        <div class="btn btn-active mt-2"> Add to Cart</div>
        </div>
</a>
    {/each}
  </div>
