---
title: "Saabumise ülevaade"
description: "Selles teemas kirjeldatakse funktsiooni saabumisülevaade. Saabumisülevaate leht on selle funktsiooni osa ja annab ülevaate kõikidest kaupadest, mille saabumist sissetuleva kaubana eeldatakse."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c1b6077ac32b6a7c30f9d9c9d0fa0eb93cf63bf6
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="arrival-overview"></a>Saabumise ülevaade

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse funktsiooni saabumisülevaade. Saabumisülevaate leht on selle funktsiooni osa ja annab ülevaate kõikidest kaupadest, mille saabumist sissetuleva kaubana eeldatakse.

Leht **Saabumisülevaade** annab ülevaate kõikide eeldatute sissetulevate kaupade kohta. Samuti näitab see saabumisi, mida saab lähtestada ülevaate põhjal. Selles teemas käsitletakse vastuvõtmisprotsessi.

## <a name="business-scenario"></a>Äristsenaarium
Kaaluge järgmist sissetulevate protsesside stsenaariumit. 

[![Äristsenaarium](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png) 

Vastuvõtuametnik Sammy soovib teada, mille saabumist eeldatakse jooksval päeval. Lehel **Saabumisülevaate** näeb Sammy praeguste ülesannete ülevaadet ja ligikaudset hinnangut tellimuste koguse, mahu, kaalu, tüübi ja muude kohta. Hiljem saabub saabumisalale tarne ja Sammy saab tarne loendi. Lehel **Saabumisülevaade** saab Sammy sooritada järgmisi toiminguid.

-   Tuvastada vastav sissetulekuorder ja registreerida sissetulek olekusse **Pooleli**. Registreerimiseks vajalikud read luuakse automaatselt ja sissetulekut saab jälgida, isegi kui kanded pole veel sisestatud olekusse **Registreeritud**.
-   Pääseda juurde vastavale saabumistöölehe viitele (st töölehele **Kauba saabumine** või töölehele **Materjalid tootmisse**) ja tuvastada töölehed, mis on toote sissetuleku värskenduseks valmis.

## <a name="arrival-overview-page"></a>Saabumisülevaate leht
Lehe **Saabumisülevaade** avamiseks klõpsake valikuid **Varude haldus** &gt; **Sissetulevad tellimused** &gt; **Saabumisülevaade**. Saate vaadata eeldatud saadavate tellimuste loendit. Ülevaade jaguneb päiseks ja ridadeks. Päise teave on rühmitatud tellimuse tüübi, eeldatud vastuvõtukuupäeva ja tarne sihtkohta järgi. Kui päiserida on sissetulekuks valitud, siis on lehe rea üksikasjade osas kõik sissetuleku viitega seotud üksikasjaread sissetulekuks valitud. Kui kõik seotud töölehe read on sisestatud, siis seda teavet ei kuvata.

### <a name="arrival-overview-profiles"></a>Saabumisülevaate profiilid

Leht **Saabumisülevaade** annab ülevaate kaupadest, mille saabumist eeldatakse, ja nende saabumise eeldatavast kuupäevast. Saabumisprotsessi osana saab kasutada mitut isiklike sätete komplekti. Iga kasutaja saab määratleda oma isiklikud sätted lehel **Saabumisülevaate profiilid**.

### <a name="set-up-item-arrival"></a>Kauba saabumise häälestamine

Selles näites soovib Sammy üles seada uut arvutit asukohas, mida kasutatakse edaspidi tegevuskoha 1 tootmisest saadetud lõpetatud kaupade vastuvõtmiseks. Sammy loob lehel **Saabumisülevaate profiilid** uue häälestuse nimega **Tegevuskoha 1 tootmine** ja täpsustab järgmisi sätteid.

1.  Sisestage kiirkaardil **Saabumisvalikud**, mis asub väljarühmas **Vahemik**, teavet päevaintervalli kohta ja laod, mida ülevaatesse kaasata.
2.  Sisestage kiirkaardil **Saabumisvalikud**, mis asub väljarühmas **Tööleht**, vastuvõttev ladu, asukoht ja töölehe nimi (kauba saabumine / materjalid tootmisse).
3.  Sisestage kiirkaardil **Saabumispäringu üksikasjad**, mis asub väljarühmas **Tegevuskoht** väljal **Piira tegevuskohaga**, tegevuskoht, millega piirata ülevaate ala kuvamist.
4.  Määrake kiirkaardil **Saabumispäringu üksikasjad**, mis asub väljarühmas **Kuvatavad kandetüübid**, suvand **Tootmistellimused** olekusse **Jah**.
5.  Määrake kiirkaardil **Saabumispäringu üksikasjad**, mis asub rühmas **Muud**, suvand **Värskenda käivitamisel** olekusse **Jah**, kui vaadet peaks käivitamisel automaatselt värskendama. Määrake suvand **Värskenda vahemiku muutmisel** olekusse **Jah**, kui vaadet peaks vahemiku väärtuste muutmisel automaatselt värskendama.

Selles näites on väli **Saabumisülevaate profiili nimi**, mis asub lehe **Saabumisülevaade** kiirtahvlil **Saabumisvalikud**, seatud olekusse **Tegevuskoha 1 tootmine**.

### <a name="prerequisites-for-arrival-journals"></a>Saabumistöölehtede eeltingimused

Saabumistöölehtede automaatseks loomiseks lehelt **Saabumisülevaade** peate määratlema asjakohast teavet kiirkaardi **Saabumisvalikud** väljarühmas **Tööleht**.

-   Töölehe loomiseks peate määrama töölehele nime. 

[![Töölehe nime määramine](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Kui määrate väärtuseid väljadel **Ladu** ja **Asukoht**, siis need väärtused rakendatakse töölehe ridadele. Kui te ei määra väärtusi, siis kasutab süsteem väärtusi dimensioonist, mis on määratud laokannetel.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Kaubad, mis on saadud ühelt eeldatud sissetulekuorderilt

Sammy valib kiirkaardil **Sissetulekud** rea ja klõpsab seejärel nuppu **Alusta saabumistöölehte**. Kõik seotud read, mis on määratud vahemikus ja millel on registreeritav kogus, on automaatselt valitud. Luuakse kauba saabumistööleht, millel on vastendus eeldatud sissetulekuorderi ja töölehe vahel. Kogus lähtestatakse automaatselt kõigil ridadel, mis on loodud.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Kaubad, mis on saadud enam kui ühelt eeldatud sissetulekuorderilt

Sammy valib kiirkaardil **Sissetulekud** mitu rida ja klõpsab seejärel nuppu **Alusta saabumistöölehte**. Luuakse kauba saabumistööleht, millel on vastendus kõikide eeldatud sissetulekuorderite ja töölehe vahel. Kõik read luuakse ühe kauba saabumistöölehe päises ja kogus lähtestatakse automaatselt.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Kaupade saamine ühelt või enamalt eeldatud sissetulekuorderilt

#### <a name="view-information"></a>Teabe vaatamine

Teatud kuupäevaintervallis eeldatud sissetulekute kohta ülevaate saamiseks sisestab Sammy järgmise teabe väljadele lehe **Saabumisülevaade** kiirkaardil **Saabumisvalikud** ja klõpsab seejärel nuppu **Värskenda**, et vaadet värskendada.

-   Saabumisülevaate profiili nimi: **Päring**
-   Kuva read: **Kõik**
-   Päeva tagasi: (tühi)
-   Päeva edasi: **0**
-   Laod: **GW, MW**

Sammy saab vaadata järgmist teavet.

-   Kõiki seotud sissetulekuordereid süsteemikuupäeva ja sealt tagasi lõpmatu arvu päevade kohta (intervall **InventTrans.StatusDate**) ning sissetulekuid ladudesse GW ja MW, olekust sõltumata.
-   Rohkem kui ühe tellimuse rea üksikasjalikku teavet. Sammy saab ülevaates valida mitu päiserida ja klõpsata seejäral nuppu **Kuva kõik valitud**, et kuvada kõikide valitud tellimuste koha vastavat rea üksikasjalikku teavet.
-   Teavet konkreetse ostutellimuse kohta. Kui Sammy tahab kuvada ainult teavet, mis on ülevaates seotud kindla viitenumbriga, saab ta sisestada kontonumbri väljale **Kontonumber** ja tellimuse numbri väljale **Viitenumber**.
-   Kõikide tellimusridade jaoks, millele on loodud kauba saabumistööleht, kuid mida pole veel sisestatud, loodi ülevaade töötlemist vajavate registreerimistoimingute jaoks. Sammy saab selle teabe vaatamiseks valida oleku **Pooleli** väljal **Kuva read**.

### <a name="update-journals"></a>Töölehtede värskendamine

Ühe või mitme töötlemist vajavate tellimusridade registreerimiseks saab Sammy valida ridasid ülevaateruudustikus või rea ruudustikus ja klõpsata valikuid **Töölehed** &gt; **Kuva sissetulekute saabumistöölehed**. Kuvatakse saabuva kauba päiseid, mis vastavad ridadele. Registreeritud kaupade ostutellimuse toote sissetuleku värskendamiseks pääseb Sammy juurde saabuva kauba töölehe päistele, mis on värskendamiseks valmis. Kauba saabumise töölehe päistele juurde pääsemiseks klõpsab ta valikuid **Töölehed** &gt; **Toote sissetuleku valmis töölehed**. Kuvatakse kõiki määratud laovahemikus toote sissetuleku värskenduseks valmis olevaid päiseridasid. (Kuvatavad päiseread ei ole seotud päevaintervalliga).

### <a name="start-an-arrival-registration"></a>Saabumise registreerimise alustamine

Sammy saab alustada rohkem kui ühe sissetuleku viite saabumist, kui valib lehel **Saabumisülevaade** mitu rida. Kui ta valib sissetulekute ülevaatest rea, siis valitakse vastavad rea üksikasjad. Kui registreerimiseks on olemas kogus, siis on nupp **Alusta saabumistöölehte** saadaval. Sammy saab saabumise registreerimise alustamiseks kasutada kahte meetodit.

-   Lehe filtreerimiseks nii, et see kuvab ainult teatud kriteeriumitele vastavaid kirjeid, skannige väljas **Hankija viide** hankijalt viitenumber, nt tarneteate vöötkood.
-   Valige käsitsi või tühistage saabumise registreerimise kirjete valik lehe **Saabumisülevaade** ülevaate või üksikasjade osas. Seejärel, kui Sammy klõpsab nuppu **Alusta saabumistöölehte**, luuakse valitud kirjed automaatselt kauba saabumistöölehel. Kirjed sisaldavad reateavet ja määratakse kõik välja kordumatu teave.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Saabumisteabe värskendamine ja toote sissetuleku töötlemine
Kui kõik kaubad on registreeritud, saab laojuhataja või ostujuht värskendada saatelehega saabunud kaupu, et neile füüsiline kulu lisada. Saabumisteabe värskendamiseks ja toote sissetuleku sisestamiseks toimige järgmiselt.

1.  Klõpsake valikuid **Varude haldus** &gt; **Sissetulevad tellimused** &gt; **Saabumisülevaade**.
2.  Klõpsake lehel **Saabumisülevaade** valikuid **Töölehed** &gt; **Toote sissetuleku valmis töölehed**, et kuvada loendit töölehtedest, mis on toote sissetuleku värskenduseks valmis.
3.  Valige töölehed, mida tuleb värskendada ja klõpsake seejärel valikuid **Funktsioonid** &gt; **Toote sissetulek**.
4.  Sisestage lehel **Sisestamine** toote sissetuleku number, kui seda pole juba töölehel olemas, ja klõpsake nuppu **OK**, et töödelda toote sissetulekut.

## <a name="summary"></a>Kokkuvõte
Leht **Saabumisülevaade** annab laojuhatajale ja laotöölistele ülevaate eeldatava töö kohta, mida tuleb sissetulekute protsessi käigus teha. Seda lehte saab kasutada ka kauba saabumisprotsessi käivitamiseks, et tagada kaupade jälgimist esimesel lattu sisenemisel.




