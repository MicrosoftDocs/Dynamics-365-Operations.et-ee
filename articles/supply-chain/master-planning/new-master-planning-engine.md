---
title: Üleminek planeerimise optimeerimisele koondplaneerimiseks
description: See artikkel annab teavet uue koondplaneerimise mootori, planeerimise optimeerimise ja olemasolevast mootorist migreerimise kohta.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: dbbc58f0dcd833f63e84a73ac68ada60bd0c291d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739947"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Üleminek planeerimise optimeerimisele koondplaneerimiseks

[!include [banner](../includes/banner.md)]

Sisseehitatud koondplaneerimise mootor kavatsetakse muuta iganenuks. See asendatakse planeerimise optimeerimise lisandmooduliga Microsoft Dynamics 365 Supply Chain Management. See artikkel annab teavet mõju kohta uutele ja olemasolevatele juurutustele. See sisaldab teavet vajalike toimingute kohta.

Planeerimise optimeerimine võimaldab koondplaneerimise arvutuste tegemist väljaspool Supply Chain Managementi ja selle Azure'i SQL-andmebaasi. Planeerimise optimeerimisega seotud eelised hõlmavad paremat jõudlust ja minimeeritud mõju SQL-andmebaasile koondplaneerimise käivitamiste ajal. Kuna kiireid planeerimise käivitamisi saab teha isegi kontoris viibimise ajal, saavad planeerijad nõudlusele või parameetri muutustele kohe reageerida.

