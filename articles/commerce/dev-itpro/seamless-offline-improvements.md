---
title: Kinkekaardi ja krediiditeatise toimingute sujuv jätkamine internetiühenduse katkemise korral
description: See artikkel annab ülevaate parendustest, mis pakuvad kindlatele maksetüüpidele sujuvat võrguühenduseta lülitit.
author: BrianShook
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
ms.author: brshoo
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: e0416a61bd5fd3b875b427ad8a6313d0e9936f0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869157"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Kinkekaardi ja krediiditeatise toimingute sujuv võrguühenduseta lülitamine

[!include [banner](../includes/banner.md)]

Kui kassa seade kaotab oma ühenduse kanali andmebaasiga, saab enamike pooleli olevate kassatoimingute ja tehingutega jätkata pärast seda, kui müüja saab hoiatusteate ühenduse kadumise kohta. Samas mõnel juhul on tehingutel siiski elemente, mis sõltuvad reaalajas teenusest, ja neid elemente ei toetata, kui kassa on võrguühenduseta. See artikkel kirjeldab mõnda funktsiooni, mis aitab vähendada kaotatud ühenduvuse mõju nendes stsenaariumides.

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

## <a name="related-articles"></a>Seotud artiklid

- [Võrguühenduseta kassa funktsioonid](../pos-offline-functionality.md)
- [Ühendusega ja ühenduseta kassatoimingud](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]