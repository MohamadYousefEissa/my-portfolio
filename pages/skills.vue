<script setup lang="ts">
import skills from "~/store/skills";
</script>
<template>
  <div class="container mx-auto px-5 md:px-[2rem] mt-10">
    <h1 class="text-[40px] md:text-[60px] text-center mb-[6rem] font-bold">
      My Skills
    </h1>
    <div
      class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 place-items-center gap-[4rem] md:gap-[5rem]"
    >
      <Skill
        v-for="skill in skills"
        :key="skill.label"
        :label="skill.label"
        :icon="skill.icon"
        :percent-value="skill.percentValue"
      />
    </div>
  </div>
</template>
