---
title: Mobiilne arvekinnitusi
description: "Mobiilne võimalusi Microsoft Dynamics 365 tegevuste lase disain mobiilne kogemusi ärikasutaja. Keerukamate stsenaariumide platvormi ka let&quot;s arendajad laiendavad nagu nad soovivad. Tõhusaim viis õppida mõned uued mõisted mobiil on minna läbi protsessi mõned stsenaariumid projekteerimine. Selle teema eesmärk praktiline lähenemine projekteerimine mobiilne stsenaariumid võttes hankija arve kinnitused mobiili kasutamise haigusjuht. Selle teema peaks aitama teil kujundada teisi variante stsenaariumid ja rakendub ka ainus põhjus, mis ei ole seotud hankijate arvete."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Mobiilne arvekinnitusi

Mobiilne võimalusi Microsoft Dynamics 365 tegevuste lase disain mobiilne kogemusi ärikasutaja. Keerukamate stsenaariumide platvormi ka let's arendajad laiendavad nagu nad soovivad. Tõhusaim viis õppida mõned uued mõisted mobiil on minna läbi protsessi mõned stsenaariumid projekteerimine. Selle teema eesmärk praktiline lähenemine projekteerimine mobiilne stsenaariumid võttes hankija arve kinnitused mobiili kasutamise haigusjuht. Selle teema peaks aitama teil kujundada teisi variante stsenaariumid ja rakendub ka ainus põhjus, mis ei ole seotud hankijate arvete.

<a name="prerequisites"></a>Eeltingimused
-------------

| Eeltingimus                                                                                            | Kirjeldus                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eelnevalt lugeda mobiilne käsiraamat                                                                                |(/ dynamics365/toimingud/dev-itpro/mobile-apps / mobile-platform.md)                                                                                                  |
| Dynamics 365 toiminguteks                                                                             | Keskkond, mis on Microsoft Dynamics 365 toiminguid versiooni 1611 ja Microsoft Dynamics toimingute platvormi update 3 (November 2016)                   |
| Installige käigultparanduse KB 3204341.                                                                              | Ülesanne Salvesti saate salvestada ekslikult kahe tiheda käske rippmenüüst dialoogid on turvaline Dynamics 365 operatsiooni platvormi Update 3 (November 2016 update) |
| Installige käigultparanduse KB 3207800.                                                                              | Selle käigultparanduse võimaldab manuseid vaadata mobiilirakendust, see sisaldub Dynamics 365 operatsiooni platvormi värskendus 3 (November 2016 värskendus).           |
| Installige käigultparanduse KB 3208224.                                                                              | Rakenduse koodi mobiilne hankija arve kinnitamise taotluse see sisaldub Microsoft Dynamics AX-i rakenduse 7.0.1 (mai 2016).                          |
| Android või iOS või Windows seadme, kuhu on installitud Dynamics 365 operatsioonide mobiilne rakendus | Otsida asjakohaseid app store appi.                                                                                                                     |

## <a name="introduction"></a>Sissejuhatus
Mobiilne kinnitused hankijaarvete nõuavad kolme käigultparandused, mis on nimetatud jaotises "Eeltingimused". Need käigultparandused ei anna tööruumi arve tunnustuse. Saate teada, mida tööruumi raames mobiilne, loetakse mobiilne käsiraamat, mis on nimetatud jaotises "Eeltingimused". Arve kinnitused tööruumi projekteerida. 

Iga organisatsiooni orchestrates ja määratleb oma äriprotsessi hankijaarvete erinevalt. Enne kujundate mobiilne kogemus hankija arve tunnustuse, kaaluge äriprotsessi järgmised aspektid. Selleks tuleb kasutada neid võimalikult palju hõlbustada kasutaja seadme andmepunkte.

