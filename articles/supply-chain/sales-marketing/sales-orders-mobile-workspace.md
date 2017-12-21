---
title: "Müügitellimuste mobiilne tööruum"
description: "Teema annab teavet müügitellimuste mobiilse tööruumi kohta. See tööruum aitab teil olla oma müügitellimustega alati kõikjal kursis."
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
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 6a613d8b2ea1503b70efad7b14fb340faad0f62e
ms.contentlocale: et-ee
ms.lasthandoff: 12/01/2017

---

# <a name="sales-orders-mobile-workspace"></a>Müügitellimuste mobiilne tööruum

[!include[banner](../includes/banner.md)]

Teema annab teavet **müügitellimuste** mobiilse tööruumi kohta. See tööruum aitab teil olla oma müügitellimustega alati kõikjal kursis. 

See mobiilne tööruum on mõeldud kasutamiseks mobiilirakendusega Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Ülevaade
**Müügitellimuste** mobiilne tööruum võimaldab vaadata üksikasjalikku teavet iga müügitellimuse kohta. See teave hõlmab tellimuse olekut, kliendi kontaktteavet ja tellimuse vastuvõtja kontaktteavet. Mobiilne tööruum **Müügitellimused** annab müügitellimustest kiirülevaate. Saate vaadata kõiki müügitellimusi, müügitellimusi klientide kaupa või konkreetse müügitellimuse andmeid. 

Mobiilne tööruum pakub kahte vaadet, mis aitavad teil müügitellimusi põhjalikult analüüsida.

### <a name="view-all-sales-orders"></a>Kõigi müügitellimuste kuvamine
Selles vaates loetletakse kõik müügitellimused.

-   Saate soovitud müügitellimuste valimiseks kasutada järgmisi filtreid.

    -   Otsing müügitellimuse alusel
    -   Otsing kliendikonto järgi
    -   Otsing kliendi nime järgi
    -   Otsing oleku järgi
    -   Otsing väljastamisoleku järgi
    -   Otsing loomise kuupäeva ja kellaaja järgi
    
-   Pärast müügitellimuste valimist saate konkreetsete tellimuste andmeid vaadata. Täpsemalt saate vaadata järgmist teavet.

    -   Kliendi nimi ja aadressiandmed
    -   Müügitellimuse erinevad kuupäevad, nagu nõutav lähetuskuupäev ja kinnitatud lähetuskuupäev.
    -   Tellimuse vastuvõtja kontaktteave
    -   Kliendi kontaktandmed
    -   Tellimuse read
    -   Saadetised, mis näitavad, kuidas ja millal müügitellimus on teele pandud

### <a name="view-orders-for-a-customer"></a>Kliendi tellimuste kuvamine
Selles vaates on loetletud müügitellimused kliendi järgi.

-   Saate kliendi tellimuste kuvamiseks kasutada järgmisi filtreid.

    -   Otsing nime alusel
    -   Otsing konto alusel

-   Pärast kliendi valimist saate vaadata järgmist teavet.

    -   Kliendi nimi ja grupp
    -   Kliendi kontaktandmed
    -   Kliendi müügitellimused ja nende üksikasjad.
    
        -   Kliendi nimi ja aadressiandmed
        -   Erinevad müügitellimuse kuupäevad
        -   Tellimuse vastuvõtja kontaktteave
        -   Kliendi kontaktandmed
        -   Tellimuse read
        -   Saadetised, mis näitavad, kuidas ja millal müügitellimus on teele pandud

## <a name="prerequisites"></a>Eeltingimused
Eeltingimused erinevad, olenevalt teie organisatsioonis juurutatud Microsoft Dynamics 365 versioonist.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Eeltingimused Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni kasutamisel 
Kui teie organisatsioonis on juurutatud rakenduse Dynamics 365 for Finance and Operations, Enterprise Edition, peab süsteemiadministraator avaldama **müügitellimuste** mobiilse tööruumi. Juhised leiate jaotisest [Mobiilse tööruumi avaldamine](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Eeltingimused Dynamics 365 for Operationsi versiooni 1611 platvormivärskendusega 3 või uuema kasutamisel
Kui teie organisatsioonis on juurutatud Dynamics 365 for Operationsi versioon 1611 platvormivärskendusega 3 või uuem, peab süsteemiadministraator täitma järgmised eeltingimused. 

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

<td>KB 4013633 on X++ värskendus või metaandmete kiirparandus, mis sisaldab mobiilset tööruumi <strong>Müügitellimused</strong>. KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laadige alla metaandmete kiirparandus teenusest Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Rakendage juurutatav pakett</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Avaldage mobiilne tööruum <strong>Müügitellimused</strong>.</td>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Teabe kuvamine kliendi müügitellimuste kohta, kasutades müügitellimuse mobiilset tööruumi

1.  Valige oma mobiilses seadmes tööruum **Müügitellimused**.
2.  Valige **Kuva kliendi tellimused**.
3.  Saate kliendi leidmiseks kasutada konto või kliendi nime teavet.
4.  Valige klient.
5.  Valige **Kontaktandmed** või **Müügitellimused**. Kui valite suvandi **Müügitellimused**, kuvatakse kliendi müügitellimuste loend.
6.  Valige **Müügitellimus**. Nüüd saate vaadata teavet müügitellimuste ja saadetiste kohta ning kliendi kontaktteavet ja tellimuse vastuvõtja kontaktteavet.

