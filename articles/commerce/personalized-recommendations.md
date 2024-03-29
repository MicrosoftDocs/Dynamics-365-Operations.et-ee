---
title: Isikupärastatud tootesoovituste lubamine
description: See artikkel kirjeldab, kuidas teha isikupärastatud tootesoovitused klientidele kättesaadavaks Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: f626704b41b9d22f6b2ff55dd4ffe1037559a83a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283610"
---
# <a name="enable-personalized-recommendations"></a>Luba isikupärastatud soovitused

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas teha isikupärastatud tootesoovitused klientidele kättesaadavaks Microsoft Dynamics 365 Commerce.

Rakenduses Dynamics 365 Commerce saavad jaemüüjad teha kättesaadavaks isikupärastatud tootesoovitused (tuntud ka kui isikupärastamine). Sel viisil saab isikupärastatud soovitusi lisada kliendi kasutuskogemusele veebis ja kassas. Kui isikupärastamise funktsioon on sisse lülitatud, saab süsteem seostada kasutaja ostu- ja tooteteabe individualiseeritud tootesoovituste loomiseks.

## <a name="personalization-prerequisites"></a>Isikupärastamise eeltingimused

Enne isikupärastatud soovituste klientidele kättesaadavaks tegemist võtke arvesse, et tootesoovitusi toetatakse ainult nende Commerce’i kasutajate jaoks, kes on migreerinud oma salvestusruumi Azure Data Lake’i salve. Enne kui kliendid saavad võtta vastu isikupärastatud tootesoovitusi, peavad jaemüüjad [lülitama tootesoovitused sisse](enable-product-recommendations.md)soovitused sisse lülitama.

> [!NOTE]
> Tootesoovituste sisselülitamisega lülitate sisse ka isikupärastamise. Kuid kui lülitate isikupärastamise välja, ei saa te muud tüüpi tootesoovitusi välja lülitada.

Lisateavet tootesoovituste kohta leiate teemast [Tootesoovituste ülevaade](product-recommendations.md).

## <a name="turn-on-personalization"></a>Isikupärastamise sisselülitamine

Isikupärastamise sisselülitamiseks toimige järgmiselt.

1. Commerce'i peakontorist otsige valikut **Funktsioonihaldus**.
1. Saadaolevate funktsioonide vaatamiseks valige **Kõik**. 
1. Sisestage otsinguväljale **Soovitused**.
1. Valige funktsioon **Isikupärastatud tootesoovitused**.
1. Tehke atribuutide paanil **Isikupärastatud tootesoovitused** valik **Luba kohe**.

![Isikupärastamise sisselülitamine.](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Kui lülitate isikupärastamise sisse, käivitatakse isikupärastatud tootesoovituste loendite loomise protsess. Kuluda võib kuni üks päev enne, kui need loendid on saadaval ja nähtavad veebis ning kassas.

## <a name="personalized-lists"></a>Isikupärastatud loendid

Lisaks olemasolevate arvuti loodud loendite isikupärastamise lubamisele võimaldab soovituste teenus toote avastamise kogemuse isikupärastamist nii võrgus kui ka kassas.

Pärast isikupärastamise sisselülitamist saavad jaemüüjad kuvada ostjatele isikustatud loendeid „Teile valitud” veebis või loendeid „Kliendile soovitatud” kassaterminalis. Lisaks saavad jaemüüjad rakendada isikupärastamist olemasolevatele tootesoovituse loenditele ja pakkuda autenditud kasutajate jaoks isikuandmete kaitse üldmäärusest (GDPR) loobumise võimalusi. Kui lülitate isikupärastamise välja, lülitate ka need funktsioonid välja.

### <a name="online-picks-for-you-lists"></a>Veebipõhised loendid „Teile valitud”

Loend „Teile valitud” on tehisintellekti masinõppe (AI-ML) loend, mis kuvab autenditud kasutaja soovitatud toodete isikupärastatud loendi. See loend põhineb kasutaja omnikanali ostuajalool. Isikupärastatud soovitusi värskendatakse dünaamiliselt, kui kasutaja teeb rohkem oste. Seda tüüpi loend toetab ka kategooria filtreerimist, nii et jaemüüjad saavad kuvada navigeerimise hierarhial põhinevad peamised valikud.

Enne kui loend „Teile valitud” saab e-kaubanduse lehel ilmuda, peavad järgmised kasutajanõuded olema täidetud.

- Kasutajad peavad olema sisse logitud. Anonüümsed kasutajad ei näe isikupärastatud soovitusi.
- Kasutajatel peab olema kontol vähemalt üks ost.
- Kasutajad peavad isikupärastatud soovituste saamisega nõustuma.

Järgmisel joonisel on kujutatud loendi „Teile valitud” näide veebipoe lehel.

![Veebipõhine loend Teile valitud.](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>Loendid „Kliendile soovitatud” kassas

Oma kliendisuhtluse kogemuse parandamiseks saavad jaemüüjad isikupärastada olemasolevate klientide üksikasjade lehti, lisades kontekstipõhise loendi „Kliendile soovitatud”.

Järgmisel joonisel on kujutatud loendi „Kliendile soovitatud” näide kassaterminalis.

![Loend Kliendile soovitatud kassas.](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Isikupärastamise rakendamine olemasolevatele soovituste loenditele

Jaemüüjad saavad rakendada isikupärastamist olemasolevatele soovituste loenditele, nagu „Uus”, „Populaarne”, „Enim müüdud”, „Inimestele meeldib ka” ja „Sageli koos ostetud”. Olemasolevatele loenditele isikupärastamise rakendamisel eemaldatakse nendest loenditest sisselogitud kasutaja poolt varasemalt ostetud esemed. Nii anonüümsetele kasutajatele kui isikupärastatud soovituste saamisest loobunud kasutajatele kuvatakse olemasolevate loendite vaikimisi versioonid. Nii ei pea jaemüüjad eraldi lehe kogemust käsitsi haldama.

Näiteks on sisselogitud kasutaja juba ostnud musta kella ja pruunid töösaapad, mis ilmuvad järgmisel joonisel loendis „Populaarne – vaikimisi”. Seetõttu näeb kasutaja nende toodete asemel uusi tooteid, nagu on näidatud loendis „Populaarne – isikustatud”.

![Isikupärastamise rakendamine.](./media/applypersonalization.png)

Isikupärastamise rakendamiseks olemasolevale soovituste loendile rakenduse Commerce saidiehitajas, toimige järgmiselt.

1. Avage olemasoleva saidiehitaja leht, mis sisaldab tootekogumi moodulit.
1. Valige vasakpoolsel navigeerimispaanil tootekogumi moodul.
1. Valige parempoolsel navigeerimispaani jaotises **Tooted** loend.
1. Dialoogiaknas **Vali toote loendi konfigureerimine** jaotises **Tüüp** valige loendi tüüp.
1. Valige märkeruut **Rakenda isikupärastamine** ja valige seejärel **OK**.

    ![Populaarsete loendile isikupärastamise rakendamine.](./media/ApplyPersonalizationToTrending.PNG)

1. Salvestage leht, lõpetage selle redigeerimine ja seejärel avaldage see. Pärast lehe avaldamist kuvatakse sisselogitud kasutajatele isikupärastatud populaarsete loendeid.

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[ Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
