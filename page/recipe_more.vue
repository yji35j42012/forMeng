<style scoped></style>

<template>
    <div class="container">
        <div class="recipe_more boxShadow">
            <div class="recipe_more_title">
                木耳炒甜豆 (五辛素)
                <i class="icon_keep" v-html="icon_all.keep"></i>
            </div>
            <div class="recipe_more_pic">
                <div class="main">
                    <img src="./images/recipe/recipe1.jpg" alt="" />
                </div>
                <div class="season">
                    <img src="./images/spring.png" alt="" />
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
                <li data-txt="份量">3 人份</li>
                <li data-txt="時間">10 分鐘</li>
                <li class="ingredients">食材</li>
                <li data-txt="甜豌豆/荷蘭豆">
                    <span>一包</span>
                </li>
                <li data-txt="乾木耳/鮮木耳">
                    <span>3片</span>
                </li>
                <li data-txt="香菇素蠔油">
                    <span>½茶匙</span>
                </li>
                <li data-txt="香菇粉">
                    <span>少許</span>
                </li>
                <li data-txt="太白粉">
                    <span>¾茶匙</span>
                </li>
            </ul>
        </div>
        <div class="recipe_list boxShadow">
            <ul class="recipe_list_ul">
                <li class="recipe_list_li">
                    <div class="recipe_list_img">
                        <img src="./images/recipe/recipe1_1.jpg" alt="" />
                    </div>
                    <div class="recipe_list_txt">甜豆剝去纖維</div>
                </li>
                <li class="recipe_list_li">
                    <div class="recipe_list_img">
                        <img src="./images/recipe/recipe1_2.jpg" alt="" />
                    </div>
                    <div class="recipe_list_txt">木耳泡發後切小塊</div>
                </li>
            </ul>
        </div>
        <div class="recipe_message boxShadow">
            <div class="recipe_message_title">留言</div>
            <div class="recipe_message_img">
                <i class="icon_img" v-html="icon_all.img"></i>
            </div>
            <div class="recipe_message_txt">
                <textarea name="" id="" cols="30" rows="13"></textarea>
            </div>
            <div class="recipe_message_btnBox">
                <button class="normal_btn">發表留言</button>
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
