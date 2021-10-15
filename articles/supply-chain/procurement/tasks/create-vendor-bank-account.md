---
title: Hankija pangakonto loomine
description: Selles protseduuris kirjeldatakse, kuidas luua hankijale pangakontot.
author: Henrikan
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d24535035d26ca1313e293f9958b1b5000bb845
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575407"
---
# <a name="create-a-vendor-bank-account"></a>Hankija pangakonto loomine

[!include [banner](../../includes/banner.md)]

Selles protseduuris kirjeldatakse, kuidas luua hankijale pangakontot. Saate seda protseduuri kasutada demoandmete ettevõttes USMF.

1. Avage **Navigeerimispaan > Moodulid > Hanked > Hankijad > Kõik hankijad**.
2. Valige hankija, kellele tahate pangakontot luua ja seejärel klõpsake linki väljal **Hankija konto ID**.
3. Klõpsake **Toimingupaanil** suvandit **Hankija**.
4. Klõpsake **Pangakontod**.
5. Klõpsake **tegumiribal** valikut **Uus**.
6. Sisestage väärtus väljale **Pangakonto**. Seda ID-d kasutatakse hankija kirje pangakonto tuvastamiseks.  
7. Sisestage väärtus väljale **Nimi**.
8. Väljale **Pangagrupid** sisestage või valige väärtus.
9. Väljale **Protsessikoodi tüüp** valige sobiv variant. See on marsruudi valiku tüüp, mida kasutatakse rahvusvaheliste maksete puhul.  
10. Sisestage väärtus väljale **Pangakonto number**.
11. Sisestage väärtus väljale **SWIFT-kood**.
12. Sisestage väärtus väljale **IBAN**.
    - IBAN-number peab olema õiges vormingus. Näiteks võite kasutada numbrit DE89370400440532013000.  
    - Pangakonto olek on Aktiivne, kui aktiveerimiskuupäev on kätte jõudnud ja aegumiskuupäeva pole ületatud. See on aktiivne ka juhul, kui väljad Aktiveerimiskuupäev ja Aegumiskuupäev on mõlemad tühjad. Kui nii välja Aktiveerimiskuupäev kui ka välja Aegumiskuupäev kuupäevad on tulevikus, ei ole elektroonilised maksed võimalikud. Muud makseviisid on kättesaadavad ja pangakonto on aktiivne.  
13. Laiendage jaotist **Seadistus**.
14. Sisestage väärtus väljale **Tekstikood**. Sellel väljal on määratud kood, mis kuvatakse saaja pangaväljavõttel.  
15. Sisestage väärtus väljale **Sõnum pangale**.
16. Sisestage väärtus väljale **Vahetuskursi viide**. See on mis tahes edaspidise või fikseeritud tähtajaga vahetuskursi viitenumber.
17. Väljale **Valuuta** sisestage või valige väärtus. Eelpäringute väljastamisel annab see jaotis ülevaate nende olekust (ootel või kinnitatud).  
18. Laiendage jaotist **Aadress**.
19. Laiendage jaotist **Eelpäringud**.
20. Laiendage jaotist **Kontaktteave**.
21. Sisestage väärtus väljale **Telefon**.
22. Sulgege leht.
23. Klõpsake valikut **Redigeeri**.
24. Laiendage jaotist **Makse**.
25. Väljale **Pangakonto** valige äsja loodud konto.
26. Klõpsake valikut **Salvesta**. Aadress võib pärineda pangagrupist, kui see on määratud, või võite selle siin lisada.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]