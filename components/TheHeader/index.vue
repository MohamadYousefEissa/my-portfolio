<template>
  <header>
    <nav>
      <div class="backdrop" />
      <div
        class="container py-[1rem] md:py-[1.5rem] px-5 md:px-[2rem] lg:px-[10rem] mx-auto"
      >
        <div class="flex items-center">
          <div class="md:w-7/12 xl:w-9/12">
            <NuxtLink id="logo" to="/" class="leading-none">
              <p>MohamadYousefEissa</p>
              <p>Portfolio</p>
            </NuxtLink>
          </div>
          <div
            id="nav-menu"
            class="w-full flex justify-between invisible translate-x-[80%] md:translate-x-0 md:visible opacity-0 md:opacity-100"
          >
            <ul class="flex md:gap-6">
              <li><NuxtLink to="/">Home</NuxtLink></li>
              <li><NuxtLink to="/projects">Projects</NuxtLink></li>
              <li><NuxtLink to="/skills">Skills</NuxtLink></li>
            </ul>
            <div class="flex justify-center items-end md:items-center gap-5">
              <a
                href="https://www.linkedin.com/in/mohamad-yousef-eissa-381a6429a/"
                target="_blank"
              >
                <Icon name="bi:linkedin" />
              </a>
              <a href="https://github.com/MohamadYousefEissa" target="_blank">
                <Icon name="bi:github" />
              </a>
              <a href="https://wa.me/+963936552400" target="_blank">
                <Icon name="bi:whatsapp" />
              </a>
              <div>
                <UIThemeButton />
              </div>
            </div>
          </div>
          <div class="w-full flex md:hidden justify-end">
            <TheHeaderHamburger />
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<style scoped>
nav {
  background-color: hsl(from var(--main-bg) h s l / 0.1);
  li > .router-link-active {
    color: var(--sec-clr);
    font-weight: bold;
  }
  a {
    width: 18px;
    height: 18px;
    transition: color 0.15s;
  }
  li > a:not(.router-link-active):hover {
    color: hsl(from var(--sec-clr) h s l / 0.6);
  }
}
#logo {
  width: fit-content;
  font-weight: bold;
  display: block;

  p:first-of-type {
    font-size: 10px;
  }
}

li {
  font-size: 14px;
}
@media screen and (max-width: 767px) {
  #nav-menu {
    position: fixed;
    top: 80px;
    left: 0;
    width: 100%;
    height: calc(100vh - 80px);
    height: calc(100dvh - 80px);
    background: rgba(0, 0, 0, 0.374);
    background-color: hsl(from var(--main-bg) h s l / 0.1);
    z-index: 1;
    padding: 0 0 1rem 0;
    flex-direction: column;
    backdrop-filter: blur(10px);
    transition: all 0.5s ease-in-out;
  }
  #nav-menu ul {
    display: grid;
    place-items: center;
    height: 50%;

    a {
      display: grid;
      place-items: center;
      font-size: 16px;
      font-weight: bold;
      &:hover {
        color: var(--main-clr);
      }
    }
    a,
    li {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
