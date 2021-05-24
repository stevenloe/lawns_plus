<template>
  <a
    :href="item.url"
    :name="item.text"
    class="block px-2 py-2 font-semibold text-white rounded md:py-1 hover:bg-green-800"
    >{{item.text}}</a
  >
</template>
<script>
export default {
  props: ['item']
}
</script>