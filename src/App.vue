<template>
  <div id="app">
    <div id="menu">
      <div id="side">
        <router-link to="/">Home</router-link>
        <router-link to="/about">
          About Each Character
        </router-link>
        <router-link to="/fight">
          View Fight
        </router-link>
      </div>
    </div>
    <router-view />
    <div id="footer"> 
      <a href="https://github.com/adamscott95/creative-project-3"><p>View my Github Repo here.</p></a>
    </div>
  </div>
</template>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 50px 100px;

}

#heading {
  display: flex;
  justify-content: center;
}

#menu {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 5px;
  grid-template-areas: "none brand side";
  margin-bottom: 50px;
}

#menu a {
  color: #B84901;
}

#brand {
  grid-area: brand;
  display: flex;
  justify-content: center;
}

#brand img {
  height: 200px;
}

#side {
  grid-area: side;
  display: flex;
  justify-content: flex-end;
  flex-direction: column;
}

#side img {
  width: 50px;
}

.menu-item {
  display: flex;
  flex-direction: column;
}

.menu-item p {
  margin: 0px;
}

.browse {
  margin-right: 50px;
}

#footer {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background-color: rgb(242, 242, 243);
    margin-top: 5%;
    width: 100%;
}

#footer p {
    padding-bottom: 0;
    padding-top: 1%;
    order: 1;
}
</style>
