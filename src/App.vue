<template>
  <div id="app">
    <div id="navbar">
      <div id="navbar__top">
        <div id="navbar__top__content">
          <div id="navbar__title">Software Procurement Portal</div>
          <button id="navbar__btn-login" class="btn--green btn--small">Log in</button>
        </div>
      </div>
      <div id="navbar__bottom">
        <div id="navbar__bottom__content">
          <div id="navbar__bottom__links"></div>
          <router-link to="/" class="navbar__bottom__link" id="navbar_home">Home</router-link>
          <router-link to="/request-list" class="navbar__bottom__link" id="navbar_placeholder">Requests</router-link>
        </div>
      </div>
    </div>
    <div id="body">
      <router-view id="content"/>
    </div>
    <div id="footer"></div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
html, body {
  padding: 0;
  margin: 0;
}
a {
  text-decoration: inherit;
  color: inherit;
}
.basic-link:hover {
  text-decoration: underline;
}
button {
  transition: all 0.2s ease 0s;
}
button:hover {
  cursor: pointer;
}
.btn--green {
  border: none;
  color: #F2FAFD;
  background: #55BA47;
}
.btn--green:hover {
  background: #499e3e;
}
.btn--green:active {
  background: #408a36;
}
.btn--blue {
  border: none;
  color: #F2FAFD;
  background: #0098DB;
}
.btn--blue:hover {
  background: #0085be;
}
.btn--blue:active {
  background: #0071a1;
}
.btn--small {
  border-radius: 4px;
  padding: 16px 32px;
  box-shadow: 1px 1px 4px 0 rgba(0,0,0,0.1),
              2px 4px 4px 0 rgba(0,0,0,0.05);
}
.btn--large {
  border-radius: 8px;
  padding: 16px 32px;
  box-shadow: 1px 1px 4px 0 rgba(0,0,0,0.1),
              2px 4px 4px 0 rgba(0,0,0,0.05);
}
.btn--full {
  border-radius: 8px;
  padding: 16px 0;
  width: 100%;
  font-size: 1.3rem;
  box-shadow: 1px 1px 4px 0 rgba(0,0,0,0.1),
              2px 4px 4px 0 rgba(0,0,0,0.05);
}
#app {
  font-family: Arial, Helvetica, 'Avenir', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  width: 100vw;
  height: 100vh;

  display: grid;
  grid-template-rows: 2fr 11fr 1fr;
  grid-template-columns: 2fr 6fr 2fr;
  background: #F4F4F5;
}
#navbar {
  grid-row: 1 / 2;
  grid-column: 1 / 4;
  display: flex;
  flex-direction: column;
}
#navbar__top {
  z-index: 101;
  width: 100%;
  height: 50%;
  background: #1F2C33;
  justify-content: space-between;
  /* box-shadow: 1px 2px 6px 0 rgba(0,0,0,0.125),
              2px 4px 12px 0 rgba(0,0,0,0.075); */

  display: grid;
  grid-template-columns: 24% 52% 24%;
}
#navbar__top__content {
  grid-column: 2 / 3;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
#navbar__title {
  font-size: 2rem;
  color: #F2FAFD;
  margin: 0;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.075);
}
#navbar__btn-login {
  margin: 0 20px;
}
#navbar__bottom {
  z-index: 100;
  width: 100%;
  height: 50%;
  background: linear-gradient(to right, #14a9e9 , #0098d8);
  color: #F2FAFD;
  /* box-shadow: 1px 2px 6px 0 rgba(0,0,0,0.125),
              2px 4px 12px 0 rgba(0,0,0,0.075); */

  display: grid;
  grid-template-columns: 24% 52% 24%;
}
#navbar__bottom__content {
  height: 100%;
  grid-column: 2 / 3;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
#navbar__bottom__links {
  margin: 0;
}
.navbar__bottom__link {
  height: 100%;
  padding: 0 32px;
  display: flex;
  align-items: center;
  transition: all 0.2s ease 0s;
}
.navbar__bottom__link:hover {
  color: #0098d8;
  background: #F4F4F5;
  cursor: pointer;
}
.navbar__bottom__link:active {
  color: #0098d8;
  background: #F4F4F5;
}
#body {
  width: 100%;
  grid-row: 2 / 3;
  grid-column: 1 / 4;
  margin: 0;
  padding: 0;
  background: #F4F4F5;
  display: grid;
  grid-template-rows: 10% 80% 10%;
  grid-template-columns: 24% 52% 24%;
  align-items: center;
}
#content {
  grid-row: 2 / 3;
  grid-column: 2 / 3;
  width: 100%;
  box-sizing: border-box;
  background: #FFFFFF;
  /* padding: 0; */
  border-radius: 8px;
  box-shadow: 0px 1px 4px 0 rgba(0,0,0,0.1),
              0px 4px 4px 0 rgba(0,0,0,0.05);
}
#footer {
  z-index: 101;
  width: 100%;
  height: 100%;
  background: #1F2C33;
  grid-row: 3 / 4;
  grid-column: 1 / 4;
  /* box-shadow: 1px -2px 6px 0 rgba(0,0,0,0.125),
              2px -4px 12px 0 rgba(0,0,0,0.075); */
}
.page {
  padding: 20px;
}
.page__header {
  width: 100%;
  padding: 0 0 8px;
  margin: 0 0 16px;
  border-bottom: 2px solid rgba(31, 44, 51, 0.1);
}
.page__title {
  /* display: inline-block; */
  /* text-align: center; */
  padding: 0;
  margin: 0;
  font-size: 2.1rem;
}
</style>
