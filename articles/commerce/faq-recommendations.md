---
title: Tootesoovituste KKK
description: Sellest teemast leiate teavet toimingute ja tööriistade kohta, mida saate kasutada toote soovituste või nende tulemustega seotud probleemide tõrkeotsinguks.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f0140f798e000ca66c67afa00f788abc560c8a07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216695"
---
# <a name="product-recommendations-faq"></a>Tootesoovituste KKK


[!include [banner](includes/banner.md)]

Sellest teemast leiate teavet toimingute ja tööriistade kohta, mida saate kasutada [toote soovituste](product-recommendations.md) või nende tulemustega seotud probleemide tõrkeotsinguks.

## <a name="best-practices"></a>Head tavad
Väga oluline on kasutada tooteetalonide ja -variantide kontseptsiooni. Ülema tooteetaloni variantide mõistlik rühmitamine aitab loetleda algoritme ja teenus loob paremaid mudeleid. Lisaks saab teenus kasutada ainult üht toote eksemplari, mitte panna kõik lähedalt seotud variandid loendisse. Kui kõik lähedalt seotud variandid pannakse loendisse, võivad ilmneda valed või topelttulemused.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Miks puuduvad tooted soovituste loenditest?

Tavaliselt kui toode puudub toote soovituste loendist, võib esineda toote konfiguratsiooni probleem. Näiteks võib olla toote algus- või lõppkuupäev olla vale, mõõtmed võivad olla valesti konfigureeritud või toode ei pruugi olla õiges kanali sortimendis jne.

Kui kaup puudub tehisintellekti masinõppel (AI-ML) põhinevast soovituste loendist, võib toode mitte vastata soovituste loendi kriteeriumitele või see ei pruugi omada piisavalt ostutehinguid, et soovituste loend seda näitaks.

Soovitame teil kontrollida järgmisi etappe.
1. **Veenduge, et toodete soovitused oleksid lubatud HQ-s.** Lisateavet selle teenuse lubamise kohta leiate teemast [Tootesoovituste lubamine](enable-product-recommendations.md).
1. **Veenduge, et toote põhiatribuudid oleksid määratud.** Näiteks peavad tootesortimendid olema määratud valikule **Kaasa**.
1. **Värskelt sorditud toodete puhul võib kuluda kuni 3 tundi, enne kui toode hakkab uues loendis ilmuma.**
1. **Kui toode ei ilmu ikka veel suvandites Populaarne, Enim müüdud, inimestele meeldib ka, või Sageli koos ostetud, siis ei pruugi sellel tootel olla piisavalt kandeid.** Sellisel juhul võite oodata, kuni esineb rohkem kandeid, värskendada vaikimisi soovituste loendi parameetreid või kasutada käsitsi sekkumist soovituste tooteloendi tulemuste muutmiseks. Lisateavet soovituse parameetrite kohta vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).
1. **Veenduge, et toode vastaks loendi soovituste kriteeriumidele.** Lisateavet toote soovituse parameetrite kohta vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Kuidas ma saan vältida kehvade soovituse tulemuste tagastamist?

Soovituste loendid vajavad tulemuste esitamiseks suurt tehingute hulka. Seetõttu on oluline, et kasutajad esitaksid täieliku ajaloolise kandeteabe.

Lisaks ei ole toodetel, millel puuduvad kanded või mis omavad vähe kandeid, tulemusi **Inimestele meeldib ka** või **Sageli koos ostetud**, seega need soovituse loendites **Populaarsed** ega **Enim müüdud** ei ilmu. Selline olukord võib sageli esineda väga uute toodete puhul või vanade toodete puhul, mida on vähe ostetud. Populaarsete uute kaupadega laheneb see probleem hõlpsalt.

Soovitame teil järgida järgmisi etappe.
1. **Veenduge, et toode vastaks selle loendi soovituste kriteeriumidele.** Lisateavet toote soovituse parameetrite kohta vaadake teemast AI-ML-põhiste tootesoovituse tulemuste muutmine.
1. **Kui toode on uus, kaaluge soovituste loendi muutmist, kuni tootel on rohkem kandeid.** Lisateavet selle kohta, kuidas soovituse loendi tulemusi muuta, vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).


- **Veenduge, et toode vastaks selle loendi soovituste kriteeriumidele.** Lisateavet toote soovituse parameetrite kohta vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).
- **Kui toode on uus, kaaluge soovituste loendi muutmist, kuni tootel on rohkem kandeid**. Lisateavet selle kohta, kuidas soovituse loendi tulemusi muuta, vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Kas ma saan toote eemaldada, kuid seda endiselt poes näha?

Kui ettevõttel tekib vajadus, saate algoritmiliselt loodud loendeid reguleerida. Samas kui toode soovituse loendist eemaldatakse, jääb toode kaupluses leitavaks. Lisateavet selle kohta, kuidas toote soovituse tulemusi muuta, vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).

Kui peate blokeerima kauba poes avastamise, peate muutma suvandi **Kauba sortiment** valikule **Välista**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Kuidas lisada loendit e-kaubanduse lehele?

Lisateavet toote soovituse lehtede e-kaubanduse veebisaidile lisamise kohta leiate teemast [Tootesoovituste loendite lisamine lehtedele](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Kuidas lubada tootesoovitused kassas?

Pärast tootesoovituste lubamist peate lisama soovituste paneeli juhtelemendi kassaekraanile. Lisateabe saamiseks vt [Soovituste juhtelemendi lisamine kassaseadmete kandekuvale](add-recommendations-control-pos-screen.md).

## <a name="additional-resources"></a>Lisaressursid

[Tootesoovituste ülevaade](product-recommendations.md)

[Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas](enable-adls-environment.md)

[Luba tootesoovitused](enable-product-recommendations.md)

[Isikupärastatud soovituste lubamine](personalized-recommendations.md)

[Isikupärastatud tootesoovitustest loobumine](personalization-gdpr.md)

[„Sarnaste toodete vaatamise” soovituste lubamine](shop-similar-looks.md)

[Tootesoovituste lisamine kassas](product.md)

[Soovituste lisamine kandeekraanile](add-recommendations-control-pos-screen.md)

[AI-ML-i soovituste tulemuste kohandamine](modify-product-recommendation-results.md)

[Loo kuraatorite soovitused käsitsi](create-editorial-recommendation-lists.md)

[Soovituste loomine demoandmetega](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]