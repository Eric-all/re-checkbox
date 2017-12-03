<template>
<span :class="classes">
  <input
    :type="type"
    :name="name"
    :disabled="disabled"
    :checked="defaultchecked"
    @click="handleClick"
    :class="prefixCls + '-input'"
  >
  <span :class="prefixCls + '-inner'"></span>
</span>
</template>

<script>
  import classname from 'classnames'
  export default {
    name: 'Checkbox',
    props: {
      prefixCls: {
        type: String,
        default: 're-checkbox'
      },
      name: String,
      type: {
        type: String,
        default: 'checkbox'
      },
      checked: Boolean,
      disabled: Boolean
    },
    data () {
      return {
        defaultchecked: this.checked
      }
    },
    methods: {
      handleClick (e) {
        if (this.disabled) return
        this.defaultchecked = !this.defaultchecked
        this.$emit('onChange', this.defaultchecked, e)
      }
    },
    computed: {
      classes () {
        return classname(this.prefixCls, {
          [`${this.prefixCls}-checked`]: this.defaultchecked,
          [`${this.prefixCls}-disabled`]: this.disabled
        })
      }
    }
  }
</script>
