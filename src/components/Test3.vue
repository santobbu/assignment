<template>
  <div>
    <p>
      3.) If 1 = 5 , 2 = 25 , 3 = 325 , 4 = 4325 Then 5 = X - Please create new function for finding X value
    </p>
    <div>
        <div>input number of index: <input type="number" v-model="indexNo" /></div>
        <div class="answer">Result: <strong>{{getSequencNumber()}}</strong></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Test3',
  data () {
    return {
      indexNo: 5
    }
  },
  methods: {
    getNextNumber: function (index, previousNo) {
      if (index === 0) return ''
      else if (index === 1) return '5'
      else return index + previousNo
    },
    getSequencNumber: function () {
      var sequenceStr = ''
      var currentNo = ''
      for (var i = 0; i <= this.indexNo; i++) {
        currentNo = this.getNextNumber(i, currentNo)
        sequenceStr += currentNo + ' '
      }

      return sequenceStr
    }
  }
}
</script>

<style scope>
.answer {
  padding: 8px;
}
</style>
