<style scoped></style>

<template>
	<div class="container">
		<div class="infoHead">
			<div class="infoHead_detail">
				<h1>節氣食補</h1>
				<div class="car">
					<div class="car_box boxShadow">
						<div class="car_pic">
							<img src="../images/spring.png" alt="" />
						</div>
						<h2 class="car_title">
							大地回暖陽氣發,飲食宜清淡,少食辛辣的食物。
						</h2>
					</div>
				</div>
			</div>
			<div class="infoHead_pic">
				<img src="../images/solarterms.png" alt="" />
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
	methods: {},
};
</script>
