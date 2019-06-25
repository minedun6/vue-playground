<template>
    <span class="tiles">
        <tile v-for="(tile, index) in tiles" :key="index" :tile="tile"></tile>
    </span>
</template>

<script>
    import Tile from './Tile.vue';

    export default {
        props: ['tiles'],
        components: {
            Tile
        }
    }
</script>

<style>
.tiles {
    position: absolute;
    display: block;
    width: 992px;
    height: 664px;
    margin: 0;
    padding: 0;
}
</style>