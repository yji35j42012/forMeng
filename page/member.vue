<style scoped></style>

<template>
	<div class="admInfo">
		<div class="admInfo_title">
			<span v-if="isEdit">修改會員資料</span>
			<span v-else>會員資料</span>
		</div>
		<button
			v-if="!isEdit"
			class="normal_btn"
			@click="editMemberHandler('edit')"
		>
			<i class="icon_pen" v-html="icon_all.pen"></i>
			修改會員資料
		</button>
		<div class="admInfo_body boxShadow">
			<table class="normal_tb">
				<tr>
					<th>姓名</th>
					<td>
						<input
							class="normal_tb_inp"
							type="text"
							value="黃小明"
							:disabled="!isEdit"
						/>
					</td>
				</tr>
				<tr v-if="isEdit" class="showEdit">
					<th>暱稱</th>
					<td>
						<input
							class="normal_tb_inp"
							type="text"
							value="小明"
							:disabled="!isEdit"
						/>
					</td>
				</tr>
				<tr>
					<th>性別</th>
					<td v-if="!isEdit">男</td>
					<td v-else class="showEdit">
						<label class="normal_radio">
							<input
								type="radio"
								name="gender_mode"
								value="credit"
							/>
							<span></span>
							男
						</label>
						<label class="normal_radio">
							<input
								type="radio"
								name="gender_mode"
								value="credit"
							/>
							<span></span>
							女
						</label>
					</td>
				</tr>
				<tr>
					<th>生日</th>
					<td>
						<label class="normal_select msg_right" data-txtr="月">
							<select :disabled="!isEdit">
								<option value="">1</option>
							</select>
							<i v-html="icon_all.select_arr"></i>
						</label>
						<label class="normal_select msg_right" data-txtr="月">
							<select :disabled="!isEdit">
								<option value="">1</option>
							</select>
							<i v-html="icon_all.select_arr"></i>
						</label>
					</td>
				</tr>
				<tr>
					<th>手機</th>
					<td>
						<input
							class="normal_tb_inp"
							type="text"
							value="0952123456"
							:disabled="!isEdit"
						/>
					</td>
				</tr>
				<tr>
					<th>地址</th>
					<td>
						<input
							class="normal_tb_inp"
							type="text"
							value="台北市中山區"
							:disabled="!isEdit"
						/>
					</td>
				</tr>
				<tr>
					<th>Email</th>
					<td>
						<input
							class="normal_tb_inp"
							type="text"
							value="retaerg@gmail.com"
							:disabled="!isEdit"
						/>
					</td>
				</tr>
				<tbody v-if="isEdit">
					<tr>
						<th>修改密碼</th>
						<td></td>
					</tr>
					<tr>
						<th>舊密碼</th>
						<td>
							<input class="normal_tb_inp" type="text" value="" />
						</td>
					</tr>
					<tr>
						<th>新密碼</th>
						<td>
							<input class="normal_tb_inp" type="text" value="" />
						</td>
					</tr>
					<tr>
						<th>確認新密碼</th>
						<td>
							<input class="normal_tb_inp" type="text" value="" />
						</td>
					</tr>
				</tbody>
			</table>
		</div>

		<button
			v-if="isEdit"
			class="normal_btn _submitEdit"
			@click="editMemberHandler('ok')"
		>
			儲存修改
		</button>
	</div>
</template>

<script>
module.exports = {
	data() {
		return {
			icon_all: icon_all,
			isEdit: false,
		};
	},
	components: {},
	mounted() {
		// console.log(store.state.nowPage);
	},
	computed: {},
	methods: {
		editMemberHandler(str) {
			if (str == "edit") {
				this.isEdit = true;
			} else if (str == "ok") {
				this.isEdit = false;
			}
		},
	},
};
</script>
