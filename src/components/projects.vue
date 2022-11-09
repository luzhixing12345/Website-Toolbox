<template lang="">
    <div class="Project">
        <div class="title">
            <div id="title">Projects</div>
            <div class="line"></div>
        </div>
        <div class="multi-projects">      
            <div v-for="(project,index) in projects" v-key="index" class="project" >
                <button @click="jumpToLink(project.link)">
                    <div>{{project.title}}</div>
                    <div>{{project.description}}</div>
                </button>
            </div>
        </div>  
    </div>
</template>
<script>
export default {
    data() {
        return {
            projects : [
                {title:'Stack Memory Draw',description:'',link:''},
                {title:'Stack Memory Draw',description:'',link:''},
                {title:'Stack Memory Draw',description:'',link:''},
                {title:'Stack Memory Draw',description:'',link:''},
                // {title:'Stack Memory Draw',description:'',link:''},
                // {title:'Stack Memory Draw',description:'',link:''},
                // {title:'Stack Memory Draw',description:'',link:''},
                // {title:'Stack Memory Draw',description:'',link:''},
            ]
        }
    },
    methods: {
        jumpToLink(link) {
            window.open(link,"_blank");
        }
    },
}
</script>
<style lang="css" scoped>

.Project {
    min-height:50%;
    /* min-height: 100vh; */
    display: flex;
    flex-direction: column;
    /* justify-content: center; */
    align-items: center;
    /* overflow: hidden; */
    width: 100%;
    /* margin: 0 auto; */
    overflow-y: auto;
    /* align-items: center; */
    /* margin-left: 22%; */
}

.title {
    width: 80%;
    margin-left: 20%;
}

.title #title {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    font-size: 2vw;
    font-weight:600;
}

 .title .line {
    width: 80%;
    height: 2px;
    background-color: rgb(216, 216, 216);
}

.multi-projects {
    width: 80%;
    margin-left: 20%;
    display: flex;
    flex-wrap: wrap;
}

.multi-projects .project {
    width:40%;
}

.multi-projects .project button {
    border: 0;
    width: 90%;
    margin-top: 20px;
    min-height: 100px;
    border-radius: 15px;
    background-color: white;
    opacity: 0.6;
    box-shadow: rgba(17, 17, 26, 0.05) 0px 1px 0px, rgba(17, 17, 26, 0.1) 0px 0px 8px;
    transition: all 1s;
}

.multi-projects .project button:hover {
    transition: all 1s;
    box-shadow: rgba(0, 0, 0, 0.56) 0px 22px 70px 4px;
    opacity: 1;
}


</style>