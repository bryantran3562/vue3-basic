<template>

  <div>
    <pre>
          {{ JSON.stringify(formValues, null, 2) }}
    </pre>

  </div>




<form @submit="formSubmit">

  <label for="name">Name</label>
  <!--BT - You can add modifier - .trim to the v-model to remove all white space before and after a string -->
  <input type="text" v-model.trim="formValues.name">

  <br>

  <label for="profile">Profile</label>
  <textarea name="profile" id="profile" cols="30" rows="10" v-model="formValues.profile"></textarea>

  <br>

  <label for="country">Select Country</label>

  <select name="country" id="country" v-model="formValues.country">
  <option value="singapore">singapore</option>
  <option value="india">India</option>
  <option value="vietnam">Vietnam</option>
  </select>

  <br>

  <label for="country">Job Country</label>

  <select name="job" id="job" multiple v-model="formValues.jobcountries">
  <option value="singapore">singapore</option>
  <option value="india">India</option>
  <option value="vietnam">Vietnam</option>
  </select>

  <div>
    <input type="checkbox" v-model="formValues.remoteWork" true-value = "yes" false-value="no">
    <label for="remoteWork">Remote Work ?</label>
  </div>


  <div>
      <label for="skillSet">Skill Sets</label>
      <br>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillSet">
      <label for="html">HTML</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillSet">
      <label for="css">CSS</label>
      <!--BT - You need to have the value set, so that it can store it in the array. Otherwise, it doesn't know what value to store -->
      <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet">
      <label for="javascript">JAVASCRIPT</label>

  </div>

  <div>
      <label for="yearOfExperience">Year of Experience</label>
      <br>
      <input type="radio" id="0-2" value="0-2" v-model="formValues.yearOfExperience">
      <label for="0-2">0-2 years</label>
      <input type="radio" id="2-5" value="2-5" v-model="formValues.yearOfExperience">
      <label for="2-5">2-5 years</label>
      <input type="radio" id="10" value="10" v-model="formValues.yearOfExperience">
      <label for="10">10 years</label>

  </div>

  <div>
    <button>Submit</button>
  </div>
</form>

</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {

  name: 'App',

  data(){
    return {

      formValues: {
        name: '',
        profile: '',
        jobcountries: [],
        remoteWork: "no",
        skillSet: [],
        yearOfExperience: ''
      }
    }
    },
  methods: {
        formSubmit(event){
          //BT - Because when you click on the 'Submit' button, the browser will refresh the page. We don't want it.
          event.preventDefault()
          console.log(this.formValues)

        }
    }
  

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
