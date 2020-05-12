<template>
	<thead>
		<tr>
			<!-- Toggle Button -->
			<div>
				<th class="w-1/5 bg-gray-100 text-left align-top p-4">
					<span
						class="mr-2 text-sm font-semibold text-gray-500"
						:class="{ 'text-gray-700': !isMonthly }"
						>Annually</span
					>
					<toggle-button
						v-model="isMonthly"
						:value="false"
						color="#3183cd"
						:sync="false"
						:speed="200"
					/>
					<span
						class="ml-2 text-sm font-semibold text-gray-500"
						:class="{ 'text-gray-700': isMonthly }"
						>Monthly</span
					>
				</th>
			</div>
			<div class="text-blue-600 text-sm mt-4">
				Save up to 30% by paying anually.
			</div>
			<th class="thead">
				<Price :title="'Hobby'" :isMonthly="isMonthly" :plans="plans.hobby" />
			</th>
			<th class="thead">
				<Price :title="'Growth'" :isMonthly="isMonthly" :plans="plans.growth" />
			</th>
			<th class="thead">
				<Price :title="'Business'" :isMonthly="isMonthly" :plans="plans.business" />
			</th>
			<th class="thead">
				<Price :title="'Enterprise'" :isMonthly="isMonthly" :plans="plans.enterprise" />
			</th>
		</tr>
	</thead>
</template>

<script>
import Price from './Price';

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
	components: {
		Price,
	},
};
</script>
