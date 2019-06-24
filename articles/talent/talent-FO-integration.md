---
title: Rakenduse Dynamics 365 for Talent rakendusse Dynamics 365 for Finance and Operations integreerimise KKK
description: Selles teemas selgitatakse, millised andmed sünkroonitakse rakenduste Talent ja Finance and Operations integratsioonis.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: db542e4df79480624ff6e5ff1996ad930fc1564b
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617339"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>Rakenduse Dynamics 365 for Talent rakendusse Dynamics 365 for Finance and Operations integreerimise KKK

[!include [banner](includes/banner.md)]

Teemas on toodud vastused peamistele küsimustele selle kohta, milliseid andmeid sünkroonitakse, kui Dynamics 365 for Talent integreeritakse rakendusega Dynamics 365 for Finance and Operations.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Kas sünkroonitakse kõik andmed või ainult mõned andmeüksused?

Rakenduse Core Human Resources (HR) puhul sünkroonitakse andmete alamkogum. Kõigi üksuste loendi leiate teemast [Integratsioon rakendusest Dynamics 365 for Talent rakendusse Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).

Rakenduste Attract ja Onboard puhul on kõik andmed teenuse Common Data Service omaandmed.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Kas uue vastenduse saab luua malle kasutamata?

Mallid on alguspunkt. Saate luua oma malli, kuid malli on integratsiooniprojekti loomisel alati vaja. Lisateavet andmeintegraatori (DI), mallide ja projektide kohta vaadake teemast [Andmete integreerimine teenusesse Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Kas ma saan vastendada finantsdimensioonide edastamise rakenduste Talent ja Finance and Operations vahel?

Finantsdimensioonid puuduvad praegu teenusest Common Data Service ja seetõttu ei ole need ka vaikemalli osa. See üksus on kavas, kuid praegu pole väljastamise ajakava saadaval.

Andmete puhul, mis on olemas rakenduses Finance and Operations, kuid puuduvad rakendusest Talent, linkige kaks süsteemi kokku, kasutades Talenti funktsiooni **Linkide konfigureerimine**. Lisateavet linkide konfigureerimise kohta rakenduste Talent ja Finance and Operations vahel vt teemast [Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (31. oktoober 2018)](whats-new-talent-october-31.md).

![Finantsdimensioonide vastendamine](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>Töövõtjate importimisel liiguvad need mõnikord rakenduses Finance and Operations passiivsete töötajate loendisse. Miks?

See tõrge võib ilmneda, kui töövõtjal pole Talentis aktiivse töösuhte üksikasjade kirjet. Probleemi lahendamiseks minge jaotisse **Personalihaldus \> Töövõtjad \> Töösuhte ajalugu \> Kuupäevahaldur** ja kontrollige, kas seal on aktiivse töösuhte üksikasjade kirje olemas.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Kui soovin vastendada ainult väljade alamkogumi, siis kas vastendamata väljade muutmine käivitab sünkroonimise?

Andmete sünkroonimine järgib käivitusgraafikut. Integratsioon valib kirje, kui selle mis tahes väli muutub, olenemata sellest, kas väli on integratsioonivastenduse osa või mitte.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Kuidas saata ainult aktiivse töötaja muudatused, mitte lõpetatud kirjed?

Kasutades täpsemat päringut, saate lähteandmeid filtreerida ja ümber kujundada, enne kui edastate need sihtkohta.

![Aktiivsete töötajate täpsem päring](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>Kas saan määrata, millised väljad saadetakse rakendusse Finance and Operations kindla üksuse puhul?

Integratsiooniülesandele saab välju lisada või neid eemaldada. Kõiki andmevälju, mis on teenuse Common Data Service üksuses olemas, ei asustata rakendusest Core HR.
Lisaandmeid saab asustada PowerAppsi kaudu.

![Integratsiooniülesandele väljade lisamine ja nende eemaldamine](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Seadistan integratsiooni pakett-tööna, kuid Talentil kadus ühendus sihtsüsteemiga. Kuidas saata sihtsüsteemi sama muudatuste kogum?

Erandite töötlemiseks pole eriseadistus vajalik. Andmeintegraator jäädvustab ja teatab automaatselt tõrgetest, mis ilmnevad lähte- ja sihtkohas, ning lubab käsitsi uuesti proovida. See ei võimalda siiski andmeid käsitsi parandada. Kui andmete värskendamine on vajalik, tuleb seda teha kas lähte- või sihtkohas.

## <a name="can-i-set-up-bi-directional-integration"></a>Kas saan seadistada kahesuunalise integratsiooni?

Ei, integratsioon on praegu ainult ühesuunaline (Talentist Finance and Operationsisse). Siiski on saadaval vaikemall andmete saatmiseks Talentist Finance and Operationsisse.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Kas saan integratsiooni osana lubada kirjete kustutamise?

Ei, andmeintegraator ei talleta kustutatud kirjeid andmeedastuseks. Praegu hõlmab see ainult andmete loomist ja värskendamist (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Kas tõrkega käituse saab uuesti käivitada? Kui jah, siis kas see saadab kogu faili või ainult muudatused?

Andmeintegraatori esmane käitamine on alati täielik. Järgmised käitused põhinevad muudatuste jälgimisel. Tõrkega käituse korral eraldab see kõnealused kirjed käitusest ja saadab teenusest Common Data Service välja uusimad muudatused.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Saan projekti salvestamisel tõrketeate „Projektil on vastendustõrked”. Mida teha?

Kontrollige oma integratsioonivõtmete seadistust, tehke seadistusse vajalikud muudatused ja seejärel värskendage üksuseid projektis.

Vaikemalli kasutamisel imporditakse integratsioonivõtmed automaatselt. See probleem võib ilmneda, kui olemasolevale mallile lisatakse uusi ülesandeid.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Kui mul on N juriidilist isikut, mille töötajatel on töösuhe, siis kas pean looma neist igaühe jaoks vastenduse?

Jah, rakenduses Finance and Operations peab iga juriidilise isiku kohta olema andmeintegratsioonis eraldi integratsiooniprojekt.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Pean edastama andmeid, mis ei ole Microsofti vaikemalli osa. Kas saan seda teha?

Jah, olemasolevale mallile saab välju lisada või neid eemaldada. Malli saab muuta, kaasates lisaandmeid teistest teenuse Common Data Service üksustest. Malli kaasamiseks peab üksus olema teenuses Common Data Service. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Lõin äsja uued Finance and Operationsi ja Talenti keskkonnad ning saan tõrketeate „Andmete väärtus rikub tervikluse piiranguid”. Miks?

Tõrke põhjused võivad olla järgmised.

- Andmeedastuse tulemuseks on topeltkirjete eraldamine lähtekohas (Common Data Service).

- Andmeedastusel on Finance and Operationsis vajalike väljade puhul nullväärtused. Kontrollige, kas teenuses Common Data Service olevad andmed vastavad rakenduse Finance and Operations nõuetele.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Kui esineb käivitustõrkeid ja töövõtja ID-d ei sünkroonita, siis kuidas leida ajalooline töö, milles on nurjunud töövõtja kirje?

Andmeintegraator loob rakenduses Finance and Operations mitu projekti. Seos andmeintegraatori ülesande ja rakenduse Finance and Operations projekti vahel on üksühene.

Jälgige aega andmeintegraatori käivitusajaloost ja leidke rakenduses Finance and Operations projekti indeks – 1. Kui ülesande number on andmeintegraatoris 9, siis indeks Finance and Operationsis on 8.

1. Märkige üles ülesande indeks andmeintegraatorist (selles näites 9).

![Andmeintegraatorist ülesande indeksi ülesmärkimine](media/CaptureTaskIndex.png)

2. Jälgige projekti käivitusaega.

![Projekti käivitusaja jälgimine](media/CaptureTimeOfExecution.png)

3. Rakenduses Finance and Operations leidke indeks – 1. Selles näites vastab projekt järelliitega 8 ja projekti indeksiga 0 käivitusaeg etapis 2 näidatud käivitusajale.

![Indeksi tuvastamine](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Pärast Talenti ja Finance and Operationsi integreerimist ei näe ma enam oma Talenti andmeid rakenduses Finance and Operations. Mida teha?

Integratsioon rakendusse Finance and Operations on kaheetapiline protsess. Esmalt kontrollige, kas Talenti andmed on värskendatud ja teenuses Common Data Service saadaval. See on peaaegu reaalajas sünkroonimine ja seda saab kontrollida PowerAppsis, vaadates andmeüksustes olevaid andmeid.

![Andmed teenuses Common Data Service](media/DataInCDS.png)

Kui andmeid ei kuvata teenuses Common Data Service oodatud viisil, siis kontrollige, kas integratsioon toetab üksust. Teenuse Common Data Service lisaandmete kaasamiseks on vajalik muudatus Microsofti poolel.

Kui üksust toetatakse ja andmed on teenuses Common Data Service saadaval, siis kontrollige, kas vastendus on andmeintegraatoris õige. Kui integraatori vastendus tundub olevat korras, siis kontrollige edukalt käitatud andmehalduse töid. Tõrked võivad ilmneda pakett-tööde käivitamisel. Lisateavet andmehalduse kohta vt teemast [Andmehaldus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>Pärast töövõtjate importimist rakendusse Finance and Operations on nende aadressid valed. Mida teha?

**Asukoha ID** numbriseeria kasutab rakendustes Talent ja Finance and Operations sama mustrit. Numbriseeria peab olema mõlemal poolel kordumatu, et andmete integreerimisel teenusest Common Data Service rakendusse Finance and Operations ei tekiks aadressivastuolusid.

Talenti juurutamise ajal kontrollige, et numbriseeriad poleks Talentis ja Finance and Operationsis samad. Veenduge, et ükski numbriseeria poleks identne, kui andmeid võidakse hallata mõlemas süsteemis.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Ühendusekogumi loomisel ei näe ma ühendust ripploendis Ühendus. Mida teha?

Veenduge, et valiksite ühenduste loomisel suvandid Dynamics 365 for Finance and Operations (praegu eelvaateversioonis) ja Common Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Saan töösuhete sünkroonimisel tõrketeate „Atribuuti CompanyInfo_FK pole olemas” või „Väärtust 12/31/2154 23:59:59 väljal Töösuhte lõppkuupäev ei leitud seotud tabelist Töösuhe”. Mida teha?

Veendute, et vastendaksite õigete juriidiliste isikutega. Juriidilise isiku sünkroonimine pole vaikemalli osa, seega peaks iga Talentis ja teenuses Common Data Service olev juriidiline isik olemas olema ka Finance and Operationsis.
Veenduge ka, et valiksite seostatud ühendusekogumi jaoks õiged juriidilised isikud.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>Pärast projekti seadistamist kuvatakse väljavastendus Finance and Operationsi puhul tühjana. Mida teha?

Värskendage andmeüksuseid rakenduses Finance and Operations, minnes jaotisse **Andmehaldus \> Raamistiku parameetrid \> Üksuse sätted \> Värskenda üksuste loendit.** Selle lõpuleviimiseks kulub mõni minut, seejärel peaksite neid vastendusi nägema. See probleem ilmneb uute projektide loomisel.

![Puuduv väljavastendus](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Lisaressursid

- Andmeintegraator (DI): 

  - [Andmete integreerimine teenusesse Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [Andmeintegraatori tõrkehaldus ja tõrkeotsing](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [DSR-i taotlustele vastamine süsteemi loodud logide puhul teenustes PowerApps, Microsoft Flow ja Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Andmehaldus

  - [Andmehaldus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
