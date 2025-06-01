<template>
  <section class="informacoes">
          <div>
            <FontAwesomeIcon icon="truck" />
            <p>
              Frete grátis para SC
            </p>
          </div>
          <div style="border-left: #2e649e solid 2px; border-right: #2e649e solid 2px; margin: 0 6vw">
            <FontAwesomeIcon icon="star" style="margin-left: 5.5vw;" />
            <p style="margin-right: 5.5vw; ">
              Livros recomendados
            </p>
          </div>
          <div>
            <FontAwesomeIcon icon="book-open" />
            <p>
              Mais vendidos
            </p>
          </div>
        </section>
</template>

<style scoped>

section.informacoes {
  display: flex;
  border-bottom: #4a88cb solid 2px;
  border-top: #4a88cb solid 2px;
  padding: 4vw 0;
  justify-content: center;
}

section.informacoes div {
  display: flex;
  font-size: 1.2rem;
  padding: 2vw;
  align-items: center;
}

section.informacoes div p {
  font-weight: 600;
  margin-left: 0.6vw;
}

</style>