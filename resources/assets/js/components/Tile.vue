<template>
    <vue-drag-resize class="tile"
        :active="true"
        :handles="['br']"
        :parent="true" 
        :resizable="true" 
        :minw="128" :minh="128" 
        :grid="[65.75,65.75]" 
        :w="width" :h="height" 
        :x="x" :y="y"
        @dragging="onDrag"
        @resizing="onResize"
    />
</template>

<script>
import vueDragResize from 'vue-draggable-resizable'

export default {
    components: {
        vueDragResize
    },
    data() {
        return {
            x: 0,
            y: 0,
            width: 126, 
            height: 126
        }
    },
    props: ["tile"],
    methods: {
        onDrag: function (x, y) {            
            this.x = x;
            this.y = y;
        },
        onResize: function (x, y,width, height) {
            this.x = x;
            this.y = y;
            this.width = width;
            this.height = height;
        }
    }
};
</script>

<style>
.tile {
    position: absolute;
    display: inline-block;
    background: #15a4fa;
    margin: 3px !important;
}

.handle {
  background-color: transparent !important;
  border-width: 0px !important;
}

.handle.handle-br {
    bottom: 0;
    right: 0;
    z-index: 99;
    font-family: FontAwesome;
    display: inline-block;
    content: "\\f0da"    
}
</style>
