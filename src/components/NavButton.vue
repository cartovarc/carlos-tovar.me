<template>
  <q-btn
    stretch
    flat
    clickable
    type="a"
    target="_blank"
    :href="href">
    <span
      class="q-mr-xs">
      <slot></slot>
    </span>
    <q-icon
      name="link"
      color="grey-5"
      class="justify-"
      size="xs"/>
  </q-btn>
</template>

<script>
export default {
  props: ['href']
}
</script>

