---
title: "Vaba kaubavaru mobiilne tööruum"
description: "See teema annab teavet vaba kaubavaru mobiilse tööruumi kohta. See tööruum aitab saada alati ja kõikjal mobiilseid ülevaateid reserveeritud ning vabadest kaubavarudest."
author: Mirzaab
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: c54f6f12e47ae0a185a7918517c7fd601f457fa4
ms.contentlocale: et-ee
ms.lasthandoff: 12/01/2017

---

# <a name="inventory-on-hand-mobile-workspace"></a>Vaba kaubavaru mobiilne tööruum

[!include[banner](../includes/banner.md)]

See teema annab teavet **vaba kaubavaru** mobiilse tööruumi kohta. See tööruum aitab saada alati ja kõikjal ülevaateid reserveeritud ning vabadest kaubavarudest.

See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Ülevaade
Tavaliselt on ettevõtetel iga päev mitu laosaadetist ja sissetulekut. Need liikumised muudavad pidevalt vaba kaubavaru olekut. Mobiilne tööruum **Vaba kaubavaru** aitab näha ettevõtteülest vaba kaubavaru olekut, et saaksite enda valitud mobiilsel seadmel viimaseid ülevaateid varude andmetest. Olenemata sellest, kas töötate laos, ostu- või müügiosakonnas, tootmises või juhtkonnas või teil on muud rollid, pääsete vaba kaubavaru andmetele alati ja kõikjal juurde. 

Mobiilne tööruum annab kiire ülevaate vaba kaubavaru olekust kõigis asutustes. See võimaldab teil vaadata vaba kaubavaru kõigis asutustes, materjali praegusi reserveeringuid ja reserveerimata vaba kaubavaru. Saate vaba kaubavaru päringute esitamiseks sisestada ka kaubakoode ning teha olemasolevate toodete ja variantide filtreeritud otsingut. 

Konkreetsemalt pakub mobiilne tööruum järgmisi funktsioone.

-   Saate otsida tootekoodi või tootenime järgi tooteid, mille vaba kaubavaru olekut on vaja vaadata.
-   Valitud toodete puhul saate vaadata järgmisi andmeid.

    -   Vaba kaubavaru laoala järgi
    -   Vaba kaubavaru lao järgi
    -   Vaba kaubavaru asukoha järgi
    -   Vaba kaubavaru partii järgi (partii kaudu juhitavate toodete puhul)
    -   Vaba kaubavaru varude oleku järgi
    
-   Toodete vaba kaubavaru näidatakse järgmiselt.

    -   Füüsiliste varude järgi (see vaade kajastab kogu summat).
    -   Füüsiliste reserveeritud kaupade järgi (see vaade kajastab reserveeritud summat).
    -   Vabade füüsiliste varude järgi (see vaade kajastab vaba kogust, millel puuduvad reserveeringud).

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Eeltingimused Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni kasutamisel 
Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, peab süsteemiadministraator avaldama **vaba kaubavaru** mobiilse tööruumi. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

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
<td>Rakendage KB 4013633.</td>
<td>Süsteemiadministraator</td>

<td>KB 4013633 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Vaba kaubavaru</strong>. KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Mobiilse tööruumi <strong>Vaba kaubavaru</strong> avaldamine.</td>
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

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Toote vaba kaubavaru vaatamine, kasutades mobiilset tööruumi Vaba kaubavaru

1.  Valige oma mobiilses seadmes tööruum **Vaba kaubavaru**.

2.  Valige **Kauba vaba kaubavaru kontrollimine**. Näete loendit toodetest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Kui teie kaupa pole loendis, valige **Otsi lisa**. Otsige tootekoodi järgi või lülituge toote nime järgi otsimisse.

4.  Valige toode. Kui kaubal on pilt, siis kuvatakse see pilt.
5.  Tehke vaba kaubavaru oleku vaatamiseks üks järgmistest valikutest.

    -   Kuva vaba kaubavaru laoala järgi
    -   Kuva vaba kaubavaru lao järgi
    -   Kuva vaba kaubavaru asukoha järgi
    -   Kuva vaba kaubavaru partii järgi (partii kaudu juhitavate toodete puhul)
    -   Kuva vaba kaubavaru varude oleku järgi

    Toodete vaba kaubavaru näidatakse järgmiselt.
    -   Füüsiliste varude järgi (see vaade kajastab kogu summat).
    -   Füüsiliste reserveeritud kaupade järgi (see vaade kajastab reserveeritud summat).
    -   Vabade füüsiliste varude järgi (see vaade kajastab vaba kogust, millel puuduvad reserveeringud).

