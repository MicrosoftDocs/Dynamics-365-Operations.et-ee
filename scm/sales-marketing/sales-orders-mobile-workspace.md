---
title: "Müügitellimuste mobiilne tööruum"
description: "See teema annab teavet Microsoft Dynamics 365 for Operationsi mobiilirakenduse jaoks saadaoleva müügitellimuste mobiilse tööruumi kohta. See tööruum aitab teil olla oma müügitellimustega alati kõikjal kursis."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 119b80e5d8067ffbf75d8b067f4803558c2c94b0
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Müügitellimuste mobiilne tööruum

[!include[banner](../includes/banner.md)]


See teema annab teavet Microsoft Dynamics 365 for Operationsi mobiilirakenduse jaoks saadaoleva müügitellimuste mobiilse tööruumi kohta. See tööruum aitab teil olla oma müügitellimustega alati kõikjal kursis. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Müügitellimuste mobiilse tööruumi ülevaade
---------------------------------------------

Mobiilne tööruum **Müügitellimused** pääseb juurde Microsoft Dynamics 365 for Operationsile ja võimaldab teil vaadata iga müügitellimuse kohta üksikasjalikku teavet. See teave hõlmab tellimuse olekut, kliendi kontaktteavet ja tellimuse vastuvõtja kontaktteavet. Mobiilne tööruum **Müügitellimused** annab müügitellimustest kiirülevaate. Saate vaadata kõiki müügitellimusi, müügitellimusi klientide kaupa või konkreetse müügitellimuse andmeid. Mobiilne tööruum pakub kahte vaadet, mis aitavad teil müügitellimusi põhjalikult analüüsida.

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
Enne mobiilse tööruumi **Müügitellimused** juurutamist veenduge, et teie süsteemiadministraator oleks täitnud järgmised eeltingimused.

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
<td>Kui teie organisatsioonis pole Dynamics 365 for Operations veel juurutatud, peaks süsteemiadministraator nägema teadet <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Microsoft Dynamics 365 for Operationsi demokeskkonna juurutamine</a>.</td>
</tr>
<tr class="even">
<td>Juurutatud peab olema KB 4013633.</td>
<td>Süsteemiadministraator</td>
<td>KB 4013633 (X\+\+ värskendus või metaandmete kiirparandus) sisaldab tarneahela haldamiseks nelja mobiilset tööruumi. KB 4013633 juurutamiseks peab süsteemiadministraator toimima järgmiselt.
<ol>
<li>Laadima KB 4013633 alla Microsoft Dynamicsi elutsükliteenustest (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Installima metaandmete kiirparanduse</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Looma juurutatava paketi</a>, mis sisaldab mudelit <strong>SCMMobile</strong>, ja seejärel laadima juurutatava paketi LCS-i üles.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Rakendama juurutatavat paketti</a> teie Microsoft Dynamics 365 for Operationsi süsteemile.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobiilne tööruum <strong>Müügitellimused</strong> tuleb avaldada Dynamics 365 for Operationsi mobiilirakenduses.</td>
<td>Süsteemiadministraator</td>
<td><ol>
<li>Käivitage oma brauseris rakendus Dynamics 365 for Operations.</li>
<li>Valige lehel <strong>Süsteemiparameetrid</strong> suvand <strong>Mobiilsete tööruumide haldamine</strong>.</li>
<li>Valige mobiilne tööruum <strong>Müügitellimused</strong>.</li>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Teabe kuvamine kliendi müügitellimuste kohta, kasutades mobiilset tööruumi
1.  Valige oma mobiilses seadmes tööruum **Müügitellimused**.
2.  Valige **Kuva kliendi tellimused**.
3.  Saate kliendi leidmiseks kasutada konto või kliendi nime teavet.
4.  Valige klient.
5.  Valige **Kontaktandmed** või **Müügitellimused**. Kui valite suvandi **Müügitellimused**, kuvatakse kliendi müügitellimuste loend.
6.  Valige **Müügitellimus**. Nüüd saate vaadata teavet müügitellimuste ja saadetiste kohta ning kliendi kontaktteavet ja tellimuse vastuvõtja kontaktteavet.





