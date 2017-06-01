---
title: "Vaba kaubavaru mobiilne tööruum"
description: "See teema annab teavet Microsoft Dynamics 365 for Operationsi mobiilirakenduse jaoks saadaoleva vaba kaubavaru mobiilse tööruumi kohta. See tööruum aitab saada alati ja kõikjal mobiilseid ülevaateid reserveeritud ning vabadest kaubavarudest."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Vaba kaubavaru mobiilne tööruum

[!include[banner](../includes/banner.md)]


See teema annab teavet Microsoft Dynamics 365 for Operationsi mobiilirakenduse jaoks saadaoleva vaba kaubavaru mobiilse tööruumi kohta. See tööruum aitab saada alati ja kõikjal mobiilseid ülevaateid reserveeritud ning vabadest kaubavarudest.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Vaba kaubavaru mobiilse tööruumi ülevaade
--------------------------------------------------

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
Enne mobiilse tööruumi **Vaba kaubavaru** juurutamist veenduge, et teie süsteemiadministraator oleks täitnud järgmised eeltingimused.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Roll</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Juurutatud peab olema Microsoft Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuemaga.</td>
<td>Süsteemiadministraator</td>
<td>Kui teie organisatsioonis pole Dynamics 365 for Operations veel juurutatud, peaks süsteemiadministraator nägema teadet <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operationsi demokeskkonna juurutamine</a>.</td>
</tr>
<tr class="even">
<td>Juurutatud peab olema KB 4013633.</td>
<td>Süsteemiadministraator</td>
<td>KB 4013633 (X\+\+ värskendus või metaandmete kiirparandus) sisaldab tarneahela haldamiseks nelja mobiilset tööruumi. KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li>Laadima KB 4013633 alla Microsoft Dynamicsi elutsükliteenustest (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Rakendama juurutatavat paketti</a> teie Microsoft Dynamics 365 for Operationsi süsteemile.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobiilne tööruum <strong>Vaba kaubavaru</strong> tuleb avaldada Dynamics 365 for Operationsi mobiilirakenduses.</td>
<td>Süsteemiadministraator</td>
<td><ol>
<li>Käivitage oma brauseris rakendus Dynamics 365 for Operations.</li>
<li>Valige lehel <strong>Süsteemiparameetrid</strong> suvand <strong>Mobiilsete tööruumide haldamine</strong>.</li>
<li>Valige tööruum <strong>Vaba kaubavaru</strong>.</li>
<li>Klõpsake nuppu <strong>Mobiilse tööruumi avaldamine</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operationsi mobiilirakenduse alla laadimine ja installimine
Laadige mobiilirakenduste poest alla mobiilirakendus Microsoft Dynamics 365 for Operations ja installige see.

-   Androidile: [Dynamics 365 for Operations Google Play Store’is](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone’ile: [Dynamics 365 for Operations iTunes apps store’is](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Logige sisse, et kasutada Dynamics 365 for Operationsi mobiilirakendust
1.  Käivitage rakendus oma mobiilses seadmes.
2.  Sisestage oma Dynamics 365 for Operationsi URL.
3.  Sisestage ettevõte, millesse soovite sisse logida. Näiteks sisestage **USMF**.
4.  Esmakordsel sisselogimisel palutakse teil sisestada oma Dynamics 365 for Operationsi konto kasutajanimi ja parool. Sisestage oma identimisteave.
5.  Pärast sisselogimist näete oma ettevõtte jaoks saadaolevaid tööruume. Pange tähele, et teie süsteemiadministraator avaldab hiljem uue tööruumi. Võite mobiilsete tööruumide loendi värskendamiseks tõmmata. 

    [![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Toote vaba kaubavaru vaatamine, kasutades mobiilset tööruumi Vaba kaubavaru
1.  Valige oma mobiilses seadmes tööruum **Vaba kaubavaru**.
2.  Valige **Kauba vaba kaubavaru kontrollimine**. Näete loendit toodetest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Dynamics 365 for Operationsi mobiiliplatvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
3.  Kui teie kaupa pole loendis, valige **Otsi lisa**, et kasutada Dynamics 365 for Operationsis veebiotsingut. Otsige tootekoodi järgi või lülituge toote nime järgi otsimisse.
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






