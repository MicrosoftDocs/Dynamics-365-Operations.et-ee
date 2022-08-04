---
title: Topeltkirjutuse häälestus teenustest Lifecycle Services
description: See artikkel selgitab, kuidas seadistada topeltkirjutust ühenduse elutsükli Microsoft Dynamics teenustest (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a002bae22044ea10be30340a87a191305f6c6b92
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111966"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Topeltkirjutuse häälestus teenustest Lifecycle Services

[!include [banner](../../includes/banner.md)]



See artikkel selgitab, kuidas lubada topeltkirjutust elutsükli Microsoft Dynamics teenustest (LCS).

## <a name="prerequisites"></a>Eeltingimused

Kliendid peavad integratsiooni lõpule Power Platform viima, nagu on kirjeldatud järgmistes teemades:

- Kui te ei kasuta ja soovite oma Microsoft Power Platform finants- ja operatsioonide keskkondi laiendada platvormivõimaluste lisamisega, [Power Platform vt Integreerimine – Luba keskkonna juurutamise ajal](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Kui teil on juba Dataverse olemas keskkonnad Power Platform ja soovite need ühendada finants- ja operatsioonide keskkondadega, vaadake integreerimist [Power Platform – Lubage pärast keskkonna juurutamist](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Saate häälestada uute või olemasolevate keskkondade topeltkirjutust Dataverse.

Järgige neid samme LCS-i keskkonna üksikasjade lehel **topeltkirjutuse häälestamiseks** lehel:

1. Lehel **Keskkonna üksikasjad** laiendage jaotist **Power Platform Integratsioon** väljal.

2. Valige **topeltkirjutuse rakenduse** nupp.

    ![Power Platform integratsioon.](media/powerplat_integration_step2.png)

3. Tingimustega nõustumiseks valige märkeruut **Konfigureeri**.

4. Jätkamiseks valige **OK**.

5. Edenemist saate jälgida keskkonna üksikasjade lehte perioodiliselt värskendades. Seadistus kestab tavaliselt 30 minutit või vähem.  

6. Kui seadistus on lõpule viidud, teavitab teade teid, kas protsess õnnestus või kui see ebaõnnestus. Kui seadistus nurjus, kuvatakse sellega seotud tõrketeade. Enne järgmisele astmele teisaldamist peate parandama kõik tõrked.

7. Valige **Linkige Power Platform keskkonnaga** et luua link rakenduse Dataverse ja käesoleva keskkonna andmebaasiga. Seadistus kestab tavaliselt 5 minutit või vähem.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Link Power Platform keskkonda.":::

8. Kui linkimine on lõpetatud, kuvatakse hüperlink. Kasutage linki finantside ja toimingute keskkonnas topeltkirjutuse haldusalasse sisselogimiseks. Sealt saate seadistada üksuse vastendamised.

## <a name="linking-mismatch"></a>Mittevastavuse linkimine

Võimalik, et teie topeltkirjutuskeskkond on lingitud eksemplariga Dataverse, kui LCS ei ole seadistatud integreerimiseks Power Platform. Selline seostatav lahknevus võib põhjustada ootamatut käitumist. On soovitatav, et LCS-i keskkonna üksikasjad ühtiksid sellega, millega olete topeltkirjutuses ühendatud, nii et sama ühendust saaks kasutada ärisündmustes, virtuaalsetes tabelites ja lisandmoodulites.

Kui teie keskkonnas on seostatav lahknevus, kuvab LCS hoiatuse, mis sarnaneb järgmise näitega teie keskkonna üksikasjade lehel: "Microsoft Power Platform tuvastas, et teie keskkond on lingitud topeltkirjutuse kaudu teise kohta, kui on määratud integratsioonis, mis pole soovitatav."

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform integratsioonilink on vasta.":::

Kui saate selle hoiatuse, proovige ühte järgmistest lahendustest.

- Kui LCS-i Power Platform keskkond ei ole kunagi integreerimiseks häälestatud, Dataverse saate ühendada topeltkirjutuses konfigureeritud eksemplariga, järgides selle artikli juhiseid.
- Kui LCS-i keskkond on integreerimiseks juba seadistatud, peate topeltkirjutuse lingi tühistama ja selle LCS-i Power Platform [määratud keskkonnaga uuesti ühendama, kasutades stsenaariumi lähtestamist või linkimist](relink-environments.md#scenario-reset-or-change-linking).

Minevikus oli saadaval käsitsi toepileti valik, kuid see oli enne 1. valikut olemas.  Microsoft ei toeta enam käsitsi uuesti linkimise taotlusi tugiteenuste kaudu.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

