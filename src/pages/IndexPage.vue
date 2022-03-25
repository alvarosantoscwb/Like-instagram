<template>
  <q-page class="flex flex-center bg-grey-2">
    <div class="bg-white q-pa-sm shadow-2">
      <q-item v-for="id in posts" v-bind:key="id" class="user1 bg-white shadow-2" style="border-radius: 3px">
        <q-item-label style="text-transform: initial" caption></q-item-label>
        <q-item-section avatar>
          <q-avatar>
            <img :src="id.img" />
          </q-avatar>
        </q-item-section>
        <q-item-section>
          <q-item-label>{{id.username}}</q-item-label>
        </q-item-section>
        <q-btn round unelevated icon="mdi-dots-vertical" />
        <img name="q-mb-lg" :src="id.img" />
      </q-item>
      <q-item class="q-pa-xs bg-white shadow-2" style="border-radius: 3px">
        <q-btn round unelevated icon="mdi-heart" />
        <q-btn round unelevated icon="mdi-message-outline" />
        <q-btn round unelevated icon="mdi-arrow-" />
      </q-item>
      </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  data() {
    return {
      posts: [
        {
          id: 1938120391,
          img: "https://placeimg.com/500/500/animals",
          username: "Melvin Morrison",
          userImg: "https://randomuser.me/api/portraits/men/24.jpg",
        },
        {
          id: 12312312323,
          img: "https://placeimg.com/500/500/arch",
          username: "Jacqueline Woods",
          userImg: "https://randomuser.me/api/portraits/women/86.jpg",
        },
        {
          id: 123123123,
          img: "https://placeimg.com/500/500/nature",
          username: "Claire Day",
          userImg: "https://randomuser.me/api/portraits/women/1.jpg",
        },
        {
          id: 31323243241,
          img: "https://placeimg.com/500/500/people",
          username: "Lawrence Wade",
          userImg: "https://randomuser.me/api/portraits/men/19.jpg",
        },
        {
          id: 4134562434,
          img: "https://placeimg.com/500/500/tech",
          username: "Aiden Cook",
          userImg: "https://randomuser.me/api/portraits/men/96.jpg",
        },
      ],
    };
  },
});
</script>
