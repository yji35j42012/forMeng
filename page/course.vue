<style scoped></style>

<template>
    <div class="container">
        <div class="infoHead">
            <h1>廚藝教室</h1>
            <div class="infoHead_pic">
                <img src="../images/course/mascot_title.png" alt="" />
            </div>
        </div>
        <div class="infoBody">
            <div class="card">
                <div class="card_pic">
                    <img src="../images/course/course001-1.jpg" alt="" />
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
                        <button class="normal_btn">了解更多</button>
                    </div>
                </div>
            </div>
            <div class="filter">
                <h2>條件篩選</h2>
                <label class="normal_select">
                    <select>
                        <option value="">推薦排序</option>
                    </select>
                    <i>
                        <svg
                            width="17"
                            height="10"
                            viewBox="0 0 17 10"
                            fill="none"
                            xmlns="http://www.w3.org/2000/svg"
                        >
                            <path
                                d="M1.5 1.5L8.5 8.5L15.5 1.5"
                                stroke="#005F5F"
                                stroke-width="2.91667"
                                stroke-linecap="round"
                                stroke-linejoin="round"
                            />
                        </svg>
                    </i>
                </label>
                <label class="normal_select">
                    <select>
                        <option value="">選擇課程日期</option>
                    </select>
                    <i>
                        <svg
                            width="17"
                            height="10"
                            viewBox="0 0 17 10"
                            fill="none"
                            xmlns="http://www.w3.org/2000/svg"
                        >
                            <path
                                d="M1.5 1.5L8.5 8.5L15.5 1.5"
                                stroke="#005F5F"
                                stroke-width="2.91667"
                                stroke-linecap="round"
                                stroke-linejoin="round"
                            />
                        </svg>
                    </i>
                </label>
                <ul class="filter_group">
                    <li class="filter_group_title">素食分類</li>
                    <li>
                        <label class="normal_checkbox">
                            <input type="checkbox">
                            <span></span>
                            全素
                        </label>
                        <label class="normal_checkbox">
                            <input type="checkbox">
                            <span></span>
                            蛋素
                        </label>
                    </li>
                </ul>
                <ul class="filter_group">
                    <li class="filter_group_title">價格</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
module.exports = {
    data() {
        return {};
    },
    components: {},
    mounted() {
        // console.log(store.state.nowPage);
    },
    computed: {},
    methods: {},
};
</script>
