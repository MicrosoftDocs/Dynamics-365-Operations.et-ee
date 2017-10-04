---
title: Kuluobjektid
description: "Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse. Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse. Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 823d3edd106925339607d01fbf5f1921b85ff244
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="cost-objects"></a>Kuluobjektid

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse. Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse. Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid.  

<a name="cost-objects"></a>Kuluobjektid
------------

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

<a name="see-also"></a>Vt ka
--------

[Tootedimensioonigrupp](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Laoala dimensiooni grupp](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Jälgimisdimensioonigrupp](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Mis on uus või muudetud](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)

[Kulukirjed](cost-entries.md)



