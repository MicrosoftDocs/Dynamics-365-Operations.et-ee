---
title: Hankija arvete ülevaade
description: Selles teemas antakse üldteavet hankija arvete kohta. Hankija arved on maksetaotlused saadud toodete ja teenuste eest. Hankija arved võivad esindada kehtivate teenuste arvet või need võivad põhineda kindlate kaupade ja teenuste ostutellimustel.
author: abruer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b57c18b5b2cf690111511e4c5a92d51fc23dd68c
ms.sourcegitcommit: 901ec3b360303bb8b4d9a9dcfecc6d75d7f844a0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/05/2019
ms.locfileid: "1618269"
---
# <a name="vendor-invoices-overview"></a>Hankija arvete ülevaade

[!include [banner](../includes/banner.md)]


Selles teemas antakse üldteavet hankija arvete kohta. Hankija arved on maksetaotlused saadud toodete ja teenuste eest. Hankija arved võivad esindada kehtivate teenuste arvet või need võivad põhineda kindlate kaupade ja teenuste ostutellimustel.

## <a name="vendor-invoices"></a>Hankijaarved

Ostutellimuse hankija arve on arve, mis koostatakse toodete või teenuste vastuvõtmisel hankijale esitatud ostutellimuse põhjal. Hankijaarve sisaldab päist ning kaupade ja teenuste jaoks vähemalt üht rida. Hankijaarve viib lõpule tsükli ostutellimusest toote sissetulekuni ja omakorda hankijaarveni.

Kuigi mõned hankija arved on seotud ostutellimusega, võivad hankija arved sisaldada ka ridu, mis ei vasta ostutellimuse ridadele. Saate luua ka hankija arveid, mis ei ole seotud ühegi ostutellimusega. Need hankija arved võivad kajastada pidevaid teenuseid (nt kommunaalteenuste arve) ja nende lisamisel pole vaja ostutellimusele viidata.

On mitmeid viise hankija arve sisestamiseks.

- Hankijaarve register võimaldab teil kiiresti sisestada ostutellimusele mitteviitavaid arveid, et saaksite kulusid koondada. Hankijaarve kinnitamise töölehe kasutamisel saate need arved valida ja sisestada need juurdekasvu tühistamiseks hankijasaldosse.
- Hankija arve töölehe abil saate sisestada kiiresti (ühe toiminguga) arveid, mis ei viita ostutellimusele.
- Koos hankija arvete kaustaga võimaldab hankija arvete register kulude koondamiseks kiiresti arveid sisestada. Hiljem saate avada seotud ostutellimused arve sisestamiseks kulukonto suhtes.
- Lehed **Avatud hankija arved** ja **Ootel hankija arved** võimaldavad luua hankija arveid kinnitatud ostutellimustest.

Järgmises arutelus on lisateave lehtede **Avatud hankija arved** või **Ootel hankija arved** kasutamise kohta hankija arve loomiseks ostutellimusest.

## <a name="understanding-invoice-line-quantities"></a>Arve rea koguste teave

Kui avate hankija arve seotud ostutellimusest, luuakse ostutellimusest arve read. Vaikimisi võetakse kogused toote sissetuleku koguselt. Kuid saate kasutada ka ühte järgmistest vaikekäitumistest.

- **Kohe tarnitav kogus** – kasutage seda valikut osaliste tarnete puhul. Välja **Kogus** vaikeväärtus on võetud koguselt, mis on määratud ostutellimuse väljal **Kohe tarnitav**.
- **Tellitud kogus** – kasutage seda valikut terviksaadetiste puhul. Välja **Kogus** vaikeväärtus on võetud koguselt, mis on määratud ostutellimuse väljal **Tellitud**.
- **Registreeritud kogus** – kasutage seda valikut, kui kaup nõuab registreerimist, nagu on määratud lehel **Kauba mudeligrupid**. Vaikeväärtus väljal **Kogus** on füüsiline uuendamiskogus, mis on registreeritud.
- **Toote sissetuleku kogus** – kasutage seda valikut, kui toote sissetulek on tellimuse puhul juba saabunud. Vaikeväärtus väljal **Kogus** on pärit saadaolevate toote sissetulekute täielikust kogusest.
- **Registreeritud kogus ja teenused** – kasutage seda valikut, kui ladustatavate kaupade saabumistöölehtedel või mitteladustatavate kaupade puhul on registreeritud kogused. See võimalus hõlmab ka teenuseid, olenemata sellest, kas need on registreeritud.

Kui teie juriidiline isik kasutab arvete võrdlemist, saate vaadata koguse võrdlemise tulemusi veerus **Toote sissetuleku koguse vastavusseviimine**. Saate kasutada koguse vastavusseviimise tulemuste vaatamiseks ka nuppu **Vastavusseviimise üksikasjad**, mis asub toimingupaani vahekaardil **Ülevaatus**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Ostutellimuselt puudunud rea lisamine

Saate hankija arvele lisada ostutellimuses puuduva rea. Peate valima kaubakoodi või hankekategooria. Seejärel saate lisada reale koguseid, hindu ja summasid. Rida kaasatakse ainult arve koondsummade vastavusseviimise põhimõtetesse.

## <a name="submitting-a-vendor-invoice-for-review"></a>Hankija arve esitamine läbivaatuseks

