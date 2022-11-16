<template>
  <div class="counter" >
    <button :disabled="index < 1" @click="index--">&larr;</button> 
    <h1>{{index}}</h1> 
    <button :disabled="index == (images.length - 1) " @click="index++">&rarr;</button>
  </div>
  <div>{{images[index]}}</div>
</template>

<script>


export default {
  name: 'HelloWorld',
  data() {
    return {
      index: 0,
      images: [
        "courge","displine","no fap","freindship","something profound"
      ]
    }
  },
}



</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
button{
  font-weight: bolder;
  background: white;
  border: solid 1px;
  font-size: 50px;
  padding: 0;
  text-align: center;
  border: 0;
  padding-bottom: 20px;
}

.counter{
  display: flex;
  align-items: center;
  justify-content: center;
}

.counter > *{
  margin-inline: 30px;
}

</style>
