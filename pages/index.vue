<template>
  <div v-if="authenticated" class="flex justify-center items-center h-screen">
    <h1 class="text-xl">Hallo 😊</h1>
  </div>
  <div v-else class="flex justify-center items-center h-screen">
    <div class="card card-compact w-96 bg-base-100 shadow-xl">
      <div class="card-body p-2">
        <form>
          <input v-model="password" class="input input-bordered input-primary w-full" placeholder="Type here"
            type="password">
          <div class="card-actions justify-end">
            <button class="btn btn-primary" @click="login">Login</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
const password = ref(null)
const authenticated = ref(false)

function login() {
  if (password.value === "123456")
    authenticated.value = true
  else
    alert("Falsches Passwort!")
}

</script>