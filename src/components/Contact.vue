<template>
  <div>
    <h1 class="aboutBA d-flex justify-content-center align-items-center m-5">Contact Us</h1>
    <div class="d-flex justify-content-around flex-row">
      <div class="w-300 d-flex flex-column">
        <h3>Свежест 42</h3>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vitae cupiditate porro corrupti, magnam delectus perspiciatis libero tenetur expedita quod adipisci sunt itaque aspernatur fuga explicabo nisi repellendus similique esse maiores!</p>
        <a href>
          <i class="fab fa-facebook-square">Facebook</i>
        </a>
      </div>
      <div class="d-flex flex-column">
        <div class="d-flex mt-2 flex-row align-items-center">
          <i class="fas mr-2 fa-map-marker-alt"></i>
          <p>Burgas, Karnobat,</p>
        </div>
        <div class="d-flex mt-2 flex-row align-items-center">
          <i class="fas mr-2 fa-phone-volume"></i>
          <a href="tel:+359889456119">0889 456 119</a>
        </div>
        <div class="d-flex mt-2 flex-row align-items-center">
          <i class="fas mr-2 fa-file-contract"></i>
          <a href>общи условия</a>
        </div>
        <div class="d-flex mt-2 flex-row align-items-center">
          <i class="fas mr-2 fa-user-tie"></i>
          <a href>защита на личните данни</a>
        </div>
      </div>
      <div>
        <b-form @submit="onSubmit" @reset="onReset" v-if="show">
          <b-form-group
            id="input-group-1"
            label="Email address:"
            label-for="input-1"
            description="We'll never share your email with anyone else."
          >
            <b-form-input
              id="input-1"
              v-model="form.email"
              type="email"
              required
              placeholder="Enter email"
            ></b-form-input>
          </b-form-group>

          <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
            <b-form-input id="input-2" v-model="form.name" required placeholder="Enter name"></b-form-input>
          </b-form-group>

          <b-form-group id="input-group-3" label="Subject:" label-for="input-3">
            <b-form-input id="input-3" v-model="form.subject" required placeholder="Enter subject"></b-form-input>
          </b-form-group>

          <b-form-group id="input-group-4" label="Message:" label-for="input-4">
            <b-form-textarea id="input-4" v-model="form.text" required placeholder="Enter subject"></b-form-textarea>
          </b-form-group>

          <b-button type="submit" variant="primary">Submit</b-button>
          <b-button type="reset" variant="danger">Reset</b-button>
        </b-form>
        <!-- <b-card class="mt-3" header="Form Data Result">
          <pre class="m-0">{{ form }}</pre>
        </b-card>-->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        email: "",
        name: "",
        subject: "",
        text: "",
      },

      show: true,
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(evt) {
      evt.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      (this.form.subject = ""), (this.form.text = "");
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    },
  },
};
</script>

<style scoped>
#input-4 {
  height: 100px;
  resize: none;
}
.fas,
.fab {
  font-size: 25px;
  color: #3498db;
  transition: 0.2s ease-in-out;
}
.fas:hover,
.fab:hover {
  color: #226b9c;
}
.w-300 {
  width: 300px;
}
.aboutBA::before {
  margin-right: 5px;
  content: "";
  width: 50px;
  height: 2px;
  background: #3498db;
  display: inline-block;
}
.aboutBA::after {
  margin-left: 5px;
  content: "";
  width: 50px;
  height: 2px;
  background: #3498db;
  display: inline-block;
}
</style>