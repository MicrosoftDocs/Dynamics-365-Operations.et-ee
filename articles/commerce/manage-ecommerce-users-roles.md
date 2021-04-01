---
title: E-kaubanduse kasutajate ja rollide haldamine
description: See teema selgitab, kuidas anda kasutajatele juurdepääs teie Microsoft Dynamics 365 Commerce’i saidi autorluse keskkonnale.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a2235a43fd69adddeaba4c29305435db0fa39d64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255915"
---
# <a name="manage-e-commerce-users-and-roles"></a>E-kaubanduse kasutajate ja rollide haldamine


[!include [banner](includes/banner.md)]

See teema selgitab, kuidas anda kasutajatele juurdepääs teie Microsoft Dynamics 365 Commerce’i saidi autorluse keskkonnale.

Et aidata kontrollida kasutajate juurdepääsu ja anda kasutajatele luba konkreetsete ülesannete täitmiseks, kasutab saidi autorluse keskkond rakenduses Microsoft Azure Active Directory (Azure AD) loodud turvagruppe. Kõigepealt määrate autorluse keskkonnas igale rollile Azure AD-st uue või olemasoleva turvagrupi. Seejärel annate või tühistate individuaalsete kasutajate load, lisades need kasutajad vastavasse turvagruppi või eemaldades need turvarühmast.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Autorluse keskkonna rollide ülevaade

Rakenduse Dynamics 365 for Commerce autorluse keskkond toetab järgmisi rolle.

| Roll                 | Kirjeldus |
|----------------------|-------------|
| Süsteemiadministraator | Selle rolliga kasutajatel on kõik õigused kõigi tööriistade ja kõigi hinnangute ning arvustuste jaoks. Nad saavad luua ka saite. |
| Administraator   | Selle rolliga kasutajad omavad kõiki privileege kõikide antud saidi struktuuri tööriistadele ja RnR-ile. |
| Veebitootja         | Selle rolliga kasutajad saavad luua lehti, fragmente ja malle, laadida üles ja hallata varasid ning rikastada tooteid ja kategooriaid. |
| Lugeja               | Selle rolliga kasutajad saavad vaadata lehti, malle, varasid, fragmente, paigutusi ja sätteid, kuid ei tohi teha muudatusi. |
| RnR-i moderaator        | Selle rolliga kasutajad saavad hallata toote arvustusi. |

## <a name="system-administrator-role"></a>Süsteemiadministraatori roll

Rakenduse Dynamics 365 Commerce ettevalmistamisel Microsoft Dynamicsi teenuse Lifecycle Services (LCS) keskkonnas, küsitakse teilt rolli **Süsteemiadministraator** jaoks turvagrupi määramist. See roll rakendub seejärel automaatselt kõigile saitidele, mille konfigureeritavas keskkonnas loote. Selle rolli turvagruppi saab uuendada ainult LCS-is. Kõikide saitide lehel **Saidihaldus** ilmub see kirjutuskaitstuna ja ainult teavitaval eesmärgil.

## <a name="administrator-role"></a>Administraatori roll

Commerce’is uue saidi loomisel küsitakse teilt rolli **Administraator** jaoks turvagrupi määramist. Vaadake selles teemas eelnevalt toodud tabelit selle rolli antavate lubade ülevaateks.

## <a name="add-or-update-security-groups"></a>Turvagruppide lisamine või värskendamine

Pärast saidi loomist pääsevad selle saidi autoriseerimise keskkonnale juurde ainult kasutajad, kes on turvagruppides, mis on seotud rollidega **Süsteemiadministraator** ja **Administraator**. Kasutajatele rollide **Veebitootja**, **RnR-i moderaator** ja **Lugeja** määramiseks peate määrama nendele rollidele turvagrupid. Rollile turvagrupi lisamiseks või hetkel rollile määratud turvagrupi uuendamiseks toimige järgmiselt.

1. Avage sait, mida soovite uuendada.
1. Avage jaotises **Saidihaldus** leht **Turve**.
1. Valige muutmiseks roll.
1. Lisage rollidele turvagrupid või eemaldage rollidelt turvagrupid.

## <a name="additional-resources"></a>Lisaressursid

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)

[Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused](search-engine-optimization-considerations.md)

[Sisu turbepoliitika (CSP) haldamine](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]