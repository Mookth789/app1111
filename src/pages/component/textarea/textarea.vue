<template>
	<view>
		<page-head :title="title"></page-head>
		<view class="uni-title uni-common-pl">พื้นที่อินพุตสามารถปรับได้สูงและไม่มีแถบเลื่อนปรากฏขึ้น</view>
		<view class="uni-textarea">
			<textarea @blur="bindTextAreaBlur" auto-height />
			</view>
			<view class="uni-title uni-common-pl">แบบอักษรตัวยึดเป็นพื้นที่ข้อความสีแดง</view>
			<view class="uni-textarea">
				<textarea placeholder-style="color:#F76260" placeholder="แบบอักษรตัวยึดเป็นสีแดง"/>
			</view>
		</view>
</template>
<script>
	export default {
		data() {
			return {
				title: 'textarea',
				focus: false
			}
		},
		methods: {
			bindTextAreaBlur: function (e) {
				console.log(e.detail.value)
			}
		}
	}
</script>

<style>
</style>
