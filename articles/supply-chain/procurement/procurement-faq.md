---
title: Hangete KKK
description: See teema annab vastused korduma kippuvatele küsimustele (KKK-d) Supply Chain Management hangete funktsiooni kohta
author: Henrikan
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 99d44f2409d8207ed7a0fb1fc92a99de42240e86
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577188"
---
# <a name="procurement-faq"></a>Hangete KKK

[!include [banner](../includes/banner.md)]

See teema annab vastused korduma kippuvatele küsimustele (KKK-d) Supply Chain Management hangete funktsiooni kohta.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kas saan kuvada ainult minu loodud ostutellimusi?

See funktsioon pole praegu saadaval.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kas ma saan reserveerida varusid ja luua kandeid ostutellimusel registreeritud varude põhjal?

### <a name="issue-description"></a>Probleemi kirjeldus

Isegi kui kaupade olek on ostutellimusel *Registreeritud*, saate varusid siiski reserveerida. Teisisõnu saate luua kandeid registreeritud varude põhjal.

### <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Looge ostutellimus.
2. Registreerige ostutellimuse rida.
3. Pange tähele, et saate luua reserveeringuid või kandeid registreeritud varude põhjal.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud. Eeldatakse, et registreeritud kaubad on füüsiliselt lattu või varudesse saabunud ja seetõttu on need reserveerimiseks saadaval.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kas ma saan otsida üles ostutellimuse tühistanud kasutaja?

Seda teavet jälgitakse ainult siis, kui ostutellimuse puhul kasutatakse muudatuste haldust. Kui kasutate muudatuste haldust, saate vaadata, kes esitas muudatuse (tühistamise) ja kes selle kinnitas.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Miks ei saa ma linkida ostulepingut olemasoleva ostutellimusega?

Ostutellimuse loomisel tuleb ostuleping ostutellimusega seostada. Vastasel juhul ei saa ostutellimuse ridu seostada ostulepingu ridadega.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Mis põhjustab teate „Värskendatud hinnad ja allahindlused sisestati käsitsi või tegemist on välise dokumendiga”?

Kui muudate tarnekuupäeva, võidakse kuvada teade „Värskendatud hinnad ja allahindlused sisestati käsitsi või tegemist on välise dokumendiga”. Te saate selle teate, kuna lähetuskuupäeva muutmisel võidakse aktiveerida muu kaubanduslepe või müügileping, mis võib hindu muuta. Lähetuskuupäeva muutmine võib mõjutada ka laograafikuid ja muud seotud teavet.

Teade kuvatakse, kui muudetakse mõnda kuupäeva või muud parameetrit. Teate eesmärk on teha kindlaks, et te olete teadlik hinnamuutustest, mis võivad tekkida nende muudatuste tõttu.

See teade on kaubandusleppe hindamise (TAE) viip. Täieliku kirjelduse leiate teemast [Kaubandusleppe hindamise poliitika](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Miks ma ei saa sisestada rohkem kui üht arvet ostutellimuse reale, millel on kategooriapõhised kaubad?

Kui soovite arveid sisestada, on kogus kohustuslik. Kui rea terve kogus on arveldatud ainult osalise summana, ei saa te ülejäänud summat teises arves arveldada.
