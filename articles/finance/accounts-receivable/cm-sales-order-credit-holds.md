---
title: Müügitellimuste krediidi ootelolekud
description: See teema kirjeldab nende reeglite seadistust, mida kasutatakse müügitellimuse krediidi ootele panemiseks.
author: mikefalkner
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d94b19061838f9bb2552c3c91c6b3591040ccf52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827646"
---
# <a name="credit-holds-for-sales-orders"></a>Müügitellimuste krediidi ootelolekud
[!include [banner](../includes/banner.md)]

See teema kirjeldab nende reeglite seadistust, mida kasutatakse müügitellimuse krediidi ootele panemiseks. Krediidihalduse blokeerimise reegleid saab rakendada üksikule kliendile või klientide grupile. Blokeerimise reeglid määratlevad vastuseid järgmistele asjaoludele.

1. Ületatud päevade arv
2. Kontode olek
3. Maksetingimused
4. Krediidilimiit on aegunud
5. Tähtaja ületanud summa
6. Müügitellimuse summa
7. Saadaoleva krediidi kasutatud osa

Lisaks on kaks parameetrit, mis juhivad täiendavaid müügitellimust blokeerivaid stsenaariume

1. Muutus maksetingimustes
2. Muutus tasakaalustuse allahindlustes

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Blokeerimise reeglite ja välistuse reeglite seadistamine

Kui klient algatab müügikande, vaadatakse müügitellimuse teave üle blokeerimise reeglite kogumi suhtes, mis juhivad otsust selle kohta, kas lubada kliendile krediiti ja lubada müügil edasi liikuda. Saate määratleda ka välistused, mis tühistavad blokeerimise reeglid ja lubavad müügitellimuse töötlemist. Saate seadistada blokeerimise reeglid ja välistamise reeglid lehel **Krediidihaldus > Seadistus > Krediidihalduse seadistus > Blokeerimise reeglid**.

### <a name="days-overdue"></a>Tähtaja lõppemisest möödunud päevade arv

Avage vahekaart **Ületatud päevad**, kui blokeerimise reegel rakendub kliendile, kellel on üks või mitu teatud arv päevi tähtaja ületanud arvet.
1. Valige kliendi vahemik, millele see reegel **Kehtib**.
   - Valige **Tabel**, kui reegel rakendub kindlale kliendile.
   - Valige **Grupp**, kui reeglit rakendatakse kliendigrupi tasemel. 
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele.
2. Kui olete vahemiku määratlenud, peate määrama **Konto/grupi**, mida selles vahemikus kasutatakse.
   - Vahemiku **Tabel** korral annab otsing valimiseks klientide loendi. 
   - Valige **Grupp**, kui reegel rakendub kliendi krediidigrupile.
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele. 
3. Valige **Riskirühm**, et kasutada krediidiriski halduse ooteloleku kriteeriumi rakendamist klientidele, kes on rühmitatud ühise tegurite komplekti põhjal, nt reitingute Dun ja Bradstreet põhjal, tegutsemisaastate arvu, kliendiks olemise aja põhjal jne.  
4. Valige seadistatava reegli tüüp. **Blokeerimise** suvand loob reegli, mis blokeerib tellimuse. **Välistamise** suvand loob reegli, mis välistab teise reegli poolt tellimuse blokeerimise. 
5. Valige **Väärtuse tüüp**. Vaikimisi kirje on fikseeritud päevade arv. Kui loote välistamise, saate määrata selle asemel fikseeritud päevade arvu või summa. 
6. Sisestage **Tähtaja ületanud** päevade arv, mis valitud blokeerimise reegli jaoks lubatakse, enne kui tellimus pannakse läbivaatamiseks krediidiriski haldusega seotud ootelolekusse. Tähtaja ületanud päevade arv kujutab endast täiendavat ajapikenduse päevade arvu, mis lisatakse maksetähtaega ületanud päevade arvule, mis arvel enne tähtaja ületanuks pidamist olla võib. Kui määrasite **Väärtuse tüübiks** välistamise summa, siis sisestage see summa ja summa valuuta.

