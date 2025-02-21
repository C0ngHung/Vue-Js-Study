<template>
    <ChildrenComponent :fruits="fruits" :name="name" :age="age"
    @handleEmit = "buttonEmit" @handleAlert = "buttonAlert"></ChildrenComponent>

</template>

<script setup>
import { ref } from 'vue';
import ChildrenComponent from './ChildrenComponent.vue';

// emit - click - focus - blur - input - change - submit - keydown - keyup - keypress - mouseover - mouseout - mouseenter - mouseleave - mousedown - mouseup - mousemove - contextmenu - touchstart - touchend - touchmove - touchcancel - scroll - wheel - copy - cut - paste - drag - dragstart - dragend - dragover - dragenter - dragleave - drop - transitionend - animationstart - animationend - animationiteration - toggle



// props truyền từ component cha xuống component con

const fruits = ref(['Apple', 'Banana', 'Cherry']);

const name = ref('Công');
const age = ref(20);

const buttonEmit = () => {
  alert('emit')
}
const buttonAlert = () => {
  alert('alert')
}

</script>