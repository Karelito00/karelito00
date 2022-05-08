<template>
  <v-container style="padding: 0 20px">
    <h3 v-if="menu" style="margin-left: 3px">Skills</h3>
    <div style="display: flex; flex-wrap: wrap">
      <div v-for="skill in skills" :key="skill" class="skill">
        {{ skill }}
      </div>
    </div>
  </v-container>
</template>

<script>
export default {
  props: {
    menu: {
      require: true,
      type: Boolean
    }
  },
  data() {
    return {
      skills: [
        'vim',
        'git',
        'github',
        'gitflow',
        'vue',
        'css/scss',
        'aws',
        'javascript',
        'typescript',
        'serverless',
        'python',
        'c/c++',
        'data structures',
        'React',
        'haskell',
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
::v-deep .skill {
  background: #353535;
  font-size: 15px;
  padding: 2px 10px;
  margin-bottom: 5px;
  border-radius: 4px;
  margin-left: 3px;
  margin-right: 3px;
  @media (max-width: 650px) {
    font-size: 14px;
  }
}
</style>
