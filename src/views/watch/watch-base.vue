<template>
  <div class="watch-base">
    <p>
      <span>watch的对象: </span>
      <span>{{genderDict}}</span>
    </p>
    <p>
      <span>改变的对象: </span>
      <span>{{gender}}</span>
    </p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        genderDict: '1',
        gender: ''
      }
    },
    watch: {
      genderDict: {
        handler(newVal, oldVal){
          console.log('监听genderDict',newVal, oldVal);
          this.gender = newVal === '1' ? '男' : '女'
        },
        // immediate: true
      }
    }
  }
</script>