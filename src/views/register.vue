<template>
  <section id="register">
    <div class="container">
      <div class="shadow p-3">
        <div class="row justify-content-center align-content-center">

          <h2 class="p-3 text-center">𝚁𝚎𝚐𝚒𝚜𝚝𝚎𝚛 𝙿𝚊𝚐𝚎</h2>
          <form  @submit.prevent="register">
            <div class="mb-3">
              <label class="form-label">𝙽𝚊𝚖𝚎 :</label>
              <input v-model="fname" type="text" class="form-control" required />
            </div>

            <div class="mb-3">
              <label for="exampleInputEmail1" class="form-label">𝙴𝚖𝚊𝚒𝚕 𝙰𝚍𝚍𝚛𝚎𝚜𝚜 :</label>
              <input v-model="email" type="email" class="form-control" required />
            </div>

            <div class="mb-3">
              <label class="form-label">𝙿𝚊𝚜𝚜𝚠𝚘𝚛𝚍</label>
              <input v-model="password" type="password" class="form-control" required />
            </div>

            <div class="row mx-auto justify-content-center">
              <button type="submit" class="btn">
                𝚂𝚞𝚋𝚖𝚒𝚝
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      fname: "",
      email: "",
      password: "",
    };
  },
  methods: {
    register() {
      const payload = {
        userFname: this.fname,
        email: this.email,
        password: this.password,
        cart: null,
        userLname: '',
        userType: 'user',
        phoneNumber: ""
      };
      this.$store.dispatch("register", payload);
    },
  },
};
</script>

<style scoped>
form {
  margin-top: 60px;
  /* width:600px; */
  /* height:500px */
  margin-bottom: 60px;
}

#register {
  height: 80vh
}

label,
.btn,
h2 {
  font-weight: bold
}

.container {
  padding-bottom: 40px;
  padding-top: 40px
}

.btn {
  background-color: gray;
  color: white;
  width: 200px
}

.btn:hover {
  background-color: var(--color-);
  color: black;
}
</style>
