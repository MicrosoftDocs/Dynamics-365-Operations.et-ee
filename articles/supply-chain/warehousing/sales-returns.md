---
title: Müügitagastused
description: See teema annab teavet tagastustellimuste protsessi kohta. See hõlmab teavet klienditagastuste ning nende mõju kohta kuluarvestusele ja vaba kaubavaru kogustele.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnTable, ReturnTableListPagePreviewPane, ReturnTableReferences, SalesReturnExpiredOrdersPart, SalesReturnFindOrderFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c01a945735f6340a0efd3d9c5ff74dd8cebd9ab7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263320"
---
# <a name="sales-returns"></a>Müügitagastused

[!include [banner](../includes/banner.md)]

See teema annab teavet tagastustellimuste protsessi kohta. See hõlmab teavet klienditagastuste ning nende mõju kohta kuluarvestusele ja vaba kaubavaru kogustele.

Kliendid saavad tagastada kaupu erinevatel põhjustel. Näiteks võib kaup olla defektne või see ei pruugi vastata kliendi ootustele. Tagastusprotsess käivitub, kui klient väljastab kauba tagastamiseks taotluse. Pärast kliendi taotluse vastuvõtmist luuakse tagastustellimus.

## <a name="return-order-process"></a>Tagastustellimuse protsess
Järgmine näide annab ülevaate tagastustellimuse protsessist.  

