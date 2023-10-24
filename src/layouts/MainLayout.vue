<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="q-pa-lg bg-white">
      <q-toolbar
        class="q-py-sm"
        style="background-color: #f7f8f8; color: #050f27; border-radius: 20px"
      >
        <div class="row full-width">
          <div class="self-center">
            <q-toolbar-title>
              <q-avatar class="q-mx-sm">
                <img src="../assets/HutlyLogo.svg" />
              </q-avatar>
              <strong>Hutly®</strong></q-toolbar-title
            >
          </div>
          <q-space />
          <div v-if="$q.screen.gt.sm" class="self-center">
            <q-tabs no-caps v-model="tab" style="color=#050f27">
              <q-tab name="home" label="Home" />
              <q-tab name="project" label="Project" />
              <q-tab name="aboutus" label="Abous Us" />
              <q-tab name="faqs" label="FAQs" />
            </q-tabs>
          </div>
          <q-space />
          <div class="text-right self-center">
            <q-btn
              no-caps
              flat
              text-color="white"
              class="bg-primary"
              style="border-radius: 20px"
              label="Contact Us"
            />
          </div>
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",
});
</script>
