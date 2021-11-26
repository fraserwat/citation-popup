<template>
  <main>
    <h1>The Two Factors of a Commodity: Use-Value and Value</h1>
    <p>The wealth of those societies in which the capitalist mode of production prevails, presents itself as "an immense accumulation of commodities,"<sup class="citation">1<span></span></sup> its unit being a single commodity. Our investigation must therefore begin with the analysis of a commodity.</p>
    <p>A commodity is, in the first place, an object outside us, a thing that by its properties satisfies human wants of some sort or another. The nature of such wants, whether, for instance, they spring from the stomach or from fancy, makes no difference.<sup class="citation">2<span></span></sup> Neither are we here concerned to know how the object satisfies these wants, whether directly as means of subsistence, or indirectly as means of production.</p>
    <p>Every useful thing, as iron, paper, &c., may be looked at from the two points of view of quality and quantity. It is an assemblage of many properties, and may therefore be of use in various ways. To discover the various uses of things is the work of history.<sup class="citation">3<span></span></sup> So also is the establishment of socially-recognized standards of measure for the quantities of these useful objects. The diversity of these measures has its origin partly in the diverse nature of the objects to be measured, partly in convention.</p>
  </main>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      citationText: {
        "1": "Karl Marx, \"Zur Kritik der Politischen Oekonomie.\" Berlin, 1859, p. 3.",
        "2": "\"Desire implies want, it is the appetite of the mind, and as natural as hunger to the body... The greatest number (of things) have their value from supplying the wants of the mind.\" Nicholas Barbon: \"A Discourse Concerning Coining the New Money Lighter. In Answer to Mr. Locke’s Considerations, &c.\", London, 1696, pp. 2, 3.",
        "3": "\"Things have an intrinsick vertue\" (this is Barbon’s special term for value in use) \"which in all places have the same vertue; as the loadstone to attract iron\" (l.c., p. 6). The property which the magnet possesses of attracting iron, became of use only after by means of that property the polarity of the magnet had been discovered."
      }
    }
  },
  mounted() {
    [...document.querySelectorAll("sup.citation")].forEach(citation => {
      citation.childNodes[1].innerText = this.citationText[citation.innerText];
      citation.addEventListener('hover', c => {
        console.log(c.target)
        c.target.childNodes[1].style.left = "-10rem"
      })
    })
  }
}
</script>
