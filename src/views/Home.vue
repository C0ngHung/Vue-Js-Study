<template>
    <!-- <h3>{{ fullName }}</h3> -->
  
    <!-- <input type="text" v-model="age" class="form-control" placeholder="Nhập tuổi" />
    <p v-if="canRegister">Đủ điều kiện đăng ký</p>
    <p v-else>Không đủ điều kiện đăng ký</p> -->

    <h1>Danh sách người dùng</h1>
    <ul v-for="user in users" :key="user.id">
      <li>
        {{ user.name }} - {{ user.age }}
      </li>
    </ul>

    <h1>Danh sách người trên 18 tuổi</h1>

    <ul v-for="user in usersOver18" :key="user.id">
        <li>
        {{ user.name }} - {{ user.age }}
        </li>
    </ul>
  </template>

  
  
  <script setup>
  import { computed, ref, reactive } from 'vue';
  
//   const firstName = ref('Công');
//   const lastName = ref('Hùng');
  
//   const age = ref(20);
//   const canRegister = computed(() => age.value >= 18);
  
  // computed - hàm tính toán
  const fullName = computed(() => `${firstName.value} ${lastName.value}`);


  // dùng coputed -> làm việc với mảng 
  const users = reactive([{
  id: 1,
  name: 'Huy',
  age: 20,
},
{
  id: 2,
  name: 'Tuan',
  age: 15,
}])

// Dùng coputed --> lọc những người trên 18 tuổi
const usersOver18 = computed(() => users.filter(user => user.age >= 18))

  </script>
  