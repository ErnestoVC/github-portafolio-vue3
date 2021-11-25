<template>
  <div id="cards">
    <div class="card">
      <h4>{{name}}</h4>
      <p>
          <br>
        {{description}}
      </p>
      <br>
      <p><strong>{{author}}</strong></p>
      <button-url :url="url" color=""/>
      <button-url :url="homepage" color="red" v-if="homepage != null"
      title="Homepage"/>
    </div>
  </div>
</template>

<script>
import ButtonUrl from './ButtonUrl.vue';
export default {
  components: { ButtonUrl },
    props: {
        name: String,
        description: String,
        author: String,
        url: String,
        homepage: String,
    }
};
</script>

<style scoped>
.card{
    width: 250px;
    border: solid 1px #eee;
    box-shadow: 1px 1px 1px 4px #333;
    text-align: center;
    margin: 7px;
}
</style>
