---
title: Arve hõivamise lahenduse konfiguratsioonigrupid
description: See artikkel annab üldist teavet arve hõivamise lahenduse konfiguratsioonigruppide kohta.
author: sunfzam
ms.date: 09/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690979"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Arve hõivamise lahenduse konfiguratsioonigrupid

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kasutajad saavad hallata arveväljade loendit ja juriidiliste isikute käsitsi ülevaate sätet, kasutades konfiguratsioonigruppe. Kasutajad saavad seadistada arve konfiguratsioone gruppide erinevatele juriidilistele isikutele. Kõik konfiguratsioonigrupis olevad juriidilised isikud kasutavad samu arvevälju ja käsitsi läbivaatuse sätet.

## <a name="manage-configuration-groups"></a>Konfiguratsioonigruppide haldamine

Konfiguratsioonigruppide haldamiseks rakenduse abil minge installiprogrammi ja **valige** seejärel süsteemi häälestuse määratlege **\> konfiguratsioonigruppide komponent**.

**Lehel Konfiguratsioonigruppide** määratlemine kuvatakse põhi vahekaardil määratletud konfiguratsioonigruppide loend. See näitab ka vaikekonfiguratsiooni gruppi. Iga konfiguratsioonigrupi jaoks on saadaval järgmised tegevused:

- **Kopeerige konfiguratsioonigrupp** – saate luua uue konfiguratsioonigrupi olemasolevat gruppi dubleerides. Uuel grupil on samad väärtused, mis originaalgrupil kõigil väljadel, v.a Grupi **nimi ja** **Grupi kirjeldus**. Kui konfiguratsioonigrupp on dubleeritud, valige **OK**.
- **Konfiguratsioonigruppide** kustutamine – konfiguratsioonigrupi kustutamiseks valige see ja seejärel valige **kustuta**.

    > [!NOTE]
    > Vaikekonfiguratsiooni gruppi ei saa kustutada.

- **Redigeerige konfiguratsioonigrupi ID** - konfiguratsioonigrupi ID redigeerimiseks **valige väli Grupi ID** ja värskendage väärtust. Grupi kood ei tohi sisaldada tühikuid ega erimärke ning see ei tohi olla pikem kui 20 märki.

    > [!NOTE]
    > Välja Grupi **ID väärtust** saab uuendada ainult üks kord.

- **Redigeerige konfiguratsioonigrupi kirjeldust** – konfiguratsioonigrupi **kirjelduse redigeerimiseks valige väli** Kirjeldus ja uuendage väärtus.
- **Muuda käsitsi ülevaate sätet** – kasutajad saavad otsustada, kas arve tuleb käsitsi üle vaadata. Käsitsi ülevaate sätte muutmiseks valige suvand Vaja **käsitsi ülevaatamist**. Valikud on järgmised:

    - **Alati käsitsi ülevaade** – tehke see valik, kui konfiguratsioonigrupi arved vajavad alati käsitsi ülevaatamist.
    - **tõrgete ja hoiatuste korral** – tehke see valik, kui veateateid või hoiatusteateid sisaldavad arved vajavad käsitsi ülevaatamist.
    - **Vigade puhul** : valige see suvand, kui tõrketeateid sisaldavad arved vajavad käsitsi ülevaatamist.

- **Muuda usalduspunkti skoori** sätet – enesetunde skoor on metaandmed, mille arvehõive lahendus võimaldab teatada tuvastatud arveandmete täpsusest. Mida kõrgem on punktisumma, seda täpsemad võivad olla tuvastatud andmed. Konfiguratsioon võimaldab kasutajatel määratleda, millal on usaldusniisal põhinevalt vaja käsitsi läbi vaadata. Kasutajad saavad muuta arvete usalduspunkti läve. Usalduspunkti skoori sätte uuendamiseks valige väli **Usaldussumma** ja värskendage väärtust.

    Eneseskoori jaoks on kaks teatisetüüpi:

    - **Hoiatus** – arveväljad, mille usaldussummad ületavad hoiatusläve, on õiged. Hoiatuse lävi peab olema suurem kui tõrkelävi ja väiksem kui 100.
    - **Tõrge** : arveväljad, mille usaldussummad on vealäve all, loetakse nurjutuks. Kasutajale kuvatakse tõrketeated. Tõrkelävi peab olema suurem kui 0 (null) ja väiksem kui hoiatuse lävi. Hoiatusteateid kuvatakse arveväljadel, mille usaldussummad on hoiatusläve ja tõrkeläve vahel.

- **Arveväljade** haldamine – kasutajad saavad hallata arveväljade loendit, mis kuvatakse kõrvutivaaturis. Valige arvevälja **halduse** vahekaardil käigu sümbol, valige lisamiseks arveväljad ja seejärel käsk **Salvesta**. Valitud väljad lisatakse loendisse. Arve välja eemaldamiseks loendist valige **väljal** Eemalda.

### <a name="manage-file-filters-optional"></a>Faili filtrite haldamine (valikuline)

Failifiltrite haldamine võimaldab kasutajatel määratleda sissetulevate arvefailide lisafiltreid. Filtri kriteeriumidele mitte vastavad failid vastu **võetud** ja kuvatakse loendis Saadud failid, kuid kuvatakse faili kinnitamise tõrked. See käitumine erineb kanalis määratletud filtrite käitumisest. Nende filtrite puhul ei saadu enam faile, mis ei vasta kriteeriumidele. Kasutajad saavad sissetulevad failid üle vaadata ja otsustada, kas iga fail on kehtetu arve ja kas nad saavad faili aegunuks muuta või neid käsitsi kaasata tuvastamiseks ja kaasamiseks hõivatud arvetesse.

Kui arvehõive lahendus on installitud, määratakse faili vaikefilter. See failifilter on globaalne. Kui soovite erinevaid filtrisätteid, saate vaikefiltrit uuendada. Kui väli on kohustuslik, valige **nõutav**. 

### <a name="accepted-file-size"></a>Aktsepteeritav failimaht

Saate valida aktsepteeritud failisuuruse.

> [!NOTE]
> Faile, mis on suuremad kui 20 480 kilobaiti (KILOB), ei toetata.

### <a name="supported-file-types"></a>Toetatud failitüübid

Praegu toetatakse järgmisi failitüüpe:

- PDF
- PNG
- JPG
- JPEG
- Tif
- TIFF
