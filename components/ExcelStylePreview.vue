<template>
   <table class="excel-style-preview">
      <colgroup>
         <col class="sheet-number-col">
         <col>
         <col>
         <col>
         <col>
      </colgroup>
      <tr class="excel-row sheet-header">
         <th class="excel-cell sheet-corner">&nbsp;</th>
         <th class="excel-cell text">A</th>
         <th class="excel-cell text">B</th>
         <th class="excel-cell text">C</th>
         <th class="excel-cell text">D</th>
      </tr>
      <tr class="excel-row column-header">
         <td class="excel-cell sheet-number">1</td>
         <td class="excel-cell text">Text</td>
         <td class="excel-cell text">Stroke</td>
         <td class="excel-cell text">Fill</td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row bg-1">
			<td class="excel-cell sheet-number">2</td>
         <td class="excel-cell text" :style="{color: colors[0].color}">
            Background 1
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[0].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[0].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row txt-1">
			<td class="excel-cell sheet-number">3</td>
         <td class="excel-cell text" :style="{color: colors[1].color}">
            Text 1
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[1].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[1].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row bg-2">
			<td class="excel-cell sheet-number">4</td>
         <td class="excel-cell text" :style="{color: colors[2].color}">
            Background 2
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[2].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[2].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row txt-2">
			<td class="excel-cell sheet-number">5</td>
         <td class="excel-cell text" :style="{color: colors[3].color}">
            Text 2
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[3].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[3].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row acc-1">
			<td class="excel-cell sheet-number">6</td>
         <td class="excel-cell text" :style="{color: colors[4].color}">
            Accent 1
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[4].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[4].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row acc-2">
			<td class="excel-cell sheet-number">7</td>
         <td class="excel-cell text" :style="{color: colors[5].color}">
            Accent 2
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[5].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[5].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row acc-3">
			<td class="excel-cell sheet-number">8</td>
         <td class="excel-cell text" :style="{color: colors[6].color}">
            Accent 3
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[6].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[6].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row acc-4">
			<td class="excel-cell sheet-number">9</td>
         <td class="excel-cell text" :style="{color: colors[7].color}">
            Accent 4
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[7].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[7].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row acc-5">
			<td class="excel-cell sheet-number">10</td>
         <td class="excel-cell text" :style="{color: colors[8].color}">
            Accent 5
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[8].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[8].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row acc-6">
			<td class="excel-cell sheet-number">11</td>
         <td class="excel-cell text" :style="{color: colors[9].color}">
            Accent 6
         </td>
         <td class="excel-cell stroke" :style="{outlineColor: colors[9].color}"></td>
         <td class="excel-cell fill" :style="{backgroundColor: colors[9].color}"></td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row">
         <td class="excel-cell sheet-number">12</td>
         <td class="excel-cell empty">&nbsp;</td>
         <td class="excel-cell empty">&nbsp;</td>
         <td class="excel-cell empty">&nbsp;</td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row HL">
			<td class="excel-cell sheet-number">13</td>
         <td class="excel-cell text" :style="{color: colors[10].color}">
            Hyperlink
         </td>
         <td class="excel-cell text" colspan="2" :style="{color: colors[11].color}">
            Followed Hyperlink
         </td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
      <tr class="excel-row">
         <td class="excel-cell sheet-number">14</td>
         <td class="excel-cell empty">&nbsp;</td>
         <td class="excel-cell empty">&nbsp;</td>
         <td class="excel-cell empty">&nbsp;</td>
         <td class="excel-cell empty">&nbsp;</td>
      </tr>
   </table>
</template>

<script>
export default {
   name: 'ExcelStylePreview',
   props: {
      colors: {
         type: Array,
         default: null
      }
   }
}
</script>