---
title: "Kulujuhtimise mobiilne tööruum"
description: "See teema annab teavet Microsoft Dynamics 365 for Operationsi mobiilirakenduse jaoks saadaoleva kulujuhtimise mobiilse tööruumi kohta. See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal."
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
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 09383c24b0dd2ad61a836f6c8dc97f4389915772
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Kulujuhtimise mobiilne tööruum

[!include[banner](../includes/banner.md)]


See teema annab teavet Microsoft Dynamics 365 for Operationsi mobiilirakenduse jaoks saadaoleva kulujuhtimise mobiilse tööruumi kohta. See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Kulujuhtimise mobiilse tööruumi ülevaade
-------------------------------------------------

Mobiilne tööruum **Kulujuhtimine** annab kiire ülevaate kulukeskuste praegusest jõudlusest, võrreldes tegelikke kulusid eelarvestatud kuludega. Saate üksikute kuluelementide olekuid ka sügavuti uurida. 

Näiteks saab töövõtja kutse rahvusvahelisele konverentsile, kuid organisatsioon peab tasuma kõik reisikulud. Töövõtja küsib oma juhilt, kas ta saab konverentsil osaleda. Juht avab oma mobiiltelefonis kiiresti mobiilse tööruumi **Kulujuhtimine**, et näha, kas tal on töövõtja konverentsil osalemiseks olemas piisav eelarve.

### <a name="data-security"></a>Andmeturve

Mobiilses tööruumis **Kulujuhtimine** olevad andmed on kaitstud kasutaja identimisteabe kaudu. Kulukeskuse juhtidel on õigus näha vaid oma enda kulukeskuse andmeid. Juurdepääsu turbetaset hallatakse moodulis **Kuluarvestus**. 

Kuluarvestajad määratlevad mobiilse tööruumi **Kulujuhtimine** konfiguratsiooni moodulis **Kuluarvestus**. Kui tööruum on avaldatud mobiilirakenduses Microsoft Dynamics 365 for Operations, on see saadaval rakenduses. Seega saavad kõik organisatsiooni kulukeskuse juhid vaadata andmeid samas vormingus.

### <a name="actions-views-and-links"></a>Toimingud, vaated ja lingid

Mobiilne tööruum **Kulujuhtimine** rakendusele Microsoft Dynamics 365 for Operations võimaldab kasutada järgmisi toiminguid, vaateid ja linke.

-   **Tegevused**
    -   Paigutuse valimine sätte **Vali konfiguratsioon** kasutamisega.
    -   Sätte **Vali kuluobjekt** kasutamine kulukeskuste valimiseks, mille andmeid filtrida. **Märkus.** Loendis ilmuvad kulukeskused sõltuvad moodulis **Kuluarvestus** antud juurdepääsuõigustest.
-   **Vaated.** Olenevalt moodulis **Kuluarvestus** valitud toimingutest ja konfiguratsiooni häälestusest saate vaadata kaartidel järgmist teavet.
    -   Tegelik võrreldes eelarvega (praegune periood)
    -   Tegelik võrreldes parandatud eelarvega (praegune periood)
    -   Tegelik võrreldes eelarvega (eelmine periood)
    -   Tegelik võrreldes parandatud eelarvega (eelmine periood)
    -   Tegelik võrreldes eelarvega (aasta tänaseni)
    -   Tegelik võrreldes parandatud eelarvega (aasta tänaseni)

    Järgmised summad kuvatakse igal kaardil: tegelik, eelarve, hälve ja hälbe protsent.
-   **Lingid**
    -   Praeguse perioodi üksikasjad
    -   Eelmise perioodi üksikasjad
    -   Aasta tänaseni üksikasjad

    Lingi valimisel kuvatakse iga kuluelemendi kaart. Järgmised summad kuvatakse igal kaardil: tegelik, eelarve, eelarvehälve, eelarvehälbe protsent, parandatud eelarve, parandatud eelarvehälve ja parandatud eelarvehälbe protsent. 
    
    [![Kuluelemendi kaart ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Eeltingimused
Enne mobiilse tööruumi **Kulujuhtimine** juurutamist veenduge, et teie süsteemiadministraator oleks täitnud järgmised eeltingimused.

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
<td>Juurutatud peab olema Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuemaga.</td>
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
<td>Mobiilne tööruum <strong>Kulujuhtimine</strong> tuleb avaldada Dynamics 365 for Operationsi mobiilirakenduses.</td>
<td>Süsteemiadministraator</td>
<td><ol>
<li>Käivitage oma brauseris rakendus Dynamics 365 for Operations.</li>
<li>Valige lehel <strong>Süsteemiparameetrid</strong> suvand <strong>Mobiilsete tööruumide haldamine</strong>.</li>
<li>Valige tööruum <strong>Kuluobjekti ülevaade</strong> .</li>
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

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Kasutage oma kulukeskuse jõudluse vaatamiseks mobiilset tööruumi Kulujuhtimine
1.  Valige oma mobiilses seadmes tööruum **Kulujuhtimine**.
2.  Valige suvand **Kuluobjekti juhtimine**.
3.  Valige suvand **Tegevused**.
4.  Kulujuhtimise paigutuse valimiseks valige **Konfiguratsiooni valimine**.
5.  Valige suvand **Valmis**.
6.  Valige suvand **Tegevused**.
7.  Valige suvand **Kuluobjekti valimine**, et valida kulukeskused, millele on teile juurdepääs antud.
8.  Valige suvand **Valmis**.
9.  Kulukeskuse üldise jõudluse vaatamine.
10. Valige link **Praeguse perioodi üksikasjad**.
11. Saate vaadata üksikute kuluelementide jõudlust.
12. Samuti saate otsida kindlaid kuluelemente.





