---
title: Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast
description: Selles teemas selgitatakse, kuidas laadida konfiguratsiooniteenuse globaalsest hoidlast alla elektroonilise aruandluse konfiguratsioone.
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 32eb5206fadefbd024f2dd2af888d166c81b950f
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605327"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas laadida konfiguratsiooniteenuse globaalsest hoidlast alla [elektroonilise aruandluse konfiguratsioone](general-electronic-reporting.md#Configuration). Lisateavet vt teemast [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfiguratsiooniteenus](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Konfiguratsioonihoidla avamine

1. Logige rakendusse Dynamics 365 Finance sisse, kasutades üht järgmistest rollidest.

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

2. Avage **Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus**.
3. Valige jaotises **Konfiguratsiooni pakkujad** paan **Microsoft**.
3. Valige paanil **Microsoft** suvand **Hoidlad**.

    ![Elektroonilise aruandluse tööruum.](./media/er-download-configurations-global-repo-er-workspace.png)

4. Valige lehel **Konfiguratsioonihoidlad** ruudustikus olemasolev hoidla, mille tüüp on **Globaalne**. Kui hoidlat ei kuvata ruudustikus, tehke järgmist.

    1. Uue hoidla lisamiseks valige **Lisa**.
    2. Valige hoidla tüübiks **Globaalne** ja seejärel **Loo hoidla**.
    3. Viiba kuvamisel järgige autoriseerimisjuhiseid.
    4. Sisestage hoidla nimi ja kirjeldus ning seejärel valige uue hoidla kirje kinnitamiseks **OK**.
    5. Valige ruudustikus uus hoidla, mille tüüp on **Globaalne**.

5. Valitud hoidla elektroonilise aruandluse konfiguratsioonide loendi vaatamiseks valige käsk **Ava**.

    ![Konfiguratsioonihoidlate leht.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Ühe konfiguratsiooni importimine

1. Valige lehel **Konfiguratsioonihoidlad** konfiguratsioonide puult soovitud elektroonilise aruandluse konfiguratsioon.
2. Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni nõutav versioon.
3. Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast alla Finance'i praegusesse eksemplari.

    > [!NOTE]
    > Nupp **Impordi** ei ole saadaval elektroonilise aruandluse konfiguratsiooni versioonide puhul, mis on juba praeguses Finance'i eksemplaris olemas.

    ![Konfiguratsioonihoidla leht, konfiguratsioonide kiirkaart.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Filtreeritud konfiguratsioonide importimine

1. Laiendage lehel **Konfiguratsioonihoidlad** konfiguratsioonide puul kiirkaart **Filter**.
2. Sisestage ruudustikus **Sildid** kõik vajalikud sildid.
3. Valige väljal **Riigi/piirkonna kohaldatavus** sobivad riigi/piirkonna koodid ja seejärel valige **Rakenda filter**.

    > [!NOTE]
    > Kiirkaardil **Konfiguratsioonid** kuvatakse kõik konfiguratsioonid, mis vastavad määratletud valikutingimustele.

4. Valige kiirkaardil **Konfiguratsioonid** käsk **Impordi**, et laadida filtreeritud konfiguratsioonid globaalsest hoidlast praegusesse eksemplari.
5. Valige kiirkaardil **Konfiguratsioonid** käsk **Lähtesta filter**, et puhastada määratletud valikutingimused.

    ![Konfiguratsioonihoidla leht, versioonide kiirkaart, nupp Impordi.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Olenevalt ER-i sätetest kontrollitakse konfiguratsioone pärast importimist. Võib-olla teavitatakse teid leitud vasturääkivustest. Probleemid tuleb enne imporditud konfiguratsiooni versiooni kasutamist lahendada. Lisateavet leiate selle teemaga seotud ressursside loendist.

> [!NOTE]
> Elektroonilise aruandluse konfiguratsiooni saab konfigureerida teistest konfiguratsioonidest sõltuvana. Seetõttu võidakse valitud konfiguratsiooniga koos automaatselt importida ka muid konfiguratsioone. Lisateavet konfiguratsioonide sõltuvuste kohta leiate jaotisest [ER-i konfiguratsioonide sõltuvuse määramine teistest komponentidest](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
