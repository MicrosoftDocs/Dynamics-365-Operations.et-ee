---
title: Elektroonilise aruandluse konfiguratsioonide kujundamine Wordi vormingus aruannete loomiseks
description: Järgmine etapp selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab konfigureerida elektroonilise aruandluse vorminguid, et luua aruandeid Microsoft Wordi failidena.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "362345"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>Elektroonilise aruandluse konfiguratsioonide kujundamine Wordi vormingus aruannete loomiseks

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmine etapp selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab konfigureerida elektroonilise aruandluse (ER) vorminguid, et luua aruandeid Microsoft Wordi failidena. Neid toiminguid saab teha GBSI ettevõttes.

Nende etappide lõpuleviimiseks peate esmalt läbima tegevusejuhises „ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML” esitatud etapid. Eelnevalt peate näidisaruande jaoks alla laadima ja kohalikult salvestama ka järgmised mallid:

- [Maksearuande mall](https://go.microsoft.com/fwlink/?linkid=862266)
- [Maksearuande piiratud mall](https://go.microsoft.com/fwlink/?linkid=862266)


See protseduur on funktsiooni kohta, mis lisati rakenduse Microsoft Dynamics 365 for Operations versioonis 1611.


## <a name="select-the-existing-er-report-configuration"></a>Olemasoleva elektroonilise aruandluse aruande konfiguratsiooni valimine
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et konfiguratsiooni pakkuja Litware, Inc. on valitud aktiivsena.  
2. Klõpsake valikut Aruandluse konfiguratsioonid.
    * Taaskasutame olemasolevat elektroonilise aruandluse konfiguratsiooni, mis on algselt mõeldud aruande väljundi loomiseks OPENXML-vormingus.  
3. Laiendage puus sõlme „Payment model”.
4. Tehke puul valik Maksemudel \ töölehe aruande näide.
5. Klõpsake valikut Kujundaja.

## <a name="replace-the-excel-template-with-the-word-template"></a>Exceli malli asendamine Wordi malliga
    * Praegu kasutatakse Exceli dokumenti mallina väljundi loomiseks OPENXML-vormingus. Impordime aruande malli Wordi vormingus.  
1. Klõpsake suvandit Manused.
    * Asendage olemasolev Exceli mall varem allalaaditud Wordi malliga (SampleVendPaymDocReport.docx). Pange tähele, et see mall sisaldab ainult sellise dokumendi paigutust, mida soovime luua elektroonilise aruandluse väljundina.  
2. Klõpsake  Kustuta.
3. Klõpsake nuppu Jah.
4. Klõpsake valikut Uus.
5. Klõpsake suvandit Fail.
6. Klõpsake käsku Sirvi. Navigeerige asukohta ja valige varasemalt allalaaditud SampleVendPaymDocReport.docx. Klõpsake nuppu OK.
    * Valige eelmises etapis allalaaditud mall.  
7. Sisestage või valige väärtus väljal Mall.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Kohandatud XML-i osa lisamise abil Wordi malli laiendamine
1. Klõpsake nuppu Salvesta.
    * Lisaks konfiguratsiooni muudatuste salvestamisele värskendab toiming Salvesta ka manustatud Wordi malli. Kujundatud vormingu struktuur porditakse manustatud Wordi dokumenti uue kohandatud XML-i osana, mille nimi on „Aruanne”. Pange tähele, et manustatud Wordi mall sisaldab mitte ainult sellise dokumendi paigutust, mida soovime luua elektroonilise aruandluse väljundina, vaid see sisaldab ka andmete struktuuri, mille elektrooniline aruandlus sisestab käitusajal sellesse malli.  
2. Klõpsake suvandit Manused.
    * Nüüd peate siduma kohandatud XML-i osa „Aruanne” elemendid Wordi dokumendi osadega.  
    * Kui olete tuttav Wordi dokumentidega, mida saab kujundada vormidena, mis sisaldavad kohandatud XML-i osade elementidega seotud sisu juhtelemente – läbige sellise dokumendi loomiseks kõik järgmises alamülesandes olevad etapid. Lisateabe saamiseks vaadake järgmist linki https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US. Vastasel juhul jätke vahele järgmise alamülesande etapid.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Andmete sidumiste tegemiseks kohandatud XML-i osaga Wordi hankimine
    * Avage see dokument Wordis ja tehke järgmist. Avage Wordi vahekaart Arendaja (kohandage linti, kui see pole veel lubatud).  - Valige XML-i vastendamise paan.  - Valige otsingust kohandatud XML-i osa „Aruanne”.  - Tehke valitud kohandatud XML-i osa elementide ja Wordi dokumendi sisu juhtelementide vastendamine.  - Salvestage värskendatud Wordi dokument kohalikule kettale.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Wordi malli üleslaadimine sisu juhtelementidega seotud kohandatud XML-i osaga
1. Klõpsake  Kustuta.
2. Klõpsake nuppu Jah.
    * Lisage uus mall. Kui viisite lõpule eelmises alamülesandes esitatud etapid, valige ettevalmistatud ja kohalikult salvestatud Wordi dokument. Vastasel juhul valige varasemalt allalaaditud MS Wordi mall SampleVendPaymDocReportBounded.docx.  
3. Klõpsake valikut Uus.
4. Klõpsake suvandit Fail.
5. Klõpsake käsku Sirvi. Navigeerige asukohta ja valige varasemalt allalaaditud SampleVendPaymDocReportBounded.docx. Klõpsake nuppu OK.
6. Väljal Mall valige eelmises etapis allalaaditud dokument.
7. Klõpsake nuppu Salvesta.
8. Sulgege leht.

## <a name="execute-the-format-to-create-word-output"></a>Wordi väljundi loomiseks vormingu käivitamine
1. Klõpsake tegumiribal valikut Konfiguratsioonid.
2. Klõpsake valikut Kasutaja parameetrid.
3. Tehke väljal Käivita sätted valik Jah.
4. Klõpsake nuppu OK.
5. Klõpsake nuppu Redigeeri.
6. Tehke väljal Käivita mustand valik Jah.
7. Klõpsake nuppu Salvesta.
8. Sulgege leht.
9. Sulgege leht.
10. Avage Ostureskontro > Maksed > Makse tööleht.
11. Klõpsake valikut Read.
12. Märkige või tühjendage loendis kõik read.
13. Klõpsake suvandit Makse olek.
14. Klõpsake nuppu Puudub.
15. Klõpsake valikut Loo maksed.
16. Klõpsake nuppu OK.
17. Klõpsake nuppu OK.
    * Analüüsige loodud väljundit. Pange tähele, et loodud väljundit esitatakse Wordi vormingus ja sisaldab töödeldud maksete üksikasju.  

