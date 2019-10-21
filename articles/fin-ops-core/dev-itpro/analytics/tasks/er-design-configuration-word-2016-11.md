---
title: Elektroonilise aruandluse konfiguratsioonide kujundamine Wordi vormingus aruannete loomiseks
description: Järgmine etapp selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab konfigureerida elektroonilise aruandluse vorminguid, et luua aruandeid Microsoft Wordi failidena.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 327f03435ab55551953fd998dd89c831c76c4c26
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182596"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>Elektroonilise aruandluse konfiguratsioonide kujundamine Wordi vormingus aruannete loomiseks

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmine etapp selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab konfigureerida elektroonilise aruandluse (ER) vorminguid, et luua aruandeid Microsoft Wordi failidena. Neid toiminguid saab teha GBSI ettevõttes.

Nende etappide lõpuleviimiseks peate esmalt läbima tegevusejuhises „ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML” esitatud etapid. Eelnevalt peate näidisaruande jaoks alla laadima ja kohalikult salvestama ka järgmised mallid:

- [Maksearuande mall](https://go.microsoft.com/fwlink/?linkid=862266)
- [Maksearuande piiratud mall](https://go.microsoft.com/fwlink/?linkid=862266)


See protseduur on funktsiooni kohta, mis lisati rakenduse Microsoft Dynamics 365 for Operations versioonis 1611.


## <a name="select-the-existing-er-report-configuration"></a>Olemasoleva elektroonilise aruandluse aruande konfiguratsiooni valimine
1. **Navigeerimispaanil avage Moodulid > Organisatsiooni haldus > Tööruumid > Elektrooniline aruandlus**. Veenduge, et konfiguratsiooni pakkuja Litware, Inc. on valitud aktiivsena.  
2. Klõpsake valikut **Aruandluse konfiguratsioonid**. Taaskasutame olemasolevat elektroonilise aruandluse konfiguratsiooni, mis on algselt mõeldud aruande väljundi loomiseks OPENXML-vormingus.  
3. Laiendage puus sõlme „Payment model”.
4. Tehke puul valik Maksemudel \ töölehe aruande näide.
5. Klõpsake valikut Kujundaja.

## <a name="replace-the-excel-template-with-the-word-template"></a>Exceli malli asendamine Wordi malliga

Praegu kasutatakse Exceli dokumenti mallina väljundi loomiseks OPENXML-vormingus. Impordime aruande malli Wordi vormingus.

1. Klõpsake **Manused**. Asendage olemasolev Exceli mall varem allalaaditud Wordi malliga (SampleVendPaymDocReport.docx). Pange tähele, et see mall sisaldab ainult sellise dokumendi paigutust, mida soovime luua elektroonilise aruandluse väljundina.  
2. Klõpsake  **Kustuta**.
3. Klõpsake nuppu **Jah**.
4. Klõpsake valikut **Uus**.
5. Klõpsake **Fail**.
6. Klõpsake käsku **Sirvi**. Navigeerige asukohta ja valige varasemalt allalaaditud SampleVendPaymDocReport.docx. Klõpsake valikut **OK**. Valige eelmises etapis allalaaditud mall.  
7. Väljas **Mall** sisestage või valige väärtus.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Kohandatud XML-i osa lisamise abil Wordi malli laiendamine
1. Klõpsake valikut **Salvesta**. Lisaks konfiguratsiooni muudatuste salvestamisele värskendab toiming Salvesta ka manustatud Wordi malli. Kujundatud vormingu struktuur porditakse manustatud Wordi dokumenti uue kohandatud XML-i osana, mille nimi on „Aruanne”. Pange tähele, et manustatud Wordi mall sisaldab mitte ainult sellise dokumendi paigutust, mida soovime luua elektroonilise aruandluse väljundina, vaid see sisaldab ka andmete struktuuri, mille elektrooniline aruandlus sisestab käitusajal sellesse malli.  
2. Klõpsake **Manused**.
    + Nüüd peate siduma kohandatud XML-i osa „Aruanne” elemendid Wordi dokumendi osadega.  
    + Kui olete tuttav Wordi dokumentidega, mida saab kujundada vormidena, mis sisaldavad kohandatud XML-i osade elementidega seotud sisu juhtelemente – läbige sellise dokumendi loomiseks kõik järgmises alamülesandes olevad etapid. Lisateabe saamiseks vaadake [Looge ankeete, mida kasutajad täidavad või prindivad Wordides](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US). Vastasel juhul jätke vahele järgmise alamülesande etapid.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Andmete sidumiste tegemiseks kohandatud XML-i osaga Wordi hankimine

Avage see dokument Wordis ja tehke järgmist:  
1. Avage Wordi vahekaart „Arendaja“ (kohandage linti, kui see pole veel lubatud).
2. Valige paan „XML-vastendamine“.
3. Valige otsingus kohandatud XML-osa „Aruanne“.
4. Vastendage valitud kohandatud XML-i osa elemendid ja Word dokumendi sisu juhtelemendid.  5. Salvestage värskendatud Word dokument kohalikule kettale.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Wordi malli üleslaadimine sisu juhtelementidega seotud kohandatud XML-i osaga
1. Klõpsake  **Kustuta**.
2. Klõpsake nuppu **Jah**. Lisage uus mall. Kui viisite lõpule eelmises alamülesandes esitatud etapid, valige ettevalmistatud ja kohalikult salvestatud Wordi dokument. Vastasel juhul valige varasemalt allalaaditud MS Wordi mall SampleVendPaymDocReportBounded.docx.  
3. Klõpsake valikut **Uus**.
4. Klõpsake **Fail**.
5. Klõpsake käsku **Sirvi**. Navigeerige asukohta ja valige varasemalt allalaaditud SampleVendPaymDocReportBounded.docx. Klõpsake valikut **OK**.
6. Valige väljas **Mall** eelmises etapis alla laaditud dokument.
7. Klõpsake valikut **Salvesta**.
8. Sulgege leht.

## <a name="execute-the-format-to-create-word-output"></a>Wordi väljundi loomiseks vormingu käivitamine
1. Paanis **Tegevuspann** klõpsake **Konfiguratsioonid**.
2. Klõpsake valikut **Kasutaja parameetrid**.
3. Valige väljas **Käivitamisseaded** „Jah“.
4. Klõpsake valikut **OK**.
5. Klõpsake valikut **Redigeeri**.
6. Valige väljas **Käivitamismustand** „Jah“.
7. Klõpsake valikut **Salvesta**.
8. Sulgege leht.
9. Sulgege leht.
10. **Navigeerimispaanil** avage **Moodulid > Makstaolevad arved > Maksed > Maksepäevik**.
11. Klõpsake **Read**.
12. Märkige või tühjendage loendis kõik read.
13. Klõpsake **Makse olek**.
14. Klõpsake nuppu **Puudub** .
15. Klõpsake suvandit **Loo maksed**.
16. Klõpsake valikut **OK**.
17. Klõpsake valikut **OK**. Analüüsige loodud väljundit. Pange tähele, et loodud väljundit esitatakse Wordi vormingus ja sisaldab töödeldud maksete üksikasju.  

