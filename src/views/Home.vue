<script>
export default {
  name: 'Home',
  data() {
    return {
      jumboBackground: '../src/assets/img/jumbo_back.jpg',
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
              Hi there! <br> I am Samuele Cozzubbo
              </h1>
              <br>
              <h4>
                Full stack web developer
              </h4>
            </div>
            <a class="btn">
            About me
            </a>
            <div class="links">
                <ul>
                  <li>
                    1
                  </li>
                  <li>
                    2
                  </li>
                  <li>
                    3
                  </li>
                </ul>
            </div>
        </div>
        <div class="avatar">
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
  background-size: 100% auto;
  background-position: center;
  display: flex;
  align-items: center;
  justify-content: center;

  .container{
    background-color: rgb(171, 167, 167,0.2);
    width: 1500px;
    margin: 0 auto;
    height: 500px;
    display: flex;
    justify-content: space-between;

    .info{
      padding: 10px 0;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      h1{
      color: rgb(30, 30, 30);
    }

      .btn{
        background:hsla(160, 100%, 37%, 1);
        border-radius: 5px;
        padding: 5px 8px;
        border: 1px solid black;
        box-shadow: 1px 1px lightgray;
        color: rgb(30, 30, 30);
        align-self: flex-start;
        &:hover{
          cursor: pointer;
          background-color: rgb(30, 30, 30);
          color: hsla(160, 100%, 37%, 1);
          transition: all 0.2s;
        }
      }
      .links{
        ul{
          display: flex;
          list-style: none;
          justify-content: space-around;
          li{
            background-color: black;
            padding: 5px 10px;
            border-radius: 50%;
          };
        }
      }
    }

    
  }
}
</style>
