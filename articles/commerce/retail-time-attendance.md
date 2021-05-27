---
title: Aja ja kohaloleku haldus rakenduses Retail
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Commerce aja ja kohaloleku halduse puhul toetatud stsenaariume.
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7ac7eec69bda7ad2fa41a7311a71a969eddeafb6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021484"
---
# <a name="time-and-attendance-management-in-retail"></a>Aja ja kohaloleku haldus rakenduses Retail

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Commerce aja ja kohaloleku halduse puhul toetatud stsenaariume.

## <a name="manage-worker-setup-and-scheduling"></a>Töötaja seadistus ja tööaeg

### <a name="initial-configuration"></a> Algne konfiguratsioon

- Käitage konfiguratsiooniviisardit.
- Registreerige töötajad aja registreerimisega töötajatena.

### <a name="plan-worker-schedules"></a>Töötaja graafikute planeerimine

- Rakendage tööplaanija abil reeglid. Lisateavet tööde loendite kasutamise kohta vt teemast [Tööplaneerija profiilide rakendamine](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).

Konfiguratsiooni sammude kohta leiate teemast [Aja ja kohaloleku seadistamine](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).

### <a name="commerce-specific-configuration"></a>Kaubandusele spetsiifiline konfiguratsioon

- Lubage funktsiooniprofiili Kell töötajate, kellele soovite aja registreerimist lubada. Klõpsake valikuid **Kassa funktsiooniprofiilid** &gt; **Funktsioonid** &gt; **Kassa ajaregistreerimised** &gt; **Luba aja registreerimine**.
- Konfigureerige kassa (POS) õiguste gruppe, et kuvada Kellaaja kirjete vaatamisõigused. See luba võimaldab kasutajal vaadata kaupluse teiste töötajate (ja mistahes teise kaupluse töötajate, millega kasutaja aadressiraamatus seostatud on) aja registreerimisi. Võite ehk tahta anda seda luba juhataja rollile, kuid mitte kassapidaja rollile. Klõpsake valikut **Kassa loagrupid** &gt; **Kellaaja kirjete vaatamine**.

## <a name="register-time"></a>Registreerimise aeg

### <a name="cashier-and-non-cashier-time-registrations"></a>Kassa ja kassavälise aja registreerimised

- Kassas

    - Sisseregistreerimise toimingud:

        - logige sisse kassavälise toiminguga või uue vahetusega;
        - valige kellaaja toiming;
        - valige soovitud toiming:

            - Sisseregistreerimine
            - tööpaus,
            - Lõunapaus
            - Väljaregistreerimine

        <table>
        <thead>
        <tr>
        <th>Praegune olek</th>
        <th>Saadavalolevad toimingud</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Sisseregistreerimine</td>
        <td>
        <ul>
        <li>tööpaus,</li>
        <li>Lõunapaus</li>
        <li>Väljaregistreerimine</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>tööpaus,</td>
        <td>Sisseregistreerimine</td>
        </tr>
        <tr>
        <td>Lõunapaus</td>
        <td>Sisseregistreerimine</td>
        </tr>
        <tr>
        <td>Väljaregistreerimine</td>
        <td>Sisseregistreerimine</td>
        </tr>
        </tbody>
        </table>

        [![Kellaaeg kella järgi](./media/timeclockstates.png)](./media/timeclockstates.png)

- Vaadake kinnitusteadet ja kontrollige, kas praeguse toimingu kellaaeg on õige.
- Logiraamat

    - Klõpsake kellaaja tegevuste vaatamiseks valikut **Logiraamat**.
    - Muude kellaaja akende valimiseks kasutage ajafiltreid.
    - Kui töötate mitmes kaupluses, näete kõiki oma aja registreerimisi kõigis kauplustes, kus olete aja registreerinud. Valitud kaupluse ajaregistreerimiste vaatamiseks kasutage kaupluse filtrit.

- Erinevad ajavööndid

    - Kui vaatate aega mõnest teisest kohast (kassapidaja puhul logiraamatust või juhi stsenaariumi puhul valikut **Kellaaja kirjete vaatamine** kasutades) ja see koht on teises ajavööndis, on vaadeldavad kellaaja kirjed teisendatud teie kohalikku ajavööndisse. Näiteks olete kahe kaupluse juhataja, üks neist asub Arizonas ja teine Nevadas. Kassapidaja Arizonas registreerib sisse kell 9.00 . Sel ajal on kell Nevadas 8.00. Seega, kui olete Nevada kaupluses ja vaatate registreerimiskirjeid, on registreerimise ajaks märgitud kell 8.

## <a name="view-worker-time-registrations"></a>Töötaja aja registreerimise kuvamine

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Töötaja ajaregistreerimiste vaatamine ning kaupluse või tegevuse tüübi filtreerimine

Kassas:

- valige **Kellaaja kirjete vaatamine**;
- kuvatakse kõikide teiega samasse kauplusesse määratud töötajate ajaregistreerimise tegevused;
- ajaregistreerimiste filtreerimiseks saate kasutada tegevuse tüübi ja kaupluse filtreid.

## <a name="process-and-manage-time-registrations"></a>Aja registreerimiste töötlemine ja haldamine

Commerce’i kasutaja jälgib töövoogu ajaregistreerimiste arvutamiseks, kinnitamiseks ja palgaarvestusse ülekandmiseks.

### <a name="primary-operations"></a>Esmased toimingud

- Arvuta
- Kinnita
- Esita palgaarvestuseks

### <a name="other-common-operations"></a>Muud tavapärased toimingud

- Hulgiväljaregistreerimine
- Puudumise registreerimine

Protsessi aja ja kohaloleku registreerimised kohta lisateabe saamiseks vt [Protsessiaja ja kohaloleku registreerimine](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).


[!INCLUDE[footer-include](../includes/footer-banner.md)]