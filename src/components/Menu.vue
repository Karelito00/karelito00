<template>
  <v-container :class="['menu-container', {menu}]">
    <div :class="['sticky-menu', {menu}]">
      <v-container
        :class="['myinfo-container', { menu }]"
      >
        <v-avatar
          size="220"
          color="primary"
          :class="['avatar-container', {menu}]"
        >
          <img :src="profileImage" alt="karel" />
        </v-avatar>
        <h1 v-if="menu" style="color: #353535">Karel Díaz</h1>
        <div style="display: flex; justify-content: center; width: 150px">
          <div
            v-for="(network, index) in networks"
            class="social-net"
            :key="index"
          >
            <a :href="network.link" target="_blank">
              <img :src="network.img" width="20" height="20" />
            </a>
          </div>
        </div>
      </v-container>
      <skills :menu="menu" />
    </div>
  </v-container>
</template>

<script>
import Skills from './Skills.vue';

export default {
  components: {
    Skills,
  },
  props: {
    menu: {
      default: true,
      type: Boolean,
    },
  },
  data() {
    return {
      profileImage: require('../assets/profile.jpg'),
      networks: [
        {
          label: '@Karelito00',
          img: require('../assets/github_icon.svg'),
          link: 'https://github.com/Karelito00',
        },
        {
          label: '@Karelito00',
          img: require('../assets/twitter_icon.svg'),
          link: 'https://twitter.com/Karelito00',
        },
        {
          label: 'karelkdv2000@gmail.com',
          img: require('../assets/gmail_icon.svg'),
          link: 'mailito:karelkdv2000@gmail.com',
        },
        {
          label: 'karelkdv2000@gmail.com',
          img: require('../assets/linkedin_icon.svg'),
          link: 'https://www.linkedin.com/in/karel-d%C3%ADaz-vergara-705420216/',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.menu-container {
  .myinfo-container {
    display: flex; 
    align-items: center; 
    flex-direction: column;
    padding: 0;
    &:not(.menu) {
      align-items: flex-start;
      max-width: 300px;
      @media (max-width: 650px) {
        max-width: 150px;
      }
    }
  }
  .avatar-container {
    border: 0 !important;
    background: transparent !important;
    &:not(.menu) {
      min-width: 150px !important;
      max-width: 150px;
      min-height: 150px;
      max-height: 150px;
      > img {
        width: 150px;
        height: 150px;
      }
    }
    margin-bottom: 20px;
    > img {
      transform: rotate(30deg);
    }
  }
  &.menu {
    max-width: 300px;
    min-width: 300px;
    @media (max-width: 850px) {
      display: none;
    }
  }
  &:not(.menu) {
    padding: 0;
    margin-top: 20px;
    @media (min-width: 850px) {
      display: none;
    }
  }
  .sticky-menu {
    top: 85px;
    display: flex;
    position: sticky;
    flex-direction: column;
    align-items: center;
    &:not(.menu) {
      position: initial;
      flex-direction: row;
      align-items: flex-start;
      div {
        color: white;
      }
    }
    .social-net {
      cursor: pointer;
      margin-bottom: 10px;
      display: flex;
      &:not(:first-child) {
        margin-left: 10px;
      }
    }
  }
  padding: 30px 20px;
}
</style>
