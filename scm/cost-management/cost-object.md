---
title: Kuluobjektid
description: "Selles artiklis antakse teavet kuluobjektide kohta ja selgitatakse, kuidas kulusid ja koguseid akumuleeritakse. Kuluobjekt on üksus, mille jaoks kulusid ja koguseid akumuleeritakse. Kuluobjekt võib olla toode või tootevariant, näiteks laadi või värvi variandid."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 42d7ba8a41840024dc16df6863ba5eabd9c37c09
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


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

[Mida on Microsoft Dynamics AX-is uut või mis on muutunud?](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

[Kulukirjed](cost-entries.md)




