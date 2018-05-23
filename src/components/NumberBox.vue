<template>
  <div class="number-box">
    <span class="minus" @click="minus"></span>
    <input class="input" type="text" v-model="value" />
    <span class="plus" @click="plus"></span>
  </div>
</template>

<script>
export default {
  name: 'NumberBox',
  data: function () {
    return {
      value: 1
    }
  },
  methods: {
    minus () {
      if (this.value > 1) {
        this.value--
        this.$emit('input', this.value)
      }
    },
    plus () {
      this.value++
      this.$emit('input', this.value)
    }
  }
}
</script>

<style lang="scss" scoped>
  .number-box {
    display: flex;
    .minus {
      background: #ccc;
      width: 64px;
      height: 64px;
      position: relative;
      &::after {
        content: " ";
        width: 24px;
        height: 1px;
        border-bottom: 2px solid #999; /*no*/
        position: absolute;
        left: 20px;
        top: 30px;
      }
    }
    .input {
      font-size: 30px;
      text-align: center;
      border: none;
      background: transparent;
      outline: none;
      width: 80px;
    }
    .plus {
      background: #ccc;
      width: 64px;
      height: 64px;
      position: relative;
      &::before {
        content: " ";
        position: absolute;
        width: 24px;
        height: 1px;
        border-bottom: 2px solid #999; /*no*/
        left: 20px;
        top: 30px;
      }
      &::after {
        content: " ";
        position: absolute;
        width: 1px;
        height: 24px;
        border-left: 2px solid #999; /*no*/
        left: 32px;
        top: 22px;
      }
    }
  }
</style>
