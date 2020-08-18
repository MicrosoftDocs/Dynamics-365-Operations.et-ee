---
title: Eemaldatud või aegunud platvormi funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.
author: sericks007
manager: AnnBe
ms.date: 07/20/2020
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
ms.openlocfilehash: 393349240d16636d3eec747126cc1ee6f6f9998d
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651662"
---
# <a name="removed-or-deprecated-platform-features"></a>Eemaldatud või aegunud platvormi funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Finance and Operationsi rakenduste platvormi uuendustest.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.13 värskendused

> [!NOTE]
> Versioon 10.0.13 on eelväljaanne. Sisu ja funktsioonid võivad muutuda. Lisateavet eelväljaannete kohta vt teemast [Teenusevärskenduste kättesaadavus](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/public-preview-releases).

### <a name="upgrade-of-three-jquery-component-libraries"></a>Kolme jQuery komponenditeegi täiendamine 

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kolme jQuery komponenditeeki uuendatakse turvaparandustega ja valuuta haldamiseks.   
| **Asendatud teise funktsiooniga?**   | Mõjutatud on järgmised teegid: jQuery (versioonilt 2.1.4 versioonile 3.5.0), jQuery UI (versioonilt 1.11.4 versioonile 1.12.1), jQuery qTip (versioonilt 2.2.1 versioonile 3.0.3). JQuery on migreerimisjuhised internetis kättesaadavaks teinud.  |
| **Mõjutatud tootealad**         | Laiendatavad juhtelemendid, täpsemalt kohandatud JavaScripti kood, mis kasutab iganenud või eemaldatud API-sid |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Versioonis 10.0.13 / platvormivärskenduses 37 saavad kliendid pärast funktsiooni „Kolme jQuery komponenditeegi täiendamine” lubamist hakata soovi korral kasutama uusimaid teeke. Uued teegid tuleb kasutusele võtta 2021. aprilli väljaandega, et anda aega mõjutatud API-de migreerimiseks.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Olemasoleva tabeli juhtelement/forceLegacyGrid() API

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Olemasoleva tabeli juhtelement asendatakse uue ruudustiku juhtelemendiga. |
| **Asendatud teise funktsiooniga?**   | [Uue tabeli juhtelement](../..//fin-ops/get-started/grid-capabilities.md) |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Versioonis 10.0.13 on uus tabeli juhtelement üldiselt saadaval ja kliendid saavad funktsiooni valikuliselt sisse lülitada. Uus tabeli juhtelement muutub kohustuslikuks 2021. aasta oktoobri väljalaskes. Kui uus tabeli juhtelement muutub kohustuslikuks ei saa **forceLegacyGrid()** API-t enam kasutada. |

### <a name="personalization-without-saved-views"></a>Salvestatud vaadeteta isikupärastamine 

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Isikupärastamise alamsüsteem on muudetud salvestatud vaadete funktsiooniga nii, tagamaks parema jõudluse ja pakkumaks täiendavaid võimalusi. |
| **Asendatud teise funktsiooniga?**   | Salvestatud vaated |
| **Mõjutatud tootealad**         | Veebiklient |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Versioonis 10.0.13/Platvormi värskendusega nr 37 on salvestatud vaadete funktsioon üldiselt saadaval ja kliendid saavad selle valikuliselt sisse lülitada. Salvestatud vaadete funktsioon muutub kohustuslikuks 2021. aasta oktoobri väljalaskes. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.12 värskendused

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Kehtetuid väljaviiteid sisaldavad ruudustiku või grupi juhtelemendi vormilaiendused

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Ruudustiku või grupi juhtelementide andmegrupi atribuute kasutatakse väljagrupi kõikide väljade automaatseks kuvamiseks. Laiendusega lisatud ruudustiku või grupi juhtelement võib sisaldada välju, mis ei ole enam väljagrupis määratletud, või väljagrupis määratletud väljad võivad puududa. See võib põhjustada käitusajal vastuolulist käitumist. Rakenduste Finance and Operations Platformi versiooni 10.0.12 värskendused liigitavad nüüd selle probleemi kompilaatori *hoiatusena*. Probleemi lahendamiseks avage vormilaiendus ja salvestage see.
| **Asendatud teise funktsiooniga?**   | See kompilaatori hoiatus asendatakse tulevases värskenduses kompilaatori tõrkega. |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Kompilaatori hoiatus on kasutusele võetud Finance and Operationsi rakenduste versiooni 10.0.12 platvormivärskendustes. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Rakenduste Finance and Operations Platformi versiooni 10.0.11 värskendused

### <a name="explicit-safe-lists-for-self-service-environments"></a>Üksikasjalikud turvalised loendid iseteeninduskeskkondade jaoks

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | IP-de lisamine turvalistesse loenditesse on muutunud. Iseteenindus ei toeta enam turvaliste IP-de loendeid. |
| **Asendatud teise funktsiooniga?**   | Lisateavet vt teemast [Azure Active Directory tingimusliku juurdepääsu konfigureerimine](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Mõjutatud tootealad**         | Turve |
| **Juurutamissuvand**              | Pilv |
| **Olek**                         | **Aegunud:** see funktsioon on iseteeninduse juurutustes täielikult aegunud. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Uusimate Visual Studio versioonide toetamiseks tuleb Visual Studio X++ laiendites teha teatud muudatusi. Need muudatused ei ühildu Visual Studioga 2015. |
| **Asendatud teise funktsiooniga?**   | Visual Studio 2015 asemel saab kasutatavaks ja nõutavaks versiooniks Visual Studio 2017. |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Kui uute virtuaalsete masinate saadavus on Visual Studio 2017 raames välja kuulutatud, siis tuleb ainult Visual Studios 2015 sisalduvad virtuaalsed masinad hiljemalt 2021. aasta 1. väljalaskelaineks ümber juurutada. |

### <a name="field-groups-containing-invalid-field-references"></a>Sobimatuid väljaviiteid sisaldavad väljagrupid

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Tabeli metaandmete määratluste väljagrupid võivad sisaldada kehtetuid väljaviiteid. Nende väljagruppide juurutamise korral võib see põhjustada käitusaja tõrkeid teenuses Financial Reporting ja Microsoft SQL Serveri aruandlusteenustes (SSRS). Platform update'i 23 lisati kompilaatori *hoiatus*, mis lubas selle metaandmete probleemi lahendamise. Rakenduste Finance and Operations Platformi versiooni 10.0.11 värskendused liigitavad selle probleemi kompilaatori *tõrkena*.<p>Sellep probleemi lahendamiseks tehke järgmist.</p><ol><li>Eemaldage sobimatu väljaviide tabeli väljagrupi definitsioonist.</li><li>Kompileerige uuesti.</li><li>Veenduge, et kõik tõrked oleksid lahendatud.</li></ol> |
| **Asendatud teise funktsiooniga?**   | See kompilaatori tõrge asendab kompilaatori hoiatuse jäädavalt.  |
| **Mõjutatud tootealad**         | Visual Studio arendustööriistad |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | **Aegunud:** kompilaatori hoiatus on Finance and Operationsi rakenduste versiooni 10.0.11 platvormivärskendustes kompilaatori tõrge. |

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

