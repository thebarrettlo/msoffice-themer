<template>
   <main class="">
      <information-section />
      <hr class="info-hl">
      <div class="style-preview">
         <excel-style-preview :colors="colors" />
      </div>
      <section class="file-options">
         <form>
            <span class="color-group-name field-title">Color group name</span>
            <input v-model="colorGroupName" class="color-group-input" placeholder="e.g. My Color Group">
            <button class="color-group-button" type="button" @click="generateColorGroup">Get file</button>
            <span class="color-group-filename">{{ colorGroupName }}.xml</span>
         </form>
      </section>
      <section class="picker-section">
         <color-picker-module
            v-for="picker in colors"
            :key="picker.id"
            :purpose="picker.purpose"
            :color="picker.color"
            @updateColor="picker.color = $event"
         />
      </section>
   </main>
</template>

<script>
import ColorPickerModule from '~/components/ColorPickerModule.vue';
import ExcelStylePreview from '~/components/ExcelStylePreview.vue'
import InformationSection from '~/components/InformationSection.vue';
export default {
   name: 'IndexPage',
   components: { InformationSection, ExcelStylePreview, ColorPickerModule },
   data: () => ({
      colors: [
         {
            id: 0,
            purpose: "Background 1",
            color: "#ffffff"
         },
         {
            id: 1,
            purpose: "Text 1",
            color: "#000000"
         },
         {
            id: 2,
            purpose: "Background 2",
            color: "#e7e6e6"
         },
         {
            id: 3,
            purpose: "Text 2",
            color: "#44546a"
         },
         {
            id: 4,
            purpose: "Accent 1",
            color: "#4472c4"
         },
         {
            id: 5,
            purpose: "Accent 2",
            color: "#ed7d31"
         },
         {
            id: 6,
            purpose: "Accent 3",
            color: "#a5a5a5"
         },
         {
            id: 7,
            purpose: "Accent 4",
            color: "#ffc000"
         },
         {
            id: 8,
            purpose: "Accent 5",
            color: "#5b9bd5"
         },
         {
            id: 9,
            purpose: "Accent 6",
            color: "#70ad47"
         },
         {
            id: 10,
            purpose: "Hyperlink",
            color: "#0563c1"
         },
         {
            id: 11,
            purpose: "Followed Hyperlink",
            color: "#954f72"
         },
      ],
      colorGroupName: '',
   }),
   methods: {
      generateColorGroup() {
         const colors = new Array(12);

         for (let i = 0; i < 12; i++) {
            colors[i] = this.colors[i].color.substring(1);
         }

         const link = document.createElement('a');
         const colorGroupFile = new Blob([
            `<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <a:clrScheme xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" name="${this.colorGroupName}">
               <!-- Text 1 -->
               <a:dk1>
                  <a:sysClr val="windowText" lastClr="${colors[1]}"/>
               </a:dk1>
               
               <!-- Background 1 -->
               <a:lt1>
                  <a:sysClr val="window" lastClr="${colors[0]}"/>
               </a:lt1>

               <!-- Text 2 -->
               <a:dk2>
                  <a:srgbClr val="${colors[3]}"/>
               </a:dk2>

               <!-- Background 2 -->
               <a:lt2>
                  <a:srgbClr val="${colors[2]}"/>
               </a:lt2>

               <!-- Accent 1 -->
               <a:accent1>
                  <a:srgbClr val="${colors[4]}"/>
               </a:accent1>

               <!-- Accent 2 -->
               <a:accent2>
                  <a:srgbClr val="${colors[5]}"/>
               </a:accent2>
               
               <!-- Accent 3 -->
               <a:accent3>
                  <a:srgbClr val="${colors[6]}"/>
               </a:accent3>

               <!-- Accent 4 -->
               <a:accent4>
                  <a:srgbClr val="${colors[7]}"/>
               </a:accent4>

               <!-- Accent 5 -->
               <a:accent5>
                  <a:srgbClr val="${colors[8]}"/>
               </a:accent5>

               <!-- Accent 6 -->
               <a:accent6>
                  <a:srgbClr val="${colors[9]}"/>
               </a:accent6>

               <!-- Hyperlink -->
               <a:hlink>
                  <a:srgbClr val="${colors[10]}"/>
               </a:hlink>

               <!-- Followed hyperlink -->
               <a:folHlink>
                  <a:srgbClr val="${colors[11]}"/>
               </a:folHlink>
            </a:clrScheme>
         `],  {type: "application/xml"});

         link.href = URL.createObjectURL(colorGroupFile);
         link.download = this.colorGroupName.replace(/\s/g, " ") + ".xml";
         link.click();
         URL.revokeObjectURL(link.href);
      }
   }
}
</script>
