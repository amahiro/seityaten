<template>
    <div class="p-top-news l-inner">
        <ul class="c-news__list">
            <li class="c-news__list-item">
                <a class="c-news__list-link hover" href="">
                    <div class="c-news__flex">
                        <p class="c-news__tag">お知らせ</p>
                        <p class="c-news__date">2024年08月20日</p>
                    </div>
                    <p class="c-news__ttl">WEBサイトを公開しました</p>
                </a>
            </li>
        </ul>
    </div>
</template>


<style>

.p-top-news {
    padding-block: clamp(20px, 7vw, 70px);
}
.c-news__list-link {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    background-color: #f8f8f8;
    gap: 20px;
    padding: 25px 30px;
    -webkit-transition: .3s;
    transition: .3s;
}
.c-news__flex {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    gap: min(30px, 4vw);
}
.c-news__date, .c-news__tag, .c-news__ttl {
    font-size: min(16px,3.7333333333vw);
    -webkit-transition: .3s;
    transition: .3s;
}
.c-news__flex {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    gap: min(30px, 4vw);
}
.c-news__tag {
    min-width: 150px;
    min-height: 40px;
    padding: 5px 10px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    background-color: #b49970;
    border-radius: 4px;
    color: #fff;
}
.c-news__date, .c-news__tag, .c-news__ttl {
    font-size: min(16px,3.7333333333vw);
    -webkit-transition: .3s;
    transition: .3s;
}
.c-news__date {
    min-width: 120px;
}
.c-news__date, .c-news__tag, .c-news__ttl {
    font-size: min(16px,3.7333333333vw);
    -webkit-transition: .3s;
    transition: .3s;
}

@media screen and (max-width: 640px) {
    .p-top-news {
        padding-bottom: 12px;
    }
    .c-news__list-link {
        display: block;
        padding: min(25px, 4vw) min(30px, 4vw);
    }
    .c-news__flex {
        margin-bottom: 15px;
    }
    .c-news__tag {
        min-width: 120px;
        min-height: 30px;
        padding: 3px 10px;
    }
    .c-news__ttl {
        padding-left: 5px;
    }
}
</style>