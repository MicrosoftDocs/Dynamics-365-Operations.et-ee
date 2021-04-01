---
title: Osaline asukoha tsükliline inventuur
description: Tsüklilise inventuuri plaanid juhivad tegelikke inventuuritoimingud. Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abafe64a17b7b284e5e045da33bb15cf3c42800b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234677"
---
# <a name="partial-location-cycle-counting"></a>Osaline asukoha tsükliline inventuur

[!include [banner](../includes/banner.md)]

Tsüklilise inventuuri plaanid juhivad tegelikke inventuuritoimingud. Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante.

Tsüklilise inventuuri plaanide abil inventuuritöö loomisel saate juhtida tegelikke inventuuritoiminguid. Saate nõuda, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante. Konkreetseid tooteid filtreerides saab laojuht vähendada ülevaatamise üldkulusid, vältida konsolideerimisvigu ja säästa aega.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Osalise asukoha tsüklilise inventuuri konfigureerimine

Kui kasutate inventuuritoimingute jaoks lao tööprotsessi, luuakse iga asukoha jaoks tööpäis. Kui määratlete tsüklilise inventuuri plaani, võite kasutada päringut **Vali asukohad** loodava tsüklilise inventuuri töö piiramiseks. Tsüklilise inventuuri plaani jaoks toodete valimisel saate valida nii toote kui ka tootevariandi päringuid, et täpsustada, mida loendatakse.

Tsüklilise inventuuri plaaniga saab seostada **töömalli** määramiseks, kuidas tsüklilise inventuuri töö tuleks luua. Inventuuritoimingute töömallile viidatakse otse tsüklilise inventuuri plaanist.

Töömalli üksikasjade määratlemisel võite kasutada valikut **Töörea jaotused** määramiseks, kas inventuuritöö read tuleks rühmitada kaubakoodi või tootevariandi koodi alusel. See seadistus on vajalik ainult juhul, kui soovite loendada asukohas vaba kaubavaru ainult teatud toodete puhul. Loodavatel tsüklilise inventuuri töö ridadel on siin määratud teabetase ja juhendatud inventuuritoiming toimub selle taseme põhjal.

Kui seostate tsüklilise inventuuri plaanid töömallidega, kasutades valikut **Tööridade jaotused**, valitakse loodavale tsüklilise inventuuri tööle väli **Osaline tsükliline inventuur** ja töömalli definitsiooni põhjal luuakse mitu tsüklilise inventuuri töö rida.

Enne osalise tsüklilise inventuuri töö töötlemist peab tegema tsüklilise inventuuri seadistamise käigus mobiilse seadme menüüelemendile vähemalt valiku **Kuva kaubakood**. Laooperaatoril palutakse registreerida ainult inventuuriridadega seotud inventuuriteave (kaubakoodid ja tootedimensioonid). Kõiki muid vabu kaubavarusid eiratakse selle inventuuriprotsessi puhul.

Osalise tsüklilise inventuuri protsessi korral ei uuendata asukoha kuupäeva/kellaaega **Viimane tsükliline inventuur**, kuigi loendatakse kõik antud asukohas olevad üksused. Osaline tsükliline inventuur ei arvesta lehel **Tsüklilise inventuuri plaanid** parameetrit **Päevi tsükliliste inventuuride vahel**. Osaline tsükliline inventuur ei toeta mitme üksuse samaaegset loendamist samas asukohas. Osalise tsüklilise inventuuri funktsioon võib põhjustada kauba korral sama asukoha loendamist mitu korda, kui käitatakse käsk **Töötle tsüklilise inventuuri plaani**. Selle stsenaariumi vältimiseks määrake filtrid väljal **Vali asukohad**.

> [!NOTE]
> Osalise tsüklilise inventuuri protsessi käigus ei paku laorakendus nuppu **Lisa LP või kaup**.

## <a name="example"></a>Näide

Selle näite puhul tuleb laos 61 loendada ainult kaup koodiga A0001.

1. Tsüklilisele inventuurile luuakse uus töömall. Inventuuri tööridade rühmitamiseks kaubakoodi alusel kasutatakse valikut **Töörea jaotused**. Seega on loodaval tsüklilise inventuuri tööl read kaubakoodi kohta. Võite rühmitada read ka tootevariandi numbri järgi.
1. Luuakse uus tsüklilise inventuuri plaan, mis viitab äsja loodud töömallile. Tsüklilise inventuuri plaan sisaldab kõiki asukohti laos 61 (päring **Vali asukohad**), kus on kaubakoodi A0001 varud. Konkreetsete toodete valik on määratletud jaotises **Tsüklilise inventuuri tootevalikud**.
1. Tsüklilise inventuuri plaanidele saab valida tooteid, määrates välja **Tühjad asukohad** olekuks **Välista tühjad**. Tsüklilise inventuuri plaani töötlemisel luuakse kaubakoodile A0001 osaline tsüklilise inventuuri töö. Tegeliku inventuuriprotsessi saab juhendatud tsüklilise inventuuri puhul läbida mobiilse seadme menüüelemendi abil.

## <a name="additional-resources"></a>Lisaressursid

[Tsükliline inventuur](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]