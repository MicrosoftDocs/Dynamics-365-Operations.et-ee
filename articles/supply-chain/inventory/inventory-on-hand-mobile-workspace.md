---
title: Vaba kaubavaru mobiilne tööruum
description: See artikkel annab teavet mobiilse laoseisu tööruumi kohta. See tööruum aitab saada alati ja kõikjal mobiilseid ülevaateid reserveeritud ning vabadest kaubavarudest.
author: yufeihuang
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yufeihuang
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d493164b754b86a9df9ce4dcf9df8b20eeb55c5c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859426"
---
# <a name="inventory-on-hand-mobile-workspace"></a>Vaba kaubavaru mobiilne tööruum

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

See artikkel annab teavet mobiilse **laoseisu tööruumi** kohta. See tööruum aitab saada alati ja kõikjal ülevaateid reserveeritud ning vabadest kaubavarudest.

See mobiilses tööruum on mõeldud kasutamiseks koos Rakenduse Finantsid ja toimingud (Dynamics 365) mobiilirakendusega.

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
Eeltingimused erinevad teie organisatsioonis juurutatud Supply Chain Managementi versiooni põhjal.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Eeltingimused, kui kasutate Supply Chain Managementi
Kui teie organisatsioonis on juurutatud Supply Chain Management, peab süsteemiadministraator avaldama mobiilse tööruumi **Vaba kaubavaru**. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>Eeltingimused, kui kasutate platvormivärskendust 3 või uuemat 
Kui teie organisatsioonis on juurutatud platvormivärskendus 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused. 

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
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Mobiilse tööruumi <strong>Vaba kaubavaru</strong> avaldamine.</td>
<td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laadige alla ja installige mobiilirakendus

Laadige alla ja installige finantside ja toimingute (Dynamics 365) mobiilirakendus:

-   [Androidi telefonide puhul](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone’idele](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logige mobiilirakendusse sisse

1.  Käivitage rakendus oma mobiilses seadmes.
2.  Sisestage Dynamics 365 URL.
3.  Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.
4.  Pärast sisselogimist kuvatakse teie ettevõtte jaoks saadaolevad tööruumid. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem ja teil on vaja mobiilsete tööruumide loendit uuendada.

    [![Tõmmake värskendamiseks.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Toote vaba kaubavaru vaatamine, kasutades mobiilset tööruumi Vaba kaubavaru

1.  Valige oma mobiilses seadmes tööruum **Vaba kaubavaru**.

2.  Valige **Kauba vaba kaubavaru kontrollimine**. Näete loendit toodetest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Mobiiliplatvorm](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
