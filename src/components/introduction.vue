<template lang="">
    <div class="introduction">
        <div class="avatar">
            <img :src="avatar" alt="">
        </div>
        <div class="intro">
            <div id="title">Hello, I'm kamilu</div>
            <div>Welcome to my website!</div>
            <div class="buttons">
                <button v-for="(item,index) in iconButtons" v-key="index" class="button" @click="jumpToLink(item.link)">
                    <i :class="item.class"></i>
                    <div id="icon-name">{{item.name}}</div>
                </button>
            </div>
        </div>
    </div>
</template>
<script>
import 'remixicon/fonts/remixicon.css'
export default {

    data() {
        return {
            avatar: require('../assets/avatar.jpg'),
            iconButtons: [
                { name: 'Github', class: 'ri-github-fill', link:'https://github.com/luzhixing12345'},
                { name: 'Blog', class:'ri-book-line',link:'https://luzhixing12345.github.io/'},
                { name: 'Bilibili', class: 'ri-bilibili-fill',link:'https://space.bilibili.com/261543088'},
                { name: 'Zhihu', class: 'ri-zhihu-line',link:'https://www.zhihu.com/people/lu-zhi-xing-66-64' },
            ]
        }
    },
    methods: {
        jumpToLink(link) {
            window.open(link,"_blank");
        }
    }
}
</script>
<style lang="css" scoped>
.introduction {
    display: flex;
    justify-content: center;
    align-items: center;
    /* flex: 1 1 auto; */
    width: 100%;
    height: 50%;
    /* background-color: aqua; */
}

.introduction .avatar {
    height: 70%;
}

.introduction .avatar img {
    border-radius: 50%;
    border: 1px solid #d0d7de;
    box-shadow: 0 0 0 1px rgba(27, 31, 36, 0.15);
    height: 90%;
}

.introduction .intro {
    height: 100%;
    width: 40%;
    /* background-color: antiquewhite; */
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    font-size: 32px;
    font-weight: 500;
    word-wrap: break-word;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 3%;
}

.introduction .intro #title {
    font-size: 50px;
    font-weight: 650;
    margin-bottom: 20px;
}

.introduction .buttons {
    display: flex;
    width: 100%;
    height: 30%;
    flex-wrap: wrap;
}

.introduction .buttons .button {
    min-width: 100px;
    height: 50px;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    font-size: 20px;
    font-weight: 500;
    margin-top: 20px;
    margin-right: 15px;
    border-radius: 10px;
    border: 0;
    display: flex;
    align-items: center;
    background-color: white;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
    cursor: pointer;
    transition: all 0.8s;
}

.introduction .buttons .button:hover {
    transition: all 0.8s;
    background-color: rgb(55,65,81);
    color: white;
    box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px, rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px, rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
}

#icon-name {
    margin-left: 5px;
}

</style>