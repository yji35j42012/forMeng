<style scoped></style>

<template>
    <div class="header">
        <div class="logo">
            <h1>
                <img class="logo_pc" src="./images/logo_pc.png" alt="" />
                <img class="logo_ph" src="./images/logo_ph.png" alt="" />
            </h1>
        </div>
        <button id="menu_btn" class="menu_btn" @click="menuHandler">
            <span></span>
        </button>
        <ul class="menu">
            <li class="menu_item">
                <router-link to="/">首頁</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/course">廚藝教室</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/recipe">節氣食補</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/">素食地圖</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/">相關文章</router-link>
            </li>
            <li class="menu_item">
                <router-link to="/car">
                    <i class="icon_car" v-html="icon_all.car"></i>
                </router-link>
                <router-link to="/">
                    <i class="icon_member" v-html="icon_all.member"></i>
                </router-link>
            </li>
        </ul>
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
    watch: {
        $route(to, from) {
            var menu_btn = document.querySelector("#menu_btn");
            menu_btn.classList.remove("on");
        },
    },
    methods: {
        menuHandler() {
            var menu_btn = document.querySelector("#menu_btn");
            if (menu_btn.classList.contains("on")) {
                menu_btn.classList.remove("on");
            } else {
                menu_btn.classList.add("on");
            }
        },
    },
};
</script>
