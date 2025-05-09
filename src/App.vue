<template>
 <div class="app">
    <div class="main">
      <div class="description">
        <div class="description__persone">
          <img class="description__img" src="/img/persone.svg">
          <div class="description__name">Anurag Yadav</div>

        </div>
        <div>
          <div class="description__text">A well-organized, creative and goaloriented graduate possessing excellent communication, problem-solving and leadership skills with a flair to explore Computer Science
  Engineering</div>
          <svg width="267" height="2" viewBox="0 0 267 2" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g clip-path="url(#clip0_2497_72)">
              <rect x="0.656157" y="0.738616" width="265.718" height="0.504209" stroke="#E2E6EE" stroke-width="0.504209" stroke-linejoin="round" />
            </g>
            <defs>
              <clipPath id="clip0_2497_72">
                <rect width="266.222" height="1.00842" fill="white" transform="translate(0.404053 0.486511)" />
              </clipPath>
            </defs>
        </svg>
        </div>
      </div>
      <div class="contact">
        <div class="contact__wrap">
          <contacts-card :contacts="contacts"/>
        </div>
          <svg width="267" height="2" viewBox="0 0 267 2" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g clip-path="url(#clip0_2497_72)">
              <rect x="0.656157" y="0.738616" width="265.718" height="0.504209" stroke="#E2E6EE" stroke-width="0.504209" stroke-linejoin="round" />
            </g>
            <defs>
              <clipPath id="clip0_2497_72">
                <rect width="266.222" height="1.00842" fill="white" transform="translate(0.404053 0.486511)" />
              </clipPath>
            </defs>
        </svg>
      </div>
      <div class="socials">
        <div class="socials__wrap">
          <div class="socials__text">Socials</div>
            <socials-card :socials="socials"/>
        </div>
         <svg width="267" height="2" viewBox="0 0 267 2" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g clip-path="url(#clip0_2497_72)">
              <rect x="0.656157" y="0.738616" width="265.718" height="0.504209" stroke="#E2E6EE" stroke-width="0.504209" stroke-linejoin="round" />
            </g>
            <defs>
              <clipPath id="clip0_2497_72">
                <rect width="266.222" height="1.00842" fill="white" transform="translate(0.404053 0.486511)" />
              </clipPath>
            </defs>
        </svg>
      </div>
      <div class="languages">
        <div class="languages__wrap">
          <div class="languages__text__small">Languages</div>
          <languages-card :languages="languages"/>
        </div>

      </div>
      <div class="hobbies">
        <div class="hobbies__text__small">Hobbies & Interests</div>
        <hobbies-card :hobbies="hobbies"/>
      </div>
       

    </div>
    <div class="content">
      <div class="main-wrap main-wrap__height__education">
        <grafic-elem :elem="elem"/>
        <div class="education">
          <div class="title">Education</div>
          <div class="education__content-wrap">
            <education-card :universities="universities"/>
          </div>
        </div>
      </div>
      <div class="main-wrap main-wrap__height__achievements">
        <grafic-elem :elem="elem"/>
        <div class="achievements">
          <div class="title title_achievements">Achievements</div>
            <div class="achievements__content-wrap">
              <achievements-card :achievements="achievements"/>
            </div>
        </div>
      </div>
      
      
      <div class="main-wrap main-wrap__height__skills">
      <grafic-elem :elem="elem"/>
        <div class="skills">
          <div class="title">Tools/Skills</div>
            <div class="skills__content-wrap">
              <div class="skills__content-wrap-1">
                <skills-card :skills="skills"/>
              </div>
              <div class="skills__content-wrap-2">
                <tools-card :tools="tools"/>
              </div>
            </div>
            
        </div>
      </div>
      <div class="main-wrap main-wrap__height__project">
       <grafic-elem :elem="elem"/>
        <div class="projects">
          <div class="title">Latest projects</div>
          <div class="projects__content-wrap">
          <projects-card :projects="projects"/>
          </div>

          
        </div>
      </div>
      <div class="main-wrap main-wrap__height__certificates">
        <grafic-elem :elem="elem"/>
        <div class="certificates">
          <div class="title">Certificates & Awards</div>
            <div class="certificates__content-wrap">
              <certificates-card :certificates="certificates"/>
            </div>
        </div>
      </div>
    </div>
      
   
 </div>
</template>


