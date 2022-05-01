<template>
  <v-container class="content">
    <v-container class="content-container d-flex justify-space-between">
      <v-container class="menu-container">
        <v-avatar size="220" color="primary" class="avatar-container">
          <img :src="profileImage" alt="karel" />
        </v-avatar>
        <h1 style="color: #353535">Karel Díaz</h1>
        <div style="display: flex">
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
          Developer, passionate about what I do 💻. Currently I'm studying Computer
          Science at University of Havana. I love play chess in my free times, I'm not than good 
          but I enjoy it. I have a great interest in IA and I'm researching about auto machine learning,
          cause my thesis is about a topic related, today many fields of science are currently advancing 
          with the help of AI and I would like to be part of these advances.
        </p>
        <p style="font-size: 18px">
          Currently I work as a fullstack developer of webs applications and
          mainly work with Javascript, Vue, Serverless and AWS.
        </p>
        <h3 style="margin-top: 30px">Interests</h3>
        <p style="font-size: 18px">
          Travels, Computer Science, Competitive Programming, Artificial
          Intelligence, Machine Learning, Blockchain, Cryptocurrencies, Chess, 
          Series & Movies
        </p>
        <h3 style="margin-top: 30px">Achievements</h3>
        <ul style="font-size: 18px">
          <li>
            My team and me(UH_NotReturn) got silver medal 🥈 in the ICPC Caribbean contest in 2021.
          </li>
          <li>
            My team and me(UH_wake_me_up!) got bronze medal 🥉 in the ICPC Caribbean contest in 2019.
          </li>
          <li>
            I participated in the International Informatics Olympiad in 2018
            (Cuba Team).
          </li>
          <li>
            I got bronze medal 🥉 in the ibera-American Informatics Olympiad in
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
          <li>
            Backend developer using serverless, aws, typescript
          </li>
          <li>AWS (CloudFront, CodePipeline, S3, CodeBuild, Lambda, Api Gateway, Database Migration Service, 
            IAM Managment, DynamoDB)</li>
          <li>
            Swagger
          </li>
          <li>Git, gitflow, github</li>
          <li>Scrum methodology.</li>
          <li>Objective and Key Results (OKRs)</li>
          <li>Testing: cypress, jest, supertest</li>
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
        <h3 style="margin-top: 30px">Other projects</h3>
        <h4 style="margin-top: 10px">Search enginge</h4>
        <p> I develop a search engine using VueJs for frontend, and fastapi for backend, is based in 
        a vectorial model of information retrieve and was created with the help of some tools of NPL and using glove, 
        a model pretrained for words embedding.</p>
        <label> Repo: <a href="https://github.com/Karelito00/search_engine" target="_blank">https://github.com/Karelito00/search_engine</a> </label>
        <h4 style="margin-top: 10px">Assets Bots simulator</h4>
        <p> My school team and me develop a simulator of assets bots, we include an implementation of a grid bot, a rebalance bot and a smart bot, we use python for all the project, and we make a tiny compiler, we define and create a regex language, the objective of this project is setup bots in real past conditions of the market and get the best parameters</p>
        <label> Repo: <a href="https://github.com/University-Projects-UH/ia-sim-cmp" target="_blank">https://github.com/University-Projects-UH/ia-sim-cmp</a> </label>
      </v-container>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: "Content",
  data() {
    return {
      profileImage: require("../assets/profile.jpg"),
      networks: [
        {
          label: "@Karelito00",
          img: require("../assets/github_icon.svg"),
          link: "https://github.com/Karelito00",
        },
        {
          label: "@Karelito00",
          img: require("../assets/twitter_icon.svg"),
          link: "https://twitter.com/Karelito00",
        },
        {
          label: "karelkdv2000@gmail.com",
          img: require("../assets/gmail_icon.svg"),
          link: "mailito:karelkdv2000@gmail.com",
        },
        {
          label: "karelkdv2000@gmail.com",
          img: require("../assets/linkedin_icon.svg"),
          link: "https://www.linkedin.com/in/karel-d%C3%ADaz-vergara-705420216/",
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
      margin-bottom: 20px;
      > img {
        transform: rotate(30deg);
      }
    }
    .menu-container {
      width: 30%;
      padding: 30px;
      display: flex;
      flex-direction: column;
      align-items: center;
      .social-net {
        cursor: pointer;
        margin-bottom: 10px;
        display: flex;
        &:not(:first-child) {
          margin-left: 20px;
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
