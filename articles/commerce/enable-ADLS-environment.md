---
title: ADLS lubamine Dynamics 365 Commerce keskkonnas
description: Selles teemas selgitatakse, kuidas lubada Azure Data Lake Storage (ADLS) ja katsetada Dynamics 365 Commerce keskkonda, mis on toote soovituste lubamise eeltingimus.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025239"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>ADLS lubamine Dynamics 365 Commerce keskkonnas

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas lubada Azure Data Lake Storage (ADLS) ja katsetada Dynamics 365 Commerce keskkonda, mis on toote soovituste lubamise eeltingimus.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce lahenduses jälgitakse kogu toote ja kande teavet keskkonna üksuse kaupluses. Et muuta need andmed kättesaadavaks teistele Dynamics 365 teenustele, nagu andmeanalüütika, äriteave ja isikupärastatud soovitused, on vaja ühendada keskkond kliendi omanduses oleva Azure Data Lake Storage Gen 2 (ADLS) lahendusega.

Kuna ADLS on keskkonnas konfigureeritud, peegeldatakse kõik vajalikud andmed üksuse kauplusest, mis on endiselt kaitstud ja kliendi kontrolli all.

Kui toote soovitused või isikupärastatud soovitused on keskkonnas samuti lubatud, antakse toote soovituste pinule juurdepääs spetsiaalsele kaustale ADLS-is, et tuua kliendi andmed ja arvutada selle põhjal soovitusi.

## <a name="prerequisites"></a>Eeltingimused

Klientidel peab olema ADLS konfigureeritud Azure'i kordustellimuses, mida nad omavad. See teema ei hõlma Azure'i kordustellimuse ostmist või ADLS-toega salvestusruumi konto häälestust.

Lisateavet ADLS kohta vt [ADLS ametlikust dokumentatsioonist](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfiguratsiooni etapid

Selles jaotises käsitletakse ADLS lubamiseks vajalikke konfiguratsiooni etappe.

### <a name="enable-adls-in-the-environment"></a>ADLS lubamine keskkonnas

1. Logige sisse keskkonna kontoriportaali.
1. Otsige **Süsteemi parameetreid** ja navigeerige vahekaardile **Andmeühendused**. 
1. Määrake **Luba Data Lake integratsioon** väärtuseks **Jah**.
1. Määrake **Data Lake värskenduse niristamine** väärtuseks **Jah**.
1. Seejärel sisestage järgmine kohustuslik teave:
    1. **Rakenduse ID** // **Rakenduse saladus** // **DNS-i nimi** – vajalik ühenduse loomiseks KeyVaultiga, kus ADLS saladus on talletatud.
    1. **Salajane nimi** – KeyVaulti salvestatud salajane nimi, mida kasutatakse ADLS autentimiseks.
1. Salvestage muudatused lehe ülemises vasakus nurgas.

Järgmine pilt näitab näidet ADLS konfiguratsioonist.

![Ekspordi ADLS konfiguratsioon](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>ADLS ühenduse kontrollimine

1. Testige ühendust KeyVault, kasutades **Testi Azure Key Vault** linki.
1. Testige ühendust ADLS-iga, kasutades **Testi Azure Storage** linki.

> [!NOTE]
> Kui testid ebaõnnestuvad, kontrollige, kas kõik ülaltoodud KeyVaulti andmed on õiged ja proovige uuesti.

Kui ühenduse testid on edukad, peate lubama automaatse värskendamise üksuse kaupluses.

Üksuse poe automaatse värskendamise lubamiseks toimige järgmiselt.

1. Otsige **Üksuse kauplust**.
1. Liikuge vasakpoolses loendis kirjeni **RetailSales** ja valige **Redigeeri**.
1. Veenduge, et **Automaatne värskendamine lubatud** väärtuseks oleks seatud **Jah**, valige **Värskenda** ja seejärel **Salvesta**.

Järgmisel pildil on üksuse kaupluse näide, millel automaatne värskendamine on lubatud.

![Üksuse kaupluse näide, millel automaatne värskendamine on lubatud](./media/exampleADLSConfig2.png)

ADLS on nüüd keskkonna jaoks konfigureeritud. 

Kui see ei ole juba lõpule viidud, järgige juhiseid keskkonna [tootesoovituste ja isikupärastamise lubamiseks](enable-product-recommendations.md).

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Tootesoovituste lubamine](enable-product-recommendations.md)

[Tootesoovituste loendite lisamine lehtedele](add-reco-list-to-page.md)

[Soovituste juhtelemendi lisamine kassaseadmete kandekuvale](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)


