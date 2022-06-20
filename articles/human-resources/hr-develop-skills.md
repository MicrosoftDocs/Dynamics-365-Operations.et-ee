---
title: Oskuste konfigureerimine
description: Saate jälgida oma töötajate oskusi rakenduses Dynamics 365 Human Resources. Samuti saate määrata oskused, mida on vaja konkreetse töö jaoks.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: acb632042cdb535bea0dd625531f22d284653294
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893754"
---
# <a name="configure-skills"></a>Oskuste konfigureerimine

> [!IMPORTANT]
> Selles artiklis märgitud funktsioon on praegu saadaval Inimressursside klientidele finants infrastruktuuris.  


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
