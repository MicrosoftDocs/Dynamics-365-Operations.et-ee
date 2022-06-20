---
title: Pealevõtmismooduli sisseregistreerimine
description: See artikkel katab sisseregistreerimise komplekteeritud moodulile ja selgitab selle konfigureerimist Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7002db893da1802063148a9b800ffa92f3e5f065
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885471"
---
# <a name="check-in-for-pickup-module"></a>Pealevõtmismooduli sisseregistreerimine

[!include [banner](includes/banner.md)]

See artikkel katab sisseregistreerimise komplekteeritud moodulile ja selgitab selle konfigureerimist Microsoft Dynamics 365 Commerce.

Pealeregistreerimise moodulis on kinnitusleht klientide jaoks, kes kasutavad kliendi sisseregistreerimise võimalusi kauplusesse Dynamics 365 Commerce saabumisest teavitada. Pealeregistreerimise moodul võimaldab teil konfigureerida vormi, mis kogub klientidelt lisateavet, et tellimuse tarnet hõlbustada. See teave sisaldab kliendi parkimiskoha numbrit ning oma sõiduki tootjat ja mudelit. 

## <a name="module-properties"></a>Mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Kinnitustekst | Tekstistring | Sisseregistreerimise kinnituse lehel kuvatava pealkirja sisu. |
| Kuva QR-koodi | **Tõene** või **Väär** | Kui atribuudi väärtuseks on seatud **Tõene**, kuvatakse sisseregistreerimise kinnituslehel QR-kood, mis tähistab tellimuse kinnituse ID-d. |
| Lisateabe pealkiri | Tekstistring | Täiendavate teabeväljade konfigureerimisel kuvatava pealkirja sisu. |
| Lisateabe klahvid | Ressursi ID / ressursi väärtuse paar | Iga võti loob vormi välja ja sellega seotud sildi, mida kasutatakse klientidelt lisateabe kogumiseks. |
| Täiendavate teabevõtmete \> ressursi ID | Tekstistring | Iga infovõti loob vormi välja ja sellega seotud sildi, mida kasutatakse klientidelt lisateabe kogumiseks. See atribuut tuvastab lisateabe võtme. Kassas (POS) loodud ülesandes kuvatakse selle atribuudi väärtus juhiste väljal sildina. |
| Täiendavate teabevõtmete \> ressursi väärtus | Tekstistring | Kassasoleva ülesande tekstivälja silt. |
| Täiendavate teabevõtmete \> on nõutav | **Tõene** või **Väär** | See atribuut määrab, kas kliendid peavad vormi välja enne jätkamist täitma. Kui selle atribuudi väärtuseks on seatud **Tõene**, renderdatakse vormi sildi kõrvale tärn ja tehakse tühikontroll, et takistada klientide jätkamist, kui ühtegi väärtust ei sisestata. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Lehele sisseregistreerimise mooduli lisamine

Sisseregistreerimise mooduli registreerimine tuleb lisada uuele lehele, mille loote sisseregistreerimise kinnituse jaoks. See lehekülg on sisseregistreerimise kinnituskogemus klientide jaoks, kes valivad lingi **Olen siin** või nupu oma meilis. 

## <a name="configure-the-additional-information-form"></a>Lisateabe vormi konfigureerimine

Vaikimisi, kui rohkem teabevõtmeid pole konfigureeritud, näitab moodul vaikimisi kliente sisseregistreerimise kinnituslehekülge. Kuna kuvatakse sisseregistreerimise kinnitust, luuakse müügikohas ülesanne kauplusele, kust tellimus peale võetakse.

Kui konfigureeritakse üks või mitu täiendavat teabevõtit, palutakse klientidel kõigepealt sisestada teave. Kui valite **Edasta**, kuvatakse neile sisseregistreerimise kinnitus ja kassas luuakse ülesanne. 

## <a name="additional-resources"></a>Lisaressursid

[Luba kliendi sisseregistreerimise teatised kassas (POS)](enable-customer-check-in.md)
