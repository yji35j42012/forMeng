<style scoped></style>

<template>
    <div class="card boxShadow">
        <div class="card_pic">
            <img :src="course_obj.imgUrl" alt="" />
        </div>
        <div class="card_txt">
            <h2>{{ course_obj.courseName }}</h2>
            <p class="border">
                {{ course_obj.courseTxt }}
            </p>
            <div class="card_price">
                課程價格
                <span>${{ course_obj.coursePrice }}</span>
            </div>
            <ul class="card_time">
                <li>開課時間</li>
                <li>
                    {{ course_obj.courseStartTime }} <br />
                    {{ course_obj.courseEndTime }}
                </li>
            </ul>
            <div class="card_fun">
                <button class="normal_btn" @click="courseMore('123')">
                    了解更多
                </button>
                <i
                    :id="'icon_keep_' + course_obj.courseId"
                    :class="['icon_keep', course_obj.courseKeep ? 'on' : '']"
                    @click="keepHandler(course_obj.courseId)"
                    v-html="icon_all.keep"
                ></i>
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
    props: ["course_obj"],
    components: {},
    mounted() {
        // console.log(store.state.nowPage);
    },
    computed: {},
    methods: {
        courseMore(id) {
            this.$router.push("/course/" + id);
        },
        keepHandler(id) {
            this.$emit("changekeep", id);
        },
    },
};
</script>
