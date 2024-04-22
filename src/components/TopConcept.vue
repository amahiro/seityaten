<script setup>

//画像のパス
import conceptImg from "@/assets/images/concept.png";

defineProps(['siteTtl']);

</script>
<template>
    <div class="p-top-concept">
        <figure class="p-top-concept__img">
            <img :src=conceptImg alt="苦みと甘さを活かした良質なお茶。" loading="lazy" width="950" height="550">
        </figure>
        <div class="l-inner">
            <div class="p-top-concept__cont">
                <div class="p-top-concept__ttl">
                    <h2>苦みと甘さを活かした良質なお茶、{{ siteTtl }}</h2>
                </div>
                <figure class="p-top-concept__img-sp">
                    <img :src=conceptImg alt="苦みと甘さを活かした良質なお茶。" loading="lazy" width="355" height="205">
                </figure>
                <p class="p-top-concept__txt">
                    {{ siteTtl }}は創業100年の老舗<br>
                    甘みと苦みを活かしたお茶という理念を持っており<br>
                    それは今でも変わらず茶葉造りから選定など<br>
                    全てにおいてこだわりを持ちます。<br>
                    お客様に満足して頂くこと創業当時の味を守ること<br>
                    この2点を大切にしております。<br>
                    是非、当店のお茶をご堪能下さい。
                </p>
            </div>
        </div>
    </div>
</template>


<style>
.p-top-concept {
    position: relative;
    padding-block: 60px;
}
.p-top-concept__img {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    width: min(50% - clamp(20px, 5vw, 50px), 950px);
}
.p-top-concept__img img {
    height: 100%;
    -o-object-fit: cover;
    object-fit: cover;
    -o-object-position: right;
    object-position: right;
}
.p-top-concept__cont {
    position: relative;
    margin-left: auto;
    max-width: 740px;
    z-index: 2;
}
.p-top-concept__ttl {
    position: relative;
    margin-bottom: clamp(30px, 4vw, 60px);
    z-index: 2;
    text-align: right;
}
.p-top-concept__ttl h2 {
    display: inline-block;
    padding: clamp(5px, 1vw, 10px) 26px;
    background: -webkit-gradient(linear, left top, right top, from(#b49970), to(#855915));
    background: linear-gradient(90deg, #b49970 0, #855915 100%);
    font-size: clamp(16px,3vw,36px);
    text-align: left;
    color: #fff;
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
    font-weight: 700;
}
.p-top-concept__img-sp {
    display: none;
}
.p-top-concept__txt {
    margin-left: auto;
    max-width: 500px;
    font-size: clamp(14px,2vw,20px);
    color: #4d391e;
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
    font-weight: 700;
    line-height: 2.2;
}
@media screen and (max-width: 640px) {
    .p-top-concept {
        padding-block: 0;
    }
    .p-top-concept__cont {
        max-width: none;
    }
    .p-top-concept__ttl {
        -webkit-transform: translateY(50%);
        transform: translateY(50%);
        margin-right: -20px;
        margin-bottom: 0;
    }
    .p-top-concept__ttl h2 {
        padding-inline: 10px;
    }
    .p-top-concept__img {
        display: none;
    }
    .p-top-concept__img-sp {
        display: block;
        width: calc(100% + 20px);
        margin-left: -20px;
        margin-bottom: 30px;
    }
}
</style>