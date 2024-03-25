<template>
  <div
    class="d-flex flex-column justify-content-center align-items-center"
    style="width: 100%; height: 100%"
  >
    <div class="card border rounded" style="width: 320px">
      <div class="card-body border rounded border-0 shadow">
        <div class="border rounded border-0" style="font-weight: bold">
          <div class="d-flex align-items-center">
            <span style="color: #013854; text-decoration: underline; font-family: Inter, sans-serif"
              >MPay</span
            >
          </div>
        </div>
        <div>
          <form method="post" @submit.prevent="submit">
            <div class="border rounded d-flex align-items-center mb-2" style="width: 100%">
              <div
                class="d-flex"
                style="
                  border-right: 1px solid var(--bs-dark-bg-subtle);
                  padding-right: 10px;
                  padding-left: 10px;
                "
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="-32 0 512 512"
                  width="1em"
                  height="1em"
                  fill="currentColor"
                  class="text-light-emphasis"
                >
                  <!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2023 Fonticons, Inc. -->
                  <path
                    d="M224 256A128 128 0 1 0 224 0a128 128 0 1 0 0 256zm-45.7 48C79.8 304 0 383.8 0 482.3C0 498.7 13.3 512 29.7 512H418.3c16.4 0 29.7-13.3 29.7-29.7C448 383.8 368.2 304 269.7 304H178.3z"
                  ></path>
                </svg>
              </div>
              <input
                class="border-0 shadow-none form-control"
                type="text"
                style="width: 100%; border-left-width: 1px; border-left-style: solid"
                placeholder="First name"
                v-model="form.first_name"
              />
            </div>
            <div class="border rounded d-flex align-items-center mb-2" style="width: 100%">
              <div
                class="d-flex"
                style="
                  border-right: 1px solid var(--bs-dark-bg-subtle);
                  padding-right: 10px;
                  padding-left: 10px;
                "
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="-32 0 512 512"
                  width="1em"
                  height="1em"
                  fill="currentColor"
                  class="text-light-emphasis"
                >
                  <!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2023 Fonticons, Inc. -->
                  <path
                    d="M224 256A128 128 0 1 0 224 0a128 128 0 1 0 0 256zm-45.7 48C79.8 304 0 383.8 0 482.3C0 498.7 13.3 512 29.7 512H418.3c16.4 0 29.7-13.3 29.7-29.7C448 383.8 368.2 304 269.7 304H178.3z"
                  ></path>
                </svg>
              </div>
              <input
                class="border-0 shadow-none form-control"
                type="text"
                style="width: 100%; border-left-width: 1px; border-left-style: solid"
                placeholder="Last name"
                v-model="form.last_name"
              />
            </div>
            <div class="border rounded d-flex align-items-center mb-2" style="width: 100%">
              <div
                class="d-flex"
                style="
                  border-right: 1px solid var(--bs-dark-bg-subtle);
                  padding-right: 10px;
                  padding-left: 10px;
                "
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 512 512"
                  width="1em"
                  height="1em"
                  fill="currentColor"
                  class="text-light-emphasis"
                >
                  <!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2023 Fonticons, Inc. -->
                  <path
                    d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"
                  ></path>
                </svg>
              </div>
              <input
                class="border-0 shadow-none form-control"
                type="email"
                style="width: 100%; border-left-width: 1px; border-left-style: solid"
                placeholder="Email"
                v-model="form.email"
              />
            </div>
            <div class="border rounded d-flex align-items-center mb-2" style="width: 100%">
              <div
                class="d-flex"
                style="
                  border-right: 1px solid var(--bs-dark-bg-subtle);
                  padding-right: 10px;
                  padding-left: 10px;
                "
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 512 512"
                  width="1em"
                  height="1em"
                  fill="currentColor"
                  class="text-light-emphasis"
                >
                  <!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2023 Fonticons, Inc. -->
                  <path
                    d="M164.9 24.6c-7.7-18.6-28-28.5-47.4-23.2l-88 24C12.1 30.2 0 46 0 64C0 311.4 200.6 512 448 512c18 0 33.8-12.1 38.6-29.5l24-88c5.3-19.4-4.6-39.7-23.2-47.4l-96-40c-16.3-6.8-35.2-2.1-46.3 11.6L304.7 368C234.3 334.7 177.3 277.7 144 207.3L193.3 167c13.7-11.2 18.4-30 11.6-46.3l-40-96z"
                  ></path>
                </svg>
              </div>
              <input
                class="border-0 shadow-none form-control"
                type="tel"
                style="width: 100%; border-left-width: 1px; border-left-style: solid"
                placeholder="Phone number"
                maxlength="9"
                v-model="form.phone_number"
              />
            </div>
            <div class="border rounded d-flex align-items-center mb-2" style="width: 100%">
              <div class="d-flex" style="width: 100%">
                <select
                  v-model="form.operator"
                  class="border-0 shadow-none form-select"
                  style="width: 100%"
                >
                  <optgroup label="Your operator">
                    <option value="CD_AIRTELMONEY" selected="">Airtel</option>
                    <option value="CD_ORANGEMONEY">Orange</option>
                    <option value="CD_AFRICELL">Africell</option>
                  </optgroup>
                </select>
              </div>
            </div>
            <div class="border rounded d-flex align-items-center" style="width: 100%">
              <div
                class="d-flex"
                style="
                  border-right: 1px solid var(--bs-dark-bg-subtle);
                  padding-right: 10px;
                  padding-left: 10px;
                "
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 -32 576 576"
                  width="1em"
                  height="1em"
                  fill="currentColor"
                  class="text-light-emphasis"
                >
                  <!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2023 Fonticons, Inc. -->
                  <path
                    d="M64 64C28.7 64 0 92.7 0 128V384c0 35.3 28.7 64 64 64H512c35.3 0 64-28.7 64-64V128c0-35.3-28.7-64-64-64H64zm64 320H64V320c35.3 0 64 28.7 64 64zM64 192V128h64c0 35.3-28.7 64-64 64zM448 384c0-35.3 28.7-64 64-64v64H448zm64-192c-35.3 0-64-28.7-64-64h64v64zM288 160a96 96 0 1 1 0 192 96 96 0 1 1 0-192z"
                  ></path>
                </svg>
              </div>
              <input
                class="border-0 shadow-none form-control"
                type="number"
                style="width: 100%; border-left-width: 1px; border-left-style: solid"
                placeholder="Amount"
                min="500"
                step="100"
                value="500"
                v-model="form.amount"
              />
            </div>
            <span v-if="error" style="color: red; font-size: 13px;">Invalid form</span>
            <div class="mt-2">
              <button
                class="btn btn-primary border-0 shadow"
                type="submit"
                style="width: 100%; background: #013854"
                :disabled="disabled"
              >
                <span style="color: #ffcb05; font-family: Inter, sans-serif" v-if="!disabled"
                  >Submit</span
                ><span
                  class="spinner-border spinner-border-sm"
                  role="status"
                  style="color: #ffcb05"
                  v-if="disabled"
                ></span>
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
// import ModalView from '../components/Modal.vue'
export default {
  data() {
    return {
      error: false,
      errors: [],
      disabled: false,
      form: {
        first_name: '',
        last_name: '',
        email: '',
        phone_number: '',
        operator: 'CD_AIRTELMONEY',
        amount: 5000
      },
      payment: Object
    }
  },
  methods: {
    validEmail (email) {
      var re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(email);
    },

    submit() {
      this.errors = []

      if (!this.form.first_name) {
        this.errors.push("first name required")
      }

      if (!this.form.last_name) {
        this.errors.push("last name required")
      }

      if (!this.form.email) {
        this.errors.push("email required")
      } else if (!this.validEmail(this.form.email)) {
        this.errors.push("valid email required")
      }

      if (!this.form.phone_number) {
        this.errors.push("phone required")
      }

      if (!this.form.operator) {
        this.errors.push("operator required")
      }

      if (!this.form.amount) {
        this.errors.push("amount required")
      }

      if (this.errors.length) {
        this.error = true
      } else {
        this.error = false
      } 

      if (!this.error) {
        this.disabled = true
        this.myPayment()
      }
    },

    myPayment() {
      axios
        .post('https://api.monetbil.com/payment/v1/placePayment', {
          service: 'WB1iADpNSjIsgDEnlulPf4DkIq4ARZiT',
          amount: this.form.amount,
          phonenumber: this.form.phone_number,
          country: 'CD',
          currency: 'CDF',
          first_name: this.form.first_name,
          last_name: this.form.last_name,
          email: this.form.email,
          notify_url: 'https://your.server.com/monetbil/notifications',
          operator: this.form.operator
        })
        .then((res) => {
          if (res.status == 200) {
            this.payment = res.data
            // console.log(this.payment)
          }
        })
        .catch((err) => {
          console.log(err)
        })

      // check the payment
      // if (this.payment.status == 'REQUEST_ACCEPTED') {

      // }
    },

    ckeckPayment() {
      axios
        .post('https://api.monetbil.com/payment/v1/checkPayment', {
          paymentId: this.payment.paymentId
        })
        .then((res) => {
          console.log(res)
        })
        .catch((err) => {
          console.log(err)
        })
    }
  }
}
</script>