<script>
import EducationCard from "./components/EducationCard.vue";
import CertificatesCard from "./components/CertificatesCard.vue";
import AchievementsCard from "./components/AchievementsCard.vue";
import SkillsCard from "./components/SkillsCard.vue";
import ToolsCard from "./components/ToolsCard.vue";
import ProjectsCard from "./components/ProjectsCard.vue";
import GraficElem from "./components/GraficElem.vue";
import ContactsCard from "./components/СontactsCard.vue";
import SocialsCard from "./components/SocialsCard.vue";
import LanguagesCard from "./components/LanguagesCard.vue";
import HobbiesCard from "./components/HobbiesCard.vue";


export default {
  components: {
    EducationCard,
    CertificatesCard,
    AchievementsCard,
    SkillsCard,
    ToolsCard,
    ProjectsCard,
    GraficElem,
    ContactsCard, 
    SocialsCard,
    LanguagesCard,
    HobbiesCard
  }, 
  data() {
    return {
      universities: [
        {id: 1, img: "/img/education/Chandigarh_University.svg", title: "Chandigarh University", level: "Bachelor in Computer Science Engineering", time: "2020 - 2024", completion: "- 9 CGPA"},
        {id: 2, img: "/img/education/Suditi.svg", title: "Suditi Global Academy", level: "Intermediate XI - XII (CBSE)", time: "2018-2020", completion: "- 85%"},
        {id: 3, img: "/img/education/Akanksha.svg", title: "Akanksha Global Acadmey", level: "High School IX - X (CBSE)", time: "2016-2018", completion: "- 92%"}
      ],
      certificates: [
        {company: "freeCodeCamp", name: "Responsive Web Design", time: "Dec 2021 - Feb 2022", img: "/img/certificates/free_code_camp.svg"}, 
        {company: "Google", name: "Data Strcture & Algorithms", time: "Mar 2021 - Jun 2021", img: "/img/certificates/google.svg"}
      ],
      achievements: [
        {id: 1, time: "Present", place: "Chandigarh", role: "Graphic Designer", company: "Alexa Dev Community", img: "/img/achievements/Logo_ADC.svg", descr: "Creatively Designing and Developing web UI for Chandigarh University’s Alexa Developer Community, upcoming big launch of full website."},
        {id: 2, time: "Oct 2021 - Nov 2021", place: "Online", role: "Hacktoberfest Contributor", company: "Github", img: "/img/achievements/Logo_GitHub.svg", descr: "Contributed 8 PR’s in various open source projects. Great experience and learning alot about working with Github and open-source. Connecting with developers"},
        {id: 3, time: "Jan 2021 - March 2021", place: "Online", role: "Contributor", company: "Winter of Code", img: "/img/achievements/Logo_winter.svg", descr: "Overwhelming to be a part of DSC NSEC project - DSC NSEC Algorithms for Winter of Code 2020. First introduction to Git and Github. How github is used by most of the programmers in order to manage the projects."},
        {id: 4, time: "Oct 2020 - Dec 2020", place: "Online", role: "30Days of Google Cloud", company: "Google", img: "/img/achievements/Logo_google.svg", descr: "Hands on practice on Google Cloud Platform - the tool that powers apps like Google Search, Gmail and YouTube. As part of the program had learned the concepts like computing, application development, big data & machine learning using cloud."}
      ],
      skills: [
        {id: 1, name: "Figma", function: " Web UI Design, Prototyping", img: "/img/skills/Figma.svg"},
        {id: 2, name: "Java", function: "Software Development", img: "/img/skills/Java.svg"},
        {id: 3, name: "Python", function: "Design workspace", img: "/img/skills/Python.svg"}
      ],
      tools: [
        {id: 1, name: "HTML 5", function: "Structural Design", img: "/img/skills/HTML5.svg"},
        {id: 2, name: "CSS 3", function: "Style Design", img: "/img/skills/CSS3.svg"},
        {id: 3, name: "Wordpress", function: "Web development", img: "/img/skills/Wordpress.svg"},
        {id: 4, name: "VS Code", function: "Code editor", img: "/img/skills/VS.svg"},
        {id: 5, name: "Notion", function: "Project managment", img: "/img/skills/Notion.svg"},
      ],
      projects: [
        {id: 1, name: "Alexa Dev Community Landing Page", role: "Web UI design for alexa developers comunity", img: "/img/projects/ADC.svg", link: "https//figma.com", img2: "/img/projects/figma_icon.svg"},
        {id: 1, name: "Portfolio Webpage", role: "Personal Portfolio webpage with resume and blog", img: "/img/projects/Portfolio.svg", link: "https://anuragyadav365.github.io", img2: "/img/projects/portfolio_icon.svg"},
      ],
      contacts: [
        {id: 1, name: "Email", address: "anuragyadavmnp@gmail.com", img: "/img/contacts/mail.svg"},
        {id: 2, name: "Website", address: "https://anuragyadav365.github.io/portfolio.html", img: "/img/contacts/link.svg"},
        {id: 3, name: "Phone", address: "(+91) 981 5533 309", img: "/img/contacts/phone.svg"},
        {id: 4, name: "Address", address: "Hallomajra, Chandigarh, India", img: "/img/contacts/location.svg"},
      ],
      socials: [
        {id: 1, name: "Instagram", address: "@anurag.yadav.007", img: "/img/socials/instagram.svg"},
        {id: 2, name: "Github", address: "@anuragyadav365", img: "/img/socials/github.svg"},
        {id: 3, name: "Twitter", address: "@anuragmnp", img: "/img/socials/twitter.svg"},
        {id: 4, name: "Linkedin", address: "@anuragyadav", img: "/img/socials/linkedin.svg"},
      ],
      languages: [
        {id: 1, name: "Hindi", level: "Native", img: "/img/languages/Hindi.svg"},
        {id: 2, name: "English", level: "Professional working", img: "/img/languages/English.svg"},
        {id: 3, name: "Spanish", level: "Elementary", img: "/img/languages/Flag.svg"},
      ],
      hobbies: [
        {id: 1, name: "Gaming", img: "/img/hobbies/gaming.svg"},
        {id: 2, name: "Travelling", img: "/img/hobbies/travelling.svg"},
        {id: 3, name: "Sketching/Graffitti", img: "/img/hobbies/sketching.svg"},
        {id: 4, name: "Blogging", img: "/img/hobbies/blogging.svg"}
      ]
    } 
  }
}

