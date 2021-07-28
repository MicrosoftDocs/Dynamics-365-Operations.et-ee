---
title: Topeltkirjutuse häälestus teenustest Lifecycle Services
description: Selles teemas selgitatakse, kuidas häälestada topeltkirjutuse ühendust teenusest Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e604e1491bbafa041fa3f52ad0f8b454c63d47de
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359359"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Topeltkirjutuse häälestus teenustest Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas selgitatakse, kuidas häälestada topeltkirjutuse ühendust teenusest Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Eeltingimused

Integratsiooni peate lõpule Power Platform viima järgmistes teemades kirjeldatud viisil:

+ [Power Platform Integreerimine – lubage keskkonna juurutamisel](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform Integreerimine – lubage keskkonna juurutamisel](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Juhised topeltkirjutuse Dataverse häälestamiseks

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

8. Kui linkimine on lõpetatud, kuvatakse hüperlink. Logige lingi abil sisse topeltkirjutuse haldusalasse Finance and Operations keskkonnas. Sealt saate seadistada üksuse vastendamised.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Juhised topeltkirjutuse Dataverse häälestamiseks

Olemasoleva keskkonna topeltkirjutuse Dataverse häälestamiseks peate looma Microsofti [tugipileti](../../lifecycle-services/lcs-support.md). Pilet peab sisaldama:

+ Teie Finance and Operations keskkonna ID.
+ Teie keskkonna nimi rakendusest Lifecycle Services.
+ Organisatsiooni Dataverse ID või Power Platform keskkonna ID Power Platform Halduskeskusest. Taotlege oma piletis, et ID oleks integratsiooniks kasutatav Power Platform eksemplar.

> [!NOTE]
> LCS-i abil ei saa keskkondade linkimist tühistada. Keskkonna linkimise tühistamiseks avage tööruum **Andmete integratsioon** keskkonnas Finance and Operations ja seejärel valige käsk **Tühista linkimine**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
