<script lang="ts" setup>
/**
 *
 * Generate view
 *
 * @author Reflect-Media <reflect.media GmbH>
 * @version 0.0.1
 *
 * @todo [ ] Test the component
 * @todo [ ] Integration test.
 * @todo [✔] Update the typescript.
 */

const video = ref({
  script: "",
  search: "",
  voice: "en_us_001",
});
</script>

<template>
  <main class="grid grid-cols-5 gap-5 pr-10">
    <!-- Header -->
    <section class="grid grid-cols-2 gap-10 col-span-3">
      <section class="input col-span-2 rounded-lg min-h-96">
        <n-form-item :show-label="false" path="script">
          <n-input
            v-model:value="video.script"
            placeholder="Video script"
            type="textarea"
            show-count
            clearable
            :autosize="{
              minRows: 18,
              maxRows: 25,
            }"
            class="p-5 h-full bg-slate-800 rounded-xl border-none"
          />
        </n-form-item>
      </section>
      <section class="setting bg-slate-800 rounded-lg min-h-40">
        settings
      </section>
      <section class="voice bg-slate-800 rounded-lg min-h-40">voice</section>
      <section class="music bg-slate-800 rounded-lg min-h-40">music</section>
      <section class="subtitle bg-slate-800 rounded-lg min-h-40">
        subtitle
      </section>
    </section>
    <section class="col-span-2">
      <header class="col-span-5 flex justify-end">
        <n-button type="success" size="large">Generate</n-button>
      </header>
      <section class="grid place-content-center">
        <div class="phone bg-slate-700 bg-opacity-10 p-1 rounded-3xl shadow">
          <!-- Video placeholder -->
          <video
            class="aspect-[9/16] max-w-sm rounded-3xl"
            src="http://localhost:8080/static/generated_videos/output-09a4a9be-b21d-4f72-92e6-243bfb1c4cb2.mp4"
            controls
          ></video>
        </div>
      </section>
    </section>
    <section class="col-span-5">Footer</section>
  </main>
</template>
<style scoped></style>