-   Arve päises väljad kasutaja tahavad näha mobiilne kogemus ja millises järjekorras?
-   Arve ridade väljad kasutaja tahavad näha mobiilne kogemus ja millises järjekorras?
-   Kui palju arve ridu on arve? Siin 80-20 reeglit ja optimeerida 80 protsenti.
-   Kasutajad tahavad näha raamatupidamise distributsioonid (arve kodeerimise) mobiilsideseadme ajal arvustust? Kui vastus sellele küsimusele on Jah, käsitlevad järgmisi küsimusi:
    -   Arve rida on mitu raamatupidamise distributsioonid (laiendatud hinna, käibemaksu, tasu, lõheneb ja jne)? Jällegi, kohaldatakse 80-20 reegel.
    -   Kas arveid ka on raamatupidamise distributsioonid arve päisesse? Kui nii, tuleks nende raamatupidamise distributsioonid seadme?

> [!NOTE]
> See teema ei selgita kuidas muuta raamatupidamise distributsioonid, sest see funktsionaalsus veel ei toeta mobiilne stsenaariume.

-   Kasutajad tahavad näha arve manused seadme?

Arve tunnustuse mobiilne kogemus disain erinevad sõltuvalt vastuseid nendele küsimustele. Eesmärk on parandada kasutaja äriprotsessi Mobile organisatsioonis. Ülejäänud selle teema, me vaatame kaks stsenaariumi variandid, mis põhinevad eespool toodud küsimustele erinevaid vastuseid. 

Üldised suunised, mobiilne disainer töötamisel, veenduge, et värskendused kaotsimineku vältimiseks muudatuste avaldamiseks.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Contoso lihtne arve kinnitamise stsenaariumi projekteerimine
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Stsenaariumi atribuut</th>
<th>Vastus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Arve päises väljad kasutaja tahavad näha mobiilne kogemus ja millises järjekorras?</td>
<td><ol>
<li>Hankija nimi</li>
<li>Arve summa</li>
<li>Maksja</li>
<li>Arve number</li>
<li>Arve kuupäev</li>
<li>Arve kirjeldus</li>
<li>Tähtaeg</li>
<li>Arve valuuta</li>
</ol></td>
</tr>
<tr class="even">
<td>Arve ridade väljad kasutaja tahavad näha mobiilne kogemus ja millises järjekorras?</td>
<td><ol>
<li>Hankekategooria</li>
<li>Kogus</li>
<li>Ühiku hind</li>
<li>Rea netosumma</li>
<li>1099-summa</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kui palju arve ridu on arve? Siin 80-20 reeglit ja optimeerida 80 protsenti.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Kasutajad tahavad näha raamatupidamise distributsioonid (arve kodeerimise) mobiilsideseadme ajal arvustust?</td>
<td>Jah</td>
</tr>
<tr class="odd">
<td>Arve rida on mitu raamatupidamise distributsioonid (laiendatud hinna, käibemaksu, tasu ja nii edasi)? Jällegi, kohaldatakse 80-20 reegel.</td>
<td>Laiendatud hind: 2 käibemaksu: tasud 0: 0</td>
</tr>
<tr class="even">
<td>Kas arveid ka on raamatupidamise distributsioonid arve päisesse? Kui nii, tuleks nende raamatupidamise distributsioonid seadme?</td>
<td>Pole kasutusel</td>
</tr>
<tr class="odd">
<td>Kasutajad tahavad näha arve manused seadme?</td>
<td>Jah</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Tööruumi loomine

1.  Brauseris, avage Dynamics 365 operatsioonide ja Logi sisse.
2.  Pärast seda, kui olete sisse logitud, lisada **& mode = mobiilne** nagu järgmine näide ja Värskenda lehe URL: https://&lt;yoururl&gt;/? VTMS = usmf & mi = DefaultDashboard**& mode = mobiilne**
3.  Klõpsake selle **sätted** (käik) nuppu lehekülg ja seejärel klõpsake ülemises **mobiilirakendus**. Mobiilirakenduse disainer tuleb näidata üles nii, nagu ülesande recorder näitab üles.
4.  Klõpsake **lisa** luua uue tööruumi. Näiteks nimi tööruumi **minu kinnitused**.
5.  Sisestage kirjeldus.
6.  Valige värv tööruumi. Tööruumi värvi kasutatakse üldist stiili mobiilne kogemus selle tööruumi jaoks.
7.  Valige ikoon tööruumi.
8.  Klõpsake **teha**
9.  Klõpsake **avaldada tööruumi** muudatuste salvestamiseks

