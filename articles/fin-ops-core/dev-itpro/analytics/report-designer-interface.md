---
title: Aruande kujundaja liides
description: See artikkel selgitab, kuidas aruandekujundajas navigeerida ja kuidas kasutada erinevaid valikuid teie konkreetsetele nõuetele vastamiseks.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.form: FinancialReports
ms.openlocfilehash: 25d913e6f5d4c95dceda1291a2c33abe37348574
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802738"
---
# <a name="report-designer-interface"></a>Aruande kujundaja liides

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas aruandekujundajas navigeerida ja kuidas kasutada erinevaid valikuid teie konkreetsetele nõuetele vastamiseks.

## <a name="report-designer-menu-commands"></a>Aruandekujundaja menüükäsud

Järgmistes tabelites kirjeldatakse menüükäske ja suvandeid, mida saate finantsaruannete koostamisel kasutada. Mõned menüükäsud ja suvandid on saadaval ainult erandjuhtudel. Näiteks aruandlusüksuste edendamise ja alandamise käsud on saadaval ainult siis, kui aruandluspuu definitsiooni muudate.

### <a name="file-menu"></a>Failimenüü

Menüü **Fail** on saadaval kõigile kasutajatele ja see sisaldab järgmisi käske.

| Käsk                           | Kirjeldus |
|-----------------------------------|-------------|
| Uus                               | Uue aruande definitsiooni, readefinitsiooni, veeru definitsiooni, aruandluspuu määratluse, aruandegrupi definitsiooni või kausta loomine. Olenevalt teie kasutajarollist on saadaval ka lisavalikud. |
| Avatud                              | Olemasoleva readefinitsiooni, veeru definitsiooni, aruandluspuu definitsiooni või aruande definitsiooni avamine. |
| Sulge                             | Praeguse koosteüksuse sulgemine. |
| Sule kõik                         | Kõikide koosteüksuste sulgemine. |
| Salvesta                              | Praeguse readefinitsiooni, veeru definitsiooni, aruandluspuu definitsiooni või aruande definitsiooni salvestamine. |
| Salvesta nimega                           | Praeguse readefinitsiooni, veeru definitsiooni, aruandluspuu definitsiooni või aruande definitsiooni salvestamine uue nimega. |
| Atribuudid                        | Dialoogiboksi **Atribuudid** avamine, kus saate muuta aruande nime ja kirjeldust. |
| Loo                          | Praeguse aruande loomine. See käsk on saadaval aruande definitsioonis. |
| Kuva aruanne                       | Avage kõige värskem loodud aruanne. See käsk on saadaval aruande definitsioonis, kui olete loonud vähemalt ühe aruande. |
| Hiljutised aruandemääratlused         | Hiljuti loodud või muudetud aruannete loendi kuvamine. Seejärel saate loendist aruande valida. |
| Hiljutised readefinitsioonid            | Hiljuti loodud või muudetud readefinitsioonide loendi kuvamine. Seejärel saate loendist readefinitsiooni valida. |
| Hiljutised veerudefinitsioonid         | Hiljuti loodud või muudetud veeru definitsioonide loendi kuvamine. Seejärel saate loendist veeru definitsiooni valida. |
| Hiljutised aruandluspuu definitsioonid | Hiljuti loodud või muudetud aruandluspuu definitsioonide loendi kuvamine. Seejärel saate loendist aruandluspuu definitsiooni valida. |
| Välju                              | Aruande kujundajast väljumine. |

### <a name="edit-menu"></a>Redigeerimismenüü

Menüü **Redigeerimine** on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. See menüü sisaldab järgmisi käske.

