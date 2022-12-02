<style scoped></style>

<template>
    <div class="container">
        <div class="admNav">
            <div class="admNav_pic" data-txt="變更頭像">
                <img src="" alt="" />
            </div>
            <div class="admNav_share msg_left" data-txtl="已分享食譜 ">0</div>
            <ul class="admNav_ul boxShadow">
                <li class="admNav_li on">會員資料</li>
                <li class="admNav_li">訂單記錄</li>
                <li class="admNav_li">我的食譜</li>
                <li class="admNav_li">收藏</li>
            </ul>
        </div>
        <router-view></router-view>
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
