<template lang="html">
    <div :class="[btnClass,cname]">
        <!--用插槽在标签里加文本-->
        <!--当使用btn标签时，标签里的有内容的话就会代替这里的插槽了，占空-->
        <slot/>
    </div>
</template>

<script>
export default {
    props: {
//        props 中的值提供一个带有验证需求的对象，
        cname: {
            type: String,
            default: "",
        },
    },
    data() {
        return {
            btnClass: "btn",
        }
    },
}
</script>

<style lang="scss">
@import "../../css/element.scss";
.btn{
  @include btn;
}
</style>
