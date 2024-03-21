<template>
  <div
    class="d-flex flex-column justify-content-center align-items-center"
    style="width: 100%; height: 100%"
  >
    <div class="card border rounded" style="width: 320px">
      <div class="card-body border rounded border-0 shadow">
        <div class="mb-5">
          <img
            class="border rounded border-0"
            src="/src/assets/img/8766d22f-ba58-4e9d-87c7-024691b61972_thumb.png"
            style="width: 100px"
          />
        </div>
        <div>
          <form method="post">
            <div class="border rounded d-flex mb-2">
              <select
                class="border-0 shadow-none form-select"
                style="height: 45px; width: 45px; margin-bottom: 0px; outline: none"
              >
                <option value="+250">Rwanda (+250)</option></select
              ><input
                class="border-0 shadow-none form-control"
                type="tel"
                id="input-number"
                placeholder="Your phone number"
                style="height: 45px; outline: none"
              />
            </div>
            <div>
              <button
                class="btn btn-primary"
                type="submit"
                style="width: 100%; background: #013854"
              >
                <span style="color: #ffcb05; font-weight: bold">Submit</span
                ><span
                  class="spinner-border spinner-border-sm"
                  role="status"
                  style="color: #ffcb05"
                ></span>
              </button>
            </div>
          </form>
          <span
            class="d-flex justify-content-center align-items-center"
            style="font-size: 13px; color: #ffcb05"
            ><i class="far fa-question-circle" style="margin-right: 3px"></i>Mobile Payment</span
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    clickMe() {
      alert('bien')
    }
  }
}
</script>
