<template>
	<div>
		<!-- Desktop table -->
		<table class="w-full hidden sm:block">
			<Thead />
			<Tbody />
		</table>

		<!-- Mobile table -->
		<MobileTable />
	</div>
</template>

<script>
import Thead from './Thead';
import Tbody from './Tbody';
import MobileTable from './MobileTable';

export default {
	components: {
		Thead,
		MobileTable,
		Tbody,
	},
};
</script>
