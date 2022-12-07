<style scoped></style>

<template>
	<div class="admInfo">
		<div class="admInfo_body">
			<ul class="pageTab">
				<li class="pageTab_li on">
					<button class="normal_btn">廚藝教室</button>
				</li>
				<li class="pageTab_li">
					<button class="normal_btn">節氣食譜</button>
				</li>
				<li class="pageTab_li">
					<button class="normal_btn">食譜</button>
				</li>
				<li class="pageTab_li">
					<button class="normal_btn">地圖</button>
				</li>
				<li class="pageTab_li">
					<button class="normal_btn">文章</button>
				</li>
			</ul>
			<div class="card_group">
				<div
					class="card boxShadow"
					v-for="(item, index) in 2"
					:key="index"
				>
					<div class="card_pic">
						<img src="./images/course/course001-1.jpg" alt="" />
					</div>
					<div class="card_txt">
						<h2>地瓜餅 (奶素)</h2>
						<p class="border">
							超級食物「地瓜」含有豐富的膳食纖維、β-胡蘿蔔素、鎂、鉀等營養素。製作成地瓜餅當早餐或點心都很適合...
						</p>
						<div class="card_price">
							課程價格
							<span>$1,200</span>
						</div>
						<ul class="card_time">
							<li>開課時間</li>
							<li>
								10月21日(五) 19:00-21:00 <br />
								11月18日(五) 19:00-21:00
							</li>
						</ul>
						<div class="card_fun">
							<button
								class="normal_btn"
								@click="courseMore('123')"
							>
								了解更多
							</button>
							<i
								:id="'icon_keep_' + index"
								class="icon_keep"
								@click="keepHandler(index)"
								v-html="icon_all.keep"
							></i>
						</div>
					</div>
				</div>
				<ul class="normal_page">
					<li>1</li>
					<li>2</li>
					<li>3</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
module.exports = {
	data() {
		return {
			icon_all: icon_all,
		};
	},
	components: {},
	mounted() {
		// console.log(store.state.nowPage);
	},
	computed: {},
	methods: {
		editMemberHandler() {},
	},
};
</script>
