<template>
  <div class="card-story">
    <transition name="modal">
      <div v-if="isOpen">
        <div class="overlay" @click.self="isOpen = false;">
          <div class="modal">
              <div class="modal-header">
                  <div class="image-wrap">
                        <img :src="story.src" />
                    </div>
                    <div class="text-wrap">
                        <h5>{{story.topic}}</h5>
                        <p>by {{story.name}} <span>{{story.twitterHandle}}</span> </p>
                    </div>
                    <div class="numberOfLikes">
                      <button @click="increment"><i class="fas fa-heart"></i> LIKE</button>
                      <p class="likes">{{counter}} likes</p>
                    </div>
              </div>
              <div class="modal-content">
                 <p> {{story.content}}</p>
                 <p> {{story.content}}</p>
                 <p> {{story.content}}</p>
              </div>
              <div class="modal-footer">
                <div class="tag-tweet">
                    <div class="tag">
                    <p><i class="fas fa-tag"></i> </p> 
                  </div>
                  <div class="tweet">
                    <button><i class="fab fa-twitter"></i> TWEET</button>
                    <button><i class="fas fa-exclamation-triangle"></i> REPORT</button>
                  </div>
                </div>
                <div class="close">
                  <button @click="isOpen = false;"> Close </button>
                </div>
              </div>
            
          </div>
        </div>
      </div>
    </transition>
    <div class="inner-card">
      <div class="header-card">
        <div class="image-wrap">
          <img :src="story.src" />
        </div>
        <div class="text-wrap">
          <h5>{{story.name}}</h5>
          <p>{{story.profession}}</p>
        </div>
      </div>
      <div class="story-detail">
        <h5>{{story.topic}}</h5>
        <p>{{story.details}}</p>
        <button @click="isOpen=!isOpen">VIEW STORY</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Story",
  props: ["story"],
  data: function(){
    return {
      counter: 0,
      isOpen: false
    };
  },
    methods: {
      increment() { 
        this.counter++;
      }
    }
  
};
</script>

<style lang="scss">
$primary-color: #045b7e;
.modal {
  width: 60%;
  margin: 50px auto;
  border-radius:5px;
  background-color: #fff;
  border-radius: 2px;

  transition: all 0.2s ease-in;
  .modal-header{
      background-color: #f7f9de;
      width:100%;
      height:100px;
      border-top-left-radius: 5px;
      border-top-right-radius: 5px;
      padding:30px;
      display: flex;
      .text-wrap{
        padding-left:20px;
        margin-top: 5px;
        p{
          font-size:13px;
          color:#757575;
          font-weight: 400;
          span{
            color:#045B7E;
          }
        }
      }
      .numberOfLikes{
        margin-left:auto;
        display: flex;
        margin-top: 7px;
        button{
          height:35px;
          padding: 5px;
          background-color: #D8DAAA;
          border-radius:5px;
          border:none;
          cursor:pointer;
          width:100px;
          font-family: 'Poppins', sans-serif;
          i{
            margin-right: 8px;
          }
        }
        p{
          font-size:13px;
          margin:7px 0 0 10px;
        }
      }
  }
  .modal-content{
    padding:30px 50px;
    width:100%;
    overflow-y:scroll;
    min-height: auto;
    max-height:450px;

    p{
      font-size:14px;
      color:#9C9C9C;
      margin-bottom: 20px;
    }
  }
  .modal-footer{
    width:100%;
    height:150px;
    padding: 30px;
    background-color: #f7f9de;
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
    .tag-tweet{
      display: flex;
    }
    .tweet{
      margin-left: auto;
      button{
         height:32px;
          padding: 5px;
          background-color: #D8DAAA;
          border-radius:5px;
          font-size:12px;
          font-weight: 500;
          border:none;
          cursor:pointer;
          width:100px;
          font-family: 'Poppins', sans-serif;
          margin-left: 20px;
          i{
            margin-right: 7px;
          }
      }
    }
    .close{
      margin-top: 25px;
      @extend .tweet;
      margin-left:0;
      text-align: center;
      button{
        border:1px solid #045b7e;
        color:#045b7e;
        background-color: transparent;
        height:40px;
      }
    }

  }
   @media  only screen and (max-width:320px){
        width:95%;
        margin-top:10px;
        .modal-header{
          display: block;
          padding:15px;
          height:150px;
          .image-wrap{
            float: left;
          }
          .text-wrap{
            float: left;
            width:70%;
          }
          .numberOfLikes{
            margin-left: 0;
            display: block;
          }

        }
        .modal-content{
          padding:30px 20px;
        }
    }
    @media  only screen and (min-width:321px) and (max-width:540px){
        width:95%;
        margin-top:10px;
        .modal-header{
          display: block;
          padding:15px;
          height:150px;
          .image-wrap{
            float: left;
          }
          .text-wrap{
            float: left;
            width:80%;
            height: 70px;
          }
          .numberOfLikes{
            margin-left: 0;
            display: block;
            //float: right;
            padding-top:10px;
              width:70%;
            button{
              float: left;
            }
            p{
              margin-top:7px;
            }
          }

        }
        .modal-content{
          padding:30px 20px;
        }
    }
     @media  only screen and (min-width:541px) and (max-width:720px){
         padding: 20px 50px;
    }
}
.fadeIn-enter {
  opacity: 0;
}

