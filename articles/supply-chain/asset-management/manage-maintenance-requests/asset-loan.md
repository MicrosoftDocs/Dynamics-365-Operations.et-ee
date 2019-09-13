---
title: Varade laenud
description: Selles teemas kirjeldatakse, kuidas registreerida laenuvarasid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8680241b1300aceda3280893982a1eff3d2e09e0
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847478"
---
# <a name="asset-loans"></a>Varade laenud

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kui teie ettevõte saab varasid remondi- või hooldustööde jaoks kas sisemistest asukohtadest või klientidelt ja kui te ajutiselt laenate varasid nendele asukohtadele või klientidele, saab varahaldus jälgida varalaene.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Vara laenude registreerimine hooldustaotluse korral

1. Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Kõik hooldustaotlused** või **Aktiivsed hooldustaotlused**.
2. Valige hoolduspäring, kuhu soovite varalaenu registreerida, ja seejärel valige **Redigeeri**.
3. Lehel **Taotle** valige **Saada laenuvara**.
4. Valige vara ja sisestage eeldatav tagastuskuupäev.
5. Valige nupp **OK**.

> [!NOTE]
> - Laenuvara saate saata ainult siis, kui sama vara tüüpi vara on saadaval.
> - Varal, mida laenate peab olema vara elutsükli olek, mis võimaldab seda kasutada laenuvarana, nt **InStorage**. Kui vara laen on registreeritud, värskendatakse vara elutsükli olekut automaatselt, nt **OnLoan**.

Kõigi teistele asukohtadele või klientidele laenatud varade loendi vaatamiseks valige **Varahaldus**\>**Üldine**\>**Varalaen**\>**Kõik varalaenud**. Kui vara jaoks on valitud märkeruut **Lõpetatud**, on vara teie ettevõttele registreeritud kui tagastatud.

![Joonis 1](media/06-manage-maintenance-requests.png)

Lehel **Aktiivsed varalaenud** saate vaadata loendit kõigist laenuvaradest, mis pole veel teie ettevõttele tagastatud.

## <a name="register-loan-assets-as-returned"></a>Registreeri laenuvarad kui tagastatud

1. Valige **Varahaldus**\>**Üldine**\>**Varalaen**\>**Aktiivsed varalaenud**.
2. Valige varalaen, mida soovite registreerida kui tagastatud ja seejärel valige **Tagasta varalaen**.
3. Väljale **Tagastatud** sisestage kuupäev ja kellaaeg.
4. Valige nupp **OK**.
5. Värskendage loendilehte **Aktiivsed varalaenud** ja märkate, et varalaenu ei kuvata enam loendis.