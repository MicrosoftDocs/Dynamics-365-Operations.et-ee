---
title: Süsteemi määratletud ja kasutaja määratletud tabelipiirangud
description: 'See artikkel selgitab kahte toote konfiguratsioonimudeli komponentide tabelipiirangu tüüpi: kasutaja määratletud ja süsteemi määratletud. Tabelipiirangud kajastavad lubatud atribuudikombinatsioonide matriitse, kus iga rida määratleb ühe võimalike atribuudiväärtuste kogumi.'
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4b484c99bc8f1cc830d4177460ec15a26714a56
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577380"
---
# <a name="system-defined-and-user-defined-table-constraints"></a>Süsteemi määratletud ja kasutaja määratletud tabelipiirangud

[!include [banner](../includes/banner.md)]

See artikkel selgitab kahte toote konfiguratsioonimudeli komponentide tabelipiirangu tüüpi: kasutaja määratletud ja süsteemi määratletud. Tabelipiirangud kajastavad lubatud atribuudikombinatsioonide matriitse, kus iga rida määratleb ühe võimalike atribuudiväärtuste kogumi.

Tabelipiirangud tähistavad toote konfiguratsioonimudelisse kuuluvate komponentide puhul lubatud atribuudikombinatsioonide maatrikseid. Tabeli iga rida määratleb ühe võimalike atribuudiväärtuste komplekti. Saate toote konfiguratsioonimudelis deklareerida kaht tüüpi piiranguid.

-   **Avaldisepiirang** – saate luua avaldise, mis määratleb atribuutide vahelised seosed, et toote konfigureerimisel oleks võimalik valida ainult ühilduvaid väärtusi.
-   **Tabelipiirangu** – saate luua tabeli, mis määratleb kõik määratud atribuudikomplekti puhul lubatud kombinatsioonid. Saadaval on kaht tüüpi tabelipiiranguid: kasutaja määratletud tabelipiirangud ja süsteemi määratletud tabelipiirangud.

See artikkel kirjeldab toote konfiguratsioonimudelisse kuuluvate komponentide kasutaja määratletud ja süsteemi määratletud tabelipiiranguid.

## <a name="user-defined-table-constraints"></a>Kasutaja määratletud tabelipiirangud
Kasutaja määratletud tabelipiirang on teatud tüüpi maatriks, mida kasutatakse atribuuditüüpidega määratletud atribuudiväärtuste kombinatsiooni kirjeldamiseks. Näiteks kui toodate kõlareid, saate kasutaja määratud tabelipiirangus lisada korpuseviimistluse ja esivõre jaoks kaks veergu. Korpuseviimistluse atribuuditüübil on neli väärtust ja esivõre atribuuditüübil on kolm väärtust. Seetõttu on piirangute puudumisel võimalikud 4 x 3 = 12 kombinatsiooni. Selles näites on aga lubatud ainult kuus kombinatsiooni, nagu näidatud järgmises tabelis. See teave kuvatakse lehe **Tabelipiirangu redigeerimine** vahekaardil **Lubatud kombinatsioonid**.

| Kabinetiviimistlus | Esivõre |
|----------------|-------------|
| Must          | Must       |
| Must          | Metall       |
| Tamm            | Must       |
| Roosipuu       | Valge       |
| Valge          | Must       |
| Valge          | Valge       |

Kasutaja määratletud tabelipiirangud määratletakse staatilise tabelisisendiga, mis toimib sarnaselt avaldisepiiranguga. Kasutaja määratletud tabelipiirangu kasutamise eelis on see, et tabeleid on sageli lihtsam luua, mõista ja hallata kui pikki avaldisepiiranguid.

## <a name="system-defined-table-constraints"></a>Süsteemi määratletud tabelipiirangud
Süsteemi määratletud tabelipiirang loob tabeli atribuuditüübi ja välja vahele dünaamilise vastenduse. Kui süsteemi määratletud tabelipiirangu sisaldub toote konfiguratsioonimudelis, tagab vastendamine, et atribuuditüübi asemel kuvatakse tabelis olevad andmed. Tulemuseks on dünaamiline piirang, kuna tabeli sisu saab muuta (nt teistes moodulites).  

Süsteemi määratletud tabelipiirangu loomisel saate valida tabeli, soovi korral määratleda kasutatava päringu ja seejärel seostada atribuuditüübid valitud tabeli väljadega. Väljade tüübid peavad ühtima atribuuditüüpide tüüpidega.  

Enne kui tabeli piirang saab toote konfiguratsioonimudelis jõustuda, tuleb tabeli piirang kaasata ühte mudeli kompondi piirangusse kaasata. Protseduur on uue piirangu loomiseks, tabeli piirangu tüübi valimiseks ja seejärel kasutatava tabeli piirangu määratluse valimiseks. Viimaks tuleb kõik tabelipiirangu väljad vastendada toote konfiguratsioonimudeli atribuutidega.

## <a name="additional-resources"></a>Lisaressursid

[Toote konfiguratsioonimudelite ülevaade](product-configuration-models.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]