<template>
  <div class="h-screen flex flex-col">
    <div :class="defaultTransition">
      <div class="p-2 my-2">
        <nuxt-link to="/">
          <div class="w-8 h-8">
            <LogoTwitter />
          </div>
        </nuxt-link>
      </div>

      <div class="mt-2 space-y-3">

        <SidebarLeftTab>
          <template v-slot:icon>
            <div>
              <HomeIcon />
            </div>
          </template>
          <template v-slot:name>
            <div>Home</div>
          </template>
        </SidebarLeftTab>

        <SidebarLeftTab>
          <template v-slot:icon>
            <div>
              <HashtagIcon />
            </div>
          </template>
          <template v-slot:name>
            <div>Explore</div>
          </template>
        </SidebarLeftTab>

        <SidebarLeftTab>
          <template v-slot:icon>
            <div>
              <BellIcon />
            </div>
          </template>
          <template v-slot:name>
            <div>Notifications</div>
          </template>
        </SidebarLeftTab>

        <SidebarLeftTab>
          <template v-slot:icon>
            <div>
              <InboxIcon />
            </div>
          </template>
          <template v-slot:name>
            <div>Inbox</div>
          </template>
        </SidebarLeftTab>

        <SidebarLeftTab>
          <template v-slot:icon>
            <div>
              <BookmarkIcon />
            </div>
          </template>
          <template v-slot:name>
            <div>Bookmarks</div>
          </template>
        </SidebarLeftTab>

        <SidebarLeftTab>
          <template v-slot:icon>
            <div>
              <DocumentTextIcon />
            </div>
          </template>
          <template v-slot:name>
            <div>Lists</div>
          </template>
        </SidebarLeftTab>

        <SidebarLeftTab>
          <template v-slot:icon>
            <div>
              <UserIcon />
            </div>
          </template>
          <template v-slot:name>
            <div>Profile</div>
          </template>
        </SidebarLeftTab>

        <SidebarLeftTab>
          <template v-slot:icon>
            <div>
              <DotsCircleHorizontalIcon />
            </div>
          </template>
          <template v-slot:name>
            <div>More</div>
          </template>
        </SidebarLeftTab>


      </div>

    </div>
  </div>
</template>

<script setup>
import { HomeIcon, HashtagIcon, BellIcon, InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon, DotsCircleHorizontalIcon } from "@heroicons/vue/solid";
const { defaultTransition } = useTailwindConfig();
</script>

<style lang="scss" scoped>
</style>