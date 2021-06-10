<template>
  <div class="cliente" :class="{'cliente-pre': isPremium}">
      <div class="cliente-header" :class="{'cliente-header-pre': isPremium}">
          <h2>{{ cliente.nome }}</h2>
          <p>{{ cliente.desc }}</p>
      </div>
      <div class="cliente-body" :class="{'cliente-body-pre': isPremium}">
          <div class="dado">
            <span>Idade:</span>
            <p v-if="show">{{cliente.idade}}</p>
            <p v-else>Não informado.</p>
          </div>
          <div class="dado">
            <span>Endereço:</span>
            <p>{{cliente.end}}</p>
          </div>
          <div class="dado">
            <span>Telefone:</span>
            <p>{{cliente.cel}}</p>
          </div>
          <div class="dado">
            <span>E-mail:</span>
            <p>{{cliente.email}}</p>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    props:{
      cliente: Object,
      show: Boolean,
      isPremium: Boolean
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
  margin: 0;
  padding: 0;
  border: 0;
  box-sizing: border-box;
}

.cliente{
  font-family: sans-serif;
  background: rgb(71, 98, 150);
  border-radius: 6px;
  max-width: 350px;
  margin-bottom: 25px;
}

.cliente-header{
  border-bottom: 3px solid rgb(56, 77, 116);
  margin-bottom: 10px;
  padding: 10px;
}

.cliente-header > h2, p{
  margin-bottom: 10px;
}

.cliente-body{
    width: 100%;
    background: rgb(56, 77, 116);
    padding: 10px;
}

.cliente-body > .dado{
  display: flex;
}
.cliente-body > .dado > span{
  width: 30%;
}

/* Premium
*/

.cliente-pre{
  background: rgb(36, 36, 36);
  color: gold;
}

.cliente-header-pre{
  border-bottom: 3px solid rgb(17, 17, 17);
}

.cliente-body-pre{
  background-color: rgb(17, 17, 17);
}
</style>
