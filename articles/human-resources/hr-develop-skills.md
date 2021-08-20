---
title: Oskuste konfigureerimine
description: Saate jälgida oma töötajate oskusi rakenduses Dynamics 365 Human Resources. Samuti saate määrata oskused, mida on vaja konkreetse töö jaoks.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a8025dd4000a3678e7f7eb7faebfa45852f0054570a2948dadbc21913c63f578
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732149"
---
# <a name="configure-skills"></a>Oskuste konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate jälgida oma töötajate oskusi rakenduses Dynamics 365 Human Resources. Samuti saate määrata oskused, mida on vaja konkreetse töö jaoks.

Oskused, mida saate jälgida, on muu hulgas:

- Kontrollioskus: oskus teiste töö järele valvata.
- Juhivõimed: võime juhtida töötajaid ja äridomeene.
- Kavandamine - Võime vaadata tulevikku, luua kujutlusi ja neid ellu viia.
- HTML: oskus kirjutada HTML-koodi.

Kui te pole oskuste tüüpe ja reitingumudeleid veel seadistanud, peate need enne oskuste loomist lisama.

Töötaja oskused saavad sisestada järgmised inimesed:

- Töötajad saavad enda jaoks töötaja iseteeninduses oskusi sisestada. Need oskused vajavad juhi kinnitust.
- Juhatajad saavad töötajate oskuseid sisestada. Saate luua töövoo, mis kinnitab need oskused automaatselt.

## <a name="create-a-skill-type"></a>Oskuse tüübi loomine

Oskuste tüübid on kategooriad, mille alla kuuluvad üksikud oskused nagu näiteks haldus või müük.

1. **Töötaja arenduse** tööruumis valige **Lingid**.

2. Valige **Kompetentsi häälestus** jaotises suvand **Oskuse tüübid**.

3. Valige suvand **Uus**.

4. Täitke järgmised väljad:

   - **Oskuse tüüp**: Sisestage nimi oskuse tüübi jaoks.
   - **Kirjeldus**: Sisestage oskuse tüübi jaoks kirjeldus.

5. Valige käsk **Salvesta**.

## <a name="create-a-rating-model"></a>Hindamismudeli loomine

Hindamismudelid aitavad hinnata isiku oskuste tegelikku taset, taset, mille poole isik peaks püüdlema, või töö jaoks vajaliku oskuse taset. Igale hindamismudelis olevale tasemele määratakse tegur.

1. **Töötaja arenduse** tööruumis valige **Lingid**.

2. Valige **Kompetentsi häälestus** jaotises suvand **Hindamismudelid**.

3. Valige suvand **Uus**.

4. Täitke järgmised väljad:

   - **Hinnang**: Sisestage hindamismudeli nimi, näiteks **Oskused**.
   - **Kirjeldus**: Sisestage hindamismudeli kirjeldus, näiteks **Oskuse hinnangud**.

5. Valige **Tasemed** jaotises väärtus **Uus**. Täitke iga lisatava taseme puhul järgmised väljad:

   - **Tase**: Sisestage taseme nimi.
   - **Kirjeldus**: Sisestage taseme kirjeldus.
   - **Tegur**: Sisestage teguri väärtus 0-9. Faktorid aitavad normaliseerida erinevaid hindamismudeleid kasutavate oskuste hindeid. Igal tasemel peab olema kordumatu tegur. Kõrgemate teguriväärtustega tasemed on hindamismudelis kaalukamad.

   Jätkake vajadusel tasemete lisamist. Saate sisestada kuni 10 hindamismudeli taset.

6. Valige käsk **Salvesta**.

## <a name="create-a-skill"></a>Oskuse loomine

Enne kui saate määrata isikule või tööle oskuse, luua oskuste kaardistamise otsingu või oskuste profiili, peate lehel **Oskused** sisestama teabe oskuse kohta. Iga oskuse puhul saate valida oskuse tüübi ja määramudeli.

1. **Töötaja arenduse** tööruumis valige **Lingid**.

2. Valige **Kompetentsi häälestus** jaotises suvand **Oskused**.

3. Valige suvand **Uus**.

4. Täitke järgmised väljad:

   - **Oskus**: Sisestage nimi oskuse tüübi jaoks.
   - **Kirjeldus**: Sisestage oskuse tüübi jaoks kirjeldus.
   - **Hindamine**: Valige hindamismudel, mida soovite selle oskuse jaoks kasutada.
   - **Oskuse tüüp**: Valige oskuste tüüpide loendist.

5. Valige käsk **Salvesta**.

## <a name="see-also"></a>Vt ka

[Sisestage oskused](hr-develop-enter-skills.md)<br>
[Oskuste kaardimine](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]