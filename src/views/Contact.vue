<template>
<div>
<h3 class=" mt-6 ml-12 pl-12">Advice, Questions, Pleasantries</h3>
<p class="ml-12 mt-2  pl-12 subtitle-1">Please reach out with job posting/company suggestions, available work opportunties, advice on tools and technologies, and general inquiries. </p>
    <div class="container mt-6">
        <form @submit.prevent="sendEmail">
          <label>Name</label>
          <input 
            type="text" 
            v-model="name"
            name="from_name"
            placeholder="Your Name"
          >
          <label>Email</label>
          <input 
            type="email" 
            v-model="email"
            name="reply_to"
            placeholder="Your Email"
            >
          <label>Message</label>
          <textarea 
            name="message"
            v-model="message"
            cols="30" rows="5"
            placeholder="Message">
          </textarea>
          
          <input type="submit" value="Send">
        </form>
    </div>
</div>
</template>

<script>
import emailjs from 'emailjs-com';
import{ init } from 'emailjs-com';
init("user_wiBfgefZ2EPLj4W73Y6ey");
export default {
  name: 'ContactUs',
  data() {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm('my_gmail', 'my_template', e.target, 'user_wiBfgefZ2EPLj4W73Y6ey', {
          from_name: this.from_name,
          reply_to: this.reply_to,
          message: this.message
        })
        console.log('it works!!!')
      } catch (error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  }
}
</script>

<style scoped>
* {box-sizing: border-box;}
label {
  float: left;
}
input[type=text], [type=email], textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid rgb(204, 204, 204);
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}
input[type=submit] {
  background-color: #26A69A;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
input[type=submit]:hover {
  background-color: #00897B;
}
.container {
  display: block;
  margin:auto;
  text-align: center;
  border-radius: 8px;
  background-color: #E0F2F1;
  padding: 20px;
  width: 50%;
}
</style>