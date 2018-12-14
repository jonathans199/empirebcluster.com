<template>
  <section class="contact__container">
    <!-- <img src="@/assets/img/contact.png" class="contact__img" alt=""> -->
      <div class="contact_form"> 
        <div class="container">
          <h1 class="col-12 text-center mb-5">CONTACT US</h1>
          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ad laudantium iste necessitatibus </p>
         
          <b-form-group inline class="contact_form-group"  label-for="elementsAppend" >
            <b-input-group>
              <b-form-input placeholder="EMAIL"  type="text" ></b-form-input>
            </b-input-group>
          </b-form-group>
          <b-form-group class="contact_form-group" label-for="elementsAppend" >
            <b-input-group>
              <b-form-input placeholder="NAME"  type="text" ></b-form-input>
            </b-input-group>
          </b-form-group>
          <!-- <b-form-group class="contact_form-group"  label-for="elementsAppend" >
            <b-input-group>
              <b-form-input placeholder="PHONE" type="text" ></b-form-input>
            </b-input-group>
          </b-form-group> -->
          <b-form-group class="contact_form-group"  label-for="elementsAppend" >
            <b-input-group>
              <b-form-textarea placeholder="YOUR MESSAGE" type="text-area" :rows="9" ></b-form-textarea>
            </b-input-group>
          </b-form-group>
          <div class="col-6 contact_form-group contact_form-submit" label-for="elementsAppend" >
            <button class="contact_form-button">
              <span class="contact_form-button-text">Send Message</span>
            
            </button>
          </div>
        </div>
      </div>
  </section>
</template>


<script>
export default {
  name:'Contact',

  data(){
    return {
      form: {}
    }
  }
}
</script>
