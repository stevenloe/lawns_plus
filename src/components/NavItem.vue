<template>
  <a
    :href="item.url"
    class="block py-2 px-2 md:py-1 text-white  font-semibold rounded hover:bg-green-800"
    >{{item.text}}</a
  >
</template>
<script>
export default {
  props: ['item']
}
</script>