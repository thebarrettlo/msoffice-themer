<template>
   <div class="picker-module">
      <span class="picker-module-identifier field-title">{{ purpose }}</span>
      <Verte
         :value="color"
         picker="square" model="hex" menu-position="bottom" :enable-alpha="false" class=""
         @input="$emit('updateColor', $event)" />
      <span class="swatch-text">
         {{ color }}
      </span>
   </div>
</template>

<script>
export default {
   name: 'ColorPickerModule',
   props: {
      purpose: {
         type: String,
         default: 'Color picker'
      },
      color: {
         type: String,
         default: '#000000'
      }
   },
   emits: [
      'updateColor'
   ],
}
</script>
