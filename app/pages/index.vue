<template>
    <div class="links">
      <button @click="login" class="button--grey">
        Login
      </button>
    </div>
</template>

<script>
export default {
  methods: {
    login(){
      console.log('Requesting')
      this.$auth.loginWith('laravelSanctum', {
        data: {
          email: 'sagar@smail.com',
          password: 'pass'
        }
      })
    }
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
