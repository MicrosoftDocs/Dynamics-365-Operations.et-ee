---
title: Kinkekaardi ja krediiditeatise toimingute sujuv võrguühenduseta lülitamine
description: See teema annab ülevaate parandustest, mis pakuvad konkreetsetele maksetüüpidele sujuvat võrguühenduseta lülitust.
author: rubendel
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 8f5c8f104d8304cf9a54efcdf6e22efbc3b356b3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348264"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Kinkekaardi ja krediiditeatise toimingute sujuv võrguühenduseta lülitamine

[!include [banner](../includes/banner.md)]

Kui kassa seade kaotab oma ühenduse kanali andmebaasiga, saab enamike pooleli olevate kassatoimingute ja tehingutega jätkata pärast seda, kui müüja saab hoiatusteate ühenduse kadumise kohta. Samas mõnel juhul on tehingutel siiski elemente, mis sõltuvad reaalajas teenusest, ja neid elemente ei toetata, kui kassa on võrguühenduseta. See teema kirjeldab mõnesid funktsioone, mis aitavad vähendada kaotatud ühenduvuse mõju sellistel juhtudel.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Ühenduseta režiimis kinkekaardi kannete lõpetamine

Sisemised kinkekaardid sõltuvad reaalajas teenusest, kuna kinkekaardi saldo peab olema Microsoft Dynamics 365 Commerce Headquarters`i keskselt hallatud. Pettuse või muu sünkroonimise probleemide vältimiseks lukustatakse kinkekaardid kohe, kui need on kandesse lisatud. Lukustamise funktsioon tagab, et kinkekaarti ei saaks kasutada samaaegselt mitmes terminalis. Kui kanne on lõpetatud, kinkekaart värskendatakse ja vabastatakse.

Samas kui kassa kaotab ühenduvuse pärast kinkekaardi kandesse lisamist, võib kinkekaardi kasutuskõlbmatuks muutuda. Selle olukorra vältimiseks on rakenduses Dynamics 365 Commerce parameeter, mis lubab kinkekaardi rida sisaldavad kanded viia lõpule, kui kassa on võrguühenduseta. Kui see parameeter on sisse lülitatud, salvestatakse võrguühenduseta sunnitud kinkekaardi kanded koos võrguühenduseta kannetega ja need sünkroonitakse Commerce Headquartersiga võrguühenduseta kannete sünkroonimisel. Sünkroonimine vabastab ka kinkekaardi, et seda saaks kasutada teises terminalis.

Et lubada funktsioonil lõpetada kinkekaardi kanded pärast võrguühenduseta režiimi lülitamist, avage vahekaart **Sisestamine** lehel **Commerce’i parameetrid**. Sellel vahekaardil otsige üles kiirkart **Kinkekaart** ja seadke suvand **Luba ühenduseta režiimis kinkekaardi kannete lõpetamine** valikule **Jah**.

![Võrguühenduseta kinkekaardi seadistamine.](../media/gift.png)

Commerce’i parameetrid on tavaliselt vahemällu talletatud. Seega pärast seda, kui selle parameetri seadistus on värskendatud ja jaotusgraafik on käivitatud sünkroonima muudatuse kanaliga, võib muudatuse jõustumiseks kuluda kuni 24 tundi. Muudatuse kohe jõustumiseks lähtestage teenus Microsoft Internet Information Services (IIS).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Võrguühenduseta režiimis krediiditeatise kannete lõpetamine

Sarnaselt sisemistele kinkekaartidele on krediiditeatised Commerce Headquartersis keskselt hallatavad. Commerce’il on parameeter, mis lubab krediiditeatise kannete lõpetamist siis, kui kassa on võrguühenduseta. See parameeter toimib sarnaselt eelmises jaotises mainitud kinkekaardi parameetriga. Kui parameeter on sisse lülitatud, sünkroonitakse võrguühenduseta sunnitud krediiditeatise kanded tagasi kanali andmebaasiga, koos teiste kannetega, mis teostati kassa võrguühenduseta olemise ajal.

Et lubada funktsioonil lõpetada krediiditeatise kanded pärast võrguühenduseta režiimi lülitamist, avage vahekaart **Sisestamine** lehel **Commerce’i parameetrid**. Sellel vahekaardil otsige üles kiirkart **Krediiditeatis** ja seadke suvand **Luba ühenduseta režiimis krediiditeatise kannete lõpetamine** valikule **Jah**.

![Võrguühenduseta krediiditeatise seadistamine.](../media/creditmemo.png)

Commerce’i parameetrid on tavaliselt vahemällu talletatud. Seega pärast seda, kui selle parameetri seadistus on värskendatud ja jaotusgraafik on käivitatud sünkroonima muudatuse kanaliga, võib muudatuse jõustumiseks kuluda kuni 24 tundi. Muudatuse koheselt jõustamiseks lähtestage IIS.

## <a name="related-topics"></a>Seotud dokumendid

- [Võrguühenduseta kassa funktsioonid](../pos-offline-functionality.md)
- [Ühendusega ja ühenduseta kassatoimingud](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]