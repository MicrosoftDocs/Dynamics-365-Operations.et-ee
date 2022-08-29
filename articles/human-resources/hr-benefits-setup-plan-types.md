---
title: Plaani tüübi ülevaade
description: Plaani tüüp rakenduses Microsoft Dynamics 365 Human Resources on kindlate soodustuste tüüpide kõrgetasemeline rühmitamine.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ca14156c165ca3f536fc0120ebd03883284eb18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337286"
---
# <a name="plan-type-overview"></a>Plaanitüübi ülevaade

[!include [banner](../includes/preview-banner.md)]

Plaani tüüp on kindlate soodustuste tüüpide kõrgetasemeline rühmitamine. Igal plaani tüübil on plaani tüübi kood, mis määrab plaani tüübi reeglid. Näiteks plaani tüüp **Tavaline elu** olemaks plaani tüübi koodi **Elu**, kuna see sarnaneb elukindlustuse plaanile ja peab vastama plaani tüübi koodis **Elu** määratud reeglitele. Teine plaanitüüp võib olla **Täiendav eluiga**. Sellel plaanitüübil on ka **Elu** plaani tüübi kood.

Iga plaani tüüp näitab, kas töövõtja saab registreeruda ühe seda tüüpi plaaniga või mitmega. Näiteks võib töötaja tõenäoliselt registreeruda plaani tüübi nii **Tavaline elu** kui ka **Täiendav elu** poliisile. Töövõtjal lubatakse tõenäoliselt registreeruda ainult ühe tüübi Meditsiiniline poliisile.

Kui plaani tüüp hõlmab kontakte, siis näitab plaani tüüp, kas kontaktid on kasusaajad või sõltuvad. Näiteks oleksid plaani tüübil **Tavaline elu** kasusaajad, samas kui plaani tüübil Tavaline meditsiiniline oleksid sõltuvad. Mõnel juhul ei tohi plaanis isiklikke kontakte olla. Näiteks Paindlik kasutuskonto või Parkimishüvitis.


Plaani tüüp võib määratleda katvuse valikud. Katvuse valikud määratletakse lehel **Katvuse atribuudid**. Katvuse valik saab määrata soodustuse summa või kontaktid, kes vastavad plaani tüübile. Näiteks kui kontakti tüüp on **Kasusaaja**, peaks katvuse valik määratlema tingimused, mida kasusaaja saab soodustuse kasutamisel saada. Kui kontakti tüüp on **Sõltuv**, peaks katvuse valik määratlema sõltuva ja töövõtja vahelise seose. 

> [!IMPORTANT]
> Lehekülg **Plaani tüüp** sisaldab põhiandmeid, mis mõjutavad uue hüvitiste plaani loomisel saadaolevaid valikuid:
>
> - **Plaani tüübi kood** – see väli mõjutab **konfiguratsiooni** vahekaardil kuvatavat teavet tegeliku hüvitise häälestamisel.  
> - **Samaaegne registreerimine** – see väli määratleb, kas mitu registreerimist on lubatud. (Arstliku plaani puhul on selle välja väärtuseks tavaliselt seatud **Üks registreerimine**.)
> - **Kontakti tüüp** – see väli võimaldab plaani lisada sõltuvaid või kasusaajaid. Kui see on seatud valikule **Puudub**, ei saa soodustuses registreerunud töötajatel valida kas kasusaajat või sõltuvat.
> - **Katvuse valikud** – kasutage seda välja katvuse valikute seostamiseks plaanitüüpidega. See määratleb kas need isikud, kellele see plaanitüüp hõlmab, või katvuse summad, mis on selle plaani tüübi jaoks saadaval. Näiteks võite määrata, et meditsiiniplaani tüübi katvus on saadaval ainult töötajale, töötajale ja veel ühele inimesele või töötajale ja tema perele.

## <a name="create-plan-types"></a>Plaani tüüpide loomine

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
   | **Kindlustussuvandi muutmine** | Määrab, kas töövõtja saab elusündmuse ajal katvuse suvandeid muuta. |
   | **Uue plaani kasutuselevõtmine** | Määrab, kas töövõtja saab elusündmuse ajal plaane muuta. |
   | **Ava kõlblikkuskontroll automaatselt** | Määrab, kas elusündmuse korral taasavatakse automaatselt soodustuse registreerimise kõlblikkuskontroll. |
   | **Elusündmuse registreerimise periood** | Määrab elusündmuse aruandlusakna, päevades. **Märge**: kui te summat ei sisesta, siis süsteem eeldab, et aruandlusaken on null ja ei töötle elusündmust. |
   | **Redigeeritav ainult administraatorite järgi** | Määrab, kas administraatorid saavad plaani elusündmuse ajal tühistada või muuta. Töötaja ei saa töötaja iseteeninduse tööruumis **muudatusi** teha. |
   | **Plaani automaatne tühistamine** | Saate määrata, kas plaan tühistatakse automaatselt elusündmuse ajal. Pärast elusündmuse muudatuste töötlemist säilitab plaani **valimine** automaatse tühistamise plaani valiku. Eemaldatakse ainult **olek** Kinnitatud **või** Välja registreeritud. Plaan jääb valimata. Seetõttu ei kaota plaanivalikut töötajad, kes ei tee plaanivalikuid elusündmuse registreerimise perioodi jooksul. 

5. Valige käsk **Salvesta**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
