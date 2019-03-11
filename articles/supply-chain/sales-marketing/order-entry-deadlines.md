---
title: Tellimuse sisestamise tähtajad
description: See artikkel käsitleb tellimuse sisestamise tähtaegu. Tellimuse sisestamise tähtaeg on katkestusaeg, mis määratleb, kas kliendi tellimust käsitletakse (ja täidetakse) nii, nagu see oleks saadud jooksval päeval või järgmisel päeval.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 412ab5e2e411a93da2424cb8959b4270594bbf57
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308755"
---
# <a name="order-entry-deadlines"></a>Tellimuse sisestamise tähtajad

[!include [banner](../includes/banner.md)]

See artikkel käsitleb tellimuse sisestamise tähtaegu. Tellimuse sisestamise tähtaeg on katkestusaeg, mis määratleb, kas kliendi tellimust käsitletakse (ja täidetakse) nii, nagu see oleks saadud jooksval päeval või järgmisel päeval.

Paljudes ettevõtetes käsitletakse ainult enne teatud kellaaega vastu võetud müügitellimusi nii, nagu need oleksid vastu võetud sellel päeval. Pärast seda kellaaega vastu võetud tellimusi käsitletakse nii, nagu need oleksid vastu võetud järgmisel tööpäeval. Sellist tellimuste tähtaega nimetatakse tellimuse sisestamise tähtajaks.  

Tellimuse sisestamise tähtaegu kasutatakse sisendina tellimuse täitmisel. Nii aitavad need teil hallata klientide ootusi tellimuste tarnete kohta. Näiteks näevad kliendid, et kui esitavad teile tellimuse enne teatud kellaaega, kohustute neile kaubad tarnima samal päeval. Kui nad aga selle tähtaja ületavad, võivad nad eeldada saadetist alles järgmisel tööpäeval. Määrake tellimuse sisestamise tähtajad oma laovõimsuste ja kättetoimetaja graafikute järgi.  

Lehel **Tellimuse sisestamise tähtajad** saate määrata tellimuse sisestamise kellaajad kõigi nädalapäevade kohta. Pärast määratud kellaaegu vastu võetud tellimusi käsitletakse nii, nagu need oleksid vastu võetud järgmisel päeval. Vaikimisi on seadistatud aeg 23.59 (s.o üks minut enne vastava päeva keskööd). Saate muuta vaikimisi aegu nii, et need ühtiksid tegelike lähetus- või vastuvõtutähtaegadega.  

Saate määratleda tellimuse sisestamise tähtajad konkreetse kliendigrupi jaoks. Näiteks võite soovida, et konkreetse kliendigrupi tellimuse sisestamise tähtajad oleksid hilisemad kui teiste klientide puhul. Sellisel juhul määratlege esmalt grupid tellimuse sisestamise tähtajad lehel **Tellimuse sisestamise tähtajagrupid**. Seejärel määrake lehel **Kliendi** grupid klientidele.  

Kui teie ettevõte koosneb mitmest tegevuskohast, saate seadistada tellimuse sisestamise tähtajad iga tegevuskoha kohta. Kui tegevuskohad paiknevad erinevates ajavööndites, seadistatakse tellimuse sisestamise tähtajad iga tegevuskoha ajavööndis. Kui aga töötate müügitellimuste müügipakkumistega, teisendatakse tellimuse sisestamise tähtaeg teie ajavööndile lehel **Saadaolevad lähetus- ja vastuvõtukuupäevad**.  

Lehel **Aktiveeri tellimuse sisestamise tähtajakombinatsioonid** määratlege tegevuskohtade kombinatsioonid ja lubatud tellimuse sisestamise tähtajagrupid.

## <a name="example-order-entry-deadline"></a>Näide. Tellimuse sisestamise tähtaeg
Tellimuse sisestamise tähtaeg teisipäeviti on kell 16.00. Konkreetsel teisipäeval kell 17.00 proovite määrata lähetuskuupäevana tänase kuupäeva. (Võtke arvesse, et selles näites pole täitmisaega.) Kui ruut **Tarnekuupäeva kontrolli** on märgitud, kuvatakse hoiatus, et kuupäev on kehtetu. Hoiatus kuvatakse lehel **Saadaolevad lähetus- ja vastuvõtukuupäevad**, kus saate valida uued kuupäevad.

