<template>
    <button @click="generatePDF">make PDF</button>
    <!-- https://pdfcandle.com/pdf_color.aspx -->
    <div id="pdf" style="background-color: #000000 !important;">
        <div class="p-4" style="background-color: #000000 !important;">
            <h1>&lt;Blog Thor Demeestere/&gt;</h1>
            <blog :download="true" style="background-color: #000000 !important;" />
            <div cl ass="h-[100%] w-[100%]" style="background-color: #000000 !important;"></div>
        </div>
    </div>
</template>

<script setup lang="ts">
    import blog from '@/views/blog.vue';
    import html2pdf from 'html2pdf.js';

    function generatePDF() {
        const doc = document.querySelector('#pdf');
        html2pdf(doc, {
            margin: 0,
            filename: 'blog.pdf',
            image: { type: 'jpeg', quality: 0.98 },
            html2canvas: { scale: 2 },
            jsPDF: { unit: 'mm', orientation: 'portrait' },
            pagebreak: { mode: 'avoid-all' }
        });
    }
</script>

<style scoped></style>
