<template>
  <nav class="navbar navbar-expand"> 
    <div class="container-fluid">
      <!-- <div v-if="user"> -->
        <router-link  to="/profile">
          <img v-if="user" :src="user.profile" class="user" style="height:70px; width:70px" />
          <!-- <img v-else :src="user.profile.null" class="user" style="height:70px; width:70px"> -->
        </router-link>
      <!-- </div> -->

      <img
        class="logo"
        src="https://i.postimg.cc/Y94tKXzc/Screenshot-2022-08-25-114500-3-removebg-preview.png"
      />

      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
      >
        <span class="navbar-toggler-icon"><i class="bi bi-list"></i> </span>
      </button>

      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <div class="d-flex" v-if="user">
            <!-- <li class="nav-item">
              <router-link to="/">
                <img
                src="https://i.postimg.cc/Y94tKXzc/Screenshot-2022-08-25-114500-3-removebg-preview.png"
                />
              </router-link>
            </li> -->

            <li class="nav-item">
              <router-link to="/cart">
                <a class="nav-link"><i class="bi bi-cart2 m-1"></i>𝙲𝚊𝚛𝚝</a>
              </router-link>
            </li>

            <li class="nav-item">
              <router-link to="/">
                <a class="nav-link" @click="logout"
                  ><i class="bi bi-box-arrow-right"></i>𝙻𝚘𝚐𝚘𝚞𝚝</a
                >
              </router-link>
            </li>
          </div>
          <div class="d-flex" v-else>
            <li class="nav-item">
              <router-link to="/login">
                <a class="nav-link"><i class="bi bi-person"></i>𝙻𝚘𝚐𝚒𝚗 </a>
              </router-link>
            </li>
          </div>
        </ul>
      </div>
    </div>
  </nav>

  <!-- <div class="container">
    <div class="row">
      <div class="col my-auto ms-4">
        <router-link to="/login">
          <a><i class="bi bi-person"></i>𝙻𝚘𝚐𝚒𝚗 </a>
        </router-link>
        <router-link to="/register">
          <a><i class="bi bi-person"></i>register </a>
        </router-link>
      </div>
      <div class="col lead text-center me-5">
        <img
          src="https://i.postimg.cc/Y94tKXzc/Screenshot-2022-08-25-114500-3-removebg-preview.png"
        />
      </div>
      <div class="col my-auto lead text-end"> -->
  <!-- <router-link to="/wishlist">
        <a><i class="bi bi-heart m-1"></i>𝚆𝚒𝚜𝚑  𝙻𝚒𝚜𝚝</a>
      </router-link> -->
  <!-- <router-link to="/cart">
          <a class="mx-3"><i class="bi bi-cart2 m-1"></i>𝙲𝚊𝚛𝚝</a>
        </router-link>
      </div> -->

  <!-- <button class="btn" @click="logout">
        logout
      </button> -->
  <!-- <router-link :to="name='contact'">
          <a> contact </a>
      </router-link> -->
  <!-- </div>
  </div> -->
</template>

<script>
export default{
  computed: {
    user() {
      return this.$store.state.user;
    },
  },

  methods: {
    logout() {
      this.$store.state.token = null;
      this.$store.state.user = null;
      this.$store.state.cart = null;
      localStorage.clear();
    },
  },
};
</script>

<style scoped>
.container {
  /* height:70px; */
  max-width: 100%;
  /* background-color: rgb(0, 0, 0); */
  background-size: cover;
  --bs-gutter-x: 0rem;
  position: fixed;
  z-index: 1;
  overflow: hidden;
  /* margin-left:20px */
}
.user{
  height:70px;
  width:73px;
  aspect-ratio:1;
  margin-top:0px;
}
/* #img {
  height: 70px;
  width: 70px;
  aspect-ratio: 1;
  margin-top: 0px;
  margin-left: 1%;
} */
a {
  text-decoration: none;
  color: rgb(94, 93, 93);
  /* text-decoration-line:unset; */
  font-size: 20px;
  font-weight: bold;
  /* margin: auto; */
}
a:hover {
  color: rgb(210, 14, 70);
}
span{
  color:white
}
img {
  margin-top: 10px;
  height: 70px;
  width: 230px;
  /* margin-left:4%; */
  border-width:1px;
  border-radius: 50%;
  /* margin-right:auto; */
}
.logo {
  margin-left: 36%;
}
nav {
  background-color: rgba(224, 221, 221, 0);
  height: 70px;
}
/* .row {
  height: 60px;
  max-width: 100%;
  background-size: cover;
  box-shadow: 0px 5px 25px var(--color-secondary);
  backdrop-filter: blur(5px);
  background-color: var(--color-);
  padding: 0px;
  border-radius: 0;
} */
@media screen and (max-width:950px){
  .logo{
    margin-left:30%
  }
}
@media screen and (max-width: 735px) {
  a {
    font-size: 15px;
  }
  .logo {
    margin-left: 20%;
  }
}
@media screen and (max-width:595px){
  .logo{
    margin-left: 15%;
  }
  img{
    height: 60px;
  width: 180px;
  }
}
@media screen and (max-width:495px){
  .logo{
    margin-left: 10%;
  }
  img{
    height: 50px;
  width: 160px;
  }
  #img{
    height:60px;
    width:60px
  }
}
@media screen and (max-width:350px){
  .logo{
    height:0px;
    width:0px;
  }
}

</style>
