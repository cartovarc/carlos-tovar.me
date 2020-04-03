<template>
  <q-btn
    type="a"
    target="_blank"
    :href="href"
    :icon="icon"
    flat>
    <span class="q-ml-xs">
      <slot></slot>
    </span>
  </q-btn>
</template>

<script>
export default {
  props: ['href', 'icon']
}
</script>

