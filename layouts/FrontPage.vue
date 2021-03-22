<template>
  <div>
    <Header />
    <Nuxt />
    <Footer />
  </div>
</template>



<style>

.wrapper {
  padding: 4em 0 2em 0;
}

.wrapper.split .primary {
  padding: 3em 3em 1em 0;
}

.wrapper.split .secondary > section {
  padding: 3em 0 1em 3em;
}
.wrapper.split .primary {
  padding: 3em 0 1em 0;
  float: left;
  width: 100%;
}

.wrapper.split .secondary {
  float: flex;
  width: 100%;
}

.wrapper.split .secondary > section {
  padding: 3em 3em 1em 3em;
  left: -3em;
  width: calc(100% + 6em);
}

.wrapper.split .secondary > section:before {
  width: 100%;
}

.wrapper:after {
  clear: both;
  content: "";
  display: block;
}

.wrapper.split {
  overflow-x: hidden;
  padding: 0;
}

.wrapper.split .primary {
  padding: 6em 4em 4em 0;
  float: left;
  width: 50%;
}

.wrapper.split .secondary {
  color: #838886;
  float: left;
  width: 50%;
}

.wrapper.split .secondary > section {
  padding: 4em 0 2em 4em;
  color: #000000;
  position: relative;
}

.wrapper.split .secondary > section > * {
  position: relative;
  z-index: 1;
}

.wrapper.split .secondary > section:before {
  content: "";
  display: block;
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 1000%;
  z-index: 0;
}

.wrapper.split .secondary > section:nth-child(2n):before {
  background: #ffffff;
}

.wrapper.split .secondary > section:nth-child(2n + 1):before {
  background: #f5f5f5;
}

.wrapper.split .secondary > section h1,
.wrapper.split .secondary > section h2,
.wrapper.split .secondary > section h3,
.wrapper.split .secondary > section h4,
.wrapper.split .secondary > section h5,
.wrapper.split .secondary > section h6 {
  color: #000000;
}

.wrapper.split .secondary > section strong,
.wrapper.split .secondary > section b {
  color: #000000;
}

.wrapper.split .secondary > section header p {
  color: #070707;
}

.wrapper.split .secondary > section input[type="submit"],
.wrapper.split .secondary > section input[type="reset"],
.wrapper.split .secondary > section input[type="button"],
.wrapper.split .secondary > section .button {
  border-color: #000000;
  color: #000000 !important;
}

.wrapper.split .secondary > section input[type="submit"]:hover,
.wrapper.split .secondary > section input[type="reset"]:hover,
.wrapper.split .secondary > section input[type="button"]:hover,
.wrapper.split .secondary > section .button:hover {
  background-color: rgba(144, 144, 144, 0.075);
}

.wrapper.split .secondary > section input[type="submit"]:active,
.wrapper.split .secondary > section input[type="reset"]:active,
.wrapper.split .secondary > section input[type="button"]:active,
.wrapper.split .secondary > section .button:active {
  background-color: rgba(144, 144, 144, 0.2);
}

.wrapper.split .secondary > section .image.style2 {
  background: rgba(144, 144, 144, 0.075);
}

.wrapper.style1 {
  background-color: #323232;
  color: #ffffff;
}

.wrapper.style1.split .secondary > section h1,
.wrapper.style1.split .secondary > section h2,
.wrapper.style1.split .secondary > section h3,
.wrapper.style1.split .secondary > section h4,
.wrapper.style1.split .secondary > section h5,
.wrapper.style1.split .secondary > section h6 {
  color: #000000;
}

.wrapper.style1 h1,
.wrapper.style1 h2,
.wrapper.style1 h3,
.wrapper.style1 h4,
.wrapper.style1 h5,
.wrapper.style1 h6,
.wrapper.style1 strong,
.wrapper.style1 b {
  color: #ffffff;
}

.wrapper.style1 header p {
  color: #000000;
}

.wrapper.style1 input[type="submit"],
.wrapper.style1 input[type="reset"],
.wrapper.style1 input[type="button"],
.wrapper.style1 .button {
  border-color: #ffffff;
  color: #ffffff !important;
}

.wrapper.style1 input[type="submit"]:hover,
.wrapper.style1 input[type="reset"]:hover,
.wrapper.style1 input[type="button"]:hover,
.wrapper.style1 .button:hover {
  background-color: rgba(255, 255, 255, 0.075);
}

.wrapper.style1 input[type="submit"]:active,
.wrapper.style1 input[type="reset"]:active,
.wrapper.style1 input[type="button"]:active,
.wrapper.style1 .button:active {
  background-color: rgba(255, 255, 255, 0.2);
}

.wrapper.style1 .image.style2 {
  background: rgba(255, 255, 255, 0.2);
}

.wrapper.style1 blockquote.testimonial p {
  background-color: rgba(0, 0, 0, 0.25);
}

.wrapper.style1 blockquote.testimonial p:after {
  border-top-color: rgba(0, 0, 0, 0.25);
}

.wrapper.style1 blockquote.testimonial cite .name {
  color: #ffffff;
}

.wrapper.style1 blockquote.testimonial cite .title {
  color: #f9c3c0;
}

.wrapper.style1 .tree:before {
  background: #ffffff;
}

.wrapper.style1 .tree:after {
  background: #ffffff;
}

.wrapper.style1 .icon.major:before {
  color: #000000;
}

.wrapper.style1 .icon.major:after {
  background: #ffffff;
}


</style>