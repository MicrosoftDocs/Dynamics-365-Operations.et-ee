--- 
title: "Müügitellimuse arvete loomine"
description: "Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-order-invoices"></a>Müügitellimuse arvete loomine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus. See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="create-an-invoice-from-a-sales-order"></a>Müügitellimusest arve loomine
1. Avage Müügireskontro > Tellimused > Ilma arvet väljastamata lähetatud müügitellimused.
2. Valige loendist müügitellimus. 
3. Klõpsake toimingupaanil valikut Arve.
4. Klõpsake valikut Arve.
    * Pange tähele, et selle müügitellimusega on seostatud mitu saatelehte. Saatelehe numbri asemel kuvatakse ainult sõna <multiple> (mitu).  
5. Laiendage jaotis Parameetrid.
    * Arve sisestamiseks peab sisestamise väärtuseks olema määratud Jah. Võite ka sisestamise välja lülitada ja arve ainult printida. Sama tulemuse saate ka siis, kui loote arve asemel esialgse arve.  
    * Seda suvandit kasutatakse pakett-tööde puhul. Päring käivitatakse pakett-töö käivitamisel.    
6. Väljal Printimine valige Pärast.
7. Väljal Prindi arve valige suvand Jah.
    * Prindihaldus võimaldab mitme arve koopiat printida, samuti PDF‑vormingus arvet meiliga saata.  
8. Väljal Prinditasud valige Summeerimine.
9. Väljal Krediidilimiidi kontrollimine valige Saldo.
10. Klõpsake valikut Tühista.

## <a name="combine-orders-into-a-single-invoice"></a>Tellimuste ühte arvesse ühendamine
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Leidke klient, kellel on mitu arvet avatud.
3. Valige avatud müügitellimus
4. Valige mõni teine sama kliendi avatud müügitellimus.
5. Klõpsake toimingupaanil valikut Arve.
6. Klõpsake valikut Arve.
7. Laiendage jaotis Parameetrid.
8. Valige väljal Kogus väärtus Kõik.
    * Pange tähele, et ülevaate jaotises on loetletud kaks arvet. Ühendame need nüüd ühte arvesse.  
9. Väljal Koondsisestamine valige Arve konto.
10. Müügitellimuste ühte arvesse ühendamiseks klõpsake käsku Korralda.
    * Kaks müügitellimust on nüüd ühte arvesse ühendatud.   
11. Klõpsake valikut Tühista.
12. Klõpsake nuppu Jah.

## <a name="post-invoices-in-a-batch"></a>Partii jaoks arvete sisestamine
1. Avage Müügireskonto > Arved > Partii arveldamine > Arve.
2. Klõpsake Vali.
3. Klõpsake nuppu OK.
4. Klõpsake valikut Partii.
5. Pakktöötluse sisse lülitamiseks klõpsake suvandit Jah.
6. Klõpsake valikut Korduvus.
7. Valige Päevad
8. Klõpsake nuppu OK.
9. Klõpsake nuppu OK.
10. Klõpsake valikut Tühista.
11. Klõpsake nuppu Jah.


