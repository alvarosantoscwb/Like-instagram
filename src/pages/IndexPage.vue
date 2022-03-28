<template>
  <q-page class="flex flex-center bg-grey-2">
    <div class="q-ma-xs">
      <q-card
        v-for="post in posts"
        :key="post.id"
        class="user1 q-mb-md bg-white shadow-2"
        style="border-radius: 5px"
      >
        <q-item class="bg-white shadow-2" style="border-radius: 5px">
          <q-item-label style="text-transform: initial" caption></q-item-label>
          <q-item-section avatar>
            <q-avatar>
              <img :src="post.userImg" />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label style="font-weight: 500">{{
              post.username
            }}</q-item-label>
          </q-item-section>
          <q-btn round unelevated icon="las la-ellipsis-v" />
        </q-item>
        <img style="height: 425px; width: 425px" :src="post.img" />
        <div class="q-pa-md">
          <q-btn round unelevated icon="las la-heart" />
          <q-btn round unelevated icon="las la-comment-alt" />
          <q-btn round unelevated icon="las la-share" />
        </div>
      </q-card>
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
