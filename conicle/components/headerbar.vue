<template>
  <div>
    <!-- <div class="line "></div> -->
    <el-menu
      :default-active="activeIndex2"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
      background-color="#FF0712"
      text-color="#fff"
      active-text-color="#fff"
    >
      <el-menu-item index="1">Menu</el-menu-item>
      
      <el-menu-item index="2">
        <img class="logo" :src="require(`../assets/${logox}`)" />
      </el-menu-item>
      <!-- flex-grow -->

      <el-menu-item index="3">
        <el-input
          placeholder="Type something"
          prefix-icon="el-icon-search"
          v-model="input2"
        >
        </el-input>
      </el-menu-item>

      <el-menu-item index="4">register</el-menu-item>

      <el-menu-item index="5" @click="dialogFormVisible = true">
        <i class="el-icon-arrow-right icon-bar"></i>
        login
      </el-menu-item>

      <el-submenu index="6">
        <template slot="title"></template>
        <el-collapse v-model="activeNames" @change="handleChange">
          <el-collapse-item title="Change Language" name="1">
            <div>English</div>
            <div>Thai</div>
          </el-collapse-item>
          <el-collapse-item title="Font size" name="2">
            <div>Normal</div>
            <div>Large</div>
            <div>Extra Large</div>
          </el-collapse-item>
        </el-collapse>
      </el-submenu>
    </el-menu>

    <!-- login popup-->
    <el-dialog :visible.sync="dialogFormVisible">
      <div>
        <img class="logo-login" :src="require(`../assets/${conicleX}`)" />
      </div>
      <div class="button-form">HRD PLATFORM System</div>
      <el-form :model="form">
        <div class="form">Username</div>
        <el-input
          v-model="form.name"
          autocomplete="off"
          placeholder="Username or Email"
        ></el-input>

        <div class="form">Password</div>
        <el-input
          v-model="form.name"
          autocomplete="off"
          placeholder="Password"
        ></el-input>
        <div class="form">
          <el-checkbox v-model="checked">Remember me</el-checkbox>
        </div>

        <el-button
          type="danger"
          @click="dialogFormVisible = false"
          class="button-form"
          >Login</el-button
        >
        <el-divider>OR</el-divider>
        <div class="form">
          <el-button
            @click="dialogFormVisible = false"
            class="button-form"
            style="background: white"
          >
            <img
              class="logo-button-login"
              :src="require(`../assets/${google_logo}`)"
            />
            Login with Google</el-button
          >
        </div>
        <div>
          <el-button
            @click="dialogFormVisible = false"
            class="button-form button-facebook form"
          >
            <img
              class="logo-button-login"
              :src="require(`../assets/${facebook_logo}`)"
            />
            Login with Facebook</el-button
          >
        </div>
      </el-form>
      <div class="button-form">
        Don't have an account? <el-link type="danger">Register</el-link>
      </div>
    </el-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1',
      input: '',
      activeNames: ['1'],
      dialogFormVisible: false,
      form: {
        name: '',
        region: '',
        date1: '',
        date2: '',
        delivery: false,
        type: [],
        resource: '',
        desc: '',
      },
      formLabelWidth: '120px',
      checked: true,
      logox: 'logoX.png',
      google_logo: 'google-logo.svg',
      facebook_logo: 'facebook-logo.svg',
      conicleX:'ConicleX.png'
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath)
    },
    handleChange(val) {
      console.log(val)
    },
  },
}
</script>

<style scoped>
.form {
  margin: 10px 0px;
}

.button-facebook {
  color: white;
  background: #3b579d;
}

.button-form {
  width: 100%;
  text-align: center;
}

.logo {
  width: 100%;
  height: 100%;
}

.logo-login{
  width: 100%;
  height: 100%;
  margin:auto;

}

.logo-button-login {
  max-width: 20px;
  max-height: 20px;
  width: 100%;
  height: 100%;
}

.icon-bar {
  color: white;
}
</style>
