---
title: Paindliku laotaseme dimensiooni reserveerimise poliitika
description: See teema kirjeldab varude reserveerimise poliitikat, mis võimaldab partiijälgimisega tooteid müüvatel ettevõtetel käitada nende logistikat, nagu WMS-i toega toimingud, kindlatel partiidel kliendi müügitellimuste jaoks. Seda ka siis, kui tootega seostatud reserveerimise hierarhia ei luba kindlaid partiisid reserveerida.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 65304216b579b8def493d1e4218174cb9617013d
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652175"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Paindliku laotaseme dimensiooni reserveerimise poliitika

[!include [banner](../includes/banner.md)]

Kui varude reserveerimise hierarhia tüüp „partii-alla\[asukoha\]” on seotud toodetega, siis ei saa ettevõtted, mis müüvad partiijälgimisega tooteid ja käitavad nende logistikat, mis on lubatud Microsoft Dynamics 365 laohaldusesüsteemi (WMS) jaoks, reserveerida nende toodete kindlaid partiisid kliendi müügitellimustele.

Sarnaselt ei saa kindlaid litsentsiplaate reserveerida müügitellimustes olevate toodete jaoks, kui need tooted on seotud reserveerimise vaikehierarhiaga.

Selles teemas kirjeldatakse varude reserveerimise poliitikat, mis võimaldab nendel ettevõtetel kindlaid partiisid või litsentsiplaate reserveerida isegi siis, kui tooted on seotud reserveerimise hierarhia üksusega „partii-alla\[asukoht\]”.

## <a name="inventory-reservation-hierarchy"></a>Varude reserveerimise hierarhia

See jaotis võtab kokku olemasoleva varude reserveerimise hierarhia.

Varude reserveerimise hierarhia näitab, et laoala dimensioonidega seotud ulatuses on nõudetellimus seotud asukoha kohustuslike dimensioonide, lao ja varude olekuga, samas kui lao loogika vastutab nõutud koguste jaoks asukoha määramise ja selle reserveerimise eest. Teisisõnu, nõudetellimuse ja laotoimingute vahelises suhtluses eeldatakse, et nõudetellimus määrab selle, kust tellimus tuleb saata (st millisest asukohast ja laost). Seejärel toetub ladu laoruumidest nõutava koguse leidmisel oma loogikale.

Kuid selleks, et kajastada äritegevuse mudelit, on jälgimisdimensioonid (partii- ja seerianumbrid) siiski paindlikumad. Varude reserveerimise hierarhia võib hõlmata stsenaariume, mille puhul kehtivad järgmised tingimused.

- Ettevõte tugineb oma laotoimingutele, et hallata partii- või seerianumbritega koguste komplekteerimist pärast seda, kui ladustamisruumis on kogused leitud. Sellele mudelile viidatakse sageli kui *partii-alla\[asukoht\]*. Seda kasutatakse tavaliselt siis, kui toote partii- või seerianumbri ID ei ole klientidele oluline, kuna nad suunavad nõudluse müügiettevõttele.
- Kui partii- või seerianumbrid on osa kliendi tellimuse täpsustusest ja need kirjendatakse nõudetellimusel, on laos olevaid koguseid leidnud toimingud piiratud konkreetsete nõutud numbritega ja neid ei tohi muuta. Sellele mudelile viidatakse sageli kui *partii-üles\[asukoht\]*.

Nende stsenaariumide puhul on probleemiks, et igale väljastatud tootele saab määrata ainult ühe varude reserveerimise hierarhia. Seetõttu ei saa WMS pärast seda, kui hierarhia määramine on määratlenud, millal partii või seerianumber tuleb reserveerida (kas siis, kui nõudetellimus on tehtud, või lao komplekteerimise ajal), jälgitud üksuste käsitsemisel ajastust ad-hoc-alusel muuta.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Partiijälgimisega kaupade paindlik reserveerimine

### <a name="business-scenario"></a>Äristsenaarium

Selle stsenaariumi puhul kasutab ettevõte varude strateegiat, mille puhul lõpetatud kaupu jälgitakse partii numbrite järgi. See ettevõte kasutab ka WMS-i töökogust. Kuna sellel töökogusel on hästivarustatud loogika lao komplekteerimise ja saatmise toimingute planeerimiseks ning käitamiseks partiis lubatud kaupade puhul, on enamik lõpetatud kaupadest seotud „partii-alla\[asukoht\]“ varude reserveerimise hierarhiaga. Seda tüüpi toiminguseadistuse eeliseks on see, et partiide komplekteerimise ja laovaliku otsused (mis on tegelikult reserveerimise otsused) lükatakse edasi, kuni alustatakse lao komplekteerimise toimingutega. Neid ei tehta kliendi tellimuse esitamise ajal.

Kuigi „partii-alla\[asukoht\]” reserveerimise hierarhia teenib ettevõtte ärieesmärke hästi, nõuavad paljud ettevõtte kliendid toodete uuesti tellimisel sama partiid, mida nad varem ostsid. Seetõttu ootavad ettevõtted paindlikkust selle osas, kuidas partii reserveerimise reegleid käsitletakse, nii et olenevalt klientide nõudlusest sama kauba järele võivad ilmneda järgmised käitumismustrid.

- Partii numbrit saab kirjendada ja reserveerida, kui volitatud töötleja on tellimuse vastu võtnud, ja seda ei saa muuta laotoimingute ajal ja/või muude nõudmiste tõttu. Selline käitumine aitab tagada, et tellitud partiinumber saadetakse kliendile.
- Kui partiinumber ei ole kliendile oluline, saab laotoimingute komplekteerimise käigus määrata partiinumbri pärast seda, kui müügitellimuse registreerimine ja reserveerimine on tehtud.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Müügitellimuse kindla partii reserveerimise lubamine

Selleks, et mahutada soovitud paindlikkus partii reserveerimise käitumises kaupadele, mis on seotud „partii-alla\[asukoht\]” varude reserveerimise hierarhiaga, peavad varude haldurid lehel **Varude reserveerimise hierarhiad** valima märkeruudu **Luba reserveerimine nõudetellimusel** valiku **Partiinumber** tasemel.

![Varude reserveerimise hierarhia paindlikuks muutmine](media/Flexible-inventory-reservation-hierarchy.png)

Kui hierarhias valitakse tase **Partiinumber**, valitakse automaatselt kõik seda taset ületavad dimensioonid kuni **Asukoha** tasemeni. (Vaikimisi valitakse tasemest **Asukoht** üle olevad dimensioonid.) Selline käitumine peegeldab loogikat, kus kõik dimensioonid partiinumbri ja asukoha vahel on samuti automaatselt reserveeritud pärast seda, kui reserveerite tellimuse reale kindla partiinumbri.

> [!NOTE]
> Märkeruut **Luba reserveerimine nõudetellimusel** kehtib ainult reserveerimise hierarhia tasemete puhul, mis jäävad lao asukoha dimensioonist allapoole.
>
> **Partiinumber** ja **Litsentsiplaat** on hierarhias ainsad tasemed, mida saab kasutada paindliku reserveerimise poliitikas. Teisisõnu ei saa te valida märkeruutu **Luba reserveerimine nõudetellimusel** taseme **Asukoht** või **Seerianumber** jaoks.
>
> Kui teie reserveerimise hierarhia sisaldab seerianumbri dimensiooni (mis peab alati olema väiksem kui tase **Partiinumber**) ja kui olete pakktöötluse numbrile sisse lülitanud partii-spetsiifilise reserveerimise, jätkab süsteem seerianumbri reserveerimise ja komplekteerimise toiminguid, mis põhinevad reeglitel, mis kehtivad reserveerimise poliitika „Seeria-alla\[asukoht\]” puhul.

