<template>
	<div>
		<table class="w-full">
			<thead>
				<tr>
					<th class="w-1/5 bg-gray-200 text-center border border-gray-400 p-4">#</th>
					<th class="w-1/5 bg-gray-200 text-center border border-gray-400 p-4">
						<Price :title="'Hobby'" :price="15" />
					</th>
					<th class="w-1/5 bg-gray-200 text-center border border-gray-400 p-4">
						<Price :title="'Growth'" :price="25" />
					</th>
					<th class="w-1/5 bg-gray-200 text-center border border-gray-400 p-4">
						<Price :title="'Business'" :price="50" />
					</th>
					<th class="w-1/5 bg-gray-200 text-center border border-gray-400 p-4">
						<Price :title="'Enterprise'" :price="90" />
					</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<td>1</td>
					<td>John</td>
					<td>Smith</td>
					<td>jonh@smith.com</td>
					<td>Canada</td>
				</tr>
				<tr>
					<td>2</td>
					<td>Jane</td>
					<td>Doe</td>
					<td>jona@doe.com</td>
					<td>United States</td>
				</tr>
				<tr>
					<td>3</td>
					<td>Michael</td>
					<td>Scott</td>
					<td>michael@scott.com</td>
					<td>England</td>
				</tr>
			</tbody>
		</table>
	</div>
</template>

<script>
import Price from './Price';

export default {
	components: {
		Price,
	},
};
</script>
