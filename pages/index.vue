<template>
    <div>
        <cabezote
         :productos="comprasrealizadas"
        ></cabezote>

        <manager
         :productos="productos"
         @compra="compra">
        </manager>
        <footer class="pie">
         <span>&copy; 2024 Audífonos TechSound. Todos los derechos reservados.</span>
<br>
<span>Encuentra la mejor calidad de sonido en cada uno de nuestros productos. Audífonos para cada estilo de vida: deportivos, profesionales, inalámbricos, y más.</span>
<br>
<span>Contacto: contacto@techsound.com | Tel: +1 800 123 4567</span>
<br>
<span>Síguenos en redes sociales: Facebook, Instagram, Twitter</span>
 </footer>
    </div>
</template>
<script>
import cabezote from '~/components/cabezote.vue'
export default {
  components: { cabezote },
    data() {
        return {
         
          comprasrealizadas : [],
          productos : [
            {
                imagen : 'https://down-co.img.susercontent.com/file/cn-11134207-7qukw-lhzmwe7hi6xq53@resize_w450_nl.webp',
                precio :  74.750,
                titulo : 'Auriculares Estéreo',
                descripcion : 'SPRISE Auriculares Estéreo Con Micrófono Giratorio De 3,5 Mm Y Conector USB Multidispositivo Con Diadema/Ajustable'
            },
             {
                imagen : 'https://down-co.img.susercontent.com/file/sg-11134201-7rd45-lwzckfqp56e79c@resize_w450_nl.webp',
                precio : 125.760,
                titulo : 'Diadema Auriculares Bluetooth ',
                descripcion : 'Larga Duración Sin Fugas De Sonido Inalámbricos Deportivos Plegables',

             } ,
             {
                imagen : 'https://down-co.img.susercontent.com/file/cn-11134207-7r98o-lvo5hk1jp6cn50@resize_w450_nl.webp',
                precio : 8.640,
                titulo : 'Audifonos inalambricoss E7S',
                descripcion : 'Bluetooth V5.0 Auriculares Inalámbricos 9D HIFI Sound Audifonos diadema Deportivos Con Caja',

             } ,
             {
                imagen : 'https://down-co.img.susercontent.com/file/sg-11134201-7rbm1-lphh6d4vhqnrce@resize_w450_nl.webp',
                precio : 87.134,
                titulo : 'Fone Auriculares Bluetooth ',
                descripcion : 'Deportes Dormir Diadema Inalámbricos Elásticos Música Máscara De Ojos',

             } ,
             {
                imagen : 'https://down-co.img.susercontent.com/file/sg-11134201-7rces-lsl5dqx1irov91@resize_w450_nl.webp',
                precio : 41.002,
                titulo : 'BA-Diadema Para Dormir',
                descripcion : 'Auriculares Incorporados Micrófono Inalámbrico Música Lavables Para Niños',

             } ,
             {
                imagen : 'https://down-co.img.susercontent.com/file/sg-11134201-7rd41-lw2pec95qgqcdd@resize_w450_nl.webp',
                precio : 18.464,
                titulo : 'IBN] Universal De Color Sólido',
                descripcion : 'Trenzada Diadema Cojín Protector',

             } ,

          ]
            

                               
           
        }
    },
    methods: {
      compra(data){
         this.comprasrealizadas.push(data)
      }
    },
}
</script>
<style>
.pie {
   background-color: #333; 
  color: #fff;
  padding: 40px 0;
  text-align: center; 
}
.pie span {
   font-size: 14px; /* Tamaño de fuente */
   opacity: 0.8; /* Opacidad para hacer el texto menos brillante */
}
</style>