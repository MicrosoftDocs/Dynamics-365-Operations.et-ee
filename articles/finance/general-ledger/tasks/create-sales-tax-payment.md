---
title: Käibemaksumakse loomine
description: Käibemaksu tasakaalustamise ja sisestamise töö toiming tasakaalustab käibemaksukontode käibemaksu saldod ja tasakaalustab need käibemaksu tasakaalustuskontoga kindla perioodi jooksul.
author: twheeloc
ms.date: 10/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54132ca4775482b4a06ff7e73125e804aff40cb4
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700109"
---
# <a name="create-a-sales-tax-payment"></a>Käibemaksumakse loomine

[!include [banner](../../includes/banner.md)]

Käibemaksu tasakaalustamise ja sisestamise töö toiming tasakaalustab käibemaksukontode käibemaksu saldod ja tasakaalustab need käibemaksu tasakaalustuskontoga kindla perioodi jooksul.

1. Avage **Maksud > Deklaratsioonid > Käibemaks > Käibemaksu tasakaalustamine ja sisestamine**.
2. Klõpsake väljal **Tasakaalustusperiood** otsingu avamiseks ripploendi nuppu.
3. Klõpsake loendis valitud real olevat linki.
4. Sisestage kuupäev väljale **Alates kuupäevast**.
    - Kui te suvandit **Kaasa parandused** pole lehel **Pearaamatu parameetrid** valitud, saab tasakaalustuse eri versioone töödelda. Originaal on perioodivahemiku esimene tasakaalustus ja seda saab töödelda perioodivahemiku kohta ainult üks kord. Viimased parandused tasakaalustavad käibemaksukanded, mis on sisestatud pärast algversiooni loomist.
5. Sisestage kuupäev väljale **Kande kuupäev**.
6. Klõpsake valikut **OK**.

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
