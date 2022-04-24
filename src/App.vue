<template>
    <div class="container mt-4">
      <div class="row">
        <div class="col-sm-6 mx-auto">
          <form novalidate>

            <div v-show="step === 1" class="step">
              <div class="form-group">
                <label for="name">Ваше имя</label>
                <input type="text" class="form-control" id="name">
              </div>

              <div class="form-group">
                <label for="surname">Ваша фамилия</label>
                <input type="text" class="form-control" id="surname">
              </div>

              <div class="form-group">
                <label for="email">Email</label>
                <input type="text" class="form-control" id="email">
              </div>

              <button @click="nextStep" type="button" class="btn btn-primary">Следующий шаг</button>
            </div>

            <div v-show="step === 2" class="step">
              <div class="form-group">
                <label for="password">Пароль</label>
                <input type="password" class="form-control" id="password">
              </div>

              <div class="form-group">
                <label for="passwordConfirm">Подтверждение пароля</label>
                <input type="password" class="form-control" id="passwordConfirm">
              </div>

              <button @click="nextStep" type="button" class="btn btn-primary">Следующий шаг</button>
            </div>

          </form>
        </div>
      </div>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        step: 1
      }
    },
    methods: {
      nextStep() {
        this.step++
      }
    }
  }

</script>

<style>

</style>
