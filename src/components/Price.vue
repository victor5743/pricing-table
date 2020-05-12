<template>
	<div>
		<div class="uppercase tracking-wide font-bold text-gray-700">{{ title }}</div>
		<div class="mt-3">
			<span class="text-lg">$</span>
			<span class="font-bold text-4xl ml-1">
				{{ !isMonthly ? plans.price.perYear : plans.price.perMonth }}
			</span>
			<span class="ml-2 text-sm">/ month</span>
		</div>
		<div class="mt-3">
			<a
				class="bg-blue-500 hover:bg-blue-700 text-white inline-block rounded w-4/5 px-4 py-2"
				href="#"
				>Sign Up</a
			>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		title: String,
		price: Number,
		isMonthly: Boolean,
		plans: Object,
	},
};
</script>
