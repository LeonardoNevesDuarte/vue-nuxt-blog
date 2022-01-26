<template>
  <div class="w-1/2 mx-auto my-20">
      <h1 class="text-3xl font-semibold text-red-600">{{tituloBlog}}</h1>
      <article v-for="artigo in listaArtigos" class="my-20">
          <h2 class="text-5xl font-semibold mb-5">{{artigo.titulo}}</h2>
          <p class="mb-5">{{artigo.resumo}}</p>
          <p class="text-red-500">Ler mais</p>
      </article>
  </div>
</template>

<script>
export default {
    data () {
        return {
            listaArtigos: [],
            tituloBlog: "Blog com Nuxt e Vue"
        }
    },
    created() {
        this.carregarListaArtigos();
    },
    methods: {
        carregarListaArtigos() {
            for(var i = 0; i < 5; i++) {
                var auxArtigo = {
                    titulo: "Artigo " + i,
                    resumo: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras in nunc nisl. Praesent nec augue mattis, aliquam eros eget, vestibulum felis. Maecenas consectetur aliquet sapien at gravida. Praesent vitae tellus ut risus rhoncus laoreet sit amet sed mauris. Mauris aliquet libero varius libero lacinia maximus. Donec mattis semper est vel malesuada. Nunc et nisl nec ante efficitur condimentum. Sed nunc diam, rutrum eget vehicula ut, molestie nec libero. Donec id erat commodo, lobortis lorem et, ultricies est"
                }
                this.listaArtigos.push(auxArtigo);
                auxArtigo = null;
            }
        }
    }
}
</script>
