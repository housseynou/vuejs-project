<template>
  <div class="hello">
    <div class="content">
    <div class="box">
      <h1><Bruxelles/h1>
      <p>Nuageux</p>
    </div>
    <div class="box">
      <h1>Dakar</h1>
      <p>Soleil</p>
    </div>
    <div class="box">
      <h1>Paris</h1>
      <p>Couvert</p>
    </div>
    <div class="box">
      <h1>Rome</h1>
      <p>Couvert</p>
    </div>
    <div class="box">
      <h1>Liège</h1>
      <p>Nuageux</p>
    </div>
    <div class="box">
      <h1>Namur</h1>
      <p>légère pluie</p>
    </div>
  </div>
  </div>
</template>

<script>

export default {
  name: 'AroundTheWorld',
  props: {
    msg: String
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
a {
  color: #0aeb85;
}
</style>
