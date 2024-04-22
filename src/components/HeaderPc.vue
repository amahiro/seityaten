<script setup>
const props = defineProps(
    ['siteTtl','siteNav'],
);

const siteNavs = props.siteNav;
</script>

<template>
    <div class="l-header-pc">
        <div class="l-header-pc__top">
            <div class="l-header-pc__inner l-header-pc__top-inner">
                <a href="" class="l-header-pc__logo">
                    <h1 class="l-header-pc__logo">
                        {{ siteTtl }}
                    </h1>
                </a>
            </div>
        </div>
        <div class="l-header-pc__bottom">
            <ul class="l-header-pc__inner l-header-pc__bottom-list">
                <li class="l-header-pc__bottom-item" v-for="nav in siteNavs" :key=nav>
                    <a class="hover l-header-pc__bottom-link" :href=nav.link>{{ nav.name }}
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.l-header-pc {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0,0,0,.16);
    z-index: 12;
}
.l-header-pc__top {
    top: 0;
    width: 100%;
    height: 70px;
    z-index: 10;
    -webkit-transition: .3s;
    transition: .3s;
}
.l-header-pc__top-inner {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: justify;
    -ms-flex-pack: justify;
    justify-content: space-between;
    height: 100%;
    padding: 0 15px;
}

.l-header-pc__inner {
    width: min(1100px, 100%);
    margin: 0 auto;
}
.l-header-pc__logo {
    font-size: clamp(20px,2vw,30px);
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
    font-weight: 600;
}
.l-header-pc__logo-img {
    width: clamp(175px, 20vw, 200px);
}
.l-header-pc__logo-txt {
    font-size: clamp(10px,1.2vw,12px);
    color: #b49970;
}

.l-header-pc__bottom {
    background-color: #b49970;
    height: 50px;
}
.l-header-pc__bottom-list {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -ms-flex-pack: distribute;
    justify-content: space-around;
}

.l-header-pc__inner {
    width: min(1100px, 100%);
    margin: 0 auto;
}
.l-header-pc__bottom-item {
    width: 16.6666666667%;
}
.l-header-pc__bottom-link {
    position: relative;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    width: 100%;
    height: 50px;
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
    color: #fff;
    font-size: clamp(13px,1.6vw,16px);
    text-shadow: 0 0 5px rgba(77, 57, 30, .5);
    font-weight: 600;
    -webkit-transition: all .3s ease;
    transition: all .3s ease;
}
.l-header-pc__bottom-link::after {
    content: "";
    background-color: transparent;
    display: block;
    width: 10%;
    height: 2px;
    position: absolute;
    bottom: 0;
    left: 0;
    -webkit-transition: .3s;
    transition: .3s;
    -webkit-transform: scaleX(0);
    transform: scaleX(0);
}
@media screen and (max-width: 768px) {
    .l-header-pc {
        display: none;
    }
}
</style>
