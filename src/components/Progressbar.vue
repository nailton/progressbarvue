<template>
  <div class="progress-bar">
    <div
    :class="(progress == 100) ? 'progress-inner complete': 'progress-inner'"
    :style="`width: ${progress}%`">
      <span :class="(progress > 50) ? 'white' : ''">{{ progress }}%</span>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'progressbar',
    props: ['progress']
  }
</script>
<style>
  .progress-bar{
    width: 100%;
    height: 20px;
    background-color: #fff;
    position: relative;
  }
  .progress-inner{
    height: 100%;
    background-image: linear-gradient(to right, #ED008D, #2484E4);
    border-radius: 0px 10px 10px 0px;
  }
  .progress-inner.complete{
    border-radius: 0px;
  }
  .progress-inner span{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: ##313131;
    font-size: 14px;
  }
  .progress-inner span.white{
    color: #fff;
  }
</style>
