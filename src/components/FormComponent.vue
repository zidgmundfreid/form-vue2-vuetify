<template>
  <v-container>
    <v-form
      ><v-row>
        <v-col cols="12" md="6">
          <v-textarea
            prepend-inner-icon="mdi-account"
            class="mx-2 text-area"
            label="First Name"
            rows="1"
            color="#6CEEC7"
          ></v-textarea>
        </v-col>

        <v-col cols="12" md="6">
          <v-textarea
            prepend-inner-icon="mdi-human"
            class="mx-2 text-area"
            label="Last Name"
            rows="1"
            color="#6CEEC7"
          ></v-textarea>
        </v-col>

        <v-col cols="12" md="6">
          <v-select
            @change="getPhoneCode"
            v-model="e1"
            class="text-area"
            prepend-inner-icon="mdi-map"
            :items="countries"
            color="#6CEEC7"
            menu-props="auto"
            hide-details
            label="Country"
            single-line
          ></v-select>
        </v-col>

        <v-col cols="12" md="6">
          <v-textarea
            v-model="phoneCode"
            prepend-inner-icon="mdi-phone"
            class="mx-2 text-area"
            label="Phone"
            value="phoneCode"
            rows="1"
            color="#6CEEC7"
          ></v-textarea>
        </v-col>

        <v-col cols="12" md="6">
          <v-textarea
            prepend-inner-icon="mdi-lock"
            class="mx-2 text-area"
            label="Password"
            rows="1"
            color="#6CEEC7"
          ></v-textarea>
        </v-col>

        <v-col cols="12" md="6">
          <v-textarea
            prepend-inner-icon="mdi-lock"
            class="mx-2 text-area"
            label="Confirm password"
            rows="1"
            color="#6CEEC7"
          ></v-textarea>
        </v-col>
        
        <v-col cols="12" md="6">
          <v-textarea
            prepend-inner-icon="mdi-email"
            class="mx-2 text-area"
            label="Email"
            rows="1"
            color="#6CEEC7"
          ></v-textarea>
        </v-col>

        <v-col class="checkbox" cols="12" md="6">
          <v-checkbox color="#6ceec7" hide-details></v-checkbox>
          <p>I agree to the <a href="#">Terms & Conditions</a></p>
        </v-col>
      </v-row>
    </v-form>
  </v-container>
</template>

<script>

export default {
  data: () => ({
    e1: '',
    phoneCode: '',
    info: null,

    countries: ['Moldova', 'USA', 'Ukraine'],
    phoneCodes: ['+373', '+990', '+380'],
  }),
  methods: {
    getPhoneCode() {
      this.phoneCode = this.phoneCodes[this.countries.indexOf(this.e1)];
    },
  },
};
</script>

<style lang="scss">
.v-input__slot {
  border: 1px solid #ffffff;
  box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.3);
  border-radius: 5px !important;
  padding: 15px;
}
.v-input__slot:hover {
  border: 1px solid #6ceec7;
  padding: 15px;
}

.v-input__slot:before,
.v-input__slot:after {
  display: none;
}

.v-label {
  color: #e0e0e0 !important;
}

.v-label--active {
  color: #6ceec7 !important;
}

.v-text-field__slot > textarea {
  line-height: 2.2rem;
  color: #e0e0e0 !important;
}

.row > div {
  padding: 0;
}
.v-icon {
  color: #6ceec7 !important;
}

.v-list {
  width: 575px;
}

.v-menu__content {
  margin-left: 18px;
  width: 575px;
  min-width: 575px !important;
}
.v-input {
  margin: 4px 8px;
  padding: 10px 0;
}
.v-input__slot {
  margin: 0;
  height: 65px;
}

.v-select__selection {
  color: #e0e0e0 !important;
}
.checkbox {
  position: relative;
}

.checkbox > p {
  display: inline-block;
  position: absolute;
  top: 38px;
  left: 55px;
  font-weight: 300;
  font-size: 15px;
  line-height: 18px;
  color: #e0e0e0;
}

.checkbox > p > a {
  border-bottom: 1px solid #6ceec7;
  text-decoration: none;
  cursor: pointer;
  color: #6ceec7;
  transition: 0.4s ease-in all;
}

.checkbox > p > a:hover {
  border-bottom: 1px solid #e0e0e0;
}

#app > div > div.container > form > div > div.checkbox.col-md-6.col-12 > div > div > div {
  border: none;
  box-shadow: none;
}
</style>
