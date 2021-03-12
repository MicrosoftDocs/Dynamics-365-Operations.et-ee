---
title: Ostukorvi moodul
description: See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: abb9909c03577763ff7e6242c9395a58159df6ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985975"
---
# <a name="cart-module"></a>Ostukorvi moodul

[!include [banner](includes/banner.md)]

See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Ostukorvi moodul näitab ostukorvi lisatud kaupasid enne, kui klient on kassasse läinud. Moodul näitab ka ostu kokkuvõtet ja võimaldab kliendil rakendada või eemaldada kampaaniakoode.

Ostukorvi moodul toetab sisselogitud ostu ja külalisostu. Samuti toetab see linki **Tagasi ostlema**. Saate konfigureerida selle lingi marsruudi jaotises **Saidi sätted \> Laiendused \> Marsruudid**.

Ostukorvi moodul renderdab andmed ostukorvi ID põhjal, mis on üle kogu saidi saadaval brauseri küpsis. 

Järgmisel pildil on näide Fabrikami saidi ostukorvi lehest.

![Ostukorvimooduli näide Fabrikami saidil](./media/cart2.PNG)

Järgmisel pildil on näide Fabrikami saidi ostukorvi lehest. Selles näites on reakaubal töötluskulu.

![Ostukorvimooduli näide koos reakauba töötluskuluga](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Ostukorvi mooduli atribuudid ja pesad

| Atribuut | Väärtused | Kirjeldus |
|----------------|--------|-------------|
| Pealkiri | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Ostukorvi pealkiri, näiteks „Ostukorv” või „Ostukorvis olevad kaubad”. |
| Kuva laost otsas varude tõrked | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse ostukorvilehel varudega seotud tõrkeid. Soovitame seada selle atribuudi väärtuseks **Tõene**, kui saidil kontrollitakse varusid. |
| Kuva reakaupade saatekulud | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse ostukorvi reakaupade juures saatekulud, kui see teave on saadaval. See funktsioon pole Fabrikami kujunduses toetatud, kuna kasutajad valivad tarneviisi alles maksmise voos. Kuid seda funktsiooni saab sisse lülitada ka teistes töövoogudes, kui see on rakendatav. |
| Kuva saadaolevad kampaaniad| **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on määratud **Tõene**, kuvatakse ostukorvis selles olevate kaupade alusel saadaolevad kampaaniad. See funktsioon on saadaval Dynamics 365 Commerce'i versioonis 10.0.16. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moodulid, mida saab ostukorvi moodulis kasutada

- **Tekstiplokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid. Sõnumeid juhib sisuhaldussüsteem (CMS). Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.
- **Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas. See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused. Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).

## <a name="module-properties"></a>Mooduli atribuudid

Jaotises **Saidi sätted \> Laiendused** saab konfigureerida järgmisi ostukorvi mooduli sätteid.

- **Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks. Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.
- **Varud** – varude sätete rakendamise kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).
- **Tagasi ostukorvi** – seda atribuuti kasutatakse ostukorvi lingi **Tagasi ostlema** marsruudi määramiseks. Protsessi saab konfigureerida saiditasemel, võimaldades jaemüüjatel viia klient tagasi avalehele või saidi mis tahes teisele lehele.

> [!IMPORTANT]
> Väljalaskes Dynamics 365 Commerce 10.0.14 ja uuemas koondatakse ostukorvis olevad kaubad vastavalt sätetele, mis määratletakse Commerce'i peakontori võrgupoe veebipõhises funktsiooniprofiilis. Lisateavet selle kohta, kuidas luua vebipõhist funktsiooniprofiili ja määrata kogumile nõutavad atribuudid, leiate teemast [Veebipõhise funktsiooniprofiili loomine](online-functionality-profile.md).

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Ostukorvi moodul toob toote teabe välja Commerce Scale Uniti API-de abil. Brauseriküpsise ostukorvi ID-d kasutatakse Commerce Sale Unitist kogu tooteteabe toomiseks.

## <a name="add-a-cart-module-to-a-page"></a>Lehele ostukorvi mooduli lisamine

Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus fragment** moodul **Ostukorv**.
1. Avage jaotis **Fragmendi nimi**, sisestage **Ostukorvi fragmendi** nimi ja seejärel valige **OK**.
1. Valige pesa **Ostukorv**.
1. Valige parempoolsel atribuutide paanil pliiatsisümbol, sisestage väljale pealkirja tekst ja seejärel valige märkesümbol.
1. Valige pesas **Ostukorv** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Kaupluse valija** ja klõpsake seejärel **OK**.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotises **Malli nimi** mallile nimi.
1. Valige liigenduspuu jaotises **Sisu** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.
1. Valige dialoogiboksis **Vali fragment** **Ostukorvi fragmendi** fragment ja seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Malli valimine** varem teie loodud mall, sisestage lehe nimi ja seejärel valige **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Maksmise moodul](add-checkout-module.md)

[Makse moodul](payment-module.md)

[Tarneaadressi moodul](ship-address-module.md)

[Tarnevalikute moodul](delivery-options-module.md)

[Järeletulemisteabe moodul](pickup-info-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Kinkekaardi moodul](add-giftcard.md)

[Varude saadavuse arvutamine jaemüügikanalite jaoks](calculated-inventory-retail-channels.md)

[Funktsiooniprofiili loomine võrgus](online-functionality-profile.md)
