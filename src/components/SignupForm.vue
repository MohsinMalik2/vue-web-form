<template>
  <form class="text-start" @submit.prevent="handleSubmit">
    <div class="mb-3">
      <label for="email" class="form-label">Email address</label>
      <input
        type="email"
        class="form-control"
        id="email"
        aria-describedby="emailHelp"
        required
        v-model="email"
      />
    </div>
    <div class="mb-3">
      <label for="password" class="form-label">Password</label>
      <input type="password" class="form-control" id="password" required v-model="password"/>
      <small v-if="passwordError" class="text-danger">{{passwordError}}</small>
    </div>
    <div class="mb-3">
        <label for="role" class="form-label">Role</label>
        <select class="form-select" id="role" v-model="role">
            <option value="developer">Web Developer</option>
            <option value="designer">Web Designer</option>
            <option value="operator">Web Operator</option>
        </select>
    </div>
    <div class="mb-3 form-check">
      <input type="checkbox" class="form-check-input" id="terms" required v-model="terms"/>
      <label class="form-check-label" for="terms">Accept terms & conditions</label>
    </div>
    <button class="btn btn-primary">Submit</button>
  </form>
  <div class="row">
      <div class="col-md-12 text-center">
         <p>Email: {{email}}</p>
          <p>Password: {{password}}</p>
            <p> Role: {{role}}</p>
            <p> Terms: {{terms}}</p>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return {
            email: '',
            password: '',
            role: 'operator',
            terms: false,
            passwordError : ''
        }
    },
    methods:{
        handleSubmit(){
            console.log('form submitted');

            //validating password

            this.passwordError = this.password.length > 5 ? '' : "Password Strength must be more than 5"

            if(!this.passwordError){
                console.log(this.email);
                console.log(this.password);
                console.log(this.role);
                console.log(this.terms);
            }
        }
    }
};
</script>

<style>
</style>