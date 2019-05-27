---
title: Registreerimismärgi sildi printimise lubamine
description: Kui müügi komplekteerimise tööprotsessis on viimane kaup varudest valitud, lubab see protseduur konteineri seeriaviisi lähetamise koodi (SSCC) sildi automaatse printimise.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d906ca9f5a6536870fa0c322a0792ed5672c25e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558099"
---
# <a name="enable-license-plate-label-printing"></a>Registreerimismärgi sildi printimise lubamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kui müügi komplekteerimise tööprotsessis on viimane kaup varudest valitud, lubab see protseduur konteineri seeriaviisi lähetamise koodi (SSCC) sildi automaatse printimise. Võite seda protseduuri käitada demoettevõtte USMF-i andmetega. Kui käitate seda omaenda andmeid kasutades, peaksite määrama litsentsiplaatide numbriseeria. Enne ülesande juurde asumist peaksite määrama sildiprinteri. Avage Organisatsiooni haldus > Seadistus > Võrguprinterid. Klõpsake toimingupaanil Suvandid, seejärel klõpsake nuppu Laadi dokumendi marsruudivaliku agendi installer alla. Käitage installer ja veenduge enne protseduuriga jätkamist, et töötav võrguprinter on seatud olekusse Aktiivne.


## <a name="set-up-the-gs1-company-prefix"></a>GS1 ettevõtteprefiksi seadistus
1. Avage Laohaldus > Seadistus > Laohalduse parameetrid.
2. Sisestage väljale GS1 ettevõtteprefiks GS1 ettevõtte koodi 7 numbrit.
3. Klõpsake nuppu Salvesta.
4. Sulgege leht.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>SSCC-identifitseerimisnumbri numbriseeria seadistus
1. Avage Organisatsiooni haldus > Numbriseeriad > Numbriseeriad.
2. Valige suvand väljal Ala.
3. Valige suvand väljal Viide.
4. Sisestage väärtus väljale Ettevõte.
5. Märkige loendis valitud rida.
6. Klõpsake loendis valitud real olevat linki.
7. Laiendage jaotist Segmendid.
8. Klõpsake nuppu Redigeeri.
9. Valige tabelist Segmendid esimene rida.
10. Klõpsake nuppu Eemalda.
11. Klõpsake nuppu Eemalda.
12. Klõpsake nuppu Salvesta.
13. Sulgege leht.

## <a name="create-the-document-route-layout"></a>Dokumendi marsruudivaliku paigutuse loomine
1. Avage Laohaldus > Seadistus > Dokumendi marsruudivalik > Dokumendi marsruudivaliku paigutused.
    * Saate lubada SSCC-paigutuse.  
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Paigutuse ID.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Otsige loendist ja valige soovitud kirje.
6. Klõpsake Lisa teksti lõppu.
7. Klõpsake nuppu Salvesta.
8. Sulgege leht.

## <a name="set-up-the-document-routing"></a>Dokumendi marsruudivaliku häälestamine
1. Avage Laohaldus > Seadistus > Dokumendi marsruudivalik > Dokumendi marsruudivalik.
2. Valige suvand väljal Töökäsu tüüp.
3. Klõpsake Uus.
4. Sisestage väärtus väljale Ladu.
5. Sisestage väärtus väljale Nimi.
6. Klõpsake Uus.
7. Sisestage või valige väärtus väljal Paigutuse ID.
8. Sisestage väljale Nimi printeri nimi, mida soovite kasutada.
9. Klõpsake nuppu Salvesta.
10. Sulgege leht.

## <a name="create-mobile-device-menu"></a>Mobiilse seadme menüü loomine
1. Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Menüü-üksuse nimi.
4. Sisestage väärtus väljale Pealkiri.
5. Valige suvand väljal Režiim.
6. Valige suvand Jah väljal Kasuta olemasolevat tööd.
7. Valige suvand Jah väljal Loo litsentsiplaat.
8. Laiendage jaotist Tööklassid.
9. Klõpsake valikut Uus.
10. Sisestage väärtus väljale Tööklassi ID.
11. Klõpsake nuppu Salvesta.
12. Sulgege leht.
13. Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü.
14. Otsige loendist ja valige soovitud kirje.
15. Valige puul Vali puul varem loodud menüü-üksus.
16. Klõpsake nuppu Redigeeri.
17. Menüü-üksuse menüüsse lisamiseks klõpsake noolel.
18. Klõpsake nuppu Salvesta.
19. Sulgege leht.

## <a name="update-a-work-template"></a>Töömalli värskendus
1. Avage Laohaldus > Seadistus > Töö > Töömallid.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake nuppu Redigeeri.
4. Klõpsake Uus.
5. Märkige loendis valitud rida.
6. Valige Prindi väljal Töö tüüp.
7. Sisestage või valige väärtus väljal Tööklassi ID.
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake nuppu Ülespoole.
10. Klõpsake nuppu Salvesta.
11. Sulgege leht.

