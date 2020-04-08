---
title: Ostukorvi moodul
description: See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154013"
---
# <a name="cart-module"></a>Ostukorvi moodul

[!include [banner](includes/banner.md)]

See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Ostukorvi moodul näitab ostukorvi lisatud kaupasid enne, kui klient on kassasse läinud. Moodul näitab ka ostu kokkuvõtet ja võimaldab kliendil rakendada või eemaldada kampaaniakoode.

Ostukorvi moodul toetab sisselogitud ostu ja külalisostu. Samuti toetab see linki **Tagasi ostlema**. Saate konfigureerida selle lingi marsruudi jaotises **Saidi sätted \> Laiendused \> Marsruudid**.

Ostukorvi moodul renderdab andmed ostukorvi ID põhjal, mis on üle kogu saidi saadaval brauseri küpsis.

## <a name="cart-module-properties-and-slots"></a>Ostukorvi mooduli atribuudid ja pesad

Ostukorvi moodulis on atribuut **Pealkiri**, mida saab seadistada sellistele väärtustele nagu **Ostukorv** ja **Ostukorvis olevad kaubad**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moodulid, mida saab ostukorvi moodulis kasutada

- **Tekstiplokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid. Sõnumeid juhib sisuhaldussüsteem (CMS). Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.
- **Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas. See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused. Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).

## <a name="cart-module-settings"></a>Ostukorvi mooduli sätted

Ostukorvi moodulitel on järgmised seadistused, mida saab konfigureerida jaotises **Saidi sätted \> Laiendused**.

- **Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks. Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.
- **Varude kontroll** – kui väärtus on satud suvandile **Tõene**, saab kauba lisada ostukorvi ainult pärast seda, kui ostukasti moodul on veendunud, et see oleks laos olemas. See varude kontroll tehakse nii stsenaariumide jaoks, kus kaup saadetakse, kui ka stsenaariumide jaoks, kus sellele tullakse poodi järele. Kui väärtuseks on seatud suvand **Väär**, siis enne kauba ostukorvi lisamist ja tellimuse esitamist varude kontrolli ei tehta.
- **Varude puhver** – seda atribuuti kasutatakse varude puhvri arvu määramiseks. Varusid hallatakse reaalajas ja kui paljud kliendid esitavad tellimusi, võib täpse varude arvu säilitamine olla keeruline. Kui varude kontroll on tehtud, siis kui varusid on vähem kui puhvri kogus, käsitletakse toodet kui laost otsas. Seega kui müük toimub kiiresti läbi mitme kanali, nii et varade arv pole täielikult sünkroonitud, on vähem ohtu, et müüakse kaup, mis on laost otsas.
- **Tagasi ostukorvi** – seda atribuuti kasutatakse ostukorvi lingi **Tagasi ostlema** marsruudi määramiseks. Protsessi saab konfigureerida saiditasemel, võimaldades jaemüüjatel viia klient tagasi avalehele või saidi mis tahes teisele lehele.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Ostukorvi moodul toob toote teabe välja Commerce Scale Uniti API-de abil. Brauseriküpsise ostukorvi ID-d kasutatakse Commerce Sale Unitist kogu tooteteabe toomiseks.

## <a name="add-a-cart-module-to-a-page"></a>Lehele ostukorvi mooduli lisamine

Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge fragment nimega **Ostukorvi fragment** ja lisage uuele fragmendile ostukorvi moodul.
1. Lisage ostukorvi moodulile päis.
1. Lisage kaupluse valija moodul ostukorvi moodulile.
1. Salvestage fragment, viige lõpule selle redigeerimine ja seejärel avaldage see.
1. Looge mall nimega **Ostukorvi mall**ja lisage ostukorvi fragment, mille just lõite.
1. Salvestage mall, viige lõpule selle redigeerimine ja seejärel avaldage see.
1. Looge leht, mis kasutab uut malli.
1. Salvestage ja kuvage lehe eelvaade.
1. Viige lõpule lehe redigeerimine ja seejärel avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteineri moodul](add-container-module.md)

[Kaupluse valija moodul](store-selector.md)

[Ostukasti moodul](add-buy-box.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
