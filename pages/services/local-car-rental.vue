<template>
  <div class="my-5 pt-2 lh-lg">
    <section class="page_header">
      <div class="container py-5">
        <div class="row">
          <div class="col-md-6">
            <form-wizard
              class="rounded-7 w-100"
              v-if="!submitted"
              @submit.prevent="submitEnquiryForm"
            >
              <tab-content title="Trip Information" :selected="true">
                <div class="form-group row">
                  <div class="col">
                    <label for="fromCity">From City</label>
                    <input
                      id="fromCity"
                      type="text"
                      class="form-control"
                      placeholder="e.g; Kolkata"
                      v-model="form.data.fromCity"
                      required
                    />
                  </div>
                  <div class="col">
                    <label for="toCity">To City</label>
                    <input
                      id="toCity"
                      type="text"
                      class="form-control"
                      placeholder="e.g; Kolkata"
                      v-model="form.data.toCity"
                      required
                    />
                  </div>
                </div>
                <div class="form-group row mt-3">
                  <div class="col">
                    <label for="pickupDate">Pickup Date</label>
                    <input
                      id="pickupDate"
                      type="date"
                      class="form-control"
                      v-model="form.data.pickupDate"
                      required
                    />
                  </div>
                  <div class="col">
                    <label for="returnDate">Return Date</label>
                    <input
                      id="returnDate"
                      type="date"
                      class="form-control"
                      v-model="form.data.returnDate"
                      required
                    />
                  </div>
                </div>
              </tab-content>

              <tab-content title="Your Information">
                <div class="form-group row">
                  <div class="col">
                    <label for="name">Name</label>
                    <input
                      id="name"
                      type="text"
                      class="form-control"
                      placeholder="Full Name"
                      v-model="form.name"
                      required
                    />
                  </div>
                  <div class="col">
                    <label for="email">Email Address</label>
                    <input
                      id="email"
                      type="email"
                      class="form-control"
                      placeholder="Email Address"
                      v-model="form.email"
                      required
                    />
                  </div>
                </div>
                <div class="form-group row mt-3">
                  <div class="col">
                    <label for="phoneNumber">Phone Number</label>
                    <input
                      id="phoneNumber"
                      type="tel"
                      class="form-control"
                      placeholder="Phone Number"
                      v-model="form.phone_number"
                      required
                    />
                  </div>
                  <div class="col">
                    <label for="query">Query (optional)</label>
                    <textarea
                      v-model="form.query"
                      class="form-control"
                      id="query"
                      rows="1"
                      placeholder="Type your query (optional)"
                    ></textarea>
                  </div>
                </div>
              </tab-content>
            </form-wizard>
            <div
              v-if="submitted"
              class="card bg-white d-flex align-items-center py-5"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="150"
                height="150"
                fill="currentColor"
                class="bi bi-check2-circle text-success"
                viewBox="0 0 16 16"
              >
                <path
                  d="M2.5 8a5.5 5.5 0 0 1 8.25-4.764.5.5 0 0 0 .5-.866A6.5 6.5 0 1 0 14.5 8a.5.5 0 0 0-1 0 5.5 5.5 0 1 1-11 0z"
                />
                <path
                  d="M15.354 3.354a.5.5 0 0 0-.708-.708L8 9.293 5.354 6.646a.5.5 0 1 0-.708.708l3 3a.5.5 0 0 0 .708 0l7-7z"
                />
              </svg>
              <p class="fs-1 text-center fw-bold text-dark mt-4">
                Submitted Successfully!
              </p>
            </div>
          </div>
          <div class="col-md-6"></div>
        </div>
      </div>
    </section>

    <section class="my-5 py-3 py-md-4 container">
      <h2 class="fw-bold mb-4">Local Car Rental</h2>
      <div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quo,
          excepturi aspernatur explicabo quaerat quas libero voluptatem
          consequatur laboriosam sed unde aut in tempora eum illo ut ab culpa
          corrupti natus?
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro,
          laboriosam? Quaerat repellat possimus dolores, quod voluptatem ullam.
          Ratione, doloribus, iure quia itaque odio qui obcaecati corporis quod,
          pariatur tempore consequuntur!
        </p>
      </div>
    </section>

    <Rates />
  </div>
</template>

<script>
import { FormWizard, TabContent } from "vue-step-wizard";
import "vue-step-wizard/dist/vue-step-wizard.css";
import axios from "axios";
export default {
  name: "LocalCarRental",
  components: {
    FormWizard,
    TabContent,
  },
  data() {
    return {
      form: {
        name: "",
        email: "",
        phone_number: "",
        query: "",
        data: {
          fromCity: "",
          toCity: "",
          pickupDate: "",
          returnDate: "",
        },
      },
    };
  },
  methods: {
    async submitEnquiryForm() {
      let that = this;
      await axios
        .post("https://crm.nullstacktechnologies.com/ucs/enquiry/", this.form)
        .then(function (response) {
          that.submitted = true;
        })
        .catch(function (error) {
          alert("Error in Form");
          that.submitted = false;
        });
    },
  },
};
</script>

<style scoped>
.page_header {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("/bg_top.webp");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
