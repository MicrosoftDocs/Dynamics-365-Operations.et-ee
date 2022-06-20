---
title: Hankijaarvete ülevaade
description: Selles artiklis antakse üldteavet hankija arvete kohta.
author: abruer
ms.date: 02/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b88390085d86956c38c0fc167395509d0c54f860
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894167"
---
# <a name="vendor-invoices-overview"></a>Hankija arvete ülevaade

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Selles artiklis antakse üldteavet hankija arvete kohta. Hankija arved on maksetaotlused saadud toodete ja teenuste eest. Hankija arved võivad esindada kehtivate teenuste arvet või need võivad põhineda kindlate kaupade ja teenuste ostutellimustel.

## <a name="vendor-invoices"></a>Hankijaarved

Ostutellimuse hankija arve koostatakse toodete või teenuste vastuvõtmisel hankijale esitatud ostutellimuse põhjal. Hankijaarve sisaldab päist ning kaupade ja teenuste jaoks vähemalt üht rida. Hankijaarve viib lõpule tsükli ostutellimusest toote sissetulekuni ja omakorda hankijaarveni.

Kuigi mõned hankija arved on seotud ostutellimusega, võivad hankija arved sisaldada ka ridu, mis ei vasta ostutellimuse ridadele. Saate luua ka hankija arveid, mis ei ole seotud ühegi ostutellimusega. Need hankijaarved võivad esindada jooksvaid teenuseid, nt kommunaalarveid. Jooksva teenuse lisamisel ei pea te ostutellimusele viitama.

On mitmeid viise hankija arve sisestamiseks.

- Hankijaarve register võimaldab teil kiiresti sisestada ostutellimusele mitteviitavaid arveid, et saaksite kulusid koondada. Hankijaarve kinnitamise töölehe kasutamisel saate need arved valida ja sisestada need juurdekasvu tühistamiseks hankijasaldosse.
- Hankija arve töölehe abil saate sisestada kiiresti (ühe toiminguga) arveid, mis ei viita ostutellimusele.
- Koos hankija arvete kaustaga võimaldab hankija arvete register kulude koondamiseks kiiresti arveid sisestada. Hiljem saate avada seotud ostutellimused arve sisestamiseks kulukonto suhtes.
- Lehed **Avatud hankija arved** ja **Ootel hankija arved** võimaldavad luua hankija arveid kinnitatud ostutellimustest.

Järgmises arutelus on lisateave lehtede **Avatud hankija arved** või **Ootel hankija arved** kasutamise kohta hankija arve loomiseks ostutellimusest.

## <a name="understanding-invoice-line-quantities"></a>Arve rea koguste teave

Kui avate hankija arve seotud ostutellimusest, loob süsteem ostutellimusest arve read. Vaikimisi võtab süsteem kogused toote sissetuleku koguselt. Kuid saate kasutada ka ühte järgmistest vaikekäitumistest.

- **Kohe tarnitav kogus** – kasutage seda valikut osaliste tarnete puhul. Vaikeväärtus väljal Kogus **seatakse** ostutellimuse väljal **Tarni kohe** määratud kogusele.
- **Tellitud kogus** – kasutage seda valikut terviksaadetiste puhul. Vaikeväärtus väljal Kogus **seatakse** ostutellimuse väljal **Tellitud** määratud kogusele.
- **Registreeritud kogus** – kasutage seda valikut, kui kaup nõuab registreerimist, nagu on määratud lehel **Kauba mudeligrupid**. Vaikeväärtus väljal **Kogus** on füüsiline uuendamiskogus, mis on registreeritud.
- **Toote sissetuleku kogus** – kasutage seda valikut, kui toote sissetulek on tellimuse puhul juba saabunud. Vaikeväärtus väljal Kogus **on** saada tavate toote sissetulekute kogusumma.
- **Registreeritud kogus ja teenused** – kasutage seda valikut, kui ladustatavate kaupade saabumistöölehtedel või mitteladustatavate kaupade puhul on registreeritud kogused. See võimalus hõlmab ka teenuseid, olenemata sellest, kas need on registreeritud.

