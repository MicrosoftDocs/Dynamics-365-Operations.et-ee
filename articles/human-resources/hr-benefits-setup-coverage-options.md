---
title: Katvuse suvandite loomine
description: See artikkel kirjeldab Microsofti laovarude valikuid Dynamics 365 Human Resources osaleja jaoks soodustusplaanis või programmis.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9c107e31e58ba1302cd02e2e82aa405dda0fdef
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337289"
---
# <a name="create-coverage-options"></a>Katvuse suvandite loomine


Kindlustuskaitse võimalused määravad kindlaks, kes peaks olema kaetud või kui palju kindlustusplaanis on kindlustuskaitset. Näiteks meditsiiniplaani puhul võib teil olla valik **Ainult töövõtja**, valik **Töövõtja + 1** ja valik **Pere**. Elukindlustuse puhul võite pakkuda katteid **1x palk** või **2x palk** ulatuses.

Pärast hüvitiste katvuse valikute määratlemist saate neid uuesti kasutada. Saate siduda suvandi ühe või mitme plaaniga.

> [!IMPORTANT]
> Kui katvuse valikud on määratud, lisage need soodustuse plaani tüübile. Plaani tüüp seostatakse seejärel soodustuse plaani või programmiga. Plaani tüübiga seostatud katvuse valikud on saadaval kõigile selle plaani tüübiga loodud plaanidele.

## <a name="create-coverage-options"></a>Katvuse suvandite loomine
1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Katvuse valikud**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Katvuse valik** | Kordumatu katvuse valiku nimi. |
   | **Kirjeldus** | Katvuse valiku kirjeldus. |
   | **Planeerimise kood** | Katvuse koodid määravad minimaalsed ja maksimaalsed summad iga sobiva kaetud isiku tüübi jaoks. Katvuse kood näitab, kes on kaetud või plaani tüübile lubatud katvuse summa. Saate väljendada katvuse summat summana dollarites või protsendina. Näide:<ul><li>**EMP+1** – kvalifitseerumiseks peab töövõtjal olema üks sõltuv isik valitud (kui valitud on rohkem kui üks, siis need enam ei kvalifitseeru).</li><li>**EMP+perekond** – kvalifitseerumiseks peab töövõtjal olema vähemalt kaks sõltuvat isikut valitud.</li></ul> |
   | **Maksimaalne arv** | Maksimaalne sõltuvate isikute arv. |
   | **Olek** | Katvuse valiku olek. Kui katvuse valiku olek on seatud **Passiivseks**, ei saa plaani tüüpides katvuse valikut valida. |
   | **Protsent** | Protsendi summa. See väli on aktiivne ainult juhul, kui väljal Katvuse kood on valitud % × palk. |
   | **Jagaja** | Jagaja, mida kasutatakse arvutamisel, kui valite katvuse koodi % × palk. |
   | **Miinimumprotsent** | Minimaalne protsent, kui valite katvuse koodi Protsent. |
   | **Maksimumprotsent** | Maksimaalne protsent, kui valite katvuse koodi Protsent. |

4. Jaotises **Isikliku kontakti sobivuse suvandid** lisage igale katvuse valikule sobiv isiklike kontaktide sobivuse suvand.

5. Vahekaardil **Iseteenindus** määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Luba töövõtja panuse summa määramine** | Määrab, kas lubada töötajatel soodustuste valimisel muuta soodustuste osamakse summat. Kui märgite selle ruudu, arvutab süsteem hüvitise plaani parameetrid, võttes aluseks osamakse summa, mille töötaja sisestab soodustuste iseteeninduses. |
   | **Luba töövõtja kindlustussumma määramine** | Määrab, kas lubada töötajatel soodustuste valimisel muuta soodustuste katvuse summat. Kui märgite selle ruudu, arvutab süsteem hüvitise plaani parameetrid, võttes aluseks katvuse summa, mille töötaja sisestab töövõtja iseteeninduses. |

6. Valige käsk **Salvesta**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
