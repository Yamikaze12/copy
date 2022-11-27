<template>
  <div class="form-auth">

    <div v-if="showLogin">
      <Mylogin />
      <p>
        belum punya akun? 
        <a href="#" @click="showLogin = false">Buat akun!</a>
      </p>
    </div>

    <div v-else>
      <Myregister />
      <p>
        sudah punya akun? 
        <a href="#" @click="showLogin = true">Login</a>
      </p>
    </div>

  </div>
</template>

<script>
    import Mylogin from '../components/Auth/Login.vue'
    import Myregister from '../components/Auth/Register.vue'
    import {ref} from 'vue'
    export default{
      name:"HomeView",
      components:{Mylogin, Myregister},
      setup(){
        const showLogin = ref(true)

        return {showLogin}
      }
    }
</script>
<style scoped>

</style>
