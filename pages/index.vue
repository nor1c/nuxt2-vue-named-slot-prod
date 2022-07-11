<template>
  <Layout>
    <client-only>
      <template #layout-namedslot>
        <p>named slot from Layout.vue</p> <!-- named slot not working in layouts -->
      </template>
    </client-only>

    <TestSlot>
      <template #testslot-namedslot>
        named slot from TestSlot component <!-- work perfectly-->
      </template>
    </TestSlot>
  </Layout>
</template>

<script>
import Layout from '~/components/layouts/Layout.vue'
import TestSlot from '~/components/TestSlot.vue'

export default {
  name: 'IndexPage',
  components: {
    Layout,
    TestSlot
  }
}
</script>
