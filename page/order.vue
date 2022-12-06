<style scoped></style>

<template>
    <div class="admInfo">
        <div class="admInfo_title">訂單記錄</div>
        <div class="admInfo_body boxShadow _list">
            <table class="normal_tbList">
                <tr>
                    <th><span>訂購日期</span></th>
                    <th><span>訂單編號</span></th>
                    <th><span>訂單金額</span></th>
                    <th><span>訂單狀態</span></th>
                </tr>
                <tr>
                    <td>10/5</td>
                    <td>A34FER9870</td>
                    <td>1000</td>
                    <td>已付款</td>
                </tr>
                <tr>
                    <td>10/5</td>
                    <td>A34FER9870</td>
                    <td>1000</td>
                    <td>已付款</td>
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
