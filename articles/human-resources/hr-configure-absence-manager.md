---
title: Puudumiste halduri rolli konfigureerimine
description: See teema kirjeldab, kuidas seadistada puudumiste halduri rolli töötaja puhkuse haldamiseks.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9e7865a0bb33944c803c628f94371a4c75cc38bd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693027"
---
# <a name="configure-the-absence-manager-role"></a>Puudumiste halduri rolli konfigureerimine

>[!Important]
>Selles teemas märgitud funktsioone saavad kliendid praegu kasutada eraldiseisvas teenuses Dynamics 365 Human Resources. Osa või kõik funktsioonid on saadaval osana Finance'i taristu tulevasest väljalaskest pärast Finance'i versiooni 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Mõnedes organisatsioonides ei pruugi personalijuhatajad oma meeskonna puhkuseid hallata. Selle asemel võib puudumise haldur selle protsessiga tegeleda mitme osakonna ja meeskonna meeskonnaliikmete jaoks. Puudumiste halduritel on puhkusehalduseks järgmised võimalused:

- Vaadake üle ja kinnitage puhkus alternatiivse hierarhia alusel.
- Kuva töörühma liikme saldosid.
- Saate vaadata puudumiste kalendrit.

## <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

1. Valige **Süsteemihaldus** tööruumis **Funktsioonihaldus**.

2. Lubage **Funktsioonihaldus** vahekaardil funktsioon **Puudumiste haldur puhkuste haldamiseks**.

## <a name="define-a-custom-hierarchy"></a>Kohandatud hierarhia määratlemine

Puudumiste halduri funktsioon kasutab kohandatud hierarhiat, mida tuleb konfigureerida.

1. Valige **Organisatsiooni haldus** tööruumis **Positsioonihierarhia tüübid**.

2. Looge ametikoha hierarhia tüüp nimega **Puhkus**.

3. Valige **Puhkus ja puudumine** tööruumi jaotises **Lingid** suvand **Puhkuse ja puudumise parameetrid**.

4. Valige varem loodud **Puhkuse** hierarhia tüüp vahekaardi **Üldine** ripploendist **Puudumiste hierarhia**. See puhkuse hierarhia seos tuleb täita iga juriidilise isiku jaoks, kus kasutatakse puudumise halduri funktsioone.

Pärast hierarhiatüübi määratlemist tuleb ametikohale määrata ametikoha hierarhia aruanne.

1. Valige **Organisatsiooni haldus** tööruumis **Kõik ametikohad**.

2. Valige ametikoht, mille jaoks soovite puudumise hierarhiat lisada.

3. Valige vahekaardil **Seosed** suvand **Lisa**.

4. Valige väljal **Hierarhia nimi** suvand **Puhkus**.

5. Valige ametikoht väljal **Millisele ametikohale annab aru**. Töötaja nimi täidetakse automaatselt pärast ametikoha valimist.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Määrake kasutajale Puudumiste halduri roll.

Puudumiste halduri roll tuleb töötajatele määrata, et nad saaksid puhkusetaotlusi heaks kiita või tagasi lükata.

1. **Süsteemiadministraator** tööruumis valige **Lingid**.

2. Valige jaotises **Kasutajad** link **Kasutajad**.

3. Valige kasutajate loendist kasutaja, kellele määrata Puudumise halduri roll.

4. Vahekaardil **Kasutaja roll** valige suvand **Määra rollid**.

5. Valige loendist **Puudumiste halduri** roll. Seejärel valige **OK**.

    > [!IMPORTANT]
    > Veenduge, et töötaja roll on määratud ka kasutajale, kellele te Puudumiste halduri rolli määrate. Vastasel juhul ei saa töötaja seda funktsiooni kasutada.

6. Pärast Puhkuse hierarhia loomist saate seda vaadata järgmiste sammude abil.

    1. Valige **Organisatsiooni haldus** tööruumis **Ametikoha hierarhia**.
    
    2. Valige väljal **Hierarhia tüüp** suvand **Puhkus**.

## <a name="absence-manager-workspace"></a>Puudumiste halduri tööruum

**Töötaja iseteeninduse** tööruumis kuvatakse **Puhkuste haldamine** vahekaardil puudumiste teave töötajate kohta, kes on puhkuse hierarhias puudumiste haldurisse määratud. Puudumiste halduril on mõned võimalused saadaval: 
 - Vaba aja taotluste läbi vaatamine.</br>
 - Töötaja nimel töölt eemaldumistaotluse esitamine.</br>
 - Saate vaadata kõiki nendesse puhkusehierarhiasse määratud töötajaid.</br>
 - Puudumiste halduri kalendri kuvamine.</br>