[![Tagastustellimuse protsess](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

On kaks tagastustellimuse protsessi tüüpi: füüsiline tagastus ja ainult kreedit.

-   **Füüsiline tagastus** – tagastustellimus autoriseerib toodete füüsilist tagastust.
-   **Ainult kreedit** – tagastustellimus autoriseerib kliendi krediiti, kuid ei nõua, et klient tooted füüsiliselt tagastaks.

### <a name="physical-return-order-process"></a>Füüsiline tagastustellimuse protsess

1.  **Tagastustellimuse loomine.** Dokumenteerige formaalselt kliendi autoriseerimine, et tagastada mis tahes defektsed või soovimatud tooted. Tagastustellimus ei nõua, et ettevõte aktsepteeriks tagastatud tooteid või pakuks kliendile krediiti. Tagastuse aktsepteerimisel saate autoriseerida asenduskauba saatmise enne, kui defektne kaup on tagastatud.
2.  **Kontrollimiseks lattu saabumine.** Viige tagastustellimuse dokumendi suhtes lõpule algne kontrollimine ja kinnitamine. Tagastustellimus toetab täiendavaks kontrollimiseks ja kvaliteedikontrolli tegemiseks ka tagastatud kaupade vaheladu.
3.  **Likvideerimise kindlaksmääramine.** Viige kontrollimise protsess lõpule ja otsustage, mida teha tagastatud toodetega. Osana sellest etapist otsustage, kas krediteerite klienti, lükkate tootetagastuse tagasi või aktsepteerite tootetagastust, praagite toote ja saadate seejärel kliendile asendustoote.
4.  **Saatelehe loomine.** Looge saateleht ja kinnitage 3. etapis tehtud likvideerimisotsus. Viige logistikaprotsessid lõpule.
5.  **Loo arve.** Sulgege tagastustellimus.

### <a name="credit-only-process"></a>Ainult kreediti protsess

1.  **Tagastustellimuse loomine.** Dokumenteerige formaalselt kliendi autoriseerimine, et kreeditit vastu võtta ilma defektsete või soovimatute toodete tagastamiseta. Valiku **Ainult kreedit** likvideerimiskood autoriseerib otsuse krediteerida klienti ilma füüsilise tagastuseta.
2.  **Loo arve.** Looge kreeditarve ja sulgege seejärel tagastustellimus.

## <a name="return-material-authorization"></a>Tagastatud kauba autoriseerimine
Tagastatud kauba autoriseerimise (RMA) töötlemine põhineb müügitellimuse funktsionaalsusel. Tagastus registreeritakse tagastustellimusena, mis luuakse müügitellimusena ja sellega võib olla seotud mõni muu müügitellimus, mida nimetatakse asendustellimuseks. Mõlemad müügitellimused on seotud tagastuse algse numbriga.

-   **Tagastustellimus** – RMA registreerimiseks loote tagastustellimuse, mis on müügitellimus, millel on määratud tüüp **Tagastatud tellimus** Mis tahes tagastuse teabele tehtavaid muudatusi värskendatakse automaatselt müügitellimusel. Kuni tagastustellimusel on olek **Avatud**, ei ilmu see müügitellimuste loendisse. Kasutate tagastust, et käsitleda tagastatud kaupade saabumist ja sissetulekut, aga ka selleks, et autoriseerida ainult kreediti likvideerimistoimingut (vt jaotist **Likvideerimiskoodid ja likvideerimistoimingud**). Kõiki teisi järeltegevuse protsesse tuleb käsitleda müügitellimuses.
-   **Asendustellimus** – kui asendustellimus tuleb kliendile tarnida, võib tagastus hõlmata teist seotud müügitellimust. Kohese saadetise toetamiseks saate tagastuse jaoks luua manuaalse asendustellimuse. Teise võimalusena saab asendustellimust luua automaatselt pärast seda, kui saabumine, kontrollimine ja sissetulek on lõpule viidud tagastuse rea kauba jaoks, millel on asendamist näitav likvideerimiskood. Asendustellimusel on samad müügitellimusega seotud funktsioonid. Näiteks saate seda kasutada kohandatud toote konfigureerimiseks asenduskaubaks, luua tagastatud kauba parandamiseks tootmistellimuse, luua hankijalt asenduse saatmiseks otsetarne ostutellimuse või toetada teisi eesmärke.

## <a name="create-a-return-order"></a>Tagastustellimuse loomine
Tagastustellimuse protsess käivitub, kui klient võtab teie organisatsiooniga ühendust, et tagastada defektne või soovimatu toode ja/või et see krediteerida. Kui teie organisatsioon aktsepteerib tagastuse, dokumenteeritakse tagastus tagastustellimusega. See tagastustellimus muutub tagastatud toote sisemise töötlemise keskpunktiks. Järgmine illustratsioon näitab tagastustellimuse loomise protseduuri.  

[![Protseduur tagastustellimuse loomiseks](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Tagastustellimuse päise loomine

Tagastustellimuse loomisel tuleb lisada järgmises tabelis sisalduv teave.

| Väli              | Kirjeldus                                              | Kommentaarid                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kliendi konto   | Viide tabelile Kliendid                       | Peate sisestama olemasoleva kliendikonto.                                                                                                                                                                                                                                                                                                  |
| Tarneaadress   | Aadress, kuhu kaup tagastatakse                 | Vaikimisi kasutatakse organisatsiooni aadressi. Kui päises valitakse spetsiifiline ladu, muudetakse tarneaadress lao tarneaadressiks. Seda aadressi saate muuta lehel **Tagastustellimuse üksikasjad**.                                                                                                  |
| Tegevuskoht/ladu     | Tagastatud toodet vastuvõttev tegevuskoht või ladu | Tagastustellimuse tarneaadress määratakse tegevuskoha või lao tarneaadressi põhjal.                                                                                                                                                                                                                                 |
| Tagastuse number         | Tagastustellimusele määratud ID              | Tagastuse numbrit kasutatakse tagastustellimuse protsessi jooksul alternatiivvõtmena. Määratav tagastuse number põhineb tagastuse numbriseerial, mis seadistatakse lehel **Müügireskontro parameetrid**.                                                                                                                              |
| Lõpptähtaeg           | Viimane kuupäev, millal kauba saab tagastada               | Vaikeväärtus arvutatakse praeguse kuupäevana, millele lisandub kehtivuse periood. Näiteks kui tagastus kehtib ainult 90 päeva alates tagastustellimuse loomise kuupäevast ja tagastustellimus loodi 1. mail, on väljal olev väärtus **30. juuli**. Kehtivusperiood määratakse lehel **Müügireskontro parameetrid**. |
| Tagastuspõhjuse kood | Kliendi põhjus toote tagastamiseks          | Põhjuse kood valitakse kasutaja määratletud põhjusekoodide loendis. Saate seda välja igal ajal värskendada.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Tagastustellimuse ridade loomine

Pärast tagastuspäise lõpuleviimist saate luua tagastusread, kasutades üht järgmistest meetoditest.

-   Sisestage iga tagastusrea jaoks kauba üksikasjad, kogus ja muu teave.
-   Looge tagastusrida, kasutades funktsiooni **Otsi müügitellimust**. Soovitame teil kasutada seda funktsiooni tagastustellimuse loomisel. Funktsioon **Otsi müügitellimust** tuvastab tagastusrealt viite arveldatud müügitellimuse reale ja toob rea üksikasjad, nagu kauba number, kogus, hind, allahindlus ja kuluväärtused müügirealt. Viide aitab tagada, et kui toode tagastatakse ettevõttele, hinnatakse seda sama ühikukuluga, millega see müüdi. Viide kinnitab ka, et tagastustellimusi ei looda kogusele, mis ületab arvel müüdud kogust.

>[Märkus.] Tagastusridu, millel on viide müügitellimusele, käsitletakse müügi paranduste või tühistamistena. Lisateabe saamiseks vaadake teemas allpool toodud jaotist „Pearaamatusse sisestamine”.

### <a name="charges"></a>Tasud

Tasud ja kulud saab lisada tagastustellimusele ühe või mitme järgmise meetodi kaudu.

-   Saate tagastustellimuse päisele, tagastustellimuse reale või mõlemale käsitsi kulud lisada.
-   Tasud saab tagastuse põhjusekoodi funktsioonina automaatselt tagastustellimuse päisele lisada.
-   Tasud saab rea likvideerimiskoodi põhjal automaatselt tagastustellimuse reale lisada.

Tasud lisatakse automaatselt pärast seda, kui reale on määratud tagastuse põhjuse- või likvideerimiskood. Kui põhjusekoodi muudetakse hiljem, siis olemasolevat kulukirjet ei eemaldata, kuid uue põhjusekoodi põhjal võidakse lisada uus kulukirje. Tagastustellimuse ridadele tasude lisamisel muutuvad tasud, mis arvutatakse protsendina rea või tellimuse väärtusest, negatiivseks, kui rida või rea tellimus on negatiivne, välja arvatud juhul kui protsent on ka negatiivne number. Negatiivse väärtusega tasu tähistab krediiti kliendile.

### <a name="return-reason-codes"></a>Tagastuspõhjuste koodid

Tagastustele põhjusekoodide rakendamisega saate muuta tagastusmustrite analüüsimise lihtsamaks. Põhjusekoodid annavad teavet selle kohta, miks klient soovib kaupu tagastada. Mõnedel organisatsioonidel on palju põhjusekoode. Need organisatsioonid võivad grupeerida põhjusekoode põhjusekoodi gruppidesse, et saada parem ülevaade ja akumuleeritud aruandluse jaoks.

### <a name="disposition-codes-and-disposition-actions"></a>Likvideerimiskoodid ja -tegevused

Oluline etapp tagastustellimuse protsessis on likvideerimiskoodi määramine tagastustellimuse reale osana saabumise registreerimisest. Likvideerimiskood määratleb järgmise teabe.

-   **Finantsmõjud** – kas klienti tuleks tagastatud kaupade eest krediteerida ja kas mis tahes tasud tuleks lisada tagastustellimuse reale.
-   **Tagastatud kauba likvideerimine** – kas kauba saab lisada tagasi varudesse, kas see tuleks välja praakida või kas see tuleks kliendile tagastada?
-   **Tagastatud kauba logistika** – kas asenduskaup tuleks kliendile väljastada?

Lisaks määratlemisele, kuidas tagastatud kaupu likvideerida, saavad likvideerimiskoodid põhjustada tagastusreale tasude põhjustamist. Neid saab kasutada ka statistilise analüüsi jaoks tagastuste grupeerimiseks. Likvideerimiskoodid määratletakse osana tagastustellimuste seadistusest. Lisaks peab iga likvideerimiskood viitama ühele integreeritud likvideerimistegevusele. Järgmine tabel annab loendi integreeritud likvideerimiskoodidest ja nende tegevustest. **Oluline.** Kui kaupa ei tohiks tagastada, kuid klienti peaks siiski krediteerima, määrake tagastusreale likvideerimiskood **Ainult kreedit**.

<table>
<thead>
<tr class="header">
<th>Likvideerimiskood</th>
<th>Finantsilised mõjud</th>
<th>Mõjud logistikale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ainult kreedit</td>
<td><ul>
<li>Kliendilt krediteeritakse müügihind, millest on lahutatud kõik tasud.</li>
<li>Kauba väljapraakimisest tulenev kahjum sisestatakse pearaamatusse.</li>
</ul></td>
<td>Kaupa ei tohiks tagastada. Seda likvideerimistegevust kasutatakse järgmiste juhtumite puhul.
<ul>
<li>Osapoolte vahel on piisavalt usaldust.</li>
<li>Defektse kauba tagastamise kulu on tõkestav.</li>
<li>Kaupu ei saa lubada tagasi varudesse. Teiste tingimuste tõttu pole füüsiline tagastus vajalik.</li>
</ul></td>
</tr>
<tr class="even">
<td>Krediit</td>
<td><ul>
<li>Kliendilt krediteeritakse müügihind, millest on lahutatud kõik tasud.</li>
<li>Varude väärtust suurendatakse tagastatud kauba kulu võrra.</li>
</ul></td>
<td>Kaup tagastatakse ja lisatakse tagasi varudesse.</td>
</tr>
<tr class="odd">
<td>Asenda ja kanna kreeditisse</td>
<td><ul>
<li>Kliendilt krediteeritakse müügihind, millest on lahutatud kõik tasud.</li>
<li>Varude väärtust suurendatakse tagastatud kauba kulu võrra.</li>
<li>Luuakse asendus eraldi müügitellimusele ja seda käsitletakse eraldi.</li>
</ul></td>
<td>Kaup tagastatakse ja lisatakse tagasi varudesse.</td>
</tr>
<tr class="even">
<td>Asenda ja kanna praaki</td>
<td><ul>
<li>Kliendilt krediteeritakse müügihind, millest on lahutatud kõik tasud.</li>
<li>Kauba väljapraakimisest tulenev kahjum sisestatakse pearaamatusse.</li>
<li>Luuakse asendus eraldi müügitellimusele ja seda käsitletakse eraldi.</li>
</ul></td>
<td>Kaup tagastatakse ja praagitakse välja.</td>
</tr>
<tr class="odd">
<td>Tagasta kliendile</td>
<td>Puudub, välja arvatud mis tahes tasud.</td>
<td>Kaup tagastatakse, kuid saadetakse pärast kontrollimist tagasi kliendile. Seda likvideerimistegevust võidakse kasutada, kui kaupa on sihilikult kahjustatud või kui garantii on tühistatud.</td>
</tr>
<tr class="even">
<td>Praak</td>
<td><ul>
<li>Kliendilt krediteeritakse müügihind, millest on lahutatud kõik tasud.</li>
<li>Kauba väljapraakimisest tulenev kahjum sisestatakse pearaamatusse.</li>
</ul></td>
<td>Kaup tagastatakse või praagitakse välja.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Kontrollimiseks lattu saabumine
Enne kui saate tagastatud kaubad saatelehe sisestamisega varudes füüsiliselt vastu võtta, peavad kaubad läbima saabumise registreerimise ja valikulise kontrollimise. Järgmine näide annab ülevaate saabumisprotsessist. Järgmistes jaotistes on kirjeldatud iga etappi, mida illustratsioonis on näidatud.  

[![Saabumisprotsess](./media/salesreturn03.png)](./media/salesreturn03.png)  

Protsessil on mitu muud variatsiooni, mida selles teemas ei käsitleta. Siin on mõned nendest variatsioonidest.

-   Ärge kasutage saabumise töölehe loomiseks loendit **Saabumise ülevaade**. Selle asemel looge käsitsi saabumise tööleht. Tagastustellimustel on viiteks **Müügitellimus**.
-   Kui kasutate laohaldust, looge kaubaaluste transportimine. Tagastusreal on kaubaaluse transportimise käigus olek **Saabunud**.
-   Registreerige tagastatud kauba saabumine otse tagastustellimuse realt, kasutades funktsiooni **Registreerimine**.

Saabumisprotsessi käigus integreeritakse tagastused lao saabumiste üldise protsessiga. Saabumisprotsess toetab ka vahelaoorderite loomist tagastatud kaupadele, mis peavad läbima eraldi kontrollimise.

### <a name="identify-products-in-the-arrival-overview-list"></a>Saabumise ülevaateloendis toodete tuvastamine

Leht **Saabumise ülevaade** annab loendi plaanitud sissetulevatest saabumistest. 
>[Märkus.] Tagastustellimustelt tulenevaid saabumisi tuleb muud tüüpi saabumiskannetest eraldi töödelda. Pärast lehel **Saabumise ülevaade** sissetuleva paketi tuvastamist (nt kaasasoleva tagastusdokumendi abil) klõpsake tegumiribal nuppu **Alusta saabumistöölehte**, et luua ja käivitada saabumisega ühtiv saabumise tööleht.

### <a name="edit-the-arrival-journal"></a>Saabumise töölehe redigeerimine

Määrates suvandi **Vahelao haldus** olekusse **Jah**, saate tagastusreale vahelaoorderi luua. Kui rida on saadetud kontrollimiseks vahelattu, ei saa te likvideerimiskoodi määrata. 
 
Kui määrate suvandi **Vahelao haldus** kauba varude mudeligrupis olekusse **Jah**, märgistatakse suvand **Vahelao haldus** lehel **Tööleheread** saabumise töölehe rea jaoks ja seda ei saa muuta. Kui rida saadetakse vahelattu, peate määrama sobiva vahelao. 

Kui saabumisrida ei saadeta kontrollimiseks, peab lao saabumise ametnik määrama likvideerimiskoodi otse saabumise töölehereale ja saabumise töölehe seejärel sisestama. Kui sama likvideerimiskoodi ei tohiks määrata tagastusrea tervele kogusele või kui rea täiskogust pole vastu võetud, peate rea tükeldama. Saabumise töölehe rea tükeldamisel tükeldate ka tagastusrea (**SalesLine**) ja loote uue partii ID. Saate rea tükeldada, vähendades saabumise töölehe rea kogust. Töölehe sisestamisel luuakse uus tagastusrida, mille olek on järelejäänud koguse puhul **Eeldatud**. Saate rea ka tükeldada, klõpsates valikuid **Funktsioonid** &gt; **Tükelda**.

### <a name="process-the-quarantine-order"></a>Vahelaoorderi töötlemine

Kui tagastud tooted saadetakse kontrollimiseks vahelattu, viiakse mis tahes täiendav töötlemine lõpule vahelaoorderis. Iga vahelattu saadetava saabumise rea jaoks luuakse üks vahelaoorder. Likvideerimiskood näitab kontrolliprotsessi tulemust. 

Saate vahelaoorderi tükeldada sarnaselt saabumise töölehe tükeldamisele. Vahelaoorderi tükeldamisel põhjustate tagastusrea vastavat tükeldamist. Pärast likvideerimiskoodi sisestamist viige vahelaoorder lõpule, kasutades funktsiooni **Lõpp** või funktsiooni **Kinnita lõpetamine**. Kui valite **Teata lõpetamisest**, luuakse määratud laos uus saabumine. Seejärel saate seda saabumist töödelda, kasutades lehte **Saabumise ülevaade**. 

Kui saabumine pärineb vahelaoorderist, ei saa te muuta kontrollimise käigus määratud likvideerimiskoodi. Kui lõpetate vahelaoorderi funktsiooni **Lõpp** abil, registreeritakse partii automaatselt. Mõnikord saadetakse kaup vahelaost tagasi lähetamise ja vastuvõtmise osakonda. Näiteks ei pruugi vahelao kontrollija teada, kus kaupa varudes talletada. Sellisel juhul tuleb vastavat saatelehte värskendada, et vahelao tõttu määratud likvideerimiskoodi õigesti registreerida ja selle alusel õigesti toimida. 

Sissetuleku kinnitamise saab saata kliendile tagastusrea registreerimisel. Aruanne **Tagasta kinnitus** sarnaneb tagastustellimuse dokumendile. Aruanne **Tagasta kinnitus** pole süsteemis töölehele paigutatud või muul viisil registreeritud ja see pole tagastustellimuse protsessis vajalik etapp.

## <a name="replace-a-product"></a>Toote asendamine
Tooteasenduse haldamiseks on kaks meetodit.

-   **Esimene asendus** – asendage toode enne tagastatud toote kliendilt vastuvõtmist.
-   **Asendamine likvideerimiskoodiga** – looge automaatselt uus asendustellimuse rida.

### <a name="up-front-replacement"></a>Esimene asendus

Esimeses asenduses saab asenduskauba kliendile toimetada enne kauba tagastamist. See meetod on kasulik ka siis, kui kaup on masinaosa, mida ei saa eemaldada, välja arvatud juhul, kui selle asemele on võtta varuosa või kui soovite, et teie kliendil oleks asendustoode võimalikult kiiresti olemas. Esimene asendustellimus on sõltumatu müügitellimus. Päiseteave käivitatakse kliendi ja reateave tagastustellimuse kaudu. Asendustellimust saate redigeerida, töödelda ja kustutada tagastustellimusest sõltumatult. Asendustellimuse kustutamisel saate sõnumi, et tellimus loodi asendustellimusena. Järgmine illustratsioon näitab asendustellimuse protsessi.  

![Esimene asendusprotsess](./media/SalesReturn04.png)

Asendustellimus hõlmab viidet asendustellimusele. Kui esimene asendustellimus luuakse tagastustellimusele enne defektse kauba tagastamist, ei saa te pärast defektse kauba tagastamist asenduse jaoks likvideerimiskoode valida.

### <a name="replacement-by-disposition-code"></a>Asendamine likvideerimiskoodiga

Kui tarnite kliendile asenduskauba ja kasutate tagastustellimusel olevat likvideerimistegevust **Asenda ja kanna praaki** või **Asenda ja kanna kreeditisse**, kasutage järgmisel illustratsioonil näidatud protsessi.  

![Asendusprotsess likvideerimisprotsessi kasutamisel](./media/SalesReturn05.png)

Asenduskaup tarnitakse, kasutades sõltumatut müügitellimust ehk asendusmüügitellimust. See müügitellimus luuakse tagastustellimuse jaoks saatelehe loomisel. Tellimusepäis kasutab kliendilt teavet, millele viidatakse tagastustellimuse päises. Reateavet kogutakse teabest, mis sisestatakse lehel **Asenduskaup**. Leht **Asenduskaup** peab olema täidetud ridadele, millel on sõnaga „asendama” algavad likvideerimistegevused. Siiski pole asenduskauba kogus ega identiteet kinnitatud ega piiratud. See käitumine võimaldab juhtumeid, kus klient soovib sama kaupa, kuid erineva konfiguratsiooni või suurusega, aga ka juhtumeid, kus kliendid soovivad täiesti erinevat kaupa. Vaikimisi sisestatakse lehele **Asenduskaup** identne kaup. Siiski saate valida teise kauba, tingimusel, et funktsioon on seadistatud. 

>[Märkus.] Saate redigeerida ja kustutada asendusmüügitellimuse pärast selle loomist.

## <a name="generate-a-packing-slip"></a>Saatelehe loomine
Enne kui tagastatud kaupu saab varudesse vastu võtta, peate värskendama saatelehte tellimusele, millel kaubad kuuluvad. Nii nagu arve värskendamise protsess on finantskande värskendamine, on saatelehe värskendamisprotsess laokirje värskendamine. Teisiti öeldes kinnitab see protsess muudatused varudesse. Tagastuste korral rakendatakse likvideerimistegevuseks määratud etapid saatelehe värskendamise käigus. Saatelehe loomisel toimuvad järgmised sündmused.

-   Laos kasutatakse standardset protsessi füüsilise sissetuleku tegemiseks. Pearaamatusisestused luuakse siis, kui varude mudeligrupp (**Sisesta füüsiline ladu**) ja müügireskontro parameetrid (**Sisesta saateleht pearaamatusse**) on määratud sobivalt.
-   Kaubad, mis on tähistatud sõna „praak” sisaldavate likvideerimistegevusega, praagitakse ja varude kadu sisestatakse pearaamatusse.
-   Kaubad, mis on tähistatud likvideerimistegevusega **Tagasta kliendile**, võetakse vastu ja tarnitakse kliendile. Nendel kaupadel pole varudele mingit netoväärtuse mõju.
-   Luuakse asendusmüügitellimus. See müügitellimus põhineb lehel **Asenduskaup** esitatud teabel.

Saate luua saatelehe ainult ridadele, mille tagastusolek on **Registreeritud** ja ainult tagastusreal oleva täiskoguse jaoks. Kui mitmel tagastustellimuse real on olek **Registreeritud**, saate ridade alamkogumi jaoks luua saatelehe, kustutades lehelt **Saatelehe sisestamine** teised read. 

Osalised tagastused määratletakse tagastustellimuse ridade, mitte tagastustellimuse saadetiste tingimustel. See tähendab, et kui saate täiskoguse, mis on näidatud ühel tagastustellimuse real, kuid te ei saa midagi tagastustellimuse teistelt ridadelt, siis pole tarne osaline tarne. Kui tagastustellimuse rida nõuab 10 kauba ühiku tagastamist, kuid saate ainult neli ühikut, on tarne osaline tarne. Kui kõik oodatud tagastuskaubad pole saabunud, saate seada saadetise kõrvale ja oodata ülejäänud tagastatud koguse saabumist. Teise võimalusena saate registreerida ja sisestada osalise koguse. Osana saatelehtede sisestamise protsessist saate siduda kliendi saatmisdokumentidest pärineva saatelehe viitenumbri tellimuseridadega. See seos on valikuline ja ainult viitamiseks. See ei loo ühtki kandevärskendust. 

Üldiselt saate saatelehe protsessi vahele jätta ja minna otse arveldamisse. Sellisel juhul viiakse arveldamise käigus lõpule etapid, mida oleksite teinud saatelehe loomise käigus.

## <a name="generate-an-invoice"></a>Loo arve
Kuigi leht **Tagastustellimus** sisaldab teavet ja tegevusi, mis on vajalikud tagastustellimuste spetsiaalsete logistiliste aspektide käsitlemiseks, peate arveldusprotsessi lõpuleviimiseks kasutama lehte **Müügitellimus**. Teie organisatsioon saab seejärel arveldada samaaegselt tagastustellimused ja müügitellimused ning sama isik saab arveldusprotsessi vastavalt vajadusele lõpule viia. Lehel **Müügitellimus** tagastustellimuse vaatamiseks klõpsake seotud müügitellimuse avamiseks müügitellimuse numbri linki. Tagastustellimuse leiate ka lehelt **Kõik müügitellimused**. Tagastustellimused on müügitellimused, millel on tellimuse tüüp **Tagastatud tellimus**.

### <a name="credit-correction"></a>Kreediti parandus

Osana arvaldamisprotsessist kontrollige, kas mis tahes muud tasud on õiged. Pearaamatu sisestuste parandusteks (storno) muutumiseks kaaluge arve/kreeditarve sisestamisel lehel **Arve sisestamine** oleva vahekaardi **Muu** suvandi **Kreediti parandus** kasutamist arve/kreeditarve sisestamisel. 
>[Märkus.] Vaikimisi aktiveeritakse suvand **Kreediti parandus** siis, kui **Kreeditarve kui parandus** lehel **Müügireskontro parameetrid** on lubatud. Soovitame teil tagastusi stornoga mitte postitada.

## <a name="create-intercompany-return-orders"></a>Kontsernisiseste tagastustellimuste loomine
Tagastustellimused saab teie organisatsioonisiseselt kahe ettevõtte vahel lõpule viia. Toetatud on järgmised stsenaariumid.

-   Lihtsad kontsernisisesed tagastused kahe kontsernisiseses suhtes osaleva ettevõtte vahel.
-   Tagastustellimuse loomisel loodav kontsernisisene kett luuakse müügiettevõttes.
-   Hankija tagastustellimuse loomisel loodav kontsernisisene kett luuakse ostuettevõttes.
-   Otsetarne saadetise tagastused väliskliendi ja kahe kontsernisiseses seoses osaleva ettevõtte vahel.

### <a name="setup"></a>Häälestus

Järgmine näide illustreerib minimaalset seadistust, mis on vajalik kahe ettevõtte jaoks kontsernisiseses suhtes osalemiseks ja kontserni kaubavahetuse eeliste kasutamiseks.  

![Minimaalne seadistus](./media/SalesReturn06.png)

Järgmises stsenaariumis on CompBuy ostu- ja CompSell müügiettevõte. Tavaliselt tarnib ettevõtte kaubad ostuettevõttesse või otsetarne saadetise stsenaariumites otse lõppkliendile. CompBuys on hankija IC\_CompSell määratletud kontsernisisese lõpp-punktina, mis on seotud ettevõttega CompSell. Samaaegselt on CompSellis klient IC\_CompBuy määratletud kontsernisisese lõpp-punktina, mis on seotud ettevõttega CompBuy. Mõlemas ettevõttes peavad olema määratletud sobivad tegevuspoliitika üksikasjad ja väärtuste vastendused. Otsetarne saadetise stsenaariumis luuakse müügiettevõttes kontsernisisene tagastustellimus, mis on ka kontsernisisene müügitellimus. Kontsernisisese tagastustellimuse tagastuse numbri saab CompSellis valida tagastuse numbriseeriast või selle saab kopeerida tagastuse numbrilt, mis on CompBuys algsele tagastustellimusele määratud. Neid tegevusi määrab tegevuspoliitikas **PurchaseRequisition** olevad tagastuse numbri sätted. Tagastuse numbri sünkroonimisel peate tegema plaani numbri kokkupõrgete ohu vähendamiseks olukorras, kus kaks ettevõtet kasutavad sama numbrijada.

### <a name="simple-intercompany-returns"></a>Lihtsad kontsernisisesed tagastused

See stsenaarium hõlmab samas organisatsioonis kaht ettevõtet, nagu on näidatud järgmises näites.  

![Lihtne kontsernisisene tagastus](./media/SalesReturn07.png)

Tellimusahela saab luua, kui ostuettevõttes luuakse hankija tagastustellimus või müügiettevõttes luuakse kliendi tagastustellimus. Teises ettevõttes luuakse vastav tellimus ja tagatakse, et hankija tagastustellimuse päise ja rea teave kajastaks kliendi tagastusreal olevaid sätteid. Loodav tagastustellimus võib olemasolevale kliendiarvele viidet lisada või seda välistada (**Otsi müügitellimust**). Kahe tellimuse saatelehti ja arveid saab individuaalselt töödelda. Näiteks ei pea te looma saatelehte hankija tagastustellimuse jaoks enne kliendi tagastustellimuse jaoks saatelehe loomist.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Otsetarne saadetise tagastused kolme osapoole hulgas

Selle stsenaariumi saab luua, kui tüübi **Otsetarne** varasem müük on lõpule viidud ja kui ettevõttes, kes suhtleb kliendiga, eksisteerib kliendi suhtes arve. Järgmisel illustratsioonil on ettevõtte CompBuy tooted varasemalt kliendile Väline müünud ja arveldenud. Tooted lähetati kliendile otse ettevõttest CompSell kontsernisisese tellimusahela kaudu.  

![Otsetarne saadetise tagastused kolme osapoole vahel](./media/SalesReturn08.png)

Kui klient Väline soovib tooteid tagastada, luuakse kliendi jaoks ettevõttes CompBuy tagastustellimus (RMA02). Kontsernisisese keti loomiseks peab tagastustellimus olema märgitud otsetarne jaoks. Funktsiooni **Otsi müügitellimust** kasutamisel tagastusele kliendiarve valimiseks luuakse kontsernisisene tellimusahel, mis koosneb järgmistest dokumentidest.

-   **Algne tagastustellimus:** RMA02 (ettevõte CompBuy)
-   **Ostutellimus:** PO02 (ettevõte CompBuy)
-   **Kontsernisisene tagastustellimus:** RMA\_00032 (ettevõte CompSell)

Pärast otsetarne kontsernisisese keti loomist peab kogu tagastuste füüsiline käsitsemine ja töötlemine toimuma ettevõttes CompSell kontsernisisese tagastustellimuse RMA\_00032 kontekstis. Tooteid ei saa ettevõttes CompBuy vastu võtta. Likvideerimiskoodi määramisel kontsernisisesele tagastustellimusele sünkroonitakse see algse tagastustellimusega, et lubada algse tellimuse õige arveldamine.

## <a name="post-to-the-ledger"></a>Pearaamatusse sisestamine
Tagastustellimuse arveldamisel loodavaid pearaamatu sisestusi mõjutavad mõned olulised sätted ja parameetrid.

-   **Tagastamise omahind** – laomudelite puhul, mis ei ole **Standardne omahind**, määrab parameeter **Tagastamise omahind** kauba kulu selle aktsepteerimisel tagasi varudesse või väljapraakimisel. Varude õige hindamise arvutamiseks on oluline parameeter **Tagastamise omahind** õigesti määrata. Kui kasutate tagastustellimuse rea loomiseks funktsiooni **Otsi müügitellimust**, millel on viide kliendiarvele, on väärtus **Tagastamise omahind** võrdne müüdava kauba kuluhinnaga. Muul juhul tuleneb kuluhinna väärtus kaubaseadistusest või selle saab sisestada käsitsi.
-   **Kreediti parandus / storno** – parameeter **Kreediti parandus** lehel **Arve sisestamine** määrab, kas sisestused tuleb salvestada positiivsete (DR/CR) kirjete või korrigeerivate, negatiivsete kirjetena.

Järgnevates näidetes tähistatakse tagastamise omahind kui **Lao omahind**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Näide 1. Tagastustellimus ei viita kliendiarvele

Tagastustellimus ei viita kliendiarvele. Tagastatud kaup krediteeritakse. Parameetrit **Kreediti parandus** ei valita tagastustellimuse arve või kreeditarve loomisel.  

![Tagastustellimus ei viita kliendiarvele](./media/SalesReturn09.png)  

>[Märkus.] Kauba põhihinda kasutatakse parameetri **Tagastamise omahind** vaikeväärtusena. Vaikehind erineb lao väljamineku ajal omahinnast. Seetõttu on mõju see, et 3 kadu on kuludesse kantud. Täiendavalt ei hõlma tagastustellimus allahindlust, mis anti kliendile müügitellimusel. Seetõttu esineb üleliigset krediiti.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Näide 2. Tagastustellimuse jaoks valitakse kreediti parandus.

Näide 2 on sama mis näide 1, kuid parameeter **Kreediti parandus** valitakse tagastustellimuse arve loomisel.  

![Tagastustellimus krediiditäpsustuse valimisel ](./media/SalesReturn10.png)  

>[Märkus.] Pearaamatu sisestused sisestatakse negatiivsete parandustena.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Näide 3. Tagastustellimuse rea loomiseks kasutatakse funktsiooni Otsi müügitellimust.

Selles näites kasutatakse tagastustellimuse rea loomiseks funktsiooni **Otsi müügitellimust**. Parameetrit **Kreediti parandus** ei valita arve loomisel.  

![Tagastustellimuse rida, mis luuakse funktsiooni Otsi müügitellimust kasutades ](./media/SalesReturn11.png)  

>[Märkus.] **Allahindlus** ja **Tagastamise omahind** on korrektselt seatud. Seetõttu toimub kliendiarve täpne tühistamine.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]