<style scoped></style>

<template>
    <div class="container">
        <div class="recipe_more boxShadow">
            <div class="recipe_more_title">
                木耳炒甜豆 (五辛素)
                <i class="icon_keep" v-html="icon_all.keep"></i>
            </div>
            <div class="recipe_more_pic">
                <div class="menu">
                    <img src="../images/recipe/recipe1.jpg" alt="" />
                </div>
                <div class="season">
                    <img src="../images/spring.png" alt="" />
                </div>
            </div>
            <ul class="recipe_more_info">
                <li>清甜的什錦蔬菜，吃得到滿滿營養！</li>
                <li>
                    🥦相關食譜：「便當店清炒豌豆(五辛素)」、「便當店大黃瓜炒木耳(五辛素)」、「木耳炒雞蛋(五辛素)」、「九層塔炒茄子(五辛素)」、「素食炒三絲(五辛素)」、「清炒四季豆(五辛素)」
                </li>
            </ul>
        </div>
        <div class="recipe_detail boxShadow">
            <ul class="recipe_detail_ul">
                <li>
                    <div class="size">
                        份量 <br />
                        3 人份
                    </div>
                </li>
                <li>
                    時間<br />
                    10 分鐘
                </li>
            </ul>
        </div>
        <div class="recipe_list"></div>
        <div class="recipe_message"></div>
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
