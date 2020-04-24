---
title: Plaani tüüpide loomine
description: Plaani tüüp rakenduses Microsoft Dynamics 365 Human Resources on kindlate soodustuste tüüpide kõrgetasemeline rühmitamine. Igal plaani tüübil on plaani tüübi kood, mis määrab plaani tüübi reeglid.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 06a36f9f3fef54e7e06d616c9179374db4ce7115
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229690"
---
# <a name="create-plan-types"></a>Plaani tüüpide loomine

Plaani tüüp rakenduses Microsoft Dynamics 365 Human Resources on kindlate soodustuste tüüpide kõrgetasemeline rühmitamine. Igal plaani tüübil on plaani tüübi kood, mis määrab plaani tüübi reeglid. Näiteks plaani tüüp Tavaline elu olemaks plaani tüübi koodi Elu, kuna see sarnaneb elukindlustuse plaanile ja peab vastama plaani tüübi koodis Elu määratud reeglitele. Teine plaani tüüp võib olla Täiendav elu, mis on samuti koos plaani tüübi koodi Elu.

Iga plaani tüüp näitab, kas töövõtja saab registreeruda ühe seda tüüpi plaaniga või mitmega. Näiteks võib töötaja tõenäoliselt registreeruda plaani tüübi Elu nii Tavaline elu kui ka Täiendav elu poliisile. Töövõtjal lubatakse tõenäoliselt registreeruda ainult ühe tüübi Meditsiiniline poliisile.

Kui plaani tüüp hõlmab kontakte, siis näitab plaani tüüp, kas kontaktid on kasusaajad või sõltuvad. Näiteks oleksid plaani tüübil Tavaline elu kasusaajad, samas kui plaani tüübil Tavaline meditsiiniline oleksid sõltuvad. Mõnel juhul ei tohi plaanis isiklikke kontakte olla. Näiteks Paindlik kasutuskonto või Parkimishüvitis.

Plaani tüüp võib määratleda katvuse valikud. Katvuse valikud määratletakse vormil Katvuse valik. Katvuse valik saab määrata soodustuse summa või kontaktid, kes vastavad plaani tüübile. Näiteks kui kontakti tüüp on Kasusaaja, peaks katvuse valik määratlema tingimused, mida kasusaaja saab soodustuse kasutamisel saada. Kui kontakti tüüp on Sõltuv, peaks katvuse valik määratlema sõltuva ja töövõtja vahelise seose. 

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Plaani tüübid**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Plaani tüüp** | Kordumatu nimi, mis tuvastab plaani tüübi. |
   | **Kirjeldus** | Plaani tüübi kirjeldus. |
   | **Plaani tüübi kood** | Valige väärtuse ripploendist plaani tüübi kood. Plaani tüübi koodi loend kuvab kõik plaani tüübid, mis on praeguses versioonis toetatud. |
   | **Samaaegne registreerimine** | Määrab, kas töövõtja saab registreerida sama plaanitüübi kohta mitu soodustusplaani või ainult ühe soodustusplaani. |
   | **Kontakti tüüp** | Määratleb isikliku kontakti rolli. Väärtused on tühi, Sõltuv ja Kasusaaja. Kui nende plaani tüüp ei nõua katvuse valiku põhjal sõltuvat või kasusaajat, võite jätta **kontakti tüübi** tühjaks. |

4. Elusündmuse suvandite konfigureerimiseks valige **Toimingud** ja seejärel valige suvand **Elusündmuse suvandid**. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Plaani tüüp** | Plaani tüüp, millele elusündmuse suvandeid konfigureerida. |
   | **Elusündmuse tüübi ID** | Elusündmuse tüübi ID. |
   | **Luba tühistamine** | Määrab, kas töövõtja saab elusündmuse ajal soodustusplaani tühistada. |
   | **Kindlustussuvandi muutmine** | Määrab, kas töövõtja saab elusündmuse ajal katvuse suvandeid muuta. |
   | **Uue plaani kasutuselevõtmine** | Määrab, kas töövõtja saab elusündmuse ajal plaane muuta. |
   | **Plaani automaatne tühistamine** | Määrab, kas tühistada plaan elusündmuse ajal automaatselt. |
   | **Ava kõlblikkuskontroll automaatselt** | Määrab, kas elusündmuse korral taasavatakse automaatselt soodustuse registreerimise kõlblikkuskontroll. |
   | **Aruandlusaken** | Määrab elusündmuse aruandlusakna, päevades. **Märge**: kui te summat ei sisesta, siis süsteem eeldab, et aruandlusaken on null ja ei töötle elusündmust. |

5. Valige käsk **Salvesta**. 
