<template>
  <!-- Modal -->
  <div
    class="modal fade"
    id="exampleModal"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">π°ππ πΏππππππ</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <form>
            <div class="mb-3">
              <label for="exampleInputPassword1" class="form-label"
                ><span>π</span>ππππ :</label
              >
              <input v-model="title" type="text" class="form-control" />
            </div>

            <div class="mb-3">
              <label class="form-label"><span>πΈ</span>ππππ πππ»</label>
              <input v-model="img" type="text" class="form-control" />
            </div>

            <div class="mb-3">
              <label class="form-label"><span>π²</span>πππππππ’</label>
              <input v-model="category" type="text" class="form-control" />
            </div>

            <div class="mb-3">
              <label class="form-label"><span>π³</span>ππππππππππ</label>
              <input v-model="description" type="text" class="form-control" />
            </div>

            <div class="mb-3">
              <label class="form-label"><span>πΏ</span>ππππ</label>
              <input v-model="price" type="number" class="form-control" />
            </div>
          </form>
        </div>
        <div class="modal-footer">
          <button
            type="button"
            class="btn"
            data-bs-dismiss="modal"
          >
          π²ππππ
          </button>
          <button type="button" @click="addProd" class="btn" data-bs-dismiss="modal">
            π°ππ πΏππππππ
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default{
  data() {
    return {
      title: "",
      img: "https://elitebba.com/wp-content/uploads/2017/04/default-image.jpg",
      category: "",
      description: "",
      price: 0,
    };
  },
  methods: {
    addProd() {
      const payload = {
        title: this.title,
        img: this.img,
        catergory: this.category,
        description: this.description,
        price: this.price,
      };
      this.$store.dispatch("addProd", payload);
    },
  },
};
</script>

<style scoped>
  h5{
    color:rgb(210, 14, 70);
    font-weight:bold;
  }
  label{
    font-weight:bold
  }
  span{
    color:rgb(210, 14, 70);
    font-size:20px;
  }

</style>
