<template>
  <div class="row justify-content-center">
    <div class="col-lg-8">
      <div class="section_title">
        <h2>{{text1}} <span>{{text2}}</span></h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props: ['text1', 'text2', 'text3']
};
</script>

<style lang="scss" scoped></style>
