<script lang="ts">
	import { enhance, type SubmitFunction } from '$app/forms';
	import { page } from '$app/stores';
	import '$lib/app.css';
	import Drawer from './Drawer.svelte';

	const submitUpdateTheme: SubmitFunction = ({ action }) => {
		const theme = action.searchParams.get('theme');

		if (theme) {
			document.documentElement.setAttribute('data-theme', theme);
		}
	};

	const themes = [
		'light',
		'dark',
		'cupcake',
		'bumblebee',
		'emerald',
		'corporate',
		'synthwave',
		'retro',
		'cyberpunk',
		'valentine',
		'halloween',
		'garden',
		'forest',
		'aqua',
		'lofi',
		'pastel',
		'fantasy',
		'wireframe',
		'black',
		'luxury',
		'dracula',
		'cmyk',
		'autumn',
		'business',
		'acid',
		'lemonade',
		'night',
		'coffee',
		'winter'
	];
</script>

<div class="bg-base-100 sticky top-0 shadow-lg z-40">
    <div class="flex items-center justify-center py-5 border-b-2 border-black-500">
        <div class="">
            <p class="text-center">Shop digital gift cards for every occasion.</p>

        </div>
    </div>
	<div class="flex items-center justify-between p-2 lg:container lg:mx-auto">
		<div class="">

			<a href="/" class="font-bold text-primary text-xl"><img fetchpriority="high" src="https://wpdemo.triple-a.io/wp-content/uploads/2022/10/crypto-dark.svg" class="logo dark-logo w-250 h-30" alt="CryptoGiftCards">
            </a>
		</div>
		<div class="">
			<a href="/" style="margin-left:-60px" class="font-bold text-primary text-xl">Shop</a>
		</div>

		<div  class="">

			<!-- <div class="dropdown dropdown-hover dropdown-end">
				<label class="btn">Theme</label>
				<ul tabindex="0" class="dropdown-content menu p-2 shadow bg-base-100 h-96 overflow-scroll">
					<form method="POST" use:enhance={submitUpdateTheme}>
						{#each themes as theme}
							<li>
								<button formaction="/?/setTheme&theme={theme}&redirectTo={$page.url.pathname}"
									>{theme}</button
								>
							</li>
						{/each}
					</form>
				</ul>
			</div> -->
            <label class="btn btn-primary">My Account</label>
            <a href="/cart"><label  class="btn btn-primary">Cart</label></a>

		</div>
	</div>
</div>
