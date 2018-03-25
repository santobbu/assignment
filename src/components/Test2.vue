<template>
  <div>
    <p>
      2.) (Y + 24)+(10 × 2) = 99  - Please create new function for finding Y value
    </p>
    <div>
        <div>Equation:
            (<strong>{{getCalculation()}}</strong> + <input type="number" v-model="inputA" />)
            + (<input type="number" v-model="inputB" /> x <input type="number" v-model="inputC" />)
            = <input type="number" v-model="inputD" />
        </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Test2',
  data () {
    return {
      inputA: 24,
      inputB: 10,
      inputC: 2,
      inputD: 99
    }
  },
  methods: {
    getCalculation: function () {
      return this.inputD - (this.inputB * this.inputC) - this.inputA
    }
  }
}
</script>

<style scope>
input[type=number] {
  width: 50px;
}
</style>
