<style scoped></style>

<template>
    <div class="container">
        <div class="infoHead">
            <h1>廚藝教室</h1>
            <div class="infoHead_pic">
                <img src="./images/course/mascot_title.png" alt="" />
            </div>
        </div>
        <div class="infoBody">
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
            <div class="filter">
                <button class="filter_btn" @click="filterHnadler">
                    <i v-html="icon_all.filter"></i>
                </button>
                <div id="filter_box" class="filter_box boxShadow">
                    <h2>條件篩選</h2>
                    <label class="normal_select">
                        <select>
                            <option value="">推薦排序</option>
                        </select>
                        <i v-html="icon_all.select_arr"></i>
                    </label>
                    <label class="normal_select">
                        <select>
                            <option value="">選擇課程日期</option>
                        </select>
                        <i v-html="icon_all.select_arr"></i>
                    </label>
                    <ul class="filter_group">
                        <li class="filter_group_title">素食分類</li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                全素
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                蛋素
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                五辛素
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                奶素
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                蛋奶素
                            </label>
                        </li>
                    </ul>
                    <ul class="filter_group">
                        <li class="filter_group_title">價格</li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                $800 以下
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                $800 ~ $1500
                            </label>
                        </li>
                        <li>
                            <label class="normal_checkbox">
                                <input type="checkbox" />
                                <span></span>
                                $1500 以上
                            </label>
                        </li>
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
        filterHnadler() {
            var filter_box = document.querySelector("#filter_box");
            if (filter_box.classList.contains("on")) {
                filter_box.classList.remove("on");
            } else {
                filter_box.classList.add("on");
            }
        },
        courseMore(id) {
            this.$router.push("/course/" + id);
        },
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
