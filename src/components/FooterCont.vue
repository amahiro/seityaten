<script setup>
const props = defineProps(
    ['siteTtl','siteNav'],
);

const siteNavs = props.siteNav;

</script>


<template>
    <div>
        <div class="l-inner">
            <div class="l-footer__ttl">
                {{ siteTtl }}
            </div>
            <ul class="l-footer__list c-flex--fnav">
                <li class="l-footer__item" v-for="nav in siteNavs" :key=nav>
                    <a :href=nav.link class="l-footer__link">
                        {{ nav.name }}
                    </a>
                </li>
            </ul>
        </div>
        <p class="l-footer__copy">
            <small>© 2024 amanohiroki</small>
        </p>
    </div>
</template>

<style>
.l-footer {
    padding: 50px 15px 20px;
    background-color: #000;
}
.l-footer__ttl {
    font-size: clamp(20px,3.6vw,36px);
    color: #fff;
    font-weight: 600;
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
    text-align: center;
    margin-bottom: 20px;
}
.l-footer__list {
    margin: 0 -15px;
}

.l-footer__item {
    padding: 0 15px;
}

.l-footer__copy,
.l-footer__link {
    color: #000;
    font-weight: 500;
    letter-spacing: .05em;
}

.l-footer__copy {
    font-size: 1.2rem;
    margin-top: 10px;
    text-align: center;
}
.c-flex--fnav {
    display: flex;
    -webkit-align-items: center;
    align-items: center;
    -webkit-justify-content: center;
    justify-content: center;
}
.l-footer__copy,
.l-footer__link {
    color: #fff;
    font-weight: 500;
    letter-spacing: .05em;
    font-size: clamp(12px,1.4vw,14px);
}
@media screen and (max-width: 640px) {
    .l-footer__list {
        -webkit-flex-wrap: wrap;
        flex-wrap: wrap;
    }
    .l-footer__item {
        text-align: center;
        width: 33.3333333333%;
    }
}
</style>