Kui teie juriidiline isik kasutab arvete võrdlemist, saate vaadata koguse võrdlemise tulemusi veerus **Toote sissetuleku koguse vastavusseviimine**. Saate kasutada koguse vastavusseviimise tulemuste vaatamiseks ka nuppu **Vastavusseviimise üksikasjad**, mis asub toimingupaani vahekaardil **Ülevaatus**.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Ostutellimuselt puudunud rea lisamine

Saate hankija arvele lisada ostutellimuses puuduva rea. Peate valima kaubakoodi või hankekategooria. Seejärel saate lisada reale koguseid, hindu ja summasid. Rida kaasatakse ainult arve koondsummade vastavusseviimise põhimõtetesse.

## <a name="submitting-a-vendor-invoice-for-review"></a>Hankija arve esitamine läbivaatuseks

Teie organisatsioon võib kasutada töövoogusid, et hallata hankijaarvete läbivaatamise protsessi. Töövoo läbivaatamine võib olla vajalik ostuarve päise, arverea või mõlema jaoks. Töövoo juhtelemendid rakenduvad päisele või reale olenevalt sellest, mis on juhtelemendi valimise ajal aktiivne. Nupu Sisesta **asemel** saadetakse nupp **Edasta** hankija arve ülevaatusprotsessi kaudu.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>Arve töövoogu edastamise takistamine 

Järgnevalt on loetletud miteid viise, kuidas saate takistada arve esitamist töövoogu.

- **Arve kogusumma ja registreeritud kogusumma ei ole võrdsed.** Arve esitanud isikule saadetakse teatis selle kohta, et kogusummad ei ole võrdsed. Teatis annab võimaluse parandada saldosid enne arve uuesti töövoogu saatmist. See funktsioon on saadaval, kui lehel **Funktsioonihaldus** on parameeter **Keela töövoogu esitamine, kui arve kogusumma ja arve registreeritud kogusumma ei ole võrdsed** sisse lülitatud. 
- **Arve sisaldab eraldamata kulusid.** Arve esitanud isik saab teate, et arve sisaldab eraldamata kuludes, võimaldades tal arvet enne töövoogu uuesti esitamist parandada. See funktsioon on saadaval, kui lehel **Funktsioonihaldus** on parameeter **Keela töövoogu esitamine, kui hankija arvel on eraldamata kulusid** sisse lülitatud.
- **Arvel on sama arvenumber teise sisestatud arvega.** Arve edastanud isikule saadetakse teade, mis näitab, et leiti duplikaatnumbriga arve. Duplikaatnumbrit saab parandada enne arve uuesti töövoole edastamist. See teatis kuvatakse siis, kui ostureskontro parameetriks **Kontrolli kasutatavat arvenumbrit** on määratud **Lükka duplikaat tagasi**. See funktsioon on saadaval, kui lehel **Funktsioonihaldus** on parameeter **Keela töövoogu esitamine, kui sisestatud arvel on selline number juba olemas ja süsteemis ei ole lubatud topeltnumbriga arvete vastuvõtmine** on sisse lülitatud.
- **Arve sisaldab rida, kus arve kogus on väiksem kui vastendatud toote sissetuleku kogus.** Isik, kes arve esitab või proovib postitada, saab teate, et kogused ei ole võrdsed. Teatis annab võimaluse parandada saldosid enne arve uuesti töövoogu saatmist. See funktsioon on saadaval juhul, kui **Hankija arvete sisestamise blokeerimise** parameeter on **Funktsioonide haldus** lehel ja parameetri **Ostureskontro blokeerimine ja töövoole esitamine** lehel **Konto maksu parameetrid** sisse lülitatud.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Hankijaarvete vastavusseviimine toote sissetulekutega

Saate sisestada ja salvestada hankijaarvete teavet ning vastendada arveread tootesissetuleku ridadega. Saate ka rea osalisi koguseid vastavusse viia.

Võite luua hankija arve, mis põhineb toote sissetuleku rea kaupadel, mis on vastu võetud praeguse kuupäevani, isegi kui konkreetse ostutellimuse kõik kaubad pole veel vastu võetud. Võite kasutada seda võimalust näiteks siis, kui hankija saadab ühe arve kuus, mis katab kõik saadetised, mis ta selle kuu jooksul lähetas. Iga toote sissetulek tähistab osalist väi täielikku ostutellimusel oleva kauba tarnet.

