<script setup>
import { ref } from 'vue';

const props = defineProps(
    ['siteTtl','siteNav'],
);

const siteNavs = props.siteNav;


//ドロワーの開閉に関する関数
//ドロワーボタンの押下でクラスを追加する
const isDrawerOpen = ref(false)
function drawerOpen() {
    if( isDrawerOpen.value ) {
        isDrawerOpen.value = !isDrawerOpen.value;
    } else {
        isDrawerOpen.value = isDrawerOpen;
    }
}
</script>

<template>
    <div class="l-header-sp">
        <div class="l-header-sp_logo">{{ siteTtl }}</div>
        <div :class="{ 'l-header-sp_btn': true, 'is--drawer-btn': isDrawerOpen }" @click=drawerOpen>
            <span></span>
        </div>
        <div :class="{ 'l-header-sp__drawer': true, 'is--drawer-open': isDrawerOpen }">
            <ul>
                <li v-for="nav in siteNavs" :key=nav>
                    <a :href=nav.link>{{ nav.name }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>
<style scoped>
.l-header-sp {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0,0,0,.16);
    display: none;
    height: 60px;
    align-items: center;
    justify-content: space-between;
    padding: 15px;
    z-index: 999;
}
.l-header-sp_btn {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    width: 60px;
    height: 60px;
    background-color: #000;
    z-index: 9999;
}
.l-header-sp_btn::before,
.l-header-sp_btn::after {
    content: '';
    position: absolute;
    left: 50%;
    transform: translate(-50%,-50%);
    width: 30px;
    height: 1px;
    background-color: #fff;
    transition: all .3s ease;
}
.l-header-sp_btn::before {
    top: calc(50% - 10px);
}
.l-header-sp_btn::after {
    top: calc(50% + 10px);
}
.l-header-sp_btn span {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    width: 30px;
    height: 1px;
    background-color: #fff;
    transition: all .3s ease;
}
.is--drawer-btn span {
    opacity: 0;
}
.is--drawer-btn::before {
    transform: translate(-50%, calc(-50% + 10px)) rotate(45deg);
}
.is--drawer-btn::after {
    transform: translate(-50%, calc(-50% - 10px)) rotate(-45deg);
}
.l-header-sp__drawer {
    opacity: 0;
    visibility: hidden;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 9998;
    transition: all .3s ease;
}
.l-header-sp__drawer.is--drawer-open {
    opacity: 1;
    visibility: visible;
}
.l-header-sp__drawer ul {
    margin-top: -60px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 20px;
}
.l-header-sp__drawer ul li {
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
    font-weight: 600;
}
.l-header-sp_logo {
    font-family: "游明朝", "Yu Mincho", YuMincho, "Hiragino Mincho Pro", serif;
    font-weight: 600;
}

@media screen and (max-width: 768px) {
    .l-header-sp {
        display: flex;
    }
}
</style>