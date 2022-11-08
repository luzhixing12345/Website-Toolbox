<template>
    <div class="list">
        <div v-for="(service, index) in Services" :key="index" class="service-item">
            <div>{{ service.name }}</div>
            <div>{{ service.description }}</div>
        </div>
    </div>
</template>
<script>
export default {
    name: "Service",
    data() {
        return {
            Services: []
        }
    },
}
</script>
<style scoped>
.list {
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center;
    overflow-y: auto;
    /* justify-content: space-between; */
}

.list .service-item {
    /* flex: 0 1 40%; */
    margin-top: 100px;
    border-radius: 15px;
    width: 40%;
    min-height: 15%;
    background-color: #8eecf5;
    opacity: 0.6;
    margin: 50px auto;
    box-shadow: rgba(17, 17, 26, 0.05) 0px 1px 0px, rgba(17, 17, 26, 0.1) 0px 0px 8px;
    transition: all 1s;
}

.list .service-item:hover {
    transition: all 1s;
    box-shadow: rgba(0, 0, 0, 0.56) 0px 22px 70px 4px;
    opacity: 1;
}

.list .service-item :first-child {
    font-size: 35px;
    font-weight: bolder;
    margin: 10px 10px;
}

.list .service-item :last-child {
    font-size: 24px;
    margin-left: 10px;
}

</style>