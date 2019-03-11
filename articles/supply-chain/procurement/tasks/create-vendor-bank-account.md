---
title: Hankija pangakonto loomine
description: Selles protseduuris kirjeldatakse, kuidas luua hankijale pangakontot.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deb3587667ac13b95617ec219995bfef931df00c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "360620"
---
# <a name="create-a-vendor-bank-account"></a>Hankija pangakonto loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris kirjeldatakse, kuidas luua hankijale pangakontot. Saate seda protseduuri kasutada demoandmete ettevõttes USMF.

1. Tehke valik Hanked > Hankijad > Kõik hankijad.
2. Valige hankija, kellele soovite pangakontot luua, ja klõpsake siis hankija konto ID linki.
3. Klõpsake toimingupaanil suvandit Hankija.
4. Klõpsake valikut Pangakontod.
5. Klõpsake valikut Uus.
6. Sisestage väärtus väljale Pangakonto.
    * Seda ID-d kasutatakse hankija kirje pangakonto tuvastamiseks.  
7. Sisestage väärtus väljale Nimi.
8. Sisestage väärtus väljale Pangagrupid või valige see.
9. Tehke valik väljal Protsessikoodi tüüp.
    * See on protsessikoodi tüüp, mida kasutatakse rahvusvaheliste maksete puhul.  
10. Sisestage väärtus väljale Pangakonto number.
11. Sisestage väärtus väljale SWIFT-kood.
12. Sisestage väärtus väljale IBAN.
    * IBAN-number peab olema õiges vormingus. Näiteks võite kasutada numbrit DE89370400440532013000.  
    * Pangakonto olek on Aktiivne, kui aktiveerimiskuupäev on kätte jõudnud ja aegumiskuupäeva pole ületatud. See on aktiivne ka juhul, kui väljad Aktiveerimiskuupäev ja Aegumiskuupäev on mõlemad tühjad. Kui nii välja Aktiveerimiskuupäev kui ka välja Aegumiskuupäev kuupäevad on tulevikus, ei ole elektroonilised maksed võimalikud. Muud makseviisid on kättesaadavad ja pangakonto on aktiivne.  
13. Laiendage jaotist Seadistus.
14. Sisestage väärtus väljale Teksti kood.
    * Sellel väljal on määratud kood, mis kuvatakse saaja pangaväljavõttel.  
15. Sisestage väärtus väljale Teade pangale.
16. Tippige väärtus väljale Vahetuskursi viide.
    * See on mis tahes edaspidise või fikseeritud tähtajaga vahetuskursi viitenumber.  
17. Valige või sisestage väärtus väljal Valuuta.
    * Eelpäringute väljastamisel annab see jaotis ülevaate nende olekust (ootel või kinnitatud).  
18. Laiendage jaotist Aadress.
19. Laiendage jaotist Eelpäringud.
20. Laiendage jaotist Kontaktteave.
21. Sisestage väärtus väljale Telefon.
22. Sulgege leht.
23. Klõpsake nuppu Redigeeri.
24. Laiendage jaotist Makse.
25. Valige väljalt Pangakonto äsja loodud konto.
26. Klõpsake nuppu Salvesta.
    * Aadress võib pärineda pangagrupist, kui see on määratud, või võite selle siin lisada.  

