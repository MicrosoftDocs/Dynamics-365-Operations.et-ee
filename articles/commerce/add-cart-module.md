---
title: Ostukorvi moodul
description: See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411269"
---
# <a name="cart-module"></a>Ostukorvi moodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Ostukorvi moodul näitab ostukorvi lisatud kaupasid enne, kui klient on kassasse läinud. Moodul näitab ka ostu kokkuvõtet ja võimaldab kliendil rakendada või eemaldada kampaaniakoode.

Ostukorvi moodul toetab sisselogitud ostu ja külalisostu. Samuti toetab see linki **Tagasi ostlema**. Saate konfigureerida selle lingi marsruudi jaotises **Saidi sätted \> Laiendused \> Marsruudid**.

Ostukorvi moodul renderdab andmed ostukorvi ID põhjal, mis on üle kogu saidi saadaval brauseri küpsis. 

Järgmisel pildil on näide Fabrikami saidi ostukorvi lehest.

![Ostukorvi mooduli näide](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>Ostukorvi mooduli atribuudid ja pesad

Ostukorvi moodulis on atribuut **Pealkiri**, mida saab seadistada sellistele väärtustele nagu **Ostukorv** ja **Ostukorvis olevad kaubad**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moodulid, mida saab ostukorvi moodulis kasutada

- **Tekstiplokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid. Sõnumeid juhib sisuhaldussüsteem (CMS). Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.
- **Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas. See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused. Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).

## <a name="module-properties"></a>Mooduli atribuudid

Jaotises **Saidi sätted \> Laiendused** saab konfigureerida järgmisi ostukorvi mooduli sätteid.

- **Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks. Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.
- **Varud** – varude sätete rakendamise kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).
- **Tagasi ostukorvi** – seda atribuuti kasutatakse ostukorvi lingi **Tagasi ostlema** marsruudi määramiseks. Protsessi saab konfigureerida saiditasemel, võimaldades jaemüüjatel viia klient tagasi avalehele või saidi mis tahes teisele lehele.

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Ostukorvi moodul toob toote teabe välja Commerce Scale Uniti API-de abil. Brauseriküpsise ostukorvi ID-d kasutatakse Commerce Sale Unitist kogu tooteteabe toomiseks.

## <a name="add-a-cart-module-to-a-page"></a>Lehele ostukorvi mooduli lisamine

Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Lehe fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus lehe fragment** moodul **Ostukorv**.
1. Jaotises **Lehe fragmendi nimi** sisestage nimi **Ostukorvi fragment** ja seejärel valige **OK**.
1. Valige pesa **Ostukorv**.
1. Valige parempoolsel atribuutide paanil pliiatsisümbol, sisestage väljale pealkirja tekst ja seejärel valige märkesümbol.
1. Valige pesas **Ostukorv** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Kaupluse valija** ja klõpsake seejärel **OK**.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotises **Malli nimi** mallile nimi.
1. Valige liigendpuust pesa **Keha**, valige kolmikpunkt (**...**) ja seejärel suvand **Lisa fragment**.
1. Valige dialoogiboksis **Lehe fragmendi valimine** fragment **Ostukorvi fragment** ja seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Malli valimine** varem teie loodud mall, sisestage lehe nimi ja seejärel valige **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteineri moodul](add-container-module.md)

[Kaupluse valimise moodul](store-selector.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)

[Varude saadavuse arvutamine jaemüügikanalite jaoks](calculated-inventory-retail-channels.md)
