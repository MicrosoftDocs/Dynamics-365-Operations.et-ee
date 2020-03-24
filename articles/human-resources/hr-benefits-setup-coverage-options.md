---
title: Katvuse suvandite loomine
description: Katvussuvandid rakenduses Microsoft Dynamics 365 Human Resources on kasutaja valitud soodustuse plaani või programmi katvuse tasemed, nagu meditsiiniplaani jaoks suvand Ainult töövõtja või elukindlustuse plaani jaoks 2 × palk.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092702"
---
# <a name="create-coverage-options"></a>Katvuse suvandite loomine

[!include [banner](includes/preview-feature.md)]

Katvussuvandid rakenduses Microsoft Dynamics 365 Human Resources on kasutaja valitud soodustuse plaani või programmi katvuse tasemed, nagu meditsiiniplaani jaoks suvand Ainult töövõtja või elukindlustuse plaani jaoks 2 × palk. Kui see on määratletud, siis on soodustuse katvuse valikud uuesti kasutatavad ja saate siduda valiku ühe või mitme plaaniga.

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
