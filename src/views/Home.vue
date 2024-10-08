<script>
export default {
  name: 'Home',
  data() {
    return {
      jumboBackground: '../src/assets/img/jumbo_back.jpg',
      avatar: '../src/assets/img/avatar.jpg',
    };
  }
}
</script>

<template>
  <main>
    <div class="jumbotron">
      <div class="container">
        <div class="info">
            <div class="text">
              <h1>
              Hi there! I am  <br> <span class="name">Samuele Cozzubbo</span>
              </h1>
              <br>
              <h4>
                Full stack web developer
              </h4>
              <br>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam deserunt temporibus, facilis nobis necessitatibus voluptatem velit ut repellendus. Suscipit necessitatibus eaque ab quas sint commodi dolorum totam beatae omnis repudiandae.
              </p>
            </div>
            <a class="btn">
            About me
            </a>
            <div class="links">
                <ul>
                  <li class="icon">
                    <a href="#"><i class="fa-brands fa-linkedin"></i></a>
                  </li>
                  <li class="icon">
                    <a href="#"><i class="fa-brands fa-github"></i></a>
                  </li>
                </ul>
            </div>
        </div>
        <div class="avatar">
          <img :src="avatar" alt="">
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss">
.jumbotron{
  width: 100vw;
  height: calc(100vh - 50px);
  background-image: url('../assets/img/jumbo_back.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  display: flex;
  align-items: center;
  justify-content: center;

  .container{
    background-color: rgb(171, 167, 167,0.2);
    max-width: 1120px;
    padding: 0 20px;
    margin: 0 auto;
    //height: 500px;
    display: flex;
    justify-content: space-between;

    .info{
      max-width: 40%;
      padding: 10px 0;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      .name{
        font-weight: bold;
      }
      h1{
      color: rgb(30, 30, 30);
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
    }

      .btn{
        background:hsla(160, 100%, 37%, 1);
        border-radius: 25px;
        padding: 10px 20px;
        border: 1px solid black;
        box-shadow: 1px 1px lightgray;
        color: rgb(30, 30, 30);
        margin: 20px 0;
        transition: all 0.2s;
        &:hover{
          cursor: pointer;
          background-color: rgb(30, 30, 30);
          color: hsla(160, 100%, 37%, 1);
          box-shadow: 0px 0px 15px 5px hsla(160, 100%, 37%, 0.8);
          transition: all 0.2s;
        }
      }
      .links{
        ul{
          display: flex;
          gap: 20px;
          list-style: none;
          .icon{
            font-size: 2rem;
            &:hover{
              border-bottom: 1px solid white;
            }
          };
        }
      }
    }

    /* AVATAR */
    .avatar{
      align-self: center;
      img{
        width: 300px;
        border-radius: 50%;
        
      }
    }
  }
}

@media (max-width: 768px) {
      .jumbotron{
        display: inline-block;
      }
    .container {
      flex-direction: column;
      
      .info {
        max-width: 80%!important;
        margin-bottom: 20px;
      }

      .avatar {
        img {
          position: absolute;
          max-width: 100px;
          top: 60px;
          right: 20px;
        }
      }

      .hamburger {
        display: block;
        position: absolute;
        top: 20px;
        right: 20px;
        z-index: 10;
      }
    }
}
</style>