### <a name="accounts-status"></a>Kontode olek

Avage vahekaart **Konto olek**, kui blokeerimise reegel kehtib valitud konto olekuga kliendile.
1. Valige seadistatava reegli tüüp.  **Blokeerimine** loob reegli, mis blokeerib tellimuse. **Välistamine** loob reegli, mis välistab teise reegli poolt tellimuse blokeerimise. 
2. Valige **Konto olek**, mille põhjal paneb reegel müügitellimuse ootele või välistab selle.

### <a name="terms-of-payment"></a>Maksetingimused

Valige **Maksetingimused**, kui blokeerimise reegel rakendub valitud maksetingimustele.
1. Valige seadistatava reegli tüüp.  **Blokeerimine** loob reegli, mis blokeerib tellimuse. **Välistamine** loob reegli, mis välistab teise reegli poolt tellimuse blokeerimise. 
2. Valige **Maksetingimused**, mille põhjal paneb reegel müügitellimuse ootele või välistab selle.

### <a name="credit-limit-expired"></a>Krediidilimiit on aegunud

Kui blokeerimise reegel rakendub aegunud krediidilimiidiga klientidele, avage vahekaart **Krediidilimiit aegunud**.
1. Valige kliendi vahemik, millele see reegel **Kehtib**.
   - Valige **Tabel**, kui reegel rakendub kindlale kliendile.
   - Valige **Grupp**, kui reeglit rakendatakse kliendigrupi tasemel. 
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele.
2. Kui olete vahemiku määratlenud, peate määrama **Konto/grupi**, mida selles vahemikus kasutatakse.
   - Vahemiku **Tabel** korral annab otsing valimiseks klientide loendi. 
   - Valige **Grupp**, kui reegel rakendub kliendi krediidihalduse grupile.
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele. 
3. Valige **Riskigrupp**, et piirata veelgi nende klientide loendit, kes pannakse krediidihaldusega seotult ootele. 
4. Valige seadistatava reegli tüüp. 
   - Valige **Blokeerimine**, et luua reegel, mis blokeerib tellimuse. 
   - Valige **Välistamine**, et luua reegel, mis välistab teise reegli poolt tellimuse blokeerimise. 
5. Sisestage valitud blokeerimise reeglile enne krediidihaldusega seotud ootelolekusse panemist väärtus **Päevi krediidilimiidi aegumisest**. Tähtaja ületanud päevade arv tähistab täiendavat ajapikendust, mis lisatakse krediidilimiidi aegumisest möödunud päevade arvule.

### <a name="overdue-amount"></a>Tähtaja ületanud summa

Kui blokeerimise reegel kehtib tähtaja ületanud summadega klientidele, avage vahekaart **Tähtaja ületanud summa**.
1. Valige kliendi vahemik, millele see reegel **Kehtib**.
   - Valige **Tabel**, kui reegel rakendub kindlale kliendile.
   - Valige **Grupp**, kui reeglit rakendatakse kliendigrupi tasemel. 
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele.
2. Kui olete vahemiku määratlenud, peate määrama **Konto/grupi**, mida selles vahemikus kasutatakse.
   - Vahemiku **Tabel** korral annab otsing klientide otsingu. 
   - Valige **Grupp**, kui reegel rakendub kliendi krediidihalduse grupile.
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele. 
3. Valige **Riskigrupp**, kui soovite piirata veelgi nende klientide loendit, kes pannakse krediidihaldusega seotult ootele. 
4. Valige seadistatava reegli tüüp. 
   - Valige **Blokeerimine**, et luua reegel, mis blokeerib tellimuse. 
   - Valige **Välistamine**, et luua reegel, mis välistab teise reegli poolt tellimuse blokeerimise. 
