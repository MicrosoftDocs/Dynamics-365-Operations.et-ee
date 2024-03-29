---
title: Elektrooniline sõnumside
description: See artikkel annab ülevaate ja häälestuse teabe elektroonilise sõnumite jaoks Microsoft Dynamics 365 Finantsis.
author: AdamTrukawka
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3e2fe6a70d449adea07f5aa0db9e625f0378d8c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283450"
---
# <a name="electronic-messaging"></a>Elektrooniline sõnumside

[!include [banner](../includes/banner.md)]

See artikkel annab ülevaate ja seadistusteabe elektrooniliste **teadete** (EM) funktsioonide kohta.

Hiljuti kehtestasid erinevate riikide ja piirkondade valitsused ja seadusandlikud asutused üle kogu maailma aruandlusnõuded ettevõtetele, kes on nendes riikides või piirkondades registreeritud. Nende nõuete eesmärk on hankida nendelt ettevõtetelt elektroonilises vormingus andmeid, otse süsteemist, kus neid arvutatakse, hoiustatakse ja töödeldakse.

365 Finantside EM-funktsioonid Microsoft Dynamics toetavad mitmesuguseid finantside ja valitsusasutuste vahelise elektroonilise ristluse protsesse aruandluseks, esitamiseks ja ametliku teabe saamiseks.

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

## <a name="security-privileges"></a>Turbeprivileegid

Elektrooniliste teadete jaoks on saadaval järgmised turva privileegid.

| Turvalisuse privileeg           | Juurdepääsu tase | Seos |
|------------------------------|--------------|-------------|
| Elektronsõnumite haldamine | See privileeg annab täieliku juurdepääsu EM-funktsioonile. Kui teil on see privileeg, saate seadistada elektroonilise sõnumside ja käivitada kogu töötluse. | See privileeg on kaasatud **Maksu müügitehingute säilitamine** turvakohustuste hulka. See kohustus sisaldub omakorda **raamatupidaja** turberollis. |
| Elektronsõnumite kuvamine     | See privileeg annab kirjutuskaitstud juurdepääsu EM-funktsioonile. Kui teil on see privileeg, saate vaadata elektroonilise sõnumside seadeid ja sõnumeid. Te ei saa siiski midagi seadistada ega käivitada. | See privileeg sisaldub **Päring müügimaksu tehingute staatuses** turvakohustuste hulka. See kohustus sisaldub omakorda järgmistes turberollides:<ul><li>Sissenõuete haldur</li><li>Müügireskontro ametnik</li><li>Müügireskontro haldur</li><li>Maksuametnik</li><li>Raamatupidaja</li><li>Pearaamatupidaja</li><li>Raamatupidaja</li><li>Müügijuht</li><li>Ostureskontro ametnik</li></ul> |
| Tööta elektronsõnumitega  | See privileeg annab juurdepääsu ainult **elektrooniliste teadete** ja **elektrooniliste teadete kaupade** lehtedele. Kui teil on see privileeg, saate käivitada kogu töötlemise, mis on kutsutud neilt lehtedelt. | See privileeg kuulub turvakohustustesse **Elektrooniliste teadete haldamine**. See kohustus sisaldub omakorda **Elektrooniliste sõnumite operaator** turberollis. |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>EM-funktsiooni toetatud riigispetsiifilised regulatiivsed funktsioonid

Järgmises tabelis antakse teavet mõnede RIIGIspetsiifiliste regulatiivsete funktsioonide kohta, mida EM-i funktsioonid toetavad.

| Riik     | Funktsiooni nimi | Funktsiooni demo salvestamine |
|-------------|--------------|------------------------|
| Hispaania       | [KM-i kohene teave (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungari     | [Veebipõhine arveldussüsteem](../localizations/emea-hun-online-invoicing.md) | |
| Ühendkuningriik | [KM-aruande esitamismuudatused (maksude digitaalseks muutmine)](../localizations/emea-gbr-mtd-vat-integration.md) | [Finantsid ja toimingud: UK digitaalne maks – KM-i deklaratsioon Dynamics 365-s](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Leedu   | [i.SAF-aruandlus](../localizations/emea-ltu-isaf.md) | |
| Poola      | [Käibemaksudeklaratsioon registritega (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finantsid: SAF/JPK KM-i auditi registrid](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Holland | [Käibemaksudeklaratsioon Hollandi jaoks](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tšehhi Vabariik | [Käibemaksudeklaratsioon](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasiilia      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Venemaa      | [Käibemaksudeklaratsioon](../localizations/rus-vat-declaration.md) | |
| Venemaa      | [Raamatupidamise elektrooniline aruandlus](../localizations/rus-accounting-reporting.md) | |
| Venemaa      | [Kasumi maksudeklaratsioon](../localizations/rus-profit-tax-declaration.md) | |
| Venemaa      | [Otsese maksu deklaratsioon](../localizations/rus-assessed-tax-declaration.md) | |
| Venemaa      | [Transpordimaksu deklaratsioon](../localizations/rus-transport-tax-declaration.md) | |
| Venemaa      | [Maamaksu deklaratsioon](../localizations/rus-land-tax-declaration.md) | |
| Norra      | [Käibemaksutagastus otseedastusega Altinnile](../localizations/emea-nor-vat-return.md) | [Uus KM-i tagastus otseedastusega Dynamics 365 Finantside Altinnile](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| Prantsusmaa      | [KM-i deklaratsioon (Prantsusmaa)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| Austria     | [KM-i deklaratsioon (Austria)](../localizations/emea-aut-vat-declaration-austria.md) | |
| Saksamaa     | [KM-i deklaratsioon (Saksamaa)](../localizations/emea-deu-vat-declaration-germany.md) | |
| Holland | [Käibemaksudeklaratsioon Hollandi jaoks](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Rootsi      | [KM-i deklaratsioon (Rootsi)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| Šveits | [KM-deklaratsioon (Šveits)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


