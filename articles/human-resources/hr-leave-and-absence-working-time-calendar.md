---
title: Tööajakalendri loomine
description: Määratlege rakenduses Dynamics 365 Human Resources tööajakalender, pühad ja mittetöised ajad.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 54aa85acb43c1e9a474bea9996c72c7e7017c245
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068915"
---
# <a name="create-a-working-time-calendar"></a>Tööajakalendri loomine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduse Dynamics 365 Human Resources tööajakalender kuvab päevad ja tunnid, mil töövõtjad teie organisatsioonis töötavad. Kui töötaja esitab vaba aja taotluse, ei pea nad puhkuste ja kinniolekuaegade pärast muretsema.

Vaba aja taotluste sujuvamaks muutmiseks konfigureerige järgmised üksused oma organisatsiooni jaoks.

- Tööajakalender
- Pühad ja kinniolekuajad
- Mittetöötamise aeg

Saate tööajakalendri seadistamisel lisada vähemalt kaks üksust. Lisaks saate neid eraldi konfigureerida või uuendada.

## <a name="set-up-a-working-time-calendar"></a>Tööajakalendri seadistamine

Seadistage vähemalt üks tööajakalender, mis kuvab teie töötamise päevad ja tunnid. Kui teil on asukohad mitmes riigis ja regioonis, võite soovida seadistada tööajakalendri iga piirkonna jaoks.

1. Valige lehel **Organisatsiooni haldus** suvand **Kalendrid**.

2. Valige suvand **Uus** ja sisestage oma kalendri nimi ning kirjeldus.

3. Jaotises **Loomissuvandid** valige oma organisatsiooni tööpäevad ja sisestage tööajad. 
   - Puhkuse või kinniolekuaja lisamiseks valige nupp **Lisa** suvandi **Pühad ja kinniolekuajad** kõrval.
   - Mittetöötamise aja (nt lõunad või pausid) lisamiseks valige käsk **Lisa** jaotises **MITTETÖÖTAMISE AEG** ja sisestage nimi ning ajavahemik.

4. Jaotises **Päevad** valige suvand **Loo**, et luua kalendrisse päevad. Sisestage kalendri kuupäevavahemik ja valige seejärel suvand **Loo päevad**.

5. Töögraafikute lisamiseks valige suvandis **Töögraafik** käsk **Lisa** ja sisestage iga töögraafiku ajad.

## <a name="configure-holidays-and-closures"></a>Pühade ja kinniolekuaegade konfigureerimine

Saate pühasid ja kinniolekuaegu lisada või muuta tööajakalendris eraldi.

1. Valige lehel **Organisatsiooni haldus** suvand **Pühad ja kinniolekuajad**.

2. Valige suvand **Uus** ja sisestage püha või kinniolekuaja nimi ja kuupäev.

## <a name="configure-non-work-time"></a>Mittetöötamise aja konfigureerimine

Saate mittetöötamise aegu lisada või muuta tööajakalendris eraldi.

1. Valige **lehel Organisatsiooni administreerimine** käsk **MITTETÖÖAEG**.

2. Valige suvand **Uus** ja sisestage mittetöötamise aja nimi ja ajavahemik.

Kui olete kuvanud puhkuste ja puudumiste riigipühade korrigeerimiste eelvaatefunktsiooni, kasutab rakendus Human Resources pühasid ja kinnioleku kuupäevasid, et kalendris registreeritud töövõtjate reguleerimiseks määrata päevade arv.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
- [Puhkuste ja puudumiste tüüpide konfigureerimine](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
