<template>
	<layout>
		<layout-content>
			<a-button>Test Button</a-button>
		</layout-content>
	</layout>
</template>

<script>
import { Button, Layout, LayoutContent } from 'ant-design-vue';

export default {
  name: 'HomeView',
	components: {
		AButton: Button,
		Layout,
		LayoutContent
	}
}
</script>
