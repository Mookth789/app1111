<template>
	<view>
		<page-head :title="title"></page-head>
		<view class="uni-common-mt">
			<view class="uni-form-item uni-column">
				<view class="title">ส่วนประกอบของแบบฟอร์มอยู่ภายในฉลาก</view>
				<checkbox-group class="uni-list" @change="checkboxChange">
					<label class="uni-list-cell uni-list-cell-pd" v-for="item in checkboxItems" :key="item.name">
						<view>
							<checkbox :value="item.name" :checked="item.checked"></checkbox>
						</view>
						<view>{{item.value}}</view>
					</label>
				</checkbox-group>
			</view>

			<view class="uni-form-item uni-column">
				<view class="title">ฉลากใช้สำหรับเพื่อระบุส่วนประกอบของแบบฟอร์ม</view>
				<radio-group class="uni-list" @change="radioChange">
					<view class="uni-list-cell uni-list-cell-pd" v-for="(item,index) in radioItems" :key="index">
						<view>
							<radio :id="item.name" :value="item.name" :checked="item.checked"></radio>
						</view>
                        <label class="label-2-text" :for="item.name">
                            <text>{{item.value}}</text>
                        </label>
					</view>
				</radio-group>
			</view>

			<view class="uni-form-item uni-column">
				<view class="title">เมื่อมีหลายป้าย ให้เลือกป้ายแรก</view>
				<checkbox-group class="uni-list" @change="checkboxChange">
					<label class="label-3">
						<view class="uni-list-cell uni-list-cell-pd">
							<checkbox class="checkbox-3">ตัวเลือกที่1</checkbox>
						</view>
						<view class="uni-list-cell uni-list-cell-pd">
							<checkbox class="checkbox-3">ตัวเลือกที่2</checkbox>
						</view>
						<view class="uni-link uni-center" style="margin-top:20rpx;">คลิกข้อความใต้ป้ายกำกับเพื่อเลือกช่องทำเครื่องหมายแรกตามค่าเริ่มต้น</view>
					</label>
				</checkbox-group>
			</view>

		</view>
	</view>
</template>
<script>
	export default {
		data() {
			return {
				title: 'label',
				checkboxItems: [{
						name: 'USA',
						value: 'USA'
					},
					{
						name: 'CHN',
						value: 'CHN',
						checked: 'true'
					}
				],
				radioItems: [{
						name: 'USA',
						value: 'USA'
					},
					{
						name: 'CHN',
						value: 'CHN',
						checked: 'true'
					}
				],
				hidden: false
			}
		},
		methods: {
			checkboxChange: function(e) {
				var checked = e.detail.value
				console.log(checked)

			},
			radioChange: function(e) {
				var checked = e.detail.value
				console.log(checked)
			}
		}
	}
</script>

<style>
	.uni-list-cell {
		justify-content: flex-start
	}

	.uni-list .label-3 {
		padding: 0;
	}
    
    .label-2-text {
        flex: 1;
    }
</style>
