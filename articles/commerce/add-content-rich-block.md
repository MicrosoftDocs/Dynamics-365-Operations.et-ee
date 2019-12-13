---
title: Sisurikas plokimoodul
description: See teema hõlmab sisurikkaid plokimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785417"
---
# <a name="content-rich-block-module"></a>Sisurikas plokimoodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab sisurikkaid plokimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Sisurikas plokimoodul on erikonteiner, kuhu saab lisada ühe või mitu sisurikka ploki üksust. Sisurikkaid plokimooduleid kasutatakse lehe tekstiliseks sisuks. See sisu võib olla kas teavitav või kampaaniaga seotud.

Sisurikkad plokimoodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele. Need on eraldiseisvad moodulid, mis ei sõltu lehekülje kontekstist ega ühestki teisest moodulist.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>E-kaubanduse sisurikaste plokimoodulite näited

Sisurikkaid plokimooduleid saab kasutada järgmistel viisidel.

* Toote üksikasjade lehel toote funktsioonide tutvustamiseks.
* Teavitamise eesmärgil mis tahes lehel. Näiteks võivad need selgitada püsikliendiprogrammide eeliseid, kirjeldada tarne- ja tagastamispoliitikaid, vastata korduma kippuvatele küsimustele või lisada sisu osale „Tutvustus”.
* Lisada toote üksikasjade lehele kohandatud sõnumeid. (nt „Üle 50 euro maksvad tellimused tarnitakse tasuta”).
* Lahtiütluste ja kontaktandmete jaoks toote üksikasjade lehtedel, ostukorvi lehtedel, maksmise lehtedel ja teistel lehtedel (nt „Tarnimisele ja tagastustele kehtivad poe eeskirjad”).

## <a name="content-rich-block-module-properties"></a>Sisurikka plokimooduli atribuutide sisu

| Atribuudi nimi     | Väärtus                                 | Atribuut |
|-------------------|---------------------------------------|----------|
| Veergude arv | Number vahemikus **1** kuni **4**     | Sisurikka ploki veergude arv. Seal võib olla kuni neli veergu. |
| Laius             | **Täida konteiner** või **Täida ekraan** | Kui väärtuseks on seatud **Täida konteiner**, on konteineris olevad kaubad piiratud konteineri laiusega. Kui väärtuseks on seatud **Täida ekraan**, ei ole kaubad konteineri laiusega piiratud, vaid võivad minna täisekraani režiimi. Soovitud paigutuse saavutamiseks saate väärtust muuta. |

## <a name="content-rich-block-item-module-properties"></a>Sisurikka ploki kauba mooduli atribuutide sisu

| Atribuudi nimi | Väärtus          | Kirjeldus |
|---------------|----------------|-------------|
| Lõik     | Lõigu tekst | Iga sisurikka bloki kaupa saatev tekst. Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Sisurikka plokimooduli lehele lisamine

Uuele lehele sisurikka plokimooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge lehe mall nimega **Sisu mall**.
1. Lisage vaikelehe pessa **Peamine** sisurikas plokimoodul.
1. Registreerige mall ja avaldage see.
1. Kasutage äsja loodud sisu malli, et luua leht, mille nimi on **Sisu leht**.
1. Lisage uue lehe pessa **Peamine** sisurikas plokimoodul.
1. Määrake sisurikka plokimooduli atribuutides veergude arvuks **2**.
1. Valige sisurikka plokimooduli sisus suvand **Lisa moodul** ja lisage sisurikka ploki kauba sisu (näiteks **kaup1**).
1. Lisage uues sisurikkas ploki üksuses uus sisu ja paragrahvi tekst.
1. Valige sisurikka plokimooduli sisus suvand **Lisa moodul** ja lisage sisurikka ploki kauba sisu (näiteks **kaup2**).
1. Lisage uues sisurikkas ploki üksuses uus sisu ja paragrahvi tekst.
1. Salvestage leht ja kuvage muudatuste eelvaade. Peaksite nägema kahte rikasteksti plokki kahe veeruga vaates.
1. Registreerige leht ja avaldage see.

> [!NOTE]
> Kui lisate kolmanda rikasteksti ploki üksuse, virnastatakse see kahe eelnevalt lisatud üksuse alla. Muutes veergude ja konteineris olevate üksuste arvu, võite saavutada tekstisisu erinevad paigutused.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Teatise moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Sisupaigutuse moodul](add-content-placement-modules.md)

[Funktsioonimoodul](add-feature-module.md)

[Pannoomoodul](add-hero-module.md)

[Videopleieri moodul](add-video-player.md)

