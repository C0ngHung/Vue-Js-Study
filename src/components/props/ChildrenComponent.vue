<template>
    <h3>Danh sách</h3>
    <ul v-for="fruit in fruits" :key="fruit">
        <li>
            {{ fruit }}
        </li>
    </ul>

    <h3>Thông tin cá nhân</h3>
    <p>Họ và tên: {{ name }}</p>
    <p>Tuổi: {{ age }}</p>

    <button class="btn btn-primary" @click="$emit('handleEmit')">Emit</button>
    <button class="btn btn-warning" @click="$emit('handleAlert')">Alert</button>
</template>

<script setup>

// props truyền từ component cha xuống component con

//define props
const props = defineProps({

    //object : data type
    fruits: Array,
    name: String,
    age: Number
})

// emit

defineEmits(['handleEmit', 'handleAlert'])

</script>