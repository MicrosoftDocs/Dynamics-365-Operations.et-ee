---
title: Kulujuhtimise mobiilne tööruum
description: See artikkel annab teavet mobiilse kulude juhtimise tööruumi kohta. See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal.
author: AndersGirke
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d6d3fdcc0b0387a92f138b0ba7cf537f473b91a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069559"
---
# <a name="cost-controlling-mobile-workspace"></a>Kulujuhtimise mobiilne tööruum

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

See artikkel annab teavet mobiilse kulude **juhtimise tööruumi** kohta. See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal.

See mobiilses tööruum on mõeldud kasutamiseks koos finantside ja toimingute (Dynamics 365) mobiilirakendusega.

## <a name="overview"></a>Ülevaade
Mobiilne tööruum **Kulujuhtimine** annab kiire ülevaate kulukeskuste praegusest jõudlusest, võrreldes tegelikke kulusid eelarvestatud kuludega. Saate üksikute kuluelementide olekut ka sügavuti uurida.

Näiteks saab töövõtja kutse rahvusvahelisele konverentsile, kuid organisatsioon peab tasuma kõik reisikulud. Töötaja küsib oma juhilt, kas ta saab konverentsil osaleda. Juht avab oma mobiiltelefonis kiiresti mobiilse tööruumi **Kulujuhtimine**, et näha, kas tal on töövõtja konverentsil osalemiseks olemas piisavad eelarvevahendid.

### <a name="data-security"></a>Andmeturve
Mobiilses tööruumis **Kulujuhtimine** olevad andmed on kaitstud kasutaja identimisteabe kaudu. Kulukeskuse juhtidel on õigus näha vaid oma enda kulukeskuse andmeid. Juurdepääsu turbetaset hallatakse moodulis **Kuluarvestus**.

Kuluarvestajad määratlevad mobiilse tööruumi **Kulujuhtimine** konfiguratsiooni moodulis **Kuluarvestus**. Kui tööruum on mobiilirakenduses avaldatud, on see rakenduses saadaval. Seega saavad kõik organisatsiooni kulukeskuse juhid vaadata andmeid samas vormingus.

### <a name="actions-views-and-links"></a>Toimingud, vaated ja lingid
**Kulujuhtimise** mobiilne tööruum pakub järgmisi toiminguid, vaateid ja linke.

-   **Tegevused**

    -   Paigutuse valimine sätte **Vali konfiguratsioon** kasutamisega.
    -   Sätte **Vali kuluobjekt** kasutamine kulukeskuste valimiseks, mille andmeid filtrida.
    
        > [!NOTE]
        > Loendis ilmuvad kulukeskused sõltuvad moodulis **Kuluarvestus** antud juurdepääsuõigustest.

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

    Lingi valimisel kuvatakse iga kuluelemendi kaart. Järgmised summad kuvatakse igal kaardil: tegelik, eelarve, eelarvehälve, eelarvehälbe protsent, parandatud eelarve, parandatud eelarvehälve ja parandatud eelarvehälbe protsent.
    
    [![Kuluelemendi kaart.](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Eeltingimused Microsoft Dynamics 365 finantside kasutamisel
Kui teie organisatsioonis on juurutatud Finance, peab süsteemiadministraator avaldama mobiilse tööruumi **Kulujuhtimine**. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Eeltingimused, kui kasutate rakenduse versiooni 1611 platvormivärskendusega 3 või uuemat
Kui teie organisatsioonis on juurutatud versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused.

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

<td>KB 4013633 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Kulujuhtimine</strong>. KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Avaldage <strong>kulujuhtimise</strong> mobiilne tööruum.</td>
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