Igal ajahetkel saate lubada partii-spetsiifilist reserveerimist olemasolevale „partii-alla\[asukoht\]” reserveerimise hierarhiale teie juurutuses. See muudatus ei mõjuta reserveeringuid ja avatud lao tööd, mis loodi enne muudatuse toimumist. Kuid märkeruutu **Luba reserveerimine nõudetellimusel** ei saa tühjendada, kui **Reserveeritud tellitud**, **Reserveeritud füüsilise** või **Tellitud** probleemi tüübi laokanded on olemas ühe või mitme selle reserveerimise hierarhiaga seotud kauba puhul.

> [!NOTE]
> Kui kauba olemasoleva reserveerimise hierarhia ei luba tellimuse partii täpsustust, saate selle uuesti määrata reserveerimise hierarhiasse, mis lubab partii spetsifikatsioone, tingimusel et hierarhia taseme struktuur on mõlemas hierarhias sama. Kasutage funktsiooni **Muuda reserveerimise hierarhiat kaupadele** ümbermääramiseks. See muudatus võib olla oluline, kui soovite vältida partiis jälitatud kaupade alamhulga paindlikku partii reserveerimist, kuid lubada seda ülejäänud tooteportfellile.

Olenemata sellest, kas olete märkinud ruudu **Luba reserveerimine nõudetellimusel**, kui te ei soovi kindlat partiinumbrit kaubale tellimuse rea jaoks reserveerida, rakendatakse laotoimingute vaikeloogikat, mis kehtib „partii-alla\[asukoht\]” reserveerimise hierarhia puhul.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Kindla partiinumbri reserveerimine kliendi tellimuse jaoks

Pärast seda, kui partii jälgitud kauba „partii-alla\[asukoht\]” varude reserveerimise hierarhia on seadistatud lubama kindla partiinumbrite reserveerimist müügitellimustel, võivad müügitellimuse töötlejad võtta sama kauba kohta kliendi tellimusi ühel järgmistest viisidest, olenevalt kliendi nõudest.

- **Sisestage tellimuse üksikasjad partiinumbrit täpsustamata** – seda lähenemist tuleks kasutada juhul, kui toote partii spetsifikatsioon ei ole kliendile oluline. Kõik olemasolevad protsessid, mis on seotud selle tüübi tellimuse käsitsemisega, jäävad süsteemis muutmata. Kasutajate osas ei nõuta täiendavaid kaalutlusi.
- **Sisestage tellimuse üksikasjad ja reserveerige konkreetne partiinumber** – seda lähenemist tuleks kasutada siis, kui klient nõuab kindlat partiid. Tavaliselt nõuavad kliendid kindlat partiid, kui nad tellivad varem ostetud toodet. Seda tüüpi partii-spetsiifilist reserveerimist nimetatakse *tellimusega kooskõlastatud reserveerimiseks*.

Järgmised reeglid kehtivad koguste töötlemisel ja partiinumber on seotud kindla tellimusega.

- Selleks et lubada kauba kindla partii numbri reserveerimist kauba puhul, mis on märgitud jaotises „partii-alla\[asukoht\]”, peab süsteem reserveerima kõik dimensioonid asukoha kaudu. See vahemik sisaldab tavaliselt litsentsiplaadi dimensiooni.
- Asukoha direktiive ei kasutata, kui komplekteerimise töö on loodud müügirea jaoks, mis kasutab tellimusega seotud partii reserveerimist.
- Tellimusega seotud partiide töö laotöötluse ajal ei tohi ei kasutaja ega süsteem partii numbrit muuta. (See töötlemine hõlmab erandite käsitlemist.)

Järgmises näites kuvatakse täielik töövoog.

## <a name="example-scenario-batch-number-allocation"></a>Näidisstsenaarium: partiinumbri määramine

Selle näite jaoks peavad olema installitud demoandmed ja peate kasutama demoandmete ettevõtet **USMF**.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Varude reserveerimise hierarhia seadistamine partiile konkreetse reserveerimise lubamiseks

1. Avage **Laohaldus** \> **Seadistus** \> **Varud \> Reserveerimine hierarhiasse**.
2. Valige suvand **Uus**.
3. Väljale **Nimi** sisestage nimi (nt **BatchFlex**).
4. Väljale **Kirjeldus** sisestage kirjeldus (nt **Partii alla paindlikkuse**).
5. Väljal **Valitud** valige **Seerianumber** ja **Omanik** ning seejärel klõpsake vasakut nooleklahvi, et teisaldada need väljale **Saadaolev**.
6. Valige nupp **OK**.
7. Märkige dimensioonitaseme real **Partiinumbri** ruut **Luba reserveerimine nõudetellimusel**. Tasemed **Litsentsiplaat** ja **Asukoht** valitakse automaatselt ja nende märkeruute ei saa tühjendada.
8. Valige käsk **Salvesta**.

### <a name="create-a-new-released-product"></a>Uue väljastatud toote loomine

1. Määrake toote kolm koondandmete parameetrit, kasutades neid väärtusi.

    - Valige väljal **Laoala dimensioonigrupp** suvand **Ladu**.
    - Valige väljal  **Jälgimisdimensiooni grupp** suvand **Batch-Phy**.
    - Valige väljal **Reserveeringu hierarhia** suvand **BatchFlex**.

2. Looge kaks partiinumbrit, nt **B11** ja **B22**.
3. Lisage kauba kogused laoseisu, kasutades järgmisi väärtusi.

    | Ladu | Partii number | Koht | Litsentsiplaat | Kogus |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Puudub          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Müügitellimuse üksikasjade sisestamine

