<template>
  <section id="register">
    <div class="container">
      <div class="shadow p-3">
      <div
        class="row justify-content-center align-content-center"
      >
        
          <h2 class="p-3 text-center">ππππππππ πΏπππ</h2>
          <div class="mb-3">
            <label class="form-label">π½πππ :</label>
            <input v-model="fname" type="text" class="form-control" />
          </div>

          <div class="mb-3">
            <label for="exampleInputEmail1" class="form-label"
              >π΄ππππ π°ππππππ :</label
            >
            <input v-model="email" type="email" class="form-control" />
          </div>

          <div class="mb-3">
            <label class="form-label"
              >πΏππππ πππ</label
            >
            <input v-model="password" type="password" class="form-control" />
          </div>
       
        </div> 
        <div class="row mx-auto justify-content-center">
          <button type="button" @click="register" class="btn">
            ππππππ
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default{
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
        fname: this.fname,
        email: this.email,
        password: this.password,
      };
      this.$store.dispatch("register", payload);
    },
  },
};
</script>

<style scoped>
form {
  margin-top:60px;
  /* width:600px; */
  /* height:500px */
  margin-bottom:60px;
}
#register{
  height:80vh
}
label ,.btn , h2{
  font-weight:bold
}
.container{
  padding-bottom:40px;
  padding-top:40px
}
.btn{
  background-color:gray;
  color:white;
  width:200px
}
.btn:hover{
  background-color:var(--color-);
  color:black;
}
</style>
