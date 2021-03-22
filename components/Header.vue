<template>
  <header id="header">
    <NuxtLink to="/"><h1>NEWTON</h1></NuxtLink>
    <nav id="nav">
      <ul>
        <li class="current"><NuxtLink to="/">Home</NuxtLink></li>
        <li>
          <NuxtLink to="/intro">About</NuxtLink>
          <ul>
            <li><NuxtLink to="/intro#Οbjectives">Objectives</NuxtLink></li>
            <li><NuxtLink to="/intro#Approach">Approach</NuxtLink></li>
            <li><NuxtLink to="/intro#Programme">Work Programme</NuxtLink></li>
          </ul>
        </li>
        <li class="current"><NuxtLink to="/technicaldocs">Technical Documents</NuxtLink></li>
        <li class="current"><NuxtLink to="/datapage">Data</NuxtLink></li>
        <li>
          <NuxtLink to="/institutions">Participants</NuxtLink>
          <ul>
            <li><NuxtLink to="/intro">Institutes</NuxtLink></li>
            <li><NuxtLink to="/intro#People">People</NuxtLink></li>
          </ul>
        </li>
        <li>
          <NuxtLink to="/outreach">Outreach</NuxtLink>
          <ul>
            <li><NuxtLink to="/intro#News">News</Nuxtlink></li>
            <li><NuxtLink to="/intro#Papers">Papers</NuxtLink></li>
            <li><NuxtLink to="/intro#Conferences">Conferences</NuxtLink></li>
          </ul>
        </li>
        <li><NuxtLink to="/community">Community</NuxtLink></li>
      </ul>
    </nav>
  </header>
</template>



<style>
#header {
  background: #000000;
  box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.125);
  color: #dfdfe4;
  height: 4.5em;
  left: 0;
  line-height: 4.5em;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 10000;
  padding-top: 0em;
}

#header .container {
  position: relative;
}

#header .icon:before {
  color: #7bceba;
  line-height: inherit;
  font-size: 0.9em;
}

#header h1,
#header h2,
#header h3,
#header h4,
#header h5,
#header h6,
#header strong,
#header b {
  color: #ffffff;
}

#header h1 {
  font-size: 1.25em;
  height: inherit;
  left: 2%;
  line-height: inherit;
  position: absolute;
  top: 0;
}

#header h1 a.icon:before {
  margin-right: 0.5em;
}

#header nav {
  height: inherit;
  line-height: inherit;
  position: absolute;
  right: 0;
  top: 0;
}

#header nav > ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

#header nav > ul > li {
  -moz-transition: background-color 0.2s ease-in-out;
  -webkit-transition: background-color 0.2s ease-in-out;
  -ms-transition: background-color 0.2s ease-in-out;
  transition: background-color 0.2s ease-in-out;
  display: inline-block;
  margin: 0 auto; /*---this one changes the space between items---*/
  padding: 0;
}

#header nav > ul > li > a {
  color: #ffffff;
  display: block;
  font-family: "Montserrat", Helvetica, sans-serif;
  font-weight: 700;
  letter-spacing: 0.05em;
  line-height: 2.5em;
  padding: 0 1em;
  text-decoration: none;
  text-transform: uppercase;
}

#header nav > ul > li > a.icon:before {
  margin-right: 0.5em;
}

#header nav > ul > li.active {
  background-color: rgba(0, 0, 0, 0.075);
}

#header nav > ul > li.current {
  background-color: rgba(0, 0, 0, 0.25);
}

#header nav > ul > li > ul {
  display: none;
}

#header nav > ul > li:last-child {
  margin-right: 0;
}

.dropotron {
  background: #6382a0;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.075);
  color: #dfdfe4;
  list-style: none;
  margin-top: -0.5em;
  min-width: 15em;
  padding: 0.5em 0;
}

.dropotron > li {
  box-shadow: inset 0 1px 0 0 rgba(255, 255, 255, 0.1);
  padding: 0;
}

.dropotron > li > a {
  color: #dfdfe4;
  display: block;
  font-family: "Montserrat", Helvetica, sans-serif;
  font-weight: 400;
  letter-spacing: 0.05em;
  line-height: 2.75em;
  padding: 0 1em;
  text-decoration: none;
  text-transform: uppercase;
}

.dropotron > li:hover > a,
.dropotron > li.active > a {
  background-color: #7bceba;
  color: #ffffff !important;
}

.dropotron > li:first-child {
  box-shadow: none !important;
}

.dropotron.level-0 {
  font-size: 0.8em;
  margin-top: 3.5em;
}

.dropotron.level-0:before {
  border-bottom: solid 1em #6382a0;
  border-left: solid 1em transparent;
  border-right: solid 1em transparent;
  content: "";
  display: block;
  height: 2em;
  left: 50%;
  margin-left: -1em;
  position: absolute;
  top: -2em;
  width: 2em;
}
</style>