<template>
  <div>
    <v-row>
      <v-col cols="12" class="text-center"><h2>My Skill Set</h2></v-col>
    </v-row>
    <v-row>
      <v-col
        v-for="(skill, i) in skills"
        :key="i"
        cols="12"
        md="6"
        class="md-6"
      >
        <v-card shaped elevation="9" class="ma-1">
          <v-row>
            <v-col cols="4">
              <v-img :src="skill.image"></v-img>
            </v-col>
            <v-col cols="8">
              <v-card-title>{{ skill.title }}</v-card-title>
              期間：{{ skill.periods }}
              <v-spacer />
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'SkillPage',
  data() {
    return {
      skills: [
        {
          title: 'Vue.js',
          image:
            'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg',
          periods: '1ヶ月',
        },
        {
          title: 'JavaScript',
          image:
            'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg',
          periods: '3ヶ月',
        },
        {
          title: 'HTML5',
          image:
            'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg',
          periods: '3ヶ月',
        },
        {
          title: 'CSS3',
          image:
            'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg',
          periods: '1ヶ月',
        },
        {
          title: 'Java',
          image:
            'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg',
          periods: '3ヶ月',
        },
      ],
    }
  },
}
</script>

<style></style>