5. Sisestage valitud blokeerimise reeglile enne krediidihaldusega seotud ootelolekusse ülevaatamiseks panemist väärtus **Tähtaja ületanud summa**. 
6. Valige **Väärtuse tüüp**, mis määratleb selle väärtuse tüübi, mida kasutatakse testimiseks, kui palju krediidilimiidist on ära kasutatud. Blokeerimise reeglid nõuavad protsenti, kuid välistamisel võib olla kas fikseeritud summa või protsent. Lävi on seotud krediidilimiidiga.
7. Sisestage valitud reegli jaoks väärtus **Krediidilimiidi lävi** enne, kui klient läheb krediidihaldusega seotult ootele. See võib olla summa või protsent, mis põhineb väärtuse tüübi all valitud väärtuse tüübist.
8. Reegel kontrollib, kas **Tähtaja ületatud summa** on ületatud ja **Krediidilimiidi lävi** on ületatud. 

### <a name="sales-order"></a>Müügitellimus 

Valige **Müügitellimus**, kui blokeerimise reegel rakendub müügitellimuse väärtusele.
1. Valige kliendi vahemik, millele see reegel **Kehtib**.
   - Valige **Tabel**, kui reegel rakendub kindlale kliendile.
   - Valige **Grupp**, kui reeglit rakendatakse kliendigrupi tasemel. 
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele.
2. Kui olete vahemiku määratlenud, peate määrama **Konto/grupi**, mida selles vahemikus kasutatakse.
   - Vahemiku **Tabel** korral annab otsing klientide otsingu. 
   - Valige **Grupp**, kui reegel rakendub kliendi krediidihalduse grupile.
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele. 
3. Valige **Riskigrupp**, kui soovite piirata veelgi nende klientide loendit, kes pannakse krediidihaldusega seotult ootele. 
4. Valige seadistatava reegli tüüp.  
   - Valige **Blokeerimine**, et luua reegel, mis blokeerib tellimuse. 
   - Valige **Välistamine**, et luua reegel, mis välistab teise reegli poolt tellimuse blokeerimise. 
5. Sisestage valitud blokeerimise reeglile enne krediidihaldusega seotud ootelolekusse panemist väärtus **Müügitellimuse summa**. 

Müügitellimuse reegel sisaldab täiendavat sätet, mis tühistab kõik muud reeglid. Sellise välistamise loomiseks, mis vabastab müügitellimuse, võtmata arvesse muid reegleid, valige välistuse rea märkeruut **Vabasta müügitellimus**.

### <a name="credit-limit-used"></a>Krediidilimiit on kasutatud

Kui blokeerimise reegel rakendub kliendi kasutatud krediidilimiidi summale, valige **Kasutatud krediidilimiit**.
1. Valige kliendi vahemik, millele see reegel **Kehtib**.
   - Valige **Tabel**, kui reegel rakendub kindlale kliendile.
   - Valige **Grupp**, kui reeglit rakendatakse kliendigrupi tasemel. 
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele.
2. Kui olete vahemiku määratlenud, peate määrama **Konto/grupi**, mida selles vahemikus kasutatakse.
   - Vahemiku **Tabel** korral annab otsing klientide otsingu. 
   - Valige **Grupp**, kui reegel rakendub kliendi krediidihalduse grupile.
   - Valige **Kõik**, kui reegel rakendub kõigile klientidele. 
3. Valige **Riskigrupp**, kui soovite piirata veelgi nende klientide loendit, kes pannakse krediidihaldusega seotult ootele. 
4. Valige seadistatava reegli tüüp.
   - Valige **Blokeerimine**, et luua reegel, mis blokeerib tellimuse. 
   - Valige **Välistamine**, et luua reegel, mis välistab teise reegli poolt tellimuse blokeerimise. 
5. Valige **Allesolev lävi**, mis määratleb krediidilimiidi protsendi, mis blokeerib müügitellimuse. Kui tellimuse väärtus suurendab kasutatud krediidilimiidi summat üle selle protsendi, pannakse tellimus ootele. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Müügitellimuse ootele panemine teiste kriteeriumide alusel
  
### <a name="rank-payment-terms"></a>Maksetingimuste hindamine  