| Käsk                                | Kirjeldus |
|----------------------------------------|-------------|
| Ennista                                   | Viimase tegevuse ennistamine. |
| Tee uuesti                                   | Viimase ennistamistegevuse tühistamine. |
| Lõika                                    | Valitud teksti kustutamine ja selle kopeerimine lõikelauale. |
| Kopeeri                                   | Valitud teksti kopeerimine lõikelauale. |
| Kleebi                                  | Viimati lõigatud või kopeeritud teksti sisestamine lõikelaualt. |
| Tühjenda                                  | Valitud koosteüksuse lahtri sisu kustutamine. |
| Otsi                                   | Dialoogiboksi **Otsi ja asenda** avamine, milles saate vaatepaani teksti otsida. |
| Asenda                                | Dialoogiboksi **Otsi ja asenda** avamine, milles saate vaatepaani teksti otsida ja asendada. |
| Lisa dimensioonidest read            | Dialoogiboksi **Sisesta read dimensioonidest** avamine, milles saate valida readefinitsiooni kaasatavad dimensiooniväärtused. See käsk on saadaval readefinitsioonis. |
| Nummerda read uuesti                          | Kõikide numbriliste reakoodide ümbernummerdamine. See käsk on saadaval readefinitsioonis. |
| Rea lingid                              | Dialoogiboksi **Rea lingid** avamine, milles saate määrata andmelinkide allikad readefinitsioonides ja aruandluspuu definitsioonides. See käsk on saadaval readefinitsioonis. |
| Ümarduse korrigeerimine                    | Dialoogiboksi **Ümardamise korrigeerimised** avamine, milles saate määrata ümardamise parameetrid. See käsk on saadaval readefinitsioonis. |
| Halda dimensioonikogumeid                  | Dialoogiboksi **Dimensioonikogumid** avamine, milles saate luua ja muuta dimensioonikogumeid. See käsk on saadaval readefinitsioonis või aruandluspuu definitsioonis. |
| Lisa rida                             | Tühja rea lisamine readefinitsiooni või tühja päiserea lisamine veeru definitsiooni. See käsk on saadaval readefinitsioonis või veeru definitsioonis. |
| Kustuta rida                             | Valitud rea kustutamine readefinitsioonist või valitud päiserea kustutamine veeru definitsioonist. See käsk on saadaval readefinitsioonis või veeru definitsioonis. |
| Lisa veerg                          | Tühja veeru lisamine veeru definitsiooni. See käsk on saadaval veeru definitsioonis. |
| Kustuta veerg                          | Valitud veeru kustutamine veeru definitsioonist. See käsk on saadaval veeru definitsioonis. |
| Dimensioonidest aruandlusüksuste sisestamine | Dialoogiboksi **Sisesta aruandlusüksused dimensioonidest** avamine, milles saate valida aruandluspuu definitsiooni kaasatavad dimensiooniväärtused. See käsk on saadaval aruandluspuu definitsioonis. |
| Dimensioonikogumi hierarhia importimine         | Dialoogiboksi **Impordi dimensioonikogumi hierarhia** avamine, milles saate importida dimensioonikogumi hierarhia finantsandmetest. See käsk on saadaval aruandluspuu definitsioonis süsteemi ..\\financial-dimensions\\dimension-based puhul. |
| Sisesta aruandlusüksus                  | Tühja rea lisamine aruandluspuu definitsiooni. See käsk on saadaval aruandluspuu definitsioonis. |
| Aruandlusüksuse kustutamine                  | Valitud aruandlusüksuse rea kustutamine aruandluspuu definitsioonist. See käsk on saadaval aruandluspuu definitsioonis. |

### <a name="view-menu"></a>Menüü Vaade

Menüü **Vaade** on saadaval kõigile kasutajatele ja see sisaldab järgmisi käske.

| Käsk         | Kirjeldus                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigeerimispaan | Navigeerimispaani kuvamine või peitmine.                                      |
| Tööriistaribad        | Nähtavate tööriistaribade valimine.                                  |
| Olekuriba      | Näitab või peidab olekuteabe aruandekujundaja **aknas**. |
| Tervitusleht    | Avab lehe **Tere tulemast**.                                             |

### <a name="format-menu"></a>Vormingu menüü

Menüü **Vorming** on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. See menüü sisaldab järgmisi käske.

