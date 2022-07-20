<template>
	<layout>
		<layout-content>
			<a-button>Test Button</a-button>
			<a-form :colon="false" label-align="left">
				<a-form-item label="Trade Name">
					<a-input v-model:value="formState.tradeName"></a-input>
				</a-form-item>
			</a-form>
		</layout-content>
	</layout>
</template>

<script>
import {
	Button,
	Layout,
	LayoutContent,
	Form,
	FormItem,
	Input
} from 'ant-design-vue';

export default {
  name: 'HomeView',
	components: {
		AButton: Button,
		AForm: Form,
		AFormItem: FormItem,
		AInput: Input,
		Layout,
		LayoutContent
	},
	data () {
		return {
			formState: {
				tradeName: ''
			},
		}
	}
}
</script>