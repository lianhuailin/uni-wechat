<template>
	<view class="content">
		<view class="left">
			<view class="left-avatar">
				<img src="../../static/images/avatar.jpg" alt="">
			</view>
			<uni-icons custom-prefix="iconfont" type="icon-wechat_message-copy" :size="26" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-lianxiren" :size="26" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-shoucang" :size="26" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-wenjianjia" :size="26" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-pengyouquan" :size="26" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-hudiejie" :size="26" color="#a2a2a2"></uni-icons>
			<view style="flex-grow: 1;"></view>
			<uni-icons custom-prefix="iconfont" type="icon-xiaochengxu" :size="26" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-shouji" :size="26" color="#a2a2a2"></uni-icons>
			<uni-icons custom-prefix="iconfont" type="icon-liebiao" :size="26" color="#a2a2a2"></uni-icons>
		</view>
		<view class="middle">
			<view class="header">
				<view class="search-box">
					<uni-icons class="search-icon" type="search" :size="22"></uni-icons>
					<input class="search-input" type="text" value="" placeholder="搜索" />
				</view>
				<uni-icons class="icon-btn-add" type="plusempty" :size="24"></uni-icons>
			</view>
			<view class="contacts-list">
				<view class="contacts-box" v-for="(item, inde) in contactsList">
					<view class="contacts-img">
						<image src="../../static/images/avatar.jpg"></image>
					</view>
					<view class="contacts-info">
						<view class="contacts-name">移动app外包群</view>
						<view class="contacts-content">王志伟：@李春生-php开发工程师 刚才统计一下BUG表：红色：验证不通过</view>
					</view>
					<view class="contacts-time-info">
						<view class="time">14:12</view>
						<view class="clock">
							<uni-icons custom-prefix="iconfont" type="icon-guanbishengyin" :size="14" color="#bbbbbb"></uni-icons>
						</view>
					</view>
				</view>
			</view>
		</view>
		<view class="right">right</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				contactsList: [{

				}, {

				}, {

				}, {

				}, {

				}, {

				}, {

				}, {

				}, {

				}, {

				}, {

				}],
			}
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

			.icon-wechat_message-copy,
			.icon-lianxiren,
			.icon-shoucang,
			.icon-wenjianjia,
			.icon-pengyouquan,
			.icon-hudiejie {
				margin-top: 20px;
				cursor: pointer;
			}

			.icon-wechat_message-copy:hover,
			.icon-lianxiren:hover,
			.icon-shoucang:hover,
			.icon-wenjianjia:hover,
			.icon-pengyouquan:hover,
			.icon-hudiejie:hover,
			.icon-xiaochengxu:hover,
			.icon-shouji:hover,
			.icon-liebiao:hover {
				color: #07c160 !important;
			}

			.icon-wechat_message-copy {
				margin-top: 30px;
			}

			.icon-xiaochengxu,
			.icon-shouji,
			.icon-liebiao {
				margin-bottom: 20px;
				cursor: pointer;
			}
		}

		.middle {
			width: 312px;
			border-right: 1px solid #cdcdcd;

			.header {
				display: flex;
				margin-top: 32px;
				align-items: center;
				padding-bottom: 15px;

				.search-box {
					display: flex;
					justify-content: center;
					background-color: #e2e2e2;
					border-radius: 8px;
					padding: 4px 4px;
					width: 100%;
					margin-right: 10px;
					margin: 0 15px;

					.search-icon {
						margin: 0 2px;
					}

					.search-input {
						width: 100%;
					}
				}

				.icon-btn-add {
					background-color: #e2e2e2;
					padding: 3px;
					border-radius: 4px;
					color: #616161 !important;
					margin-right: 15px;
					cursor: pointer;
				}

				.icon-btn-add:hover {
					background-color: #d1d1d1;
				}
			}

			.contacts-list {
				max-height: 548px;
				overflow-y: scroll;

				.contacts-box {
					height: 80px;
					display: flex;
					background-color: #f5f5f5;

					.contacts-img {
						margin-top: 18px;
						image {
							height: 44px;
							width: 44px;
							margin: 0 14px 0 16px;
						}
					}

					.contacts-info {
						display: flex;
						flex-direction: column;
						width: 100%;
						white-space: nowrap;
						text-overflow: ellipsis;
						word-break: break-all;
						overflow: hidden;

						.contacts-name {
							margin-top: 16px;
							font-size: 18px;
						}

						.contacts-content {
							font-size: 12px;
							color: #999999;
							margin-top: 8px;
						}
					}

					.contacts-time-info {
						display: flex;
						flex-direction: column;
						width: 54px;
						margin: 0 10px;
						color: #999999;
						
						.time {
							font-size: 14px;
							margin-top: 18px;
						}
						
						.clock {
							text-align: right;
							margin-top: 8px;
						}
					}
				}

				.contacts-box:hover {
					background-color: #d8d8d8;
				}
			}

			.contacts-list::-webkit-scrollbar {
				/*隐藏滚轮*/
				display: none;
			}
		}

		.right {
			min-width: 500px;
		}
	}
</style>
