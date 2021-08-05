<template>
    <div class="partner d-flex align-items-center justify-content-between flex-wrap gap-20px">
        <div class="partner__item d-flex align-items-center"  v-for="(item, index) in partners" :key="index">
            <img class="partner__img" :src="item.img" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name:'Partners',

     props: [
      "partners"
    ]
}
</script>

<style lang="scss">
.partner{
    gap: 16px;
}
</style>