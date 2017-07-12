<template>
    <div
        class="app-footer">
        <slot>footer</slot>
        </div>
</template>
<script>
export default {

}
</script>
<style lang="scss">
.app-footer {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 60px;
    line-height: 60px;
    border-top: 1px solid #eee;
}
</style>
