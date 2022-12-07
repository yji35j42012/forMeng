<style scoped></style>

<template>
	<div class="container">
		<ul class="step">
			<li
				class="step_item boxShadow msg_right on"
				data-txtr="確認訂單資訊"
			>
				<span></span>
			</li>
			<li class="step_item boxShadow msg_right" data-txtr="選擇付款方式">
				<span></span>
			</li>
			<li class="step_item boxShadow msg_right" data-txtr="確認結帳">
				<span></span>
			</li>
		</ul>
		<div class="car_group" v-if="show.check">
			<div class="car_item boxShadow" v-for="item in 5" :key="item">
				<div class="car_item_pic">
					<img src="./images/course/course001-1.jpg" alt="" />
				</div>
				<div class="car_item_info">
					<div class="detail">
						<h2>地瓜餅 (奶素)</h2>
						<p class="detail_time">課程時間</p>
						<p class="detail_date">10月21日(五) 19:00-21:00</p>
					</div>
					<div class="price">
						<div class="price_txt">價格</div>
						<div>$1,200</div>
					</div>
					<div class="cancel">
						<button class="normal_btn">取消品項</button>
						<i class="icon_close" v-html="icon_all.close"></i>
					</div>

					<i class="icon_keep" v-html="icon_all.keep"></i>
				</div>
			</div>
		</div>
		<div class="car_total" v-if="show.check">
			<button class="normal_btn">訂單總計 $3,600</button>
		</div>
		<div class="car_subscriber" v-if="show.subscriber">
			<div class="car_subscriber_list boxShadow">
				<div class="title">訂購人</div>
				<div class="info">
					<ul class="info_ul">
						<li class="info_li msg_left" data-txtl="姓名">
							<input type="text" value="姓名" />
						</li>
						<li class="info_li msg_left" data-txtl="聯絡電話">
							<input type="text" value="666777888" />
						</li>
						<li class="info_li msg_left" data-txtl="Email">
							<input type="text" value="aaa@gamil.com" />
						</li>
					</ul>
				</div>
			</div>
			<div class="car_subscriber_list boxShadow">
				<div class="title">付款方式</div>
				<div class="info _pay">
					<ul>
						<li>
							<label class="normal_radio">
								<input
									type="radio"
									name="pay_mode"
									v-model="show.pay_mode"
									value="credit"
								/>
								<span></span>
								信用卡一次付清
							</label>
						</li>
						<li>
							<label class="normal_radio">
								<input
									type="radio"
									name="pay_mode"
									v-model="show.pay_mode"
									value="atm"
								/>
								<span></span>
								ATM轉帳
							</label>
						</li>
						<li>
							<label class="normal_radio">
								<input
									type="radio"
									name="pay_mode"
									v-model="show.pay_mode"
									value="store"
								/>
								<span></span>
								超商代碼繳費
							</label>
						</li>
					</ul>
				</div>
			</div>
		</div>
		<div class="pay" v-if="show.pay_mode == 'credit'">
			<div class="pay_title">信用卡一次付清</div>
			<div class="pay_box boxShadow _credit">
				<div class="pay_box_title">信用卡卡號</div>
				<ul class="pay_box_ul">
					<li class="pay_box_li">
						<input type="text" class="credit_input" />
					</li>
					<li>-</li>
					<li class="pay_box_li">
						<input type="text" class="credit_input" />
					</li>
					<li>-</li>
					<li class="pay_box_li">
						<input type="text" class="credit_input" />
					</li>
					<li>-</li>
					<li class="pay_box_li">
						<input type="text" class="credit_input" />
					</li>
				</ul>
				<div class="pay_box_title">有效年月</div>
				<div class="pay_box_info">
					<label class="normal_select msg_right" data-txtr="月">
						<select>
							<option value="">1</option>
						</select>
						<i v-html="icon_all.select_arr"></i>
					</label>
					<span>月</span>
					<label class="normal_select msg_right" data-txtr="年">
						<select>
							<option value="">2015</option>
						</select>
						<i v-html="icon_all.select_arr"></i>
					</label>
					<span>年</span>
				</div>
				<div class="pay_box_title">背面末三碼</div>
				<div class="pay_box_info">
					<input type="text" class="credit_input" />
				</div>
				<div class="pay_box_pic">
					<img src="./images/card.jpg" alt="" />
				</div>
			</div>
		</div>
		<div class="pay" v-if="show.pay_mode == 'atm'">
			<div class="pay_title">ATM轉帳</div>
			<div class="pay_box boxShadow _atm">
				<div class="pay_box_tb">
					<table>
						<caption class="title">
							轉帳資料
						</caption>
						<tr>
							<th>銀行代碼：</th>
							<td width="100%">
								888熊齋銀行
							</td>
						</tr>
						<tr>
							<th>轉張帳號：</th>
							<td>1234567890123456(共16碼)</td>
						</tr>
						<tr>
							<th>轉帳金額：</th>
							<td>1,200</td>
						</tr>
						<tr class="limit_itme">
							<th>繳款期限：</th>
							<td>
								<!-- <div class="func"> -->
								2022年10月13日23分59前
								<button class="normal_btn">
									利用網路ATM繳款
								</button>
								<!-- </div> -->
							</td>
						</tr>
					</table>
				</div>
			</div>
		</div>
		<div class="pay" v-if="show.pay_mode == 'store'">
			<div class="pay_title">超商代碼繳費</div>
			<div class="pay_box boxShadow _store">
				<div class="pay_box_title">
					需自行至超商機台輸入代碼，產生繳費單後前往櫃檯繳費。
				</div>
				<div class="pay_box_radio">
					<div class="title">請選擇超商</div>
					<label class="normal_radio">
						<input type="radio" name="gender" />
						<span></span>
						<img class="seven1" src="./images/711-1.jpg" alt="" />
						<img class="seven2" src="./images/711-2.jpg" alt="" />
					</label>
					<label class="normal_radio">
						<input type="radio" name="gender" />
						<span></span>
						<img
							class="family"
							src="./images/familymart_logo.jpg"
							alt=""
						/>
						<img class="ok" src="./images/ok_logo.png" alt="" />
						<img
							class="hilife"
							src="./images/hilife_logo.png"
							alt=""
						/>
					</label>
				</div>
				<ul class="pay_box_note">
					<li>注意事項：</li>
					<li>
						超商代收-代碼的繳費期限為7天，請務必於期限內進行繳款。
					</li>
					<li>
						例：10/13的10:00分購買商品，繳費期限為7天，表示10/20的10:00分前您必須前往繳費。
					</li>
				</ul>
			</div>
		</div>
		<div class="car_func">
			<button class="normal_btn _white" @click="backBtn">
				{{ btn.whiteBtn }}
			</button>
			<button class="normal_btn" @click="checkBtn">
				{{ btn.greenBtn }}
			</button>
		</div>
	</div>
</template>

<script>
module.exports = {
	data() {
		return {
			show: {
				check: true,
				subscriber: false,
				pay_mode: null,
				credit: false,
				atm: false,
				store: false,
			},
			btn: {
				whiteBtn: "繼續購物",
				greenBtn: "確認訂單",
			},
			step: "check",
			pay_mode: "",
			icon_all: icon_all,
		};
	},
	components: {},
	mounted() {
		// console.log(store.state.nowPage);
	},
	computed: {},
	methods: {
		checkBtn() {
			console.log("checkBtn");
			if (this.step == "check") {
				console.log("checkBtn", this.step);
				this.show.subscriber = true;
				this.step = "subscriber";
			}
		},
		backBtn() {},
	},
};
</script>
