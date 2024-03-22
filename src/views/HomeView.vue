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
            <div>
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
          <div class="d-flex justify-content-end">
            <button
              class="btn btn-primary btn-sm bg-transparent border-0 d-flex align-items-center"
              type="button"
              style="padding: 0px; font-size: 12px; color: #013854; margin-top: 10px"
              data-bs-target="#about"
              data-bs-toggle="modal"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
                width="1em"
                height="1em"
                fill="currentColor"
                style="margin-right: 4px"
              >
                <!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License) Copyright 2023 Fonticons, Inc. -->
                <path
                  d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512zM169.8 165.3c7.9-22.3 29.1-37.3 52.8-37.3h58.3c34.9 0 63.1 28.3 63.1 63.1c0 22.6-12.1 43.5-31.7 54.8L280 264.4c-.2 13-10.9 23.6-24 23.6c-13.3 0-24-10.7-24-24V250.5c0-8.6 4.6-16.5 12.1-20.8l44.3-25.4c4.7-2.7 7.6-7.7 7.6-13.1c0-8.4-6.8-15.1-15.1-15.1H222.6c-3.4 0-6.4 2.1-7.5 5.3l-.4 1.2c-4.4 12.5-18.2 19-30.6 14.6s-19-18.2-14.6-30.6l.4-1.2zM224 352a32 32 0 1 1 64 0 32 32 0 1 1 -64 0z"
                ></path></svg
              >About
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <ModalView />
</template>

<script>
import axios from 'axios'
import ModalView from '../components/Modal.vue'
export default {
  components: {
    ModalView
  },
  data() {
    return {
      disabled: false,
      form: {
        first_name: 'elie',
        last_name: 'ruhamya',
        email: 'elieruhamya20@gmail.com',
        phone_number: '979411354',
        operator: 'CD_AIRTELMONEY',
        amount: 5000
      }
    }
  },
  methods: {
    submit() {
      this.disabled = true
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
          console.log(res)
        })
        .catch((err) => {
          console.log(err)
        })
    }
  }
}
</script>
