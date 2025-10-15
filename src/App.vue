<!-- options API -->
<script>
// import Button from './components/Button.vue'
// import Header from './components/Header.vue'
// import Student from './components/Student.vue'

// export default {
//   components: {
//     Student,
//     Button,
//     Student,
//   },
// }
</script>

<!-- composition api -->
<script setup>
// import component
import Button from './components/Button.vue'
import Header from './components/Header.vue'
import Student from './components/Student.vue'
</script>

<template>
  <Header />

  hello vue <br />

  <!-- pemanggilan/penggunaan component (Using a Component) -->
  <Student />
  <Button />
</template>
