<style scoped></style>

<template>
	<div class="container">
		<div class="infoHead">
			<div class="infoHead_detail">
				<h1>節氣食補</h1>
				<div class="car">
					<div class="car_box boxShadow">
						<div class="car_pic">
							<img src="./images/spring.png" alt="" />
							<map name="ImageMap03">
								<area shape="polygon" coords="34,44,270,350" href="#" alt="">
							</map>
						</div>
						<h2 class="car_title">
							大地回暖陽氣發,飲食宜清淡,少食辛辣的食物。
						</h2>
					</div>
				</div>
			</div>
			<div class="infoHead_pic">
				<img src="./images/recipe.png" alt="" />
			</div>
			<div class="infoHead_filter">
				<div class="normal_search">
					<input type="text" placeholder="搜尋食譜" />
					<button class="normal_search_btn">
						<i class="icon_search" v-html="icon_all.search"></i>
					</button>
				</div>
				<label class="normal_select">
					<select>
						<option value="">季節分類</option>
					</select>
					<i v-html="icon_all.select_arr"></i>
				</label>
				<label class="normal_select">
					<select>
						<option value="">節氣分類</option>
					</select>
					<i v-html="icon_all.select_arr"></i>
				</label>
				<label class="normal_select">
					<select>
						<option value="">素食分類</option>
					</select>
					<i v-html="icon_all.select_arr"></i>
				</label>
				<label class="normal_select">
					<select>
						<option value="">烹飪時間</option>
					</select>
					<i v-html="icon_all.select_arr"></i>
				</label>
			</div>
		</div>
		<div class="infoBody">
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
							<i class="icon_keep" v-html="icon_all.keep"></i>
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
		solartermsMore(id) {
			this.$router.push("/recipe/" + id);
		},
	},
};
</script>
