<script>
export default {
  name: 'front',
  data () {
    return {
      projects: [
        {
          "title": "프로젝트 1 이름",
          "duration": "프로젝트 1 기간"
        },
        {
          "title": "프로젝트 2 이름",
          "duration": "프로젝트 2 기간"
        },
      ],
      prizes: [
        {
          "title": "상 1 이름",
          "prize": "상 1 등수"
        },
        {
          "title": "상 2 이름",
          "prize": "상 2 등수"
        }
      ],
      "careers": [
        "경력 1",
        "경력 2"
      ]
    }
  }
}
</script>

<template>
  <div class='card'>
    <div class='project-wrapper'>
      <span class='category'>Projects</span>
      <ul>
        <li
          :key='`project-${i}`'
          v-for="(project, i) in projects"
          class='project'
        >
          <span>[{{ project.duration }}] {{ project.title }}</span>
        </li>
      </ul>
    </div>

    <div class='prize-wrapper'>
      <span class='category'>Prizes</span>
      <ul>
        <li
          :key='`prize-${i}`'
          v-for="(prize, i) in prizes"
          class='prize'
        >
          <span>{{ prize.title }} - {{ prize.prize }}</span>
        </li>
      </ul>
    </div>

    <div class='career-wrapper'>
      <span class='category'>Careers</span>
      <ul>
        <li
          :key='`career-${i}`'
          v-for="(career, i) in careers"
          class='career'
        >
          <span>{{ career }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.card {
  position: relative;
  width: 30rem;
  height: 100%;
  background-color: #f6f6f6;
  border-radius: 15px;
  box-shadow: 20px 20px 60px #d1d1d1, -20px -20px 60px #ffffff;
  font-family: 'Inter', sans-serif;
  font-weight: 300;
  overflow-x: hidden; 
  overflow-y: scroll;
  padding: 10px;
  box-sizing: border-box;
}

.button {
  color: #606060;
  cursor: pointer;
  user-select: none;
}

.content-wrapper {
  position: relative;
}

.project-wrapper,
.prize-wrapper,
.career-wrapper {
  margin: 5% 0 0 5%;
  line-height: 1.5rem;
}
</style>
