<template>
	<view class="content">
		<view class="left">
			<view class="left-avatar">
				<img src="../../static/images/avatar.jpg" alt="">
			</view>
			<uni-icons custom-prefix="iconfont" type="icon-wechat_message-copy" :size="28" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-lianxiren" :size="28" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-shoucang" :size="28" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-wenjianjia" :size="28" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-pengyouquan" :size="28" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-hudiejie" :size="28" color="#a2a2a2"></uni-icons>
			<view style="flex-grow: 1;"></view>
			<view class="">333</view>
			<view class="">333</view>
			<view class="">333</view>
			<view class="">333</view>
		</view>
		<view class="middle">middle</view>
		<view class="right">right</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {}
		},
		onLoad() {

		},
		methods: {}
	}
</script>


<style lang="scss" scoped>
	page {
		height: 100%;
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.content {
		min-height: 625px;
		border: 1px solid #cdcdcd;
		box-shadow: 2px 2px 10px #cdcdcd;
		border-radius: 2px;
		display: flex;

		.left {
			width: 68px;
			background-color: #2e2e2e;

			display: flex;
			flex-direction: column;
			align-items: center;

			.left-avatar {
				margin-top: 45px;

				img {
					width: 44px;
					height: 44px;
					border-radius: 2px;
				}
			}

			.icon-wechat_message-copy,.icon-lianxiren,.icon-shoucang,.icon-wenjianjia,.icon-pengyouquan,.icon-hudiejie {
				margin-top: 20px;
				cursor: pointer;
			}
			.icon-wechat_message-copy:hover,
			.icon-lianxiren:hover,
			.icon-shoucang:hover,
			.icon-wenjianjia:hover,
			.icon-pengyouquan:hover,
			.icon-hudiejie:hover {
				color: #07c160;
				background-color: #07c160;
			}
			.icon-wechat_message-copy {
				margin-top: 30px;
			}
		}

		.middle {
			width: 312px;
		}

		.right {
			min-width: 500px;
		}
	}
</style>