**Puhkuse halduse** tööruumis on kaks vahekaarti:
 - **Vaba aja taotlus**: see vahekaart loetleb kõik ootelolevad puudumise taotlused, mille puudumiste haldur saab kinnitada. Puudumiste haldur saab valida mitu kirjet ja tegutseda nendega samaaegselt. Kui ettevõtteülene puhkusevaade on lubatud, kuvatakse selles loendis kõigi juriidiliste isikute ootelolevad väljaminekutaotlused, mille juurde neil on juurdepääs. Vastasel juhul kuvatakse see praegu valitud juriidilise isiku ootel olevate vaba aja taotluste kohta. </br>
 - **Kõik töötajad**: Sellel vahekaardil loetletakse puhkuse hierarhias kõik puudumiste haldajale määratud töötajad. Igale töötajale on saadaval mõned valikuvõimalused:
    - **Taotle puhkust** – Saate edastada valitud töötajale uue vaba aja taotluse.</br>
    - **Vaba aeg** – vaadake valitud töötaja saldosid, heakskiidetud vaba aega ja puhkeaja taotlusi.</br>

## <a name="approve-time-off-requests"></a>Vaba aja taotluste kinnitamine

Puudumise haldurid saavad töötajate aja mahavõtmise taotlusi heaks kiita või tagasi lükata. 

> [!IMPORTANT]
> Enne, kui puudumise haldurid saavad puhkusetaotlusi heaks kiita või tagasi lükata, tuleb puhkuse taotlemise töövoog konfigureerida, et määrata neile ülevaatamiseks puhkuse taotlemise tööüksused.
>
> 1. Leheküljel **Inimressurside töövood** valige või looge puhkuse taotluse töövoog.
> 2. Valige suvand **Seosta hierarhia** ja seejärel valige **Hierarhia nimi** väljal **Puhkus**.
> 3. Värskendage töövoogu töövoo kujundajas. Jaotises **Määramistüüp** valige suvand **Hierarhia** ja seejärel valige vahekaardil **Hierarhia valik** suvand **Konfigureeritav hierarhia**.
>
> Teavet puhkusetaotluse töövoo loomise kohta leiate teemast [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md).

1. Valige töölehel **Töötaja iseteenindus** vahekaart **Puhkuste haldur**.

2. Valige **Puhkuse taotlus** vahekaardilt puhkuse taotlus, millele soovite midagi teha. Selles loendivaates saate valida mitu kirjet.

3. Kasutage ruudustiku ülaosas nuppe Kinnita, Keeldu või Delegeeri vaba aja taotluseks. 

Teise võimalusena saab kasutaja kasutada vasakul paani **Vaba aja taotlus**, et navigeerida kõigi väljasolevate tööüksuste ajaloendisse. 

## <a name="view-time-off-in-the-calendar"></a>Kalendris puhkuse kuvamine

Puudumiste halduri rolli kasutajad saavad vaadata oma kalendris puhkuste taotlusi. Puhkusekalendrile juurdepääsemiseks järgige järgmisi samme.

> [!IMPORTANT]
> Süsteemiadministraator peab puudumiste halduri kalendri vaatevalikud konfigureerima. **Puhkuse ja puudumise parameetrite** lehel on vahekaardil **Kalender** suvand sünnipäevade, üksikasjadeta puudumiste, puudumiste ja ootel puhkusetaotluste peitmiseks või näitamiseks. Samuti on võimalus kalendrivaate valikut filtreerida töötaja tüübi järgi.

1. Tööruumis **Töötaja iseteenindus** valige **Puudumiste haldur** ja seejärel **Puudumiste halduri kalender**.

2. Väljale **Kuupäev** sisestage soovitud kuupäevad.

3. Värskendage vaate valikuid vastavalt vajadusele.

Puudumiste halduri kalender näitab kõiki kirjeid töötajate kohta, kes on puhkuse hierarhias puudumiste haldurile sellest teada andnud.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
- [Puhkusetaotluse loomine töövoogu](hr-leave-and-absence-workflow.md)
- [Meeskonna ja ettevõtte kalendrite kuvamine](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
