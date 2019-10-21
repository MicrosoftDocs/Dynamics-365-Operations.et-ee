---
title: Töölehel hilinenud maksu arvutamise lubamine
description: See teema selgitab, kuidas kasutada funktsiooni **Töölehel hilinenud maksu arvutamise lubamine**, et parandada maksude arvutamise jõudlust töölehe ridade suure mahu korral.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177310"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Töölehel hilinenud maksu arvutamise lubamine
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See teema selgitab, kuidas kasutada funktsiooni **Töölehel hilinenud maksu arvutamise lubamine**, et parandada maksude arvutamise jõudlust töölehe ridade suure mahu korral.

Praeguse käibemaksu arvutamise käitumine käivitatakse töölehel reaalajas, kui kasutaja uuendab maksuga seotud välju, nt käibemaksugrupp/kauba käibemaksugrupp. Iga töölehe uuendamine rea tasemel, arvutab maksusumma uuesti kõigil töölehe ridadel. See aitab kasutajal näha reaalajas arvutatud maksusummat, kuid see võib tekitada ka jõudluse probleemi töölehe ridade suure mahu korral.

See funktsioon annab võimaluse jõudluse probleemi lahendamiseks viivitada maksude arvutamisega. Kui see funktsioon on sisse lülitatud, arvutatakse maksusumma ainult siis, kui kasutaja klõpsab käsku "Käibemaks" või sisestab töölehe.

Kasutaja saab parameetri sisse/välja lülitada kolmel tasandil.
- Juriidilise isiku järgi
- Töölehe nime järgi
- Töölehe päise järgi

Süsteem käsitleb töölehe päise parameetrit lõplikuna. Töölehe päise parameetri väärtus tuletatakse vaikimisi töölehe nimest. Töölehe nime parameetri väärtus tuletatakse töölehe nime loomisel vaikimisi pearaamatu parameetrist.

Töölehe väljad „Tegelik käibemaksusumma” ja „Arvutatud käibemaksu summa" peidetakse, kui see parameeter on sisse lülitatud. Eesmärk on kasutajat mitte eksitada, kuna nende kahe välja väärtus näitab alati 0, enne kui kasutaja käivitab maksu arvutamise.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Hilinenud maksu arvutamise lubamine juriidilise isiku järgi

1. Avage **Pearaamat > Pearaamatu seadistamine > Pearaamatu parameetrid**
2. Klõpsake suvandit **Käibemaks**.
3. Leidke kiirkaardilt **Üldine** parameeter **Hilinenud maksu arvutamine**, lülitage see sisse/välja

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Hilinenud maksu arvutamise lubamine töölehe nime järgi

1. Avage **Pearaamat > Töölehe seadistamine > Töölehtede nimed**
2. Leidke kiirkaardilt **Üldine** parameeter **Hilinenud maksu arvutamine**, lülitage see sisse/välja

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Hilinenud maksu arvutamise lubamine töölehe järgi

1. Avage **Pearaamat > Töölehe kanded > Päevaraamatud**
2. Klõpsake valikut **Uus**
3. Valige töölehe nimi.
4. Klõpsake **Häälestus**
5. Leidke parameeter **Hilinenud maksu arvutamine**, lülitage see sisse/välja

![](media/delayed-tax-calculation-journal-header.png)
