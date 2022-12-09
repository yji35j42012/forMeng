<style scoped></style>

<template>
    <div class="admInfo">
        <div class="admInfo_body">
            <ul class="pageTab">
                <li class="pageTab_li on">
                    <button class="normal_btn">廚藝教室</button>
                </li>
                <li class="pageTab_li">
                    <button class="normal_btn">節氣食譜</button>
                </li>
                <li class="pageTab_li">
                    <button class="normal_btn">食譜</button>
                </li>
                <li class="pageTab_li">
                    <button class="normal_btn">地圖</button>
                </li>
                <li class="pageTab_li">
                    <button class="normal_btn">文章</button>
                </li>
            </ul>
            <div class="card_group">
                <coursecard
                    v-for="(item, index) in courseData"
                    :key="index"
                    :course_obj="item"
                    @changekeep="changeKeepHanlder"
                >
                </coursecard>
                <ul class="normal_page">
                    <li>1</li>
                    <li>2</li>
                    <li>3</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
module.exports = {
    data() {
        return {
            icon_all: icon_all,
            courseData: [
                {
                    courseId: "1",
                    imgUrl: "./images/course/course001-1.jpg",
                    courseName: "地瓜餅 (奶素)",
                    courseTxt:
                        "超級食物「地瓜」含有豐富的膳食纖維、β-胡蘿蔔素、鎂、鉀等營養素。製作成地瓜餅當早餐或點心都很適合...",
                    coursePrice: "1,200",
                    courseStartTime: "10月21日(五) 19:00-21:00",
                    courseEndTime: "11月18日(五) 19:00-21:00",
                    courseKeep: false,
                },
                {
                    courseId: "2",
                    imgUrl: "./images/course/course001-1.jpg",
                    courseName: "地瓜餅 (奶素)",
                    courseTxt:
                        "超級食物「地瓜」含有豐富的膳食纖維、β-胡蘿蔔素、鎂、鉀等營養素。製作成地瓜餅當早餐或點心都很適合...",
                    coursePrice: "1,200",
                    courseStartTime: "10月21日(五) 19:00-21:00",
                    courseEndTime: "11月18日(五) 19:00-21:00",
                    courseKeep: true,
                },
            ],
        };
    },
    components: {
        coursecard: httpVueLoader("../components/Course_card.vue"),
    },
    mounted() {
        // console.log(store.state.nowPage);
    },
    computed: {},
    methods: {
        editMemberHandler() {},
        changeKeepHanlder(id) {
            this.courseData.forEach((item) => {
                if (item.courseId == id) {
                    item.courseKeep = !item.courseKeep;
                    return;
                }
            });
        },
    },
};
</script>
