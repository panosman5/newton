<template>
  <div id="main" class="wrapper style3">
    <div class="container medium">
      <header class="major">
        <h2>Technical Documents</h2>
        <p>Technical Documents regarding Newton can be found here</p>
      </header>

      <div class="box alt">
        <!--<div class="row gtr-uniform gtr-200">--> 
          <div class="col-12-medium">
           
            <section class="feature" style="width=100%">
              <span class="icon solid major fa-file-pdf"></span>

              <span class="image right"
                ><a href="#" target="_blank"
                  ><img
                    src="@/assets/images/conferences/tecdoc1.png"
                    alt="" /></a
              ></span>
              <h3>Science Requirement Baseline</h3>
              <p style="text-align: justify"></p>
            </section>
          </div>
          
        <!--</div>-->
      </div>
      <br><br><br><br>
      <header class="major">
        <p>Complete the form to request access to the Technical Documents</p>
      </header>

      <!-- Content -->
      <section id="content">
        <FormulateForm
          @submit="submitHandler"
          method="post"
          #default="{ hasErrors }"
        >
          <div class="row gtr-uniform">
            <div class="col-6 col-12-xsmall">
              <FormulateInput
                type="text"
                v-model="applicant.name"
                id="name"
                placeholder="Name*"
                validation="required"
              />
            </div>
            <div class="col-6 col-12-xsmall">
              <FormulateInput
                type="text"
                v-model="applicant.surname"
                id="surname"
                placeholder="Surname*"
                validation="required"
              />
            </div>
            <div class="col-12">
              <FormulateInput
                type="email"
                v-model="applicant.email"
                id="email"
                placeholder="Email*"
                validation="required|email"
              />
            </div>
            <div class="col-12">
            <FormulateInput
              v-model="applicant.options"
              :options="{
                first: 'Science Requirement Baseline',
                second: 'To be added soon',
              }"
              type="select"
              placeholder="Select Technical Documents"
              label="Select the Documents you want access to."
            />
            </div>
            <div class="col-12">
              <FormulateInput
                type="text"
                v-model="applicant.institution"
                id="institution"
                placeholder="Institution*"
                validation="required"
              />
            </div>
            <div class="col-12">
              <textarea
                v-model="applicant.message"
                id="message"
                placeholder="Enter why you need access*"
                rows="6"
                validation="required"
              ></textarea>
            </div>
            <p><i>The fields with an asterisk are required fields</i></p>
            <div class="col-12">
              <ul class="actions special">
                <li>
                  <input
                    type="submit"
                    value="Request Access"
                    class="primary"
                    :disabled="hasErrors"
                  />
                </li>
              </ul>
            </div>
          </div>
        </FormulateForm>
      </section>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import VueAxios from "vue-axios";
import Vue from "vue";
Vue.use(VueAxios, axios);
export default {
  data() {
    return {
      applicant: {
        name: null,
        surname: null,
        email: null,
        institution: null,
        message: null,
        messageError: null,
      },
    };
  },

  methods: {
    submitHandler() {
      this.axios
        .post("http://localhost:3003/data", this.applicant)
        .then((response) => {
          console.warn(response);
        });

      console.log("Email: ", this.applicant.email);
      console.log("Name: ", this.applicant.name);
      console.log("Surname: ", this.applicant.surname);
      console.log("Chosen Document: ", this.applicant.options);
      console.log("Institution: ", this.applicant.institution);
      console.log("Message ", this.applicant.message);
    },
  },
};
</script>

<style>
</style>