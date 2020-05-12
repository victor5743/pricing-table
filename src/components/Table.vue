<template>
	<div>
		<table class="w-full">
			<Thead />
			<Tbody />
		</table>
	</div>
</template>

<script>
import Thead from './Thead';
import Tbody from './Tbody';

export default {
	components: {
		Thead,
		Tbody,
	},
};
</script>
