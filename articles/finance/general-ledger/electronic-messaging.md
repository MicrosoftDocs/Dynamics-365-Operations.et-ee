---
title: Elektrooniline sõnumside
description: Selles teemas antakse elektroonilise sõnumside ülevaade ja seadistusteave rakenduses Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 339e0c811a70ca6b722d8967c2df103500578664
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433715"
---
# <a name="electronic-messaging"></a>Elektronsõnumid

[!include [banner](../includes/banner.md)]

Selles teemas antakse **elektroonilise sõnumside** (EM) ülevaade ja seadistusteave.

Hiljuti kehtestasid erinevate riikide ja piirkondade valitsused ja seadusandlikud asutused üle kogu maailma aruandlusnõuded ettevõtetele, kes on nendes riikides või piirkondades registreeritud. Nende nõuete eesmärk on hankida nendelt ettevõtetelt elektroonilises vormingus andmeid, otse süsteemist, kus neid arvutatakse, hoiustatakse ja töödeldakse.

Elektroonilise sõnumside funktsionaalsus Microsoft Dynamics 365 Finance toetab erinevaid protsesse elektrooniliseks koostalitluseks rakenduse Finance ning süsteemide vahel, mida valitsused ja seadusandlikud asutused pakuvad ametliku teabe aruandluseks, esitamiseks ja saamiseks.

Elektroonilise sõnumside funktsionaalsus on integreeritud **elektroonilise aruandluse** (ER) mooduliga. Seetõttu saate elektronsõnumite jaoks seadistada ER-vormingud. Lisateabe saamiseks vt [Elektrooniline aruandlus (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>EM-funktsiooni põhimõisted

EM-i funktsioonid põhinevad järgmistel üksustel:

- **Elektrooniline teade** – aruanne või deklaratsioon, mille kohta tuleb esitada või edastada ettevõttesiseselt, nmaksuametile saadetav aruanne.
- **Elektronsõnumi üksused** – kirjed, mis tuleb kaasata esitatavasse sõnumisse.
- **Elektronsõnumi töötlemine** – tegevuste ahel, mis tuleb käivitada vajalike andmete kogumiseks, aruannete loomiseks, andmete talletamiseks Azure Blob mälus, aruannete edastamiseks väljapoole süsteemi, vastuste saamiseks väljastpoolt süsteemi ning andmebaasi värskendamiseks saadud teabe põhjal. Ahela tegevused võivad olla lingitud või linkimata.

Järgmine illustratsioon näitab kliendiandmete elektrisõnumi voogu.

![Elektroonilise sõnumside andmevoog.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>EM-funktsiooni toetatud stsenaariumid

Elektronsõnumite funktsioon toetab järgmisi stsenaariume:

- Sõnumite loomine ja aruannete koostamine, mis põhinevad eri tüüpi seostatud eksportimise ER-vormingutel. Nende tüüpide seas on Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst ja Microsoft Word.
- Sõnumite, mis põhinevad teabel, mida taotleti ja saadi asutuselt seostatud importimise ER-vormingu kaudu, automaatne loomine ja töötlemine.
- Teabe kogumine ja töötlemine andmeallikast sõnumiüksustena. Andmeallikas on rakenduse Rahandus tabel.
- Täiendava teabe talletamine ja erinevate väärtuste hindamine, kutsudes eraldi määratletud täidetavad klassid seoses sõnumite või sõnumiüksustega.
- Teabe koondamine, mis on kogutud sõnumiüksustes, selle teabe tükeldamine sõnumite järgi ja aruannete loomine, mis on seotud eksporditavate ER-vormingutega.
- Koostatud aruannete edastamine veebiteenusele, kasutades turbeteavet, mis on talletatud rakenduse Azure võtmehoidlasse.
- Vastuse saamine veebiteenuselt, vastuse tõlgendamine ja andmete värskendamine rakenduses Rahandus vajadust mööda.
- Loodud aruannete talletamine ja ülevaatamine.
- Kogu logiteabe talletamine ja ülevaatamine, mis on seotud tegevustega, mis käivitatakse sõnumi või sõnumiüksuse jaoks.
- Töötlemise kontrollimine erinevate sõnumi ja sõnumiüksuse olekutega.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>EM-funktsiooni toetatud riigispetsiifilised regulatiivsed funktsioonid

Järgmises tabelis antakse teavet mõnede RIIGIspetsiifiliste regulatiivsete funktsioonide kohta, mida EM-i funktsioonid toetavad.

| Riik     | Funktsiooni nimi | Funktsiooni demo salvestamine |
|-------------|--------------|------------------------|
| Hispaania       | [KM-i kohene teave (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungari     | [Veebipõhine arveldussüsteem](../localizations/emea-hun-online-invoicing.md) | |
| Ühendkuningriik | [KM-aruande esitamismuudatused (maksude digitaalseks muutmine)](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: Ühendkuningriigi digitaalmaks – KM-i deklaratsioon Dynamics 365-s](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Leedu   | [i.SAF-aruandlus](../localizations/emea-ltu-isaf.md) | |
| Poola      | [Käibemaksudeklaratsioon registritega (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK KM-i auditi registrid](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Holland | [Käibemaksudeklaratsioon Hollandi jaoks](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tšehhi Vabariik | [Käibemaksudeklaratsioon](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasiilia      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Venemaa      | [Käibemaksudeklaratsioon](../localizations/rus-vat-declaration.md) | |
| Venemaa      | [Raamatupidamise elektrooniline aruandlus](../localizations/rus-accounting-reporting.md) | |
| Venemaa      | [Kasumi maksudeklaratsioon](../localizations/rus-profit-tax-declaration.md) | |
| Venemaa      | [Otsese maksu deklaratsioon](../localizations/rus-assessed-tax-declaration.md) | |
| Venemaa      | [Transpordimaksu deklaratsioon](../localizations/rus-transport-tax-declaration.md) | |
| Venemaa      | [Maamaksu deklaratsioon](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

