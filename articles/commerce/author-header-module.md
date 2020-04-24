---
title: Päise moodul
description: See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261440"
---
# <a name="header-module"></a>Päise moodul


[!include [banner](includes/banner.md)]

See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce'i lehe päis koosneb mitmest moodulist, nagu päis, navigeerimismenüü, otsing, reklaambänner ja küpsistega nõustumise moodulid. 

Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi sümbolit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba. Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade). Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).

## <a name="properties-of-a-header-module"></a>Päise mooduli atribuudid

Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**. 

Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**. Lisateavet vt jaotisest [Logo lisamine](add-logo.md). 

Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.

## <a name="modules-that-are-available-in-a-header-module"></a>Päise moodulis saadaolevad moodulid

Päise moodulis saab kasutada järgmisi mooduleid.

- **Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke. Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Commerce. Navigeerimise menüül on atribuut **Navigeerimise allikas**, mida kasutatakse jaemüügi serveri navigatsiooni menüü elementide ja staatilise menüü elementide määramiseks allikana. Kui allikana on määratud staatilised menüü-elemendid, saab esitada seotud linke teistele saidi lehekülgedele. Konfigureeritud üksused ilmuvad seejärel päise navigeerimises. 
- **Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks. Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**. Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada. Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.
- **Ostukorvi ikoon** – ostukorvi ikooni moodul tähistab ostukorvi ikooni, mis näitab ostukorvis olevate kaupade arvu igal ajahetkel. Lisateavet vt teemast [Ostukorvi ikooni moodul](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Lehele päise mooduli loomine

Päise mooduli loomiseks tehke järgmist.

1. Looge fragment nimega **Päise fragment** ja lisage sellele konteineri moodul.
1. Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.
1. Lisage konteineri moodulile reklaambänner ja küpsistega nõustumise moodulid.
1. Lisage fragmendile veel üks konteineri moodul ja seadistage atribuudi **Laius** väärtuseks **Täida konteiner**.
1. Lisage teisele konteineri moodulile päise moodul.
1. Lisage päise mooduli pesasse **Navigeerimise menüü** navigeerimise menüü moodul. 
1. Konfigureerige navigatsioonimenüü atribuudi paanil navigatsioonimenüü mooduli atribuudid.
1. Lisage päise mooduli pesasse **Otsing** otsingu moodul. 
1. Konfigureerige otsingumooduli atribuudi paanil otsingumooduli atribuudid. 
1. Lisage ostukorvi ikooni moodul päisemooduli pesasse **Ostukorvi ikoon**. 
1. Konfigureerige ostukorvi ikooni mooduli atribuudi paanil ostukorvi ikooni mooduli atribuudid. Kui soovite, et ostukorvi ikoonil hõljutamisel kuvatakse väike ostukorv, valige sätte **Kuva väike ostukorv** jaoks väärtus **Tõene**.
1. Salvestage lehe fragment, lõpetage selle redigeerimine ja seejärel avaldage see. 


Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.

1. Lisage vaikelehe pesasse **Peamine** päise lehe fragment, mis sisaldab päise päise moodulit.
1. Salvestage mall, lõpetage selle redigeerimine ja seejärel avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteineri moodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