Maksetingimuste muutmisel saate jõustada kreeditijuhtimise reeglite käivitamise. Peate maksetingimused järjestama ja määrama neile astmeväärtuse. Kui muudate tellimuse maksetingimusi nendeks maksetingimusteks, millel on kõrgem aste kui vanadel maksetingimustel, saadetakse tellimus krediidihaldusse ja see nõuab kinnitamist.

Maksetingimuste järjestused saate seadistada lehel **Krediidihaldus > Seadistus > Krediidihalduse seadistus > Maksetingimuste järjestamine**.

1. Järjestamiseks valige maksetingimused väljal **Maksetingimused**, kui valite tingimuse, kuvatakse selle kirjeldus väljal **Kirjeldus**.
2. Valige tingimuse aste väljal **Aste**. Väärtused on kõik teineteisega seotud, nii et saate kasutada 1, 2, 3 või 10, 20, 30. Sama väärtust saate kasutada ka enamiku maksetingimuste puhul, nii et kreeditikontroll käivitatakse ainult ühe või kahe maksetingimustega.

### <a name="rank-settlement-discounts"></a>Tasakaalustuse allahindluste hindamine   

Tasakaalustuste allahindluste muutmisel saate jõustada kreeditijuhtimise reeglite käivitamise. Peate tasakaalustuste allahindlused järjestama ja määrama neile astmeväärtuse. Kui muudate tellimuse tasakaalustuste allahindlusi nendeks tasakaalustuste allahindlusteks, millel on kõrgem aste kui vanadel tasakaalustuste allahindlustel, saadetakse tellimus krediidihaldusse ja see nõuab kinnitamist.

Maksetingimuste järjestused saate seadistada lehel **Krediidihaldus > Seadistus > Krediidihalduse seadistus > Tasakaalustuste allahindluste järjestamine**.

1. Valige see **Skonto**, mida soovite järjestada. Kuvatakse tasakaalustuste allahindluse **Kirjeldus**.
2. Valige **Astme** väärtus. Väärtused on kõik teineteisega seotud, nii et saate kasutada 1, 2, 3 või 10, 20, 30. Sama väärtust saate kasutada ka enamiku tasakaalustuste allahindluste korral, nii et kreeditikontroll käivitatakse ainult ühe või kahe tasakaalustuste allahindlusega.

## <a name="sequence-the-application-of-rules"></a>Reeglite kohaldamise järjestus

Reeglid käivitatakse kindlas järjestuses, mille muudate vastavalt oma organisatsiooni vajadustele. 

- Üks müügitellimuse välistamise reeglite eksemplar võimaldab teil tühistada kõik reeglid, mis võivad müügitellimuse blokeerida. Looge müügitellimuse välistamise reegel ja märkige suvand **Vabasta müügitellimus**. Tellimust ei panna ootele, kui see välistamise reegel on tõene ja teisi reegleid ei kontrollita.
- Blokeerimise reeglid võivad tellimuse ootele panna.
- Välistamise reeglid käivitatakse pärast blokeerimise reegleid. Välistamise reeglid mõjutavad ainult reeglit, millel need on määratletud. 
- Blokeerimise ja välistamise reeglid käivitatakse tabelis, seejärel grupis, seejärel kogu tellimuse juures. Selle töötlemise järjekorra tõttu on võimalik, et Kõigi tasemel on blokeerimise reegel, mida ei käitata, kuna käivitatakse tabeli või grupi taseme välistamise reegel.
- Välistused ei tühista blokeerimise reeglit, kui need on samal tasemel. Näiteks grupi tasemel välistamise reegel ei tühista grupi tasemel blokeerimise reeglit. Te ei pea seadistama välistusi tasemel Kõik, välja arvatud ülalmainitud müügitellimuse ühe eksemplari välistamise reegli korral. 

