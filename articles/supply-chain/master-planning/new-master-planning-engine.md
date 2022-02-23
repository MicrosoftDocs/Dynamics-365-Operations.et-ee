---
title: Üleminek planeerimise optimeerimisele koondplaneerimiseks
description: See teema annab teavet planeerimise optimeerimise kohta, mis on uus koondplaneerimise mootor, ja olemasolevalt mootorilt ülemineku kohta.
author: ChristianRytt
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 94e5668da45c524ed9ab9eef10b40d0fb5336a65
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645992"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Üleminek planeerimise optimeerimisele koondplaneerimiseks

[!include [banner](../includes/banner.md)]

Sisseehitatud koondplaneerimise mootor kavatsetakse muuta iganenuks. See asendatakse planeerimise optimeerimise lisandmooduliga Microsoft Dynamics 365 Supply Chain Management. See teema annab teavet uute ja olemasolevate juurutuste mõju kohta. See sisaldab teavet vajalike toimingute kohta.

Planeerimise optimeerimine võimaldab koondplaneerimise arvutuste tegemist väljaspool Supply Chain Managementi ja selle Azure'i SQL-andmebaasi. Planeerimise optimeerimisega seotud eelised hõlmavad paremat jõudlust ja minimeeritud mõju SQL-andmebaasile koondplaneerimise käivitamiste ajal. Kuna kiireid planeerimise käivitamisi saab teha isegi kontoris viibimise ajal, saavad planeerijad nõudlusele või parameetri muutustele kohe reageerida.