## <a name="example-different-order-entry-deadlines-per-site"></a>Näide. Erinevad tellimuse sisestamise tähtajad tegevuskohtade puhul
Teie ettevõte koosneb kahest saidist. Tegevuskohad paiknevad erinevates ajavööndites, nagu on näidatud järgmises tabelis.

| Sait A                      | Sait B                      |
|-----------------------------|-----------------------------|
| Kalifornia                  | Florida                     |
| Lääneranniku aeg | Idaranniku aeg |

Tegevuskohtadele A ja B on määratletud järgmised tellimuse sisestamise tähtajad.

| Nädalapäev             | A: tellimuse sisestamise tähtajad (Lääneranniku aeg) | B: tellimuse sisestamise tähtajad (Idaranniku aeg) |
|-----------------------------|--------------------------------|--------------------------------|
| Esmaspäev                      | 13.00                          | 14.00                          |
| teisipäev                     | 13.00                          | 14.00                          |
| kolmapäev                   | 13.00                          | 14.00                          |
| neljapäev                    | 13.00                          | 14.00                          |
| Reede                      | 13.00                          | 14.00                          |

Teie olete tellimuste töötleja Utah’s, kus ajavööndiks on mäestikupiirkonna aeg. See tähendab, et senikaua, kuni esitate tellimused tegevuskohale A enne 14.00 mäestikupiirkonna aja järgi ja tegevuskohale B enne 12.00 mäestikupiirkonna aja järgi, vastate mõlema tegevuskoha puhul tellimuse sisestamise tähtaegadele.  

Järgmine tabel näitab, kuidas on tellimuse sisestamise tähtajad tegevuskohtadele A ja B teisendatud mäestikupiirkonna ajale.

| Laoala A: lääneranniku aeg         | Laoala A: mäestikupiirkonna aeg        | Laoala B: idaranniku aeg           | Laoala B: mäesikupiirkonna aeg        |
|---------------------|--------------------|-----------------------|--------------------|
| 13.00               | 14.00              | 14.00                 | 12.00              |

**Märkus.** Kui kehtib suveaeg, korrigeeritakse selle järgi ka tellimuse sisestamise tähtaegu.

## <a name="example-same-order-entry-deadline-per-site"></a>Näide. Sama tellimuse sisestamise tähtaeg tegevuskoha kohta
Teie ettevõte koosneb kahest saidist. Tegevuskohad paiknevad erinevates ajavööndites, nagu on näidatud järgmises tabelis.

| Sait A                      | Sait B                      |
|-----------------------------|-----------------------------|
| Kalifornia                  | Florida                     |
| Lääneranniku aeg | Idaranniku aeg |

Tegevuskohtadele A ja B on määratletud järgmised tellimuse sisestamise tähtajad.

| Nädalapäev | Lääneranniku aeg ja idaranniku aeg |
|-----------------|-------------|
| Esmaspäev          | 13.00       |
| Teisipäev         | 13.00       |
| Kolmapäev       | 13.00       |
| Neljapäev        | 13.00       |
| Reede          | 13.00       |

Teie olete tellimuste töötleja Utah’s, kus ajavööndiks on mäestikupiirkonna aeg. See tähendab, et senikaua, kuni esitate tellimused tegevuskohale A enne 14.00 mäestikupiirkonna aja järgi ja tegevuskohale B enne 11.00 mäestikupiirkonna aja järgi, vastate mõlema tegevuskoha puhul tellimuse sisestamise tähtaegadele. 

Järgmine tabel näitab, kuidas on tellimuse sisestamise tähtajad tegevuskohtadele A ja B teisendatud mäestikupiirkonna ajale.

| Laoala A: lääneranniku aeg         | Laoala A: mäestikupiirkonna aeg        | Laoala B: idaranniku aeg           | Laoala B: mäestikupiirkonna aeg        |
|---------------------|--------------------|-----------------------|--------------------|
| 13.00               | 14.00              | 13.00                 | 11.00              |

**Märkus.** Kui kehtib suveaeg, korrigeeritakse selle järgi ka tellimuse sisestamise tähtaegu.

<a name="additional-resources"></a>Lisaressursid
--------

[Tarnegraafikud](delivery-schedules.md)