Lisateavet planeerimise optimeerimise kohta vt koondplaneerimise [süsteemi ülesehitusest](master-planning-architecture.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Olemasoleva koondplaneerimise mootori iganemine

Microsoft plaanib plaanimise optimeerimise käigus aegunud koondplaneerimise mootori aegunuks. See muudatus mõjutab kõiki pilvkeskkondi. Kohapealseid installe ei mõjutata. Versioonis 10.0.16 ja uuemas versioonis kuvatakse tõrketeade, kui käivitate taunitud koondplaneerimise mootori plaanitud tootmistellimusi loomata. Vaatamata tõrketeatele viiakse koondplaneerimise käivitamine siiski edukalt lõpule.

Taunitud koondplaneerimise mootori kohta lisateabe saamiseks [lugege teateid jaotises Eemaldatud või Taunitud funktsioonid jaotises Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Migreerimine, teated ja erandid

Olemasolevate keskkonnade omanikud, kes käitavad aegunud koondplaneerimise mootorit plaanitud tootmistellimusi loomata, saavad meili, mis annab erandiprotsessi üksikasjad. Soovitame töötada koos partneriga, et hinnata ja planeerida migreerumist planeerimise optimeerimise funktsiooni.

Nagu on mainitud, saate tõrketeate versioonis 10.0.16 ja hiljem, kui käivitate taunitud koondplaneerimise mootori plaanitud tootmistellimusi loomata. See tõrketeade sisaldab juhiseid migreerimise ja erandi taotlemise kohta.

### <a name="new-deployments"></a>Uued juurutused

Plaanimise optimeerimist tuleb pidada kõigi pilves juurutuste koondplaneerimise vaikemootoriks. Üldjuhul tuleks planeerimise optimeerimist kasutada kõigi uute juurutuste puhul, mis ei loo koondplaneerimise ajal plaanitud tootmistellimusi. Kui uus juurutamine sõltub funktsioonidest, mida plaanimise optimeerimine praegu ei toeta, saate taotleda erandt, nii et saate jätkata taunitud koondplaneerimise mootori kasutamist.

### <a name="existing-deployments"></a>Olemasolevad juurutused

Olemasolevate koondplaneerimisest sõltuvate pilvepõhise juurutuste omanikud peaksid kavandama ülemineku planeerimise optimeerimisele. Kui teie rakendamine sõltub funktsioonidest, mida plaanimise optimeerimine praegu ei toeta, saate taotleda erandlikkust, nii et saate jätkata taunitud koondplaneerimise mootori kasutamist.

Keskkondades, mis praegu kasutavad iganevaid koondplaneerimise protsesse, saadab Microsoft meilisõnumi keskkonna administraatorile. See meilisõnum annab teavet toimingute kohta, mis on vajalikud, et migreerida või taotleda erandit.

## <a name="the-exception-process"></a>Erandiprotsess

Saate taotleda erandt, kui peate kasutama edasi taunitud koondplaneerimise mootorit, sest teie äriprotsessid sõltuvad peatselt vähemalt ühest funktsioonist, mida plaanimise optimeerimises praegu ei rakendata. Saadaolevate funktsioonide loendi leiate teemast [Planeerimise optimeerimise sobivuse analüüs](planning-optimization/planning-optimization-fit-analysis.md).

Praegu on planeerimise optimeerimise migratsiooni erandid asjakohased ainult juhul, kui koondplaneerimise protsess ei sisalda tootmist (st koondplaneerimise loodud plaanitud tootmistellimusi) ja te nõuate taunitud koondplaanimise mootorit väljaspool versiooni 10.0.15.

Pärast nõutavate funktsioonide kättesaadavaks muutumist annab Microsoft ajapikenduse perioodi, kuni erand aegub. Keskkonna administraatorit teavitatakse, kui nõutavad funktsioonid on saadaval ja ajapikenduse periood on alanud.

Järgmises vooskeemis summeeritakse selles artiklis antud teave, et oleks võimalik kiiresti teada saada, kas tuleks teha erand. Kui teil on vaja taotleda erandit, täitke ja esitage [Planning Optimization migreerimise ja erandi küsimustik](https://go.microsoft.com/fwlink/?linkid=2144962). Tootegrupp vastutab iga eranditaotluse hindamise ja kinnitamise eest, seega esitage oma taotlus otse tootegrupile, kasutades esitatud linki ja ärge looge selle jaoks tugipiletit. Kui teie taotlus lükatakse tagasi, siis ärge looge tugipiletit, kuna Microsoft Support ei saa ümber hinnata ega anda erandeid.

![Erandi vooskeem.](media/exception-diagram.png "Erandi vooskeem")

> [!NOTE]
> Erandit saate taotleda ainult rentnikele, kes hetkel kaasavad või kaasavad tulevikus tootmiskeskkondadega, mitte ainult liivakastikeskkondadega üürnikele. Kui teil on vaja keelata planeerimise optimeerimise erandi tõrge infrastruktuuri teenuse (IaaS-i) liivakastikeskkonnas, käivitage SQL-i päring, mis on esitatud teemas [Liivakastikeskkonad](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Liivakastikeskkonnad

Kas ma saab oma kaustakeskkonnas kasutada taunitud koondplaneerimise mootorit? Kas mul on vaja erandit?

**Vastus:** erandid pole kaustakeskkondades tavaliselt asjakohased, kuna optimeerimise erandi tõrge ei takista aegunud koondplaanimise mootori edukat töötamist. Kuid kui tõrketeade häirib teid, saate selle keelata infrastruktuuri teenuse (mitte Service Fabricu) liivakastikeskkonnas, käivitades järgmise andmebaasipäringu.

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

**Vastus:** ei. Kohapealse keskkonna puhul pole erand nõutav. Saate jätkata mittetaunitud koondplaneerimise mootori kasutamist. Teie keskkonna administraatorit teavitatakse, kui midagi on vaja teha.

### <a name="production-scenarios"></a>Tootmisstsenaariumid

Kasutame plaanitud tootmistellimusi, aga olen mures, mis juhtub, kui võtame kasutusele versiooni 10.0.16. Kas peaksin midagi tegema?

**Vastus:** muretsemiseks pole põhjust. Saate jätkata mittetaunitud koondplaneerimise mootori kasutamist versioonis 10.0.16. Soovitame siiski hinnata, kas üleminekut planeerimise optimeerimisele praeguste funktsioonidega alustada saab. Samuti soovitame teil püsida kursis uute funktsioonidega.

### <a name="email-from-microsoft"></a>Microsofti meilisõnum

Meie keskkonna administraator sai Microsoftilt meilisõnumi. Meilisõnumis öeldakse, et peaksime üle minema planeerimise optimeerimisele või erandit taotlema. Kas pean midagi tegema?

**Vastus:** jah. Teie keskkonda mõjutatakse, kui te ei järgi meilisõnumis toodud juhiseid. Saate kas määratud kuupäevaks planeerimise optimeerimisele üle minna või taotleda meilisõnumis oleva lingi kaudu erandit. See link avab küsimustiku. Kui olete selle küsimustiku täitnud ja esitanud, saate vastuse meilisõnumiga. Pärast küsimustiku esitamist püüab Microsoft vastata nädala jooksul, ehkki see protsess tehakse käsitsi.

### <a name="error-messages"></a>Tõrketeated

Kasutan versiooni 10.0.16 või uuemat versiooni ja koondplaneerimise käitamisel kuvatakse järgmine tõrketeade. Kas koondplaneerimine on blokeeritud?

> Saate selle tõrketeate, sest plaanimise optimeerimise toetatud stsenaariumite puhul kasutati taunitud koondplaneerimise mootorit. Peaksite nüüd plaanimise optimeerimisele üle kandma, kuna integreeritud koondplaneerimise mootor on aegunud. Arvestage, et see koondplaneerimise käivitamine viidi siiski edukalt lõpule.
>
> Kui teie migreerimisel on ootel funktsioonidest tugevad sõltuvused, saate taotleda erandt taunitud koondplaneerimise mootori jätkuvale kasutamisele.
>
> Alustamiseks täitke järgmine küsimustik ja vajaduse korral paluge erandit planeerimise optimeerimisele üleminekul.

**Vastus:** ei, koondplaneerimine ei ole blokeeritud. Teie koondplaneerimine viidi edukalt lõpule ja saate tulemust kasutada tavalisel viisil. Kuid selleks, et välistada edaspidi selle tõrketeate kuvamine koondplaneerimise käitamise ajal, peate kohe planeerimise optimeerimisele üle minema või taotlema erandit, kasutades tõrketeates olevat linki.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
