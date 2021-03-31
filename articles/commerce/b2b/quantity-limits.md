---
title: Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks
description: Selles teemas kirjeldatakse ettevõtetevahelise (B2B) e-kaubanduse saitidele toote koguse piirangute seadistamist.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1208b968e476ccbc7a726facf1db896c7bf3c36f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211173"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse ettevõtetevahelise (B2B) e-kaubanduse saitidele toote koguse piirangute seadistamist.

Enamikel toodetel on mõõtühik, mis määratleb nende grupeerimise. Grupeerimine mõjutab seda, kuidas tooteid saab müüa. Mõnel tootel võib koguste jaoks olla täiendav grupeerimine. See grupeerimine määrab, kas tooteid saab müüa üksikult või kordühikuna ja kas on olemas minimaalne või maksimaalne tellimuse koguse piirang, mida tuleb järgida.

Koguse piiramise funktsioon tagab, et minimaalsed, maksimaalsed, mitmekordsed ja standardkogused, mis on konfigureeritud rakenduses Microsoft Dynamics 365 Commerce (vaiketellimuse sätetes või Commerce'i saidiehitaja saidisätetes) rakendatakse klienditellimustele, e-kaubanduse saidil esitatakse. Toote koguse piiranguid praegu kassas ja kõnekeskustes ei toetata.

Paljud jaemüüjad pakuvad mitmesuguste toote- ja täitmisnõuete täitmiseks klienditellimuste (tuntud ka kui eritellimused) võimalust. Tüüpilised stsenaariumid on näiteks järgmised.

- Klient soovib, et kindlate variantide tooteid müüdaks mitme kaupa.
- Klient soovib tooted kätte saada teisest poest või asukohast kui see, kust ta tooted ostis. Kaupluste pakkimisstandardid erinevad siiski veebimüügi pakkimisstandarditest.
- Klient soovib osta piiratud versiooniga toodet, millel on maksimaalse ostetava koguse piirang.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Commerce'i peakontoris tellimuse vaikesätete funktsiooni sisse lülitamine

Enne toote kogusepiirangute seadmist tuleb tellimuse vaikesätete funktsioon Commerce'i peakontoris sisse lülitada.

Tellimuse vaikesätete sisselülitamiseks toimige järgmiselt.

1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.
1. Leidke ja valige funktsioon **Tellimuse saidi- ja vaikseätete toetamine klienditellimustes**.
1. Valige parempoolse paani allosas suvand **Luba kohe**. 

## <a name="define-quantity-settings"></a>Koguse sätete määratlemine 

Lehel **Tellimuse vaikesätted** saate määratleda koguse sätted.

Koguse sätete määratlemiseks järgige neid samme. 

1. Avage toote **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Väljastatud tooted kategooria järgi**.
1. Valige väljastatud toode.
1. Valige toimingupaani vahekaardil **Varude haldus** grupis **Tellimuse sätted** suvand **Tellimuse vaikesätted**. 
1. Seadke toote müügikogused jaotise **Müügikogus** kiirkaardil **Müügitellimus** lehel **Tellimuse vaikesätted**.

    - **Mitu** - kogus, mille kordades toodet osta saab.
    - **Minimaalne tellimuse kogus** - minimaalne ostetavate toodete arv.
    - **Maksimaalne tellimuse kogus** - maksimaalne ostetavate toodete arv.
    - **Standardne toote kogus** - vaikekogus, mis sisestatakse automaatselt toote valimisel.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Commerce'i saidiehitajas B2B toote koguse piirangute funktsiooni sisse lülitamine

Commerce'i saidiehitajas B2B toote koguse piirangute funktsiooni sisse lülitamiseks toimige järgmiselt.

1. Avage **Saidi sätted \> Laiendused**
1. Valige jaotises **Luba tellimuse koguse piirangud** ripploendist **Lubatud B2B klientide jaoks**. 

> [!NOTE] 
> Värskendatud saidiehitaja sätted jõustuvad alles pärast faili app.settings.json värskendamist. Lisateabe saamiseks vt [SDK ja mooduliteegi värskendused](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Lisaressursid

[B2B e-kaubanduse saidi seadistamine](set-up-b2b-site.md)

[B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.](org-model.md)

[Äripartnerkasutajate haldamine B2B e-kaubandussaitidel](manage-b2b-users.md)

[Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]