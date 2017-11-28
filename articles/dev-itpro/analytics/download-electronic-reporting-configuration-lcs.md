---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services
description: Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8fae33fbe2d1433e4263ed4087dad2bc894e0b84
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services

[!include[banner](../includes/banner.md)]


Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.

Selles õpikus selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.

1.  Logige Finance and Operationsisse sisse, kasutades üht järgmistest rollidest.
    -   Elektroonilise aruandluse arendaja
    -   Elektroonilise aruandluse funktsionaalne konsultant
    -   Süsteemiadministraator

2.  Minge jaotisse **Organisatsiooni haldamine** &gt; **Elektrooniline aruandlus**.
3.  Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.
4.  Klõpsake paanil **Microsoft** suvandit **Hoidlad**. [![ms-i-elektroonilise-aruandluse-värskendamine-lcs-ist-ms-i-hoidlate-loendi-avamine](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla tüübiga **LCS**. Kui hoidlat ei kuvata ruudustikus, tehke järgmist.
    1.  Uue hoidla lisamiseks klõpsake käsku **Lisa**.
    2.  Valige hoidla tüüp **LCS**.
    3.  Klõpsake käsku **Loo hoidla**.
    4. Viiba kuvamisel järgige autoriseerimisjuhiseid.
    5.  Sisestage hoidla nimi ja kirjeldus.
    6.  Uue hoidla kirje kinnitamiseks klõpsake **OK**.
    7.  Valige võrgustikus uus andmebaas tüübiga **LCS**.

6.  Valitud hoidla ER-i konfiguratsioonide loendi vaatamiseks klõpsake käsku **Ava**. [![ms-i-elektroonilise-aruandluse-värskendamine-lcs-ist-lcs-i-hoidla-loomine](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Valige vasakul paanil konfiguratsioonide puus soovitud ER-i konfiguratsioon.
8.  Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.
9.  Klõpsake käsku **Impordi**, et laadida valitud versioon LCS-ist alla Finance and Operationsi praegusesse eksemplari. **Märkus.** Nupp **Impordi** ei ole saadaval ER-i konfiguratsiooni versioonide puhul, mis on juba Dynamics 365 for Finance and Operationsi praeguses eksemplaris olemas. [![ms-i-elektroonilise-aruandluse-värskendamine-konfiguratsiooni-allalaadimine](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Märkus.** Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist. Võib-olla teavitatakse teid leitud vasturääkivustest. Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada. Lisateavet vaadaje selle teemaga seotud artiklite loendist.

<a name="see-also"></a>Vt ka
--------

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)




