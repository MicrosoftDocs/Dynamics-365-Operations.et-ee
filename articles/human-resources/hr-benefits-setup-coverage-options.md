---
title: Katvuse suvandite loomine
description: Katvussuvandid rakenduses Microsoft Dynamics 365 Human Resources on kasutaja valitud soodustuse plaani või programmi katvuse tasemed.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9f67a97ec57bade840e1035c6011b94427a77c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055576"
---
# <a name="create-coverage-options"></a>Katvuse suvandite loomine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Katvussuvandid rakenduses Microsoft Dynamics 365 Human Resources on kasutaja valitud soodustuse plaani või programmi katvuse tasemed. Näiteks võivad katvussuvandid hõlmata suvandit **Ainult töövõtja** meditsiiniplaani jaoks või suvandit **2 × palk** elukindlustuse plaani jaoks. Kui see on määratletud, saate soodustuse kindlustussuvandeid uuesti kasutada. Saate siduda suvandi ühe või mitme plaaniga.

Kui katvuse valikud on määratud, lisage katvuse valikud soodustuse plaani tüübile. Plaani tüüp seostatakse seejärel soodustuse plaani või programmiga. Plaani tüübiga seostatud katvuse valikud on saadaval kõigile selle plaani tüübiga loodud plaanidele. 

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Katvuse valikud**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Katvuse valik** | Kordumatu katvuse valiku nimi. |
   | **Kirjeldus** | Katvuse valiku kirjeldus. |
   | **Planeerimise kood** | Katvuse koodid määravad minimaalsed ja maksimaalsed summad iga sobiva kaetud isiku tüübi jaoks. Katvuse kood näitab, kes on kaetud või plaani tüübile lubatud katvuse summa. Saate väljendada katvuse summat summana dollarites või protsendina. Näide:</br></br>- **EMP+1** – kvalifitseerumiseks peab töövõtjal olema üks sõltuv isik valitud (kui valitud on rohkem kui üks, siis need enam ei kvalifitseeru).</br></br>- **EMP+perekond** – kvalifitseerumiseks peab töövõtjal olema vähemalt kaks sõltuvat isikut valitud. |
   | **Maksimaalne arv** | Maksimaalne sõltuvate isikute arv. |
   | **Olek** | Katvuse valiku olek. Kui katvuse valiku olek on seatud passiivseks, ei saa plaani tüüpides katvuse valikut valida. |
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