</script>



<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  width: 1198px;
  display: flex;
  justify-content: start;
}
.content {
  width: 843px;
  height: 1698px;
}
.main {
  width: 354px;
  height: 1698px;
  background: #fff;
  padding: 48px;
}
.education {
  padding: 0px 0px 48px 0px;
  width: 697px;
  height: 272px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.main-wrap__height__education {
  height: 272px;
}
.title {
  font-weight: 500;
  font-size: 24px;
  color: #2e2e48;
}
.education__content-wrap {
  width: 697px;
  height: 158px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.certificates {
  width: 695px;
  height: 269px;
}
.main-wrap__height__certificates {
  height: 269px;
}
.certificates__content-wrap {
  margin-top: 32px;
  margin-bottom: 48px;
}
.achievements {
  padding: 0px 0px 48px 0px;
  width: 697px;
  height: 471px;
}
.main-wrap__height__achievements {
  height: 471px;
}
.achievements__content-wrap {

}
.title_achievements {
  margin-bottom: 32px;
}
.skills {
  width: 697px;
  height: 363.76px;
}
.main-wrap__height__skills {
  height: 363.76px;
}
.skills__content-wrap {
  margin-top: 32.27px;
  width: 697px;
  height: 250px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.skills__content-wrap-1 {
  width: 697px;
  height: 129px;
  display: flex;
  justify-content: space-between;
}
.skills__content-wrap-2 {
  width: 697px;
  height: 112px;
  display: flex;
  justify-content: space-between;
}
.projects {
  width: 697px;
  height: 264.45px;
}
.main-wrap {
  width: 793.81px;  
  display: flex;
  justify-content: start;
}
.main-wrap__height__project {
  height: 264.45px;
}
.projects__content-wrap {
  margin-top: 32.27px;
  width: 697px;
  height: 150px;
  display: flex;
  justify-content: space-between;
}
.description__img {
  width: 96px;
  height: 96px;
}
.description__name {
  font-weight: 500;
  font-size: 32px;
  color: #2e2e48;
}
.description__persone {
  width: 266px;
  height: 153px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.description__text {
  font-weight: 500;
  font-size: 16px;
  line-height: 133%;
  color: #47516b;
}
.description {
  height: 340px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.contact {
  height: 314px;
}
.contact__wrap {
  margin-top: 32.27px;
  margin-bottom: 32.27px;
  width: 266px;
  height: 250px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.socials {
  height: 322.35px;
}
.socials__wrap{
  width: 266px;
  height: 257px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-bottom: 32.27px;
  margin-top: 32.27px;
}
.socials__text {
  padding-top: 1px;
  font-weight: 400;
  font-size: 12px;
  color: #79819a;
}
.languages__wrap {
  width: 266px;
  height: 197px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-bottom: 32.27px;
  margin-top: 32.27px;
}
.languages__text__small {
  font-weight: 400;
  font-size: 12px;
  color: #79819a;
}
.hobbies {
  width: 266px;
  height: 218px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
