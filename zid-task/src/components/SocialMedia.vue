<template>
  <div>
    <v-img
      class="justify-center ml-10"
      src="@/assets/zid-logo.png"
      max-height="50"
      max-width="200"
    />
    <v-icon
      v-for="(item, i) in items.slice(0, large ? items.length : 3)"
      :key="i"
      large
      class="ma-5"
      color="white"
      v-text="item.icon"
    />
    <v-icon
      style="position: absolute; bottom: 20px; right: 40px"
      v-text="iconforsupport"
    />
  </div>
</template>

<script>
  export default {
    props: {
      large: {
        type: Boolean,
        default: false,
      },
    },

    data () {
      return {
        items: [
          {
            name: 'Youtube',
            icon: 'mdi-youtube',
          },
          {
            name: 'Linkeding',
            icon: 'mdi-linkedin',
          },
          {
            name: 'Instagram',
            icon: 'mdi-instagram',
          },
          {
            name: 'Twitter',
            icon: 'mdi-twitter',
          },
        ],
        iconforsupport: 'mdi-chat',
      }
    },
  }
</script>
