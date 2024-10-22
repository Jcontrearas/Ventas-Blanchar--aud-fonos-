<template>
  <v-dialog
    v-model="mostrar"
    width="auto"
    persistent
  >
    <v-card
      class="custom-card"
    >
      <v-card-title class="card-title">
        <span>Productos Comprados</span>
      </v-card-title>

      <v-card-text>
        <div v-for="(data, index) in compras" :key="index" class="product-item">
          <h3>{{ data.titulo }}</h3>
          <p>Precio: ${{ data.precio.toFixed(2) }}</p>
        </div>
      </v-card-text>

      <template v-slot:actions>
        <v-btn
          class="ms-auto"
          color="primary"
          @click="cerrar()"
        >
          Cerrar
        </v-btn>
      </template>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  props: {
    show: {
      type: Boolean,
      default: false
    },
    compras: {
      type: Array,
    },
  },
  data() {
    return {
      mostrar: false      
    }
  },
  methods: {
    cerrar() {
      this.$emit('cerrar')
    }
  },
  watch: {
    show() {
      this.mostrar = this.show
    }
  }   
}
</script>

<style scoped>
.custom-card {
  background: #f5f5f5; /* Color de fondo claro */
  border-radius: 10px; /* Bordes redondeados */
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1); /* Sombra sutil */
  transition: transform 0.2s; /* Efecto de transición */
}

.custom-card:hover {
  transform: scale(1.02); /* Aumenta el tamaño ligeramente al pasar el ratón */
}

.card-title {
  background: linear-gradient(90deg, rgba(255, 105, 180, 1), rgba(255, 0, 150, 1)); /* Degradado en el título */
  color: white; /* Texto blanco */
  padding: 10px; /* Espaciado */
  text-align: center;
}

.product-item {
  border-bottom: 1px solid #e0e0e0; /* Línea separadora */
  padding: 10px 0; /* Espaciado vertical */
}

.product-item:last-child {
  border-bottom: none; /* Eliminar la línea en el último elemento */
}
</style>
