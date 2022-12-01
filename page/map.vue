<style scoped></style>

<template>
    <div class="container">
        <div class="infoHead">
            <h1>素食地圖</h1>
            <div class="infoHead_pic">
                <img src="../images/map/map_title.png" alt="" />
            </div>
            <div class="infoHead_filter">
                <label class="normal_select msg_top" data-txtt="Step1">
                    <select>
                        <option value="">選擇課程日期</option>
                    </select>
                    <i v-html="icon_all.select_arr"></i>
                </label>
                <label class="normal_select msg_top" data-txtt="Step2">
                    <select>
                        <option value="">選擇課程日期</option>
                    </select>
                    <i v-html="icon_all.select_arr"></i>
                </label>
                <label class="normal_select msg_top" data-txtt="Step3">
                    <select>
                        <option value="">選擇課程日期</option>
                    </select>
                    <i v-html="icon_all.select_arr"></i>
                </label>
            </div>
        </div>
        <div class="infoBody">
            <div class="card_group">
                <div class="card boxShadow">
                    <div class="card_pic">
                        <img src="../images/map/map1.jpg" alt="" />
                    </div>
                    <ul class="card_txt">
                        <h2>全國素食-大安復興店</h2>
                        <ul class="card_txt_ul">
                            <li class="msg_left" data-txtl="地址：">
                                台北市大安區復興南路二段314號
                            </li>
                            <li class="msg_left" data-txtl="營業時間：">
                                每日早上10：30～13：50，下午16：30～20：00
                            </li>
                            <li class="msg_left" data-txtl="電話：">
                                02-27361168
                            </li>
                            <li class="card_func">
                                <ul class="sort">
                                    <li class="sort_li">全素</li>
                                    <li class="sort_li">蛋素</li>
                                    <li class="sort_li">奶素</li>
                                </ul>
                                <button class="normal_btn">查看地圖</button>
                                <i class="icon_keep"
                                    ><svg
                                        width="25"
                                        height="32"
                                        viewBox="0 0 25 32"
                                        xmlns="http://www.w3.org/2000/svg"
                                    >
                                        <path
                                            d="M1.5 30V3.71875C1.5 2.21721 2.7312 1 4.25 1H20.75C22.2688 1 23.5 2.21721 23.5 3.71875V30L12.5 23.6562L1.5 30Z"
                                            stroke="#333333"
                                            stroke-width="2"
                                        ></path>
                                    </svg>
                                </i>
                            </li>
                        </ul>
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
    methods: {},
};
</script>
