---
title: "Mobiilse tööruumi projekti ajakirje"
description: "See teema annab teavet projekti ajakirje mobiilse tööruumi kohta. See tööruum võimaldab kasutajatel sisestada ja säästa aega projektiga, kasutades oma mobiilset seadet."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9bf79af6eea6f899158fc3c8d523587cb11c90ad
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="project-time-entry-mobile-workspace"></a>Mobiilse tööruumi projekti ajakirje

[!include [banner](../includes/banner.md)]

See teema annab teavet **projekti ajakirje** mobiilse tööruumi kohta. See tööruum võimaldab kasutajatel sisestada ja säästa aega projektiga, kasutades oma mobiilset seadet.

See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations. 

## <a name="overview"></a>Ülevaade
Igapäevase töö käigus on projekti ressursid sageli objektil või reisimas. Mobiilne tööruum **Projekti ajakirje** võimaldab kasutajatel sisestada projekti puhul arveldatavat või mittearveldatavat aega nende valitud mobiilses seadmes. Nii saavad projekti ressursid registreerida ajakirjeid igal ajal ja igal pool. Samuti saavad nad vaadata juba registreeritud ajakirjeid. 

Konkreetsemalt saavad kasutajad teha mobiilses tööruumis **Projekti ajakirje** järgmisi toiminguid.

-   Mis tahes valitud kuupäeva puhul saate sisestada kindlale ülesandele kulutatud tundide arvu.
-   Saate otsida projekti nime või kliendi järgi, et leida projekt, mille kohta aega sisestada.
-   Saate määrata kulutatud aja kohta kategooria ja tegevuse.
-   Saate registreerida aja projekti puhul arveldatava või mittearveldatavana.
-   Soovi korral saate sisestada väliseid või sisemisi kommentaare.

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Eeltingimused Microsoft Dynamics 365 for Finance and Operationsi kasutamisel
Kui teie organisatsioonis on juurutatud rakendus Microsoft Dynamics 365 for Finance and Operations, peab süsteemiadministraator avaldama **projekti ajakirje** mobiilse tööruumi. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Eeltingimused Microsoft Dynamics 365 for Operationsi versiooni 1611 platvormivärskendusega 3 või uuema kasutamisel
Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused. 

<table>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Roll</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Rakendage KB 4018050.</td>
<td>Süsteemiadministraator</td>
<td>KB 4018050 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Projekti ajakirje</strong>. KB 4018050 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looma juurutatava paketi</a>, mis sisaldab mudeleid <strong>ApplicationSuite</strong> ja <strong>ProjectMobile</strong>, ning seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Avaldage mobiilne tööruum <strong>Projekti ajakirje</strong>.</td>
<td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laadige alla ja installige mobiilirakendus

Laadige alla ja installige Dynamics 365 for Unified Operationsi mobiilirakendus.

-   [Androidi telefonidele](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse
1.  Käivitage rakendus oma mobiilses seadmes.
2.  Sisestage Dynamics 365 URL.
3.  Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
4.  Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.

[![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Aja sisestamine, kasutades projekti ajakirje mobiilset tööruumi
1.  Valige oma mobiilses seadmes tööruum **Projekti ajakirje**.
2.  Valige suvand **Ajakirje**. Kuvatakse praeguse nädala kalendrikuupäevad.
3.  Valige soovitud kuupäeva puhul suvandid **Toimingud** &gt; **Uus kirje**.
4.  Sisestage registreeritavate tundide arv.
5.  Valige ajakirje jaoks projekt. Loendis kuvatakse projektid, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateavet leiate teemast [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Kui teie projekti pole loendis, valige **Otsi**. Saate otsida nime järgi või lülituda otsingule projekti nime või kliendi järgi.
7.  Valige kategooria. Loendis kuvatakse kategooriad, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateavet leiate teemast [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Kui teie kategooriat pole loendis, valige **Otsi**. Saate otsida kategooria järgi või lülituda kategooria nime järgi otsingule.
9.  Valige tegevus. Loendis kuvatakse tegevused, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateavet leiate teemast [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Kui teie tegevust pole loendis, valige **Otsi**. Saate otsida tegevuse numbri järgi või lülituda otstarbe järgi otsingule.

11. Valige rea atribuut.
12. Valikuline: saate sisestada väliseid ja sisemisi kommentaare.
13. Valige suvand **Valmis**.

