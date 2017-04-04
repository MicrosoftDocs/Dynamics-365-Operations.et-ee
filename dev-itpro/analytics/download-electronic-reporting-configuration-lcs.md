---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services
description: "Selles artiklis käsitletakse lae elektrooniline aruandlus (ER) koosseisudes: Microsoft Dynamics elutsükli teenused (LCS)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services

Selles artiklis käsitletakse lae elektrooniline aruandlus (ER) koosseisudes: Microsoft Dynamics elutsükli teenused (LCS).

Selles õpikus selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.

1.  Logige Dynamics 365 for Operationsisse sisse, kasutades üht järgmistest rollidest.
    -   Elektroonilise aruandluse arendaja
    -   Elektroonilise aruandluse funktsionaalne konsultant
    -   Süsteemiadministraator

2.  Mine **organisatsiooni haldamine**&gt;**elektrooniline**.
3.  Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.
4.  Klõpsake paanil **Microsoft** suvandit **Hoidlad**. [![Update-er-from-LCS-for-MS-Open-MS-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla tüübiga **LCS**. Kui hoidlat ei kuvata ruudustikus, tehke järgmist.
    1.  Uue hoidla lisamiseks klõpsake käsku **Lisa**.
    2.  Valige hoidla tüüp **LCS**.
    3.  Klõpsake käsku **Loo hoidla**.
    4.  Sisestage hoidla nimi ja kirjeldus.
    5.  Uue hoidla kirje kinnitamiseks klõpsake **OK**.
    6.  Valige võrgustikus uus andmebaas tüübiga **LCS**.

6.  Valitud hoidla ER-i konfiguratsioonide loendi vaatamiseks klõpsake käsku **Ava**. [![Update-er-from-LCS-for-MS-Make-LCS-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Valige vasakul paanil konfiguratsioonide puus soovitud ER-i konfiguratsioon.
8.  Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.
9.  Klõpsake käsku **Impordi**, et laadida valitud versioon LCS-ist alla Dynamics 365 for Operationsi praegusesse eksemplari. **Märkus.** Nupp **Impordi** ei ole saadaval ER-i konfiguratsiooni versioonide puhul, mis on juba Dynamics 365 for Operationsi praeguses eksemplaris olemas. [![Update-er-from-LCS-for-MS-Download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Märkus.** Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist. Võib-olla teavitatakse teid leitud vasturääkivustest. Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada. Lisateabe saamiseks vt selle teema seotud esemete loetelu.

<a name="see-also"></a>Vt ka
--------

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)


