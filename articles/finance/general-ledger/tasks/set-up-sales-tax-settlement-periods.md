---
title: Käibemaksu tasakaalustusperioodide häälestamine
description: See artikkel selgitab, kuidas seadistada käibemaksu tasakaalustusperioode Dynamics 365 Finances.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f8514494b5d3534fc236def817df0d58fe80d70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846679"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Käibemaksu tasakaalustusperioodide häälestamine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas seadistada käibemaksu tasakaalustusperioode. Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu. Tasakaalustusprotsessi saab käitada konkreetse kuupäevavahemiku tasakaalustusperioodi puhul. Kõik tasakaalustusperioodiga seotud maksukoodid tasakaalustatakse. Seotud käibemaksuhalduri seadistamisest olenevalt sisestatakse maksukohustus kas hankija või pearaamatu kontole.

See ülesanne kasutab demoettevõtte USMF andmeid.

1. Minge > **käibemaksu > käibemaksu > käibemaksu tasakaalustusperioodidele**.
2. Valige suvand **Uus**.
3. Sisestage välja **Tasakaalustusperiood** väärtus.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige väljal **Maksuhaldur** käibemaksu haldur, kellele tasakaalustusperioodi puhul loodud aruanded ja maksed saadetakse.
6. Otsige loendist ja valige soovitud kirje.
7. Valige väljas **Maksetingimused** soovitud kirje rippmenüüst. Seotud käibemaksuhalduri saab seadistada kui hankija ja käibemaksu tasakaalustus loob avatud hankija arve. Maksetingimused määratlevad avatud hankija arve maksetähtaja.  
8. Valige tasakaalustusperioodi vahemike tüüp.
9. Sisestage perioodivahemiku ühikute arv perioodi kohta. Näiteks kvartalis on 3 kuud.
10. Märkige või tühjendage ruut **Kasuta käibemaksu tasakaalustamiseks pakktöötlust**. Tasakaalustusperioodi tasakaalustusprotsessi saab töödelda taustal pakett-tööna. See on soovitatav suure hulga maksukannete puhul kuupäevavahemiku jooksul.
11. Märkige või tühjendage märkeruut **Vastasmaksukannete loomise ennetamine**. Süsteem loob tasakaalustusprotsessi ajal vaikimisi vastasmaksukandeid, mis põhjustavad jõudlusprobleeme, kui perioodivahemikul on suur hulk maksukandeid. Märkige see märkeruut, et vältida vastasmaksukannete loomist.
12. Laiendage vahekaarti **Perioodivahemikud**.
13. Valige **Lisa**.
14. Sisestage kuupäev välja **Alguskuupäev** uuele reale.
15. Sisestage kuupäev väljale **Lõppkuupäev**.
16. Valige **Uus perioodivahemik**. Kui esimene perioodivahemik on sisestatud, saab uusi perioode luua automaatselt. Vajaduse korral saate naasta ja uusi perioodivahemikke lisada.  
17. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
