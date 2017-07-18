---
title: "Toodete ja tootevariantide otsimine tellimuse sisestamise käigus"
description: "Kasutage välja <strong>Kaubakood </strong>, et otsida tooteid ja tootevariante, kui loote käsitsi müügi- või ostutellimuse rea.  See võimaldab teil kiiresti leida tootevariante, kui teil on ainult konfiguratsiooni string või üks saadaolevatest tootedimensioonidest."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3960cc3eb9b8d488973d258db45aa0ab9f1dd988
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

---

# <a name="search-for-products-and-product-variants-during-order-entry"></a>Toodete ja tootevariantide otsimine tellimuse sisestamise käigus

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]

Kasutage välja <strong>Kaubakood </strong>, et otsida tooteid ja tootevariante, kui loote käsitsi müügi- või ostutellimuse rea.  See võimaldab teil kiiresti leida tootevariante, kui teil on ainult konfiguratsiooni string või üks saadaolevatest tootedimensioonidest.

Mõnikord, kui millestki on üleküllus, pole see parim olukord, kus olla, ja see on eriti tõsi siis, kui müüte sarnaseid tooteid ja proovite meeles pidada kaubanumbreid või toote otsingunimesid, et müügitellimusele sisestamiseks õiget toodet leida. Saate kasutada müügi- või ostutellimuse real olevat välja **Kaubakood** otsinguväljana. Saate sisestada mis tahes osa tootenimest, numbri või dimensiooni ja saate otsingu, mis kuvab kõik otsingusõnale vastavad kaubad.

## <a name="how-search-works"></a>Otsingu tööpõhimõte
Toodete ja tootevariantide otsimisel on oluline mõista, kuidas otsingufunktsioon leiab tooted, mis vastavad teie sisestatud tekstile. Peamised otsingureeglid otsingutulemuste saamiseks on järgmised.

-   Otsingutulemused annavad mis tahes vastava kirje, eirates välja, kuhu otsingutekst on sisestatud.
-   Otsingutekst peab vastavas kirjes esinema selle täispikkuses.
-   Vastavus ilmneb isegi juhul, kui otsingutekst leitakse vastavas kirjes tekstistringi keskel. See ei pea ilmnema tekstistringi alguses.
-   Otsinguteksti käsitletakse ühe tekstistringina isegi siis, kui see sisaldab tühimärki.

### <a name="examples"></a>Näited

Järgmised näited kasutavad tooteid ja tootevariante, et kirjeldada, kuidas otsingut käsitletakse erinevates stsenaariumides. **Eeltingimus:** jaotises **Müük ja turundus &gt; Seadistus &gt; Otsing &gt; Otsinguparameetrid** &gt; **Otsingu tüüp** valige suvand **Täieliku vastavus**.

| Toote tüüp     | Toote nimi    | Tootenumbri kuvamine | Kaubakood | Konfiguratsioon |
|------------------|-----------------|------------------------|-------------|---------------|
| Eristatav toode | SpeakerMidRange | D0001                  | D0001       | Pole            |
| Tootevariant  | Aktiivne kõlar  | D0010:::must:         | D0010       | 000005        |
| Tootevariant  | Aktiivne kõlar  | D0010:::valge:         | D0010       | Valge         |

Kui sisestate „kõla” väljale **Kaubakood**, saate kõik eespoolt toodud tooted otsingu tulemusena. Kui sisestate väljale **Kaubakood** sõna „must”, saate tulemusena teise toote, kuna sellel on tekst „must” ekraani tootenumbris. Need kaks näidet kirjeldavad, et otsing ei ole ainult välja alguses, vaste esineb isegi siis, kui otsingutekst leitakse vastava kirje tekstistringi keskel.  

Kui sisestate „05”, saate tulemuseks ainult teise tootevariandi, kuna sellel on konfiguratsioonis „05”. See kirjeldab, et otsing on kõikides lubatud väljades lehel **Otsingukriteeriumid**.  

Kui sisestate „kõla 05”, ei saa te ühtki tulemust. Seda seetõttu, et otsib otsib sisestatud täisteksti. Otsing ei proovi leida „kõla” ja seejärel kitsendada tulemusi nendeni, mis sisaldavad „05”.  

