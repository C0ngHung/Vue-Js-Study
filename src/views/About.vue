<template>
    <h1>Thông tin cá nhân</h1>
    <label for="" class="form-lable">Họ và tên:</label>
    <input type="text" v-model="user.name" class="form-control" placeholder="Nhập họ và tên">
    <label for="" class="form-lable">Tuổi:</label>
    <input type="number" v-model="user.age" class="form-control" placeholder="Nhập tuổi">
    <label for="" class="form-lable">Email:</label>
    <input type="text" v-model="user.email" class="form-control" placeholder="Nhập email">


    <h1>Kết quả</h1>
    <div class="card">
        <div class="card-body">
            <p>Họ và tên: {{ user.name }}</p>
            <p>Tuổi: {{ user.age }}</p>
            <p>Email: {{ user.email }}</p>
        </div>
    </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const user = reactive({
    name: '',
    age: '',
    email: ""
})

</script>