Kui arve on töövoos, saab kinnitaja uuendada arve koguseid nii, et need ühtiksid väärtusega väljal **Toote vastuvõtukogus vastendamiseks**. Selleks valige funktsioon **Värskenda arve koguseid vastavalt toote vastuvõtu kogustele töövoos** tööruumis **Funktsioonihaldus** ja valige **Luga**. Kui töövoo protsessi kinnitaja on eemaldanud arve realt kõik toote sissetulekud, kustutatakse arve rida. Kui see funktsioon pole lubatud, siis arve koguseid töövoos arvete jaoks ei uuendata.

Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** vastuvõetud kogustega valitud toote sissetulekutelt. Kui kõigi ostutellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse ostutellimuse olekuks **Arveldatud**. Kui kogus **Arve jääk** ei ole 0, siis ostutellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid.

See valik eeldab, et ostutellimuse kohta on sisestatud vähemalt üks toote sissetulek. Hankija arve aluseks on need toote sissetulekud ja arve näitab saatelehtedelt pärit koguseid. Finantsteave arve jaoks põhineb teabel, mis sisestatakse, kui sisestate arve.

Lisainfot vt teemast [Hankija arve kirjendamine ja sissetulnud kogusega vastendamine](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md)

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>Hankija arve töövoole automatiseeritud ülesande konfigureerimine pakett-töö abil hankija arve sisestamiseks

Saate hankija arve töövoogu lisada automaatse sisestamise ülesande, nii et arveid töödeldakse partiis. Arvete sisestamine partiis võimaldab töövoo protsessi jätkata ilma, et peaksite ootama sisestuse lõpetamist, mis parandab kõigi ülesannete töövoogu esitamise üldist jõudlust.

Hankija arve sisestamiseks partiis lülitage lehel **Funktsioonihaldus** sisse parameeter **Hankija arvesisestamine partiis**. Hankija arve töövoogusid saate konfigureerida jaotises **Ostureskontro > Häälestus > Ostureskontro töövood**.

Saate vaadata ülesannet **Sisesta hankija arve partiis** töövoo redaktoris, sõltumata sellest, kas funktsiooni parameeter **Hankija arve sisestamine partiis** on lubatud. Kui funktsiooni parameeter pole lubatud, siis arvet, mis sisaldab parameetrit **Sisesta hankija arve partiiülesande abil**, ei töödelda töövoos enne, kuni parameeter on lubatud. Ülesannet **Sisesta hankija arve partii abil** ei tohi kasutada samas töövoos automatiseeritud ülesandega **Hankija arvete sisestamine**. Samuti peaks ülesanne **Sisesta hankija arve partii abil** olema töövoo konfiguratsiooni viimane element.

Saate määratleda partiisse kaasatavate arvete arvu ja partii ümberplaneerimise ooteaja tundides, kui avate jaotise **Ostureskontro > Häälestus > Ostureskontro parameetrid > Arve > Arve töövoogu**. 

## <a name="working-with-multiple-invoices"></a>Mitme arvega töötamine

Saate töötada mitme arvega samal ajal ja pärast need kõik korraga sisestada. Kui soovite luua mitu arvet, kasutage lehte **Ootel hankija arved**. Kui peate sisestama ja printima mitu hankijaarvet, kasutage arve **kinnitamise töölehte**. Kui kasutate arve **kinnitamise** töölehte, peab ostutellimuse jaoks olema sisestatud vähemalt üks toote sissetulek ja ostutellimuse arve tuleb sisestada arveregistrisse. Arve finantsiline teave tuleb arvelt, mis sisestati registrisse.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Kasutuses olevate hankija arvete taastamine

Kui hankija arve on kasutuses, ei saa teine kasutaja seda muuta. Siiski võib arve olek vahel näidata, et arvet kasutatakse, isegi kui seda aktiivselt ei muudeta. Näiteks võib rakendus olla peatunud arve muutmise ajal, või kasutaja võis arve kogemata rakenduses lahti jätta.

Saate kasutada lehte **Taasta hankija arved**, et taastada või väljastada hankija arveid, mis on olnud kasutuses rohkem kui neli tundi, nii et neid saaks muuta. Saate avada selle lehe **Perioodiline ülesanne** alt või paani tööruumis **Hankija arved**. Kui arve on taastatud, on see lehel **Hankija arve** muutmiseks saadaval.