Reegli **Kasutatud krediidilimiit** käitumine muutub vastavalt Krediidi ja võlanõuete parameetrivormil oleva parameetri **Kontrolli müügitellimuse krediidilimiiti** seadistustele.
- Kui parameetri väärtuseks on seatud eEi, siis kasutatud krediidilimiidi reeglit ei käivitata.
- Kui parameetri väärtuseks on seatud Jah ja kui **Teata krediidilimiidi ületamisel** on seadistatud hoiatuse peale, saate krediidilimiidi ületamisel hoiatuse. Käivitatakse **Kasutatud krediidilimiidi** reeglid, et näha, kas teil on reegleid, mida soovite käivitada. Kuid selle stsenaariumi puhul te tavaliselt reegleid ei lisa.
- Kui parameetri väärtuseks on seatud Jah ja kui **Teata krediidilimiidi ületamisel** on seadistatud tõrke peale, kontrollitakse krediidilimiiti ja kui krediidilimiit on ületatud, pannakse tellimus ootele. Lisaks käivitatakse **Kasutatud krediidilimiidi** reeglid, et näha, kas on täiendavaid reegleid, mis tuleks käivitada. Tõrketeadet ei kuvata, kuid kuvatakse blokeerimise põhjus **Krediidilimiit ületatud**. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Sätted, mis muudavad tellimuse ootele paigutamise viisi

Tellimusi saab krediidihaldusest välja jätta isegi juhul, kui on olemas reeglid. 

- Kui muudate sätted **Eemalda klient krediidihaldusest** jaotises **Kõik kliendid > Vali klient > kiirvahekaart Krediit ja võlanõuded** väärtusele **Jah**, siis ei töödelda selle kliendi ühtegi tellimust
- Kui muudate väärtuse **Välista krediidihaldusest** jaotise **müügitellimuse päis** kiirkaardil **Krediidihaldus** väärtusele **Jah**, siis ei töödelda krediidihalduse reegleid. Seda sätet saab teha ainult krediidiametnik või krediidihaldur.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Ootel tellimuste töötlemine, kasutades krediidihalduse ootelepaneku loendit

Krediidi halduse ootelepaneku loend laseb krediidihalduritel vaadata kõiki müügitellimusi, mis on paigutatud ootele, ja laseb neil eemaldada ootelepanekuid, kui krediidiprobleemid on lahendatud. Leht **Krediidihalduse ootelepaneku loend** kuvab kõiki müügitellimusi, mis on ootele pandud. Saate ootelepaneku loendit vaadata lehel **Kõik krediidihalduse ootelepanekud** (**Krediidihaldus > Krediidihalduse ootelepaneku loend > Kõik krediidihalduse ootelepanekud**).
Kõigi juriidiliste isikute müügitellimused saadetakse samasse krediidihalduse ootelepaneku loendisse, pakkudes keskset vaadet kõigist tähelepanu nõudvatest tehingutest. Kasutajad näevad ainult nende juriidiliste isikute andmeid, millele neil on juurdepääs.

Müügitellimuse saab paigutada ootelepaneku loendisse järgmistel põhjustel.
1. Kliendil on arve, mis on määratud päevade arvuga tähtaja ületanud. 
2. Tellimusel on kindel konto olek.
3. Tellimusel on kindlad maksetingimused.
4. Kliendil on aegunud krediidilimiit.
5. Kliendil on tähtaja ületanud summa ja ta on kasutanud määratud protsenti oma krediidilimiidist
6. Müügitellimus ületab teatud summa.
7. Klient on ületanud teatud protsendi oma krediidilimiidist.
8. Maksetingimused erinevad kliendi vaikimisi maksetingimustest.
9. Tasakaalustuse allahindlused erinevad kliendi jaoks vaikimisi seatud tasakaalustuse allahindlusest.

Blokeerimise põhjus kuvatakse iga müügitellimuse kohta ootelepaneku loendis. Kui ootelepanekul on rohkem kui üks põhjus, kuvatakse põhjusena **Mitu**. Saate kasutada tegevuspaani menüüd **Blokeerimise põhjused**, et vaadata kõiki põhjusi, miks müügitellimus ootele pandi. Saate ka vaadata **Blokeerimise põhjuseid** Kiirinfos.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Tellimuste vabastamine ootelepaneku loendist töötlemiseks

Kui olete uurinud välja ootelepaneku põhjused ja olete need lahendanud, saate müügitellimused edasiseks töötlemiseks vabastada.

