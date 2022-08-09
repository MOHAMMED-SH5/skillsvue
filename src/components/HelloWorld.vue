<template>
  <div class="hello">
<div class="card mt-2 ms-2" style="width: 15rem;">
  <img src="@/assets/logo.png" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">{{userId}}</h5>
    <p class="card-text">{{id}}</p>
    <p class="title card-text">{{title}}</p>
    <p class="body card-text">{{body}}</p>
  </div>
</div>


  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props:["userId","id","tittle","body"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.card
{
  height: 70vh;
}
.title,.body
{
  font-size: 10px;
}
</style>
