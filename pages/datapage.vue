<template>
  <div id="main" class="wrapper style3">
    <div class="container medium">
      <header class="major">
        <h2>Scientific Data</h2>
        <p>Complete the form to request access to the Scientific Data</p>
      </header>

      <!-- Content -->
      <section id="content">
        <form method="post" action="#">
          <div class="row gtr-uniform">
            <div class="col-6 col-12-xsmall">
              <input
                type="text"
                name="name"
                id="name"
                value=""
                placeholder="Name*"
              />
            </div>
            <div class="col-6 col-12-xsmall">
              <input
                type="text"
                name="surname"
                id="surname"
                value=""
                placeholder="Surname*"
              />
            </div>
            <div class="col-12">
              <input
                type="email"
                name="email"
                id="email"
                value=""
                placeholder="Email*"
              />
            </div>
            <div class="col-12">
              <input
                type="text"
                name="institution"
                id="institution"
                value=""
                placeholder="Institution*"
              />
            </div>
            <div class="col-12">
              <textarea
                name="message"
                id="message"
                placeholder="Enter your message*"
                rows="6"
              ></textarea>
            </div>
            <p><i>The fields with an asterisk are required fields</i></p>
            <div class="col-12">
              <ul class="actions special">
                <li>
                  <input type="submit" value="Request Access" class="primary" />
                </li>
              </ul>
            </div>
          </div>
        </form>
      </section>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>