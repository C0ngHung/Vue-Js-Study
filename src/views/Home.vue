<template>
    <h1 class="text-danger">{{ count }}</h1>
    <button @click="handleCount" class="btn btn-success">Increment</button>

    <p>Text: {{ inputText }}</p>
    <input v-model="inputText" type="text" class="form-control" placeholder="Enter text">
    <h1>{{ user.name }}</h1>
    <h2>{{ user.age }}</h2>
    <h3>{{ user.email }}</h3>

    <ul v-for="(user, index) in users" :key="user.name">
        <li>{{ index + 1 }} - {{ user.name }}</li>
        <li>{{ user.age }}</li>
        <li>{{ user.email }}</li>
    </ul>


    <table class="table">
        <thead>
            <tr>
                <th>STT</th>
                <th>Name</th>
                <th>Age</th>
                <th>Email</th>
                <th>Gender</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(user, index) in users" :key="user.name">
                <td>{{ index + 1 }}</td>
                <td>{{ user.name }}</td>
                <td>{{ user.age }}</td>
                <td>{{ user.email }}</td>
                <td>{{ user.isActive ? "Nam " : "Nữ" }}</td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>
    import { reactive, ref } from 'vue'
    // Khi muốn sử dụng biến khai báo với ref, cần thêm từ khóa value

    // Khởi tạo giá trị ban đầu ~ number hoặc text
    const count = ref(0)
    const inputText = ref('VitaminCode01');
    

// reactive ~ muốn sử dụng biến khai báo với reactive, không cần thêm từ khóa value
// được sử dụng để tạo đối tượng hoặc mảng phản ứng
// tất cả các thuộc tính bên trong reactive đều là đối tượng phản ứng
    const user = reactive({
        name: 'VitaminCode',
        age: 20,
        email: "C0ngHungDCH@gmail.com",
    })


    // Computed

    // v-for ~ vòng lặp
    const users = reactive([
  { name: 'Gia Minh', age: 21, email: "user@example.com", isActive:true },
  { name: 'Jer', age: 21, email: "user@example.com" },
  { name: 'Hải Nam', age: 21, email: "user@example.com" },
  { name: 'Công Hùng', age: 21, email: "user@example.com" },
])
    // arrow function
    // @click

    // const handleCount = () => {
    //     count.value++
    // };

</script>

<style scoped>
</style>