<template>
  <section id="login">
    <div class="container">
      <div class="shadow p-3">
      <div class="row mx-auto justify-content-center align-content-center">
        
          <h2 class="p-3 text-center">π»ππππ πΏπππ</h2>
          <div class="mb-3">
            <label class="form-label"
              >π΄ππππ π°ππππππ</label
            >
            <input
              v-model="email"
              type="email"
              class="form-control"
            />
            <div class="form-text">
              ππ'ππ πππππ πππππ π’πππ πππππ π πππ πππ’πππ ππππ.
            </div>
          </div>
          <div class="mb-3">
            <label class="form-label"
              >πΏππππ πππ</label
            >
            <input
              v-model="password"
              type="password"
              class="form-control"
            />
          </div>
          <div class="text">
            <router-link to="/register">
              <span>π³πππ ππππ ππ πππππππ?
              ππππ-ππ ππππ</span>
            </router-link>
          </div>
          <div v-if="msg">
            {{msg}}
          </div>
          
        </div>
        <div class="row mx-auto justify-content-center">
            <button type="button" @click="login" class="btn">
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
      email: "",
      password: "",
    };
  },
  computed: {
    msg() {
      return this.$store.state.msg
    }
  },
  methods: {
    login() {
      const payload = {
        email: this.email,
        password: this.password,
      };
      this.$store.dispatch("login", payload);
    },
  },
};
</script>

<style scoped>
#login{
  height:80vh
}
form {
  margin-top:60px;
  /* width:600px; */
  /* height:500px */
  margin-bottom:40px;
}
label ,.btn , h2{
  font-weight:bold
}
.btn{
  background-color:gray;
  color:white;
  width:200px;
  height:40px;
  padding-bottom:20px;
}
.btn:hover{
  background-color:var(--color-);
  color:black;
}
.container{
  padding-bottom:40px;
  padding-top:40px
}
a{
  text-decoration:none;
  color:#6c757d;
}
.text{
  padding-bottom:10px;
}
@media screen and (max-width:767px){
  .row {
    width:500px
  }
}
@media screen and (max-width:690px){
  .row {
    width:390px
  }
}
@media screen and (max-width:430px){
  .row {
    width:280px
  }
}
</style>
