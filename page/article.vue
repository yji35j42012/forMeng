<style scoped></style>

<template>
    <div class="container">
        <div class="infoHead">
            <h1>素食地圖</h1>
            <div class="infoHead_pic">
                <img src="./images/article/article_title.png" alt="" />
            </div>
            <ul class="infoHead_tab">
                <li class="infoHead_tab_li on">
                    <button class="normal_btn">食譜</button>
                </li>
                <li class="infoHead_tab_li">
                    <button class="normal_btn">文章</button>
                </li>
            </ul>
            <div class="infoHead_filter">
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
                <button class="normal_btn">
                    <i class="icon_pen" v-html="icon_all.pen"></i>
                    寫食譜
                </button>
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
    methods: {},
};
</script>