| Käsk               | Kirjeldus |
|-----------------------|-------------|
| Laadid ja vormindamine | Saate avada **dialoogiboksi Laadid ja** vormindamine, kus saate luua ja muuta readefinitsioonide ja veerudefinitsioonide teksti laadi. See käsk on saadaval readefinitsioonis või veeru definitsioonis. |
| Veeru laius          | Saate avada **dialoogiakna** Veeru laius, kus saate seada valitud veeru laiuse. See käsk on saadaval readefinitsioonis, veeru definitsioonis või aruandluspuu definitsioonis. |
| Peida                  | Valitud veeru peitmine. See käsk on saadaval readefinitsioonis, veeru definitsioonis või aruandluspuu definitsioonis. |
| Kuva                | Valitud veergude vaheliste peidetud veergude muutmine nähtavaks. See käsk on saadaval readefinitsioonis, veeru definitsioonis või aruandluspuu definitsioonis. |

### <a name="company-menu"></a>Ettevõtte menüü

Menüü **Ettevõte** on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. See menüü sisaldab järgmisi käske.

| Käsk               | Kirjeldus                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Ettevõtted             | Dialoogiboksi **Ettevõtted** avamine, milles saate ettevõtteid luua ja muuta.                                          |
| Koosteüksuste rühmad | Avage dialoogiboks **Blokeerimisgruppide loomine**, kus saate luua, muuta, importida ja eksportida ehitusplokkide gruppe. |

### <a name="go-menu"></a>Avamise menüü

Menüü **Mine** on kõikidele kasutajatele kättesaadav ning sisaldab järgmisi käske.

> [!NOTE]
> Nende käskude mõju pole nähtav, kui navigeerimispaan pole nähtav.

| Käsud                   | Kirjeldus                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Aruande definitsioonid         | Aruande definitsioonide kuvamine navigeerimispaanil.                                    |
| Readefinitsioonid            | Readefinitsioonide kuvamine navigeerimispaanil.                                       |
| Veeru definitsioonid         | Veeru definitsioonide kuvamine navigeerimispaanil.                                    |
| Aruandluspuu definitsioonid | Aruandluspuu definitsioonide kuvamine navigeerimispaanil.                            |
| Turvalisus                   | Kasutajate, gruppide ja ettevõtete turvalisuse teabe kuvamine navigeerimispaanil. |

### <a name="tools-menu"></a>Tööriistade menüü

Menüü **Tööriistad** on saadaval kõigile kasutajatele, kuid mõne käsu saadavus on piiratud. See menüü sisaldab järgmisi käske.

| Käsk                       | Kirjeldus |
|-------------------------------|-------------|
| Kaitse                       | Parooli rakendamine aktiivsele koosteüksusele. See käsk on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. |
| Aruannete järjekorra olek           | Dialoogiboksi **Aruannete järjekorra olek** avamine, milles näete kõiki hiljuti loodud aruandeid ja iga aruande üksikasju. |
| Lähtesüsteemi teave     | Microsoft Dynamics ERP süsteemi sätete kuvamine. See käsk on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. |
| Väljaregistreeritud üksused             | Praegu avatud readefinitsioonide, veeru definitsioonide, aruandluspuu definitsioonide ja aruande definitsioonide kuvamine. See käsk on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. |
| Värskenda vahemällu talletatud finantsandmed | Finantsdimensioonide veeru andmete värskendamine. |
| Suvandid                       | Dialoogiboksi **Suvandid** avamine, milles saate muuta kasutaja eelistusi aruande kujundaja puhul. |

### <a name="window-menu"></a>Akna menüü

Menüü **Aken** on saadaval kõigile kasutajatele ja see sisaldab järgmisi käske.

| Käsk              | Kirjeldus |
|----------------------|-------------|
| Paani horisontaalselt    | Kõikide avatud akende kuvamine üksteise kõrval. |
| Paani vertikaalselt      | Kõikide avatud akende kuvamine üksteise peal. |
| Virnasta              | Kõikide avatud akende kihitamine nii, et iga akna tiitliriba on nähtav. |
| Külmuta horisontaalselt    | Valitud rea külmutamine nii, et rida oleks kerides aknas endiselt nähtav. See käsk on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. |
| Külmuta vertikaalselt      | Valitud veeru külmutamine nii, et veerg oleks kerides aknas endiselt nähtav. See käsk on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. |
| Avatud akende loend | Avatud akende loendi kuvamine. Akna esiplaanile toomiseks valige aken. |

