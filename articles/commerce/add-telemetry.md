---
title: Telemeetria toetamiseks saidilehtedele skriptikoodi lisamine
description: See artikkel kirjeldab, kuidas lisada kliendipoolset skripti koodi oma saidi lehtedele, et toetada kliendipoolse telemeetria kogumist.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a0a5103d239c7f93ad6888a2eaf56d1cac32bd58
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282268"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Telemeetria toetamiseks saidilehtedele skriptikoodi lisamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lisada kliendipoolset skripti koodi oma saidi lehtedele, et toetada kliendipoolse telemeetria kogumist.

Veebianalüüs on oluline tööriist, kui soovite mõista, kuidas kliendid teie saidiga suhtlevad, ja teha otsuseid, mis aitavad maksimaalse teisenduse kogemust optimeerida. Saadaval on palju veebianalüüsi pakette, et aidata teid nende eesmärkide saavutamisel, nagu Google Analytics, Clicky, Moz Analytics ja KISSMetrics. Enamik veebianalüüsi pakette nõuavad, et lisaksite oma saidi kõikidele lehtedele HTML-i elemendis **\<head\>** kliendipoolse skriptikoodi.

> [!NOTE]
> Selle artikli juhised kehtivad ka teistele kohandatud kliendipoolsetele funktsioonidele, Microsoft Dynamics 365 Commerce mis ei ole omased.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Skriptikoodi jaoks taaskasutatava fragmendi loomine

Fragment võimaldab teil taaskasutada tekstisisest või välist skripti koodi saidi kõigil lehtedel, olenemata kasutatavast mallist.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Tekstisisese skriptikoodi jaoks taaskasutatava fragmendi loomine

Saidiehitajas taaskasutatava fragmendi loomiseks tekstisisese skriptikoodi jaoks järgige neid juhiseid.

1. Avage **Fragmendid** ja valige seejärel **Uus**.
1. Valige dialoogiboksis **Uus fragment** suvand **Tekstisisene skript**.
1. Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.
1. Valige loodud fragmendi jaotises moodul **Tekstisisene vaikeskript**.
1. Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript. Seejärel konfigureerige teised suvandid vastavalt vajadusele.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Tekstivälise skriptikoodi jaoks taaskasutatava fragmendi loomine

Saidiehitajas taaskasutatava fragmendi loomiseks tekstivälise skriptikoodi jaoks järgige neid juhiseid.

1. Avage **Fragmendid** ja valige seejärel **Uus**.
1. Valige dialoogiboksis **Uus fragment** suvand **Väline skript**.
1. Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.
1. Valige loodud fragmendi jaotises moodul **Tekstiväline vaikeskript**.
1. Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL. Seejärel konfigureerige teised suvandid vastavalt vajadusele.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

> [!NOTE]
> Kui sisu turbepoliitika (CSP) on teie saidi jaoks lubatud, veenduge, et kõik välised URL-id oleksid lisatud rakenduse Commerce saidiehitajas CSP direktiivi **script-src**. Lisateavet leiate teemast [Sisu turbepoliitika (CSP) haldamine](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Lisage fragment, mis sisaldab malli skriptikoodi

Saidiehitajas malli skriptikoodi sisaldava fragmendi lisamiseks järgige neid juhiseid.

1. Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.
1. Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.
1. Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa fragment**.
1. Valige fragment, mille lõite oma skriptikoodi jaoks.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Tekstivälise või -sisese skripti lisamine otse malli

Kui soovite sisestada tekstisisese või -välise skripti otse ühe malli juhitavasse lehtede komplekti, ei pea te esmalt fragmenti looma.

### <a name="add-an-inline-script-directly-to-a-template"></a>Tekstisisese skripti lisamine otse malli

Saidiehitajas tekstisisese skripti otse malli lisamiseks järgige neid juhiseid.

1. Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.
1. Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.
1. Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Dialoogiboksis **Lisa moodul** valige **Tekstisisene skript**.
1. Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript. Seejärel konfigureerige teised suvandid vastavalt vajadusele.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

### <a name="add-an-external-script-directly-to-a-template"></a>Tekstvälise skripti lisamine otse malli

Saidiehitajas tekstivälise skripti otse malli lisamiseks järgige neid juhiseid.

1. Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.
1. Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.
1. Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Dialoogiboksis **Lisa moodul** valige **Tekstiväline skript**.
1. Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL. Seejärel konfigureerige teised suvandid vastavalt vajadusele.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Leheikooni lisamine](add-favicon.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
