---
title: "Osaline asukoha tsükliline inventuur"
description: "Tsüklilise inventuuri plaanid juhivad tegelikke inventuuritoimingud. Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 856ac2a61bc06a772b586a0cf77496fc360db623
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="partial-location-cycle-counting"></a>Osaline asukoha tsükliline inventuur

[!include[banner](../includes/banner.md)]


Tsüklilise inventuuri plaanid juhivad tegelikke inventuuritoimingud. Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante.

Tsüklilise inventuuri plaanide abil inventuuritöö loomisel saate juhtida tegelikke inventuuritoiminguid. Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante. Konkreetseid tooteid filtreerides saab laojuht vähendada ülevaatamise üldkulusid, vältida konsolideerimisvigu ja säästa aega.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Osalise asukoha tsüklilise inventuuri konfigureerimine
Kui kasutate inventuuritoimingute jaoks lao tööprotsessi, luuakse iga asukoha jaoks tööpäis. Kui määratlete tsüklilise inventuuri plaani, võite kasutada päringut **Vali asukohad** loodava tsüklilise inventuuri töö piiramiseks. Tsüklilise inventuuri plaani jaoks toodete valimisel saate valida nii toote kui ka tootevariandi päringuid, et täpsustada, mida loendatakse. 

Tsüklilise inventuuri plaaniga saab seostada **töömalli** määramiseks, kuidas tsüklilise inventuuri töö tuleks luua. Inventuuritoimingute töömallile viidatakse otse tsüklilise inventuuri plaanist. 

Töömalli üksikasjade määratlemisel võite kasutada valikut **Töörea jaotused** määramiseks, kas inventuuritöö read tuleks rühmitada kaubakoodi või tootevariandi koodi alusel. See seadistus on vajalik ainult juhul, kui soovite loendada asukohas vaba kaubavaru ainult teatud toodete puhul. Loodavatel tsüklilise inventuuri töö ridadel on siin määratud teabetase ja juhendatud inventuuritoiming toimub selle taseme põhjal. 

Kui seostate tsüklilise inventuuri plaanid töömallidega, kasutades valikut **Tööridade jaotused**, valitakse loodavale tsüklilise inventuuri tööle väli **Osaline tsükliline inventuur** ja töömalli definitsiooni põhjal luuakse mitu tsüklilise inventuuri töö rida. 

Enne osalise tsüklilise inventuuri töö töötlemist peab tegema tsüklilise inventuuri seadistamise käigus mobiilse seadme menüüelemendile vähemalt valiku **Kuva kaubakood**. Laooperaatoril palutakse registreerida ainult inventuuriridadega seotud inventuuriteave (kaubakoodid ja tootedimensioonid). Kõiki muid vabu kaubavarusid eiratakse selle inventuuriprotsessi puhul. 

Osalise tsüklilise inventuuri protsessi puhul ei uuendata asukoha kuupäeva/kellaaega **Viimane tsükliline inventuur**.

## <a name="example"></a>Näide
Selle näite puhul tuleb laos 61 loendada ainult kaup koodiga A0001.

1.  Tsüklilisele inventuurile luuakse uus töömall. Inventuuri tööridade rühmitamiseks kaubakoodi alusel kasutatakse valikut **Töörea jaotused**. Seega on loodaval tsüklilise inventuuri tööl read kaubakoodi kohta. Võite rühmitada read ka tootevariandi numbri järgi.
2.  Luuakse uus tsüklilise inventuuri plaan, mis viitab äsja loodud töömallile. Tsüklilise inventuuri plaan sisaldab kõiki asukohti laos 61 (päring **Vali asukohad**), kus on kaubakoodi A0001 varud. Konkreetsete toodete valik on määratletud jaotises **Tsüklilise inventuuri tootevalikud**.
3.  Tsüklilise inventuuri plaanidele saab valida tooteid, määrates välja **Tühjad asukohad** olekuks **Välista tühjad**. Tsüklilise inventuuri plaani töötlemisel luuakse kaubakoodile A0001 osaline tsüklilise inventuuri töö. Tegeliku inventuuriprotsessi saab juhendatud tsüklilise inventuuri puhul läbida mobiilse seadme menüüelemendi abil.



<a name="see-also"></a>Vt ka
--------

[Tsükliline inventuur](cycle-counting.md)

