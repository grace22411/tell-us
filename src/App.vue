<template>
  <div id="app">
    <Modal />
      <div class="section">
        <Header />
        <Caption />
      </div>
      <div class="report">
        <p> Eiusmod cupidatat anim ullamco amet est.Eiusmod cupidatat anim ullamco <a href="">Report here</a></p>
      </div>
      <div class="cards">
          <Story 
            v-for= "story in stories" 
            :key="story.color"
            :story="story"
          />

          <div class="load">
            <button>LOAD MORE</button>
          </div>
      </div>
      <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Caption from './components/Caption.vue'
import Story from './components/Story.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Caption,
    Story,
    Footer
  },
   data () {
        return {
            stories: [
              {
                topic: "Marriage Crisis",
                name: "Darlene Richards",
                profession: "Software Engineer",
                details: "Eu pariatur ad consectetur tempor sint cupidatat dolore qui officia dolore proiden duis id. Elit officia amet do eiusmod voluptate",
                src: require('./assets/pics-1.png'),
                content: "Irure tempor ullamco in ex culpa. Ut pariatur tempor sit est. Cillum deserunt aute anim esse consequat in cupidatat voluptate dolore. Qui id sit minim magna commodo do pariatur anim. Dolore do deserunt aute incididunt aliquip nulla nulla esse Lorem cupidatat cupidatat minim et eu",
                twitterHandle: "@whitefish664"
              },
              {
                topic: "Irreversible Mistake",
                name: "Gregory Fisher",
                profession: "Software Engineer",
                details: "Eu pariatur ad consectetur tempor sint cupidatat dolore qui officia dolore proiden duis id. Elit officia amet do eiusmod voluptate",
                src: require('./assets/pic-2.png'),
                content: "",
                twitterHandle: "@dar11244"
              },
              {
                topic: "My Life Story",
                name: "Bessie Williamson ",
                profession: "Software Engineer",
                details: "Eu pariatur ad consectetur tempor sint cupidatat dolore qui officia dolore proiden duis id. Elit officia amet do eiusmod voluptate",
                src: require('./assets/pic-3.png'),
                content: "",
                twitterHandle: "@yummy234"
              },
              {
                topic: "My kids and I",
                name: "Esther Simmmons",
                profession: "Software Engineer",
                details: "Eu pariatur ad consectetur tempor sint cupidatat dolore qui officia dolore proiden duis id. Elit officia amet do eiusmod voluptate",
                src: require('./assets/pic-2.png'),
                content: "",
                twitterHandle: "@tina346"
              },
              {
                topic: "My Rape Story",
                name: "Brooklyn Mckinney",
                profession: "Software Engineer",
                details: "Eu pariatur ad consectetur tempor sint cupidatat dolore qui officia dolore proiden duis id. Elit officia amet do eiusmod voluptate",
                src: require('./assets/pics-1.png'),
                content: "",
                twitterHandle: "@brooklyn45"
              },
              {
                topic: "Adolescence Mistake",
                name: "Brandie Wilson",
                profession: "Software Engineer",
                details: "Eu pariatur ad consectetur tempor sint cupidatat dolore qui officia dolore proiden duis id. Elit officia amet do eiusmod voluptate",
                src: require('./assets/pic-3.png'),
                content: "",
                twitterHandle: "@wilson349"
              },

            ]
        }
    }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');
*{
   margin: 0;
  padding: 0;
  box-sizing:border-box;
}
body,html{
  margin: 0;
  padding: 0;
  height: 100%;
  width:100%;
}
#app {
  font-family: 'Poppins', sans-serif;;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.section{
  width:100%;
  height:500px;
  background-color: #F3F5CA;
}
.cards{
  display:flex;
  flex-wrap: wrap;
  background-color: #feffe9;
  width:100%;
  height: auto;
  justify-content:center;
  padding: 20px 100px;;
  .load{
    padding: 40px 0;
    button{
      height:40px;
      padding: 5px;
      background-color: #D8DAAA;
      border-radius:5px;
      border:none;
      width:150px;
      font-family: 'Poppins', sans-serif;
    }
  }
   @media  only screen and (max-width:320px){
        padding: 20px;
    }
    @media  only screen and (min-width:321px) and (max-width:540px){
        padding: 20px 30px;
    }
     @media  only screen and (min-width:541px) and (max-width:720px){
         padding: 20px 50px;
    }
}

.report{
  width:100%;
  text-align: center;
  padding: 30px 0 0px 0;
  background-color: #feffe9;
   p{
    color:#757575;
    a{
      color:#045B7E;
      font-weight: 700;
      text-decoration: none;;
    }
  }
  @media  only screen and (max-width:320px){
        padding: 30px 20px 0 20px;
        p{
          font-size:14px;
        }
    }
    @media  only screen and (min-width:321px) and (max-width:540px){
        padding: 30px 30px 0 20px;
        p{
          font-size:14px;
        }
    }
     @media  only screen and (min-width:541px) and (max-width:720px){
         padding: 20px 50px;
    }
}
 
 

</style>
