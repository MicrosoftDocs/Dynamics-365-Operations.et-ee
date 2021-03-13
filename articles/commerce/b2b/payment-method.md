---
title: Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks
description: Selles teemas kirjeldatakse, kuidas konfigureerida kliendikonto makseviisi ettevõtetevahelise (B2B) e-kaubanduse saitide jaoks.
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
ms.openlocfilehash: 754e2f83d6c8ff5d3698d98062e54bba7ccd9836
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035896"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas konfigureerida kliendikonto makseviisi ettevõtetevahelise (B2B) e-kaubanduse saitide jaoks.

Jaemüüjad võivad võtta e-kaubanduse kanalis müüdavate toodete ja teenuste eest tasu erinevat tüüpi maksemeetoditega. Kõik jaemüüja aktsepteeritavad maksetüübid tuleb konfigureerida süsteemi seadistamisel rakenduses Microsoft Dynamics 365 Commerce. B2B e-kaubanduse saitidel peab toetama kliendikonto (või "ettemaksi") makseviisi. 

## <a name="prerequisites"></a>Eeltingimused

1. Lisage kliendikonto makseviis Commerce'i peakontoris.
2. Siduge kliendikonto makseviis e-kaubanduse kanaliga.
3. Veenduge, et säte **Luba kontol** on kliendi jaoks Commerce'i peakontori jaotises **Jaemüük ja kaubandus \> Kliendid \> Kõik kliendid \> Makse vaikesätted** lubatud. Veenduga ka, et parameetrid **Krediidilimiit** on kliendi jaoks õigesti seadistatud Commerce'i peakontori jaotises **Jaemüük ja kaubandus \> Kliendid \> Kõik kliendid \> Krediit ja võlanõuded**. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Kliendikonto makseviisi lubamine Commerce'i saidiehitajas 

Kliendikonto makseviisi lubamiseks Commerce'i saidiehitajas toimige järgmiselt.

1. Avage **Saidi sätted \> Laiendused**.
1. Seadke atribuut **Luba kliendikonto maksed** väärtusele **B2B-klientidele lubatud**. 
1. Valige suvand **Salvesta ja avalda**.

> [!NOTE]
> Uued saidi sätted jõustuvad alles pärast faili app.settings.json värskendamist. Lisateabe saamiseks vt [SDK ja mooduliteegi värskendused](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Kliendikonto makseviisi lubamine B2B e-kaubanduse saidi kassa lehel

Kliendikonto makseviisi lubamiseks B2B e-kaubanduse saidi kassa lehel toimige järgmiselt.

1. Leidke ja redigeeride Commerce'i saidiehitajas kassa lehte või fragmenti, mis sisaldab kassamoodulit B2B e-kaubanduse saidi jaoks.
1. Valige lahtrist **Kassa jaotise konteiner** käsk **Lisa moodul** ja seejärel lisage moodul **Kliendikonto makse**.
1. Paigutage moodul **Kliendikonto makse** valides kolmikpunkti (**...**) ja seejärel valides vastavalt vajadusele kas **Nihuta üles** või **Nihuta alla**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Kinnitage, et kliendikonto makseviis on lubatud ja avaldatud.

Kinnitamiseks, et kliendikonto makseviis on lubatud ja avaldatud, toimige järgmiselt.

1. Logige e-kaubanduse saidile sisse.
1. Lisage toode ostukorvi.
1. Minge kassa lehele. Peaksite nägema uut makseviisi **Kliendikonto**.

## <a name="additional-resources"></a>Lisaressursid

[B2B e-kaubanduse saidi seadistamine](set-up-b2b-site.md)

[B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.](org-model.md)

[Äripartnerist kasutajate haldamine B2B e-kaubanduse saitidel](manage-b2b-users.md)

[Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks](quantity-limits.md)

[SDK ja mooduliteegi värskendused](../e-commerce-extensibility/sdk-updates.md)
