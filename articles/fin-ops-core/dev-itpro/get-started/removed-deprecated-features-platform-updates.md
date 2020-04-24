---
title: Eemaldatud või aegunud platvormi funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.
author: sericks007
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: 0072ca507301fdb880f0595a06377ff01366ca20
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260525"
---
# <a name="removed-or-deprecated-platform-features"></a>Eemaldatud või aegunud platvormi funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.11 värskendused

### <a name="field-groups-containing-invalid-field-references"></a>Sobimatuid väljaviiteid sisaldavad väljagrupid

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Tabeli metaandmete määratluste väljagrupid võivad sisaldada kehtetuid väljaviiteid. Nende väljagruppide juurutamise korral võib see põhjustada käitusaja tõrkeid teenuses Financial Reporting ja Microsoft SQL Serveri aruandlusteenustes (SSRS). Platform update'i 23 lisati kompilaatori *hoiatus*, mis lubas selle metaandmete probleemi lahendamise. Rakenduste Finance and Operations Platformi versiooni 10.0.11 värskendused liigitavad selle probleemi kompilaatori *tõrkena*.<p>Sellep probleemi lahendamiseks tehke järgmist.</p><ol><li>Eemaldage sobimatu väljaviide tabeli väljagrupi definitsioonist.</li><li>Kompileerige uuesti.</li><li>Veenduge, et kõik tõrked oleksid lahendatud.</li></ol> |
| **Asendatud teise funktsiooniga?**   | See kompilaatori tõrge asendab kompilaatori hoiatuse jäädavalt.  |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | **Aegunud:** kompilaatori hoiatus on rakenduste Finance and Operations platformi versiooni 10.0.11 värskendustes nüüd kompilaatori tõrge. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-litsentsid, mis on loodud SHA1 räsialgoritmi abil

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Sõltumatu tarkvara hankija (ISV) litsentside loomise protsess on muutunud. Lisateabe saamiseks vt [sõltumatu tarkvara hankija (ISV) litsentsimine](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Asendatud teise funktsiooniga?**   | Jah. Windows PowerShelli kasutamine litsentside loomiseks. |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | <strong>Aegunud:</strong> ISV litsentsid, mis loodi SHA1 räsialgoritmi abil. See algoritm sõltus sertidest, mis loodi utiliidi MakeCert abil ja see utiliit on aegunud.<p><strong>Aegunud:</strong> SHA1 kasutamine turbe või räsimise eesmärgil. SHA1 ei tööta enam 2021. aasta alguses. Seetõttu ei tohiks seda enam kasutada.<p><strong>Eemaldatud:</strong> toetus transpordi kihi turvalisusele (tls) 1.0 ja TLS 1.1 sissetulevad või väljaminevad taotlused. |

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

