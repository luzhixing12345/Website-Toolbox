<template>
  <div class="main">
    <navigation></navigation>
    <introduction></introduction>
  </div>

</template>

<script>
// import Service from './components/Service'
import navigation from './components/navigation'
import introduction from './components/introduction'
export default {
  name: 'App',
  components: {
    navigation,
    introduction
  }
}

</script>

<style scope>
body,html,.main{
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background-color: #f8f9fa;
}

/* body {
  background-image: url("./assets/backgroundImage.jpg");
  background-position: center;
  background-size: cover; 
  background-attachment: scroll;
} */
</style>
