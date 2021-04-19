---
title: Tarnevalikute moodul
description: See teema hõlmab tarnevalikute mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f97dcd42e22e319d9af7cbf57fce7c10d8565d04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801985"
---
# <a name="delivery-options-module"></a>Tarnevalikute moodul

[!include [banner](includes/banner.md)]

See teema hõlmab tarnevalikute mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.

Tarnevalikute moodulid võimaldavad klientidel valida oma veebitellimuse jaoks tarneviisi, nt lähetamise või pealevõtmise. Tarneviisi määramiseks on vajalik tarneaadress. Kui tarneaadress muutub, tuleb tarnevalikud uuesti hankida. Kui tellimus sisaldab ainult kaupu, millele minnakse poodi järele, siis see moodul peidetakse automaatselt.

Lisateavet tarneviiside konfigureerimise kohta leiate teemadest [Võrgukanali seadistamine](channel-setup-online.md) ja [Tarneviiside seadistamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Igal tarneviisil võib olla seotud kulu. Lisateavet veebipoe jaoks kulude konfigureerimise kohta leiate teemast [Omnikanali täpsemad automaatsed kulud](omni-auto-charges.md).

Commerce'i versioonis 10.0.13 värskendati tarnevalikute moodulit, et toetada funktsioone **Päisekulud ilma proportsionaalse jaotamiseta** ja **Lähetamine reakuluna**. Kui proportsionaalne jaotamine on välja lülitatud, eeldatakse, et e-kaubanduse töövoog ei luba ostukorvis olevate kaupade jaoks valida erinevat tarneviisi (see tähendab, et mõned kaubad määratakse lähetamiseks, kuid teised pealevõtmiseks). Funktsiooni **Päisekulud ilma proportsionaalse jaotamiseta** jaoks on vajalik, et Commerce'i peakontoris oleks sisse lülitatud lipp **Luba kanalis järjekindel tarneviisi käitlemine**. Kui see lipp on sisse lülitatud, rakendatakse saatekulusid kas päise- või reatasemel, sõltuvalt Commerce'i peakontori konfiguratsioonist.

Fabrikami kujundus toetab kombineeritud tarneviisi, kus mõni kaup määratakse lähetamiseks, kuid teised pealevõtmiseks. Selle viisi puhul jaotatakse saatekulud proportsionaalselt kõigi kaupade vahel, mille tarneviis on lähetamine. Kombineeritud tarneviisi toimimiseks peate Commerce'i peakontoris enne konfigureerima funktsiooni **Päisekulud koos proportsionaalse jaotamisega**. Lisateavet selle konfiguratsiooni kohta leiate teemast [Päisekulude proportsionaalselt jaotamine müügiridade järgi](pro-rate-charges-matching-lines.md).

Kui reakaupade puhul rakenduvad saatekulud, saab neid kuvada iga kauba ostukorvireal. Selle funktsiooni jaoks on vaja, et atribuut **Kuva reakauba saatekulud** oleks nii ostukorvi- kui ka maksmise mooduli puhul sisse lülitatud. Lisateavet leiate teemadest [Ostukorvimoodul](add-cart-module.md) ja [Maksmise moodul](add-checkout-module.md).

Järgmisel illustratsioonil on näide tarnevalikute moodulist maksmise lehel.

![Tarnevalikute mooduli näide maksmise lehel](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Tarnevalikute mooduli atribuudid

| Atribuut | Väärtused | Kirjeldus |
|----------|--------|-------------|
| Pealkiri | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Tarnevalikute mooduli valikuline pealkiri. |
| Kohandatud CSS-i klassinimi | Tekst | Kaskaadlaadistiku (CSS) kohandatud klassi nimi, mida kasutatakse selle mooduli renderdamiseks, kui seda on vaja. |
| Tarneviisi valikute filtreerimine | **Ära filtreeri** või **Lähetusega mitteseotud viisid** | Väärtus, mis määrab, kas tarnevalikute moodul peaks filtreerima välja kõik tarneviisid, mis pole seotud lähetusega. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksmise lehele tarnevalikute mooduli lisamine ja vajalike atribuutide seadistamine

Tarnevalikute moodulit saab lisada ainult maksmise moodulisse. Lisateavet selle kohta, kuidas konfigureerida tarnevalikute moodulit ja lisada seda maksmise lehele, leiate teemast [Maksmise moodul](add-checkout-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Maksmismoodul](add-checkout-module.md)

[Makse moodul](payment-module.md)

[Tarneaadressi moodul](ship-address-module.md)

[Järeletulemisteabe moodul](pickup-info-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Kinkekaardi moodul](add-giftcard.md)

[Võrgukanali seadistamine](channel-setup-online.md)

[Omnikanali täpsemad automaatsed kulud](omni-auto-charges.md)

[Päisekulude proportsionaalselt jaotamine müügiridade järgi](pro-rate-charges-matching-lines.md)

[Tarneviiside seadistamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]