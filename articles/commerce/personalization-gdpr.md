---
title: Isikupärastatud soovitustest loobumine
description: See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce isikupärastatud soovituste saamisest.
author: bebeale
ms.date: 09/15/2020
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
ms.openlocfilehash: 1e7d0f505ce49bc9be0d027cbb0d636c9de0600b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804449"
---
# <a name="opt-out-of-personalized-recommendations"></a>Isikupärastatud tootesoovitustest loobumine

[!include [banner](includes/banner.md)]

See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce isikupärastatud soovituste saamisest.

Konto loomise ajal seadistatakse uued kliendid automaatselt saama isikupärastatud soovitusi. Samas pakub rakendus Dynamics 365 Commerce jaemüüjatele erinevaid võimalusi nende soovituste saamisest loobumiseks ja oma isikuandmete töötlemise piiramiseks. Autenditud kasutajad, kes loobuvad isikupärastatud soovituste saamisest, lõpetavad kohe isikupärastatud loendite nägemise. Lisaks eemaldatakse kõik isikupärastamiseks kogutavad isikuandmed isikupärastatud soovituste mudelitest.

Lisateavet isikupärastatud tootesoovituste kohta vt jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Jaemüüjate loobumiskogemuse rakendamise viisid

Jaemüüjatel on loobumiskogemuse rakendamiseks kolm viisi.

### <a name="opting-out-on-behalf-of-users"></a>Kasutajate nimel loobumine

Commerce’i kontori kontohalduses saavad jaemüüjad loobuda kasutajate nimel.

1. Otsige kontori avalehelt **kõiki kliente**.
1. Otsige ja valige klient ning seejärel valige kiirkaart **Jaemüük**.

    ![Jaemüügi kiirkaart](./media/Disablepersonalizationpart1.png)

1. Jaotises **Privaatsus** seadke suvand **Keela isikupärastamine** väärtusele **Jah**.

    ![Privaatsussätted](./media/Disablepersonalizationpart2.png)

1. Valige **Salvesta** ja sulgege leht.

### <a name="module-based-opt-out-experience"></a>Moodulipõhine loobumise kogemus

Jaemüüjad võivad lubada autenditud kasutajatel ise isikupärastatud soovitustest loobuda. Selle loobumiskogemuse pakkumiseks lisage kasutaja loobumise moodul konto profiili lehtedele.

### <a name="custom-extensions"></a>Kohandatud laiendid

Jaemüüjad saavad luua oma laiendid, et hallata kasutajate loobumise kogemust. Lisateavet vt [Jaemüügiserveri API-de kutsumine](e-commerce-extensibility/call-retail-server-apis.md) ja [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Isikupärastatud soovituste andmete digitaalse koopia hankimine autenditud kasutaja nimel

Kliendid võivad soovida saada oma isikuandmete digitaalset koopiat ja vaadata nende soovituste tulemusi ka eksporditud vaates. Kui klient seda teavet taotleb, peab jaemüüja looma kohandatud laienduse, mis kutsub jaemüügiserveri rakenduse programmeerimise liidest (API) ja päringuid teie loendist **Teile valitud**, mis põhineb kliendi ID-l. Seejärel saab tulemusi eksportida komaeraldusega väärtuste (CSV) vormingus ja jagada kliendiga.

Järgmine näide näitab, kuidas jaemüüja saab seda ülesannet täita.

1. Jaemüüja loob kohandatud laienduse, et tõmmata kasutaja nimel isiklikke soovituste andmeid. Lisateavet moodulite loomise, olemasolevate moodulite kloonimise, jaemüügiserveri API-de kutsumise ja andmetegevuste kutsumise kohta vt teemast [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).
2. Kohandatud laiend teeb kutsungi tuumandmetegevusele **hangi-soovitused** ja edastab sellele nõutud teabe, mis põhineb loendi nõuetel. Loendi **Teile valitud** korral peab laiend edastama andmetegevusele õige loendi nime ja kliendi ID.

    Üks kohandatud laiendi loomise viis on kloonida olemasolevaid toote kogumise mooduleid, mida kasutatakse soovituste tulemuste tagastamiseks. Selle olemasoleva mooduli kloonimisega saab jaemüüja olemasolevat koodi muuta ja lisada uue nupu, mis ekspordib soovituste tulemused CSV-faili. Lisateavet leiate teemast [Mooduliteegi mooduli kloonimine](e-commerce-extensibility/clone-starter-module.md) ja [Tootekogumi moodulid](product-collection-module-overview.md).

    Jaemüügiserveri API teegi täieliku vaate leiate teemast [Jaemüügiserveri kliendi ja tarbija API-d](dev-itpro/retail-server-customer-consumer-api.md).

3. Pärast kohandatud laiendi loomist saab jaemüüja eksportida CSV-faili kõigi soovituste tulemustega autenditud kasutaja kordumatu kliendi ID alusel.
4. Jaemüüja saab anda eksporditud CSV-faili, mis sisaldab soovitatavate toodete täielikku isikupärastatud loendit, autenditud kasutajaga ühiskasutusse.

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)

[Tootesoovituste KKK](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
