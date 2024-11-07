<template>
  <div class="bg-neutral-500 flex flex-col items-center justify-center">
    <div
      class="bg-white rounded-lg shadow-md p-4 mb-6 w-full max-w-md"
      v-for="cert in certifications"
      :key="cert.title"
    >
      <div class="flex items-center">
        <div class="w-1/3">
          <img :src="cert.imagePath" class="w-full h-auto" />
        </div>
        <div class="w-2/3 pl-4">
          <h2 class="text-lg font-bold mb-1">{{ cert.title }}</h2>
          <p class="text-gray-600 mb-1">Earned in {{ cert.year }}</p>
          <p class="text-sm">{{ cert.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      certifications: [
        {
          title: "AWS Certified Developer",
          year: 2022,
          description:
            "Demonstrates proficiency in building and deploying secure and scalable applications on the AWS platform.",
          imagePath: "/images/aws-certified-developer.png",
        },
        {
          title: "Kubernetes Certified Administrator",
          year: 2021,
          description:
            "Validates the skills and knowledge to configure, manage, and operate production-grade Kubernetes clusters.",
          imagePath: "/images/kubernetes-certified-admin.png",
        },
        {
          title: "Google Cloud Certified Professional",
          year: 2023,
          description:
            "Certifies the ability to design, develop, and manage robust, secure, and scalable solutions on the Google Cloud platform.",
          imagePath: "/images/google-cloud-certified.png",
        },
      ],
    };
  },
};
</script>

<style>
/* No custom styles needed, using Tailwind CSS utility classes */
</style>
