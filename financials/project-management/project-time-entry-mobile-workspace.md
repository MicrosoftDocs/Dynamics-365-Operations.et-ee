---
title: "Projekti ajakirje mobiilne tööruum rakendusele Dynamics 365 for Operations"
description: "See teema annab teavet projekti ajakirje mobiilse tööruumi kohta. See tööruum võimaldab kasutajatel sisestada ja säästa aega projektiga, kasutades oma mobiilset seadet."
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Mobiilse tööruumi projekti ajakirje

[!include[banner](../includes/banner.md)]

„[!include[banner](../includes/banner.md)]”


See teema annab teavet projekti ajakirje mobiilse tööruumi kohta rakendusele Microsoft Dynamics 365 for Operations. See tööruum võimaldab kasutajatel sisestada ja säästa aega projektiga, kasutades oma mobiilset seadet.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Projekti ajakirje mobiilse tööruumi ülevaade
---------------------------------------------------

Igapäevase töö käigus on projekti ressursid sageli objektil või reisimas. Mobiilne tööruum **Projekti ajakirje** võimaldab kasutajatel sisestada projekti puhul arveldatavat või mittearveldatavat aega nende valitud mobiilses seadmes. Nii saavad projekti ressursid registreerida ajakirjeid igal ajal ja igal pool. Samuti saavad nad vaadata juba registreeritud ajakirjeid. 

Konkreetsemalt pakub mobiilne tööruum **Projekti ajakirje** järgmisi funktsioone.

-   Mis tahes valitud kuupäeva puhul saate sisestada kindlale ülesandele kulutatud tundide arvu.
-   Saate otsida projekti nime või kliendi järgi, et leida projekt, mille kohta aega sisestada.
-   Saate määrata kulutatud aja kohta kategooria ja tegevuse.
-   Saate registreerida aja projekti puhul arveldatava või mittearveldatavana.
-   Soovi korral saate sisestada väliseid või sisemisi kommentaare.

Mobiilse tööruumi **Projekti ajakirje** juurutamiseks vaadake selle teema järgmisi jaotisi.

## <a name="prerequisites"></a>Eeltingimused
Enne mobiilse tööruumi **Projekti ajakirje** juurutamist veenduge, et teie süsteemiadministraator oleks täitnud järgmised eeltingimused.

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
<td>Kui teie organisatsioonis pole Dynamics 365 for Operations veel juurutatud, peaks süsteemiadministraator vaatama teemat <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operationsi demokeskkonna juurutamine</a>.</td>
</tr>
<tr class="even">
<td>Juurutatud peab olema KB 4018050.</td>
<td>Süsteemiadministraator</td>
<td>KB 4018050 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Projekti ajakirje</strong>. KB 4018050 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li>Laadima KB 4018050 alla Microsoft Dynamicsi elutsükliteenustest (LCS).</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudeleid <strong>ApplicationSuite</strong> ja <strong>ProjectMobile</strong>, ning seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Rakendama juurutatava paketi</a> teie Dynamics 365 for Operationsi süsteemi.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobiilne tööruum <strong>Projekti ajakirje</strong> tuleb avaldada Dynamics 365 for Operationsi mobiilirakenduses.</td>
<td>Süsteemiadministraator</td>
<td><ol>
<li>Käivitage oma brauseris rakendus Dynamics 365 for Operations.</li>
<li>Valige lehe <strong>Süsteemi parameetrid</strong> vahekaardil <strong>Mobiilsete tööruumide haldamine</strong> tööruum <strong>Projekti ajakirje</strong>.</li>
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
5.  Pärast sisselogimist näete oma ettevõtte jaoks saadaolevaid tööruume. Pange tähele, et teie süsteemiadministraator avaldab uue tööruumi hiljem. Võite mobiilsete tööruumide loendi värskendamiseks tõmmata.

[![Tõmmake värskendamiseks](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Aja sisestamine, kasutades projekti ajakirje mobiilset tööruumi
1.  Valige oma mobiilses seadmes tööruum **Projekti ajakirje**.
2.  Valige suvand **Ajakirje**. Kuvatakse praeguse nädala kalendrikuupäevad.
3.  Valige soovitud kuupäeva puhul suvandid **Toimingud** &gt; **Uus kirje**.
4.  Sisestage registreeritavate tundide arv.
5.  Valige ajakirje jaoks projekt. Näete loendit projektidest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Dynamics 365 for Operationsi mobiiliplatvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  Kui soovitud projekti pole loendis, valige suvand **Otsi**, et kasutada Dynamics 365 for Operationsis veebiotsingut. Saate otsida nime järgi või lülituda otsingule projekti nime või kliendi järgi.
7.  Valige kategooria. Näete loendit kategooriatest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Dynamics 365 for Operationsi mobiiliplatvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  Kui soovitud kategooriat pole loendis, valige suvand **Otsi**, et kasutada Dynamics 365 for Operationsis veebiotsingut. Saate otsida kategooria järgi või lülituda kategooria nime järgi otsingule.
9.  Valige tegevus. Näete loendit tegevustest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 kaupa, kuid arendaja saab seda arvu muuta. Lisateabe saamiseks peaksite arendajad vaatama teemat [Dynamics 365 for Operationsi mobiiliplatvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. Kui soovitud tegevust pole loendis, valige suvand **Otsi**, et kasutada Dynamics 365 for Operationsis veebiotsingut. Saate otsida tegevuse numbri järgi või lülituda otstarbe järgi otsingule.
11. Valige rea atribuut.
12. Valikuline: saate sisestada väliseid ja sisemisi kommentaare.
13. Valige suvand **Valmis**.






