<template>
  <div class="home">
    <Section color="blue-dark" title="Présentation" id="presentation" />
    <Section color="dark" title="Parcours" id="parcours" />
    <Section color="blue-dark" title="Compétences" id="competences" />
    <Section color="dark"  title="Projets" id="projets" />
    <Section color="blue-dark" title="Contact" id="contact" />
  </div>
</template>

<script>
import Section from '@/components/Section'

export default {
  name: 'Home',
  components: { Section },
}
</script>
