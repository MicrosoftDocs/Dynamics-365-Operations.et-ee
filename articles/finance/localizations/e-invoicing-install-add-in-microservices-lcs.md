---
title: Lifecycle Servicesi mikroteenuste lisandmooduli installimine
description: See artikkel selgitab, kuidas installida elektroonilise arvelduse lisandmooduli elutsükli Microsoft Dynamics teenustes (LCS).
author: gionoder
ms.date: 07/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 849d450ddb538e83a4aa6375fc99c705af154c61
ms.sourcegitcommit: 7a03b336d3c1c90770cc9913668c476e34ebf24a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/29/2022
ms.locfileid: "9208983"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Lifecycle Servicesi mikroteenuste lisandmooduli installimine

[!include [banner](../includes/banner.md)]

Elektroonilise arveldamise teenuse Microsoft Dynamics autentimine nõuab, et registreerite oma 365 Dynamics 365 Supply Chain Management Microsoft Dynamics Finantsid või keskkonna teenuste platvormil, installides lisandmooduli oma keskkonna jaoks elutsükli teenustes (LCS).

Keskkonna registreerimiseks järgige neid samme.

1. Logige oma LCS-i kontole sisse.
2. Projekti armatuurlaudal valige LCS-projekt.
2. Valige projektis **Keskkonnad** armatuurlaual oma juurutatud keskkond. Teie valitud keskkond peab töötama.
3. **Power Platform Valige vahekaardil** Integratsioon jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.
4. Valige **Elektrooniline arveldamine**.
5. Väljale **AAD-rakenduse ID** sisestage **091c98b0-a1c9-4b02-b62c-7753395ccabe**. See väärtus ei muutu. Kontrollige, et sisestate ainult globaalselt kordumatu ID (GUID). Ärge lisage muid sümboleid (nt tühikud, komad, perioodid või jutumärgid).
6. Sisestage väljale **AAD rentniku ID** oma Azure'i tellimuse konto ID. Teie Azure Active Directory määratud rentnik Azure AD peaks olema sama rentnik, mida kasutatakse regulatiivse konfiguratsiooni teenuses (RCS).
7. Vaadake üle tingimused ja märkige seejärel ruut.
8. Valige **Installi**. Mõne minuti pärast peaks olek **Installimine** muutuma olekuks **Installitud**. Võimalik, et peate lehekülge värskendama, et seda muudatust näha.

Elektrooniline arveldus on nüüd kasutamiseks valmis.

> [!NOTE]
> Ettevõtetel on tavaliselt mitu finants- või tarneahela halduskeskkonda. Need keskkonnad hõlmavad tootmiskeskkondasid, kasutaja kinnitamiskatse (UAT) keskkondi ja arenduskeskkondasid (box). Peate lõpule viima eelneva protseduuri kõigi keskkonnate puhul, mida soovite elektroonilise arveldamisega ühendada.
