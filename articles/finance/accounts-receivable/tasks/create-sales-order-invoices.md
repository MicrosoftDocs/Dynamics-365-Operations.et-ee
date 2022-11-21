---
title: Müügitellimuse arvete loomine
description: See artikkel kirjeldab, kuidas arveldada müügitellimusi, k.a arvete ühendamine ja pakktöötlus.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ff76eac54da6621d999d9b629fac920ba8de294
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778380"
---
# <a name="create-sales-order-invoices"></a>Müügitellimuse arvete loomine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas arveldada müügitellimusi, k.a arvete ühendamine ja pakktöötlus. See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="create-an-invoice-from-a-sales-order"></a>Müügitellimusest arve loomine
1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Ilma arvet väljastamata lähetatud müügitellimused**.
2. Valige loendist müügitellimus. 
3. Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**. Pange tähele, et selle müügitellimusega on seostatud mitu saatelehte. Saatelehe numbri asemel kuvatakse ainult sõna *mitu*.  
4. Laiendage jaotist **Parameetrid**.
    - Arve sisestamiseks peab sisestamise **väärtuseks** olema seatud Jah. Võite ka sisestamise välja lülitada ja arve ainult printida. Sama tulemuse saate ka siis, kui loote arve asemel esialgse arve.  
    - Seda suvandit kasutatakse pakett-tööde puhul. Päring käivitatakse pakett-töö käivitamisel.
5. **Väljal Printimine** valige väärtus **Pärast**.
6. Väljal **Prindi arve** valige suvand **Jah**. Prindihaldus saab printida arve mitmeid koopiaid ning saata arve ka e-kirjaga PDF-failina.  
7. Väljal Prinditasud **valige** suvand **Summeeri**.
8. Väljal Krediidilimiidi **kontrollimine** valige **saldo**.
9. Klõpsake **Tühista**.

## <a name="combine-orders-into-a-single-invoice"></a>Tellimuste ühte arvesse ühendamine
1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.
2. Leidke klient, kellel on mitu arvet avatud.
3. Saate valida mitu avatud müügitellimust kliendi kohta.
4. Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**.
5. Laiendage jaotist **Parameetrid**.
6. Valige väljal **Kogus** suvand **Kõik**. Pange tähele, et ülevaate jaotises on loetletud kaks arvet. Ühendame need nüüd ühte arvesse.  
7. **Valige väljal Koonds uuendamine** väärtus **Arve konto**.
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
