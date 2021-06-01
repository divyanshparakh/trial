<template>
  <form id="lr">
    <input
      type="text"
      name="firstname"
      placeholder="First Name"
      autofocus
      required
      v-if="F"
      v-model="firstname"
    />
    <input
      type="text"
      name="lastname"
      placeholder="Last Name"
      required
      v-if="F"
      v-model="lastname"
    />
    <input
      type="email"
      name="email"
      placeholder="E-mail or Username"
      autofocus
      required
      v-model="email"
    />
    <input
      type="date"
      id="dob"
      name="dob"
      placeholder="DD/MM/YYYY"
      value="11/05/1999"
      max="1950-1-1"
      required
      v-if="F"
      v-model="dob"
    />
    <select name="country" v-if="F" v-model="country">
      <option
        v-for="(Country, index) in Countries"
        :key="index"
        value="Country.code"
        >{{ Country.name }}</option
      >
    </select>
    <input
      type="tel"
      name="mobile"
      placeholder="Mobile Number"
      required
      v-if="F"
      v-model="mobile"
    />
    <input
      type="tel"
      maxlength="4"
      name="otp"
      placeholder="OTP"
      v-if="F == true && verified == false"
      v-model="otp"
      @focus="verify()"
    />
    <input
      type="password"
      name="password"
      placeholder="Password"
      required
      v-model="password1"
    />
    <input
      type="password"
      name="password"
      placeholder="Confirm Password"
      required
      v-if="F"
      v-model="password2"
    />
    <button
      type="submit"
      name="Register"
      v-if="F"
      @submit="SubmitCheck(), Register()"
    >
      Register
    </button>
    <button type="submit" name="login" v-else @submit="Login()">Login</button>
  </form>
</template>

<script>
import Countries from "@/assets/Countries.json";

export default {
  components: {},
  props: ["F"],
  data() {
    return {
      firstname: "",
      lastname: "",
      email: "",
      dob: "",
      country: "",
      mobile: "",
      otp: "",
      password1: "",
      password2: "",
      verified: false,
      Countries: Countries,
      passwordmatch: false
    };
  },
  computed: {},
  methods: {
    verify() {
      console.log("Function Executed");
      this.verified = true;
    },
    SubmitCheck() {
      if (this.password1 === this.password2) {
        this.passwordmatch = true;
      }
    },
    Login() {
      console.log("Logged In!");
    },
    Register() {
      console.log("Registered!");
    }
  },
  created() {},
  mounted() {}
};
</script>

<style lang="scss" scoped>
#lr {
  display: flex;
  flex-flow: column wrap;
  align-content: space-around;
  align-items: center;
  font-size: 16px;
  input,
  select {
    margin: 2px;
    background: lightyellow;
    border: none;
    text-align: center;
    height: 2em;
    width: 20em;
    color: #ff3800;
  }
  #dob {
    color: hsla(13, 100%, 50%, 0.6);
  }
  button {
    margin-top: 2em;
    width: 20em;
    height: 2em;
    background-color: #ff3800;
    border: none;
    color: hsl(13, 0%, 100%);
  }
}

@media only screen and (min-width: 600px) {
  /* For tablets: */
  #lr {
    font-size: 18px;
  }
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
  #lr {
    font-size: 50px;
    padding: 20px;
    input,
    select {
      height: 2.5em;
      margin: 3px;
      &:focus {
        z-index: 1;
        transform: scaleX(1.2);
      }
    }
  }
}
</style>
