<template>
	<div>
		<h2 @click="showName">学校名称：{{name}}</h2>
		<h2>学校地址：{{address}}</h2>
	</div>
</template>

<script>
	//引入一个hunhe
	// import {hunhe,hunhe2} from '../mixin'
	//数据冲突时，以自身的为主，但是生命周期钩子是都会要的
	export default {
		name:'School',
		data() {
			return {
				name:'尚硅谷',
				address:'北京',
				x:666
			}
		},
		// mixins:[hunhe,hunhe2],
	}
</script>