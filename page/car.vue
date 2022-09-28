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
        <div class="car_group">
            <div class="car_item boxShadow" v-for="item in 5" :key="item">
                <div class="car_item_pic">
                    <img src="../images/course/course001-1.jpg" alt="" />
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
        <div class="car_total">
            <button class="normal_btn">訂單總計 $3,600</button>
        </div>
        <div class="car_subscriber">
            <div class="car_subscriber_list boxShadow">
                <div class="title">訂購人</div>
                <div class="info">
					<ul class="info_ul">
						<li class="info_li msg_left" data-txtl="姓名">
							<input type="text" value="姓名">
						</li>
						<li class="info_li msg_left" data-txtl="聯絡電話">
							<input type="text" value="666777888">
						</li>
						<li class="info_li msg_left" data-txtl="Email">
							<input type="text" value="aaa@gamil.com">
						</li>
					</ul>
				</div>
            </div>
            <div class="car_subscriber_list boxShadow">
                <div class="title">付款方式</div>
                <div class="info"></div>
            </div>
        </div>

        <div class="car_func">
            <button class="normal_btn _white">繼續購物</button>
            <button class="normal_btn">確認訂單</button>
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
