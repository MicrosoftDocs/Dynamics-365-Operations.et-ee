---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services
description: Selles teemas selgitatakse, kuidas laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla elektroonilise aruandluse (ER) konfiguratsioone.
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 719b277fb828ea2085ea80bc4a36c2af3412f66b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683301"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas teenuse Microsoft Dynamics Lifecycle Services (LCS) [ühiste vahendite teegist](../lifecycle-services/asset-library.md) laadida alla [elektroonilise aruandluse (ER) konfiguratsioonide](general-electronic-reporting.md#Configuration) uusimat versiooni.

1. Logige rakendusse sisse, kasutades üht järgmistest rollidest.

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

2. Avage **Organisatsiooni haldamine** &gt; **Tööruumid** &gt; **Elektrooniline aruandlus**.
3. Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.
4. Valige paanil **Microsoft** suvand **Hoidlad**.

    [![Paan Microsoft lokaliseerimise konfiguratsioonide lehel](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla tüübiga **LCS**. Kui hoidlat ei kuvata ruudustikus, tehke järgmist.

    1. Hoidla lisamiseks valige **Lisa**.
    2. Valige hoidla tüüp **LCS**.
    3. Valige käsk **Loo hoidla**.
    4. Kui teil palutakse end autoriseerida, järgige ekraanil kuvatavaid juhiseid.
    5. Sisestage hoidla nimi ja kirjeldus.
    6. Uue hoidla kirje kinnitamiseks valige **OK**.
    7. Valige võrgustikus uus andmebaas tüübiga **LCS**.

6. Valitud hoidla elektroonilise aruandluse konfiguratsioonide loendi vaatamiseks valige käsk **Ava**.

    [![Konfiguratsioonihoidlate leht](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Kui teil on probleeme LCS-i hoidlasse juurde pääsemisega konfiguratsioonide allalaadimiseks LCS-i ühiste vahendite teegist, saate selle asemel laadida konfiguratsioonid alla [globaalsest hoidlast](er-download-configurations-global-repo.md).

7. Valige vasakul paanil konfiguratsioonide puus soovitud ER-i konfiguratsioon.
8. Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.
9. Valige käsk **Impordi**, et laadida valitud versioon LCS-ist alla praegusesse eksemplari.

    > [!NOTE]
    > Nupp **Impordi** ei ole saadaval ER-i konfiguratsiooni versioonide puhul, mis on juba praeguses eksemplaris olemas.

    [![Konfiguratsioonihoidla leht](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist. Võib-olla teavitatakse teid leitud vasturääkivustest. Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada. Lisateavet vaadake selle teemaga seotud teemade loendist.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]