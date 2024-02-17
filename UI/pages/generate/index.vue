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
</script>

<template>
  <main class="grid grid-cols-5 gap-5">
    <!-- Header -->
    <section class="grid grid-cols-2 gap-10 col-span-3">
      <section class="input col-span-2 bg-slate-500 rounded-lg min-h-96">
        input
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
    <section class="grid place-content-center col-span-2">
      <div class="phone bg-slate-700 bg-opacity-10 p-1 rounded-3xl shadow">
        <!-- Video placeholder -->
        <video
          class="aspect-[9/16] max-w-sm rounded-3xl"
          src="http://localhost:8080/static/generated_videos/output-09a4a9be-b21d-4f72-92e6-243bfb1c4cb2.mp4"
          controls
        ></video>
      </div>
    </section>
    <section class="col-span-5">Footer</section>
  </main>
</template>
<style scoped></style>