1) Valige ooteloleku loendi rida. Saate vabastada mitu tellimust, valides rohkem kui ühe rea.
2) Valige vabastamiseks valitud tellimuse **Vabastamise põhjus**.  
3) Sisestage iga vabastamiseks valitud tellimuse **Ülevaatamise kuupäev**.  
4) Tellimuse vabastamiseks valige toimingupaanilt menüü **Vabasta**. See menüü on saadaval ainult pärast kannete valimist. Kasutajale esitatakse kaks valikut.
   - Valige **Sisestamisega**, et eemaldada ootelolek ja sisestada dokument, kasutades sama sisestamise protsessi, mida kasutati ootele panemisel. Näiteks kui müügitellimuse kinnitus pandi ootele, lõpetatakse müügitellimuse kinnitus pärast vabastamist. Kuvatakse müügitellimuse sisestamise vorm, lubades kasutajal kinnituse sisestada.
   - Valige **Sisestamata**, et eemaldada ootelepanek ilma täiendava töötluseta. Müügitellimuse saab sisestada käsitsi.

### <a name="rejecting-orders-in-the-hold-list"></a>Ootelepaneku loendis tellimuste tagasilükkamine
Müügitellimuse tagasilükkamiseks saate kasutada toimingupaani menüüd **Keeldu**
1. Valige ooteloleku loendi rida. Saate vabastada mitu tellimust, valides rohkem kui ühe rea.
2. Tellimus eemaldatakse ootelepaneku loendist ja müügitellimuse päis värskendatakse, et näidata, et tellimus lükati tagasi.

### <a name="automatically-releasing-credit-management-holds"></a>Krediidihaldusega soetud ootelepaneku automaatne vabastamine
Müügitellimused pannakse ootelepaneku loendisse blokeerimisreeglite põhjal. Siiski võivad mõned ootelepaneku põhjused ajas muutuda, kui müügitellimus jääb ootenimekirja pikaks ajaks. Näiteks võib klient maksta oma arve, vabastades oma krediidilimiidi. 

Saate kasutada menüüd **Vabastamise hindamine**, et vaadata ootelepaneku nimekirjas olevad müügitellimused üle ja vabastada need automaatselt, kui ootele panemise põhjus on lahendatud.
1.  Valige menüü **Vabastamise hindamine**
2.  Kõigi müügitellimuste ülevaatamiseks valige **Blokeerimisreeglite töötlemine**. Valige **Valitud ridade blokeerimisreeglite töötlemine**, et vaadata üle ainult valitud read.
3. Kuvatakse liugur, et saaksite valida ühe kliendi. Kõigi klientide valimiseks jätke kliendi ripploend tühjaks. 
4. Kui klõpsate OK, käivitatakse protsess taustal ja te saate jätkata tööd teiste ülesannetega. Kui valite pakktöötluse enne nupu OK klõpsamist, käivitatakse protsess partiina nupu OK klõpsamisel. Ootel olevate tellimuste töötlemiseks võib kuluda veidi aega, seega kasutage tellimuste oleku värskendamiseks nuppu Värskenda. 
5.  Kui blokeerimise põhjus tellimuse puhul enam ei kehti, ei peeta blokeerimise põhjust enam kehtivaks ja te ei näe enam blokeerimise põhjusi vaadates põhjuse kõrval märget.
6.  Kui kõik blokeerimise põhjused on kõrvaldatud, lisatakse blokeerimise põhjuste loendisse uus põhjus **Valmis vabastamiseks**. Müügitellimuse saab automaatselt vabastada.
7.  Kui **Automaatse vabastamise** parameeter vahekaardil **Krediidihaldus ja võlanõuded > Seadistus > Krediidihalduse ja võlanõuete parameetrid > Krediit > Automaatne vabastamine** on seadistatud väärtusele **Sisestamisega**, palutakse teil blokeeritud dokumendi sisestamise vormi abil sisestada.
8.  Kui **Automaatse vabastamise** parameeter vahekaardil **Krediidihaldus ja võlanõuded > Seadistus > Krediidihalduse ja võlanõuete parameetrid > Krediit > Automaatne vabastamine** on seadistatud väärtusele **Sisestamiseta**, peate tellimuse käsitsi sisestama.

