<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      message: "",
    };
  },
};
</script>
<template>
  <div class="bg-gradient-to-r from-neutral-500 to-neutral-800 py-16">
    <div class="max-w-2xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="space-y-8">
        <!-- Contact Information Card -->
        <div class="bg-white shadow-md rounded-lg p-8">
          <h2 class="text-2xl font-bold mb-4">Contact me</h2>
          <form
            action="https://formsubmit.co/51b0cec53a1a2cd9ad4c66bbcd406601"
            method="POST"
          >
            <div class="space-y-4">
              <label for="name" class="block text-sm font-medium text-gray-700"
                >Name</label
              >
              <input
                type="text"
                id="name"
                name="name"
                v-model="name"
                class="mt-1 block w-full shadow-sm text-lg border-2 border-[#CDBFBF] rounded-md p-2"
                required
              />
              <input type="text" name="_honey" style="display: none" />
              <label for="email" class="block text-sm font-medium text-gray-700"
                >Email</label
              >
              <input
                type="email"
                id="email"
                name="email"
                v-model="email"
                class="mt-1 block w-full shadow-sm text-lg border-2 border-[#CDBFBF] rounded-md p-2"
                required
              />
              <label
                for="message"
                class="block text-sm font-medium text-gray-700"
                >Message</label
              >
              <textarea
                id="message"
                v-model="message"
                name="message"
                rows="3"
                class="mt-1 block w-full shadow-sm text-lg border-2 border-[#CDBFBF] rounded-md p-2"
                required
              ></textarea>
              <input
                type="file"
                name="attachment"
                accept="image/png, image/jpeg, application/pdf"
              />
            </div>
            <div class="mt-6">
              <button
                type="submit"
                class="bg-[#CDBFBF] hover:bg-gray-200 text-black font-medium py-2 px-4 rounded-md transition-colors"
              >
                Send Email
              </button>
            </div>
          </form>
        </div>

        <!-- Follow Me Card -->
        <div class="bg-white shadow-md rounded-lg p-8">
          <h2 class="text-2xl font-bold mb-4">Follow Me</h2>
          <div class="space-y-4">
            <div class="flex items-center space-x-4">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                x="0px"
                y="0px"
                width="24"
                height="24"
                viewBox="0 0 48 48"
              >
                <path
                  fill="#0288D1"
                  d="M42,37c0,2.762-2.238,5-5,5H11c-2.761,0-5-2.238-5-5V11c0-2.762,2.239-5,5-5h26c2.762,0,5,2.238,5,5V37z"
                ></path>
                <path
                  fill="#FFF"
                  d="M12 19H17V36H12zM14.485 17h-.028C12.965 17 12 15.888 12 14.499 12 13.08 12.995 12 14.514 12c1.521 0 2.458 1.08 2.486 2.499C17 15.887 16.035 17 14.485 17zM36 36h-5v-9.099c0-2.198-1.225-3.698-3.192-3.698-1.501 0-2.313 1.012-2.707 1.99C24.957 25.543 25 26.511 25 27v9h-5V19h5v2.616C25.721 20.5 26.85 19 29.738 19c3.578 0 6.261 2.25 6.261 7.274L36 36 36 36z"
                ></path>
              </svg>
              <a
                href="https://www.linkedin.com/in/qindi-wu-547a2aa9/"
                class="text-gray-700 font-medium hover:text-indigo-500 transition-colors"
                >LinkedIn</a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style></style>
