<template>
  <footer class="bg-purple-700" aria-labelledby="footerHeading">
    <h2 id="footerHeading" class="sr-only">Footer</h2>
    <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <!-- Enlaces -->
        <div class="grid grid-cols-2 gap-8 xl:col-span-2">
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div
              v-for="(item, index) in footerItems"
              :key="item.title"
              :class="{ 'mt-12 md:mt-0': index === 1 }"
            >
              <h3
                class="
                  text-sm
                  font-semibold
                  text-white
                  tracking-wider
                  uppercase
                "
              >
                {{ item.title }}
              </h3>
              <ul class="mt-4 space-y-4">
                <li v-for="{ to, name } in item.items" :key="to">
                  <a
                    :href="to"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    {{ name }}
                  </a>
                </li>
              </ul>
            </div>
          </div>
          <!-- <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <h3
                class="
                  text-sm
                  font-semibold
                  text-white
                  tracking-wider
                  uppercase
                "
              >
                Company
              </h3>
              <ul class="mt-4 space-y-4">
                <li>
                  <a
                    href="#"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    About
                  </a>
                </li>

                <li>
                  <a
                    href="#"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    Blog
                  </a>
                </li>

                <li>
                  <a
                    href="#"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    Jobs
                  </a>
                </li>

                <li>
                  <a
                    href="#"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    Press
                  </a>
                </li>

                <li>
                  <a
                    href="#"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    Partners
                  </a>
                </li>
              </ul>
            </div>
            <div class="mt-12 md:mt-0">
              <h3
                class="
                  text-sm
                  font-semibold
                  text-white
                  tracking-wider
                  uppercase
                "
              >
                Legal
              </h3>
              <ul class="mt-4 space-y-4">
                <li>
                  <a
                    href="#"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    Claim
                  </a>
                </li>

                <li>
                  <a
                    href="#"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    Privacy
                  </a>
                </li>

                <li>
                  <a
                    href="#"
                    class="text-base text-purple-300 hover:text-white"
                  >
                    Terms
                  </a>
                </li>
              </ul>
            </div>
          </div>
          -->
        </div>

        <!-- Formulario-->
        <div class="mt-8 xl:mt-0">
          <h3 class="text-sm font-semibold text-white tracking-wider uppercase">
            Suscríbete a la newsletter
          </h3>
          <p class="mt-4 text-base text-purple-300">
            Las últimas noticias, artículos y recursos, directo a tu email.
          </p>
          <form
            id="revue-form-footer"
            class="mt-4 sm:flex sm:max-w-md"
            action="https://www.getrevue.co/profile/baumannzone/add_subscriber"
            method="post"
            name="revue-form"
            target="_blank"
          >
            <label for="member_email_footer" class="sr-only"
              >Introduce tu email en este campo si te quieres suscribir a la
              newsletter.</label
            >
            <input
              id="member_email_footer"
              name="member[email]"
              type="email"
              autocomplete="email"
              required
              class="
                appearance-none
                min-w-0
                w-full
                bg-white
                border border-transparent
                rounded-md
                py-2
                px-4
                text-base text-gray-900
                placeholder-gray-500
                focus:outline-none
                focus:ring-2
                focus:ring-offset-2
                focus:ring-offset-purple-800
                focus:ring-purple-300
                focus:border-purple-300
                focus:placeholder-purple-700
              "
              placeholder="Enter your email"
            />
            <div class="mt-3 rounded-md sm:mt-0 sm:ml-3 sm:flex-shrink-0">
              <button
                type="submit"
                class="
                  w-full
                  bg-purple-500
                  border border-transparent
                  rounded-md
                  py-2
                  px-4
                  flex
                  items-center
                  justify-center
                  text-base
                  font-medium
                  text-white
                  hover:bg-purple-600
                  focus:outline-none
                  focus:ring-2
                  focus:ring-offset-2
                  focus:ring-offset-gray-800
                  focus:ring-purple-500
                "
              >
                Suscríbete
              </button>
            </div>
          </form>
        </div>
      </div>
      <div
        class="
          mt-8
          border-t border-purple-800
          pt-8
          md:flex md:items-center md:justify-between
        "
      >
        <div
          class="
            flex flex-wrap
            space-x-6
            sm:order-2
            justify-start
            sm:justify-end
          "
        >
          <a
            v-for="{ name, url } in socialIcons"
            :key="name"
            class="text-purple-400 hover:text-purple-300 mb-2"
            :href="url"
            target="_blank"
          >
            <span class="sr-only">{{ name }}</span>
            <SvgIcon :icon-name="name" />
          </a>
        </div>
        <p class="mt-8 text-base text-purple-400 md:mt-0 md:order-1">
          &copy; 2021 Baumannzone - Desarrollo Full Stack JavaScript.
        </p>
      </div>
    </div>
  </footer>

  <!--  <footer aria-labelledby="footerHeading" class="bg-purple-800">
    <h2 id="footerHeading" class="sr-only">Footer</h2>
    <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8">
      <div class="xl:grid xl:grid-cols-3 xl:gap-10">
        <div class="space-y-8 xl:col-span-1">
          <img
            src="/_nuxt/img/rambito-js.da47b2b.png"
            alt="Baumannzone"
            class="h-10"
          />
          <p class="text-purple-200 text-base">
            Jorge Baumann - Open Source, Javascript, Vue, Firebase, CSS y
            desarrollo web.
          </p>
          <div class="flex space-x-6">
            <a
              href="https://instagram.com/baumannzone"
              class="text-purple-200 hover:text-white"
              ><span class="sr-only">instagram</span>
              <svg
                aria-hidden="true"
                focusable="false"
                data-prefix="fab"
                data-icon="instagram"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
                class="svg-inline&#45;&#45;fa fa-instagram fa-w-14 fa-lg"
              >
                <path
                  fill="currentColor"
                  d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"
                  class=""
                ></path></svg></a
            ><a
              href="https://twitter.com/baumannzone"
              class="text-purple-200 hover:text-white"
              ><span class="sr-only">twitter</span>
              <svg
                aria-hidden="true"
                focusable="false"
                data-prefix="fab"
                data-icon="twitter"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
                class="svg-inline&#45;&#45;fa fa-twitter fa-w-16 fa-lg"
              >
                <path
                  fill="currentColor"
                  d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z"
                  class=""
                ></path></svg></a
            ><a
              href="https://dev.to/baumannzone"
              class="text-purple-200 hover:text-white"
              ><span class="sr-only">dev</span>
              <svg
                aria-hidden="true"
                focusable="false"
                data-prefix="fab"
                data-icon="dev"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
                class="svg-inline&#45;&#45;fa fa-dev fa-w-14 fa-lg"
              >
                <path
                  fill="currentColor"
                  d="M120.12 208.29c-3.88-2.9-7.77-4.35-11.65-4.35H91.03v104.47h17.45c3.88 0 7.77-1.45 11.65-4.35 3.88-2.9 5.82-7.25 5.82-13.06v-69.65c-.01-5.8-1.96-10.16-5.83-13.06zM404.1 32H43.9C19.7 32 .06 51.59 0 75.8v360.4C.06 460.41 19.7 480 43.9 480h360.2c24.21 0 43.84-19.59 43.9-43.8V75.8c-.06-24.21-19.7-43.8-43.9-43.8zM154.2 291.19c0 18.81-11.61 47.31-48.36 47.25h-46.4V172.98h47.38c35.44 0 47.36 28.46 47.37 47.28l.01 70.93zm100.68-88.66H201.6v38.42h32.57v29.57H201.6v38.41h53.29v29.57h-62.18c-11.16.29-20.44-8.53-20.72-19.69V193.7c-.27-11.15 8.56-20.41 19.71-20.69h63.19l-.01 29.52zm103.64 115.29c-13.2 30.75-36.85 24.63-47.44 0l-38.53-144.8h32.57l29.71 113.72 29.57-113.72h32.58l-38.46 144.8z"
                  class=""
                ></path></svg></a
            ><a
              href="https://github.com/baumannzone"
              class="text-purple-200 hover:text-white"
              ><span class="sr-only">github</span>
              <svg
                aria-hidden="true"
                focusable="false"
                data-prefix="fab"
                data-icon="github"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 496 512"
                class="svg-inline&#45;&#45;fa fa-github fa-w-16 fa-lg"
              >
                <path
                  fill="currentColor"
                  d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"
                  class=""
                ></path></svg></a
            ><a
              href="https://www.youtube.com/channel/UCTTj5ztXnGeDRPFVsBp7VMA"
              class="text-purple-200 hover:text-white"
              ><span class="sr-only">youtube</span>
              <svg
                aria-hidden="true"
                focusable="false"
                data-prefix="fab"
                data-icon="youtube"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 576 512"
                class="svg-inline&#45;&#45;fa fa-youtube fa-w-18 fa-lg"
              >
                <path
                  fill="currentColor"
                  d="M549.655 124.083c-6.281-23.65-24.787-42.276-48.284-48.597C458.781 64 288 64 288 64S117.22 64 74.629 75.486c-23.497 6.322-42.003 24.947-48.284 48.597-11.412 42.867-11.412 132.305-11.412 132.305s0 89.438 11.412 132.305c6.281 23.65 24.787 41.5 48.284 47.821C117.22 448 288 448 288 448s170.78 0 213.371-11.486c23.497-6.321 42.003-24.171 48.284-47.821 11.412-42.867 11.412-132.305 11.412-132.305s0-89.438-11.412-132.305zm-317.51 213.508V175.185l142.739 81.205-142.739 81.201z"
                  class=""
                ></path></svg></a
            ><a
              href="https://twitch.tv/baumannzone"
              class="text-purple-200 hover:text-white"
              ><span class="sr-only">twitch</span>
              <svg
                aria-hidden="true"
                focusable="false"
                data-prefix="fab"
                data-icon="twitch"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
                class="svg-inline&#45;&#45;fa fa-twitch fa-w-16 fa-lg"
              >
                <path
                  fill="currentColor"
                  d="M391.17,103.47H352.54v109.7h38.63ZM285,103H246.37V212.75H285ZM120.83,0,24.31,91.42V420.58H140.14V512l96.53-91.42h77.25L487.69,256V0ZM449.07,237.75l-77.22,73.12H294.61l-67.6,64v-64H140.14V36.58H449.07Z"
                  class=""
                ></path></svg></a
            ><a
              href="https://codepen.com/baumannzone"
              class="text-purple-200 hover:text-white"
              ><span class="sr-only">codepen</span>
              <svg
                aria-hidden="true"
                focusable="false"
                data-prefix="fab"
                data-icon="codepen"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
                class="svg-inline&#45;&#45;fa fa-codepen fa-w-16 fa-lg"
              >
                <path
                  fill="currentColor"
                  d="M502.285 159.704l-234-156c-7.987-4.915-16.511-4.96-24.571 0l-234 156C3.714 163.703 0 170.847 0 177.989v155.999c0 7.143 3.714 14.286 9.715 18.286l234 156.022c7.987 4.915 16.511 4.96 24.571 0l234-156.022c6-3.999 9.715-11.143 9.715-18.286V177.989c-.001-7.142-3.715-14.286-9.716-18.285zM278 63.131l172.286 114.858-76.857 51.429L278 165.703V63.131zm-44 0v102.572l-95.429 63.715-76.857-51.429L234 63.131zM44 219.132l55.143 36.857L44 292.846v-73.714zm190 229.715L61.714 333.989l76.857-51.429L234 346.275v102.572zm22-140.858l-77.715-52 77.715-52 77.715 52-77.715 52zm22 140.858V346.275l95.429-63.715 76.857 51.429L278 448.847zm190-156.001l-55.143-36.857L468 219.132v73.714z"
                  class=""
                ></path></svg
            ></a>
          </div>
        </div>
        <div class="mt-12 grid grid-cols-2 gap-8 xl:mt-0 xl:col-span-2">
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <h3
                class="
                  text-sm
                  font-semibold
                  text-purple-100
                  tracking-wider
                  uppercase
                "
              >
                Secciones
              </h3>
              <ul class="mt-4 space-y-4">
                <li>
                  <a
                    href="/"
                    aria-current="page"
                    class="
                      text-base text-purple-200
                      hover:text-white
                      nuxt-link-exact-active nuxt-link-active
                    "
                  >
                    Inicio
                  </a>
                </li>
                <li>
                  <a
                    href="/blog"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Blog
                  </a>
                </li>
                <li>
                  <a
                    href="/uses"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Usos
                  </a>
                </li>
                <li>
                  <a
                    href="/about"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Sobre mí
                  </a>
                </li>
                <li>
                  <a
                    href="/links"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Links
                  </a>
                </li>
              </ul>
            </div>
            <div class="mt-12 md:mt-0">
              <h3
                class="
                  text-sm
                  font-semibold
                  text-purple-100
                  tracking-wider
                  uppercase
                "
              >
                Apóyame
              </h3>
              <ul class="mt-4 space-y-4">
                <li>
                  <a
                    href="https://www.buymeacoffee.com/baumannzone"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Buy me a coffee
                  </a>
                </li>
                <li>
                  <a
                    href="https://github.com/sponsors/baumannzone"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    GitHub Sponsors
                  </a>
                </li>
                <li>
                  <a
                    href="https://www.twitch.com/baumannzone/"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Twitch Prime
                  </a>
                </li>
              </ul>
            </div>
          </div>
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <h3
                class="
                  text-sm
                  font-semibold
                  text-purple-100
                  tracking-wider
                  uppercase
                "
              >
                Sígueme
              </h3>
              <ul class="mt-4 space-y-4">
                <li>
                  <a
                    href="https://twitter.com/baumannzone"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Twitter
                  </a>
                </li>
                <li>
                  <a
                    href="https://www.twitch.tv/baumannzone"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Twitch
                  </a>
                </li>
                <li>
                  <a
                    href="https://www.instagram.com/baumannzone/"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Instagram
                  </a>
                </li>
                <li>
                  <a
                    href="https://github.com/baumannzone"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    GitHub
                  </a>
                </li>
                <li>
                  <a
                    href="https://www.youtube.com/channel/UCTTj5ztXnGeDRPFVsBp7VMA"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    YouTube
                  </a>
                </li>
              </ul>
            </div>
            <div class="mt-12 md:mt-0">
              <h3
                class="
                  text-sm
                  font-semibold
                  text-purple-100
                  tracking-wider
                  uppercase
                "
              >
                Legal
              </h3>
              <ul class="mt-4 space-y-4">
                <li>
                  <a
                    href="/privacy"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Política de Privacidad
                  </a>
                </li>
                <li>
                  <a
                    href="/cookies"
                    class="text-base text-purple-200 hover:text-white"
                  >
                    Cookies
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="mt-12 border-t border-purple-600 pt-8">
        <p class="text-base text-gray-400 xl:text-center">
          © 2021 Baumannzone. Todos los derechos reservados.
        </p>
      </div>
    </div>
  </footer>-->
