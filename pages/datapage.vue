<template>
  <div id="main" class="wrapper style3">
    <div class="container medium">
      <header class="major">
        <h2>Scientific Data</h2>
        <p>Complete the form to request access to the Scientific Data</p>
      </header>

      <!-- Content -->
      <section id="content">
        <FormulateForm @submit="submitHandler" #default="{ hasErrors }">
          <div class="row gtr-uniform">
            <div class="col-6 col-12-xsmall">
              <FormulateInput
                type="text"
                v-model="name"
                id="name"
                placeholder="Name*"
                validation="required"
              />
            </div>
            <div class="col-6 col-12-xsmall">
              <FormulateInput
                type="text"
                v-model="surname"
                id="surname"
                placeholder="Surname*"
                validation="required"
              />
            </div>
            <div class="col-12">
              <FormulateInput
                type="email"
                v-model="email"
                id="email"
                placeholder="Email*"
                validation="required|email"
              />
            </div>
            <div class="col-12">
              <FormulateInput
                type="text"
                v-model="institution"
                id="institution"
                placeholder="Institution*"
                validation="required"
              />
            </div>
            <div class="col-12">
              <textarea
                v-model="message"
                id="message"
                placeholder="Enter why you need access*"
                rows="6"
                validation="required"
              ></textarea>
              <div v-if="messageError" class = "error"> {{ messageError }} </div>
            </div>
            <p><i>The fields with an asterisk are required fields</i></p>
            <div class="col-12">
              <ul class="actions special">
                <li>
                    <input type="submit" value="Request Access" class="primary" :disabled="hasErrors"  />
                </li>
              </ul>
            </div>
          </div>
        </FormulateForm>
        <p>Name: {{name}}, Email: {{email}}, Text: {{ message }}</p>
      </section>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            surname: '',
            email: '',
            institution: '',
            message: '',
            messageError: ''
        }
    },
    methods: {
        submitHandler() {

            this.messageError = this.message.lenght > 20 ?
            '' : 'You have to enter a message'

            if(!this.messageError){
            console.log('Email: ', this.email)
            console.log('Name: ', this.name)
            console.log('Surname: ', this.surname)
            console.log('Institution: ', this.institution)
            console.log('Message ', this.message)
            }

            
        }
    }
   
};
</script>

<style>
.error{
    color:red;
    margin-top: 10px;
    font-size: 0.8em;
    font-weight: bold;
    font-style: italic;
}
</style>