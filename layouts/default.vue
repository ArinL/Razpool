<template>
  <div>
    <alheader>
      <template slot="title">{{ title }}</template>
      <nuxt-link slot="link" v-for="(link, index) in links" :key="index" :to="link.url">{{ link.name }}</nuxt-link>
    </alheader>
    <nuxt/>
    <alfooter>
      <template slot="title">{{ title }}</template>
    </alfooter>
  </div>
</template>

<script>
import alheader from "~/components/Header.vue";
import alfooter from "~/components/Footer.vue";

export default {
  components: {
    alheader,
    alfooter
  },
  data() {
    return {
      title: "razpool",
      links: [
        {
          name: "About",
          url: "about"
        },
        {
          name: "Services",
          url: "services"
        },
        {
          name: "Contact",
          url: "contact"
        }
      ]
    };
  }
};
</script>

<style>
html {
  box-sizing: border-box;

  font: 16px "Source Sans Pro", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  -webkit-text-size-adjust: 100%;
  -ms-text-size-adjust: 100%;
  word-spacing: 1px;
}

p {
  line-height: 1.5;
}

body {
  background: #f1f5f9;
}

html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
b,
u,
i,
center,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
embed,
figure,
figcaption,
footer,
header,
hgroup,
main,
menu,
nav,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
  padding: 0;
  margin: 0;
  border: 0;
  font-size: 100%;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section {
  display: block;
}
/* HTML5 hidden-attribute fix for newer browsers */
*[hidden] {
  display: none;
}
body {
  line-height: 1;
}
ol,
ul {
  list-style: none;
}
a {
  font-weight: normal;
  text-decoration: none;
  color: initial;
}
blockquote,
q {
  quotes: none;
}
blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}
table {
  border-spacing: 0;
  border-collapse: collapse;
}
</style>
