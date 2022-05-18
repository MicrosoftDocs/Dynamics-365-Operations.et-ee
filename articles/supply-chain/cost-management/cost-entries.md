---
title: Kulukirjed
description: Sellese artiklis antakse teavet kulukirjete ja nende loomise aja kohta. Kulukirje on kirje, mis registreerib antud sündmuse koguse ja kulu.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07e0e5f2e579d81fc96e1e03a2c63aea4c5c956f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673266"
---
# <a name="cost-entries"></a>Kulukirjed

[!include [banner](../includes/banner.md)]

Sellese artiklis antakse teavet kulukirjete ja nende loomise aja kohta. Kulukirje on kirje, mis registreerib antud sündmuse koguse ja kulu.

Kulukanded on laokannete koondsummad, mis salvestatakse aktiivsetel finantsvarude dimensioonidel.

## <a name="examples"></a>Näited
### <a name="example-1-no-cost-entries-are-created"></a>Näide 1: kulukirjeid pole loodud

Registreeritakse üleviimistöölehe sündmus. Sündmus edastab ühe kauba A ühiku asukohast A asukohta B. Asukoha varude dimensiooni ei arvestata kuluobjekti osaks. Seetõttu loob sündmus kaks laokannet ja mitte ühtegi kulukirjet.

### <a name="example-2-cost-entries-are-created"></a>Näide 2: luuakse kulukirjed

Registreeritakse üleviimistöölehe sündmus. Sündmus edastab ühe kauba A ühiku laoalalt 1 laoalale 2. Laoala varude dimensioon arvestatakse kuluobjekti osaks. Seetõttu loob sündmus kaks laokannet ja kaks kulukirjet.

### <a name="example-3-one-cost-entry-is-created"></a>Näide 3: luuakse üks kulukirje

Ostutellimusele registreeritakse toote sissetuleku sündmus. Sündmus registreerib 100 kauba A ühikut ühiku hinnaga 10.00 USA dollarit (USD). Kuna kaup A kasutab varude halduse eesmärgi jälgimiseks seerianumbrit, luuakse igale vastu võetavale kaubale kordumatu seerianumber. Seetõttu loob sündmus 100 laokannet ja ühe kulukirje.

## <a name="cost-entries-page"></a>Kulukirjete leht
Uus leht **Kulukirjed** võimaldab vaadata ja juhtida koguste ja kulude registreerimist. See leht täiendab lehti **Laokanne** ja **Lao tasakaalustus**. Sündmuse kirjed registreeritakse kronoloogilises järjekorras. Seetõttu on võimalik konkreetse sündmuse või kõigi dokumendiga seotud sündmuste kogunenud kulusid kiiresti leida ja juhtida. Siin on näide.

-   Kaubale A registreeritakse toote sissetuleku sündmus. Vastu võetakse sada ühikut ühiku hinnaga 10.00 USA dollarit.
-   Mõni päev pärast arvesündmuse registreerimist suureneb kulu 11.00 USA dollarini. Seetõttu on kogusumma 1100 USA dollarit. Luuakse teine kanne, mis kajastab 100 USA dollari suurust vahet.
-   Mõni päev hiljem registreeritakse ostutellimusel lisatasu 15.00 USA dollarit transpordikulu katteks.

| Kanne | Kuupäev       | Viide      | Kood | Saatepartii ID  | Kogus | Summa  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01-01-2015 | Ostutellimus | 100001 | 0000101 | 100,00   | 1000.00 |
| 00002   | 20-01-2015 | Ostutellimus | 100001 | 0000101 |          | 100,00  |
| 00003   | 31-01-2015 | Korrigeerimine     | 100001 | 0000101 |          | 15,00   |

Lehel **Kulukirjed** saab filtreerida dokumendi ID ja dokumendi kuupäeva alusel. 

> [!NOTE]
> Kulukeskused on saadaval ainult [kuluobjektide](cost-object.md) või väljastatud toodete puhul.

## <a name="additional-resources"></a>Lisaressursid

[Kuluobjektid](cost-object.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]