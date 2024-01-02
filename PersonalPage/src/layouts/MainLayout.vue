<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Personal Page
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
        For more information
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'CV',
    icon: 'school',
    link: '/#/CV'
  },
  {
    title: 'Linkedin',
    icon: 'chat',
    link: 'https://www.linkedin.com/in/alafsantos'
  },
  {
    title: 'Github',
    icon: 'code',
    link: 'https://github.com/alafSantos'
  },
  {
    title: 'ORCID',
    icon: 'record_voice_over',
    link: 'https://orcid.org/0000-0002-5469-3872'
  },
  {
    title: 'Lattes Curriculum',
    icon: 'info',
    link: 'http://lattes.cnpq.br/4461462146153067'
  }
]

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
