--- 
title: "Saate häälestada hankija arve poliitikaid."
description: "Hankija arvepoliitikad käivitatakse, kui sisestate hankija arve leheküljel Hankija arve ja avate lehekülje Hankija arve poliitika rikkumised."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f51c117da75a0382a38e75154ecef758f9a5d6c1
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vendor-invoice-policies"></a>Saate häälestada hankija arve poliitikaid.

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hankija arvepoliitikad käivitatakse, kui sisestate hankija arve leheküljel Hankija arve ja avate lehekülje Hankija arve poliitika rikkumised. Hankija arve töövoogu saate konfigureerida ka selliselt, et hankija arve poliitikad käivitatakse iga kord, kui sisestate arve töövoogu. 

Hankija arvepoliitikad ei kehti arvetele, mis on loodud arveregistris või arve töölehel. 

Arvete võrdlemise kinnitamisel ei kasutata hankija arvepoliitikaid, vaid selle sätted määratakse leheküljel Ostureskontro parameetrid.

Salvestamisel kasutatakse demoettevõtte USMF-i. Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli. Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Hankija arve poliitikate loomise ettevalmistus
1. Avage Ostureskontro > Seadistus > Ostureskontro parameetrid.
2. Klõpsake vahekaarti Arve kinnitamine.
3. Märkige või tühjendage ruut Arve päise oleku automaatne värskendus.
4. Klõpsake nuppu OK.
5. Valige suvand väljal Lahknevustega arvete sisestamine.
6. Sulgege leht.
7. Avage Ostureskontro > Poliitika seadistus > Hankija arvepoliitikad.
8. Klõpsake valikut Parameetrid.
9. Klõpsake btnAdd.
10. Sulgege leht.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Hankija arvete poliitika reegli tüüpide loomine
1. Avage Ostureskontro > Poliitika seadistus > Hankija arve poliitikareegli tüübid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Reegli nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake väljal Päringu nimi otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake nuppu Salvesta.
9. Sulgege leht.

## <a name="define-a-vendor-invoice-policy"></a>Hankija arvepoliitika määratlemine
1. Avage Ostureskontro > Poliitika seadistus > Hankija arvepoliitikad.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Laiendage või ahendage jaotist Poliitika organisatsioonid.
6. Valige puul Contoso Entertainment System USA.
7. Klõpsake vahekaarti Lisa.
8. Laiendage või ahendage jaotist Poliitika reeglid.
9. Klõpsake valikut Loo poliitika reegel.
10. Sisestage väärtus väljale Poliitika reegel.
11. Klõpsake käsku Filtreeri.
12. Klõpsake vahekaarti Lisa.
13. Märkige loendis valitud rida.
14. Klõpsake väljal Tabel otsingu avamiseks ripploendi nuppu.
15. Klõpsake loendis valitud real olevat linki.
16. Klõpsake väljal Tuletatud tabel otsingu avamiseks ripploendi nuppu.
17. Klõpsake loendis valitud real olevat linki.
18. Klõpsake väljal Väli otsingu avamiseks ripploendi nuppu.
19. Sisestage väärtus väljale Väli.
20. Sulgege leht.
21. Sisestage väärtus väljale Kriteeriumid.
22. Klõpsake nuppu OK.
23. Klõpsake nuppu OK.
24. Sulgege leht.
25. Sulgege leht.


