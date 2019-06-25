<template>
    <div class="ipad-grid">
        <div class="cell" v-for="i in 150" :key="i"></div>
        <tiles :tiles="tiles"></tiles>
    </div>
</template>

<script>
    import Tiles from './Tiles.vue';

    export default {
        props: ['tiles'],
        components: {
            Tiles
        }
    }
</script>

<style>
.ipad-grid {
    width: 992px;
    height: 664px;
    margin: 85px auto 0;
    display: grid;
    grid-template-columns: repeat(15, 1fr);
    border: 1px dashed;
}

.cell {
    border: 1px solid #eee;
}
</style>