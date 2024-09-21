<script setup lang="ts">
const sampleTitle = 'Course Description';
const sampleDescription = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Egestas purus viverra accumsan in nisl nisi. Arcu cursus vitae congue mauris rhoncus aenean vel elit scelerisque. In egestas erat imperdiet sed euismod nisi porta lorem mollis. Morbi tristique senectus et netus. Mattis pellentesque id nibh tortor id aliquet lectus proin. Sapien faucibus et molestie ac feugiat sed lectus vestibulum. Ullamcorper velit sed ullamcorper morbi tincidunt ornare massa eget. Dictum varius duis at consectetur lorem. Nisi vitae suscipit tellus mauris a diam maecenas sed enim. Velit ut tortor pretium viverra suspendisse potenti nullam. Et molestie ac feugiat sed lectus. Non nisi est sit amet facilisis magna. Dignissim diam quis enim lobortis scelerisque fermentum. Odio ut enim blandit volutpat maecenas volutpat. Ornare lectus sit amet est placerat in egestas erat. Nisi vitae suscipit tellus mauris a diam maecenas sed. Placerat duis ultricies lacus sed turpis tincidunt id aliquet.';
</script>

<template>
  <div class="section">
    <div class="section-content p-8 sm:p-12 md:p-16 xl:p-20">
      <div class="title font-bold text-3xl sm:text-4xl">{{ sampleTitle }}</div>
      <div class="content text-black-600 text-md md:text-xl lg:text-xl">
        This course provides a comprehensive introduction to the probabilistic foundations and learning algorithms behind generative models, with a particular emphasis on deep learning architectures. Students will explore generative models as conditional probability distributions represented by 𝑝(𝑥∣𝑦), where 𝑥 is a high-dimensional random vector and 𝑦 may be high or low-dimensional. The curriculum covers key topics such as sampling, density estimation, training techniques, latent space exploration, and architectural design choices.
      </div>
      <div class="content text-black-600 text-md md:text-xl lg:text-xl">
        In addition, practical applications like data generation, imputation, and latent space interpolation will be thoroughly examined. Hands-on projects and exercises will accompany the course, allowing students to investigate the scalability of different methods and their theoretical foundations in real-world contexts.
      </div>
    </div>
  </div>
</template>

<style scoped>
.content {
  font-size: 20px;
  line-height: 1.75rem;
}
</style>