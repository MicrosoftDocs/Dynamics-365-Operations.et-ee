---
title: Käibemaksumakse loomine
description: Käibemaksu tasakaalustamise ja sisestamise töö toiming tasakaalustab käibemaksukontode käibemaksu saldod ja tasakaalustab need käibemaksu tasakaalustuskontoga kindla perioodi jooksul.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735864"
---
# <a name="create-a-sales-tax-payment"></a>Käibemaksumakse loomine

[!include [banner](../../includes/banner.md)]

Käibemaksu tasakaalustamise ja sisestamise töö toiming tasakaalustab käibemaksukontode käibemaksu saldod ja tasakaalustab need käibemaksu tasakaalustuskontoga kindla perioodi jooksul.

1. Avage **Maksud > Deklaratsioonid > Käibemaks > Käibemaksu tasakaalustamine ja sisestamine**.
2. **Otsingu** avamiseks valige väljal Tasakaalustusperiood rippnupp.
3. Klõpsake loendis valitud real olevat linki.
4. Sisestage kuupäev väljale **Alates kuupäevast**. Kui te suvandit **Kaasa parandused** pole lehel **Pearaamatu parameetrid** valitud, saab tasakaalustuse eri versioone töödelda. **Originaal** on perioodiintervalli esimene tasakaalustus ja seda saab perioodiintervalli puhul töödelda ainult üks kord. Viimased parandused tasakaalustavad käibemaksukanded, mis on sisestatud pärast algse versiooni loomist.
5. Sisestage kuupäev väljale **Kande kuupäev**.
6. Valige nupp **OK**. Käibemaksu **maksete aruanne** prinditakse perioodi tasakaalustatud käibemaksukannete ülevaatamiseks.

Alustades **finantsversioonist** **·** **·** **10**.0.24, võite jätta välja käibemaksu maksete aruande, mis luuakse vahetult pärast seda, kui käibemaksu perioodilised tasakaalustamise ja sisestamise protseduurid rakendatakse funktsioonihalduse tööruumi käibemaksu tasakaalustuse loomise aruande käibemaksuaruande eraldi aruande alusel.

Kui see funktsioon on lubatud, siis pärast tasakaalustusprotsessi lõpetamist käibemaksu maksearuannet ei prindita. Selle asemel saate järgmise teate: "Käibemaksu tasakaalustamine ja sisestamine on lõpule viidud. Kanne 'xxxx, m/aaaa' on sisestatud."

Saate käibemaksu maksearuande siiski käsitsi käivitada, **kui saadate maksuaruanded TaxInquiries** > **ja reportsSales** > **tax inquiriesSales** > **tax payments**.

## <a name="performance-consideration"></a>Jõudluse arvesse võtmisest

Käibemaksu maksmise protseduur võib võtta aega. Protseduuri jõudlust mõjutavad põhitegurid on arvete arv tasakaalustusperioodil ja kirjete arv, mis tuleb sisestada käibemaksu tasakaalustuskandesse. Jõudluse parandamiseks võite valida, et möödute funktsioonidest, mis pole teie protsessis vajalikud.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Lubage käibemaksu makse jõudluse täiustamise funktsioon

**Käibemaksu makse jõudluse parandamise** funktsioon võib aidata parandada käibemaksu maksmise protseduuri jõudlust, kasutades üht rida, arvestusvaluuta summat ja aruandlusvaluuta summat käibemaksu makse kande ridadel, kus on sama põhikonto, pearaamatu dimensioon ja valuuta.

1. Minge jaotisse **Süsteemihaldus** \> **Tööruumid** \> **Funktsioonihaldus**.
2. Otsige ja valige **Kõik** vahekaardil **käibemaksu makse jõudluse täiustus**.
3. Valige **Luba**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Enneta vastasmaksukannete genereerimist

Vaikimisi sisestab käibemaksu maksekanne käibemaksu tasakaalustavad kanded iga käibemaksukandega, mis tasakaalustatakse käibemaksu makseprotseduuril. Need käibemaksu vastaskanded kaasatakse **käibemaksu/pearaamatu vastavusseviimise** aruandesse. Need näitavad perioodi jooksul tasakaalustamata käibemaksukannete laekumata saldot.

Ent käibemaksu vastaskonto kanded võivad käibemaksu maksmise protseduuri seisakut suurendada. Seetõttu saab nõudmisel aktiveerida lennupileti nimega **TaxReportGenOffsetTaxTransPerRecordSetFlighting**. See lendamine võib aidata parandada vastasmaksu kannete loomise jõudlust riikidele ja regioonidele, v.a Tai, Poola, Ungari, Leedu, Malaisia, India, Itaalia, Venemaa, Tšehhi Vabariik, Eesti ja Läti.

> [!NOTE]
> Kui maksukannete tabelis on kohandatud välju, ei saa lendmist aktiveerida.

Kuna **käibemaksu/pearaamatu vastavusse viimise** aruannet kasutatakse üldiselt ainult sisemisel otstarbel ja seda ei nõuta paljudes maksuametites, saate valida käibemaksu makse kandele vastasmaksekande mitte loomist.

1. Avage **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksu tasakaalustusperioodid**.
2. Saate valida arveldusperioodi.
3. Seadke **Üldine** kiirkaardil suvandi **Väldi vastasmaksu kannete genereerimist** väärtusele **Jah**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
