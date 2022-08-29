---
title: Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks
description: See artikkel kirjeldab, kuidas seada toote koguse piiranguid ettevõtetele (B2B) e-kaubanduse saitidele.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: 76a7ad2c3095d1402ff214dbfee26b344b492681
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275673"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas seada toote koguse piiranguid ettevõtetele (B2B) e-kaubanduse saitidele.

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

[B2B e-kaubandussaidi häälestamine](set-up-b2b-site.md)

[B2B äripartnerite haldamine kliendihierarhiaid kasutades](partners-customer-hierarchies.md)

[Äripartnerkasutajate haldamine B2B e-kaubandussaitidel](manage-b2b-users.md)

[Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
