<style scoped></style>

<template>
    <div class="admInfo">
        <div class="admInfo_title">會員資料</div>
        <button class="normal_btn" @click="editMemberHandler">
            <i class="icon_pen" v-html="icon_all.pen"></i>
            修改會員資料
        </button>
        <div class="admInfo_body boxShadow">
            <table class="normal_tb">
                <tr>
                    <th>姓名</th>
                    <td>黃小明</td>
                </tr>
                <tr>
                    <th>性別</th>
                    <td>男</td>
                </tr>
                <tr>
                    <th>生日</th>
                    <td>1月1日</td>
                </tr>
                <tr>
                    <th>手機</th>
                    <td>0952123456</td>
                </tr>
                <tr>
                    <th>地址</th>
                    <td>台北市中山區</td>
                </tr>
                <tr>
                    <th>Email</th>
                    <td>retaerg@gmail.com</td>
                </tr>
            </table>
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
        editMemberHandler() {},
    },
};
</script>
