---
title: Topeltkirjutuse häälestus teenustest Lifecycle Services
description: Selles teemas selgitatakse, kuidas häälestada topeltkirjutuse ühendust teenusest Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1fd15b5d664fead10949750678a2d3eab967af22
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781388"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Topeltkirjutuse häälestus teenustest Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas selgitatakse, kuidas häälestada topeltkirjutuse ühendust teenusest Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Eeltingimused

Integratsiooni peate lõpule Power Platform viima järgmistes teemades kirjeldatud viisil:

+ [Power Platform Integreerimine – lubage keskkonna juurutamisel](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Power Platform Integreerimine – lubage keskkonna juurutamisel](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

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

## <a name="linking-mismatch"></a>Mittevastavuse linkimine

On võimalik, et teie LCS-keskkond on lingitud ühe Dataverse eksemplariga, samas kui teie topeltkirjutuskeskkond on lingitud teise Dataverse eksemplariga. Selline seostamine võib põhjustada ootamatut käitumist ja see võib lõppeda andmete saatmisega valesse keskkonda. Topeltkirjutuse jaoks soovitatav keskkond on see, mis luuakse Power Platform integratsiooni ja pikaajalise integreerimise osana, see on ainus viis luua seos keskkondade vahel.

Kui teie keskkonnas on seostatav lahknevus, kuvab LCS hoiatuse teie keskkonna üksikasjade lehel, mis on sarnane lingile "Microsoft tuvastas, et teie keskkond on topeltkirjutuse kaudu lingitud integratsioonis määratud erinevasse sihtkohta, mis pole rakenduses Power Platform soovitatav":

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform integratsioonilink on vasta.":::

Kui ilmneb see tõrge, on teie vajadustest lähtuvalt kaks võimalust:

+ [Kahekordse kirjutamise keskkondade linkimise tühistamine ja uuesti linkimine (linkimise lähtestamine või muutmine)](relink-environments.md#scenario-reset-or-change-linking) nagu on määratud teie LCS-i keskkonna üksikasjade lehel. See on ideaalvalik, kuna saate seda käivitada ilma Microsoft`i toeta.  
+ Kui soovite linki topeltkirjutuses säilitada, võite paluda Microsoft`i tugiteenustelt abi, et muuta Power Platform integratsiooni, et kasutada olemasolevat Dataverse keskkonda vastavalt eelmises jaotises dokumenteeritud versioonile.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
