---
title: Sisupaigutuse moodul
description: See teema hõlmab sisupaigutuse ja sisupaigutuse üksuse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785296"
---
# <a name="content-placement-module"></a>Sisupaigutuse moodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab sisupaigutuse ja sisupaigutuse üksuse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Sisupaigutuse moodul on erikonteiner, kuhu saab lisada teised moodulid konkreetses paigutuses. Sisupaigutuse moodulid toetavad järgmist tüüpi mooduleid, nagu järgmised alammoodulid: sisupaigutuse üksus, konto tervituse üksus, konto tellimise üksus, konto soovinimekirja üksus ja konto profiili üksus.

Sisupaigutuse moodulid tuletavad andmeid nende toetatud alammoodulitest. Seetõttu saab sisupaigutuse mooduleid kasutada mitmel viisil, olenevalt sellele lisatavatest moodulitest.

Sisupaigutuse üksuse moodulid kasutavad nii pilte kui ka teksti, et tutvustada kampaaniaid, eeskirju ja toote funktsioone. Näiteks saab sisupaigutuse üksuse moodulit kasutada avalehel poe eeskirjade või tarneteabe kuvamiseks. Sisupaigutuse üksuse moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele. Samas saab neid kasutada ainult sisupaigutuse mooduli sees.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>E-kaubanduse sisupaigutuse moodulite näited

* Sisupaigutuse mooduleid, mis sisaldavad sisupaigutuse üksuse mooduleid, saab kasutada avalehel või turunduse lehtedel, et tutvustada nii piltide kui ka teksti kaudu tootefunktsioone, kampaaniaid, poe eeskirju, tarneteavet ja muud teavet.
* Sisupaigutuse mooduleid, mis sisaldavad sisupaigutuse üksuse mooduleid, saab kasutada toote üksikasjade lehtedel, et tutvustada toote omadusi.
* Sisuhalduse moodulid, mis sisaldavad konto tervitamise üksuse või konto tellimise üksuse mooduleid, saab kasutada kontohalduse lehtedel.

## <a name="content-placement-module-properties"></a>Sisupaigutuse mooduli atribuudid

| Atribuudi nimi | Väärtus | Kirjeldus |
|---------------|-------|-------------|
| Laius         | **Mahuta konteinerisse** või **Täida ekraan** | Kui väärtuseks on seatud **Mahuta konteinerisse**, on sisupaigutuse moodulis olevad kaubad piiratud sisupaigutuse mooduli laiusega. Kui väärtuseks on seatud **Täida ekraan**, ei ole kaubad sisupaigutuse mooduli laiusega piiratud, vaid võivad minna täisekraani režiimi. |

## <a name="content-placement-item-module-properties"></a>Sisupaigutuse üksuse mooduli atribuudid

| Atribuudi nimi | Väärtus | Kirjeldus |
|---------------|-------|-------------|
| Pealkiri       | Pealkirja tekst ja pealkirja sildid (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Igal sisupaigutuse üksuse moodulil võib olla pealkiri. Atribuut **Pealkirja** toetab pealkirja silte. Vaikimisi kasutatakse pealkirja silti **H2**, kuid pealkirja silti saab vajadusel muuta juurdepääsu nõuetele vastavaks. |
| Lõik     | Lõigu tekst | Sisupaigutuse üksuse moodulid toetavad RTF-vormingus lõigu teksti. Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst ning hüperlingid. Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile. |
| Pilt         | Pildifail | Tekstiga saab seostada pildi. |
| Seos          | Lingi URL ja lingi tekst | Tekstile saab lisada lingi, et suunata kasutajad ümber kindlale lehele. |
| Paani suurus     | Number vahemikus **1** kuni **12** | Iga sisupaigutuse üksuse puhul määratleb see atribuut pesade arvu, mille üksus peab sisupaigutuse moodulis täitma. Sisupaigutuse mooduli maksimaalne suurus on 12 pesa. Kui sisupaigutuse mooduli esimese *n* üksuse paani kogusuurus ületab 12 pesa, murtakse üksuse teksti read järgmisele reale. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Sisupaigutuse mooduli lisamine, mis sisaldab lehe sisupaigutuse üksuse moodulit

Uuele lehele sisupaigutuse mooduli lisamiseks, mis sisaldab sisupaigutuse üksuse moodulit, ja nõutavate atribuutide määramiseks, toimige järgmiselt.

1. Looge mall nimega **sisupaigutuse mall**.
1. Lisage vaikelehe pessa **Peamine** sisupaigutuse moodul.
1. Lisage sisupaigutuse moodulis sisupaigutuse üksuse moodul.
1. Registreerige mall ja avaldage see.
1. Kasutage äsja loodud sisupaigutuse malli, et luua leht, mille nimi on **Sisupaigutuse leht**.
1. Lisage uue lehe pessa **Peamine** sisupaigutuse moodul.
1. Lisage sisupaigutuse moodulis sisupaigutuse üksuse moodul.
1. Sisupaigutuse üksuse mooduli atribuutide paanil valige pilt, lisage pealkiri, lisage lõik, lisage link, määrake lingi URL ja määrake paani suuruseks **6**.
1. Korrake samme 7 ja 8, et lisada teine sisupaigutuse üksuse moodul, millel on sama paani suurus.
1. Salvestage ja kuvage lehe eelvaade. Peaksite nägema kahte sisupaigutamise üksust, mis kuvatakse kõrvuti. Saate kohandada iga sisupaigutuse üksuse mooduli atribuuti **Paani suurus** või lisada rohkem mooduleid, et saavutada soovitud paigutus.
1. Registreerige leht ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Teatise moodul](add-alert.md)

[Karusellmoodul](add-carousel.md)

[Sisurikas plokimoodul](add-content-rich-block.md)

[Funktsioonimoodul](add-feature-module.md)

[Pannoomoodul](add-hero-module.md)

[Videopleieri moodul](add-video-player.md)
