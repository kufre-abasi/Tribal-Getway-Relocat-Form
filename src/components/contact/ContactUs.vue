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
  <div class="w-full md:w-1/2">
    <div class="leading-loose max-w-xl text-left mt-20">
      <!-- <p class="font-general-regular text-gray-500 text-md mb-8">
        Please fill out the form to create your custom package.
      </p> -->
      <form ref="form" class="font-general-regular space-y-7" @submit.prevent="sendEmail">
        <div>
          <label class="block text-lg text-primary-dark mb-2" for="name">Name </label>
          <input
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            id="name"
            name="name"
            type="text"
            required=""
            placeholder="Your Name"
            aria-label="Name"
            v-model="from_name"
          />
        </div>

        <div>
          <label class="block text-lg text-primary-dark mb-2" for="email">Email</label>
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
          <label class="block text-lg text-primary-dark mb-2" for="message"
            >Message</label
          >
          <textarea
            class="w-full px-5 py-2 border border-primary border-opacity-50 bg-opacity-50 text-secondary-light bg-primary-light rounded-md text-md"
            name="message"
            cols="14"
            rows="6"
            aria-label="Message"
            v-model="message"
          ></textarea>
        </div>
        <input class="bg-primary p-8 py-2" type="submit" value="Send" />

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
