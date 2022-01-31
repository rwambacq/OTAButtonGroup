<template>
  <div :class="{
    filled,
    empty: !filled,
    btn: true
  }">
    {{filled ? "" : "+"}}
  </div>
</template>

<script>
// A button that can either be styled as a solid button or an empty 'add' button
export default {
  name: 'Button',
  props: {
    filled: {  // indicates whether the button is a filled button or an empty button, used to dynamically set styling
      type: Boolean,
      default: true
    }
  }
}
</script>

<style scoped>
  .btn {
    width: 36px;
    height: 36px;
    border-radius: 4px;
    cursor: pointer;
  }
  .filled {
    background: #013A63;
  }

  .empty {
    background: #EDFAFF;
    border: 1px dashed #013A63;
    user-select: none;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.75rem;
    font-weight: 600;
  }
</style>
