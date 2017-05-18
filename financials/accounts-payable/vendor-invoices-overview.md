---
title: "Hankijaarvete ülevaade"
description: "Selles artiklis antakse üldteavet hankija arvete kohta. Hankija arved on maksetaotlused saadud toodete ja teenuste eest. Hankija arved võivad esindada kehtivate teenuste arvet või need võivad põhineda kindlate kaupade ja teenuste ostutellimustel."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a6b18343337ca7058c5027c8d4325c4301f1abed
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-invoices-overview"></a>Hankijaarvete ülevaade

[!include[banner](../includes/banner.md)]


Selles artiklis antakse üldteavet hankija arvete kohta. Hankija arved on maksetaotlused saadud toodete ja teenuste eest. Hankija arved võivad esindada kehtivate teenuste arvet või need võivad põhineda kindlate kaupade ja teenuste ostutellimustel. 

<a name="vendor-invoices"></a>Hankijaarved
---------------

Ostutellimuse hankija arve on arve, mis koostatakse toodete või teenuste vastuvõtmisel hankijale esitatud ostutellimuse põhjal. Hankijaarve sisaldab päist ning kaupade ja teenuste jaoks vähemalt üht rida. Hankijaarve viib lõpule tsükli ostutellimusest toote sissetulekuni ja omakorda hankijaarveni. 

Kuigi mõned hankija arved on seotud ostutellimusega, võivad hankija arved sisaldada ka ridu, mis ei vasta ostutellimuse ridadele. Saate luua ka hankija arveid, mis ei ole seotud ühegi ostutellimusega. Need hankija arved võivad kajastada pidevaid teenuseid (nt kommunaalteenuste arve) ja nende lisamisel pole vaja ostutellimusele viidata. 

On mitmeid viise hankija arve sisestamiseks.

-   Hankijaarve register võimaldab teil kiiresti sisestada ostutellimusele mitteviitavaid arveid, et saaksite kulusid koondada. Hankijaarve kinnitamise töölehe kasutamisel saate need arved valida ja sisestada need juurdekasvu tühistamiseks hankijasaldosse.
-   Hankija arve töölehe abil saate sisestada kiiresti (ühe toiminguga) arveid, mis ei viita ostutellimusele.
-   Koos hankija arvete kaustaga võimaldab hankija arvete register kulude koondamiseks kiiresti arveid sisestada. Hiljem saate avada seotud ostutellimused arve sisestamiseks kulukonto suhtes.
-   Lehed **Avatud hankija arved** ja **Ootel hankija arved** võimaldavad luua hankija arveid kinnitatud ostutellimustest.

Järgmises arutelus on lisateave lehtede **Avatud hankija arved** või **Ootel hankija arved** kasutamise kohta hankija arve loomiseks ostutellimusest.

## <a name="understanding-invoice-line-quantities"></a>Arve rea koguste teave
Kui avate hankija arve seotud ostutellimusest, luuakse ostutellimusest arve read. Vaikimisi võetakse kogused toote sissetuleku koguselt. Kuid saate kasutada ka ühte järgmistest vaikekäitumistest.

-   **Kohe tarnitav kogus** – kasutage seda valikut osaliste tarnete puhul. Välja **Kogus** vaikeväärtus pärineb ostutellimuse koguseväljalt **Kohe tarnitav**.
-   **Tellitud kogus** – kasutage seda valikut terviksaadetiste puhul. Välja **Kogus** vaikeväärtus pärineb ostutellimuse koguseväljalt **Tellitud**.
-   **Registreeritud kogus** – kasutage seda valikut, kui kaup nõuab registreerimist, nagu on määratud lehel **Kauba mudeligrupid**. Vaikeväärtus väljal **Kogus** on füüsiline uuendamiskogus, mis on registreeritud.
-   **Toote sissetuleku kogus** – kasutage seda valikut, kui toote sissetulek on tellimuse puhul juba saabunud. Vaikeväärtus väljal **Kogus** on pärit saadaolevate toote sissetulekute täielikust kogusest.
-   **Registreeritud kogus ja teenused** – kasutage seda valikut, kui ladustatavate kaupade saabumistöölehtedel või mitteladustatavate kaupade puhul on registreeritud kogused. See võimalus hõlmab ka teenuseid, olenemata sellest, kas need on registreeritud.

Kui teie juriidiline isik kasutab arvete võrdlemist, saate vaadata koguse võrdlemise tulemusi veerus **Toote sissetuleku koguse vastavusseviimine**. Saate kasutada koguse vastavusseviimise tulemuste vaatamiseks ka menüükäsku **Vastavusseviimise üksikasjad** vahekaardil **Ülevaatus**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Ostutellimuselt puudunud rea lisamine
Saate hankijaarvele lisada uue ostutellimuses puuduva rea. Peate valima kaubakoodi või hankekategooria. Seejärel saate lisada reale koguseid, hindu ja summasid. Rida kaasatakse ainult arve koondsummade vastavusseviimise põhimõtetesse.

## <a name="submitting-a-vendor-invoice-for-review"></a>Hankija arve esitamine läbivaatuseks
Teie organisatsioon võib kasutada töövoogusid, et hallata hankijaarvete läbivaatamise protsessi. Töövoo läbivaatamine võib olla vajalik ostuarve päise, arverea või mõlema jaoks. Töövoo juhtelemendid rakenduvad päisele või reale, sõltuvalt sellest, mis on juhtelemendi klõpsamise ajal aktiivne. Nupu **Sisesta** asemel näete nuppu **Edasta**, mida saate kasutada hankija arve läbivaatamisprotsessi saatmiseks.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Hankijaarvete vastavusseviimine toote sissetulekutega
Saate sisestada ja salvestada hankijaarvete teavet ning vastendada arveread tootesissetuleku ridadega. Saate ka rea osalisi koguseid vastavusse viia. 

Võite luua hankija arve, mis põhineb toote sissetuleku rea kaupadel, mis on vastu võetud õigel ajal, isegi kui konkreetse ostutellimuse kõik kaubad pole veel vastu võetud. Võite kasutada seda võimalust näiteks siis, kui hankija saadab ühe arve kuus, mis katab kõik saadetised, mis ta selle kuu jooksul lähetab. Iga toote sissetulek tähistab osalist väi täielikku ostutellimusel oleva kauba tarnet. 

Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** vastuvõetud kogustega valitud toote sissetulekutelt. Kui kõigi ostutellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse ostutellimuse olekuks **Arveldatud**. Kui kogus **Arve jääk** ei ole 0, siis ostutellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid.

See valik eeldab, et ostutellimuse kohta on sisestatud vähemalt üks toote sissetulek. Hankija arve aluseks on need toote sissetulekud ja arve näitab saatelehtedelt pärit koguseid. Finantsteave arve jaoks põhineb teabel, mis sisestatakse, kui sisestate arve.

## <a name="working-with-multiple-invoices"></a>Mitme arvega töötamine

Saate töötada mitme arvega samal ajal ja pärast need kõik korraga sisestada. Kui teil on vaja luua mitu arvet, kasutage lehte **Ootel hankija arved**. Kui peate sisestama ja printima mitu hankija arvet, kasutage arve kinnitamise töölehte. Kui kasutate arve kinnitamise töölehte, tuleb ostutellimusele sisestada vähemalt üks toote sissetulek ja ostutellimuse arve tuleb sisestada arveregistrisse. Arve finantsteave tuleb arvelt, mis sisestati registrisse.





