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
      <section class="setting bg-slate-800 rounded-lg min-h-40 p-5">
        <header class="flex items-center">
          <Icon name="material-symbols:settings" size="24" />
          <span class="text-lg ml-2">Settings</span>
          <div class="ml-auto">
            <n-button ghost text>
              <template #icon>
                <Icon name="pepicons:dots-x" />
              </template>
            </n-button>
          </div>
        </header>
        <article class="mt-5 opacity-60 flex flex-col">
          <span class="font-bold"> Search:</span>
          <span class="text-sm mt-2 truncate"> Nice video,Mountain</span>
        </article>
      </section>
      <section class="voice bg-slate-800 rounded-lg min-h-40 p-5">
        <header class="flex items-center">
          <Icon name="icon-park-outline:voice" size="24" />
          <span class="text-lg ml-2">Voice</span>
          <div class="ml-auto">
            <n-button ghost text>
              <template #icon>
                <Icon name="pepicons:dots-x" />
              </template>
            </n-button>
          </div>
        </header>
        <article
          class="mt-8 opacity-80 text-center flex items-center justify-center"
        >
          <Icon name="material-symbols:person" size="36" />
          <span class="ml-2 font-black text-lg"> US-Male</span>
        </article>
      </section>
      <section class="music bg-slate-800 rounded-lg min-h-40 p-5">
        <header class="flex items-center">
          <Icon name="icon-park-outline:music" size="24" />
          <span class="text-lg ml-2">Music</span>
          <div class="ml-auto">
            <n-button ghost text>
              <template #icon>
                <Icon name="pepicons:dots-x" />
              </template>
            </n-button>
          </div>
        </header>
        <article class="mt-8 opacity-80 flex items-center">
          <section class="w-10 h-10 bg-slate-950 rounded-md"></section>
          <section class="ml-2 flex flex-col text-sm">
            <span>The blue sky...</span>
            <span class="opacity-60">Sombreros Musical</span>
          </section>
        </article>
      </section>
      <section class="subtitle bg-slate-800 rounded-lg min-h-40 p-5">
        <header class="flex items-center">
          <Icon name="material-symbols:subtitles" size="26" />
          <span class="text-lg ml-2">Subtitle</span>
          <div class="ml-auto">
            <n-button ghost text>
              <template #icon>
                <Icon name="ph:dots-nine-thin" />
              </template>
            </n-button>
          </div>
        </header>
        <article
          class="mt-8 opacity-80 text-center flex items-center justify-center"
        >
          <span>Subtitle here</span>
        </article>
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
