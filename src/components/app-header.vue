<template>
    <div
        class="app-header">
        <slot>header</slot>
        </div>
</template>
<script>
export default {

}
</script>
<style lang="scss">
.app-header {
    position: absolute;
    left: 0;
    right: 0;
    height: 60px;
    line-height: 60px;
    border-bottom: 1px solid #eee;
}
</style>