1. Avage **Müük ja turundus** \> **Müügitellimused** \> **Kõik müügitellimused**.
2. Valige suvand **Uus**.
3. Müügitellimuse päise väljale **Kliendi konto** sisestage **US-003**.
4. Lisage uue üksuse jaoks rida ja sisestage koguseks **10**. Veenduge, et välja **Ladu** väärtuseks oleks määratud **24**.
5. Kiirkaardil **Müügitellimuse read** valige väärtus **Varud** ja seejärel jaotises **Haldamine** suvand **Partii reserveerimine**. Leht **Partii reserveerimine** näitab tellimuse rea reserveerimiseks saadaolevate partiide loendit. Selles näites näitab see kogust **20** partiinumbri **B11** ja kogust **10** partiinumbri **B22** jaoks. Pange tähele, et lehele **Partii reserveerimine** ei pääse realt juurde, kui sellel real olev üksus on seotud väärtusega „partii-alla\[asukoht\]”, kui see pole seadistatud lubama partiiga seotud reserveerimist.

    > [!NOTE]
    > Kindla partii reserveerimiseks müügitellimusele tuleb kasutada lehte **Partii reserveerimine**.
    >
    > Kui sisestate partii numbri otse müügitellimuse reale, käitub süsteem nii, nagu sisestasite kindla partii väärtuse üksusele, mille suhtes kehtib „partii-alla\[asukoht\]” reserveerimise poliitika. Rea salvestamisel kuvatakse hoiatusteade. Kui kinnitate, et partiinumber tuleb määrata otse tellimuse reale, ei käsitleta rida tavalise laohalduse loogikaga.
    >
    > Kui reserveerite koguse lehelt **Reserveerimine**, ei reserveerita ühtegi kindlat partiid ja selle rea laotegevuse käitamine järgib reegleid, mis on rakendatavad „partii-alla\[asukoht\]” reserveerimise poliitika alusel.

    See lehekülg töötab ja on seotud samal viisil, nagu see toimib ja on seotud üksuste puhul, millel on seostatud reserveerimise hierarhia tüübiga „partii-üle\[asukoha\]”. Siiski kehtivad järgmised erandid.

    - Kiirkaart **Lähtereale määratud partiinumbrid** kuvab tellimuserea jaoks reserveeritud partiinumbrid. Ruudustikus olevad partiiväärtused kuvatakse kogu tellimuserea täitmise tsüklis, sh laotöötluse etappides. Seevastu kiirkaart **Ülevaade**, korrapärase tellimuse rea reserveerimine (s.t reserveerimine, mida tehakse **Asukoha** taseme kohal olevate dimensioonide puhul), kuvatakse ruudustikus kuni laotöö loomiseni. Tööüksus võtab seejärel rea reserveerimise üle ja rea reserveeringut ei kuvata enam leheküljel. Kiirkaart **Lähtereale määratud partiinumbrid** aitab tagada, et müügitellimuse töötleja saab vaadata kliendi tellimusele määratud partiinumbreid mis tahes tööetapis kuni arveldamiseni.
    - Peale konkreetse partii reserveerimise saab kasutaja valida käsitsi partii kindla asukoha ja litsentsiplaadi, selle asemel et lasta süsteemil need automaatselt valida. See võimalus on seotud tellimuse sooritatud partii reserveerimise mehhanismi kujundusega. Nagu varem mainitud, tuleb selleks, et lubada kindla partii numbri reserveerimist üksuse puhul, mis on märgitud jaotises „partii-alla\[asukoht\]”, peab süsteem reserveerima kõik dimensioonid asukoha kaudu. Seetõttu teeb lao töö samu ladustamise dimensioone, mis olid reserveeritud tellimustega töötavate kasutajate poolt, ja see ei pruugi alati kajastada kauba ladustamise paigutust, mis on mugav või isegi võimalik komplekteerimiseks. Kui tellimuse töötlejad on lao piirangutest teadlikud, võivad nad partii reserveerimisel käsitsi valida kindlad asukohad ja litsentsiplaadid. Sellisel juhul peab kasutaja kasutama lehekülje päises funktsiooni **Kuva dimensioonid** ja lisama asukoha ja litsentsiplaadi kiirkaardi **Ülevaade** ruudustikus.