### <a name="credit-management-approval-workflow"></a>Krediidihalduse kinnitamise töövoog

Saate luua ka **Krediidihalduse töövoogusid**, et kontrollida krediidihalduse ootelolekute vabastamist. Kui olete töövoo seadistanud, kasutades selleks lehte **Krediidihaldus > Seadistus > Krediidihalduse töövood**, saadetakse vabastamiseks või tagasilükkamiseks märgitud tellimused töövoogu, kus need tuleb enne vabastamist või tagasilükkamist kinnitada. 

Kui kaasate töövoogu sisestamisega või ilma sisestamiseta vabastamise ülesanded, vabastab töövoo kinnitamine ka müügitellimuse. Kuid kui vabastamise protsessis ilmneb tõrge puuduvate seadistuse andmete tõttu või muudel põhjustel, peate müügitellimuse töövoost tagasi kutsuma, tõrke põhjustanud probleemi parandama ja seejärel tellimuse uuesti töövoogu esitama.

Kui te ei kaasa töövoogu sisestamisega või ilma sisestamiseta vabastamise ülesandeid, lubab töövoo kinnitusprotsess teil lihtsalt müügitellimuse pärast kinnitamist käsitsi vabastada.

### <a name="forced-credit-hold"></a>Sunnitud krediidihalduse ootelepanek  
  
Mõnikord võib olla vaja müügitellimusi blokeerida, isegi kui tellimus ei vasta blokeerimise reeglite kriteeriumidele. Näiteks võidakse krediidihaldurit teavitada krediidiga mitteseotud probleemist kliendiga ning ta võib otsustada panna koheselt tellimused käsitsi ootele, seni kuni probleem on kõrvaldatud. Kui see olukord ilmneb, saate müügitellimuse käsitsi ootele panna.

1. Avage see müügitellimus, mida soovite ootele panna.  
2. Valige **Sunnitud krediidihalduse ootelepanek** vahekaardil **Krediidihaldus** tegevuspaanil **Krediidihaldus**.
3. Valige **Sunnitud ootelepaneku põhjus**.
4. Klõpsake nuppu **OK**. Müügitellimus viiakse tagasi krediidihalduse ootelepaneku loendisse.

Saate ka mitu tellimust jõuga ootele panna, kasutades selleks lehte **Krediidihaldus-> Perioodilised ülesandeid, > Sunnitud krediidihalduse ootelepanek**. Näiteks võite teatud kliendi kõik müügitellimused ootele panna.
1. Valige **Sunnitud ootelepaneku põhjus**. 
2. Klõpsake nuppu **Kaasatavad kirjed**, et valida ootele pandavad müügitellimused. 
3. Valitud müügitellimuse töötlemiseks klõpsake **OK**.

Ootel sunnitud müügitellimusi ei saa töövooga töödelda.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Krediidihalduse ootelepaneku loendisse sunnitud tellimuste vabastamine
Müügitellimusi, millel on sunnitud ootelepaneku põhjus, ei saa automaatselt vabastada. Kui müügitellimus on ootele sunnitud ja te olete kasutanud protsessi, mis vabastab müügitellimused automaatselt, kuvatakse müügitellimuse olekuks **Vabastamiseks valmis** ja see jääb ootele. Tellimuse vabastamiseks peate kasutama menüüd **Vabastamine**.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Vabas vormis arved, tellimused ja projekti arvete tugi krediidihalduses 
Krediidihaldust saab praegu kasutada ainult müügitellimuste puhul. Vabas vormis arved, kassapõhised tellimused ja kõnekeskuse tellimused kasutavad ajutisi krediidilimiite ja kindlustusi/garantiisid, mille krediidilimiidi kohandamiseks lisate. Need ei kasuta blokeerimise reegleid ja neid ei panda ootele, kui krediidilimiidiga probleeme on.

Krediidihaldus ei toeta projektiarveid.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]