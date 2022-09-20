<template>
  <div class="h-screen flex flex-col">
    <div
        class="p-2 my-2 rounded-full hover:bg-blue-50 w-min dark:bg-white/20"
        :class="defaultTransition"
    >
      <nuxt-link to="/">
        <div class="w-8 h-8">
          <logo-twitter/>
        </div>
      </nuxt-link>
    </div>

    <div class="mt-2 space-y-3">
      <sidebar-left-tab active>
        <template v-slot:icon>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
            <path d="M11.47 3.84a.75.75 0 011.06 0l8.69 8.69a.75.75 0 101.06-1.06l-8.689-8.69a2.25 2.25 0 00-3.182 0l-8.69 8.69a.75.75 0 001.061 1.06l8.69-8.69z" />
            <path d="M12 5.432l8.159 8.159c.03.03.06.058.091.086v6.198c0 1.035-.84 1.875-1.875 1.875H15a.75.75 0 01-.75-.75v-4.5a.75.75 0 00-.75-.75h-3a.75.75 0 00-.75.75V21a.75.75 0 01-.75.75H5.625a1.875 1.875 0 01-1.875-1.875v-6.198a2.29 2.29 0 00.091-.086L12 5.43z" />
          </svg>
        </template>

        <template v-slot:name>
          Home
        </template>
      </sidebar-left-tab>

      <sidebar-left-tab>
        <template v-slot:icon>
          <icon-hashtag />
        </template>

        <template v-slot:name>
          Explore
        </template>
      </sidebar-left-tab>

      <sidebar-left-tab>
        <template v-slot:icon>
          <icon-bell />
        </template>

        <template v-slot:name>
          Notifications
        </template>
      </sidebar-left-tab>

      <sidebar-left-tab>
        <template v-slot:icon>
          <icon-inbox />
        </template>

        <template v-slot:name>
          Messages
        </template>
      </sidebar-left-tab>

      <sidebar-left-tab>
        <template v-slot:icon>
          <icon-bookmark />
        </template>

        <template v-slot:name>
          Bookmarks
        </template>
      </sidebar-left-tab>

      <sidebar-left-tab>
        <template v-slot:icon>
          <icon-document-text />
        </template>

        <template v-slot:name>
          Lists
        </template>
      </sidebar-left-tab>

      <sidebar-left-tab>
        <template v-slot:icon>
          <icon-user />
        </template>

        <template v-slot:name>
          Profile
        </template>
      </sidebar-left-tab>

      <sidebar-left-tab>
        <template v-slot:icon>
          <icon-ellipsis-horizontal-circle />
        </template>

        <template v-slot:name>
          More
        </template>
      </sidebar-left-tab>
    </div>

  </div>
</template>

<script lang="ts" setup>

  const { defaultTransition } = useTailwindConfig()

</script>

<style scoped>

</style>
