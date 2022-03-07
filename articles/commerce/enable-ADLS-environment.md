---
title: Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas
description: See teema annab juhiseid, kuidas ühendada Azure Data Lake Storage Gen 2 lahendus Dynamics 365 Commerce keskkonna üksuselaoga. See on nõutav samm enne tootesoovituste lubamist.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c96c29a4d9639b02e6a60ad938b7e06f7d500c68
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466288"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas

[!include [banner](includes/banner.md)]

See teema annab juhiseid, kuidas ühendada Azure Data Lake Storage Gen 2 lahendus Dynamics 365 Commerce keskkonna üksuselaoga. See on nõutav samm enne tootesoovituste lubamist.

Lahenduses Dynamics 365 Commerce koondatakse soovituste, toodete ja kannete arvutamiseks vajalikud andmed keskkonna üksuse poodi. Et muuta need andmed kättesaadavaks teistele Dynamics 365 teenustele, nagu andmeanalüütika, äriteave ja isikupärastatud soovitused, on vaja ühendada keskkond kliendi omanduses oleva Azure Data Lake Storage Gen 2 lahendusega.

Kui ülaltoodud sammud on lõpule viidud, peegeldatakse kõik keskkonna olemilao kliendiandmed automaatselt kliendi Azure Data Lake Storage Gen 2 lahendusele. Kui Commerce headquarters`i funktsioonihalduse tööruumi kaudu on soovituste funktsioonid lubatud, antakse soovituste pinu juurdepääs samale Azure Data Lake Storage Gen2 lahendusele.

Kogu protsessi jooksul jäävad kliendi andmed kaitstuks ja nende kontrolli all.

## <a name="prerequisites"></a>Eeltingimused

Keskkonna Dynamics 365 Commerce olemiladu peab olema ühendatud kontoga Azure Data Lake Gen Storage Gen2 ja sellega kaasnevad teenused.

Lisateavet Azure Data Lake Storage Gen2 ja selle kohta, kuidas seda seadistada, vaata [Azure Data Lake Storage Gen 2 ametlikust dokumentatsioonist](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfiguratsiooni etapid

See jaotis hõlmab konfigureerimistoiminguid, mis on vajalikud Azure Data Lake Storage Gen2 keskkonnas, kuna see on seotud tootesoovitustega.
Põhjalikuma ülevaate Azure Data Lake Storage Gen2 lubamiseks vajalikest toimingutest vaadake teemast [Muuda üksusepood saadavaks Data Lake üksusena](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Azure Data Lake Storage'i lubamine keskkonnas

1. Logige sisse keskkonna kontoriportaali.
1. Otsige **Süsteemi parameetreid** ja navigeerige vahekaardile **Andmeühendused**. 
1. Määrake **Luba Data Lake integratsioon** väärtuseks **Jah**.
1. Seejärel sisestage järgmine kohustuslik teave:
    1. **Rakenduse ID** // **Rakenduse saladus** // **DNS-i nimi** – vajalik ühenduse loomiseks KeyVaultiga, kus on talletatud Azure Data Lake Storage saladus.
    1. **Salajane nimi** – KeyVaulti salvestatud salajane nimi, mida kasutatakse Azure Data Lake Storage'i autentimiseks.
1. Salvestage muudatused lehe ülemises vasakus nurgas.

Järgmisel pildil on näide Azure Data Lake Storage'i konfiguratsioonist.

![Azure Data Lake Storage'i konfiguratsiooni näide.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Azure Data Lake Storage'i ühenduse kontrollimine

1. Testige ühendust KeyVault, kasutades **Testi Azure Key Vault** linki.
1. Testige Azure Data Lake Storage'i ühendust lingi **Testi Azure Storage'it** abil.

> [!NOTE]
> Kui testid ebaõnnestuvad, kontrollige, kas kõik ülaltoodud KeyVaulti andmed on õiged ja proovige uuesti.

Kui ühenduse testid on edukad, peate lubama automaatse värskendamise üksuse kaupluses.

Üksuse poe automaatse värskendamise lubamiseks toimige järgmiselt.

1. Otsige **Üksuse kauplust**.
1. Liikuge vasakpoolses loendis kirjeni **RetailSales** ja valige **Redigeeri**.
1. Veenduge, et **Automaatne värskendamine lubatud** väärtuseks oleks seatud **Jah**, valige **Värskenda** ja seejärel **Salvesta**.

Järgmisel pildil on üksuse kaupluse näide, millel automaatne värskendamine on lubatud.

![Üksuse kaupluse näide, millel automaatne värskendamine on lubatud.](./media/exampleADLSConfig2.png)

Azure Data Lake Storage on nüüd keskkonna jaoks konfigureeritud. 

Kui see ei ole juba lõpule viidud, järgige juhiseid keskkonna [tootesoovituste ja isikupärastamise lubamiseks](enable-product-recommendations.md).

## <a name="additional-resources"></a>Lisaressursid

[Üksusesalve Data Lake’i üksusena saadavaks muutmine](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Tootesoovituste ülevaade](product-recommendations.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
