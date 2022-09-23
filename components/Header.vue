<style scoped></style>

<template>
    <div class="header">
        <div class="logo">
            <h1>
                <img class="logo_pc" src="./images/logo_pc.png" alt="" />
                <img class="logo_ph" src="./images/logo_ph.png" alt="" />
            </h1>
        </div>
        <button class="menu_btn" @click="menuHandler">
            <span></span>
        </button>
        <ul id="menu" class="menu">
            <li class="menu_item">
                <router-link to="/">首頁</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/course">廚藝教室</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/">節氣食補</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/">素食地圖</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/">相關文章</router-link>
            </li>
        </ul>
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
    methods: {
        menuHandler() {
            var menu = document.querySelector("#menu");
            if (menu.classList.contains("on")) {
                menu.classList.remove("on");
            } else {
                menu.classList.add("on");
            }
        },
    },
};
</script>