</template>

<script>
import { socialIcons, navItems } from '@/constants'
import SvgIcon from '@/components/SvgIcon'

const sectionItems = navItems.map((i) => ({
  name: i.text,
  to: i.to,
}))

const footerItems = [
  {
    title: 'Secciones',
    items: sectionItems,
  },
  {
    title: 'Apóyame',
    items: [
      {
        name: 'Buy me a coffee',
        to: 'https://www.buymeacoffee.com/baumannzone',
      },
      {
        name: 'GitHub Sponsors',
        to: 'https://github.com/sponsors/baumannzone',
      },
      {
        name: 'Twitch Prime',
        to: 'https://www.twitch.com/baumannzone/',
      },
    ],
  },
  // {
  //   title: 'Sígueme',
  //   items: [
  //     {
  //       name: 'Twitter',
  //       to: 'https://twitter.com/baumannzone',
  //     },
  //     {
  //       name: 'Twitch',
  //       to: 'https://www.twitch.tv/baumannzone',
  //     },
  //     {
  //       name: 'Instagram',
  //       to: 'https://www.instagram.com/baumannzone/',
  //     },
  //     {
  //       name: 'GitHub',
  //       to: 'https://github.com/baumannzone',
  //     },
  //     {
  //       name: 'YouTube',
  //       to: 'https://www.youtube.com/channel/UCTTj5ztXnGeDRPFVsBp7VMA',
  //     },
  //   ],
  // },
  // {
  //   title: 'Legal',
  //   items: [
  //     {
  //       name: 'Política de Privacidad',
  //       to: '/privacy',
  //     },
  //     {
  //       name: 'Cookies',
  //       to: '/cookies',
  //     },
  //   ],
  // },
]

export default {
  components: {
    SvgIcon,
  },
  data() {
    return {
      footerItems,
      socialIcons,
    }
  },
}
</script>