Teie organisatsioon võib kasutada töövoogusid, et hallata hankijaarvete läbivaatamise protsessi. Töövoo läbivaatamine võib olla vajalik ostuarve päise, arverea või mõlema jaoks. Töövoo juhtelemendid rakenduvad päisele või reale olenevalt sellest, mis on juhtelemendi valimise ajal aktiivne. Nupu **Sisesta** asemel näete nuppu **Edasta**, mida saate kasutada hankija arve läbivaatamisprotsessi saatmiseks.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Hankijaarvete vastavusseviimine toote sissetulekutega

Saate sisestada ja salvestada hankijaarvete teavet ning vastendada arveread tootesissetuleku ridadega. Saate ka rea osalisi koguseid vastavusse viia.

Võite luua hankija arve, mis põhineb toote sissetuleku rea kaupadel, mis on vastu võetud praeguse kuupäevani, isegi kui konkreetse ostutellimuse kõik kaubad pole veel vastu võetud. Võite kasutada seda võimalust näiteks siis, kui hankija saadab ühe arve kuus, mis katab kõik saadetised, mis ta selle kuu jooksul lähetas. Iga toote sissetulek tähistab osalist väi täielikku ostutellimusel oleva kauba tarnet.

Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** vastuvõetud kogustega valitud toote sissetulekutelt. Kui kõigi ostutellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse ostutellimuse olekuks **Arveldatud**. Kui kogus **Arve jääk** ei ole 0, siis ostutellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid.

See valik eeldab, et ostutellimuse kohta on sisestatud vähemalt üks toote sissetulek. Hankija arve aluseks on need toote sissetulekud ja arve näitab saatelehtedelt pärit koguseid. Finantsteave arve jaoks põhineb teabel, mis sisestatakse, kui sisestate arve.

Lisainfot vt teemast [Hankija arve kirjendamine ja sissetulnud kogusega vastendamine](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="working-with-multiple-invoices"></a>Mitme arvega töötamine

Saate töötada mitme arvega samal ajal ja pärast need kõik korraga sisestada. Kui teil on vaja luua mitu arvet, kasutage lehte **Ootel hankija arved**. Kui peate sisestama ja printima mitu hankija arvet, kasutage arve kinnitamise töölehte. Kui kasutate arve kinnitamise töölehte, tuleb ostutellimusele sisestada vähemalt üks toote sissetulek ja ostutellimuse arve tuleb sisestada arveregistrisse. Arve finantsiline teave tuleb arvelt, mis sisestati registrisse.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Kasutuses olevate hankija arvete taastamine

Kui hankija arve on kasutuses, ei saa teine kasutaja seda muuta. Siiski võib arve olek vahel näidata, et arvet kasutatakse, isegi kui seda aktiivselt ei muudeta. Näiteks võib rakendus olla peatunud arve muutmise ajal, või kasutaja võis arve kogemata rakenduses lahti jätta.

Saate kasutada lehte **Taasta hankija arved**, et taastada või väljastada hankija arveid, mis on olnud kasutuses rohkem kui neli tundi, nii et neid saaks muuta. Saate avada selle lehe **Perioodiline ülesanne** alt või paani tööruumis **Hankija arved**. Kui arve on taastatud, on see lehel **Hankija arve** muutmiseks saadaval.

Saate lehele **Hankija arvete taastamine** juurdepääsu ainult siis, kui teile on määratud **Kasutuses olevate hankija arvete taastamise** kohustus ja õigus. Lisaks peab parameeter **Luba hankija arvete taastamine** lehel **Ostureskontro parameetrid** olema sisse lülitatud.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Hankija arvete töövoo oleku lähtestamine olekult Parandamatu olekule Mustand

Taastamatu tõrke tõttu peatatud töövoo eksemplaril on töövoo olekuks **Parandamatu**. Kui hankija arve töövoo olek on **Parandamatu**, saate selle lähtestada olekule **Mustand**. Seejärel saate hankija arvet redigeerida. See funktsioon on saadaval, kui lehel **Funktsioonihaldus** on parameeter **Hankija arve töövoo mustandi olekule lähtestamine** sisse lülitatud.

Saate kasutada lehte **Hankija arvete töövoo oleku lähtestamine**, et lähtestada töövoogu olekule **Mustand**. Selle lehe saate avada navigeerimisüksuselt **Perioodiline ülesanne**. Lehel kuvatakse kõik hankija arved, mille töövoo olek on praeguses juriidilises isikus **Parandamatu**. Samuti näitab see kasutajat, kes iga arve töövoogu esitas, ja arve identifikaatorit ning esitab lingi töövoo ajaloole. Selleks, et lähtestada töövoog olekule **Mustand**, märkige üks või mitu arvet ja valige seejärel käsk **Värskenda mustandiks**. Pärast töövoo olekule **Mustand** lähtestamist muutub see lehel **Hankija arve** redigeerimise jaoks kättesaadavaks.

Lehele **Hankija arvete töövoo oleku lähtestamine** saate juurde pääseda ainult juhul, kui turbekohustus **Säilita hankija arve töövoo olekut** ja privileeg **Hankija arve töövoo oleku lähtestamine** on teile määratud.

## <a name="additional-resources"></a>Lisaressursid

- [Hankija arve poliitikate seadistamine](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Arve põhiandmed ostureskontrosse hankija arve abil](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Arve põhiandmed ostureskontrosse kinnitamise töölehe abil](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Arve põhiandmed ostureskontro süsteemi arvete kausta abil](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Hankija arve kirjendamine arvete töölehele](tasks/record-vendor-invoice-invoice-journal.md)
