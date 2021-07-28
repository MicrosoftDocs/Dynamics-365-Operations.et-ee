---
title: Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas
description: Selles teemas selgitatakse, kuidas lubada Azure Data Lake Storage Dynamics 365 Commerce'i keskkonnas, mis on tootesoovituste lubamise eeltingimus.
author: bebeale
ms.date: 04/13/2020
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
ms.openlocfilehash: 9ac440362379475b05c6a37019c25e3a96be3739
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349492"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas lubada Azure Data Lake Storage Dynamics 365 Commerce'i keskkonnas, mis on tootesoovituste lubamise eeltingimus.

Dynamics 365 Commerce lahenduses jälgitakse kogu toote ja kande teavet keskkonna üksuse kaupluses. Et muuta need andmed kättesaadavaks teistele Dynamics 365 teenustele, nagu andmeanalüütika, äriteave ja isikupärastatud soovitused, on vaja ühendada keskkond kliendi omanduses oleva Azure Data Lake Storage Gen 2 lahendusega.

Kuna Azure Data Lake Storage on keskkonnas konfigureeritud, võetakse kõik vajalikud andmed üksusesalvest, mis on endiselt kaitstud ja kliendi kontrolli all.

Kui tootesoovitused või isikupärastatud soovitused on keskkonnas samuti lubatud, antakse tootesoovituste virnale juurdepääs spetsiaalsele kaustale Azure Data Lake Storage'is, et tuua kliendi andmed ja arvutada nende põhjal soovitusi.

## <a name="prerequisites"></a>Eeltingimused

Klientidel peab olema Azure Data Lake Storage konfigureeritud Azure'i kordustellimuses, mida nad omavad. See teema ei hõlma Azure'i kordustellimuse ostmist või Azure Data Lake Storage'i toega salvestusruumi konto seadistamist.

Lisateavet Azure Data Lake Storage'i kohta vt [Azure Data Lake Storage Gen 2 ametlikust dokumentatsioonist](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfiguratsiooni etapid

See jaotis hõlmab konfigureerimistoiminguid, mis on vajalikud Azure Data Lake Storage'i lubamiseks keskkonnas, kuna see on seotud tootesoovitustega.
Azure Data Lake Storage'i lubamiseks vajalikest toimingutest põhjalikuma ülevaate saamiseks vaadake teemat [Muuda üksusesalv Data Lake’i üksusena saadavaks](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Azure Data Lake Storage'i lubamine keskkonnas

1. Logige sisse keskkonna kontoriportaali.
1. Otsige **Süsteemi parameetreid** ja navigeerige vahekaardile **Andmeühendused**. 
1. Määrake **Luba Data Lake integratsioon** väärtuseks **Jah**.
1. Määrake **Data Lake värskenduse niristamine** väärtuseks **Jah**.
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
