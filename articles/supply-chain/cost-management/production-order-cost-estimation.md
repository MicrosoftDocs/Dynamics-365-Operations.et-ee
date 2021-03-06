---
title: Tootmistellimuse kulu hindamine
description: Selles artiklis antakse teavet tootmiskulude hindamise kohta. Tootmiskulude hinnang varustab teid kauba tootmiseks planeeritud tootmistellimuse koguse kavandatud materjali ja võimsuse tarbimiskuludega.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59b93b41b74bd3f4cc480c8e60e8c69b25e40e51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830240"
---
# <a name="production-order-cost-estimation"></a>Tootmistellimuse kulu hindamine

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet tootmiskulude hindamise kohta. Tootmiskulude hinnang varustab teid kauba tootmiseks planeeritud tootmistellimuse koguse kavandatud materjali ja võimsuse tarbimiskuludega. 

Pärast tootmistellimuse loomist tuleb hinnata tootmiskulusid. Eesmärgiks on hinnata tootmisprotsessi kauba ja protsessi tarbimist, sest neid hinnanguid kasutatakse järgnevate planeerimiste ja tootmisprotsesside alusena.

## <a name="production-cost-estimation"></a>Tootmiskulude hindamine
Tootmiskulude hinnangud põhinevad järgmisel teabel.

-   Tootmistellimuse kogus
-   Tootmise koosluse komponendid
-   Tootmisprotsessi operatsioonid
-   Komponentidele ja operatsioonidele rakenduvad kaudsed kulud
-   Aktiivsed kuluandmed arvutamise kuupäeva seisuga

Kui tootmiskoosluses on fiktiivne rea kaup, kajastavad kalkulatsioonid fiktiivse kauba komponente ja protsessitoiminguid. Hinnangulist toimingut võib kasutada hinnanguliste kulude ümberarvutamiseks, nii et need kajastavad uuendatud teavet. Näiteks võib uuendatud teabeks olla muudatused tootmistellimuse koguses, tootmiskoosluse komponendid, tootmisprotsessi protsessitoimingud, kaudsed kulud, mis kohanduvad neile komponentidele ja operatsioonidele või aktiivsed kuluandmed ümberarvutuse kuupäevana. Eeldatava omahinna arvutused pakuvad ka tootmiskauba müügihinda, mis põhineb kulupõhisel hinnalisandil. Eeldatava omahinna arvutused võivad valikuliselt kohanduda viitetellimustele, mis kajastavad muid tootmistellimusi, mis on lingitud tootmistellimusele.

## <a name="view-the-estimated-costs"></a>Eeldatavate omahindade vaatamine
Pärast hinnangu käivitamist saate vaadata tulemusi lehel **Hinnakalkulatsioon**. Hinnang kalkuleerib järgmised väärtused.

-   **Tootmiskulu** – tootmiskulu on hinnangu ülemine rida. See näitab tootmistellimuse käitamise kogukulu ja tootmise täielikku müügihinda. See on kõigi hinnangu kuluridade summa.
-   **Protsessi või ressursi kulud** – protsessi või ressursi kulud on tootmisoperatsioonide kulud. Need sisaldavad selliste elementide kulusid nagu seadistusaeg, käitusaeg ja üldkulud.
-   **Materjalikulud** – materjalikulud on kauba tootmiseks nõutavate koosluse komponentide kulud ja hinnad. Need kulud on eelnevalt kehtestatud ja süsteemi sisestatud.

## <a name="other-uses-of-cost-estimation"></a>Kuluhinnangu muud kasutused
Kuluhinnang annab ka järgmist teavet:

-   selgitavad hinnapakkumised,
-   tellimuse tulususe hinnangud,
-   toormaterjali kasutamise hinnangud,
-   eelmiste toodete kuluandmete võrdluse,
-   eelarve ja prognoosi teabe,
-   kindla kulu säilitamiseks vajaliku tootmismahu hinnangu.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]