Saate piirata otsingutulemuste arvu, kasutades välja **Tulemuste arv** lehel **Müük ja turundus &gt; Seadistus &gt; Otsing &gt; Otsinguparameetrid**. Kui määrate selle välja väärtuseks 0, tagastatakse kõik otsingutulemused. Kui määrate näiteks väärtusele 10, tagastab see maksimaalselt 10 otsingutulemust.

## <a name="configure-the-product-search"></a>Tooteotsingu konfigureerimine
Enne kui saate kasutada toote ja tootevariandi otsingufunktsiooni, järgige tooteotsingu konfigureerimiseks neid etappe. [![3 etappi tooteotsingu konfigureerimiseks\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>1.etapp. Lisage otsingukriteeriumitesse kõik asjakohased toote ja tootevariandi identifikaatorid.

Näited toote ja tootevariandi identifikaatoritest ja dimensioonidest, millega saate otsida, on **Toote nimetus, Kaubakood**, **Tootenumbri kuvamine, Konfiguratsioon, Värv, Suurus, Laad, Otsingunimi, jne**.  

Valige **Müük ja turundus &gt; Seadistus &gt; Otsing &gt; Otsingukriteeriumid**. Leht **Otsingukriteeriumid** võimaldab teil määratleda kliendi, potentsiaalse kliendi ja tooteotsingu kriteeriumid. Veenduge, et filtreerite lehte, kasutades toote otsingukriteeriume. Selleks lülituge lehe menüüs valikule **Toode**.  

Kuvatava tootenumbri otsingukriteeriumidele lisamiseks klõpsake lehe menüüs nuppu **Uus**. See lisab ruudustikku **Otsingukriteeriumid** uue kirje. Avage veeru otsing **Välja nimi** ja valige **DisplayProductNumber**. Toote konfiguratsiooni otsingukriteeriumidele lisamiseks looge uus kirje ruudustikus **Otsingukriteeriumid** ja valige väärtus **configId** veerus **Välja nimi**. Samal viisil looge värvi dimensiooni jaoks kirje väärtusega **Välja nimi** **InventColorId**, suuruse dimensiooni jaoks kirje väärtusega **InventSizeId** ja laadi dimensiooni jaoks kirje väärtusega **InventStyleId**.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>2. etapp. Asustage andmebaasi tabel, mida kasutatakse tooteotsinguks

Lehel **Otsingukriteeriumid** klõpsake nuppu **Otsinguandmete värskendamine**. Dialoogiboksis **Otsinguandmete värskendamine** veenduge, et valik **Allikas** on seatud väärtusele **Toode** ja seejärel klõpsake **OK**. Süsteem koondab ühte tabelisse kõik valitud 1. etapis määratud otsingukriteeriumid. Kui teil on palju tooteid ja tootevariante, võib see toiming olla üsna pikk ja teile võidakse kuvada hoiatus. Soovitame teil plaanida otsingutabeli asustamise pakktöötluse serverisse ajal, mil server ei ole liiga hõivatud.  

Kuni tabel on asustatud, ei anna tooteotsing õigeid tulemusi. Kui te ei saa ühtki otsingutulemust, veenduge, et see tabel on asustatud.  

Tabel peab olema asustatud ainult otsingukriteeriumite modifitseerimisel. Värskelt väljastatud tooted ja variandid lisatakse automaatselt tabelisse. Kustutatud tooted ja variandid eemaldatakse automaatselt tabelist.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>3. etapp. Lubage tooteotsing müügi- ja ostutellimuse ridadel

Saate selle funktsiooni lubada, valides **Müük ja turundus &gt; Seadistus &gt; Otsing &gt; Otsinguparameetrid** ja seades vahekaardil **Üldine** valiku **Otsingu lubamine** väärtusele **Jah**.  

Müügitellimuse rea sisestuse puhul on vaikekäitumine lehe **Tooteotsing** avamine, kui alustate väljale **Kaubakood** sisestamist ja seejärel vajutate klahvi **Tab**. Leht **Tooteotsing** muudab tellimuse rea loomise käigus konteksti ja võidakse arvata ebavajalikult pealetükkivaks. Kui eelistate saada otsingutulemused otsingus ja mitte kaotada konteksti tellimuse rea sisestuse käigus, saate selle asemel kasutada otsingut. Kui otsite toodet või tootevarianti, kuid te ei vali midagi otsingus ja vajutate klahvi **Tab**, kuvatakse leht **Tooteotsing**.




