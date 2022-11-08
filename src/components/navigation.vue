<template>
    <div class="navigation">
        <img :src="logo" alt="no images found">
        <div v-for="(item, index) in displays" v-key="index" class="item">
            {{ item.name }}
        </div>
    </div>
</template>
<script>
export default {
    data() {

        return {
            logo: require('../assets/logo.png'),
            displays: [
                { name: 'Trending', routerAddress: '' },
                { name: 'Contributions', routerAddress: '' }
            ]
        }
    },
}
</script>
<style scoped lang="css">
.navigation {
    display: flex;
    width: 100%;
    height: 6%;
    background-color: rgb(36, 41, 47);
}

.navigation .item {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    font-weight: 600;
    font-size: 14px;
    color: white;
    margin: auto 0;
    margin-left: 15px;
}

img {
    height: 60%;
    border-radius: 50%;
    margin: auto 0;
    margin-left: 20px;
}
</style>