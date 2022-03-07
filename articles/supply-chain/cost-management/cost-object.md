---
title: Kuluobjektid
description: Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse. Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse. Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d27e2dcfd8f70c8d4b0f2ae1254f3c4fce63bb4d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572165"
---
# <a name="cost-objects"></a>Kuluobjektid

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse. Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse. Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid.  

## <a name="cost-objects"></a>Kuluobjektid

Lehel **Kuluobjektid** on loetletud kõik toote puhul registreeritud kuluobjektid. Kuluobjektid määratletakse järgmistest allikatest pärinevate andmete põhjal.

-   Toode
-   Tootedimensioonigrupp
-   Laoala dimensiooni grupp
-   Jälgimisdimensioonigrupp

**Märkus.** Kuluobjekt tähistab ainult kuluelementi tüübiga **Otsene materjalikulu**. Kuluobjekt ja varuobjekt erinevad selle poolest, et kuluobjekt määratletakse finantsvarudele valitud varudimensioonidega. Näiteks on kaubal järgmine konfiguratsioon.

-   **Laoala:** füüsilised varud = jah, finantsvarud = jah
-   **Ladu:** füüsilised varud = jah, finantsvarud = ei
-   **Partii number:** füüsilised varud = jah, finantsvarud = ei

Järgmine tabel näitab, milline on kuluobjekt ja milline on varuobjekt.

| Objekti tüüp      | Kaubakood | Laoala | Ladu | Partii nr |
|------------------|-------------|------|-----------|-----------|
| Kuluobjekt      | x           | x    |           |           |
| Varuobjekt | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Kulude ja koguste kogunemine
-   Väärtus väljal **Väärtus** on järgmiste väärtuste summa.
    -   Füüsiline omahind
    -   Finantsiline omahind
    -   Korrigeerimised
-   Väärtus väljal **Kogus** on järgmiste väärtuste summa.
    -   Saadud
    -   Maha arvatud
    -   Sisestatud kogus
-   Väli **Keskmine ühikukulu** on arvutatud väli. Väärtuse arvutamiseks jagatakse väärtus **Väärtus** väärtusega **Kogus**.

**Märkus.** Parameetril **Kaasa füüsiline väärtus** pole eelnevatele arvutustele mingit mõju.

## <a name="additional-resources"></a>Lisaressursid

[Tootedimensioonigrupp](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[Laoala dimensiooni grupp](/dynamicsax-2012//storage-dimension-groups-form)

[Jälgimisdimensioonigrupp](/dynamicsax-2012//tracking-dimension-groups-form)

[Mis on uus või muudetud](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[Kulukirjed](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]