<script setup>
defineProps(['siteTtl']);
</script>


<template>
    <div class="p-top-about">
        <div class="l-inner">
            <h2 class="c-head-border-left--bk">{{ siteTtl }}</h2>
            <p class="p-top-about__lead c-txt">
                {{ siteTtl }}は創業100年の老舗。甘みと苦みを活かしたお茶という理念を持っておりそれは今でも変わらず茶葉造りから選定など全てにおいてこだわりを持ちます。お客様に満足して頂くこと創業当時の味を守ることこの2点を大切にしております。是非、当店のお茶をご堪能下さい。
            </p>
        </div>
    </div>
</template>

<style>
.p-top-about {
    padding: 80px 0 30px;
    color: #4d391e;
}
.c-head-border-left--bk {
    position: relative;
    margin-bottom: clamp(20px, 6vw, 60px);
    padding-left: 65px;
    font-size: clamp(24px,4vw,40px);
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
    font-weight: 700;
    color: #4d391e;
}
.c-head-border-left--bk::before {
    width: 50px;
    background: #b49970;
}
.c-head-border-left--bk::after, .c-head-border-left--bk::before {
    content: "";
    position: absolute;
    top: 50%;
    left: 0;
    height: 2px;
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%);
}
.c-head-border-left--bk::after {
    width: 25px;
    background: #4d391e;
}
.c-head-border-left--bk::after, .c-head-border-left--bk::before {
    content: "";
    position: absolute;
    top: 50%;
    left: 0;
    height: 2px;
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%);
}
.p-top-about__lead {
    margin-bottom: clamp(20px, 4vw, 40px);
}
.c-txt {
    line-height: 2;
    font-size: clamp(14px,1.6vw,16px);
    /* font-size: 1.6rem; */
    font-family: 游ゴシック medium, yu gothic medium, 游ゴシック, yu gothic, メイリオ, meiryo, ヒラギノ角ゴ pro, hiragino kaku gothic pro, sans-serif;
    color: #000;
}
@media screen and (max-width: 640px) {
    .c-head-border-left--bk {
        padding-left: 40px;
    }
    .c-head-border-left--bk::before {
        width: 30px;
    }
    .c-head-border-left--bk::after {
        width: 15px;
    }
}
</style>