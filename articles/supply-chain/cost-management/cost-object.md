---
title: Kuluobjektid
description: Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse. Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse. Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e590322c75cfb2ad21236af56656061037a4b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426399"
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

<a name="additional-resources"></a>Lisaressursid
--------

[Tootedimensioonigrupp](https://technet.microsoft.com/library/aa499382.aspx)

[Laoala dimensiooni grupp](https://technet.microsoft.com/library/hh209317.aspx)

[Jälgimisdimensioonigrupp](https://technet.microsoft.com/library/hh209465.aspx)

[Mis on uus või muudetud](../../fin-and-ops/get-started/whats-new-changed.md)

[Kulukirjed](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]