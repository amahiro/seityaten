<script setup>
defineProps(['siteTtl']);
</script>


<template>
    <section class="p-top-access">
        <div class="l-inner">
            <ul class="p-top-access__list">
                <li>
                    <div class="p-top-access__box">
                        <div class="p-top-access__cont">
                            <div class="p-top-access__cont-ttl">
                                <div>
                                    <h3 class="c-ttl07">{{ siteTtl }}</h3>
                                </div>
                            </div>
                            <dl>
                                <div class="p-top-access__cont-item p-top-access__cont-item--address">
                                    <dt class="c-ttl07">住所</dt>
                                    <dd>〇〇県△△市〇〇町0-0-0</dd>
                                </div>
                                <div class="p-top-access__cont-item p-top-access__cont-item--tel">
                                    <dt class="c-ttl07">電話番号</dt>
                                    <dd>000-0000-0000</dd>
                                </div>
                                <div class="p-top-access__cont-item p-top-access__cont-item--time">
                                    <dt class="c-ttl07">営業時間</dt>
                                    <dd>9:00～17:00</dd>
                                </div>
                                <div class="p-top-access__cont-item p-top-access__cont-item--time">
                                    <dt class="c-ttl07">店休日</dt>
                                    <dd>月曜・火曜</dd>
                                </div>
                            </dl>
                        </div>
                        <div class="p-top-access__map">
                            <iframe width="100%" height="100%" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d51840.018766061745!2d139.70919719999998!3d35.70158875!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x60188d2059b7fd4b%3A0xec61c68fe232efd2!2z5p2x5Lqs6YO95paw5a6_5Yy6!5e0!3m2!1sja!2sjp!4v1713748591877!5m2!1sja!2sjp" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                        </div>
                    </div>
                </li>
            </ul>

        </div>
    </section>
</template>

<style>
.p-top-access {
    background-color: #fff;
    color: #131313;
    padding: clamp(60px, 14vw, 140px) 0;
    padding-left: 0;
}
.p-top-access__list li {
    border: 1px solid #ded8c0;
    padding: clamp(20px, 5vw, 50px);
}
.p-top-access__box {
    display: -webkit-flex;
    display: flex;
    margin-bottom: 30px;
}
.p-top-access__cont {
    padding-right: 30px;
    width: 50%;
}
.p-top-access__cont dl {
    display: -webkit-flex;
    display: flex;
    flex-direction: column;
    gap: clamp(15px,3vw,30px) clamp(30px, 5vw, 52px);
}
.p-top-access__cont-ttl .c-ttl07 {
    margin-bottom: clamp(15px,3vw,30px);
    font-size: clamp(26px,3.6vw,36px);
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
}
.c-ttl07 {
    font-size: clamp(20px,2.4vw,24px);
    font-weight: 600;
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
}
.p-top-access__map {
    width: 50%;
}
.p-top-access__map iframe {
    widows: 100%;
    height: 100%;
}
.p-top-access dl dt {
    padding-left: 20px;
    margin-bottom: 10px;
    position: relative;
}
.p-top-access dl dt::before {
    content: '';
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    width: 10px;
    height: 100%;
    background: linear-gradient(90deg, #b49970 0, #855915 100%);
}
.p-top-access dl dd {
    font-size: clamp(14px,2vw,22px);
}
@media screen and (max-width: 640px) {
    .p-top-access__box {
        flex-direction: column;
        gap: 40px
    }
    .p-top-access__cont {
        width: 100%;
    }
    .p-top-access__map {
        width: 100%;
        aspect-ratio: 1/1;
    }
    .p-top-access dl {
        flex-wrap: wrap;
        flex-direction: row;
    }
    .p-top-access dl dt::before {
        width: 7px;
    }
    .p-top-access dl dt {
        padding-left: 15px;
    }
}
</style>