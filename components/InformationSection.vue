<template>
   <div class="info-section">
      <header>
         <h1 class="title">
            MS Office Themer
         </h1>
         <h2 class="subtitle">
            A Microsoft Office custom theme creator
         </h2>
      </header>
      <section id="intro" class="">
         <p class="body-text">
            This custom theme creator was made by Barrett Lo in December 2021 after finding it ridiculous that the Microsoft Office suite did not include a custom color/font theme creation tool for MacOS.
         </p>
         <h1 class="content-h1">
            Instructions
         </h1>
         <ol class="">
            <li>Give a name to your color group
            <li>Select a color for each purpose</li>
            <li>Click the "Generate color group" button (this will prompt a download of an XML file)</li>
            <li>Save the file and place it into the "Theme Colors" folder
               <ol class="">
                  <li>In Excel, navigate to the "Page Layout" pane</li>
                  <li>Click on "Themes"</li>
                  <li>Click on "Browse for Themes..."</li>
                  <li>Follow file path to correct folder</li>
               </ol>
            </li>
            <li>In Excel, navigate to the "Page Layout" pane</li>
            <li>Click on "Colors"</li>
            <li>Your custom color group should appear at the top</li>
         </ol>
      </section>
   </div>
</template>

<script>
export default {
   name: "InformationSection"
}
</script>
