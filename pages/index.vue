<template>
  <main>
    <img src="~/assets/images/intro2.png" width="100%" />
    
    
      <section class="wrapper style1 split">
        <div class="container">
          <div class="primary">
            <h2>Objective</h2>
            <p>
              NEWTON aims to demonstrate the potential improvement of short-term
              dust forecasts via the assimilation of Aeolus wind profiles.
            </p>
            <ul class="actions">
              <li>
                <a href="about.html#Objectives" class="button">Learn More</a>
              </li>
            </ul>
          </div>
          <div class="secondary">
            <section>
              <h3><a href="about.html">Approach</a></h3>
              <p>
                Towards the derivation of novel and unique scientific outcomes,
                regional modelling simulations, initialized with IFS
                meteorological fields with and without assimilated Aeolus L2B
                data, will be performed, whereas a variety of reference datasets
                will be utilized for the assessment of the potential
                improvements on dust forecasts.
              </p>
              <a class="button"><NuxtLink to="intro#Approach">Learn More</NuxtLink></a>
            </section>
            <section>
              <h3>Programme of Work</h3>
              <a href="about.html#Programme" class="button">Learn More</a>
            </section>
          </div>
        </div>
      </section>
    
  </main>
</template>

<script>
import Header from "~/components/Header.vue";

export default {
  components: { Header },
  layout: "Button",
  layout: "FrontPage",
};
</script>