Saate lehele **Hankija arvete taastamine** juurdepääsu ainult siis, kui teile on määratud **Kasutuses olevate hankija arvete taastamise** kohustus ja õigus. Lisaks peab parameeter **Luba hankija arvete taastamine** lehel **Ostureskontro parameetrid** olema sisse lülitatud.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Hankija arvete töövoo oleku lähtestamine olekult Parandamatu olekule Mustand

Taastamatu tõrke tõttu peatatud töövoo eksemplaril on töövoo olekuks **Parandamatu**. Kui hankija arve töövoo olek on **Taastamatu**, saate lähtestada selle olekusse **Mustand**, valides suvandi **Tagasikutsumine**. Seejärel saate hankija arvet redigeerida. See funktsioon on saadaval, kui parameeter **Hankija arvete töövoo oleku lähtestamine olekult Parandamatu olekule Mustand** lehel **Funktsioonihaldus** on sisse lülitatud.

Saate kasutada lehte **Töövoo ajalugu**, et lähtestada töövoo olekuks **Mustand**. Saate avada selle lehe jaotisest **Hankija arve** või navigeerides **Üldine > Päringud > Töövoog**. Töövoo oleku lähtestamiseks olekusse **Mustand**, valige **Tagasikutsumine**. Võite lähtestada töövoo oleku mustandiks ka valides tegevuse **Tagasikutsumine** lehel **Hankija arve** või **Ootel hankija arved**. Pärast töövoo olekule **Mustand** lähtestamist muutub see lehel **Hankija arve** redigeerimise jaoks kättesaadavaks.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>Arve kogusumma kuvamine lehel Ootel hankija arved

Saate vaadata arve kogusummat lehel **Ootel hankija arved**, lubades parameetri **Kuva arve kogusumma ootel hankija arvete loendis** lehel **Ostureskontro parameetrid**. 

## <a name="vendor-open-transactions-report"></a>Hankija avatud kannete aruanne

Aruanne **Tarnija avatud tehingud** annab üksikasjalikku teavet iga hankija avatud tehingute kohta teie määratud kuupäeva seisuga. Seda aruannet kasutatakse sageli auditiprotseduuri ajal hankijaraamatu tehingute ja pearaamatukonto tehingute vaheliste saldode kontrollimiseks.

Iga tehingu kohta sisaldab aruanne järgmisi üksikasju:

- Arve number
- Kande kuupäev
- Kande number
- Tehingu summa tehingu- ja arvestusvaluutas
- Krediidijääk tehingu- ja arvestusvaluutas
- Deebetjääk tehingu- ja arvestusvaluutas
- Kogusumma arvestusvaluutas
- Makse tähtaeg

### <a name="filter-the-data-on-the-report"></a>Aruande andmete filtreerimine

Kui loote aruande **Tarnija avatud tehingud**, on saadaval järgmised vaikeparameetrid. Saate neid kasutada aruandesse lisatavate andmete filtreerimiseks.

- **Välista tulevane arveldus** – märkige see ruut, et välistada tehingud, mis arveldatakse pärast väljale **Ava tehingud kuupäevast** sisestatud kuupäeva.
- **Avatud tehingud kuupäevast** – sisestage kuupäev, et kaasata tehingud, mis on sellel kuupäeval avatud. Kui te kuupäeva ei sisesta, määratakse sellele väljale maksimaalne kuupäev. (Maksimaalne kuupäev on viimane kuupäev, mille süsteem aktsepteerib, 31. detsember 2154.) Vaikimisi määratakse järgmisel aruande käivitamisel sellele väljale viimane sellele sisestatud kuupäev.

Aruandes sisalduvate tehinguandmete piiramiseks saate kasutada välja **Kaasamiseks kirje** all olevaid filtreid.

## <a name="additional-resources"></a>Lisaressursid

- [Saate häälestada hankija arve poliitikaid.](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Arve põhiandmed AP-süsteemis, kasutades hankija arvet](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Arve põhiandmed ostureskontrosse kinnitamise töölehe abil](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Arve põhiandmed ostureskontro süsteemi arvete kausta abil](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Hankija arve kirjendamine arvete töölehele](tasks/record-vendor-invoice-invoice-journal.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
