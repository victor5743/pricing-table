<template>
	<div class="mx-32 mt-16 sm:hidden">
		<div class="text-center border border-gray-400 text-">
			<div class="bg-gray-300 p-4">
				<div class="uppercase tracking-wide font-bold text-gray-700">Hobby</div>
				<div class="mt-3">
					<span class="text-lg">$</span>
					<span class="font-bold text-4xl ml-1">
						{{ !isMonthly ? plans.hobby.price.perYear : plans.hobby.price.perMonth }}
					</span>
					<span class="ml-2">/ month</span>
				</div>
				<div class="odd:bg-gray-200 even:bg-white flex px-3 py-4">
					<div class="text-left w-3/5">Shipping Discount</div>
					<div class="w-2/5">3</div>
				</div>
				<div class="odd:bg-gray-200 even:bg-white flex px-3 py-4">
					<div class="text-left w-3/5">Print Shipping Labels</div>
					<div class="w-2/5">5</div>
				</div>
				<div class="odd:bg-gray-200 even:bg-white flex px-3 py-4">
					<div class="text-left w-3/5">Same Day Delivery</div>
					<div class="w-2/5">1</div>
				</div>
				<div class="odd:bg-gray-200 even:bg-white px-3 py-4">
					<ul>
						<li class="flex items-center mb-4">
							<svg
								id="Capa_1"
								enable-background="new 0 0 515.556 515.556"
								height="18"
								viewBox="0 0 515.556 515.556"
								width="18"
								xmlns="http://www.w3.org/2000/svg"
							>
								<path
									d="m0 274.226 176.549 176.886 339.007-338.672-48.67-47.997-290.337 290-128.553-128.552z"
								/>
							</svg>
							<span class="ml-2">Free Custom Domain</span>
						</li>
						<li class="flex items-center mb-4">
							<svg
								id="Capa_1"
								enable-background="new 0 0 515.556 515.556"
								height="18"
								viewBox="0 0 515.556 515.556"
								width="18"
								xmlns="http://www.w3.org/2000/svg"
							>
								<path
									d="m0 274.226 176.549 176.886 339.007-338.672-48.67-47.997-290.337 290-128.553-128.552z"
								/>
							</svg>
							<span class="ml-2">SSL Security</span>
						</li>
						<li class="flex items-center mb-4">
							<svg
								id="Capa_1"
								enable-background="new 0 0 515.556 515.556"
								height="18"
								viewBox="0 0 515.556 515.556"
								width="18"
								xmlns="http://www.w3.org/2000/svg"
							>
								<path
									d="m0 274.226 176.549 176.886 339.007-338.672-48.67-47.997-290.337 290-128.553-128.552z"
								/>
							</svg>
							<span class="ml-2">Unlimited Bandwidth</span>
						</li>
						<li class="flex items-center">
							<svg
								id="Capa_1"
								enable-background="new 0 0 515.556 515.556"
								height="18"
								viewBox="0 0 515.556 515.556"
								width="18"
								xmlns="http://www.w3.org/2000/svg"
							>
								<path
									d="m0 274.226 176.549 176.886 339.007-338.672-48.67-47.997-290.337 290-128.553-128.552z"
								/>
							</svg>
							<span class="ml-2">SEO Features</span>
						</li>
					</ul>
				</div>
				<div class="odd:bg-gray-200 even:bg-white flex px-3 py-4">
					<div class="mx-auto">
						<a
							class="bg-blue-500 hover:bg-blue-700 text-white inline-block rounded w-64 px-4 py-2"
							href="#"
							>Sign Up</a
						>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			isMonthly: false,
			plans: {
				hobby: {
					price: {
						perYear: 15,
						perMonth: 20,
					},
				},
				growth: {
					price: {
						perYear: 25,
						perMonth: 30,
					},
				},
				business: {
					price: {
						perYear: 50,
						perMonth: 60,
					},
				},
				enterprise: {
					price: {
						perYear: 90,
						perMonth: 120,
					},
				},
			},
		};
	},
};
</script>
