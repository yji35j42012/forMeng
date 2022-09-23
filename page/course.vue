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
            <div class="card_group">
                <div class="card" v-for="item in 2" :key="item">
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
                            <i class="icon_keep" v-html="icon_all.keep"></i>
                        </div>
                    </div>
                </div>
                <ul class="normal_page">
                    <li>1</li>
                    <li>2</li>
                    <li>3</li>
                </ul>
            </div>
            <div class="filter" @click="filterHnadler">
                <button class="filter_btn">
                    <i v-html="icon_all.filter"></i>
                </button>
                <div id="filter_box" class="filter_box">
                    <h2>條件篩選</h2>
                    <label class="normal_select">
                        <select>
                            <option value="">推薦排序</option>
                        </select>
                        <i v-html="icon_all.select_arr"></i>
                    </label>
                    <label class="normal_select">
                        <select>
                            <option value="">選擇課程日期</option>
                        </select>
                        <i v-html="icon_all.select_arr"></i>
                    </label>
                    <ul class="filter_group">
                        <li class="filter_group_title">素食分類</li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                全素
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                蛋素
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                五辛素
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                奶素
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                蛋奶素
                            </label>
                        </li>
                    </ul>
                    <ul class="filter_group">
                        <li class="filter_group_title">價格</li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                $800 以下
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                $800 ~ $1500
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                $1500 以上
                            </label>
                        </li>
                    </ul>
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
        filterHnadler() {
            var filter_box = document.querySelector("#filter_box");
            if (filter_box.classList.contains("on")) {
                filter_box.classList.remove("on");
            } else {
                filter_box.classList.add("on");
            }
        },
    },
};
</script>
