<template>
  <v-container class="content">
    <v-container class="content-container d-flex justify-space-between">
      <v-container class="menu-container">
        <v-avatar size="200" color="primary" class="avatar-container">
          <img :src="profileImage" alt="karel" />
        </v-avatar>
        <div
          v-for="(network, index) in networks"
          class="social-net"
          :key="index"
        >
          <a :href="network.link" target="_blank">
            <img :src="network.img" width="20" height="20" />
            <p>{{ network.label }}</p>
          </a>
        </div>
      </v-container>
      <v-container
        class="info-container"
        style="color: #353535; font-size: 18px"
      >
        <div class="d-flex justify-space-between">
          <h1>Hi, I'm Karel Díaz</h1>
          <a
            style="text-decoration: none"
            href="https://drive.google.com/file/d/1EVXOKm5cv9dBGDoW15BygbO3eRq6am21/view?usp=sharing"
            target="_blanck"
            >Download</a
          >
        </div>
        <p style="font-size: 18px">
          Developer, passionate about what I do 💻. I'm student of Computer
          Science at University of Havana. I play chess in my free times, and
          most of this time I read about AI because I have a great interest in
          how many fields of science are currently advancing with the help of AI
          and I would like to be part of these advances.
        </p>
        <p style="font-size: 18px">
          Currently I work as a frontend developer of webs applications and
          mainly work with Javascript, Vue and React.
        </p>
        <h3 style="margin-top: 30px">Interests</h3>
        <p style="font-size: 18px">
          Travels, Computer Science, Competitive Programming, Artificial
          Intelligence, Machine Learning, Deep Learning, Blockchain,
          Cryptocurrencies, Chess, Series & Movies
        </p>
        <h3 style="margin-top: 30px">Achievements</h3>
        <ul style="font-size: 18px">
          <li>
            I participated in the International Informatics Olympiad in 2018
            (Cuba Team).
          </li>
          <li>
            I got bronze medal in the ibera-American Informatics Olympiad in
            2018 (Cuba Team).
          </li>
          <li>
            I participated in the ibera-American Informatics Olympiad in 2017
            (Cuba Team).
          </li>
        </ul>
        <h3 style="margin-top: 30px">Languages</h3>
        <p style="font-size: 18px; margin-bottom: 3px">
          Spanish: native
        </p>
        <p style="font-size: 18px">
          English: mid-level
        </p>
        <h3 style="margin-top: 30px">Experience</h3>
        <h4 style="margin-top: 10px">
          Developer at Alegra | Jun 2021 - Present (Full-time)
        </h4>
        <ul>
          <li>
            Frontend developer using VueJs, micro-frontends, javascript
          </li>
          <li>AWS (CloudFront, CodePipeline, S3, CodeBuild, Lamda)</li>
          <li>
            Swagger
          </li>
          <li>Git, gitflow</li>
          <li>Scrum methodology.</li>
          <li>Objective and Key Results (OKRs)</li>
          <li>Cypress, unit testing</li>
        </ul>
        <h4 style="margin-top: 10px">Qvacuba | Jan 2021 - May 2021</h4>
        <ul>
          <li>Frontend developer using ReactJs, bootstrap</li>
          <li>Mobile developer using React Native</li>
          <li>Git</li>
          <li>Scrum methodology</li>
          <li>Unit testing</li>
        </ul>
        <h4 style="margin-top: 10px">
          La Pikera | Nov 2020 - Jan 2021 (Mid-Time)
        </h4>
        <ul>
          <li>Android developer (java)</li>
          <li>Google maps api (Geocoding, Destination, Places)</li>
          <li>Git</li>
          <li>Scrum methodology</li>
        </ul>
        <h4 style="margin-top: 10px">CXMAD Enterprise | May 2020 - Oct 2020</h4>
        <ul>
          <li>Frontend developer using React (javascript and typescript)</li>
          <li>Git</li>
          <li>Scrum methodology</li>
        </ul>
      </v-container>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: "Content",
  data() {
    return {
      profileImage: require("../assets/profileImage.jpeg"),
      networks: [
        {
          label: "@Karelito00",
          img: require("../assets/github.svg"),
          link: "https://github.com/Karelito00",
        },
        {
          label: "@Karelito00",
          img: require("../assets/twitter.svg"),
          link: "https://twitter.com/Karelito00",
        },
        {
          label: "karelkdv2000@gmail.com",
          img: require("../assets/gmail.svg"),
          link: "mailito:karelkdv2000@gmail.com",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.content {
  max-width: 1100px;
  min-width: 900px;
  padding-left: 10px;
  padding-right: 10px;
  margin-top: 100px;
  margin-bottom: 50px;
  .content-container {
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.2);
    background-color: #ebebeb;
    border-radius: 4px;
    .avatar-container {
      box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.4);
      margin-bottom: 20px;
    }
    .menu-container {
      width: 30%;
      padding: 30px;
      .social-net {
        cursor: pointer;
        margin-left: 20px;
        margin-bottom: 10px;
        a {
          display: flex;
          align-items: center;
          text-decoration: none;
          p {
            color: #353535;
            margin-left: 10px;
            margin-bottom: 0;
          }
        }
      }
    }
    .info-container {
      width: 70%;
      padding: 30px;
    }
  }
}
</style>
