---
title: Varade laenud
description: Selles teemas kirjeldatakse, kuidas registreerida laenuvarasid varahalduses.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65809d9be39372412d5d6b419f7356fe2c9668a1a01ede32ef52cbd66753e6d7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752846"
---
# <a name="asset-loans"></a>Varade laenud

[!include [banner](../../includes/banner.md)]

 

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

![Hooldusnõuete haldamine.](media/06-manage-maintenance-requests.png)

Lehel **Aktiivsed varalaenud** saate vaadata loendit kõigist laenuvaradest, mis pole veel teie ettevõttele tagastatud.

## <a name="register-loan-assets-as-returned"></a>Registreeri laenuvarad kui tagastatud

1. Valige **Varahaldus**\>**Üldine**\>**Varalaen**\>**Aktiivsed varalaenud**.
2. Valige varalaen, mida soovite registreerida kui tagastatud ja seejärel valige **Tagasta varalaen**.
3. Väljale **Tagastatud** sisestage kuupäev ja kellaaeg.
4. Valige nupp **OK**.
5. Värskendage loendilehte **Aktiivsed varalaenud** ja märkate, et varalaenu ei kuvata enam loendis.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]