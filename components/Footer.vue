<template>
    <!-- Footer main -->
    <section class="ft-main">
      <div class="ft-main-item">
        <span class="image left"
          ><a href="https://www.noa.gr/en/" target="_blank"
            ><img src="~/assets/images/institutions/noa_footer2.png" alt="" /></a
        ></span>
        <span class="image left"
          ><a href="https://www.astro.noa.gr/en/" target="_blank"
            ><img src="~/assets/images/institutions/iaasars_fotter2.png" alt="" /></a
        ></span>
        <span class="image left"
          ><a href="https://react.space.noa.gr" target="_blank"
            ><img src="~/assets/images/institutions/react_footer2.png" alt="" /></a
        ></span>
        <span class="image left"
          ><a href="https://www.cyi.ac.cy/" target="_blank"
            ><img src="~/assets/images/institutions/cyi_footer.png" alt="" /></a
        ></span>
        <span class="image left"
          ><a href="https://www.esa.int/" target="_blank"
            ><img src="~/assets/images/institutions/esa_footer2.png" alt="" /></a
        ></span>
      </div>
      <div class="ft-main-item">
        <ul class="ft-social-list">
          <li>
            <a href="https://www.facebook.com/noa.react"
              ><i class="fab fa-facebook"></i
            ></a>
          </li>
          <li>
            <a href="mailto:react@noa.gr"><i class="fas fa-envelope"></i></a>
          </li>
          <li>
            <a href="https://www.linkedin.com/company/noa-react/"
              ><i class="fab fa-linkedin"></i
            ></a>
          </li>
          <li>&copy; ReACT Team, National Observatory of Athens</li>
        </ul>
      </div>
    </section>

</template>



<style>
* {
  box-sizing: border-box;
  font-family: "Lato", sans-serif;
  margin: 0;
  padding: 0;
}
ul {
  list-style: none;
  padding-left: 0;
}
footer {
  background-color: #f5f5f5;
  color: rgb(0, 0, 0);
  line-height: 1.5;
}
footer a {
  text-decoration: none;
  color: rgb(0, 0, 0);
}
a:hover {
  text-decoration: underline;
}
.ft-title {
  color: #fff;
  font-family: "Merriweather", serif;
  font-size: 1.375rem;
  padding-bottom: 0.625rem;
}
/* Sticks footer to bottom */
body {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
}
.container {
  flex: 1;
}
/* Footer main */
.ft-main {
  padding: 1.25rem 1.875rem;
  display: flex;
  flex-wrap: wrap;
}
@media only screen and (min-width: 29.8125rem /* 477px */) {
  .ft-main {
    justify-content: space-evenly;
  }
}
@media only screen and (min-width: 77.5rem /* 1240px */) {
  .ft-main {
    justify-content: space-evenly;
  }
}
.ft-main-item {
  padding: 1.25rem;
  min-width: 12.5rem;
}

/* Footer social */
.ft-social {
  padding: 0 1.875rem 1.25rem;
}
.ft-social-list {
  display: flex;
  justify-content: center;
  border-top: 1px #f5f5f5 solid;
  padding-top: 1.25rem;
}
.ft-social-list li {
  margin: 0.5rem;
  font-size: 1.25rem;
}
/* Footer legal */
.ft-legal {
  padding: 0.9375rem 1.875rem;
  background-color: #333;
}
.ft-legal-list {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}
.ft-legal-list li {
  margin: 0.125rem 0.625rem;
  white-space: nowrap;
}
/* one before the last child */
.ft-legal-list li:nth-last-child(2) {
  flex: 1;
}
</style>