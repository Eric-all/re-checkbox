<template>
  <div>
    <label>
      <v-checkbox checked/>
      &nbsp; controlled checked re-checkbox
    </label>
  </div>
</template>

<script>
import Checkbox from '../../src'
export default {
  name: 'App',
  components: {
    VCheckbox: Checkbox
  }
}
</script>
