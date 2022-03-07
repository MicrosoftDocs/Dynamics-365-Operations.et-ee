---
title: Kviitungita tagastuste makseviiside piiramine
description: Selles teemas kirjeldatakse, kuidas saab teatud maksetüüpide puhul tagasimakse keelata, kui tagastus toimub ilma kviitungita.
author: rapraj
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 716b3a924da14d94061966d0d671003a6e2b90f88a3c0c4064191b47d8930f93
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773834"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Kviitungita tagastuste makseviiside piiramine


[!include [banner](includes/banner.md)]

Kõik jaemüüja aktsepteeritavad maksetüübid tuleb konfigureerida süsteemi seadistamisel. Selles teemas kirjeldatakse, kuidas saab teatud maksetüüpide puhul tagasimakse keelata, kui tagastus toimub ilma kviitungita.

## <a name="set-up-payment-methods"></a>Seadistada maksemeetodid

Makseviiside seadistamiseks täitke järgmised ülesanded.
1. Looge makseviisid, mida aktsepteerib kogu organisatsioon.
2. Üleorganisatsiooniliste kaarditüüpide ja kaardi numbrite loomine. Kui aktsepteeritakse krediit- või deebetkaarte, peate looma ühe makseviisi kaartidele ja looma seejärel üleorganisatsioonilised kaarditüübid ja kaardi numbrid.
3. Seadistage kaupluse makseviisid. Seostage makseviisid iga kauplusega ja seejärel sisestage iga kaupluse makseviisile kauplusepõhised sätted.
4. Seadistage kauplustele kaardimakseviisid. Tehke kaardiseadistus kõikidele kaardimakseviisidele, mida kauplus aktsepteerib.

![Poe seadistus.](media/NoReceiptReturns1.png "Kaupluse häälestus") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Kviitungita tagastuste makseviiside piiramine

Kaupluse iga makseviisi puhul valige lehel **Kaupluse haldus** jaotises **Kviitungita tagastused** suvandi **Keela kviitungita tagasimaksed** sätteks **Jah**. 

Ümberlülitusklahvi vaikeväärtus on **Ei**, mis tagab, et tagasimaksete puhul on makseviis lubatud. 

Kui suvandi **Keela kviitungita tagasimaksed** sätteks on valitud **Jah**, ei lubata valitud makseviisi tagasimaksete puhul. 

![Kaupluse makseviis.](media/NoReceiptReturns3.png "Kaupluse makseviis") 

> [!NOTE]
> Kui kassapidaja valib makseviisi, mille puhul on kviitungita tagasimakse keelatud, kuvatakse teade, mis palub kontrollida lubatud makseviise.

![Aktsepteeritavad makseviisid.](media/NoReceiptReturns4.png "Aktsepteeritavad makseviisid") 

Kui kandel on nii kviitungiga tagastus kui ka kviitungita tagastus, siis piirangutingimusi ei rakendata, kuna kanne on kviitungiga tagastusvoog. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]