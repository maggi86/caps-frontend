<template>
  <div class="profile">
    <div class="container">
      <div v-if="user">
        <div class="row mx-auto justify-content-center">
          <img :src="user.profile" class="user" alt="..."/>
          </div>
          <!-- https://i.postimg.cc/pd0mPrhg/alp-ancel-WKQt-X-SKFI-unsplash.jpg -->
          <div class="row mx-auto text-center">
          <h2>{{ user.fname }}</h2>
        </div>
            <form class="my-auto">
              <h2 class="text-center">πΌπ’ π³ππππππ</h2>

              <p class="text-center">
                <button
                  class="btn mt-5"
                  type="button"
                  data-bs-toggle="collapse"
                  data-bs-target="#collapseExample"
                  aria-expanded="false"
                >
                π΄πππ ππππ πΈππππππππππ
                </button>
              </p>

              <div class="collapse" id="collapseExample">
                <div class="card border-0 card-body">
                  <div class="mb-3">
                    <label for="firstname" class="form-label"
                      >π΅πππππππ :</label
                    >
                    <input
                      v-model="user.fname"
                      type="text"
                      class="form-control"
                      placeholder="π΄ππππ ππππ π΅πππππππ"
                      required
                    />
                  </div>

                  <div class="mb-3">
                    <label for="surname" class="form-label"
                      >πΏππππππ πππ» :</label
                    >
                    <input
                      v-model="user.profile"
                      type="text"
                      class="form-control"
                      placeholder="π΄ππππ πΈππππ πππ»"
                      required
                    />
                  </div>

                  <div class="mb-3">
                    <label for="email" class="form-label"
                      >π΄ππππ π΄ππππ π°ππππππ :</label
                    >
                    <input
                      v-model="user.email"
                      type="email"
                      class="form-control"
                      placeholder="π΄ππππ ππππ π΄ππππ π°ππππππ"
                      required
                    />
                  </div>
                  <div class="row mx-auto text-center">
                  <button
                    type="button"
                    class="btn my-3"
                    @click="this.$store.dispatch('editUser', user)"
                  >
                  ππππππ ππππ
                  </button>
                  </div>
                  <div class="row mx-auto text-center">
                  <button
                    type="button"
                    class="btn"
                    @click="this.$store.dispatch('deleteUser', user.id)"
                  >
                  π³πππππ π°ππππππ
                  </button>
                  </div>
                  
                </div>
              </div>
            </form>
      </div>
      <div v-else>
        <Loader/>
      </div>
    </div>
  </div>
</template>

<script>
  import Loader from "@/components/load.vue"
export default{
  components:{
    Loader
  },
  computed: {
    user() {
      return this.$store.state.user;
    },
  },
};
</script>

<style scoped>
img {
  height: 300px;
  width: 320px;
  aspect-ratio: 1;
}
label{
  color:rgb(210, 14, 70);
  font-size:18px;
  font-weight:bold
}
.btn{
  background-color:rgb(255, 255, 255);
  border-color:rgb(210, 14, 70);
  font-weight:bold;
  width:300px;
  color:rgb(210, 14, 70);
}
.btn:hover{
  background-color:rgb(210, 14, 70);
  color:white;
}
</style>
