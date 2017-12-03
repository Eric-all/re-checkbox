<template>
  <div>
    <label>
      <v-checkbox checked/>
      &nbsp; controlled checked re-checkbox
    </label>
  </div>
</template>

<script>
import '../../lib/checkbox.css'
import Switch from '../../lib/checkbox'
export default {
  name: 'App',
  components: {
    VCheckbox: Checkbox
  }
}
</script>