6. Valige lehel **Partii reserveerimine** partii **B11** jaoks rida ja seejärel käsk **Reserveeri rida**. Automaatsel reserveerimisel ei ole asukohtade ja litsentsiplaadi määramiseks loogikat määratud. Koguse saate sisestada käsitsi väljale **Reserveerimine**. Pange tähele, et kiirkaardi **Lähtereale määratud partiinumbrid** partii **B11** kuvatakse kui **Sooritatud**.

    ![Kindla partiinumbri määramine müügitellimuse reale partii reserveerimise lehel](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Müügitellimuse rea koguse reserveerimist saab teha mitmel partiil. Sama partii reserveerimist saab teha ka mitme asukoha ja litsentsiplaadi alusel (kui nende asukohtade puhul on lubatud litsentsiplaadid).
    >
    > Kindla partii reserveerimine müügitellimuse real oleva koguse jaoks võib olla ka osaline. Näiteks 100 ühiku kogukogust saab reserveerida nii, et kindel partii on pühendunud 20 ühikule, samas kui 80 ühikut on reserveeritud saidi ja lao tasemetele mis tahes saadaoleva partii jaoks. Sel juhul kasutab WMS komplekteerimislehe töötlemisel kaht eraldiseisvat töörida.

7. Avage **Tooteteabe haldus** \> **Tooted** \> **Väljastatud tooted**. Valige üksus ja seejärel **Varude haldamine** \> **Kuva** \> **Kanded**.

    ![Tellimusega kooskõlastatud reserveerimine laokande tüübina](media/Inventory-transactions-for-order-committed-reservation.png)

8. Vaadake üle kauba varude kanded, mis on seotud müügitellimuse rea reserveerimisega.

    - Kanne, mille välja **Viide** väärtuseks on seatud **Müügitellimus** ja välja **Väljaminek** väärtuseks on seatud **Reserveeritud füüsiline**, näitab tellimuse rea reserveerimist varude dimensioonide jaoks, mis on üle taseme **Asukoht**. Kauba varude reserveerimise hierarhia kohaselt on need dimensioonid saidi, lao ja varude olek.
    - Kanne, mille välja **Viide** väärtuseks on seatud **Tellimuse tehtud reserveerimine** ja välja **Väljaminek** väärtuseks on seatud **Reserveeritud füüsiline**, näitab tellimuse rea reserveerimist kindlat partiid ja kõiki varude dimensioone üle selle. Kauba varude reserveerimise hierarhia kohaselt on need dimensioonid partiinumber ja asukoht. Selles näites on asukoht **Bulk-001**.

9. Valige müügitellimuse päises suvandid **Ladu** \> **Tegevused** \> **Laost vabastamine**. Tellimuse rida on nüüd moodustatud ja töö on loodud.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Tellitud partiinumbritega laotööde ülevaatamine ja töötlemine

1. Kiirkaardil **Müügitellimuse read** valige **Ladu**\>**Töö üksikasjad**.

    Tööl, mis tegeleb müügitellimuse reale pühendunud partii koguste komplekteerimisega, on järgmised omadused.

    - Töö loomiseks kasutab süsteem töömalle, kuid mitte asukoha direktiive. Kõik töömallide jaoks määratletud kindlad sätted, nt maksimaalne komplekteerimise read või kindel mõõtühik, rakendatakse uute tööde loomisel määramiseks. Siiski ei arvestata reegleid, mis on seotud asukoha direktiividega komplekteerimise asukohtade tuvastamiseks, kuna tellimusega kooskõlastatud reserveeringuga on juba määratud kõik varude dimensioonid. Need varude dimensioonid sisaldavad dimensioone lao ladustamise tasemel. Seetõttu pärib töö need dimensioonid, ilma et peaksite konsulteerima asukoha direktiividega.
    - Partiinumbrit ei kuvata komplekteerimise real (nagu näiteks töörea puhul, mis luuakse kaubale, millel on seostatud „partii-üle\[-asukoht\]” reserveerimise hierarhia). Selle asemel kuvatakse seotud laokannete põhjal viidatud töökandes partiinumber ja kõik muud varude dimensioonid.

        ![Tellimusega kooskõlastatud reserveeringust pärinev lao laokande töö](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Kui töö on loodud, eemaldatakse välja **Viide** väärtusega **Tellimusele kooskõlastatud reserveerimine** kauba laokanne. Laokannete puhul, mille välja **Viide** väärtuseks on seatud **Töö**, on nüüd füüsiline reserveerimine määratud kõigi koguse varude dimensioonide jaoks.

        Laotoimingud võivad jätkata töö töötlemist tavalisel viisil. Kuid mobiilseade juhendab töötajat valima kindlat partiinumbrit. Lao keskkondades, kus asukohti kontrollitakse litsentsiplaadiga pärast seda, kui töötaja jõuab asukohani, mis talletab sama partii mitmele litsentsiplaadile, saab ta valida mis tahes litsentsiplaadi, mis pole veel reserveeritud (nt teine tellimusega kooskõlastatud reserveering või töö, mis pärineb seda tüüpi reserveeringust.)

        Kui tööreal määratud asukohast komplekteerimine osutub ebaotstarbekaks, saavad laooperaatorid kasutada üht järgmistest toimingutest, et suunata kindla partii komplekteerimine mugavamasse asukohta.

        - Mobiilseadme tavatoiming **Asukoha alistamine** (eeldusel, et lao töötaja säte **Luba valitud asukoha alistamine** on lubatud)
        - Toiming **Muuda asukohta** lehel **Tööloendi üksikasjad**. 

2. Lõpetage mobiilseadmes komplekteerimine ja töö sisestamine.

    Kogus **10** on nüüd partiinumbri **B11** jaoks müügireale komplekteeritud ja asukohta **Baydoor** pandud. Sel hetkel on see veokile laadimiseks ja kliendi aadressile lähetamiseks valmis.

## <a name="flexible-license-plate-reservation"></a>Paindlik litsentsiplaadi reserveerimine

### <a name="business-scenario"></a>Äristsenaarium

Selles stsenaariumis kasutab ettevõte laohaldust ja töö töötlemist ning planeerib koormaid üksikute kaubaaluste/konteinerite alusel väljaspool Supply Chain Managementi enne töö loomist. Neid konteinereid esindavad varude dimensioonides litsentsiplaadid. Selleks toiminguks tuleb seetõttu konkreetsed litsentsiplaadid enne komplekteerimistöö lõpetamist määrata müügitellimuse ridadele. Ettevõte soovib, et litsentsiplaadi reserveerimise reeglite käsitsemine oleks paindlik, et juhtuksid järgmised asjad.

- Litsentsiplaati saab kirjendada ja reserveerida, kui volitatud töötleja võtab tellimuse vastu, ning muud nõuded ei saa seda endale võtta. Selline käitumine aitab tagada, et planeeritud litsentsiplaat saadetakse kliendile.
- Kui litsentsiplaat ei ole juba müügitellimuse reale määratud, saab laotöötaja valida litsentsiplaadi komplekteerimise ajal, pärast müügitellimuse registreerimist ja reserveerimist.

### <a name="turn-on-flexible-license-plate-reservation"></a>Paindliku litsentsiplaadi reserveerimise sisselülitamine

Enne paindliku litsentsiplaadi reserveerimise kasutamist peate oma süsteemis sisse lülitama kaks funktsiooni. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsioonide olekut ja need vajadusel sisse lülitada. Peate funktsioonid sisse lülitama järgmises järjekorras.

1. **Funktsiooni nimi:** *Paindlik dimensiooni reserveerimine laotasemel*
1. **Funktsiooni nimi:** *Paindlik tellimusega seotud litsentsiplaadi reserveerimine*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Kindla litsentsiplaadi reserveerimine müügitellimusel

Selleks, et lubada litsentsiplaadi reserveerimine tellimusel, peate valima lehel **Varude reserveerimise hierarhiad** märkeruudu **Luba reserveerimine nõudetellimusel** tasemel **Litsentsiplaat** hierarhia jaoks, mis on seotud asjaomase kaubaga.

![Varude reserveerimise hierarhialeht paindliku litsentsiplaadi reserveerimise hierarhia jaoks](media/Flexible-LP-reservation-hierarchy.png)

Saate lubada litsentsiplaadi reserveerimise tellimusel juurutuse käigus igal ajal. See muudatus ei mõjuta reserveeringuid ega avatud laotöid, mis loodi enne muudatuse toimumist. Kuid te ei saa märkeruutu **Luba reserveerimine nõudetellimusel** tühjendada, kui reserveerimise hierarhiaga seotud ühel või mitmel kaubal on avatud väljaminevate varude kandeid, mille väljamineku olek on *Tellimusel*, *Reserveeritud tellitud* või *Füüsiliselt reserveeritud*.

Isegi kui märkeruut **Luba reserveerimine nõudetellimusel** on tasemel **Litsentsiplaat** valitud, *ei ole* siiski võimalik kindlat litsentsiplaati tellimusel reserveerida. Sel juhul rakendub laotoimingute vaikeloogika, mis kehtib selle reserveerimise hierarhia puhul.

Konkreetse litsentsiplaadi reserveerimiseks peate kasutama [avatud andmeprotokolli (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) protsessi. Rakenduses saate teha reserveeringu otse müügitellimusel, kasutades käsu **Ava Excelis** valikut **Tellimusega seotud reserveeringud litsentsiplaadi kohta**. Te peate sisestama Exceli lisandmoodulis avanenud üksuse andmetes järgmised reserveeringuga seotud andmed ja valima seejärel **Avalda**, et saata andmed tagasi Supply Chain Managementi.

- Viide (toetatud on ainult väärtus *Müügitellimus*.)
- Tellimuse number (väärtust saab tuletada partiist.)
- Saatepartii ID
- Litsentsiplaat
- Kogus

Kui teil on vaja reserveerida kindlat litsentsiplaati partiijälgimisega kauba jaoks, kasutage lehte **Partii reserveerimine**, nagu on kirjeldatud jaotises [Müügitellimuse üksikasjade sisestamine](#sales-order-details).

Kui laotoimingud töötlevad müügitellimuse rida, mis kasutab tellimusega seotud litsentsiplaadi reserveerimist, ei kasutata asukohakorraldusi.

Kui laotöö kaup koosneb ridadest, mis moodustavad täieliku kaubaaluse ja millel on litsentsiplaadiga seotud kogused, saate optimeerida komplekteerimisprotsessi, kasutades mobiilse seadme menüükäsku, mille puhul on suvandi **Käitle litsentsiplaadi põhjal** väärtuseks seatud *Jah*. Selle asemel, et skannida töö kaupasid ühekaupa, saab laotöötaja seejärel komplekteerimise lõpule viimiseks litsentsiplaadi skannida.

![Mobiilse seadme menüükäsk, mille puhul on suvandi „Käitle litsentsiplaadi põhjal” väärtuseks seatud „Jah”](media/Handle-by-LP-menu-item.png)

Kuna funktsioon **Käitle litsentsiplaadi põhjal** ei toeta mitut kaubaalust hõlmavaid töid, siis on parem, kui eri litsentsiplaatide jaoks on eraldi tööüksus. Selle meetodi kasutamiseks lisage väli **Tellimusega seotud litsentsiplaadi ID** tööpäise piirina lehel **Töömall**.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Näidisstsenaarium: tellimusega seotud litsentsiplaadi reserveerimise seadistamine ja töötlemine

Selles stsenaariumis näidatakse, kuidas seadistada ja töödelda tellimusega seotud litsentsiplaadi reserveerimist.

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selles stsenaariumis viidatakse väärtustele ja kirjetele, mis kuuluvad Supply Chain Managementis esitatud standardsete demoandmete hulka. Kui soovite stsenaariumi läbida siin toodud väärtuseid kasutades, peate kasutama keskkonda, kuhu demoandmed on installitud. Lisaks seadke enne alustamist juriidilise isiku väärtuseks **USMF**.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Varude reserveerimise hierarhia loomine, mis lubab litsentsiplaate reserveerida

1. Avage **Laohaldus \> Seadistus \> Varud \> Reserveerimise hierarhia**.
1. Valige suvand **Uus**.
1. Sisestage väljale **Nimi** väärtus (nt *FlexibleLP*).
1. Sisestage väljale **Kirjeldus** väärtus (nt *Paindlik LP reserveerimine*).
1. Valige loendis **Valitud** suvandid **Partiinumber**, **Seerianumber** ja **Omanik**.
1. Valige nupp **Eemalda** ![vasakule osutav nool](media/backward-button.png), et teisaldada valitud kirjed loendisse **Saadaval**.
1. Valige nupp **OK**.
1. Märkige dimensioonitaseme **Litsentsiplaat** real märkeruut **Luba reserveerimine nõudetellimusel**. Tase **Asukoht** valitakse automaatselt ja selle märkeruutu ei saa tühjendada.
1. Valige käsk **Salvesta**.

### <a name="create-two-released-products"></a>Kahe väljastatud toote loomine

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige toimingupaanil nupp **Uus**.
1. Seadke dialoogiboksis **Uus väljastatud toode** järgmised väärtused.

    - **Tootenumber:** *Item1*
    - **Kaubakood:** *Item1*
    - **Kauba mudeligrupp:** *FIFO*
    - **Kaubagrupp:** *Audio*
    - **Laoala dimensiooni grupp:** *Ladu*
    - **Jälgimisdimensioonigrupp:** *Puudub*
    - **Reserveerimise hierarhia:** *FlexibleLP*

1. Valige toote loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Uus toode avatakse. Seadke kiirkaardil **Ladu** välja **Ühiku seeriagrupi ID** väärtuseks *ea*.
1. Korrake eelmisi samme, et luua teine toode, millel on samad sätted, kuid seadke väljade **Tootenumber** ja **Kaubakood** väärtuseks *Item2*.
1. Valige toimingupaani vahekaardi **Varude haldamine** grupis **Kuva** suvand **Vaba kaubavaru**. Seejärel valige **Koguse korrigeerimine**.
1. Korrigeerige uute kaupade vaba kaubavaru järgmises tabelis täpsustatud viisil.

    | Üksus  | Ladu | Koht | Litsentsiplaat | Kogus |
    |-------|-----------|----------|---------------|----------|
    | Item1 | 24        | FL-010   | LP01          | 10       |
    | Item1 | 24        | FL-011   | LP02          | 10       |
    | Item2 | 24        | FL-010   | LP01          | 5        |
    | Item2 | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > Peate looma need kaks litsentsiplaati ja kasutama asukohti, mis lubavad segakaupu, nt *FL-010* ja *FL-011*.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Müügitellimuse loomine ja kindla litsentsiplaadi reserveerimine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige suvand **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *24*

1. Valige **OK**, et sulgeda dialoogiboks **Müügitellimuse loomine** ja avada uus müügitellimus.
1. Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega rida.

    - **Kaubakood:** *Item1*
    - **Kogus:** *10*

1. Lisage teine järgmiste sätetega müügitellimuse rida.

    - **Kaubakood:** *Item2*
    - **Kogus:** *5*

1. Valige käsk **Salvesta**.
1. Avage kiirkaardil **Rea üksikasjad** vahekaart **Seadistus** ja märkige üles iga rea **Partii ID** väärtus. Neid väärtuseid on vaja kindlate litsentsiplaatide reserveerimisel.

    > [!NOTE]
    > Kindla litsentsiplaadi reserveerimiseks peate kasutama andmeüksust **Tellimusega seotud reserveeringud litsentsiplaadi kohta**. Kindlas litsentsiplaadis partiijälgimisega kauba reserveerimiseks saate kasutada ka lehte **Partii reserveerimine**, nagu on kirjeldatud jaotises [Müügitellimuse üksikasjade sisestamine](#sales-order-details).
    >
    > Kui sisestate litsentsiplaadi otse müügitellimuse real ja kinnitate selle süsteemi, ei kasutata selle rea puhul laohalduse töötlemist.

1. Valige **Ava Microsoft Office'is**, valige **Tellimusega seotud reserveeringud litsentsiplaadi kohta** ja laadige fail alla.
1. Avage allalaaditud fail Excelis ja valige **Luba redigeerimine**, et lubada Exceli lisandmooduli käivitamine.
1. Kui käivitate Exceli lisandmooduli esimest korda, valige käsk **Usalda seda lisandmoodulit**.
1. Kui teil palutakse sisse logida, valige **Logi sisse** ja seejärel logige sisse, kasutades sama identimisteavet, mida kasutasite rakendusse Supply Chain Management sisselogimisel.
1. Kauba reserveerimiseks kindlas litsentsiplaadis valige Exceli lisandmoodulis **Uus**, et lisada reserveerimisrida ja seejärel seadke järgmised väärtused.

    - **Partii ID:** sisestage **Partii ID** väärtus, mille leidsite kauba *Item1* müügitellimuse realt.
    - **Litsentsiplaat:** *LP02*
    - **ReservedInventoryQuantity:** *10*

1. Valige **Uus**, et lisada uus reserveerimisrida ja määrake järgmised väärtused.

    - **Partii ID:** sisestage **Partii ID** väärtus, mille leidsite kauba *Item2* müügitellimuse realt.
    - **Litsentsiplaat:** *LP02*
    - **ReservedInventoryQuantity:** *5*

1. Valige Exceli lisandmoodulis **Avalda**, et saata andmed tagasi Supply Chain Managementi.

    > [!NOTE]
    > Reserveerimisrida kuvatakse süsteemis ainult juhul, kui avaldamine on tõrgeteta lõpetatud.

1. Minge tagasi Supply Chain Managementi. 
1. Kauba reserveeringu läbivaatamiseks valige kiirkaardil **Müügitellimuse read** menüüst **Varud** suvand **Halda \> Reserveering**. Pange tähele, et kauba *Item1* müügitellimuse rea puhul on reserveeritud kogus *10* ja kauba *Item2* müügitellimuse rea puhul on kogus *5*.
1. Müügitellimuse rea reserveeringuga seotud laokannete ülevaatamiseks valige kiirkaardil **Müügitellimuse read** menüüst **Varud** suvand **Kuva \> Kanded**. Pange tähele, et reserveeringuga on seotud kaks kannet: üks, mille välja **Viide** väärtuseks on seatud *Müügitellimus*, ja üks, mille välja **Viide** väärtuseks on seatud *Tellimusega seotud reserveering*.

    > [!NOTE]
    > Kanne, mille välja **Viide** väärtuseks on seatud *Müügitellimus*, näitab tellimuse rea reserveeringut varude dimensioonide jaoks, mis on üle taseme **Asukoht** (sait, ladu ja varude olek). Kanne, mille välja **Viide** väärtuseks on seatud *Tellimusega seotud reserveering*, näitab konkreetse litsentsiplaadi ja asukoha tellimuse rea reserveeringut.

1. Müügitellimuse vabastamiseks valige toimingupaanil vahekaardi **Ladu** grupist **Tegevused** suvand **Vabasta lattu**.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Määratud tellimusega seotud litsentsiplaatidega laotöö ülevaatamine ja töötlemine

1. Valige kiirkaardil **Müügitellimuse read** menüüst **Ladu** suvand **Töö üksikasjad**.

    Litsentsiplaadi reserveerimist kasutava müügitellimuse jaoks tööd luues ei kasuta süsteem asukohakorraldusi, nagu ka siis, kui reserveerimine toimub kindla partii raames. Kuna tellimusega seotud reserveeringus on täpsustatud kõik varude dimensioonid, sealhulgas asukoht, ei pea kasutama asukohakorraldusi, kuna need varude dimensioonid sisestatakse lihtsalt töösse. Need kuvatakse jaotises **Varude dimensioonidest** lehel **Töö laokanded**.

    > [!NOTE]
    > Pärast töö loomist eemaldatakse kauba laokanne, mille välja **Viide** väärtus on *Tellimusega seotud reserveering*. Laokannete puhul, mille välja **Viide** väärtuseks on seatud *Töö*, on nüüd füüsiline reserveering määratud koguse kõigi varude dimensioonide jaoks.

1. Lõpetage mobiilses seadmes komplekteerimine ja töö sisestamine menüükäsu abil, mille märkeruut **Käitle litsentsiplaadi põhjal** on valitud.

    > [!NOTE]
    > Funktsioon **Käitle litsentsiplaadi põhjal** aitab teil töödelda kogu litsentsiplaati. Kui peate töötlema vaid osa litsentsiplaadist, ei saa te seda funktsiooni kasutada.
    >
    > Soovitame iga litsentsiplaadi jaoks luua eraldi töö. Selle tulemuse saavutamiseks kasutage funktsiooni **Tööpäise piirid**, mis asub lehel **Töömall**.

    Litsentsiplaat *LP02* on nüüd müügitellimuse ridadele komplekteeritud ja pandud asukohta *Laadimisuks*. Nüüd on see laadimiseks ja kliendile lähetamiseks valmis.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Tellitud ja kooskõlastatud partiinumbritega laotööde ülevaatamise ja töötlemise erandid

Laotöö komplekteerimiseks tellitud partii numbrite suhtes kehtivad samad standardse lao erandi käsitlemise protsessid ja toimingud, mis tavatöö puhul. Üldiselt saab avatud töö või töörea tühistada ja katkestada, kui kasutaja asukoht on täis, see võib olla lühike-komplekteeritud ja seda saab liikumise tõttu uuendada. Samuti saab vähendada juba lõpetatud töö komplekteeritud kogust või seda tööd muuta.

Järgmist põhireeglit rakendatakse kõigile nende erandite käsitlemise toimingutele: kliendile reserveeritud partiinumbrit ei saa kunagi asendada teise partii numbriga, kuid selle ladustamise dimensioone (asukoht ja litsentsiplaat) saab muuta, selleks peab kasutaja seda käsitsi värskendama või süsteem automaatselt uuendama. Automaatne värskendamine põhineb samadel juhusliku määramisega ladustamise dimensioonidel, mida rakendatakse, kui kindel partii on automaatselt reserveeritud, kuid ladustamise dimensioone ei määratud.

### <a name="example-scenario"></a>Näidisstsenaarium

Selle stsenaariumi näide on olukord, kus varem lõpetatud töö on funktsiooni **Vähenda komplekteeritud kogust** kasutamisel komplekteerimata. Selles näites eeldatakse, et olete juba lõpetanud sammud, mida kirjeldatakse jaotises [Näidisstsenaarium: partiinumbri määramine](#Example-batch-allocation). Tegevus jätkub pärast toda näidet.

1. Avage **Laohaldus** \> **Koormad** \> **Aktiivsed koormad**.
2. Valige koorem, mis loodi seoses teie müügitellimuse saadetisega.
3. Kiirkaardilt **Koorma tellimuse read** valige käsk **Vähenda komplekteeritud kogust**.
4. Valige lehel **Vähenda komplekteeritud kogust** välja **Teisalda asukohta** väärtuseks **FL-001**.
5. Väljal **Teisalda litsentsiplaadile** valige väärtus **LP33**.
6. Sisestage ruudustiku väljale **Varude kogus väljale komplekteerimata** väärtus **10**.
7. Valige nupp **OK**.

Siin on komplekteerimise tegevuse tulemused.

- Varem suletud töö olek on seatud väärtusele **Tühistatud**.
- Tüübi **Varude liikumine** uus töö luuakse komplekteerimata kogusega **10** partiinumbri**B11** jaoks. See töö näitab liikumist asukohast **Baydoor** litsentsiplaadile **LP33** asukohas **FL-001**. Olek on seatud väärtusele **Suletud**.
- Süsteem reserveerib algselt tellitud partiinumbri uuesti ja määrab asukoha ja litsentsiplaadi ID-d. (See protsess on samaväärne funktsiooni **Reserveeri rida** käitamisega antud partiinumbri puhul). Selle tulemusel näidatakse partii **B11** määratuna kiirkaardi **Lähtereale kinnitatud partiinumbrid** lehele **Partii reserveerimine** ja väli **Reserveerimine** sisaldab kogust **10** partiinumbri **B11** jaoks. Lisaks on välja **Asukoht** väärtuseks **FL-001** ja välja **Litsentsiplaat** väärtuseks on seatud **LP11**. (Kui neid ei ole näha, saate need väljad ruudustikku lisada.)

Järgmised tabelid annavad ülevaate sellest, kuidas süsteem käsitleb kindla lao tegevuste tellimusega kooskõlastatud partii reserveerimist. Tabelite sisu tõlgendamiseks oletame, et iga laotoiming käivitatakse tellimusega seotud partii reserveerimisest tuleneva olemasoleva laotöö kontekstis või et iga laotoimingu käivitamine mõjutab seda tüüpi tööd.

> [!NOTE]
> Neis tabelites näitab veerg Partii kogus on saadaval, kas partii kogus on saadaval lisaks kogusele, mis on juba reserveeritud praeguse tellimusega seotud reserveeringutele, või on juba reserveeritud laotööst, mis pärineb selle tüübi reserveeringutest.

#### <a name="override-the-pick-location-on-the-open-work"></a>Avatud tööde komplekteerimise asukoha alistamine

<table>
<thead>
<tr>
<th>Võtmeseadistuse parameeter</th>
<th>Partii kogus on saadaval</th>
<th>Võtmekasutaja sammud</th>
<th>Laotöö</th>
<th>Tellimusega kooskõlastatud partii reserveerimine</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Suvand <strong>Luba komplekteerimise asukoha alistamine</strong> on töötajale lubatud.</td>
<td>Jah</td>
<td>
<ol>
<li>Valige suvand <strong>Alista asukoht</strong> laorakenduses, kui käivitate töö komplekteerimise.</li>
<li>Valige <strong>Soovita</strong>.</li>
<li>Kinnitage uus asukoht, mis on soovitatud partii koguse kättesaadavuse alusel.</li>
</ol>
</td>
<td>Praeguse töö puhul toimuvad järgmised tegevused.
<ul>
<li>Komplekteerimise real olev asukoht uuendatakse uude asukohta. (Kui asukoha määrab litsentsiplaat, on töölao kandele määratud juhuslik litsentsiplaat ja töötaja saab valida mis tahes saadaoleva kogusega litsentsiplaadi.)</li>
<li>Kui kogus leitakse uues asukohas rohkem kui ühel litsentsiplaadil, jaotatakse algse komplekteerimise rida mitmeks reaks, et see vastaks igale litsentsiplaadile.</li>
</ul>
</td>
<td>Pole kohaldatav</td>
</tr>
<tr>
<td>Ei</td>
<td>
<ol>
<li>Valige suvand <strong>Alista asukoht</strong> laorakenduses, kui käivitate töö komplekteerimise.</li>
<li>Sisestage asukoht käsitsi.</li>
</ol>
</td>
<td>Toiming <strong>Asukoha alistamine</strong> pole võimalik. See nurjub ja kuvatakse tõrge.</td>
<td>Pole kohaldatav</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Nupp Täis – jaotab töörea kasutaja asukoha ületäitumise tõttu

<table>
<thead>
<tr>
<th>Võtmeseadistuse parameeter</th>
<th>Partii kogus on saadaval</th>
<th>Võtmekasutaja sammud</th>
<th>Laotöö</th>
<th>Tellimusega kooskõlastatud partii reserveerimine</th>
</tr>
</thead>
<tbody>
<tr>
<td>Valik <strong>Luba töö jaotamine</strong> on lubatud mobiilseadme menüükäsul.</td>
<td>Pole kohaldatav</td>
<td>
<ol>
<li>Valige laorakenduses menüüsuvand <strong>Täis</strong>, kui käivitate töö komplekteerimise.</li>
<li>Sisestage väljale <strong>Komplekteeri kogus</strong> nõutava komplekteerimise osaline kogus, et näidata kogu võimsust.</li>
</ol>
</td>
<td>
<ul>
<li>Praeguse töö puhul uuendatakse kogus järelejäänud kogusele, mis tuleb komplekteerida.</li>
<li>Komplekteeritud koguse uus töö luuakse ja suletakse.</li>
</ul></td>
<td>Pole kohaldatav</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Lõpetatud töö komplekteeritud koguse vähendamine (koormast)

<table>
<thead>
<tr>
<th>Võtmeseadistuse parameeter</th>
<th>Partii kogus on saadaval</th>
<th>Võtmekasutaja sammud</th>
<th>Laotöö</th>
<th>Tellimusega kooskõlastatud partii reserveerimine</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Pole kohaldatav</td>
<td>Jah</td>
<td>
<ol>
<li>Avage koorma realt leht <strong>Komplekteeritud koguse vähendamine</strong>.</li>
<li>Sisestage kogu kogus, mis ei lähe komplekteerimisele.</li>
<li>Valige teisaldamiseks asukoht/litsentsiplaat.</li>
</ol>
</td>
<td>
<ul> 
<li>Koorma reaga seotud töö on tühistatud.</li>
<li>Varude teisaldamiseks luuakse uus töö ja suletakse.</li>
</ul>
</td>
<td>Kogus reserveeritakse sama partii jaoks uuesti. Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</td>
</tr>
<tr>
<td>Ei</td>
<td>Vt eelmist rida.</td>
<td>Vt eelmist rida.</td>
<td>Kogus reserveeritakse samale partiile samas asukohas ja litsentsiplaadiga (kui asukoht on litsentsiplaadi kontrollitud), mis sisestati komplekteerimise ajal.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Kauba teisaldamine laos

> [!NOTE]
> See laotoiming rakendub ainult tüübi **Töö loomise protsess** teisaldamistele, mitte malli alusel teisaldamistele.

<table>
<thead>
<tr>
<th>Võtmeseadistuse parameeter</th>
<th>Partii kogus on saadaval</th>
<th>Võtmekasutaja sammud</th>
<th>Laotöö</th>
<th>Tellimusega kooskõlastatud partii reserveerimine</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Töötaja saab <strong>lubada seotud töö varude teisaldamist</strong>.</td>
<td>Jah</td>
<td>
<ol>
<li>Alustage teisaldamist laorakenduses.</li>
<li>Sisestage alg- ja lõppasukohad.</li>
</ol></td>
<td>
<ul>
<li>Kõigi olemasolevate tööde puhul, mida teisaldamine mõjutab, uuendatakse komplekteerimise asukoht uude asukohta.</li>
<li>Varude teisaldamiseks luuakse uus töö ja suletakse.</li>
</ul>
</td>
<td>Kõik olemasolevad reserveeringud, mis mõjutavad koguse liikumist antud asukohast, reserveeritakse sama partii jaoks uuesti. Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</td>
</tr>
<tr>
<td>Ei</td>
<td>Vt eelmist rida.</td>
<td>Vt eelmist rida.</td>
<td>Kõik olemasolevad reserveeringud, mis mõjutavad koguse liikumist antud asukohast, reserveeritakse uuesti sama partii ja uue asukoha ning litsentsiplaadi jaoks (kui asukoht on litsentsiplaadi kontrollitud).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Lõpetatud töö komplekteeritud koguse vähendamine (koormast või voost)

<table>
<thead>
<tr>
<th>Võtmeseadistuse parameeter</th>
<th>Partii kogus on saadaval</th>
<th>Võtmekasutaja sammud</th>
<th>Laotöö</th>
<th>Tellimusega kooskõlastatud partii reserveerimine</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Pole kohaldatav</td>
<td>Jah</td>
<td>
<ol>
<li>Avage leht <strong>Tühistatud töö</strong>.</li>
<li>Taotlemise lehel märkige ruut <strong>Jäta kaubad praegusesse asukohta</strong>.</li>
</ol>
</td>
<td>Koorma reaga seotud kõik tööd on tühistatud.</td>
<td>Kogus reserveeritakse sama partii jaoks uuesti. Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</td>
</tr>
<tr>
<td>Ei</td>
<td>Vt eelmist rida.</td>
<td>Vt eelmist rida.</td>
<td>Kogus reserveeritakse samale partiile ja asukohale ning litsentsiplaadile, kuhu kogus tühistamisel jäeti.</td>
</tr>
<tr>
<td>Jah</td>
<td>
<ol>
<li>Avage leht <strong>Tühistatud töö</strong>.</li>
<li>Taotlemise lehel märkige ruut <strong>Määra kaubad sellesse asukohta</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Praegune töö on tühistatud.</li>
<li>Varude teisaldamiseks luuakse uus töö ja suletakse.</li>
</ul>
</td>
<td>Kogus reserveeritakse sama partii jaoks uuesti. Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</td>
</tr>
<tr>
<td>Ei</td>
<td>Vt eelmist rida.</td>
<td>Vt eelmist rida.</td>
<td>Kogus reserveeritakse samale partiile ja asukohale ning litsentsiplaadile, kuhu kogus tühistamisel määrati.</td>
</tr>
<tr>
<td>Jah/ei</td>
<td>
<ol>
<li>Avage leht <strong>Tühistatud töö</strong>.</li>
<li>Taotlemise lehel märkige ruut <strong>Teisalda kaubad sellesse asukohta</strong>.</li>
</ol>
</td>
<td>Tühistamist ei toetata.</td>
<td>Pole kohaldatav</td>
</tr>
<tr>
<td>Jah/ei</td>
<td>
<ol>
<li>Avage leht <strong>Tühistatud töö</strong>.</li>
<li>Taotlemise lehel märkige ruut <strong>Teisalda kaubad asukoha direktiivi kohaselt</strong>.</li>
</ol>
</td>
<td>Tühistamist ei toetata. </td>
<td>Pole kohaldatav</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Koguse lühiajaline komplekteerimine – registreerige kogus komplekteerimise ajal asukohas/litsentsiplaadil kui füüsiliselt leidmata.

<table>
<thead>
<tr>
<th>Võtmeseadistuse parameeter</th>
<th>Partii kogus on saadaval</th>
<th>Võtmekasutaja sammud</th>
<th>Laotöö</th>
<th>Tellimusega kooskõlastatud partii reserveerimine</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Töö erandi tüübiks on seadistatud<strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>puudub</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Ei</strong>.</td>
<td>Jah</td>
<td>
<ol>
<li>Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</li>
<li>Sisestage väljale <strong>Komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</li>
<li>Väljale <strong>Põhjus</strong> sisestage väärtus <strong>Ümberjaotamine puudub</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Praegune töö on suletud ja komplekteeritud kogus on 0 (null).</li>
<li>Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</li>
</ul>
</td>
<td>Kogus reserveeritakse sama partii jaoks uuesti. Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</td>
</tr>
<tr>
<td>Ei</td>
<td>Vt eelmist rida.</td>
<td>
<ul>
<li>Lühikese komplekteerimise toiming nurjub ja kuvatakse tõrge.</li>
<li>Praegune töö jääb avatuks.</li>
</ul>
</td>
<td>Pole kohaldatav</td>
</tr>
<tr>
<td rowspan='2'>Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Puudub</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah</strong>.</td>
<td>Jah</td>
<td>
<ol>
<li>Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</li>
<li>Sisestage väljale <strong>Komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</li>
<li>Väljale <strong>Põhjus</strong> sisestage väärtus <strong>Ümberjaotamine puudub</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Praegune töö on suletud ja komplekteeritud kogus on 0 (null).</li>
<li>Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</li>
</ul>
</td>
<td>Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast, reserveeritakse sama partii jaoks uuesti. Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</td>
</tr>
<tr>
<td>Ei</td>
<td>Vt eelmist rida.</td>
<td>Vt eelmist rida.</td>
<td>Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast, eemaldatakse.</td>
</tr>
<tr>
<td>Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah/ei</strong>. Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</td>
<td>Jah</td>
<td>
<ol>
<li>Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</li>
<li>Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</li>
<li>Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</li>
<li>Valige loendist asukoht/litsentsiplaat.</li>
</ol>
</td>
<td>
<ul>
<li>Praeguse töö puhul toimuvad järgmised tegevused.
<ul>
<li>Praegune komplekteerimise rida on suletud ja komplekteeritud kogus on 0 (null).</li>
<li>Asetusrida on tühistatud.</li>
<li>Luuakse uus komplekteerimise rida. See kasutab kasutaja valitud asukohta/litsentsiplaati.</li>
<li>Luuakse uus asetusrida.</li>
</ul>
</li>
<li>Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</li>
</ul>
</td>
<td>Pole kohaldatav</td>
</tr>
<tr>
<td>Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Ei</strong>. Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</td>
<td>Ei</td>
<td>
<ol>
<li>Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</li>
<li>Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</li>
<li>Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</li>
</ol>
</td>
<td>Lühikese komplekteerimise toiming nurjub ja kuvatakse tõrge.</td>
<td>Pole kohaldatav</td>
</tr>
<tr>
<td>Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah</strong>. Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</td>
<td>Ei</td>
<td>
<ol>
<li>Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</li>
<li>Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</li>
<li>Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</li>
<li>Valige loendist asukoht/litsentsiplaat.</li>
</ol>
</td>
<td>
<ul>
<li>Praeguse töö puhul toimuvad järgmised tegevused.
<ul>
<li>Praegune komplekteerimise rida on suletud ja komplekteeritud kogus on 0 (null).</li>
<li>Asetusrida on tühistatud.</li>
</ul>
</li>
<li>Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</li>
</ul>
</td>
<td>Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast/litsentsiplaadilt, eemaldatakse.</td>
</tr>
<tr>
<td>Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Automaatne</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah/ei</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah/ei</strong>.</td>
<td>Pole kohaldatav</td>
<td>
<ol>
<li>Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</li>
<li>Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</li>
<li>Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos automaatse ümberjaotamisega</strong>.</li>
</ol>
</td>
<td>Lühiajalist komplekteerimist, mis hõlmab automaatset ümberjaotamist, ei toetata.</td>
<td>Lühiajalist komplekteerimist, mis hõlmab automaatset ümberjaotamist, ei toetata.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Muuda varude olekut

> [!NOTE]
> Seda laotoimingut saab sooritada mitmest kirjest. Siin kuvatud näites kasutatakse toimingut **Varude oleku muutmine** lehe **Vaba asukoht** alusel.

<table>
<thead>
<tr>
<th>Võtmeseadistuse parameeter</th>
<th>Partii kogus on saadaval</th>
<th>Võtmekasutaja sammud</th>
<th>Laotöö</th>
<th>Tellimusega kooskõlastatud partii reserveerimine</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Vahekaardil <strong>Ladu</strong>, kirjes <strong>Ladu</strong> on välja <strong>Eemalda reserveeringud ja märgised</strong> väärtuseks määratud <strong>Reserveeringud</strong> või <strong>Märgistused ja reserveeringud</strong>.</td>
<td>Jah</td>
<td>
<ol>
<li>Valige kindel asukoht.</li>
<li>Valige rida, millel on kindel kaup, asukoht ja litsentsiplaat (kui asukoht on litsentsiplaadi kontrollitud).</li>
<li>Valige <strong>Varude oleku muutmine</strong>.</li>
<li>Seadke välja <strong>Varude olek</strong> väärtuseks <strong>Blokeerimine</strong>.</li>
</ol>
</td>
<td>Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</td>
<td>
<ul>
<li>Kogus reserveeritakse sama partii jaoks uuesti. Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</li>
<li>Tüübi <strong>Varude oleku muutmine</strong> kaks laokannet luuakse selleks, et tähistada varude oleku dimensiooni muutumist.</li>
<li>Tüübi <strong>Varude blokeerimine</strong> ja probleemitüübi <strong>Reserveeritud füüsiline</strong> luuakse selleks, et tähistada blokeeritud koguse reserveerimist.</li>
</ul>
</td>
</tr>
<tr>
<td>Ei</td>
<td>Vt eelmist rida.</td>
<td>Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</td>
<td>
<ul>
<li>Reserveering eemaldatakse.</li>
<li>Tüübi <strong>Varude oleku muutmine</strong> kaks laokannet luuakse selleks, et tähistada varude oleku dimensiooni muutumist.</li>
<li>Tüübi <strong>Varude blokeerimine</strong> ja probleemitüübi <strong>Reserveeritud füüsiline</strong> luuakse selleks, et tähistada blokeeritud koguse reserveerimist.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Vahekaardil <strong>Ladu</strong>, kirjes <strong>Ladu</strong> on välja <strong>Eemalda reserveeringud ja märgised</strong> väärtuseks määratud <strong>Puudub</strong>.</td>
<td>Jah</td>
<td>
<ol>
<li>Valige kindel asukoht.</li>
<li>Valige rida, millel on kindel kaup, asukoht ja litsentsiplaat (kui asukoht on litsentsiplaadi kontrollitud).</li>
<li>Valige <strong>Varude oleku muutmine</strong>.</li>
<li>Seadke välja <strong>Varude olek</strong> väärtuseks <strong>Blokeerimine</strong>.</li>
</ol>
</td>
<td>Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</td>
<td>Kogus reserveeritakse sama partii jaoks uuesti. Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</td>
</tr>
<tr>
<td>Ei</td>
<td>Vt eelmist rida.</td>
<td>Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</td>
<td>Varude oleku muudatused pole lubatud.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Kitsendused

- Paindliku lao taseme dimensiooni reserveerimise funktsionaalsus ei toeta järgmisi funktsioone.

    - Tegeliku kaalu haldus
    - Füüsiline negatiivne laovaru
    - Tellitud tarnete reserveerimine
    - Üleviimistellimuste ja toormaterjalide komplekteerimine

- Konteineri konsolideerimise reeglil on direktiivi ühiku alusel pakkimisel piirangud. Tellimusega kooskõlastatud reserveeringute puhul on soovitatav mitte kasutada konteineri loomise malle, mille puhul väli **Pakk direktiiviühiku järgi** on lubatud. Praeguses kujunduses ei kasutata asukoha direktiive laotöö loomisel. Seetõttu rakendatakse konteinerite voo etapis ainult madalaimat ühikut ühikute seeriagrupis (laoühikutes).
