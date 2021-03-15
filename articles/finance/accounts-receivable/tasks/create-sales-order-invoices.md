---
title: Müügitellimuse arvete loomine
description: Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0076e838ad4eac687dc7db1bc0a94891f0ee6d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991013"
---
# <a name="create-sales-order-invoices"></a>Müügitellimuse arvete loomine

[!include [banner](../../includes/banner.md)]

Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus. See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="create-an-invoice-from-a-sales-order"></a>Müügitellimusest arve loomine
1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Ilma arvet väljastamata lähetatud müügitellimused**.
2. Valige loendist müügitellimus. 
3. Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**. Pange tähele, et selle müügitellimusega on seostatud mitu saatelehte. Saatelehe numbri asemel kuvatakse ainult sõna <multiple> (mitu).  
4. Laiendage jaotist **Parameetrid**.
    - Arve sisestamiseks peab sisestamise väärtuseks olema määratud Jah. Võite ka sisestamise välja lülitada ja arve ainult printida. Sama tulemuse saate ka siis, kui loote arve asemel esialgse arve.  
    - Seda suvandit kasutatakse pakett-tööde puhul. Päring käivitatakse pakett-töö käivitamisel.
5. Väljal **Printimine** valige „Pärast”.
6. Väljal **Prindi arve** valige suvand **Jah**. Prindihaldus võimaldab mitme arve koopiat printida, samuti PDF‑vormingus arvet meiliga saata.  
7. Väljal **Prinditasud** valige „Summeerimine”.
8. Väljal **Krediidilimiidi kontrollimine** valige „Saldo”.
9. Klõpsake **Tühista**.

## <a name="combine-orders-into-a-single-invoice"></a>Tellimuste ühte arvesse ühendamine
1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.
2. Leidke klient, kellel on mitu arvet avatud.
3. Saate valida mitu avatud müügitellimust kliendi kohta.
4. Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**.
5. Laiendage jaotist **Parameetrid**.
6. Väljal **Kogus** valige Kõik. Pange tähele, et ülevaate jaotises on loetletud kaks arvet. Ühendame need nüüd ühte arvesse.  
7. Väljal **Koondsisestamine** valige „Arve konto”.
8. Müügitellimuste ühte arvesse ühendamiseks klõpsake käsku **Korralda**. Kaks müügitellimust on nüüd ühte arvesse ühendatud.   
9. Klõpsake **Tühista**.
10. Klõpsake nuppu **Jah**.

## <a name="post-invoices-in-a-batch"></a>Partii jaoks arvete sisestamine
1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Arved > Partii arveldamine > Arve**.
2. Klõpsake **Vali**.
3. Klõpsake valikut **OK**.
4. Klõpsake valikut **Partii**.
5. Valige suvandi **Pakktöötlus** sätteks **Jah**.
6. Klõpsake valikul **Korduvus**.
7. Valige **Päevad**.
8. Klõpsake valikut **OK**.
9. Klõpsake valikut **OK**.
10. Klõpsake **Tühista**.
11. Klõpsake nuppu **Jah**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]