<template>
  <layout>
    <layout-content>
      <a-button>Test Button</a-button>
      <a-form :colon="false" label-align="left">
        <a-form-item label="Trade Name">
          <a-input v-model:value="formState.tradeName"></a-input>
        </a-form-item>
        <date-picker
          v-model:value="formState.calendar"></date-picker>
        <a-select
          v-model:value="formState.pair"
          show-search
          placeholder="Select pair"
          style="width: 200px"
          :options="pairOptions"
        ></a-select>
        <a-select
          v-model:value="formState.position"
          style="width: 200px"
          show-search
          placeholder="Select position"
          :options="positionOptions"
          ></a-select>
        <a-input-number
          v-model:value="formState.proximal"
          style="width: 200px"
          placeholder="Proximal"
          string-mode
          ></a-input-number>
        <a-input-number
          v-model:value="formState.distal"
          style="width: 200px"
          placeholder="Distal"
          string-mode
          ></a-input-number>
        <div class="selectable-area">{{ entry }}</div>
        <div class="selectable-area">{{ stopLoss }}</div>
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
  Input,
  InputNumber,
  DatePicker,
  Select,
} from 'ant-design-vue';
import pairs from '@/constants/pairs'

export default {
  name: 'HomeView',
  components: {
    AButton: Button,
    AForm: Form,
    AFormItem: FormItem,
    AInput: Input,
    AInputNumber: InputNumber,
    ASelect: Select,
    DatePicker,
    Layout,
    LayoutContent
  },
  computed: {
    entry () {
      return 1234
    },
    stopLoss () {
      return 2345
    },
  },
  data () {
    return {
      formState: {
        tradeName: '',
        calendar: '',
        // pair: '',
        // position: '',
      },
      pairOptions: pairs,
      positionOptions: [
        {
          value: 'BUY',
          label: 'BUY'
        },
				{
					value: 'SELL',
					label: 'SELL'
				},
      ]
    }
  },
  methods: {
    handleChange: (value) => {
      console.log('Selected value', value)
    },
  },
}
</script>

<style>
.selectable-area {
  background-color: #fff;
  border: 1px solid #d9d9d9;
  border-radius: 2px;
  padding: 5px 11px;
}
</style>