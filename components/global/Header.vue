<template>
  <header>
    <nav class="bg-white shadow dark:bg-gray-800">
      <div class="container px-6 py-4 mx-auto">
        <div class="lg:flex lg:items-center lg:justify-between">
          <div class="flex items-center justify-between">
            <div class="text-xl font-semibold text-gray-700">
              <a
                class="
                  text-2xl
                  font-bold
                  text-gray-800
                  dark:text-white
                  lg:text-3xl
                  hover:text-gray-700
                  dark:hover:text-gray-300
                "
                href="#"
                >Brand</a
              >
            </div>

            <!-- Mobile menu button -->
            <div class="flex lg:hidden">
              <button
                type="button"
                class="
                  text-gray-500
                  dark:text-gray-200
                  hover:text-gray-600
                  dark:hover:text-gray-400
                  focus:outline-none focus:text-gray-600
                  dark:focus:text-gray-400
                "
                aria-label="toggle menu"
              >
                <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                  <path
                    fill-rule="evenodd"
                    d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
                  ></path>
                </svg>
              </button>
            </div>
          </div>

          <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
          <div class="hidden -mx-4 lg:flex lg:items-center">
            <a
              href="#"
              class="
                block
                mx-4
                mt-2
                text-sm text-gray-700
                capitalize
                lg:mt-0
                dark:text-gray-200
                hover:text-blue-600
                dark:hover:text-indigo-400
              "
              >Web developers</a
            >
            <a
              href="#"
              class="
                block
                mx-4
                mt-2
                text-sm text-gray-700
                capitalize
                lg:mt-0
                dark:text-gray-200
                hover:text-blue-600
                dark:hover:text-indigo-400
              "
              >Web Designers</a
            >
            <a
              href="#"
              class="
                block
                mx-4
                mt-2
                text-sm text-gray-700
                capitalize
                lg:mt-0
                dark:text-gray-200
                hover:text-blue-600
                dark:hover:text-indigo-400
              "
              >UI/UX Designers</a
            >
            <a
              href="#"
              class="
                block
                mx-4
                mt-2
                text-sm text-gray-700
                capitalize
                lg:mt-0
                dark:text-gray-200
                hover:text-blue-600
                dark:hover:text-indigo-400
              "
              >Contact</a
            >
          </div>
        </div>
      </div>
    </nav>

    <div
      class="w-full bg-center bg-cover h-96"
      style="
        background-image: url(https://images.unsplash.com/photo-1504384308090-c894fdcc538d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80);
      "
    >
      <div class="flex items-center justify-center w-full h-full bg-gray-900 bg-opacity-50">
        <div class="text-center">
          <h1 class="text-2xl font-semibold text-white uppercase lg:text-3xl">
            Build Your new <span class="text-blue-400 underline">Saas</span>
          </h1>
          <button
            class="
              w-full
              px-4
              py-2
              mt-4
              text-sm
              font-medium
              text-white
              uppercase
              transition-colors
              duration-200
              transform
              bg-blue-600
              rounded-md
              lg:w-auto
              hover:bg-blue-500
              focus:outline-none focus:bg-blue-500
            "
          >
            Start project
          </button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="postcss" scoped>
.scrim-bg {
  &::before {
    content: '';
    z-index: -1;
    background-color: var(--bg);
    @apply absolute bottom-0 inset-x-0 h-12 mb-4 transition-colors duration-200 ease-in-out;
  }
  &::after {
    content: '';
    z-index: -1;
    opacity: 1;
    animation: fadeIn1 500ms ease-in-out;
    @apply pointer-events-none absolute bottom-0 inset-x-0 h-16 -mb-12;
    background: linear-gradient(to bottom, #111827, cubic-bezier(0.15, 0, 0.45, 1), transparent);
  }
}
.nuxt-link-exact-active {
  @apply text-gray-200 border-gray-400 bg-gray-800 bg-opacity-25 cursor-default;
}

.light {
  & .scrim-bg {
    &::after {
      animation-name: fadeIn2;
      background: linear-gradient(to bottom, #e5e7eb, cubic-bezier(0.15, 0, 0.45, 1), transparent);
    }
  }
  & .nuxt-link-exact-active {
    @apply text-primary-700 border-gray-600 bg-gray-100;
  }
}

/* Need two because of smoother switching between color modes */
@keyframes fadeIn1 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeIn2 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
