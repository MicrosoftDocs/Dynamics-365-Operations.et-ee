---
title: "Kulujuhtimise mobiilne tööruum"
description: "Teema annab teavet kulujuhtimise mobiilse tööruumi kohta. See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: dbedf75a6f61a9e2bc644056f0dd1e7499cedc42
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="cost-controlling-mobile-workspace"></a>Kulujuhtimise mobiilne tööruum

[!include[banner](../includes/banner.md)]

Teema annab teavet **kulujuhtimise** mobiilse tööruumi kohta. See tööruum võimaldab kulukeskuse juhtidel vaadata teavet kulukeskuse jõudluse kohta igal ajal ja kõikjal.

See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Ülevaade
Mobiilne tööruum **Kulujuhtimine** annab kiire ülevaate kulukeskuste praegusest jõudlusest, võrreldes tegelikke kulusid eelarvestatud kuludega. Saate üksikute kuluelementide olekut ka sügavuti uurida.

Näiteks saab töövõtja kutse rahvusvahelisele konverentsile, kuid organisatsioon peab tasuma kõik reisikulud. Töötaja küsib oma juhilt, kas ta saab konverentsil osaleda. Juht avab oma mobiiltelefonis kiiresti mobiilse tööruumi **Kulujuhtimine**, et näha, kas tal on töövõtja konverentsil osalemiseks olemas piisav eelarve.

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

    Lingi valimisel kuvatakse iga kuluelemendi kaart. Järgmised summad kuvatakse igal kaardil: tegelik, eelarve, eelarvehälve, eelarvehälbe protsent, parandatud eelarve, parandatud eelarvehälve ja parandatud eelarvehälbe protsent.
    
    [![Kuluelemendi kaart ](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Eeltingimused lahenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni 2017. aasta juuli värskenduse kasutamisel
Kui teie organisatsioonis on juurutatud Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni 2017. aasta juuli värskendus, peab süsteemiadministraator avaldama **kulujuhtimise** mobiilse tööruumi. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

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

<td>KB 4013633 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Kulujuhtimine</strong>. KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Rakendage juurutatav pakett</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Avaldage <strong>kulujuhtimise</strong> mobiilne tööruum.</td>
<td>Süsteemiadministraator</td>
<td>Vt jaotist <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilse tööruumi avaldamine</a>.</td>
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


