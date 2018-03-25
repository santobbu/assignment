<template>
  <div id="content">
      <h3>ASSIGNMENT</h3>
      <div class="container">
        <Test1 />
      </div>
      <div class="container">
        <Test2 />
      </div>
      <div class="container">
        <Test3 />
      </div>
  </div>
</template>

<script>
import Test1 from './components/Test1'
import Test2 from './components/Test2'
import Test3 from './components/Test3'

export default {
  name: 'App',
  components: {
    Test1,
    Test2,
    Test3
  }
}
</script>

<style scope>
#content {

}

.container {
  padding: 8px;
}
</style>