### <a name="help-menu"></a>Menüü Spikker

Menüü **Spikker** on saadaval kõigile kasutajatele ja see sisaldab järgmisi käske.

| Käsk | Kirjeldus                                                              |
|---------|--------------------------------------------------------------------------|
| Spikker    | Avage spikrilehekülg finantsaruandluses. |
|         |                                                                          |

## <a name="report-designer-toolbar-buttons"></a>Aruandekujundaja tööriistariba nupud
Järgmistes tabelites kirjeldatakse aruannete kujundamisel kasutatavaid tööriistariba nuppe. Mõned tööriistariba nupud on saadaval ainult erandjuhtudel. Näiteks aruandlusüksuste edendamise ja alandamise nupud on saadaval ainult siis, kui aruandluspuu definitsiooni muudate.

### <a name="standard-toolbar"></a>Standardne tööriistariba

Standardne tööriistariba võimaldab kiiret juurdepääsu faili ja redigeerimise käskudele. See tööriistariba sisaldab järgmisi nuppe.

| Nööp                                                                                       | Kirjeldus |
|----------------------------------------------------------------------------------------------|-------------|
| [![Nupp Uus.](./media/rowc130389.png)](./media/rowc130389.png)                              | Uue (tühja) aruande definitsiooni, readefinitsiooni, veeru definitsiooni või aruandluspuu definitsiooni loomine. |
| [![Nupp Ava.](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Olemasoleva readefinitsiooni, veeru definitsiooni, aruandluspuu definitsiooni või aruande definitsiooni avamine. |
| [![Nupp Salvesta.](./media/savec130389.png)](./media/savec130389.png)                           | Praeguse readefinitsiooni, veeru definitsiooni, aruandluspuu definitsiooni või aruande definitsiooni salvestamine. |
| [![Nupp Kopeeri.](./media/copyc130389.png)](./media/copyc130389.png)                           | Valitud teksti kopeerimine lõikelauale. |
| [![Nupp Lõika.](./media/cutc130389.png)](./media/cutc130389.png)                              | Valitud teksti kustutamine ja selle kopeerimine lõikelauale. |
| [![Nupp Kleebi.](./media/pastec130389.png)](./media/pastec130389.png)                        | Teksti lisamine lõikelaualt. |
| [![Nupp Võta tagasi.](./media/undoc130389.png)](./media/undoc130389.png)                           | Viimase tegevuse ennistamine. |
| [![Nupp Tee uuesti.](./media/redoc130389.png)](./media/redoc130389.png)                           | Viimase ennistamistegevuse tühistamine. |
| [![Nupp Otsi.](./media/findc130389.png)](./media/findc130389.png)                           | Dialoogiboksi **Otsi ja asenda** avamine, milles saate aktiivse akna teksti otsida ja asendada. |
| [![Nupp Lisa rida.](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Tühja rea lisamine readefinitsiooni või tühja päiserea lisamine veeru definitsiooni. See nupp on saadaval readefinitsioonis või veeru definitsioonis. |
| [![Nupp Lisa veerg.](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Tühja veeru lisamine veeru definitsiooni. See nupp on saadaval veeru definitsioonis. |
| [![Nupp Lukusta.](./media/lockc130389.png)](./media/lockc130389.png)                           | Parooli rakendamine aktiivsele koosteüksusele. See nupp on saadaval kasutajatele, kellel on roll **Kujundaja** või **Administraator**. |
| [![Nupp Rea link.](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Dialoogiboksi **Rea lingid** avamine, milles saate määrata andmelinkide allikad readefinitsioonides ja aruandluspuu definitsioonides. See nupp on saadaval readefinitsioonis. |
| [![Nupp Ülenda.](./media/promotec130389.png)](./media/promotec130389.png)                  | Aruandluspuu definitsiooni üksuse edendamine. Tütarüksuse valimisel ja seejärel suvandi **Edenda** klõpsamisel teisaldatakse tütarüksus selle emaüksusega samale tasemele. |
| [![Nupp Alanda.](./media/demotec130389.png)](./media/demotec130389.png)                     | Aruandluspuu definitsiooni üksuse alandamine. Üksuse valimisel ja seejärel suvandi **Alanda** klõpsamisel muutub üksus sellele eelneva üksuse tütarüksuseks. |
| [![Nupp Laienda.](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Kõikide aruandluspuu definitsiooni üksuste laiendamine valitud üksuse tasemel. |
| [![Nupp Ahenda.](./media/collapsec130389.png)](./media/collapsec130389.png)               | Aruandluspuu ahendamine. |
| [![Spikri nupp.](./media/helpc130389.png)](./media/helpc130389.png)                           | Spikri avamine. |

### <a name="formatting-toolbar"></a>Vormingu tööriistariba

Vormingu tööriistariba võimaldab lihtsat juurdepääsu laadi käskudele. See tööriistariba sisaldab järgmisi nuppe.

| Nööp                                                                                                       | Kirjeldus                                           |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [![Nupp Fondi laad.](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Valitud fondi laadi rakendamine aktiivsele tekstile.   |
| [![Nupp Font.](./media/fonttype.png)](./media/fonttype.png)                                                 | Praeguse teksti määramine valitud laadile.           |
| [![Nupp Fondi suurus.](./media/fontsize.png)](./media/fontsize.png)                                            | Seadke praegusele tekstile valitud fondi suurus (punktides). |
| [![Nupp Paks kiri.](./media/boldc130389.png)](./media/boldc130389.png)                                           | Praeguse teksti muutmine paksu kirja.                          |
| [![Nupp Kaldkiri.](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Praeguse teksti muutmine kursiivi.                        |
| [![Nupp Allajoonimine.](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Praeguse teksti allakriipsutamine.                          |
| [![Nupp Taande vähendamine.](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Aktiivse teksti taande vähendamine.             |
| [![Nupp Taande suurendamine.](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Aktiivse teksti taande suurendamine.             |
| [![Nupp Taustavärv.](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Aktiivse lahtri taustavärvi muutmine.     |
| [![Nupp Fondi värv.](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Aktiivse teksti värvi muutmine.                |

### <a name="report-designer-toolbar"></a>Aruandekoosturi tööriistariba

Aruandekoosturi tööriistariba võimaldab kiiret juurdepääsu käskudele aruandekoosturis navigeerimiseks. See tööriistariba sisaldab järgmisi nuppe.

| Nööp                                                                                              | Kirjeldus |
|-----------------------------------------------------------------------------------------------------|-------------|
| [![Nupp Aruande definitsioon.](./media/reportc130389.png)](./media/reportc130389.png)            | Menüüs **Aken** loetletud aruande definitsiooni kuvamine. |
| [![Nupp Rea definitsioon.](./media/rowc130389.png)](./media/rowc130389.png)             | Aktiivsele aruande definitsioonile määratud readefinitsiooni kuvamine. |
| [![Nupp Veeru definitsioon.](./media/columnc130389.png)](./media/columnc130389.png)  | Aktiivsele aruande definitsioonile määratud veeru definitsiooni kuvamine. |
| [![Nupp Aruandluspuu definitsioon.](./media/treec130389.png)](./media/treec130389.png)             | Aktiivsele aruande definitsioonile määratud aruandluspuu definitsiooni kuvamine. |
| [![Nupp Aruandevaatur.](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Aruandevaaturi käivitamine ja loodud aruande kõige uuema versiooni kuvamine. See nupp on saadaval aruande definitsioonis, kui olete loonud vähemalt ühe aruande. |
| [![Nupp Koosta aruanne.](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Looge aktiivsest aruandedefinitsioonist aruanne. See nupp on saadaval aruandedefinitsioonis. |

## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandlus](financial-reporting-intro.md)

[Finantsaruannete loomine](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