.fadeIn-leave-active {
  opacity: 0;
  transition: all 0.2s step-end;
}

.fadeIn-enter .modal,
.fadeIn-leave-active.modal {
  transform: scale(1.1);
}


.overlay {
  position: fixed;
  top: 0;
  left: 0;
  // display: flex;
  // justify-content: center;
  // align-items: center;
  
  width: 100%;
  height: 100%;
  background: #00000099;
  z-index: 999;
  transition: opacity 0.2s ease;
   @media  only screen and (max-width:320px){
        overflow: scroll;
    }
    @media  only screen and (min-width:321px) and (max-width:540px){
        overflow: scroll;
    }
     @media  only screen and (min-width:541px) and (max-width:720px){
        overflow: scroll;
    }
}
.card-story {
  flex: 1 1 33.33%;
  width: 100%;
  padding: 20px;
  .inner-card {
    box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.15);
    border-radius: 5px;
    padding-bottom: 10px;
    background-color: #fff;
    .header-card {
      width: 100%;
      display: flex;
      height: 100px;
      padding: 30px;
      background-color: #f7f9de;
      img {
        height: 40px;
        width: 40px;
      }
      .text-wrap {
        margin-left: 20px;
        margin-top: -3px;
        h5 {
          font-size: 17px;
          font-weight: 500;
          margin-top: 0;
        }
        p {
          font-size: 13px;
          color: #9c9c9c;
        }
      }
    }

    .story-detail {
      padding: 30px;
      h5 {
        font-size: 18px;
      }
      p {
        color: #9c9c9c;
        margin: 15px 0 20px 0;
      }
      button {
        width: 100%;
        height: 45px;
        border: 1px solid $primary-color;
        background-color: transparent;
        color: $primary-color;
        border-radius: 5px;
        font-family: "Poppins", sans-serif;
        font-size: 13px;
        font-weight: 700;
        transition: 0.2s ease-in-out;
        cursor: pointer;
      }
      button:hover {
        background-color: $primary-color;
        border: none;
        color: #fff;
      }
    }
  }
   @media  only screen and (max-width:320px){
        padding:0 0 30px 0;
        .inner-card{
          .story-detail{
            p{
              font-size:14px;
            }
          }
        }
    }
    @media  only screen and (min-width:321px) and (max-width:540px){
        padding:0 0 30px 0;
        .inner-card{
          .story-detail{
            p{
              font-size:14px;
            }
          }
        }
    }
     @media  only screen and (min-width:541px) and (max-width:720px){
         padding:0 0 30px 0;
        .inner-card{
          .story-detail{
            p{
              font-size:14px;
            }
          }
        }
    }
}
</style>