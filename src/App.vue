<template>
  <div id="app">
    <div id="nav">
      <div class="section-top">
        <div class="inner">
          <div class="logo">
            <img alt="Strydom Accounting Logo" src="./assets/logo.png">
            <h1>Strydom Accounting</h1>
            <h2>Black & White Accounting Services</h2>
          </div>
          <div class="nav">
            <div class="nav-inner">
              <router-link class="animated primary" to="/">Home</router-link>
              <router-link class="animated primary" to="/about">About</router-link>
            </div>
          </div>
        </div>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss" scoped>
  @import 'assets/scss/main';
  #app {
    .section-top {
      background: $primary;
      width: 100%;
      margin-bottom: 0;
      position: relative;
      padding-bottom: 100px;
      overflow: hidden;

      .inner {
        display: flex;
        align-items: flex-end;
        max-width: $viewport-lg;
        width: 100%;
        margin: 0 auto;
        align-items: flex-end;
      }

      &:after {
        bottom: 0;
        z-index: 1;
        position: absolute;
        min-width: 200%;
        height: 120px;
        background: $secondary;
        content: "";
        transform: rotate(-2deg) translateX(-50%);
      }
    }

    .nav {
      flex: 0 0 auto;

      .nav-inner {
        padding: 0 20px 20px;

        a {
          font-size: 1.5rem;
        }
      }
    }

    .logo {
      flex: 0 0 auto;
      padding: 20px;
      max-width: 400px;
      flex-wrap: wrap;
      text-align: center;

      img {
        width: 80px;
        height: auto;
        margin: {
          bottom: 15px;
        }
      }

      h1, h2 {
        color: #fff;
        margin: 0 auto 10px;
        padding: 0;
      }

      h1 { 
        font-size: 1.5rem;
        text-transform: uppercase;
      }

      h2 {
        font-size: 1em;
        font-weight: 100;
      }
    }

    @include respond-to($viewport-md) {
      .section-top {
        padding-bottom: 40px;

        &:after {
          height: 40px;
        }

        .inner {
          flex-wrap: wrap;
          justify-content: center;

          .logo,
          .nav {
            min-width: 100%;
            text-align: center;
          }

          .logo {
            text-align: center;
          }
        }
      }  
    }

    @include respond-from($viewport-md) {
      .section-top {
        .inner {
          .nav {
            margin: {
              bottom: 100px;
              left: 20px;
            }
          }
        }
      }  
    }

    @include respond-from($viewport-lg) {
      .section-top {  
        .inner {
          min-height: 250px;
          .nav {
            margin: {
              left: 120px;
            }
          }
        }
      }  
    }
  }
</style>
