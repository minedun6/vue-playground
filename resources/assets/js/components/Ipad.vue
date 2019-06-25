<template>
    <div class="inner-template">
        <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12">
            <button class="btn btn-xs btn-default" @click="addTile">+</button>
            <div class="ipad">
                <div class="ipad-content">
                    <div class="ipad-header"></div>
                    <grid :tiles="tiles"></grid>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Grid from './Grid.vue';

    export default {
        components: {
            Grid
        },
        data() {
            return {
                tiles: []
            }
        },
        methods: {
            addTile() {
                this.tiles.push({});
            }
        }
    }
</script>

<style>
    .inner-template > div {
        padding: 0 !important;
    }

    .ipad {
        width: 1270px;
        height: 852px;
        margin: 1px auto;
        padding-top: 45px;
        border: 1px solid #a0a3aa;
        border-radius: 62px;
        background: url(../../images/iPad.png) center no-repeat;
    }

    .ipad-content {
        position: relative;
        overflow: hidden;
        top: -1px;
        left: -2px;
        width: 1023px;
        height: 767px;
        margin: 0 auto 0 auto;
        border: 1px solid #a0a3aa;
        background: no-repeat center !important;
    }

    .ipad-header {
        position: absolute;
        width: 1022px;
        height: 80px;
        background: url(../../images/ipad-header.png) no-repeat;
        opacity: .5;
    }

    @media only screen and (max-width: 768px) {
        .panel-default {
            overflow-y: auto;
            overflow-x: scroll;
            width: 100% !important;
        }
    }

    @media only screen and (max-width: 1024px) {
        .panel-default {
            overflow-y: auto;
            overflow-x: scroll;
            width: 100% !important;
        }
    }

    @media only screen and (min-width: 1024px) {
        .panel-default {
            overflow-y: auto;
            overflow-x: scroll;
            width: 100% !important;
        }
    }
</style>