---
title: Puudumiste halduri rolli konfigureerimine
description: See teema kirjeldab, kuidas seadistada puudumiste halduri rolli töötaja puhkuse haldamiseks.
author: hasrivas
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8a8250b36d2774ac308637253b780592df316cd
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639602"
---
# <a name="configure-the-absence-manager-role"></a>Puudumiste halduri rolli konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Mõnedes organisatsioonides ei pruugi personalijuhatajad oma meeskonna puhkuseid hallata. Selle asemel võib puudumise haldur selle protsessiga tegeleda mitme osakonna ja meeskonna meeskonnaliikmete jaoks. Puudumiste halduritel on puhkusehalduseks järgmised võimalused:

- Vaadake üle ja kinnitage puhkus alternatiivse hierarhia alusel.
- Kuva töörühma liikme saldosid.
- Saate vaadata puudumiste kalendrit.

## <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

1. Valige **Süsteemihaldus** tööruumis **Funktsioonihaldus**.

2. Lubage **Funktsioonihaldus** vahekaardil funktsioon **(Eelvaade) Puudumiste haldur puhkuste haldamiseks**.

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

**Töötaja iseteeninduse** tööruumis kuvatakse **Puudumiste halduri** vahekaardil puudumiste teave töötajate kohta, kes on puhkuse hierarhias puudumiste haldurisse määratud.

Vahekaardil **Puhkus ja puudumine** on iga töötaja jaoks saadaval järgmised valikud.

- **Vaba aeg** – vaadake valitud töötaja saldosid, heakskiidetud vaba aega ja puhkeaja taotlusi.
- **Puhkusesaldod** – saate vaadata valitud töötaja erinevate puhkuseplaanide saldode loendit.

## <a name="approve-time-off-requests"></a>Vaba aja taotluste kinnitamine

Puudumise haldurid saavad töötajate aja mahavõtmise taotlusi heaks kiita või tagasi lükata. Nad saavad vajaduse korral luua taotlusi ka töötajate nimel.

> [!IMPORTANT]
> Enne, kui puudumise haldurid saavad puhkusetaotlusi heaks kiita või tagasi lükata, tuleb puhkuse taotlemise töövoog konfigureerida neile puhkuse taotlemise tööüksused ülevaatamiseks määrama.
>
> 1. Leheküljel **Inimressurside töövood** valige või looge puhkuse taotluse töövoog.
> 2. Valige suvand **Seosta hierarhia** ja seejärel valige **Hierarhia nimi** väljal **Puhkus**.
> 3. Värskendage töövoogu töövoo kujundajas. Jaotises **Määramistüüp** valige suvand **Hierarhia** ja seejärel valige vahekaardil **Hierarhia valik** suvand **Konfigureeritav hierarhia**.
>
> Teavet puhkusetaotluse töövoo loomise kohta leiate teemast [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md).

1. Valige **Töötaja iseteeninduse** töölehel vahekaart **Puudumise haldur**.

2. Valige vahekaardil **Puudumiste haldur** soovitud töötaja.

3. Valige **Üksikasjad** ja seejärel **Puhkus**.

4. Otsige puhkusetaotlus üles ja valige suvand **Kinnitamine**. Seejärel saate valida suvandi, mis kinnitab või tühistab puhkusetaotluse.

Olek **Tühistamine** näitab, et taotlus on tagasi lükatud. Olek **Lõpetatud** näitab, et taotlus on heaks kiidetud.

## <a name="view-time-off-in-the-calendar"></a>Kalendris puhkuse kuvamine

Puudumiste halduri rolli kasutajad saavad vaadata oma kalendris puhkuste taotlusi. Puhkusekalendrile juurdepääsemiseks järgige järgmisi samme.

> [!IMPORTANT]
> Süsteemiadministraator peab puudumiste halduri kalendri vaatevalikud konfigureerima. **Puhkuse ja puudumise parameetrite** lehel on vahekaardil **Kalender** suvand sünnipäevade, üksikasjadeta puudumiste, puudumiste ja ootel puhkusetaotluste peitmiseks või näitamiseks. Samuti on võimalus kalendrivaate valikut filtreerida töötaja tüübi järgi.

1. Valige tööruumis **Töötaja iseteenindus** **Puudumiste haldur** ja seejärel **Puudumiste halduri kalender**.

2. Väljale **Kuupäev** sisestage soovitud kuupäevad.

3. Värskendage vaate valikuid vastavalt vajadusele.

Puudumiste halduri kalender näitab kõiki kirjeid töötajate kohta, kes on puhkuse hierarhias puudumiste haldurile sellest teada andnud.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
- [Puhkusetaotluse loomine töövoogu](hr-leave-and-absence-workflow.md)
- [Meeskonna ja ettevõtte kalendrite kuvamine](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
