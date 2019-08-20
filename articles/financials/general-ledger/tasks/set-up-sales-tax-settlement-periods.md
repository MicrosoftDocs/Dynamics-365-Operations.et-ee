---
title: Saate häälestada käibemaksu tasakaalustusperioode.
description: Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862984"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Saate häälestada käibemaksu tasakaalustusperioode.

[!include [task guide banner](../../includes/task-guide-banner.md)]

Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu. Tasakaalustusprotsessi saab käitada konkreetse kuupäevavahemiku tasakaalustusperioodi puhul. Kõik tasakaalustusperioodiga seotud maksukoodid tasakaalustatakse. Seotud käibemaksuhalduri seadistamisest olenevalt sisestatakse maksukohustus kas hankija või pearaamatu kontole.



See ülesanne kasutab demoettevõtte USMF andmeid.



1. Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksu tasakaalustusperioodid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Tasakaalustusperiood.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige väljal Maksuhaldur, kellele tasakaalustusperioodi puhul loodud aruanded ja maksed saadetakse.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake väljal Maksetingimused otsingu avamiseks ripploendi nuppu.
    * Seotud käibemaksuhalduri saab seadistada kui hankija ja käibemaksu tasakaalustus loob avatud hankija arve. Maksetingimused määratlevad avatud hankija arve maksetähtaja.  
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake loendis valitud real olevat linki.
11. Valige tasakaalustusperioodi vahemike tüüp.
12. Sisestage perioodivahemiku ühikute arv perioodi kohta. Näiteks kvartalis on 3 kuud.
13. Märkige või tühjendage ruut Kasuta käibemaksu tasakaalustamiseks pakktöötlust.
    * Tasakaalustusperioodi tasakaalustusprotsessi saab töödelda taustal pakett-tööna. See on soovitatav suure hulga maksukannete puhul kuupäevavahemiku jooksul.  
    > [!NOTE]
    > Praegu puudub selle tugi Austrias, Belgias, Hispaanias, Itaalias, Jaapanis ja Hollandis.
14. Märkige või tühjendage Vastasmaksukannete loomise vältimise märkeruut.
    * Süsteem loob tasakaalustusprotsessi ajal vaikimisi vastasmaksukandeid, mis põhjustavad jõudlusprobleeme, kui perioodivahemikul on suur hulk maksukandeid. Märkige see märkeruut, et vältida vastasmaksukannete loomist.
15. Laiendage vahekaarti Perioodivahemikud.
16. Klõpsake vahekaarti Lisa.
17. Märkige loendis valitud rida.
18. Sisestage kuupäev väljale Alguskuupäev.
19. Sisestage kuupäev väljale Lõpukuupäev.
20. Klõpsake suvandit Uus perioodivahemik.
    * Kui esimene perioodivahemik on sisestatud, saab uusi perioode luua automaatselt. Vajaduse korral saate naasta ja uusi perioodivahemikke lisada.  
21. Sulgege leht.

