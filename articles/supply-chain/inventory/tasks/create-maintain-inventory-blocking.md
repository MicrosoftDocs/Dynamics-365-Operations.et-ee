---
title: Varude blokeerimise loomine ja haldamine
description: See protseduur näitab, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5fb3c7fc5dbeb6263357113d2a9348afc5b1ac9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212743"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Varude blokeerimise loomine ja haldamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist. Saate käitada protseduuri demoandmete ettevõttes USMF näidatud näidisväärtusi kasutades. Enne selle protseduuri alustamist peab teil olema füüsilise vaba kaubavaruga kaup saadaval.


## <a name="create-an-inventory-blocking"></a>Varude blokeerimise loomine
1. Paanil **Navigeerimispaan** avage **Moodulid > Varude haldus > Perioodilised ülesanded > Varude blokeerimine**.
2. Klõpsake valikut **Uus**.
3. Väljal **Kaubakood** klõpsake ripploendi nuppu, et avada otsing.
4. Valige loendist kaup, mille soovite valida. Valige kauba number koos füüsilise vaba kaubavaruga, mida soovite blokeerida. USMF-i kasutamisel saate valida kauba M9201.  
5. Sisestage arv väljale **Kogus**. Kauba M9201 kasutamisel peate valima alla 200.
6. Laiendage vahekaart **Varude dimensioonid**.
7. Väljal **Ladu** klõpsake ripploendi nuppu, et avada otsing.
8. Otsige loendist ja valige soovitud kirje. Kauba M9201 kasutamisel saate valida lao 51.  
9. Klõpsake valikut **Salvesta**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Varude blokeerimise tingimuste värskendamine
1. Sisestage arv väljale **Kogus** kiirkaardil **Üldine**. Blokeeritava koguse kajastamiseks värskendage varude koguse välja.  
2. Väljale **Eeldatav kuupäev** sisestage kuupäev. Võite soovida näidata, millal blokeeritud varud peaks reserveerimiseks saadaolevaks muutuma, määrates eeldatava kuupäeva. Kui suvand Prognoositud sissetulekud on varude blokeerimise puhul valitud, nagu blokeerimise käsitsi loomisel vaikimisi, kuvatakse see kuupäev prognoositud kandel.  
3. Klõpsake valikut **Salvesta**.

## <a name="remove-the-inventory-blocking"></a>Varude blokeerimise eemaldamine
1. Klõpsake paanil **Toimingupaan** käsku **Kustuta**.
2. Klõpsake nuppu **Jah**.
3. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]