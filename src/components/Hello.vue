<template>
  <q-layout>
    <div class="container">
      {{msg}}
    </div>

  </q-layout>
</template>

<script>

import { QLayout } from 'quasar'
export default {
  name: 'index',
  components: {
    QLayout
  },
  data () {
    return {
      msg: 'NoClaim Bonus Blockchain MVP using Ethereum'
    }
  }
}
</script>

<style lang="stylus">

</style>
