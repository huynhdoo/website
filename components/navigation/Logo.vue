<template>
  <v-avatar
    class="mr-3 mb-3"
    tile
    :size="
      $vuetify.breakpoint.smAndDown
        ? 'calc(20vh - ' + $vuetify.application.top + 'px)'
        : $vuetify.breakpoint.mdAndDown
          ? 'calc(30vh - ' + $vuetify.application.top + 'px)'
          : 'calc(35vh - ' + $vuetify.application.top + 'px)'
    "
  >
    <v-img
      contain
      src="/logo.svg"
      lazy-loading="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAQAAABKfvVzAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QA/4ePzL8AAAAJcEhZcwAANX8AADV/AWBNYQcAAAAHdElNRQfkAxMOMxc5K7xoAAABq0lEQVQ4y5XUy05TURQG4G+fntP2AHIrQYxAMDGg8ZIw1gmJceBTOHDq0/g0TpwY48gYI1ETAzZSIBpLQShSWrqdVAhguKzhyvr3f1k7KzxtzReDi1X0fj+dLz6/4Di8KKYBF2cIkks8D9LTrbaamuiaaaXzATteWlTyUZ8FTwyfDeh6641d+5akckMey45NnPBQ986IRE3bTTWv/DibYcsXbQXjrmsbtGHD5FkMqZLvEjVF64KpUyZPAMbM6Qru+GZb2YiJsyUNeKSmIaobMOmB0fNiveuZ16oWzHjo3v/2EHRFBR2pA4lbptXl+hQkuoKAbk9/AnuWRVVNq7rqfvpl16ZPVqxaBJvq/0xHuT1N/ZYk2FY07sCGKS1NG1bQ0TlKKRi3bsy6IQ39Mh0HMh1RZlZd/fBH92Kt2LWtpOm3EV1rKjIfjMllZlXtHAekhn02p6qgKJhUkckdIOpzw9eepMNYr2qZsKuCXBFX3NdUVsao2/KjWNvWBGVVZQ0NiWBZLgr2NW3KBINHDEHUQu6PjkQq07ElKsrtiwq9TZBGUcGMi1QUhcuemb9RO4sbSkOhDAAAACV0RVh0ZGF0ZTpjcmVhdGUAMjAyMC0wMy0xOVQxNDo1MToyMyswMTowMP1FE98AAAAldEVYdGRhdGU6bW9kaWZ5ADIwMjAtMDMtMTlUMTQ6NTE6MjMrMDE6MDCMGKtjAAAAGXRFWHRTb2Z0d2FyZQB3d3cuaW5rc2NhcGUub3Jnm+48GgAAAABJRU5ErkJggg=="
    />
  </v-avatar>
</template>
