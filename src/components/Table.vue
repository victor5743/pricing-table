<template>
	<div>
		<table class="w-full">
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
						<Price
							:title="'Enterprise'"
							:isMonthly="isMonthly"
							:plans="plans.enterprise"
						/>
					</th>
				</tr>
			</thead>
			<tbody>
				<!-- First section -->
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Shipping Discount</td>
					<td class="trow text-center">$19</td>
					<td class="trow text-center">$29</td>
					<td class="trow text-center">$39</td>
					<td class="trow text-center">$49</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Print Shipping Labels</td>
					<td class="trow text-center">3</td>
					<td class="trow text-center">4</td>
					<td class="trow text-center">5</td>
					<td class="trow text-center">6</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Same Day Delivery</td>
					<td class="trow text-center">7</td>
					<td class="trow text-center">8</td>
					<td class="trow text-center">9</td>
					<td class="trow text-center">10</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Contributors</td>
					<td class="trow text-center">11</td>
					<td class="trow text-center">12</td>
					<td class="trow text-center">13</td>
					<td class="trow text-center">14</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">API Cslls</td>
					<td class="trow text-center">
						<p class="font-bold text-gray-900 text-lg">1,000 calls</p>
						<p class="text-xs">/month</p>
					</td>
					<td class="trow text-center">
						<p class="font-bold text-gray-900 text-lg">5,000 calls</p>
						<p class="text-xs">/month</p>
					</td>
					<td class="trow text-center">
						<p class="font-bold text-gray-900 text-lg">10,000 calls</p>
						<p class="text-xs">/month</p>
					</td>
					<td class="trow text-center">
						<p class="font-bold text-gray-900 text-lg">50,000 calls</p>
						<p class="text-xs">/month</p>
					</td>
				</tr>
				<!-- Separation -->
				<tr class="bg-gray-200 border border-gray-400">
					<td class="uppercase tracking-wide font-semibold px-4 py-6 text-left">
						Shipping
					</td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
				</tr>
				<!-- Second section -->
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Free Custom Domain</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">SSL Security</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Unlimited Bandwith and Storage</td>
					<td class="trow text-center"></td>
					<td class="trow text-center"></td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">SEO Features for Site Visibility</td>
					<td class="trow text-center"></td>
					<td class="trow text-center"></td>
					<td class="trow text-center"></td>
					<td class="trow text-center">
						<Checkmark />
					</td>
				</tr>
				<!-- Separation -->
				<tr class="bg-gray-200 border border-gray-400">
					<td class="uppercase tracking-wide font-semibold px-4 py-6 text-left">
						More Features
					</td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
				</tr>
				<!-- Third section -->
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Shipping Discount</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Print Shipping Labels</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Same Day Delivery</td>
					<td class="trow text-center"></td>
					<td class="trow text-center"></td>
					<td class="trow text-center">
						<Checkmark />
					</td>
					<td class="trow text-center">
						<Checkmark />
					</td>
				</tr>
				<tr class="even:bg-gray-300">
					<td class="trow text-left">Contributors</td>
					<td class="trow text-center"></td>
					<td class="trow text-center"></td>
					<td class="trow text-center"></td>
					<td class="trow text-center">
						<Checkmark />
					</td>
				</tr>
			</tbody>
		</table>
	</div>
</template>

<script>
import Price from './Price';
import Checkmark from './Checkmark';

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
		Checkmark,
	},
};
</script>
