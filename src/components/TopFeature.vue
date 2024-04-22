<script setup>
// import { ref } from 'vue';
//画像のパス
import feature1 from "@/assets/images/feature01.jpg";
import feature2 from "@/assets/images/feature02.jpg";
import feature3 from "@/assets/images/feature03.jpg";

defineProps(['siteTtl']);


</script>

<template>
    <ul class="p-topfeature">
        <li>
            <div class="p-topfeature__img">
                <img :src=feature1 alt="">
            </div>
            <div class="l-inner">
                <div class="p-topfeature__cont">
                    <h3>良質な茶葉</h3>
                    <p>
                        私たちの暮らしのそばにはいつもお茶がありました。<br>
                        お茶は家庭に癒しを与えてくれます。<br>
                        そんなお茶をさらに美味しく飲んで頂きたい<br>
                        その思いから生まれた茶葉です。<br>
                        どうぞお召し上がりください。
                    </p>
                </div>
            </div>
        </li>
        <li>
            <div class="p-topfeature__img">
                <img :src=feature2 alt="">
            </div>
            <div class="l-inner">
                <div class="p-topfeature__cont">
                    <h3>スイーツ</h3>
                    <p>
                        創業１００年の味わい、それがスイーツになりました。<br>
                        程よい甘さからほろ苦いものまで<br>
                        {{ siteTtl }}のスイーツ是非、ご堪能下さい。
                    </p>
                </div>
            </div>
        </li>
        <li>
            <div class="p-topfeature__img">
                <img :src=feature3 alt="">
            </div>
            <div class="l-inner">
                <div class="p-topfeature__cont">
                    <h3>贈り物</h3>
                    <p>
                        大切な方へ、日々の感謝を込めて<br>
                        あなたの想いと気遣いを贈り物と一緒に届けたい<br>
                        その思いをここに込めました。
                    </p>
                </div>
            </div>
        </li>
    </ul>
</template>

<style>
.p-topfeature {
    padding: 0;
}

.p-topfeature li {
    position: relative;
}

.p-topfeature li+li {
    margin-top: clamp(40px, 8vw, 80px);
}

.p-topfeature__cont {
    padding-block: 60px;
    width: 50%;
    margin-right: auto;
    padding-right: 60px;
    padding-left: 15px;
}

.p-topfeature__cont h3 {
    font-size: clamp(20px, 2.6vw, 36px);
    font-weight: 600;
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
}

.p-topfeature__cont p {
    margin-top: clamp(20px, 3vw, 30px);
    font-size: clamp(14px, 1.6vw, 16px);
    counter-reset: #000000;
}

.p-topfeature__img {
    position: absolute;
    top: 0;
    left: 50%;
    right: 0;
    bottom: 0;
    box-shadow: 0 0 10px rgba(0, 0, 0, .16);
}

.p-topfeature__img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.p-topfeature li:nth-child(even) .p-topfeature__img {
    left: 0;
    right: 50%;
}

.p-topfeature li:nth-child(even) .p-topfeature__cont {
    margin-left: auto;
    margin-right: 0;
    padding-left: 60px;
    padding-right: 15px;
}

@media screen and (max-width: 640px) {
    .p-topfeature__img {
        position: static;
        margin-bottom: 20px;
        width: calc(100% - 20px);
        height: fit-content;
        transform: translateX(20px);
    }

    .p-topfeature li:nth-child(even) .p-topfeature__img {
        width: 100%;
        transform: translateX(-20px);
    }

    .p-topfeature__img img {
        aspect-ratio: 3/2;
    }

    .p-topfeature__cont {
        padding: 0;
        width: auto;
    }

    .p-topfeature li:nth-child(even) .p-topfeature__cont {
        padding: 0;
    }
}</style>