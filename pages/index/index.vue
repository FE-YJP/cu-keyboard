<template>
	<view class="container">
		<button type="default" @click="open">打开支付键盘</button>
		{{value}}
		<cu-keyboard confirmText="付款" ref="cukeyboard" @change="change" @confirm="confirm" @hide="hide"></cu-keyboard>
	</view>
</template>

<script>
export default {
	data() {
		return {
			value:''
		}
	},
	mounted() {

	},
	methods: {
		change(e){
			this.value = e;
			console.log("数字改变",e);			
		},
		open(){
			console.log("打开键盘");
			this.$refs.cukeyboard.open();
		},
		confirm(e){
			console.log("付款",e);
		},
		hide(){
			console.log("关闭键盘")
		}
		
	}
}
</script>

<style>

</style>
