<template>
  <div class="main">
    <Service></Service>
  </div>

</template>

<script>
import Service from './components/Service'
export default {
  name: 'App',
  components: {
    Service
  }
}

</script>

<style scope>
body,html,.main{
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
body {
  background-image: url("./assets/backgroundImage.jpg");
  background-position: center;
  background-size: cover; 
  background-attachment: scroll;
}
</style>
