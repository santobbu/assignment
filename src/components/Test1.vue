<template>
  <div>
    <p>
      1.) 3, 5, 9, 15, X  - Please create new function for finding X value
    </p>
    <div>
        <div>input number of sequence: <input type="number" v-model="indexNo" /></div>
        <div class="answer">Result: <strong>{{getSequencNumber()}}</strong></div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Test1',
  data () {
    return {
      indexNo: 5
    }
  },
  methods: {
    getSequencNumber: function () {
      var sequenceStr = ''
      var previousNo = 3
      for (var i = 0; i < this.indexNo; i++) {
        var nextSequenceNo = (previousNo + (2 * i))
        previousNo = nextSequenceNo
        sequenceStr += nextSequenceNo + ' '
      }

      return sequenceStr
    }
  }
}
</script>

<style scope>
.container {
  padding: 8px;
}
</style>
