<template>
  <section>
    <nav class="navbar navbar-expand-lg">
      <img class="ml-4" src="../../assets/logo_white.svg" alt />
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav w-100">
          <li class="nav-item active mr-auto">
            <a class="nav-link text-white pl-5" href="#">
              <svg
                id="Capa_1"
                class="mr-3"
                fill="#fff"
                enable-background="new 0 0 512 512"
                height="20"
                viewBox="0 0 512 512"
                width="20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="m512 358.121c0-68.38-26.629-132.667-74.98-181.02-48.353-48.352-112.64-74.98-181.02-74.98s-132.667 26.629-181.02 74.98c-48.351 48.353-74.98 112.64-74.98 181.02v15h205.016c4.085 12.323 12.371 22.642 23.657 29.305 8.558 5.052 17.953 7.453 27.236 7.453 18.406 0 36.36-9.448 46.376-26.413 1.956-3.313 3.522-6.781 4.717-10.345h204.998zm-235.548 10.093c-6.656 11.276-21.247 15.037-32.526 8.378-5.463-3.225-9.343-8.384-10.925-14.528-1.583-6.144-.679-12.535 2.547-17.998s8.385-9.343 14.528-10.925c1.976-.509 3.977-.76 5.964-.76 4.194 0 8.328 1.12 12.034 3.308 5.463 3.225 9.343 8.384 10.925 14.528 1.583 6.143.679 12.535-2.547 17.997zm31.689-25.093c-.032-.129-.057-.259-.09-.388-2.296-8.916-6.74-16.908-12.887-23.425l43.106-73.015-25.834-15.252-43.106 73.015c-8.675-2.233-17.819-2.264-26.737.032-13.903 3.581-25.58 12.362-32.879 24.726-2.674 4.53-4.636 9.344-5.882 14.307h-173.34c1.992-30.247 9.976-58.88 22.75-84.742l33.311 19.232 15-25.98-33.274-19.21c16.444-24.477 37.541-45.578 62.018-62.022l19.212 33.276 25.98-15-19.236-33.318c25.861-12.774 54.5-20.737 84.746-22.729v38.493h30v-38.493c30.246 1.992 58.885 9.955 84.746 22.729l-19.236 33.318 25.98 15 19.212-33.276c24.477 16.444 45.573 37.545 62.018 62.022l-33.274 19.21 15 25.98 33.311-19.232c12.774 25.862 20.758 54.495 22.75 84.742z"
                />
              </svg>
              Dashboard
              <span class="sr-only">(current)</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-white" href="#" tabindex="-1" aria-disabled="true">
              admin@gmail.com
              <svg
                version="1.1"
                id="Capa_1"
                class="mx-3"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                x="0px"
                y="0px"
                width="20"
                height="20"
                viewBox="0 0 451.847 451.847"
                fill="#fff"
                style="enable-background:new 0 0 451.847 451.847;"
                xml:space="preserve"
              >
                <g>
                  <path
                    d="M225.923,354.706c-8.098,0-16.195-3.092-22.369-9.263L9.27,151.157c-12.359-12.359-12.359-32.397,0-44.751
		c12.354-12.354,32.388-12.354,44.748,0l171.905,171.915l171.906-171.909c12.359-12.354,32.391-12.354,44.744,0
		c12.365,12.354,12.365,32.392,0,44.751L248.292,345.449C242.115,351.621,234.018,354.706,225.923,354.706z"
                  />
                </g>
              </svg>
            </a>
          </li>
        </ul>
      </div>
    </nav>
  </section>
</template>

<script>
export default {
  name: "TheNavbar",
};
</script>

<style lang="scss" scoped>
.navbar {
  background-image: linear-gradient(
    to right,
    rgba(0, 140, 255, 0.924),
    rgb(61, 174, 194)
  );
  padding: 25px;
}
</style>