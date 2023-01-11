<script>
// import Button from '../reusable/Button.vue';
// export default { components: { Button } };
// import emailjs from "@emailjs/browser";

export default {
  name: "ContactForm",
  components: {
    // Button
  },
  data() {
    return {
      from_name: "",
      email: "",
      subject: "",
      message: "",
    };
  },
  methods: {},
};
</script>

<template>
  <div class="">
    <!-- <p class="font-general-regular text-gray-500 text-md mb-8">
        Please fill out the form to create your custom package.
      </p> -->
    <form
      ref="form"
      class="font-general-regular mx-10 md:mx-20"
      @submit.prevent="sendEmail"
    >
      <p class="font-general-regular text-gray-500 text-md text-left mt-8 mb-4">
        Personal Profile____________
      </p>

      <div
        class="font-general-regular grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 mt-6 sm:gap-8"
      >
        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="name"
            >Surname Name
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Surname Name"
            aria-label="Name"
            v-model="from_name"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="name"
            >First Name
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="First Name"
            aria-label="Name"
            v-model="from_name"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="name"
            >Middle Name
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Middle Name"
            aria-label="Name"
            v-model="from_name"
          />
        </div>

        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="phone"
            >TelePhone</label
          >
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            name="phone"
            type="text"
            required=""
            placeholder="TelePhone"
            aria-label="TelePhone"
            v-model="email"
          />
        </div>

        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="email"
            >Email</label
          >
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            name="email"
            type="text"
            required=""
            placeholder="Your Email"
            aria-label="Email"
            v-model="email"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="email"
            >Age</label
          >
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            name=""
            type="text"
            required=""
            placeholder="Your Age"
            aria-label=""
            v-model="email"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="email"
            >Nationality</label
          >
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            name=""
            type="text"
            required=""
            placeholder="Nationality"
            aria-label=""
            v-model="email"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="email"
            >Marital Status</label
          >
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            name=""
            type="text"
            required=""
            placeholder="Marital Status"
            aria-label=""
            v-model="email"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark mb-2 text-left" for="email"
            >Address</label
          >
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            name=""
            type="text"
            required=""
            placeholder="Address"
            aria-label=""
            v-model="email"
          />
        </div>
      </div>
      <p class="font-general-regular text-gray-500 text-md text-left mt-10 mb-4">
        Education____________
      </p>
      <div
        class="font-general-regular grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 mt-6 sm:gap-8"
      >
        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Highest Level of Education
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Highest Level of Education"
            aria-label="Highest Level of Education"
          />
        </div>

        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Program
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Program"
            aria-label="Program"
            v-model="from_name"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Field of Study
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Field of Study"
            aria-label="Field of Study"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Location
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Location"
            aria-label="Location"
          />
        </div>
      </div>

      <p class="font-general-regular text-gray-500 text-md text-left mt-10 mb-4">
        Work Experience____________
      </p>

      <div
        class="font-general-regular grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 mt-6 sm:gap-8"
      >
        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Occupation
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Occupation"
          />
        </div>

        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Employment Type
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Employment Type"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Job Start Year
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Job Start Year"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Job End Year
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Job End Year"
          />
        </div>
        <div>
          <label class="block text-lg text-primary-dark text-left mb-2" for="name"
            >Location
          </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Location"
          />
        </div>
      </div>
      <input class="bg-primary p-8 py-2 mt-8" type="submit" value="Submit" />

      <!-- <div>
					<Button
						title="Send Message"
						class="px-4 py-2.5 text-white tracking-wider bg-indigo-500 hover:bg-indigo-600 focus:ring-1 focus:ring-indigo-900 rounded-lg duration-500"
						type="submit"
						aria-label="Send Message"
						value="submit"
					/>
				</div> -->
    </form>
  </div>
</template>

<style scoped>
input[type="submit"] {
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type="submit"]:hover {
  background-color: #45a049;
}
[type="checkbox"]:checked,
[type="radio"]:checked {
  background-color: #c3910a;
}
[type="radio"] {
  border: solid 1px #c3910a;
}
.bordercolor {
  border: solid 2px #022c0c;
}
/* .border-primary-300 {
  border: solid 2px #022c0c;
} */
</style>
