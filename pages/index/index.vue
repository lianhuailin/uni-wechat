<template>
	<view class="content">
		首页
	</view>
</template>

<script>
	export default {
		data() {
			return {
				qrcode: false,
				agent: false,
				agentOpen: false,
				agentArr: [{
					title: '关闭',
					open: false
				}, {
					title: '开启',
					open: true
				}],
				agentMore: false,
				showMoreBtn: true,
				logining: false,
			}
		},
		onLoad() {

		},
		methods: {
			changeLogin() {
				this.$data.qrcode = !this.$data.qrcode;
			},
			changeAgent() {
				this.$data.agent = !this.$data.agent;
			},
			openAgent(open) {
				if (open != this.$data.agentOpen) {
					this.$data.agentOpen = !this.$data.agentOpen;
				}
			},
			moreAgent() {
				this.$data.agentMore = true;
				this.$data.showMoreBtn = false;
			},
			gotoWechat() {
				window.open('https://filehelper.weixin.qq.com/?from=windows&type=recommend', '_blank');
			},
			agentLogin() {
				this.$data.agent = false;
				this.$data.agentMore = false;
				this.$data.showMoreBtn = true;
			},
			loginSuccess() {
				this.$data.logining = true;
				setTimeout(() => {
					uni.navigateTo({
						url: "../login/login",
					})
				}, 1200);
			}
		}
	}
</script>

<style lang="scss">
	page {
		height: 100%;
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.content {
		width: 350px;
		height: 475px;
		background-color: #ffffff;
		border: 1px solid #cdcdcd;
		box-shadow: 2px 2px 10px #cdcdcd;
		border-radius: 3px;

		display: flex;
		flex-direction: column;
	}

	.header {
		height: 34px;
		display: flex;
		align-items: center;
		justify-content: space-between;

		.wechat-title {
			font-size: 18px;
			color: $font-color;
			margin-left: 12px;
		}

		.wechat-title-right {

			.icon-close,
			.icon-shezhi,
			.icon-yonghu1 {
				height: 40px;
				width: 40px;

				padding: 10px 13px;
				cursor: pointer;
				margin: 0px;

				color: #7a7a7a !important;
			}

			.icon-shezhi:hover,
			.icon-yonghu1:hover {
				background-color: #e3e3e3;
			}

			.icon-close:hover {
				background-color: #fb7373;
			}
		}
	}

	.image-box {
		display: flex;
		align-items: center;

		.avatar {
			width: 100px;
			height: 100px;
			margin: 70px auto 0;
		}
	}

	.name-box {
		text-align: center;
		font-size: 26px;
		margin-top: 20px;
	}

	.login-box {
		margin-top: 70px;

		.btn-login {
			background-color: #07c160;
			color: #ffffff;
			width: 220px;
		}

		.btn-login:hover {
			background-color: #38cd7f;
		}
	}

	.logining-txt {
		font-size: 18px;
		color: #38cd7f;
		text-align: center;
		margin-top: 36px;
	}

	.logining-cancel-txt {
		font-size: 18px;
		color: #436895;
		text-align: center;
		margin-top: 140px;
		cursor: pointer;
	}

	.change-user-box {
		margin-top: 24px;
		color: #436895;
		font-size: 17px;

		.txt-middle {
			width: 2px;
			height: 16px;
			color: #f3f3f3;
			margin-left: 20px;
		}

		.txt-change-user,
		.txt-transport-file {
			cursor: pointer;
		}

		.txt-change-user {
			margin-left: 80px;
		}

		.txt-transport-file {
			margin-left: 20px;
		}
	}

	.scan-login-box {
		display: flex;
		flex-direction: column;
		align-items: center;

		.scan-title {
			color: #07c160;
			font-size: 26px;
			margin-top: 46px;
		}

		.qrcode {
			height: 180px;
			width: 180px;
			margin-top: 26px;
		}

		.txt-transport-file {
			color: #436895;
			font-size: 18px;
			cursor: pointer;
			margin-top: 80px;
		}
	}

	.agent-box {
		display: flex;
		flex-direction: column;
		align-items: center;
		color: $font-color;
		font-size: 18px;

		.agent-title {
			margin-top: 48px;
			color: #000000;
		}

		.agent-use {
			width: 100%;
			display: flex;
			font-size: 18px;
			margin-top: 40px;

			.agent-use-title {
				margin-left: 24px;
			}

			.agent-radio-box {
				radio {
					margin-left: 26px;
				}
			}
		}

		.agent-info {
			width: 100%;
			margin-top: 12px;

			.agent-info-address,
			.agent-info-port,
			.agent-info-user,
			.agent-info-pwd {
				display: flex;
				margin-top: 20px;
			}

			.input-address,
			.input-port,
			.input-user {
				border-bottom: 1px solid $font-color;
				height: 20px;
				line-height: 20px;
				margin-left: 10px;
			}

			.input-address:hover,
			.input-port:hover,
			.input-user:hover,
			.input-pwd:hover {
				background-color: #f5f5f5;
			}

			.txt-address,
			.txt-port,
			.txt-user,
			.txt-pwd {
				margin-left: 20px;
				width: 70px;
				text-align: justify;
			}

			.agent-more {
				color: #4395f8;
				text-align: right;
				width: 200px;
				margin: 20px auto 0;
				cursor: pointer;
			}
		}

		.agent-login {
			margin-top: 30px;

			button {
				background-color: #1aad19;
				color: #ffffff;
				border-radius: 1px;
				width: 170px;
			}

			button:hover {
				background-color: #129611;
			}
		}
	}
</style>
