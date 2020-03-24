---
title: Eemaldatud või aegunud platvormi funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095770"
---
# <a name="removed-or-deprecated-platform-features"></a>Eemaldatud või aegunud platvormi funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="platform-update-32"></a>Platvormivärskendus update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Töövoo taotluse muutmise dialoogiboks ei sisalda enam kasutaja valiku ripploendit
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | See oli turvalisuse probleem, kuna muudatuse taotluse võis saata soovimatule kasutajale. See oli ka kasutatavuse probleem, sest see sundis kasutajat määratlema, kes oli töövoo algataja, ja valida need käsitsi.  |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Töövoog |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Kasutaja valiku ripploend eemaldati taotluse muudatuse dialoogiboksist platvormi värskenduses 32. Taotluse muutmise taotlused saadetakse automaatselt algatajale, nagu see on ette nähtud. Lisateavet selle funktsiooni kohta vt teemast [Tegevused töövoo kinnitusprotsessis](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Manustatud süvitsi mindavaid linke ei toetata enam lehekülgjaotusega dokumentides, mida pilve majutatud teenus renderdab 
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Teenuse renderdatud dokumentidesse manustatud navigeermise URL-id võivad sisaldada tundlikke äriandmeid. Eemaldame manustatud süvitsi mindavate linkide toe dokumentidest ettevaatusabinõuna, et täiendavalt kaitsta kliendiandmeid. Kasutajad saavad kasu ka parandatud jõudlusest ja selle muudatuse tulemusel saavad toota dokumente interaktiivselt.  |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Aruandlus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Seda funktsiooni eemaldatakse aktiivselt teenusest.<br><br>Kaasaegne klient pakub mitmeid võimalusi vaadete loomiseks, mis sisaldavad automaatselt loodud linke, mis aitavad rakenduses navigeerida. Lehekülgjaotusega dokumente, mida teenuses renderdatakse, soovitatakse kasutada välissuhtluses, nagu adressaatidele meilitud, arhiivitud ja prinditud. Oleme parandanud dokumentide eelvaate kogemust otse brauseris, mis võimaldab otsest juurdepääsu kohalikele printeritele. Lisateabe saamiseks vaadake teemat [PDF-dokumentide eelvaade manustatud vaaturi abil](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest
Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../migration-upgrade/deprecated-features.md).

