<script setup lang="ts">

import PersonCard from "../components/PersonCard.vue";

const sampleTitle = 'Instructor Team';
const courseInstructor = {
  title: 'Course Instructor',
  firstName: 'Sajjad',
  lastName: 'Amini',
  avatar: 'Amini.jpg',
  personalWebsite: 'https://sharif.edu/~s_amini/'
};

const courseHeadAssistants = {
  title: 'Course Head Assistants',
  people: [
    {firstName: 'Ali', lastName: 'Nourian', avatar: 'Nourian.jpg', personalWebsite: 'https://alinourian.github.io/'},
    {firstName: 'Zahra', lastName: 'Sodagar', avatar: 'Sodagar.jpg', personalWebsite: 'https://zahrasodagar.github.io/'}
  ]
};

const courseAssistants = {
  title: 'Course Assistants',
  people: [
    {firstName: 'Arshak', lastName: 'Rezvani', avatar: 'profile.jpg', personalWebsite: ''},
    {firstName: 'Illia', lastName: 'Hashemi Rad', avatar: 'profile.jpg', personalWebsite: ''},
    {firstName: 'Ramtin', lastName: 'Moslemi', avatar: 'profile.jpg', personalWebsite: ''},
    {firstName: 'Ali', lastName: 'Nikkhah', avatar: 'profile.jpg', personalWebsite: ''},
    {firstName: 'Hesam', lastName: 'Hosseini', avatar: 'profile.jpg', personalWebsite: ''},
    {firstName: 'Homan', lastName: 'Zolfaghari', avatar: 'profile.jpg', personalWebsite: ''},
  ]
};
</script>

<template>
  <div class="section">
    <div class="section-content">
      <div class="title">{{ sampleTitle }}</div>
      <div class="sub-section">
        <div class="sub-section-content">
          <div class="sub-title">{{ courseInstructor.title }}</div>
          <div class="grid-team">
            <div class="grid-card">
              <PersonCard
                  :firstName="courseInstructor.firstName"
                  :lastName="courseInstructor.lastName"
                  :avatar="courseInstructor.avatar"
                  :personalWebsite="courseInstructor.personalWebsite"
              />
            </div>
          </div>
        </div>
        <div class="sub-section-content">
          <div class="sub-title">{{ courseHeadAssistants.title }}</div>
          <div class="grid-team">
            <div class="grid-card" v-for="(headAssistant, index) in courseHeadAssistants.people" :key="index">
              <PersonCard
                  :firstName="headAssistant.firstName"
                  :lastName="headAssistant.lastName"
                  :avatar="headAssistant.avatar"
                  :personal-website="headAssistant.personalWebsite"
              />
            </div>
          </div>
        </div>
        <div class="sub-section-content">
          <div class="sub-title">{{ courseAssistants.title }}</div>
          <div class="grid-team">
            <div class="grid-card" v-for="(assistant, index) in courseAssistants.people" :key="index">
              <PersonCard
                  :firstName="assistant.firstName"
                  :lastName="assistant.lastName"
                  :avatar="assistant.avatar"
                  :personal-website="assistant.personalWebsite"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.grid-card {
  display: flex;
  flex-direction: column;
}

.grid-team {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1.5rem;
}

@media (min-width: 640px) {
  .grid-team {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
}

@media (min-width: 768px) {
  .grid-team {
    grid-template-columns: repeat(4, minmax(0, 1fr));
  }
}

@media (min-width: 1024px) {
  .grid-team {
    grid-template-columns: repeat(5, minmax(0, 1fr));
  }
}

@media (min-width: 1280px) {
  .grid-team {
    grid-template-columns: repeat(6, minmax(0, 1fr));
  }
}

</style>