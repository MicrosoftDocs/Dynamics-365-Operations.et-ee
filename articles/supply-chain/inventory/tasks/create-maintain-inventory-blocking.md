---
title: Varude blokeerimise loomine ja haldamine
description: See protseduur näitab, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "322256"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Varude blokeerimise loomine ja haldamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist. Saate käitada protseduuri demoandmete ettevõttes USMF näidatud näidisväärtusi kasutades. Enne selle protseduuri alustamist peab teil olema füüsilise vaba kaubavaruga kaup saadaval.


## <a name="create-an-inventory-blocking"></a>Varude blokeerimise loomine
1. Avage Varude haldus > Perioodilised ülesanded > Varude blokeerimine.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
4. Valige loendist kaup, mille soovite valida. 
    * Valige kauba number koos füüsilise vaba kaubavaruga, mida soovite blokeerida. USMF-i kasutamisel saate valida kauba M9201.  
5. Sisestage arv väljale Kogus.
    * Kauba M9201 kasutamisel peate valima alla 200.  
6. Laiendage jaotist Varude dimensioonid.
7. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
8. Otsige loendist ja valige soovitud kirje.
    * Kauba M9201 kasutamisel saate valida lao 51.  
9. Klõpsake nuppu Salvesta.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Varude blokeerimise tingimuste värskendamine
1. Sisestage arv väljale Kogus.
    * Blokeeritava koguse kajastamiseks värskendage varude koguse välja.  
2. Sisestage kuupäev väljale Eeldatav kuupäev.
    * Võite soovida näidata, millal blokeeritud varud peaks reserveerimiseks saadaolevaks muutuma, määrates eeldatava kuupäeva. Kui suvand Prognoositud sissetulekud on varude blokeerimise puhul valitud, nagu blokeerimise käsitsi loomisel vaikimisi, kuvatakse see kuupäev prognoositud kandel.  
3. Klõpsake nuppu Salvesta.

## <a name="remove-the-inventory-blocking"></a>Varude blokeerimise eemaldamine
1. Klõpsake  Kustuta.
2. Klõpsake nuppu Jah.
3. Sulgege leht.

