<template>
  <div class="calculator">
    <div class="keyBoard rounded m-1 p-3 text-right lead bg-dark">
      {{ calcValue || 0 }}
    </div>

    <div class="row no-gutters">
      <div class="col-3" v-for="n in calElements" :key="n">
        <div class="lead text-white text-center m-1 py 3 bg-dark">
          {{ n }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Calculator-app',
  props: {
    msg: String,
  },

  data() {
    return {
      calcValue: '',
      calElements: ['c', '*', '/', '-', 7, 8, 9, '+', 4, 5, 6, '%', 1, 2, 3, '=', 0, '.'],
    }
  }
}
</script>

<style scoped>
.calculator {
  max-width: 400px;
  margin: 50px auto;
  background: #234
}

.keyBoard {
  text-align: right;
  font-weight: bold;
  color: white;
  background: black;
}

.bg-dark {
  background: #31475e;
}
</style>