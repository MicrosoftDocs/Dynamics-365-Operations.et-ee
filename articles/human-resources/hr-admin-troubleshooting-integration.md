---
title: Finance’i KKK-ga integreerimine
description: Selles artiklis selgitatakse, millised andmed sünkroonitakse rakenduste Human Resources ja Finance integratsioonis.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b9cfc0964a532cd32dda029419c892fa8ae55e02
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008719"
---
# <a name="integration-with-finance-faq"></a>Finance’i KKK-ga integreerimine

Teemas on toodud vastused peamistele küsimustele selle kohta, milliseid andmeid sünkroonitakse, kui Dynamics 365 Human Resources integreeritakse rakendusega Dynamics 365 Finance.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Kas sünkroonitakse kõik andmed või ainult mõned andmeüksused?

Sünkroonitakse andmete alamkogum. Kõigi üksuste loendi leiate teemast [Rakendusega Dynamics 365 Finance integreerimine](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a>Miks ei kuvata andmeid, mis on sünkroonitud teenusega Common Data Service?

Vaikimisi lülitatakse teenuse Common Data Service integratsioon välja uutes keskkondades, mis ei sisalda esitatud demoandmeid. Vaikimisi on see sisse lülitatud uutes keskkondades, mis sisaldavad demoandmeid, ja andmete sünkroonimine algab siis, kui keskkond on ette valmistatud. Pärast seda, kui teie keskkond on andmete sünkroonimiseks valmis, saate integratsiooni sisse lülitada. Lisateavet vt [Teenuse Common Data Service integratsiooni konfigureerimine](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Kas uue vastenduse saab luua malle kasutamata?

Mallid on alguspunkt. Saate luua oma malli, kuid malli on integratsiooniprojekti loomisel alati vaja. Lisateavet andmeintegraatori (DI), mallide ja projektide kohta vaadake teemast [Andmete integreerimine teenusesse Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Kas ma saan vastendada finantsdimensioonide edastamise rakenduste Human Resources ja Finance vahel?

Finantsdimensioonid puuduvad praegu teenusest Common Data Service ja seetõttu ei ole need ka vaikemalli osa. See üksus on kavas, kuid praegu pole väljastamise ajakava saadaval.

Andmete puhul, mis on olemas rakenduses Finance, kuid puuduvad rakendusest Human Resources, linkige kaks süsteemi kokku, kasutades Human Resourcesi funktsiooni **Linkide konfigureerimine**.

![Finantsdimensioonide vastendamine](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Töövõtjate importimisel liiguvad need mõnikord rakenduses Finance passiivsete töötajate loendisse. Miks?

See tõrge võib ilmneda, kui töövõtjal pole rakenduses Human Resources aktiivse tööhõive üksikasjade kirjet. Probleemi lahendamiseks minge jaotisse **Personalihaldus \> Töövõtjad \> Töösuhte ajalugu \> Kuupäevahaldur** ja kontrollige, kas seal on aktiivse töösuhte üksikasjade kirje olemas.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Kui soovin vastendada ainult väljade alamkogumi, siis kas vastendamata väljade muutmine käivitab sünkroonimise?

Andmete sünkroonimine järgib käivitusgraafikut. Integratsioon valib kirje, kui selle mis tahes väli muutub, olenemata sellest, kas väli on integratsioonivastenduse osa või mitte.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Kuidas saata ainult aktiivse töötaja muudatused, mitte lõpetatud kirjed?

Kasutades täpsemat päringut, saate lähteandmeid filtreerida ja ümber kujundada, enne kui edastate need sihtkohta.

![Aktiivsete töötajate täpsem päring](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Kas saan määrata, millised väljad saadetakse rakendusse Finance kindla üksuse puhul?

Integratsiooniülesandele saab välju lisada või neid eemaldada. Kõiki andmevälju, mis on teenuse Common Data Service üksuses olemas, ei asustata rakendusest Human Resources.
Lisaandmeid saab asustada Power Appsi kaudu.

![Integratsiooniülesandele väljade lisamine ja nende eemaldamine](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Seadistan integratsiooni pakett-tööna, kuid rakendusel Human Resources kadus ühendus sihtsüsteemiga. Kuidas saata sihtsüsteemi sama muudatuste kogum?

Erandite töötlemiseks pole eriseadistus vajalik. Andmeintegraator jäädvustab ja teatab automaatselt tõrgetest, mis ilmnevad lähte- ja sihtkohas, ning lubab käsitsi uuesti proovida. See ei võimalda siiski andmeid käsitsi parandada. Kui andmete värskendamine on vajalik, tuleb seda teha kas lähte- või sihtkohas.

## <a name="can-i-set-up-bi-directional-integration"></a>Kas saan seadistada kahesuunalise integratsiooni?

Ei, integreerimine on praegu ühesuunaline (Rakendusest Human Resources rakendusse Finance and Operations). Siiski on saadaval vaikemall andmete saatmiseks rakendusest Human Resources rakendusse Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Kas saan integratsiooni osana lubada kirjete kustutamise?

Ei, andmeintegraator ei talleta kustutatud kirjeid andmeedastuseks. Praegu hõlmab see ainult andmete loomist ja värskendamist (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Kas tõrkega käituse saab uuesti käivitada? Kui jah, siis kas see saadab kogu faili või ainult muudatused?

Andmeintegraatori esmane käitamine on alati täielik. Järgmised käitused põhinevad muudatuste jälgimisel. Tõrkega käituse korral eraldab see kõnealused kirjed käitusest ja saadab teenusest Common Data Service välja uusimad muudatused.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Saan projekti salvestamisel tõrketeate „Projektil on vastendustõrked”. Mida teha?

Kontrollige oma integratsioonivõtmete seadistust, tehke seadistusse vajalikud muudatused ja seejärel värskendage üksuseid projektis.

Vaikemalli kasutamisel imporditakse integratsioonivõtmed automaatselt. See probleem võib ilmneda, kui olemasolevale mallile lisatakse uusi ülesandeid.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Kui mul on N juriidilist isikut, mille töötajatel on töösuhe, siis kas pean looma neist igaühe jaoks vastenduse?

Jah, rakenduses Finance peab iga juriidilise isiku kohta olema andmeintegratsioonis eraldi integratsiooniprojekt.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Pean edastama andmeid, mis ei ole Microsofti vaikemalli osa. Kas saan seda teha?

Jah, olemasolevale mallile saab välju lisada või neid eemaldada. Malli saab muuta, kaasates lisaandmeid teistest teenuse Common Data Service üksustest. Malli kaasamiseks peab üksus olema teenuses Common Data Service. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Lõin äsja uued Finance’i ja Human Resourcesi keskkonnad ning saan tõrketeate „Andmete väärtus rikub tervikluse piiranguid”. Miks?

Tõrke põhjused võivad olla järgmised.

- Andmeedastuse tulemuseks on topeltkirjete eraldamine lähtekohas (Common Data Service).

- Andmeedastusel on Finance and Operationsis vajalike väljade puhul nullväärtused. Kontrollige, kas teenuses Common Data Service olevad andmed vastavad rakenduse Finance and Operations nõuetele.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Kui esineb käivitustõrkeid ja töövõtja ID-d ei sünkroonita, siis kuidas leida ajalooline töö, milles on nurjunud töövõtja kirje?

Andmeintegraator loob rakenduses Finance mitu projekti. Seos andmeintegraatori ülesande ja rakenduse Finance projekti vahel on üksühene.

Jälgige aega andmeintegraatori käivitusajaloost ja leidke rakenduses Finance projekti indeks – 1. Kui ülesande number on andmeintegraatoris 9, siis indeks Finance’is on 8.

1. Märkige üles ülesande indeks andmeintegraatorist (selles näites 9).

    ![Andmeintegraatorist ülesande indeksi ülesmärkimine](media/CaptureTaskIndex.png)

2. Jälgige projekti käivitusaega.

    ![Projekti käivitusaja jälgimine](media/CaptureTimeOfExecution.png)

3. Finantsis määratlege indeks -1. Selles näites vastab projekt järelliitega 8 ja projekti indeksiga 0 käivitusaeg etapis 2 näidatud käivitusajale.

    ![Indeksi tuvastamine](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>Pärast rakenduste Human Resources ja Finance integreerimist ei näe ma Human Resourcesi andmeid Finance’is. Mida teha?

Integratsioon rakendusse Finance on kaheetapiline protsess. Esmalt kontrollige, kas rakenduse Human Resources andmed on värskendatud ja teenuses Common Data Service saadaval. See on peaaegu reaalajas sünkroonimine ja seda saab kontrollida Power Appsis, vaadates andmeüksustes olevaid andmeid.

![Andmed teenuses Common Data Service](media/DataInCDS.png)

Kui andmeid ei kuvata teenuses Common Data Service oodatud viisil, siis kontrollige, kas integratsioon toetab üksust. Teenuse Common Data Service lisaandmete kaasamiseks on vajalik muudatus Microsofti poolel.

Kui üksust toetatakse ja andmed on teenuses Common Data Service saadaval, siis kontrollige, kas vastendus on andmeintegraatoris õige. Kui integraatori vastendus tundub olevat korras, siis kontrollige edukalt käitatud andmehalduse töid. Tõrked võivad ilmneda pakett-tööde käivitamisel. Lisateavet andmehalduse kohta vt teemast [Andmehaldus](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Pärast töövõtjate importimist rakendusse Finance, on nende aadressid valed. Mida teha?

**Asukoha ID** numbriseeria kasutab rakendustes Human Resources ja Finance sama mustrit. Numbriseeria peab olema mõlemal poolel kordumatu, et andmete integreerimisel teenusest Common Data Service rakendusse Finance and Operations ei tekiks aadressivastuolusid.

Human Resourcesi juurutamise ajal kontrollige, et numbriseeriad poleks rakendustes Human Resources ja Finance and Operations samad. Veenduge, et ükski numbriseeria poleks identne, kui andmeid võidakse hallata mõlemas süsteemis.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Ühendusekogumi loomisel ei näe ma ühendust ripploendis Ühendus. Mida teha?

Veenduge, et valiksite ühenduste loomisel suvandid Dynamics 365 Finance ja Common Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Saan töösuhete sünkroonimisel tõrketeate „Atribuuti CompanyInfo_FK pole olemas” või „Väärtust 12/31/2154 23:59:59 väljal Töösuhte lõppkuupäev ei leitud seotud tabelist Töösuhe”. Mida teha?

Veendute, et vastendaksite õigete juriidiliste isikutega. Juriidilise isiku sünkroonimine pole vaikemalli osa, seega peaks iga Human Resourcesis ja teenuses Common Data Service olev juriidiline isik olemas olema ka Finance’is.
Veenduge ka, et valiksite seostatud ühendusekogumi jaoks õiged juriidilised isikud.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Pärast projekti seadistamist kuvatakse väljavastendus Finance’i puhul tühjana. Mida teha?

Värskendage andmeüksuseid rakenduses Finance, minnes jaotisse **Andmehaldus \> Raamistiku parameetrid \> Üksuse sätted \> Värskenda üksuste loendit.** Selle lõpuleviimiseks kulub mõni minut, seejärel peaksite neid vastendusi nägema. See probleem ilmneb uute projektide loomisel.

![Puuduv väljavastendus](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Lisaressursid

- Andmeintegraator (DI): 

  - [Andmete integreerimine teenusesse Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [Andmeintegraatori tõrkehaldus ja tõrkeotsing](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [DSR-i taotlustele vastamine süsteemi loodud logide puhul teenustes Power Apps, Microsoft Power Automate ja Common Data Service](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Andmehaldus

  - [Andmehaldus](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
