---
title: Põhivarade praagi likvideerimine
description: Selles teemas kirjeldatakse praagina likvideeritud põhivara kannete likvideerimise protsessi.
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 413847d350ca6b2bdd6153a598ea5b3f34a33818
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826271"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Põhivarade praagi likvideerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse praagina likvideeritud põhivara kannete likvideerimise protsessi. Kandetüübid, mida saab kõrvaldada, on ka vara soetamise ja kogunenud kulumi kanded ja muud põhivara kanded. Nende kannete likvideerimine mõjutab bilansikontosid, nagu soetamise korrigeerimine, kulumi korrigeerimine, ümberhindamise, üleshindamise ja allahindamise kontod.

| Kanne                                         | Deebet (Dr.) | Krediit (Cr.) |
|-----------------------------------------------------|-------------|--------------|
| Dr. Kogunenud kulum                        | X           |              |
| Cr. Põhivara kasum/kahjum                          |             | X            |
| Dr. Põhivara kasum/kahjum                          | X           |              |
| Cr. Põhivara soetamise kontod                 |             | X            |
| Dr. Põhivara kasum/kahjum (raamatupidamislik jääkväärtus \[NBV)\] | X           |              |
| Cr. Põhivara kasum/kahjum (NBV)                    |             | X            |

> [!NOTE]
> Soovitame teil teha tihedat koostööd ettevõtte finantsjuhi (CFO) või kontrollijaga, et tuvastada õiged kontod, mida tuleks kasutada iga kandetüübi puhul, ja samuti kinnitada, et likvideerimisprotsess ja selle loodud kanded värskendatakse nendel kontodel õigesti.

Enne põhivara praagina likvideerimist peate looma pearaamatukontod, mis on seotud vara soetamise väärtusega, jooksva aasta kulumiga, eelmiste aastate kulumiga ja vara NBV-ga. Põhivara kandetüübid on loetletud lehel **Põhivarade sisestusreeglid**. Valige **Põhivarad \> Seadistus \> Põhivarade sisestusreeglid** ja seejärel valige kiirkaardi **Likvideerimine** väljal ruudusliku kohal olev valik **Praak**. Järgneval joonisel kujutatakse põhivara kanndetüüpide loendit lehel **Põhivara sisestusreeglid**.


[![Vara likvideerimine praagina, joonis 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Järgmise näite puhul soetati põhivara 1. jaanuaril 2018 ja see kantakse maha 31. märtsil 2019.

- **Soetamise hind:** 24 000,00 USA dollarit (USD)
- **Tööiga:** Kaks aastat
- **Kulumiarvestusviis:** Lineaarne tööiga
- **Kulumi summa:** 1000,00 USD kuus

Põhivara NVB arvutatakse järgmist valemit kasutades.

Raamatupidamislik jääkväärtus = soetamise hind - kulum

Selles näites soetati põhivara ja amortiseeriti 15 kuuks, 2018. aasta jaanuarist kuni 2019. aasta märtsini. Seetõttu on vara NBV 9000,00 USD (24 000,00 USD – 15 000,00 USD).

[![Põhivara kulumiarvestuse näide](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Likvideerimise töölehe loomiseks avage **Põhivarad \> Töölehe kanded \> Põhivarade tööleht** ja seejärel valige Tegevuspaanil **Read**. Valige **Likvideerimine – praak** ja seejärel valige põhivara ID. Vara täielikuks likvideerimiseks ärge sisestage väärtust väljale **Deebet** ega **Kreedit**.

[![Põhivarade tööleht](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Põhivara praagina likvideerimise kanne muudab põhivara raamatu välja väärtusi järgmistel viisidel.

- Jaotises **Saldo** muudetakse välja **Olek** väärtuseks **Praagitud**.
- Jaotises **Väljastamine** muudetakse välja **Likvideerimise kuupäev** väärtuseks kuupäev, millal vara praagiti.

[![Põhivarade töölehe üksikasjad](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Järgmisel joonisel näidatakse põhivara saldot.

[![Põhivara saldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Järgmisel joonisel näidatakse postitatavat kupongi.

[![Arvestuslik jääkväärtus](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]