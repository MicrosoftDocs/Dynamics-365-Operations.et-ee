---
title: Elektroonilise arvelduse ülevaade
description: See teema annab ülevaate Elektroonilise arveldamise kohta Microsoftis ja Dynamics 365 Finance Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23a98706bc2ab0abc2c72e9f20d8e8fbff56b2b9
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371450"
---
# <a name="electronic-invoicing-overview"></a>Elektroonilise arvelduse ülevaade

[!include [banner](../includes/banner.md)]

Microsofti elektrooniline arveldamine Dynamics 365 Finance ja Dynamics 365 Supply Chain Management on microsoftile skaleeritav mitme andmebaasi teenus, mis võimaldab konfigureeritavat elektrooniliste arvete töötlemist ja konfigureeritavat elektroonilise dokumendivahetust. Töötlemis- ja integratsioonireeglid on täielikult konfigureeritavad ning loogikat käitatakse väljaspool rakendusi Finance ja Supply Chain Management. Teenus on suunatud peamiselt elektrooniliste arvedokumentide töötlemisele ettevõtete vahel ettevõtete vahel. Kuid seda saab konfigureerida ka muudel eesmärkidel, nt ettevõtete vahel eri tüüpi dokumentide puhul.

Elektrooniline arveldus aitab teil saavutada järgmisi eesmärke:

- Riigi-/regioonipõhiste nõuete kiire ja hõlbus kasutuselevõtt
- Elektroonilise arvelduse lahenduse standardiseeritud juurutamine
- Dokumendiajaloo täiustatud jälgitavus
- Lühem juurutustsükkel
- Väiksem omanduse kogukulu (TCO)
- Kohandatavad konfiguratsioonid, mis ei nõua koodimuudatust
- Lihtsustatud konfiguratsioonipakett
- Integreeritud eksport, import ja integratsioon ning lihtne laiendatavus elektrooniliste arvedokumentide töötlemisel
- Ekspordi-, impordi- ja integratsioonikonfiguratsioonide lihtne taaskasutamine ettevõtete vahel

## <a name="service-availability"></a>Teenuse saadavus

Praegu on elektroonilise arvelduse funktsioon saadaval finants- ja tarneahela halduse klientidele. Lisateavet vaadake rakenduse litsentsitingimustest.

Kuna funktsioon, mis aadressib riigi-/regioonispetsiifilisi nõudeid, võib olla piiratud vabastamise erinevates etappides, peaksite alati üle vaatama kõige ajaomased dokumendid, mis tõstavad esile toetatud riigi-/regioonispetsiifiliste lahenduste laovarude ja ulatuse.

Elektrooniline arveldus juurutatakse järgmistes Azure'i geograafilistes piirkondades:

- Ameerika Ühendriigid
- Euroopa
- Aasia

> [!NOTE]
> Elektrooniline arveldus ei toeta kohapealseid juurutusi.

## <a name="feature-highlights"></a>Esiletõstetud funktsioonid

- Boksist välja integreerimine finants- ja tarneahelahaldusega
- Järjepidev kasutajakogemus elektroonilise arve protsessi konfigureerimisel ja jälgimisel kõigi riikide ja piirkondade puhul
- Kiirema, lihtsama ja odavama Elektroonilise arvelduse lahenduse kohandamine uutele riikidele või piirkondadele
- Teenuse konfiguratsioon regulatiivsete konfiguratsiooniteenuste (RCS) ja globaliseerimisfunktsiooni seadistuse kaudu
- Äriandmete teisendamine mitmeks elektroonilise arve vorminguks (XML, JavaScripti objekti notation \[JSON\], TXT ja komaga eraldatud väärtused CSV\[) RCS-is \] määratletud konfiguratsioonide abil:

    - Elektroonilise aruandluse (ER) vormingud, mis on saadaval riikide ja regioonide jaoks, kus konfigureeritavus elektroonilise arve teisendamiseks pole saadaval

- Konfigureeritav elektrooniliste arvete esitamine välistele veebiteenustele, sh sertifikaadi töötlemine digitaalallkirjade kaudu:

    - Integreeritud, hõlpsasti laiendatav ja konfigureeritav integratsioon mitme riigi ja regiooni lisasisuga

- Veebiteenuste vastuste töötlemine, sh erandteadete konfigureeritav käsitsemine
- Digitaalallkirjade tugi (nt digitaalallkirjad, mis kasutavad XMLDSig allkirjastamisalgoritmi)
- Võimalus saata dokumente e-kirjadele ja salvestada need SharePoint
- Elektrooniliste arveteadete pakktöötlus
- Konfigureeritav sissetulevate dokumentide teisendamine ja nende dokumentide töötlemine finants- ja tarneahela halduses
- Võime vastu võtta sissetulevaid dokumente kanalitest, nagu meil ja SharePoint

## <a name="privacy-notice"></a>Privaatsusavaldus

Elektroonilise arveldamise lubamine ja kasutamine võib nõuda piiratud andmete saatmist. Need andmed hõlmavad organisatsiooni maksuregistreerimise ID-d. Need andmed edastatakse kolmanda osapoole asutused, mille maksuametid on volitanud saatma elektroonilisi arveid eelmääratletud vormingutes, mida on vaja integratsiooniks valitsuse veebiteenustega. Andmed, mis imporditakse nendest välissüsteemidest sellesse Dynamics 365 võrguteenusse, kuuluvad meie [privaatsusavaldusele](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet vt jaotisest "Privaatsusteatis" riigi-/regioonispetsiifilises funktsioonidokumentatsioonis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
