<template>
	<view>
		<page-head :title="title"></page-head>
		<view class="uni-padding-wrap uni-common-mt">
			<view class="uni-title">แสดงvalueปัจจุบัน</view>
			<view>
				<slider value="50" @change="sliderChange" show-value />
			</view>
			
			<view class="uni-title">สเต็ปขั้นตอน</view>
			<view>
				<slider value="60" @change="sliderChange" step="5" />
			</view>

			<view class="uni-title">ตั้งต่ำสุด/สูงสุด</view>
			<view>
				<slider value="100" @change="sliderChange" min="50" max="200" show-value />
			</view>
			
			<view class="uni-title">แถบเลื่อนที่มีสีและขนาดต่างกัน</view>
			<view>
				<slider value="50" @change="sliderChange" activeColor="#FFCC33" backgroundColor="#000000" block-color="#8A6DE9" block-size="20" />
			</view>
		</view>
	</view>
</template>
<script>
	export default {
		data() {
			return {
				title: 'slider ตัวเลื่อน'
			}
		},
		methods: {
			sliderChange(e) {
				console.log('value chang：' + e.detail.value)
			}
		}
	}
</script>
