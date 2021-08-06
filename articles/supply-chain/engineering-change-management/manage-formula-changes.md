---
title: Valemite ja nende koostisainete muudatuste haldamine
description: See teema kirjeldab, kuidas teha valemihaldust ja hallata tootmise koondandmete töötlemise muudatusi.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d25ddfc992d49c9a3c24d03cb0c71d68f7aa21fa
ms.sourcegitcommit: 908a85987b604a7782407da70fb70ef75c07989f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/19/2021
ms.locfileid: "6641100"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Valemite ja nende koostisainete muudatuste haldamine

[!include [banner](../includes/banner.md)]

Kui kasutate Microsofti protsessi tootmise võimalusi, saate kasutada ka seotud valemihalduse võimalusi järgmiste Microsoft Dynamics 365 Supply Chain Management muudatuste haldamiseks:

- **Valemid ja plaanimise üksused:** Halda muudatusi valemites olevatele koostisainetele, nende kaastoodetele ja by-toodetele.
- **Kaastooted ja kaastooted:** Redigeerige kaastoodete jaby-toodete koguseid ja muud teavet valemis.
- **Tegeliku kaalu kaubad:** Tegeliku kaaluga kaupade muudatuste haldamine.

## <a name="turn-on-this-feature-in-your-system"></a>Funktsiooni sisselülitamine teie süsteemis

Selle võimaluse kasutamiseks peate täitma järgmised ülesanded.

1. Lubage *tehnilise muudatuse haldus* ja selle konfiguratsioonivõti, nagu on kirjeldatud jaotises [Tehnilise muudatuse halduse ülevaade](product-engineering-overview.md). Nagu selles teemas mainitud, veenduge, et lubate ka protsessi **tootmise litsentsivõtme muutmise halduse** mis on pesastatud **peainseneride muudatuste halduse** litsentsivõtme all.
1. Lülitage *funktsioonihalduses sisse funktsioonihalduse valemite* ja nende [koostisainete haldamise funktsioon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="feature-naming-conventions"></a>Funktsiooni nimetamis conventions

Supply Chain Management kasutajaliideses ja dokumentatsioonis nimetatakse *muudatusehalduse funktsioone* tavaliselt tehnika muudatusehalduseks ning hallatavaid tooteid nimetatakse tavaliselt *tehnikatoodeteks*. Kuigi see terminoloogia pole tavaliselt seostatud protsessi tootmise valemite haldamisega, peaksite arvama, et tehnika muudatusehaldus on lihtsalt muudatusehaldus, ja peate arvama, et tehnikatooted on versioonitud tooted.

## <a name="work-with-formula-change-management-features"></a>Tööta valemi muutmise halduse funktsioonidega

Järgmises loendis võetakse kokku, kuidas tehnika muudatusehalduse funktsioonid valemihaldusele rakenduvad. Samuti pakutakse linke lisateabele. Kuna valemi muudatusehaldus kasutab tehnika muutmise haldamise funktsioone, peaksite teadma, kuidas tehnika muudatusehaldus üldiselt töötab, nii et saate seda kasutada oma valemite ja nende koostisainete haldamiseks.

- **Tsentraliseeritud tooteandmete haldu** – seadistage organisatsioon, mis tagab hallatud väljalaskeprotsessi kaudu, et täpsed ja asjakohased tooteandmed on kasutajatele kättesaadavad kogu ettevõttes. Lisateavet vt teemast [Tehnikaettevõtted ja andmete omandiõiguse reeglid](engineering-org-data-ownership-rules.md).
- **Toote versioonimine** - jälgige tooteversioonide kaudu toodete muutusi ja kontrollige toodettarneahela kõigis etappides. Sel viisil saate jälgida muudatusi oma varudes. Lisateavet vt teemast [Tehnilised versioonid ja tehniliste toodete kategooriad](engineering-versions-product-category.md).
- **Toote töötsükli haldus** – hallake tooteandmete nähtavust organisatsiooni ulatuses ja kontrollige tooteversioonide kättesaadavust tarneahela igas etapis. Teil on üksikasjalik kontroll selle üle, millal toote versiooni saab kindlates äriprotsessides kasutada ja te saate luua oma elutsükli olekud, et need sobiksid teie ärivajadustega. Lisateavet vt jaotisest [Toote töötsükli olekud ja kanded](product-lifecycle-state-transactions.md).
- **Valemimuudatuste haldus** – kasutajad kogu teie organisatsioonis saavad taotleda valemite muudatusi. Kasutage muudatuste tellimusi pakutud muudatuste mõju hindamiseks ja dokumenteerimiseks. Lisage töövood, et hallata muudatuse protsessi ning toote ja selle valemi uute versioonide väljalaset. Lisateavet vt teemast [Tehniliste toodete muudatuste haldamine](engineering-change-management.md).
- **Valmisoleku juhtimine** - kasutage süsteemi kontrolle ja kasutajajuhiseid (küsimustikke ja kontroll-loendeid), et tagada kõigi nõutud tooteandmete täielik sisestatud sisestamineenne toote välja lastakse. Lisateavet vt jaotisest [Toote valmisolek](product-readiness.md).
- **Täiustatud toote väljast vabastamise funktsioon** - vabastage toote ja selle valemi täielikult määratud versioonidorganisatsioonist (juriidiline isik) teistele juriidilistele isikutele. Saate isegi otsustada, kas tooteteavet tuleb enne väljalaset üle vaadata või redigeerida. Lisateavet leiate jaotisest [Tootestruktuuride vabastamine](release-product-structure.md).

Pidage meeles, et enamik eelmise loendiga seotud teemadest sisaldab kooslustel põhinevaid näiteid. Valemid töötavad siiski sarnasel viisil. Siin on mõned täiendavad mõisted, mis on kasulikud teada, kui kasutate muudatusehaldust (või ainult valemi muutmise haldust) valemite ja koosluste haldamiseks:

- Iga [tooteinseneri kategooria](engineering-versions-product-category.md) puhul saate määrata tootmise tüübi (kooslus, valem või plaanimisüksus). Samuti saate määrata, kas seda kategooriat kasutavate toodete puhul on tegeliku kaalu tugi nõutav.
- Kaastooted ja kaastooted ei ole tehnikatooted. Seetõttu pole need versioonitud. Kui peate neid muutma, looge uus toode. See lähenemine lihtsustab hooldust.
- Saate hallata lõppüksusi, mis on kooslustega ja neil on tütarvalemi üksused. Funktsioon töötab mis tahes koosluste kombinatsioonide puhul, mis sisaldavad kooslusi sisaldavaid valemeid ja/või valemeid.
