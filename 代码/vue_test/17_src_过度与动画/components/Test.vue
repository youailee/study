<template>
	<div>
		<button @click="isShow = !isShow">显示/隐藏</button>
		<!-- 实现动画效果可以用transition标签，最后不会出现在dom节点上，需要指定特定的类名值才可以使用，这个标签是vue里面的，保证元素发生变化时给你加上动画效果，如果有name属性，需要把对应的样式名v修改为name名字 -->
		<transition name="hello" appear>
			<h1 v-show="isShow">你好啊！</h1>
		</transition>
	</div>
</template>

<script>
	export default {
		name:'Test',
		data() {
			return {
				isShow:true
			}
		},
	}
</script>

<style scoped>
	h1{
		background-color: orange;
	}

	.hello-enter-active{
		animation: atguigu 0.5s linear;
	}

	.hello-leave-active{
		animation: atguigu 0.5s linear reverse;
	}

	@keyframes atguigu {
		from{
			transform: translateX(-100%);
		}
		to{
			transform: translateX(0px);
		}
	}
</style>