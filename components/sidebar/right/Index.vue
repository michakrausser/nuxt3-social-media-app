<template>
  <div class="flex flex-col">
    <sidebar-right-preview-card title="What's happening">
      <sidebar-right-item
          v-for="whatsHappeningItem in whatsHappeningItems"
          :key="whatsHappeningItem.title"
      >
        <div>
          <h2 class="font-bold text-gray-800 text-md dark:text-white">
            {{ whatsHappeningItem.title }}
          </h2>

          <p class="text-xs text-gray-400">
            {{ whatsHappeningItem.count }}
          </p>
        </div>
      </sidebar-right-item>
    </sidebar-right-preview-card>

    <sidebar-right-preview-card title="Who to follow">
      <sidebar-right-item
          v-for="whoToFollowItem in whoToFollowItems"
          :key="whoToFollowItem.name"
      >
        <div class="flex justify-between items-center p-2">
          <div class="flex">
            <img
                :src="whoToFollowItem.image"
                :alt="whoToFollowItem.name"
                class="w-10 h-10 rounded-full"
            >

            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">
                {{ whoToFollowItem.name }}
              </h1>
              <p class="text-xs text-gray-400">
                {{ whoToFollowItem.handle }}
              </p>
            </div>
          </div>

          <div class="flex h-full">
            <button
                class="px-4 py-2 font-bold bg-black text-white dark:text-black dark:bg-white rounded-full"
            >
              Follow
            </button>
          </div>
        </div>
      </sidebar-right-item>
    </sidebar-right-preview-card>


  </div>
</template>

<script lang="ts" setup>
  import { reactive, toRefs } from 'vue';


  const items = reactive({
    whatsHappeningItems: [
      {
        title: 'SpaceX',
        count: '18.8k Tweets'
      },
      {
        title: '#CodingIsFun',
        count: '18.8k Tweets'
      },
      {
        title: '#artforall',
        count: '18.8k Tweets'
      }
    ],
    whoToFollowItems: [
      {
        name: 'Joe Biden',
        handle: '@JoeBiden',
        image: 'https://picsum.photos/200/300'
      },
      {
        name: 'Joe Biden',
        handle: '@JoeBiden',
        image: 'https://picsum.photos/200/300'
      },
      {
        name: 'Joe Biden',
        handle: '@JoeBiden',
        image: 'https://picsum.photos/200/300'
      },
    ]
  })

  const { whatsHappeningItems, whoToFollowItems } = toRefs( items )
</script>

<style scoped>

</style>
