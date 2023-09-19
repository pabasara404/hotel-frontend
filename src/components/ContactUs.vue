<template>
    <Navbar/>
    <div class="appBodyContact">
      <div class="leftBody">
        <form>
          <table>
            <tr>
              <td><label for="firstName">First Name *</label></td>
              <td><input type="text" id="firstName" v-model="formData.firstName"></td>
            </tr>
            <tr>
              <td><label for="lastName">Last Name *</label></td>
              <td><input type="text" id="lastName" v-model="formData.lastName"></td>
            </tr>
            <tr>
              <td><label for="email">Email *</label></td>
              <td><input type="text" id="email" v-model="formData.email"></td>
            </tr>
            <tr>
              <td><label for="message">Message *</label></td>
              <td><textarea id="message" v-model="formData.message" rows="5" cols="50"></textarea></td>
            </tr>
            <tr>
              <td colspan="2"><label for="additionalDetails">Additional Details</label></td>
            </tr>
            <tr>
              <td colspan="2"><textarea id="additionalDetails" v-model="formData.additionalDetails" rows="10" cols="70"></textarea></td>
            </tr>
            <tr>
                <td colspan="2"><button @click.prevent="submitForm">Submit</button></td>
            </tr>
          </table>
        </form>
      </div>
      <div class="rightBody">
        <h2>How Can We Help?</h2>
        <p>Please select a topic below related to your inquiry. If you don't find what you need, fill out our contact form.</p>
        <div class="card">
          <h4>Complain About Services</h4>
          <div class="para">Say What You Really Want to Say, We are Always Listening</div>
        </div>
        <hr>
        <div class="card">
          <h4>Ideas to Improve Ourselves</h4>
          <div class="para">We Have an Open Mind. Please Give Your Thoughts to Improve our Hotel.</div>
        </div>
        <hr>
        <div class="card">
          <h4>Become a Partner</h4>
          <div class="para">Join our Partner Program and Invest to Gain Profit.</div>
        </div>
        <hr>
      </div>
    </div>
  </template>
  
  <script>
  import Navbar from "./Navbar.vue";
  
  export default {
    components: {
      Navbar, // Register the Navbar component
    },
    data() {
      return {
        formData: {
          firstName: "",
          lastName: "",
          email: "",
          message: "",
          additionalDetails: "",
        },
      };
    },
    methods: {
      submitForm() {
        // Display the submitted data in an alert box
        const submittedData = JSON.stringify(this.formData, null, 2);
        alert(`Submitted Data:\n${submittedData}`);
  
        // Check if the data is correct (you can add your own validation logic)
        const isValid = this.validateFormData(this.formData);
  
        if (isValid) {
          // Handle form submission logic here (without sending emails)
          // For example, you can make an API request to your server to save the data.
        }
      },
      validateFormData(formData) {
        // Add your own validation logic here
        // For example, check if the required fields are filled correctly
        return (
          formData.firstName.trim() !== "" &&
          formData.lastName.trim() !== "" &&
          formData.email.trim() !== "" &&
          formData.message.trim() !== ""
        );
      },
    },
  };
  </script>
  
  <style scoped>
  .appBodyContact{
    display: flex;
    display:inline-flex;
    align-items: center;
    padding: 40px;
}
.leftBody{
    background-color: antiquewhite;
    padding: 80px;
    height: 395px;
    border-radius: 10px;
}
table {
    padding: 10px;
}
input[type=text] {
    border: 1px;
    border-bottom: 2px solid brown;
    margin-left: 10px;
    width: 100%;
    padding: 5px;
    background-color: antiquewhite;
  }
  input[type=text]:hover{
      background-color: rgb(224, 211, 193);
  }
  textarea{
      border:2px solid brown;
      width: 100%;
      background-color: antiquewhite;
      border-radius: 7px;

  }
  textarea:hover{
    background-color: rgb(224, 211, 193);
}
  button{
      padding: 10px;
      background-color: rgb(240, 198, 144);
      border-color: brown;
      border-radius: 5px;
      padding-left: 30px;
      padding-right: 30px;
  }
  button:hover{
    background-color: antiquewhite;

  }
.rightBody{
    padding-left: 50px;
}
.card{
    border-radius: 10px;
    padding: 10px;
    cursor: pointer;
}
.card h1{
    padding: 0 !important;
}
.card:hover{
    background-color: rgb(236, 233, 233);
}
  </style>
  