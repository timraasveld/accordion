<script setup lang="ts">
import Accordion from "@/components/Accordion.vue";
import {ref} from "vue";


const items = ref([
    {
        title: 'Referentieniveaus',
        text: '<p>ESIS kent de volgende ingangen naar overzichten op bovenschools niveau:</p>\n' +
            '<ul>\n' +
            '<li><strong>Overzichten en exporten &gt; Dashboard Managementinformatie</strong></li>\n' +
            '<li>Overzichten en exporten &gt; Overzichten &gt; Management &gt; Management overzichten per school en bovenschools</li>\n' +
            '<li>Overzichten en exporten &gt; Overzichten &gt; Management &gt; Telling Dossierregistraties-OPP-Langdurig verzuim</li>\n' +
            '<li>Overzichten en&nbsp;exporten &gt; Overzichten &gt; Management &gt; Referentieniveaus</li>\n' +
            '<li>Overzichten en exporten &gt; Overzichten &gt; Toetsen &gt; Dwarsdoorsnede historie</li>\n' +
            '<li>Overzichten en exporten &gt; Exporteren &gt; Prognose inschrijvingen</li>\n' +
            '</ul>\n' +
            '<p>Dit artikel behandelt de vierde.</p>\n' +
            '<p>Het overzicht <strong>Referentieniveaus</strong> is ontwikkeld voor directies, intern begeleiders en bovenschoolse kwaliteitsmedewerkers om inzicht te krijgen in de eindopbrengsten op basis van aantallen en percentages leerlingen per referentieniveau per toetsonderdeel op vestigings- en bestuursniveau.</p>\n' +
            '<p>Lees meer over dit overzicht in de bijlage bij dit artikel.</p>',
    },
    {
        title: 'Invoerlijst scores per groep',
        text: 'Bij een invoerlijst met omrekening worden de resultaten op de invoerlijstonderdelen wel omgerekend. ESIS zet de ingevoerde score af tegen een norm en voegt een omrekening toe aan het resultaat. Zie het voorbeeld: 21 -> V. Als resultaten worden omgerekend, zal ESIS in het overzicht en op de rapporten rekenen met de waarden die aan de omrekeningen zijn toegekend. Die toekenning is opgegeven in de beoordeling scoringswijze die aan de invoerlijst gekoppeld is. Zo kan bijvoorbeeld ‘onvoldoende’ een waarde 4 hebben of ‘goed’ een waarde 8.'
    },
    {
        title: 'Datumgrenzen bij overzicht Leerlingdossier-Registraties',
        text: '<p><strong>Aandachtspunt bij het overzicht Leerlingdossier-Registraties</strong><br> Wanneer u kiest voor het afdrukken van registraties, dan geldt het volgende met betrekking tot de <strong>datumgrenzen:</strong></p>\n' +
            '<ul>\n' +
            '<li>Alle registraties waarbij de aanmaakdatum binnen de ingevulde begin- en einddatum liggen worden getoond.</li>\n' +
            '<li>Indien er alleen een einddatum is opgegeven, worden de registraties getoond met een aanmaakdatum die voor de einddatum ligt.</li>\n' +
            '<li>Alle registraties worden getoond waarbij de startdatum na de ingevulde begindatum ligt en de einddatum na de ingevulde einddatum ligt.</li>\n' +
            '<li>Indien er alleen een einddatum is opgegeven, worden de registraties getoond waarvan de einddatum voor de ingevulde einddatum ligt.</li>\n' +
            '</ul>\n' +
            '<p>Op deze manier worden ook incidenten getoond die vandaag aangemaakt zijn, maar bijvoorbeeld een begin- en einddatum hebben van vorige maand.</p>'
    }
] as Array<AccordionItem>);
</script>

<template>
    <main>
        <accordion :items="items"/>
    </main>
</template>

<style scoped>
</style>
