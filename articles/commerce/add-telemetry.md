---
title: Telemeetria toetamiseks saidile skriptikoodi lisamine
description: Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686810"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Telemeetria toetamiseks saidile skriptikoodi lisamine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.

## <a name="overview"></a>Ülevaade

Veebianalüüs on oluline tööriist, kui soovite mõista, kuidas kliendid teie saidiga suhtlevad, ja teha otsuseid, mis aitavad maksimaalse teisenduse kogemust optimeerida. Saadaval on palju veebianalüüsi pakette, et aidata teid nende eesmärkide saavutamisel, nagu Google Analytics, Clicky, Moz Analytics ja KISSMetrics. Enamik veebianalüüsi pakette nõuavad, et lisaksite oma saidi kõikidele lehtedele HTML-i elemendis **\<head\>** kliendipoolse skriptikoodi.

> [!NOTE]
> Selle teema juhised rakenduvad ka teistele kohandatud kliendipoolsetele funktsioonidele, mida Microsoft Dynamics 365 Commerce ei paku.

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a>Skriptikoodi jaoks taaskasutatava lehe loomine

Lehe fragment võimaldab teil taaskasutada tekstisisest või välist skripti koodi saidi kõigil lehtedel, olenemata kasutatavast mallist.

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a>Tekstisisese skriptikoodi jaoks taaskasutatava lehe loomine

Saidiehitajas taaskasutatava lehe fragmendi loomiseks tekstisisese skriptikoodi jaoks järgige neid juhiseid.

1. Avage **Fragmendid** ja valige seejärel **Uus**.
1. Valige dialoogiboksis **Uus lehe fragment** suvand **Tekstisisene skript**.
1. Sisestage jaotises **Lehe fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.
1. Valige loodud lehe fragmendi jaotises moodul **Tekstisisene vaikeskript**.
1. Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript. Seejärel konfigureerige teised suvandid vastavalt vajadusele.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a>Tekstivälise skriptikoodi jaoks taaskasutatava lehe loomine

Saidiehitajas taaskasutatava lehe fragmendi loomiseks tekstivälise skriptikoodi jaoks järgige neid juhiseid.

1. Avage **Fragmendid** ja valige seejärel **Uus**.
1. Valige dialoogiboksis **Uus lehe fragment** suvand **Väline skript**.
1. Sisestage jaotises **Lehe fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.
1. Valige loodud lehe fragmendi jaotises moodul **Tekstiväline vaikeskript**.
1. Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL. Seejärel konfigureerige teised suvandid vastavalt vajadusele.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a>Lisage lehe fragment, mis sisaldab malli skriptikoodi

Saidiehitajas malli skriptikoodi sisaldava lehe fragmendi lisamiseks järgige neid juhiseid.

1. Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.
1. Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.
1. Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa lehe fragment**.
1. Valige fragment, mille lõite oma skriptikoodi jaoks.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Tekstivälise või -sisese skripti lisamine otse malli

Kui soovite sisestada tekstisisese või -välise skripti otse ühe malli juhitavasse lehtede komplekti, ei pea te esmalt lehe fragmenti looma.

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

[Tervitussõnumi lisamine](add-welcome-message.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)
