---
title: Hindade, allahindluste, lepete ja tagasimaksete tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada hindadega, allahindlustega, lepetega ja tagasimaksetega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 14fdddabde7739cbf9ba0fcee0fa0b8b816e74dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007362"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Hindade, allahindluste, lepete ja tagasimaksete tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada hindadega, allahindlustega, lepetega ja tagasimaksetega töötamisel tekkivaid probleeme.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Pärast ostutellimuse loomist ei saa ma ostulepingut ostutellimuse reaga siduda.

Ostutellimuse loomisel tuleb ostuleping ostutellimusega seostada. Vastasel juhul ei saa ostutellimuse ridu seostada ostulepingu ridadega.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Mis põhjustab teate „Värskendatud hinnad ja allahindlused sisestati käsitsi või tegemist on välise dokumendiga”?

Kui muudate tarnekuupäeva, võidakse kuvada teade „Värskendatud hinnad ja allahindlused sisestati käsitsi või tegemist on välise dokumendiga”. Te saate selle teate, kuna lähetuskuupäeva muutmisel võidakse aktiveerida muu kaubanduslepe või müügileping, mis võib hindu muuta. Lähetuskuupäeva muutmine võib mõjutada ka laograafikuid ja muud seotud teavet.

Teade kuvatakse, kui muudetakse mõnda kuupäeva või muud parameetrit. Teate eesmärk on teha kindlaks, et te olete teadlik hinnamuutustest, mis võivad tekkida nende muudatuste tõttu.

See teade on kaubandusleppe hindamise (TAE) viip. Täieliku kirjelduse leiate teemast [Kaubandusleppe hindamise poliitika](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Ostutellimuse sissetulek ei sisalda kõiki kulusid.

### <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Veenduge, et lehe **Hankeparameetrid** vahekaardil **Tarne** oleks suvandi **Loo toote sissetuleku kulud** väärtuseks seatud *Jah*.
1. Looge ostutellimus, mis sisaldab kulusid.
1. Kinnitage ostutellimus.
1. Võtke ostutellimus vastu.
1. Vaadake sissetuleku kogusummat ja võrrelge seda oodatud kogusummaga.
1. Pange tähele, et ostutellimuse sissetulek ei sisalda kõiki kulusid.

### <a name="issue-resolution"></a>Probleemi lahendamine

Lahendus sõltub sellest, kuidas lisakulud on seadistatud. Teavet lisakulude seadistamise kohta oma vajaduste järgi leiate ajaveebipostitusest [Lisakulude sisestamine toote sissetuleku ajal](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Kaubandusleppe hindu ja allahindlusi ei rakendata müügi- või ostutellimuse ridadel, mis imporditakse andmehalduse kaudu.

### <a name="issue-description"></a>Probleemi kirjeldus

Müügi- või ostutellimuse ridade puhul kohalduvaid kaubandusleppeid ei rakendata ridadel, mis imporditakse andmehalduse kaudu. Samas rakendatakse samu kaubandusleppeid käsitsi loodud müügi- või ostutellimuse ridadel.

### <a name="reason-for-the-issue"></a>Probleemi põhjus

Kui andmehalduse kaudu imporditud ostutellimuse read sisaldavad juba hinnateavet, ei hinnata kaubanduslepet nende ridade puhul ümber. Näiteks kui rea puhul on seadistatud **Rea allahindluse protsent** või mis tahes hinna ja allahindluse väärtus, siis ei otsita selle rea puhul kaubandusleppeid.

### <a name="issue-workaround"></a>Probleemi lahendus

Selline käitumine on oodatud ja on sarnane nii müügi- kui ka ostutellimuste puhul.

Lahendusega importige ostutellimuse read ilma hinnateavet määramata. Seejärel rakendatakse kaubandusleppeid ja ostutellimuse read värskendatakse määratletud kaubanduslepete alusel.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Hankija tagasimakset ei kumuleerita arvete põhjal.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui sisestatud arvetel on eri tähtajad, ei kajastu need arved hankija tagasimaksetes, mis on nende põhjal loodud.

### <a name="issue-resolution"></a>Probleemi lahendamine

See on tahtlik, et hankija tagasimakse arvutamisel ei arvestata tähtaega. Kaaluge süsteemi kohandamist nii, et tähtaeg ja suhe arvega avalduks tegeliku hankija tagasimakse puhul selgemalt.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Ostutellimuste ühiku hindasid ei arvutata ühikuteisenduse alusel.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui ostutellimusel muudetakse ühikut, ei arvutata kaubandusleppe hindu ühikuteisenduse määratluste alusel ümber.

### <a name="issue-resolution"></a>Probleemi lahendamine

Hinnad võetakse alati kaubanduslepetest (või muudest süsteemis olevatest hinnasätetest, nt müügilepingutest või kauba hindadest) ja need määratakse ühikule.

Kui ühikut tellimuse real muudetakse, otsib süsteem uue ühiku jaoks üles hinna ja rakendab seda hinda. Kui ühiku jaoks ei leita hinda, ei rakenda süsteem hinda. Ühikuteisendust ei saa kasutada hinna ümberarvutamiseks teiseks ühikuks. Teoreetiliselt ei pruugi ühe kümmet kaupa sisaldava karbi hind võrduda kümne karbi hinnaga.

### <a name="issue-workaround"></a>Probleemi lahendus

Üks viis selle probleemi lahendamiseks on veenduda, et ühikute jaoks, mida hakatakse kauba puhul tellimuse ridadel kasutama, oleks olemas kaubanduslepped.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Kaubanduslepete puhul tekivad valuuta teisenduse probleemid.

Kaubandusleppe hindu ei arvutata valuuta põhjal ümber, kui valuuta on ostutellimusel erinev.

Funktsioon *Üldvaluuta* võimaldab teil määratleda hindu ja allahindlusi ainult ühes valuutas. Seejärel saate neid vajaduse korral muusse valuutasse teisendada. Lisaks saab funktsioon pärast teisenduse lõpetamist automaatselt rakendada nutikat ümardamist.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Kui ma avan lehe „Ostuleping” reavaaterežiimis, ei saa ma lehte isikupärastada välja „Hinnaühik” lisamise kaudu rea ülevaatesse.

Mõnda lepperaamistiku jagatud välja ei saa isikupärastamistes kasutada. See piirang tuleneb juurutatud andmemudelist. Seetõttu ei saa te välja **Hinnaühik** isikupärastada.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Ostulepingust pärit ülempiirlepe ei kehti ostutaotluses.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui ostutaotlus seotakse ostulepinguga, ei kehti ostutaotluse puhul ostulepingust pärit ülempiir. Vaikehinnateave on õigesti sisestatud, kuid ostutaotluse kaudu saab tellida koguse, mis ületab ostulepingu ülempiiri.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on oodatud. Kuna taotlusi ei kinnitata alati, ei tohi ostulepingus kogust või summat reserveerida. Seetõttu ei saa te kasutada ostulepingu ülempiiri.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Kaubandusleppeid saab luua tagasilükatud pakkumiskutsete põhjal. Seetõttu ei takista süsteem kaubandusleppe töölehtede loomist juhul, kui pakkumiskutse rida pole aktsepteeritud.

Saate luua kaubandusleppeid pakkumiskutsete (RFQ) kõigi vastuste puhul olenemata sellest, kas need on aktsepteeritud või tagasi lükatud. Lisateavet leiate teemast [Pakkumiskutsete (RFQ-de) ülevaade](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]