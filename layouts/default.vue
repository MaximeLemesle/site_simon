<template>
  <div class="DefaultLayout">
    <!-- Header -->
    <slot />
    <!-- Footer -->
  </div>
</template>
<style>
/* Base */
html {
    background: #060b13;
}
* {
    font-family: DM Sans;
}


/* Links */
a {
    transition: color .1s ease-in-out;
}
a:hover {
    text-decoration: underline;
    color: #002366;
}


/* Heading */
.h1 {
  font-family: Dela Gothic One;
  font-size: 64px;
  text-transform: uppercase;
  line-height: normal;
}
.h2 {
  font-family: Airstrike;
  font-size: 48px;
  text-transform: uppercase;
  line-height: normal;
}
.h3 {
  font-family: Airstrike;
  font-size: 32px;
  text-transform: uppercase;
  line-height: normal;
}
.h4 {
  font-family: Airstrike;
  font-size: 24px;
  text-transform: uppercase;
  line-height: normal;
}


/* Text */
.italic {
    font-style: italic;
}

.nav-font {
  font-size: 24px;
  transition: color 300ms ease-in-out;
}

.nav-font:hover {
  color: #3d598f;
  text-decoration: none;
}

.footer-font {
    font-size: 12px;
}

/* Colors */
.primary-100 {
  color: #ecf1f9;
}
.primary-300 {
  color: #9cacc9;
}
.primary-500 {
  color: #3d598f;
}
.primary-700 {
  color: #002366;
}
.primary-900 {
  color: #001233;
}

.neutre-0 {
  color: #ffffff;
}
.neutre-900 {
  color: #060b13;
}


/* Background */
.bg-primary-100 {
  background-color: #ecf1f9;
}
.bg-primary-300 {
  background-color: #9cacc9;
}
.bg-primary-500 {
  background-color: #3d598f;
}
.bg-primary-700 {
  background-color: #002366;
}
.bg-primary-900 {
  background-color: #001233;
}

.bg-neutre-0 {
  background-color: #ffffff;
}
.bg-neutre-900 {
  background-color: #060b13;
}


/* Buttons */
.btn {
    padding: 1rem 2rem;
    text-transform: uppercase;
    font-family: Airstrike;
    font-size: 1.5rem;
    line-height: normal;
    width: fit-content;
    transition: all 300ms ease-in-out;
}

.btn:hover {
    text-decoration: none;
}

.btn-primary {
    background-color: #002366;
    color: #ffffff;
}

.btn-primary:hover {
    background-color: #ECF1F9;
    color: #002366;
}

.btn-secondary {
    background-color: #9CACC9;
    color: #ffffff;
}

.btn-secondary:hover {
    background-color: #ECF1F9;
    color: #002366;
}
</style>
