<template>
	<el-tabs type="border-card" class="demo-tabs">
		<el-tab-pane label="供应商查询">
			<vxe-table :column-config="{resizable: true}" border height="550" :data="tableData1">
				<vxe-column type="seq" title="序号" width="60"></vxe-column>
			 <vxe-column field="name" title="供应商名称" sortable></vxe-column>
				<vxe-column field="sex" title="地址"></vxe-column>
				<vxe-column field="age" title="联系方式"></vxe-column>
				<vxe-column field="address" title="备注" show-overflow></vxe-column>
			</vxe-table>
		</el-tab-pane>
		<el-tab-pane label="供应商录入">
			<supplieradd></supplieradd>
		</el-tab-pane>

	</el-tabs>


</template>

<script>
	import {
		defineComponent,
		ref
	} from 'vue'
	import supplieradd from './supplieradd.vue'
	export default defineComponent({
		components: {
			supplieradd
		}, //引入子组件
		setup() {
			const tableData1 = ref([{
					id: 10001,
					name: 'Test1',
					role: 'Develop',
					sex: 'Man',
					age: 28,
					address: 'test abc'
				},
				{
					id: 10002,
					name: 'Test2',
					role: 'Test',
					sex: 'Women',
					age: 22,
					address: 'Guangzhou'
				},
				{
					id: 10003,
					name: 'Test3',
					role: 'PM',
					sex: 'Man',
					age: 32,
					address: 'Shanghai'
				},
				{
					id: 10004,
					name: 'Test4',
					role: 'Designer',
					sex: 'Women',
					age: 23,
					address: 'test abc'
				},
				{
					id: 10005,
					name: 'Test5',
					role: 'Develop',
					sex: 'Women',
					age: 30,
					address: 'Shanghai'
				},
				{
					id: 10006,
					name: 'Test6',
					role: 'Designer',
					sex: 'Women',
					age: 21,
					address: 'test abc'
				},
				{
					id: 10007,
					name: 'Test7',
					role: 'Test',
					sex: 'Man',
					age: 29,
					address: 'test abc'
				},
				{
					id: 10008,
					name: 'Test8',
					role: 'Develop',
					sex: 'Man',
					age: 35,
					address: 'test abc'
				}
			])
			return {
				tableData1
			}
		}
	})
</script>

<style>
</style>
