/* eslint-disable quotes */
<template>
  <div class="home">
    <b-navbar type="dark" variant="info" sticky>
      <b-navbar-brand href="/">Funny Fart</b-navbar-brand>
      <b-navbar-nav class="ml-auto">
        <b-nav-item v-if="this.$i18n.locale === 'de'" @click="switchLocale()"
          ><strong>DE</strong> | EN</b-nav-item
        >
        <b-nav-item v-if="this.$i18n.locale === 'en'" @click="switchLocale()"
          >DE | <strong>EN</strong></b-nav-item
        >
      </b-navbar-nav>
    </b-navbar>
    <div class="flex flex-col items-center w-screen">
      <div class="mx-10">
        <h1 class="my-4 text-3xl font-bold">{{ $t("title") }}</h1>
        <h3 class="text-xl font-bold mb-1">{{ $t("description.title") }}</h3>
        <p v-html="$t('description.text1')" />
        <p class="mb-4">{{ $t('description.text2') }}</p>
        <h3 class="text-xl mb-1 font-bold">{{ $t('personalInfos.title') }}</h3>
        <p class="mb-4">{{ $t('personalInfos.text') }}</p>
        <h3 class="text-xl mb-1 font-bold">{{ $t('permissions.title') }}</h3>
        <p>{{ $t('permissions.text') }}</p>
        <code>{{ $t('permissions.audio.code')}} </code>
        <p>{{ $t('permissions.audio.text') }}</p>
        <code>{{ $t('permissions.write.code')}} </code>
        <p>{{ $t('permissions.write.text') }}</p>
        <code>{{ $t('permissions.read.code')}} </code>
        <p class="mb-4">{{ $t('permissions.read.text') }}</p>
        <h3 class="text-xl mb-1 font-bold">{{ $t('contact.title') }}</h3>
        <p class="mb-4" v-html="$t('contact.text')"/>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  methods: {
    switchLocale: function () {
      this.$i18n.locale === 'de'
        ? (this.$i18n.locale = 'en')
        : (this.$i18n.locale = 'de')
    }
  }
}
</script>

<style scoped>

</style>