Lisateavet planeerimise optimeerimise kohta vt teemast [Planeerimise optimeerimise ülevaade](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Olemasoleva koondplaneerimise mootori iganemine

Microsoft on sisseehitatud planeerimismootorit iganenuks muutmas, et teha ruumi planeerimise optimeerimisele. See muudatus mõjutab kõiki pilvkeskkondi. Kohapealseid installe ei mõjutata. Versioonis 10.0.16 ja uuemates versioonides kuvatakse tõrketeade, kui käivitate sisseehitatud koondplaneerimise ilma plaanitud tootmistellimusi loomata. Vaatamata tõrketeatele viiakse koondplaneerimise käivitamine siiski edukalt lõpule.

Lisateavet sisseehitatud planeerimismootori iganemise kohta vaadake teemast [Eemaldatud või iganenud funktsioonid teenuses Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Migreerimine, teated ja erandid

Selliste olemasolevate keskkondade omanikud, milles käitatakse sisseehitatud koondplaneerimise mootorit ilma plaanitud tootmistellimuste loomiseta, saavad e-kirja koos üksikasjadega erandiprotsessi kohta. Soovitame töötada koos partneriga, et hinnata ja planeerida migreerumist planeerimise optimeerimise funktsiooni.

Nagu öeldud, kuvatakse versioonis 10.0.16 ja uuemas versioonis tõrketeade, kui käivitate sisseehitatud koondplaneerimise ilma plaanitud tootmistellimusi loomata. See tõrketeade sisaldab juhiseid migreerimise ja erandi taotlemise kohta.

### <a name="new-deployments"></a>Uued juurutused

Planeerimise optimeerimist tuleks pidada kõigi pilvteenuse uute juurutuste puhul vaikimisi koondplaneerimise mootoriks. Üldjuhul tuleks planeerimise optimeerimist kasutada kõigi uute juurutuste puhul, mis ei loo koondplaneerimise ajal plaanitud tootmistellimusi. Kui uus juurutamine sõltub funktsionaalsusest, mida planeerimise optimeerimine praegu ei toeta, saate erandi taotleda, et saaksite jätkata sisseehitatud koondplaneerimise mootori kasutamist.

### <a name="existing-deployments"></a>Olemasolevad juurutused

Olemasolevate koondplaneerimisest sõltuvate pilvepõhise juurutuste omanikud peaksid kavandama ülemineku planeerimise optimeerimisele. Kui teie rakendus sõltub funktsionaalsusest, mida planeerimise optimeerimine praegu ei toeta, saate erandi taotleda, et saaksite jätkata sisseehitatud koondplaneerimise mootori kasutamist.

Keskkondades, mis praegu kasutavad iganevaid koondplaneerimise protsesse, saadab Microsoft meilisõnumi keskkonna administraatorile. See meilisõnum annab teavet toimingute kohta, mis on vajalikud, et migreerida või taotleda erandit.

## <a name="the-exception-process"></a>Erandiprotsess

Saate erandi taotleda, kui peate jätkama sisseehitatud koondplaneerimise mootori kasutamist, sest teie äriprotsessid sõltuvad suuresti vähemalt ühest funktsioonist, mida praegu optimeerimise planeerimisel ei rakendata. Saadaolevate funktsioonide loendi leiate teemast [Planeerimise optimeerimise sobivuse analüüs](planning-optimization/planning-optimization-fit-analysis.md).

Praegu on planeerimise optimeerimise funktsiooni migreerumise erand asjakohane, kui teie koondplaneerimise protsess ei hõlma tootmist (ehk koondplaneerimise loodud plaanitud tootmistellimused) ja vajate sisseehitatud koondplaneerimise mootori versioonist 10.0.15 uuemat versiooni.

Pärast nõutavate funktsioonide kättesaadavaks muutumist annab Microsoft ajapikenduse perioodi, kuni erand aegub. Keskkonna administraatorit teavitatakse, kui nõutavad funktsioonid on saadaval ja ajapikenduse periood on alanud.

> [!NOTE]
> Erandit saate taotleda ainult töökeskkonnale, mitte liivakastikeskkonnale. Kui teil on vaja keelata planeerimise optimeerimise erandi tõrge infrastruktuuri teenuse (IaaS-i) liivakastikeskkonnas, käivitage SQL-i päring, mis on esitatud teemas [Liivakastikeskkonad](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Liivakastikeskkonnad

Kas ma saan kasutada sisseehitatud koondplaneerimist oma liivakastikeskkonnas? Kas mul on vaja erandit?

**Vastus:** erandid ei ole tavaliselt liivakastikeskkonnas asjakohased, kuna planeerimise optimeerimise erandi tõrge ei takista sisseehitatud koondplaneerimise mootori edukat käitamist. Kuid kui tõrketeade häirib teid, saate selle keelata infrastruktuuri teenuse (mitte Service Fabricu) liivakastikeskkonnas, käivitades järgmise andmebaasipäringu.

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Kohapealsed keskkonnad

Mul on kohapealne keskkond. Kas mul on vaja erandit?

**Vastus:** ei. Kohapealse keskkonna puhul pole erand nõutav. Saate jätkata sisseehitatud koondplaneerimise kasutamist. Teie keskkonna administraatorit teavitatakse, kui midagi on vaja teha.

### <a name="production-scenarios"></a>Tootmisstsenaariumid

Kasutame plaanitud tootmistellimusi, aga olen mures, mis juhtub, kui võtame kasutusele versiooni 10.0.16. Kas peaksin midagi tegema?

**Vastus:** muretsemiseks pole põhjust. Versiooniga 10.0.16. saate sisseehitatud koondplaneerimist edasi kasutada. Soovitame siiski hinnata, kas üleminekut planeerimise optimeerimisele praeguste funktsioonidega alustada saab. Samuti soovitame teil püsida kursis uute funktsioonidega.

### <a name="email-from-microsoft"></a>Microsofti meilisõnum

Meie keskkonna administraator sai Microsoftilt meilisõnumi. Meilisõnumis öeldakse, et peaksime üle minema planeerimise optimeerimisele või erandit taotlema. Kas pean midagi tegema?

**Vastus:** jah. Teie keskkonda mõjutatakse, kui te ei järgi meilisõnumis toodud juhiseid. Saate kas määratud kuupäevaks planeerimise optimeerimisele üle minna või taotleda meilisõnumis oleva lingi kaudu erandit. See link avab küsimustiku. Kui olete selle küsimustiku täitnud ja esitanud, saate vastuse meilisõnumiga. Pärast küsimustiku esitamist püüab Microsoft vastata nädala jooksul, ehkki see protsess tehakse käsitsi.

### <a name="error-messages"></a>Tõrketeated

Kasutan versiooni 10.0.16 või uuemat versiooni ja koondplaneerimise käitamisel kuvatakse järgmine tõrketeade. Kas koondplaneerimine on blokeeritud?

> See tõrketeade kuvatakse, sest sisseehitatud koondplaneerimise mootorit kasutati selleks, et optimeerida stsenaariumeid, mida toetab planeerimise optimeerimine. Peaksite kohe planeerimise optimeerimisele üle minema, sest praegune sisseehitatud koondplaneerimine on iganenud. Arvestage, et see koondplaneerimise käivitamine viidi siiski edukalt lõpule.
>
> Juhul, kui üleminek sõltub suuresti ootel funktsioonidest, saate taotleda sisseehitatud koondplaneerimise mootori jätkuva kasutuse erandit.
>
> Alustamiseks täitke järgmine küsimustik ja vajaduse korral paluge erandit planeerimise optimeerimisele üleminekul.

**Vastus:** ei, koondplaneerimine ei ole blokeeritud. Teie koondplaneerimine viidi edukalt lõpule ja saate tulemust kasutada tavalisel viisil. Kuid selleks, et välistada edaspidi selle tõrketeate kuvamine koondplaneerimise käitamise ajal, peate kohe planeerimise optimeerimisele üle minema või taotlema erandit, kasutades tõrketeates olevat linki.
