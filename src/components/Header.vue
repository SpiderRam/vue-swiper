<template>
  <div id="header">
    <p class="lead" id="name">Carmen Owen</p>
    <h1 class="display-4" id="title">Portfolio</h1>
    <div id="copyright">&copy;2018 Carmen Owen</div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#header {
  background-image: url("../assets/hellebores.jpg");
  border-bottom: solid black 2px;
  margin-bottom: 20px;
  overflow: none;
  width: 100%;
  height: 200px;
}

#title {
  letter-spacing: 10px;
  font-family: "Acme", sans-serif;
  font-size: 80px;
  color: black;
  text-shadow: 1px 1px 2px #32cd32, 0 0 25px #adff2f, 0 0 5px #7fff00;
  text-align: center;
}

#name {
  color: black;
  font-family: "Acme", sans-serif;
  font-size: 50px;
  text-shadow: 1px 1px 2px #32cd32, 0 0 25px #adff2f, 0 0 5px #7fff00;
  text-align: center;
  margin-bottom: 0px;
}

#copyright {
  float: right;
  color: #333;
  text-shadow: 1px 1px green;
}
</style>
