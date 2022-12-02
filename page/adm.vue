<style scoped></style>

<template>
	<div class="container">
		<div class="admNav">
			<div class="admNav_pic" data-txt="變更頭像">
				<img src="" alt="" />
			</div>
			<div class="admNav_share msg_left" data-txtl="已分享食譜 ">0</div>
			<ul class="admNav_ul boxShadow">
				<li
					:class="['admNav_li', admNavState == 'm' ? 'on' : '']"
					@click="admNavHnadler('m')"
				>
					會員資料
				</li>
				<li
					:class="['admNav_li', admNavState == 'o' ? 'on' : '']"
					@click="admNavHnadler('o')"
				>
					訂單記錄
				</li>
				<li
					:class="['admNav_li', admNavState == 'r' ? 'on' : '']"
					@click="admNavHnadler('r')"
				>
					我的食譜
				</li>
				<li
					:class="['admNav_li', admNavState == 'c' ? 'on' : '']"
					@click="admNavHnadler('c')"
				>
					收藏
				</li>
			</ul>
		</div>
		<router-view></router-view>
	</div>
</template>

<script>
module.exports = {
	data() {
		return {
			icon_all: icon_all,
			admNavState: "m",
		};
	},
	components: {},
	mounted() {
		// console.log(store.state.nowPage);
	},

	computed: {},
	methods: {
		admNavHnadler(str) {
			this.admNavState = str;
			switch (str) {
				case "m":
					// this.$router.push("/adm");
					break;
				case "o":
					// this.$router.push("/order");
					break;
				case "r":
					// this.$router.push("/order");
					break;
				case "c":
					// this.$router.push("/order");
					break;
				default:
					break;
			}
		},
	},
};
</script>