### <a name="vendor-invoices-assigned-to-me"></a>Mulle määratud hankijaarved

Mobiilne tuleks kujundada on määratud kasutaja vaadata arvete loendit. Mobiili lehe kujundamine, kasutage selle **VendMobileInvoiceAssignedToMeListPage** lehe Dynamics 365 toiminguteks. Enne selle toimingu, veenduge, et üks hankija arve teile määratud läbivaatamiseks, ja et arve real on kaks väljamakseid. See seadistus vastab selle stsenaariumi.

1.  Toimingute URL Dynamics 365, asendada nimi menüü koos **VendMobileInvoiceAssignedToMeListPage** avamiseks mobiilis on **kuni mulle määratud hankijaarvete** nimekirja lehel on **arved** moodul. Sõltuvalt teie süsteemis määratud teile arvete arv näitab sellel lehel neid arveid. Kindla arve leidmiseks kasutage filtrit vasakul. Siiski me ei nõua konkreetsele arvele seda näiteks. Eeldame vaid mõned teile arve, mis võimaldab teil kavandada mobiilne leht saab. Uusi lehti, mis on saadaval on mõeldud spetsiaalselt mobiilne stsenaariumid hankijaarve arendamine. Seega, kasutage neid lehti. URL näeb järgmine URL ja pärast sisestamist, leht, mis on näidatud joonisel esinema: https://&lt;yourURL&gt;/? VTMS = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& mode = mobiilne [![kuni mulle määratud Hankijate arvete lehekülg](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Klõpsake selle **sätted** (käik) nuppu lehekülg ja seejärel klõpsake ülemises **mobiilirakendus**
3.  Valige oma tööruumi ja klõpsake **redigeerimine**
4.  Klõpsake **Lisa lehekülg** luua mobiilse esilehel.
5.  Sisestage nimi, näiteks **minu hankijaarvete**, ja kirjeldus, näiteks **mulle läbivaatamiseks määratud hankijaarvete**.
6.  Click **Done**.
7.  Mobiilne kujundaja kohta ning **väljade** vahekaardil, klõpsake **väljade**. Lehel loendi veerud peavad sarnaneb järgmise näite. [![Veergude ootel hankijaarvete mulle määratud lehekülje](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Lisama nõutavad veerud tuleb näidata kasutajatele mobiilne lehel loendi lehel. Siis lisada järjestus on kus väljad kuvatakse antud. Ainus viis muuta väljade järjekorda saab valides uuesti kõik väljad. Seda vajaduste järgi, järgmised kaheksa väljad on kohustuslikud. Kuid mõned kasutajad võiks kaaluda kaheksa väljad liiga palju teavet on mobiiltelefon. Seega, näitame vaid olulisemaid mobiilne loendivaates. Ülejäänud väljad kuvatakse kuva üksikasjad, mida me hiljem kavandada. Nüüd, lisame järgmised väljad. Klõpsake plussmärki (**+**) nendes veergudes mobiilne lehele lisada.
    1.  Hankija nimi
    2.  Arve summa
    3.  Maksja
    4.  Arve number
    5.  Arve kuupäev

    Pärast väljade lisamist tuleb mobiilne leht sarnaneb järgmise näite. [![Pärast seda, kui on lisatud väljad lehe](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Samuti peate lisama järgmised veerud nüüd, et me saate lubada töövoo tegevused hiljem.
    1.  Näita täita ülesanne
    2.  Näita tööülesande delegeerimine
    3.  Näita meenutavad ülesanne
    4.  Näita keeldu ülesanne
    5.  Taotluse täitmise ülesande kuvada
    6.  Näita uuesti ülesanne

10. Klõpsake **teha** funktsioonist väljumiseks.
11. Klõpsake **tagasi** ja siis **teha** väljumiseks tööruumi
12. Klõpsake **avaldada tööruumi** oma töö salvestada.
13. Lubade kasutada programmi **Kuva arve summa kuni Hankija arvete loendi** kontode Ostureskontro parameetrid vormi **arve**. Pange tähele, et ainult see parameeter, võimaldades arve kogusummad arvutatakse ootel Hankija arvete nimekirja lehel kuvada. See on uus võimalus eelnevalt vajaliku kiirparandus 3208224 osana.

### <a name="vendor-invoice-details"></a>Hankija arve üksikasjad

Arve andmete lehe mobiilne kujundamiseks kasutada ka **VendMobileInvoiceHeaderDetails** lehe Dynamics 365 toiminguteks. Pange tähele, et, arved, mis on teie süsteemis arvule selle lehe vanim arve (arve, mis loodi esimene). Kindla arve leidmiseks kasutage filtrit vasakul. Siiski me ei nõua konkreetsele arvele seda näiteks. Lihtsalt nõuame arve andmeid nii, et saame kujundada mobiilne leht. [![Lehe töövoo](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  Toimingute URL Dynamics 365, asendada nimi menüü koos **VendMobileInvoiceHeaderDetails** vorm
2.  Avage mobiilne disainer ning **sätted** (käik) nuppu.
3.  Klõpsake selle **muuta** nuppu, et alustada redigeerimisrežiimi tööruumis.
4.  Valige selle ** minu hankijaarvete ** lehekülg, et varem loodud ja klõpsake **muuta**.
5.  Kohta ning **väljade** vahekaardil, klõpsake selle **Grid** veeru päist.
6.  Klõpsake **atribuudid**&gt;**Lisa lehekülg**. **Märkus:** kui klõpsate selle **Grid** eemaldamist ja lisada lehe, üksikasjade lehele on loodud automaatselt suhted.
7.  Sisestage lehe pealkiri, nagu **arve üksikasjad**, ja kirjeldus, näiteks **arve päis ja tellimuserea üksikasjade vaatamine**.
8.  Klõpsake **väljade**. Pange tähele, et, kus lisate järjestus on kus väljad kuvatakse antud. Ainus viis muuta väljade järjekorda saab valides uuesti kõik väljad.
9.  Päisest, seda vajaduste järgi lisada järgmised väljad:
    1.  Hankija nimi
    2.  Arve summa
    3.  Maksja
    4.  Arve number
    5.  Arve kuupäev
    6.  Arve kirjeldus
    7.  Tähtaeg
    8.  Arve valuuta

10. Lisada read võrku lehel järgmistes valdkondades:
    1.  Hankekategooria
    2.  Kogus
    3.  Ühiku hind
    4.  Rea netosumma
    5.  1099-summa

11. Pärast kahte eelmist sammu kõigi väljade lisamist, klõpsake **teha**. Leht peab sarnaneb järgmise näite. [![Pärast seda, kui on lisatud väljad lehe](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Klõpsake **teha** funktsioonist väljumiseks.
13. Klõpsake **tagasi** ja siis **teha** väljumiseks tööruumi
14. Klõpsake **avaldada tööruumi** dokumenti salvestama

### <a name="workflow-actions"></a>Töövoo tegevused

Töövoo tegevuste lisamiseks kasutada ka **VendMobileInvoiceHeaderDetails** lehe Dynamics 365 toiminguteks. Selle lehe avamiseks asendada nimi menüükäsu URL, nagu tegite varem. Avage mobiilne disainer ning **sätted** (käik) nuppu. Järgmiste juhiste abil lisada töövoo tegevuste üksikasjade lehel.

1.  Klõpsake selle **muuta** nuppu, et alustada redigeerimisrežiimi tööruumis.
2.  Valige selle **arve üksikasjad** lehekülg, et varem loodud ja klõpsake **muuta**.
3.  Kohta ning **meetmete** vahekaardil, klõpsake **lisa toiming**.
4.  Sisestage toimingu nimetus, näiteks **kinnitamine**, ja kirjeldus, näiteks **kinnitamine arve**. Pange tähele, et meetme pealkiri, mis siin saab kasutaja mobiilirakenduse kuvatava toimingu nime.
5.  Click **Done**.
6.  Klõpsake **väljade**.
7.  Minna töövooprotsessid ning **VendMobileInvoiceHeaderDetails** lehele ja täitke toimingut, mida soovite salvestada. Et Sisesta töövoo kommentaarid käigus sõnumis välja märkused kaasatakse ka mobiilne kogemus.
8.  Pärast töövoo toimingu, klõpsake **teha** lõpetamiseks valige Välju.
9.  Klõpsake **teha** funktsioonist väljumiseks.
10. Klõpsake **tagasi** ja siis **teha** väljumiseks tööruumi
11. Klõpsake **avaldada tööruumi** dokumenti salvestama
12. Korrake juhiseid 3 – 11 salvestada kõik vajalik töövoo toiminguid. Pange tähele, et nõue on teile arveid, mis on riigi töövoo tegevused teile, et te lähete projekteerimise kättesaadavaks.
13. Avage Notepad või Microsoft Visual Studio ja kleepige järgmine kood. Faili salvestamine js faili. See kood ei kahte asja:
    1.  See peidab ekstra töövooga seotud veerud, mida me lisatakse varem mobiili nimekirja lehel. Lisasime need veerud nii, et rakendus ei tea kontekstis ja teha järgmine samm.
    2.  Põhineb aktiivset töövoosammu, kehtib see loogika näidata ainult need toimingud.

Pange tähele, et lehekülgi ja muude kontrollide JS kood nimi peab olema sama tööruumist.

1.  (metadataService, dataService, cacheService, $q) peamine funktsioon {tagasi {appInit: funktsioon (appMetadata) {/ / Peida kontrollid, mis tuleb käesoleva, kuid ei ole nähtav metadataService.configureControl ("My-müük-arve, 'ShowAccept', {peidetud: true}); metadataService.configureControl (" My-müük-arve, 'ShowApprove', {peidetud: true}); metadataService.configureControl ("My-müük-arve, 'ShowReject', {peidetud: true}); metadataService.configureControl (" My-müük-arve, 'ShowDelegate', {peidetud: true}); metadataService.configureControl ("My-müük-arve, 'ShowRequestChange', {peidetud: true}); metadataService.configureControl (" My-müük-arve, 'ShowRecall', {peidetud: true}); metadataService.configureControl ("My-müük-arve, 'ShowComplete', {peidetud: true}); metadataService.configureControl (" My--hankijaarvete, 'ShowResubmit', { peidetud: tõsi}); }, pageInit: funktsiooni (pageMetadata, http Authentication) {kui (pageMetadata.Name == "Arve üksikasjad") {/ / Kuva/peida töövoo tegevuse töövoo vastavalt samm metadataService.configureAction ("Nõustun", {nähtav: true}); metadataService.configureAction ("Kinnitamine", {nähtav: true}); metadataService.configureAction ("Keeldu", {nähtav: true}); metadataService.configureAction ("Saadik", {nähtav: true}); metadataService.configureAction ("taotluse muutmine", {nähtav: true}); metadataService.configureAction ("Tagasikutsumine" {nähtav: true}); metadataService.configureAction ("Täielik", {nähtav: true}); metadataService.configureAction ("Saatma" {nähtav: true});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Koodi faili üleslaadimise tööruumi valimisel on **Logic** vahekaarti
3.  Klõpsake **teha** funktsioonist väljumiseks.
4.  Klõpsake **tagasi** ja siis **teha** väljumiseks tööruumi
5.  Klõpsake **avaldada tööruumi** dokumenti salvestama

### <a name="vendor-invoice-attachments"></a>Hankija arve manused

1.  Klõpsake selle **sätted** (käik) nuppu lehekülg ja seejärel klõpsake ülemises **mobiilirakendus**
2.  Klõpsake selle **muuta** nuppu, et alustada redigeerimisrežiimi tööruumis.
3.  Valige selle ** arve üksikasjad ** lehekülg, et varem loodud ja klõpsake **muuta**.
4.  Määra ning **Dokumendihaldus** võimalus **Jah** allpool. **Märkus:** kui puuduvad nõuded mobiilsideseadme manuste kuvamiseks, saate jätta selle variandi seatud **nr**, mis on vaikimisi säte.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Klõpsake **teha** funktsioonist väljumiseks.
7.  Klõpsake **tagasi** ja siis **teha** väljumiseks tööruumi
8.  Klõpsake **avaldada tööruumi** dokumenti salvestama

### <a name="vendor-invoice-line-distributions"></a>Hankija arve rea distributsioonid

Nõuded seda kinnitada, et tekib ainult rida tasemel väljamakseid ning arve on alati ainult üks rida. Sest sel juhul on lihtne, peab kasutaja kogemus mobiilsideseadme olema piisavalt lihtne, et kasutaja ei pea puurida ette mitmel tasandil vaadata hoolduse jaotusi. Hankijaarvete Dynamics 365 toimingud hõlmavad näidata kõik väljamaksed arve päisest. See kogemus on, et me vajame mobiilne stsenaariumi. Seega, me kasutame nende **VendMobileInvoiceAllDistributionTree** lehe disain mobiilne stsenaariumi osas. 

> [!NOTE] 
> Teades nõuetele aitab otsustada, millist konkreetset lehte kasutada ja kuidas täpselt saaksid parandada mobiilside kasutaja kui loome stsenaarium. Teise võimalusena kasutame teisele lehele näidata jaotamist, sest selle stsenaariumi nõuded erinevad.

1.  URL-i, asendada nimi menüükäsu, nagu sa tegid enne. Ilmuval lehel peaks sarnaneb järgmise näite. [![Kõik väljamaksed lehekülg](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Avage mobiilne disainer ning **sätted** (käik) nuppu.
3.  Klõpsake selle **muuta** nuppu, et alustada redigeerimisrežiimi tööruumis. **Märkus:** näete, et kaks uut lehekülge loodi automaatselt. Süsteem loob külastamine, sest lülitasite Dokumendihaldus eelmises osas. Võite ignoreerida neid uusi lehti.
4.  Klõpsake **Lisa lehekülg**.
5.  Sisestage lehe pealkiri, nagu **vaade raamatupidamise**, ja kirjeldus, näiteks **vaade raamatupidamise arve**.
6.  Click **Done**.
7.  Kohta ning **väljade** vahekaardil, klõpsake **väljade**, väljamaksete lehel Valige järgmised väljad ja seejärel klõpsake **teinud**:
    1.  Summa
    2.  Valuuta
    3.  Pearaamatukonto

> [!NOTE] 
> Me ei valinud selle **kirjeldus** veeru jaotuse võrku, sest selle stsenaariumi nõuded kinnitanud, et laiendatud hind ainult summa, mis tekib jaotusi. Seega kasutaja ei nõua teise välja jaoks on summa liigi määramiseks. Siiski on stsenaariumi, me **on** isikuandmeid kasutatakse, sest selle stsenaariumi nõuded määrata muud tüübid on distributsioonid (nt käibemaks).
8.  Klõpsake **teha** funktsioonist väljumiseks.
9.  Klõpsake **tagasi** ja siis **teha** väljumiseks tööruumi
10. Klõpsake **avaldada tööruumi** dokumenti salvestama

**Märkus:** on **vaade raamatupidamise** mobiilne leht pole praegu seotud mobiilne lehekülgedel, et oleme loonud nii kaugele. Kuna kasutaja peaks suutma liikuda selle **Vaata raamatupidamise** lehekülg on **arve üksikasjad** lehe mobiilsideseadme, me peame tagama navigeerimine: on **arve üksikasjad** lehel on **Vaata raamatupidamise** lehekülg. Loome täiendavaid loogika kaudu JavaScript abil selles navigeerimine.

1.  Varem loodud js faili avada ja lisada järgmine kood read, mis on esile tõstetud. See kood ei kahte asja:
    1.  See aitab tagada, et kasutajad ei saa navigeerida otse tööruumi ning **vaade raamatupidamise** lehel.
    2.  Leiab navigeerimise juhtelement: selle **arve üksikasjad** lehel on **Vaata raamatupidamise** lehel.

> [!NOTE] 
> Lehti ja muud juhtelemendid JS kood nimi peab olema sama tööruumist.

1.  (metadataService, dataService, cacheService, $q) peamine funktsioon {tagasi {appInit: funktsioon (appMetadata) {/ / Peida kontrollid, mis tuleb käesoleva, kuid ei ole nähtav metadataService.configureControl ("My-müük-arve, 'ShowAccept', {peidetud: true}); metadataService.configureControl (" My-müük-arve, 'ShowApprove', {peidetud: true}); metadataService.configureControl ("My-müük-arve, 'ShowReject', {peidetud: true}); metadataService.configureControl (" My-müük-arve, 'ShowDelegate', {peidetud: true}); metadataService.configureControl ("My-müük-arve, 'ShowRequestChange', {peidetud: true}); metadataService.configureControl (" My-müük-arve, 'ShowRecall', {peidetud: true}); metadataService.configureControl ("My-müük-arve, 'ShowComplete', {peidetud: true}); metadataService.configureControl (" My--hankijaarvete, 'ShowResubmit', { peidetud: tõsi}); Peida lehti ei kehti root navigeerimine metadataService.hideNavigation('View-accounting'); Raamatupidamise metadataService.addLink kuvamiseks ("arve-detailide," View-raamatupidamine "," vaade-raamatupidamise-nav-kontroll ","Vaata raamatupidamise", true); }, pageInit: funktsiooni (pageMetadata, http Authentication) {kui (pageMetadata.Name == "Arve üksikasjad") {/ / Kuva/peida töövoo tegevuse töövoo vastavalt samm metadataService.configureAction ("Nõustun", {nähtav: true}); metadataService.configureAction ("Kinnitamine", {nähtav: true}); metadataService.configureAction ("Keeldu", {nähtav: true}); metadataService.configureAction ("Saadik", {nähtav: true}); metadataService.configureAction ("taotluse muutmine", {nähtav: true}); metadataService.configureAction ("Tagasikutsumine" {nähtav: true}); metadataService.configureAction ("Täielik", {nähtav: true}); metadataService.configureAction ("Saatma" {nähtav: true});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Koodi faili üleslaadimise tööruumi valimisel on **Logic** vahekaarti eelmise koodi ülekirjutamiseks
3.  Klõpsake **teha** funktsioonist väljumiseks.
4.  Klõpsake **tagasi** ja siis **teha** väljumiseks tööruumi
5.  Klõpsake **avaldada tööruumi** dokumenti salvestama

### <a name="validation"></a>Kinnitamine

Mobiiltelefonist, avage rakendus ja ühendada oma Dynamics 365 toimingute eksemplari. Veenduge, et logite firma kus hankijaarvete määratakse teile läbivaatamiseks. Siis peaks olema võimalik sooritada järgmisi toiminguid:

-   Vt ka **minu kinnitused** tööruumi.
-   Üldiseks on **minu kinnitused** tööruumi ja Vaata selle **minu hankijaarvete** lehel.
-   Üldiseks on **minu hankijaarvete** lehekülg ja vaadata teile määratud arvete nimekirja.
-   Üldiseks arvete hulgast ja arve päise üksikasjade ja tellimuserea üksikasjade nägemiseks.
-   Üksikasjade lehel näha lingi tarvikud ja kasutada seda linki manuste loendisse navigeerida ja vaadake manused.
-   Üksikasjade lehel näha linki selle **Vaata raamatupidamise** lehele ja selle lingi kaudu levimine lehele liikuda ja vaadata hoolduse jaotusi.
-   Üksikasjade lehel klõpsake selle **meetmete** menüü allosas ja töövoo tegevusteks, mida kohaldatakse töövoosammu.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Fabrikami keeruline arve kinnitamise stsenaariumi projekteerimine
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Stsenaariumi atribuut</th>
<th>Vastus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Arve päises väljad kasutaja tahavad näha mobiilne kogemus ja millises järjekorras?</td>
<td><ol>
<li>Hankija nimi</li>
<li>Arve summa</li>
<li>Maksja</li>
<li>Arve number</li>
<li>Arve kuupäev</li>
<li>Arve kirjeldus</li>
<li>Tähtaeg</li>
<li>Arve valuuta</li>
</ol></td>
</tr>
<tr class="even">
<td>Arve ridade väljad kasutaja tahavad näha mobiilne kogemus ja millises järjekorras?</td>
<td><ol>
<li>Hankekategooria</li>
<li>Kogus</li>
<li>Ühiku hind</li>
<li>Rea netosumma</li>
<li>1099-summa</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kui palju arve ridu on arve? Siin 80-20 reeglit ja optimeerida 80 protsenti.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Kasutajad tahavad näha raamatupidamise distributsioonid (arve kodeerimise) mobiilsideseadme ajal arvustust?</td>
<td>Jah</td>
</tr>
<tr class="odd">
<td>Arve rida on mitu raamatupidamise distributsioonid (laiendatud hinna, käibemaksu, tasu ja nii edasi)? Jällegi, kohaldatakse 80-20 reegel.</td>
<td>Laiendatud hind: 2 käibemaksu: 2 tasud: 2</td>
</tr>
<tr class="even">
<td>Kas arveid ka on raamatupidamise distributsioonid arve päisesse? Kui nii, tuleks nende raamatupidamise distributsioonid seadme?</td>
<td>Pole kasutusel</td>
</tr>
<tr class="odd">
<td>Kasutajad tahavad näha arve manused seadme?</td>
<td>Jah</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Harjutus

Järgmine muutus teha stsenaarium 1, stsenaarium 2 vajaduste järgi. Kasutage seda jaotist teostamiseks, majutatud õppimise eesmärgil.

1.  Sest rohkem Hooldusarve read oodatakse stsenaariumi 2, projektis järgmised muudatused aitavad hõlbustada kasutaja mobiilsideseadme:
    1.  Arve ridade vaatamise üksikasjade lehel (nagu puhul 1) asemel saavad kasutajad valida vaatamiseks eraldi mobiilse lehele.
    2.  Sest mitme arverea eeldatakse sel puhul, kui on **VendMobileInvoiceAllDistributionTree** lehe abil kujundada distributsioonid lehe mobiilne (nagu 1. puhul), võib tekitada segadust, kasutajal oleksid read jaotustele. Seetõttu on **VendMobileInvoiceLineDistributionTree** lehe kujundada väljamaksete lehel.
    3.  Ideaalis peaks jaotamist juhul arve rida selle stsenaariumi kontekstis. Vastasel juhul saab kasutaja minna vastavusse distributsioonid lehe vaatamiseks. Kasutama lehe link võime on drill-through, just nagu sa päis ja andmed lehekülge stsenaariumi 1.

2.  Sest üle ühe summa liik peaks stsenaariumi 2 väljamaksete tegemisel (käibemaksu, tasu ja nii edasi), oleks kasulik summa liigi kirjeldus. (Me jätta selle teabe juhul 1.)

## <a name="conclusion"></a>Lõppsõna
Mobiilsel platvormil ja võimeid taotluse abil saate kujundada mobiilne stsenaariumid, mis on optimeeritud baasi asutuses kasutaja. Tuginedes näiteid, mis on toodud selle teema, võite proovida muid variante ja luua erinevaid kogemusi, mis vastavad teatud.


