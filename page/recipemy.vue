<style scoped></style>

<template>
	<div class="admInfo">
		<div class="admInfo_title">我的食譜</div>
		<div class="admInfo_body">
			<div class="card_group">
				<div class="card boxShadow" v-for="item in 2" :key="item">
					<div class="card_pic">
						<img src="./images/recipe/recipe1.jpg" alt="" />
					</div>
					<div class="card_txt">
						<h2 data-txtby="by 史萊姆">
							木耳炒甜豆 (五辛素)
							<i
								class="icon_clock msg_right"
								data-txtr="10分"
								v-html="icon_all.clock"
							></i>
						</h2>
						<p>
							清甜的什錦蔬菜，吃得到滿滿營養！🥦相關食譜：「便當店清炒豌豆(五辛素)」、「便當店大黃瓜炒木耳(五辛素)」、「木耳炒雞蛋(五辛素)」、「九層塔炒茄子(五辛素)」、「素食炒三絲「便當店大黃瓜炒木耳(五辛素)」、「木耳炒雞蛋(五辛素)」、「九層塔炒茄子(五辛素)」、「素食炒三絲...
						</p>
						<div class="card_fun">
							<button
								class="normal_btn"
								@click="solartermsMore('123')"
							>
								了解更多
							</button>
							<i
								class="icon_recipe_pen"
								v-html="icon_all.recipe_pen"
							></i>
						</div>
					</div>
				</div>
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
