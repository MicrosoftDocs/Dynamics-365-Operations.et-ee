---
title: Mobiilsed arvete heakskiidud
description: See teema on mõeldud praktilise lähenemise pakkumiseks mobiilistsenaariumide kujundamisele, võttes mobiilse hankija arvete kinnitamise kasutusnäiteks.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2406df379084fefd4e1ca33c271b69f4dafeb5b5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358901"
---
# <a name="mobile-invoice-approvals"></a>Mobiilsed arvete heakskiidud

[!include [banner](../includes/banner.md)]

Mobiilsed võimalused võimaldavad ärikasutajatel mobiilikogemusi kujundada. Täpsemate stsenaariumide puhul võimaldab platvorm arendajatel võimalusi oma soovi kohaselt laiendada. Kõige tulemuslikum viis mõningaid neist uutest mobiilikontseptsioonidest tundma õppida on läbi mõne stsenaariumi kujundamise protsessis. See teema on mõeldud praktilise lähenemise pakkumiseks mobiilistsenaariumide kujundamisele, võttes mobiilse hankija arvete kinnitamise kasutusnäiteks. See teema aitab teil kujundada stsenaariumide muid variatsioone ja seda saab rakendada ka muudele stsenaariumidele, mis pole hankija arvetega seotud.

## <a name="prerequisites"></a>Eeltingimused

| Eeltingimus                                                                                            | Kirjeldus                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobiili käsiraamat eelnevaks lugemiseks                                                                                |[Mobiiliplatvorm](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 Finance                                                                              | Keskkond, millesse on installitud versioon 1611 ja platvormivärskendus 3 (november 2016)                   |
| Installige kiirparandus KB 3204341.                                                                              | Tegevuse salvestaja võib kogemata salvestada rippdialoogidele kaks sulgemiskäsku platvormi värskenduses 3 (2016. aasta novembri värskendus). |
| Installige kiirparandus KB 3207800.                                                                              | See kiirparandus võimaldab vaadata manuseid mobiilikliendil, mis sisaldub platvormi värskenduses 3 (2016. aasta novembri värskendus).           |
| Installige kiirparandus KB 3208224.                                                                              | Rakenduse kood mobiilse hankija arve kinnitamise rakenduse jaoks, mis sisaldub versioonis 7.0.1 (mai 2016).                          |
| Androidi, iOS-i või Windowsi seade, millesse on installitud mobiilirakendus. | Otsige rakendust vastavast rakenduste poest.                                                                                                                     |

## <a name="introduction"></a>Sissejuhatus
Hankija arvete mobiilsed kinnitused nõuavad kolme kiirparandust, mis on nimetatud jaotises „Eeltingimused”. Need kiirparandused ei paku tööruumi arvete kinnitamiseks. Seda, mis on mobiili kontekstis tööruum, saate lugeda jaotises „Eeltingimused” nimetatud mobiili käsiraamatust. Arvete kinnitamise tööruum vajab kujundamist. 

Iga organisatsioon korraldab ja määratleb hankija arvete äriprotsessi erinevalt. Enne hankija arvete kinnituste jaoks mobiilikogemuse kujundamist tuleks arvestada järgimisi äriprotsessi aspekte. Kasutajakogemuse optimeerimiseks seadmel tuleks neid andmepunkte kasutada võimalikult palju.

-   Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?
-   Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?
-   Mitu arverida arvel on? Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.
-   Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha? Kui vastus sellele küsimusele on jah, siis kaaluge järgmisi küsimusi.
    -   Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud, jagamised jne) arve real on? Rakendage jällegi 80-20 reeglit.
    -   Kas arvete päises on ka arvestuse jaotused? Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?

    > [!NOTE]
    > Selles teemas ei selgitata, kuidas arvestuse jaotusi redigeerida, kuna seda funktsiooni ei toetata praegu mobiilistsenaariumide puhul.

-   Kas kasutajad soovivad seadmel arve manuseid näha?

Arvete kinnitamise mobiiliversioon on erinev, olenevalt nende küsimuste vastustest. Eesmärk on optimeerida organisatsioonis kasutaja äriprotsessi kogemust mobiilil. Ülejäänud teemas vaatame kahte stsenaariumivarianti, mis põhinevad erinevatel vastustel eelnevatele küsimustele. 

Üldise juhisena veenduge mobiilikujundajaga töötamisel, et avaldaksite muudatused, et vältida nende kaotsiminekut.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Lihtsa arve kinnitamise stsenaariumi kujundamine Contoso jaoks
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
<td>Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</td>
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
<td>Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</td>
<td><ol>
<li>Hankekategooria</li>
<li>Kogus</li>
<li>Ühiku hind</li>
<li>Rea netosumma</li>
<li>1099-summa</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mitu arverida arvel on? Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha?</td>
<td>Jah</td>
</tr>
<tr class="odd">
<td>Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud jne) arve real on? Rakendage jällegi 80-20 reeglit.</td>
<td>Laiendatud hind: 2 Käibemaks: 0 Tasud: 0</td>
</tr>
<tr class="even">
<td>Kas arvete päises on ka arvestuse jaotused? Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?</td>
<td>Pole kasutusel</td>
</tr>
<tr class="odd">
<td>Kas kasutajad soovivad seadmel arve manuseid näha?</td>
<td>Jah</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Tööruumi loomine

1.  Avage brauser ja logige rakendusse sisse.
2.  Kui olete sisse loginud, lisage URL-ile **&mode=mobile**, nagu on näidatud järgmises näites, ja värskendage lehte: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**. Mobiilirakenduse kujundaja peaks ilmuma samamoodi, nagu ilmub tegevuse salvestaja.
4.  Klõpsake uue tööruumi loomiseks nuppu **Lisa**. Selle näite puhul andke tööruumile nimi **Minu kinnitused**.
5.  Sisestage kirjeldus.
6.  Valige tööruumi värv. Tööruumi värvi kasutatakse selle tööruumi üldise mobiiliversiooni stiili puhul.
7.  Valige tööruumi ikoon.
8.  Klõpsake nuppu **Valmis**
9.  Muudatuste salvestamiseks klõpsake nuppu **Avalda tööruum**

### <a name="vendor-invoices-assigned-to-me"></a>Mulle määratud hankijaarved

Esimene mobiilne leht, mis vajab kujundamist, on kasutajale ülevaatamiseks määratud arvete loend. Selle mobiilse lehe kujundamiseks kasutage lehte **VendMobileInvoiceAssignedToMeListPage**. Enne selle protseduuri läbimist veenduge, et teile oleks ülevaatamiseks määratud vähemalt üks hankija arve ja et arve real oleks kaks jaotust. See seadistus vastab selle stsenaariumi nõuetele.

1.  Asendage URL-is menüüelemendi nimi stringiga **VendMobileInvoiceAssignedToMeListPage**, et avada loendilehe **Mulle määratud ootel hankija arved** mobiiliversioon moodulis **Ostureskontro**. Olenevalt sellest, kui palju arveid on teile teie süsteemis määratud, kuvatakse sellel lehel need arved. Konkreetse arve otsimiseks võib kasutada vasakul olevat filtrit. Kuid selle näite puhul pole meil konkreetset arvet vaja. Meil on lihtsalt vaja, et teile oleks määratud mõni arve, mis võimaldaks teil mobiilset lehte kujundada. Uued saadaolevad lehed on kujundatud spetsiaalselt hankija arve mobiilistsenaariumide väljatöötamiseks. Seega tuleb kasutada neid lehti. URL peab sarnanema järgmisele URL-ile ja kui olete selle sisestanud, peab avanema joonisel näidatud leht: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile 

    [![Mulle määratud hankija minu lehel ootel arved.](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
    
2.  Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**
3.  Valige oma tööruum ja klõpsake nuppu **Redigeeri**
4.  Klõpsake esimese mobiilse lehe loomiseks nuppu **Lisa leht**.
5.  Sisestage nimi nagu **Minu hankija arved** ja kirjeldus nagu **Mulle ülevaatamiseks määratud hankija arved**.
6.  Klõpsake nuppu **Valmis**.
7.  Klõpsake mobiilse kujundaja vahekaardil **Väljad** nuppu **Vali väljad**. Loendilehe veerud peavad sarnanema järgmisele illustratsioonile. 

    [![Veerud lehel Mulle määratud ootel hankija arved minu lehel.](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
    
8.  Lisage vajalikud veerud loendilehelt, mis tuleb mobiililehel kasutajatele kuvada. Väljad kuvatakse lõppkasutajatele lisamise järjekorras. Ainus võimalus väljade järjestust muuta on kõik väljad uuesti valida. Selle stsenaariumi nõuete põhjal on vaja järgmist kaheksat välja. Kuid mõned kasutajad võivad leida, et kaheksa välja on mobiilsel seadmel liiga palju teavet. Seega näitame mobiili loendivaates ainult kõige olulisemaid välju. Ülejäänud väljad kuvatakse üksikasjavaates, mille kujundame hiljem. Praegu lisame järgmised väljad. Klõpsake plussmärki (**+**) nende veergude mobiililehele lisamiseks.
    - Hankija nimi
    - Arve summa
    - Maksja
    - Arve number
    - Arve kuupäev

    Pärast väljade lisamist peab mobiilileht sarnanema järgmisele illustratsioonile. 
    
    [![Leht pärast väljade lisamist.](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)

9.  Nüüd tuleb lisada ka järgmised väljad, et hiljem saaks töövootoimingud lubada.
    - Kuva lõpetamise ülesanne
    - Kuva delegeerimise ülesanne
    - Kuva tagasikutsumise ülesanne
    - Kuva tagasilükkamise ülesanne
    - Kuva taotluse täitmise ülesanne
    - Kuva uuesti esitamise ülesanne

10. Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.
11. Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks
12. Töö salvestamiseks klõpsake nuppu **Avalda tööruum**
13. Lubage ostureskontro vormi jaotises **Arve** valik **Kuva ootel hankija arvete loendis arve koondsumma**. Pange tähele, et arve koondsummad arvutatakse ootel hankija arvete loendilehel kuvamiseks ainult selle parameetri lubamisel. See on uus võimalus, mis kuulub eeltingimuseks olevasse kiirparandusse 3208224.

### <a name="vendor-invoice-details"></a>Hankija arve andmed

Arve üksikasjade lehe kujundamiseks mobiiliversioonile kasutage lehte **VendMobileInvoiceHeaderDetails**. Pange tähele, et olenevalt sellest, kui palju arveid on teile teie süsteemis määratud, kuvatakse sellel lehel vanim arve (esimesena koostatud arve). Konkreetse arve otsimiseks võib kasutada vasakul olevat filtrit. Kuid selle näite puhul pole meil konkreetset arvet vaja. Meil on lihtsalt vaja mõningaid arveandmeid, et saaksime mobiilset lehte kujundada. 

[![Töövoo leht.](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. Asendage URL-is menüüelemendi nimi stringiga **VendMobileInvoiceHeaderDetails** vormi avamiseks

2. Avage mobiilne kujundaja nupult **Sätted** (hammasratas).

3. Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.

4. Valige eelnevalt loodud leht **Minu hankija arved** ja klõpsake siis nuppu **Redigeeri**.

5. Klõpsake vahekaardil **Väljad** veerupäist **Ruudustik**.

6. Klõpsake valikuid **Atribuudid &gt; Lisa leht**. **Märkus.** Kui klõpsate pealkirja **Ruudustik** ja lisate lehe, luuakse automaatselt seos üksikasjade lehega.

7. Sisestage lehe pealkiri, nt **Arve üksikasjad** ja kirjeldus, nt **Kuva arve päis ja rea üksikasjad**.

8. Klõpsake nuppu **Vali väljad**. Pange tähele, et väljad kuvatakse lõppkasutajatele lisamise järjekorras. Ainus võimalus väljade järjestust muuta on kõik väljad uuesti valida. 

9. Lisage selle stsenaariumi nõuete põhjal päisest järgmised väljad.
   - Hankija nimi
   - Arve summa
   - Maksja
   - Arve number
   - Arve kuupäev
   - Arve kirjeldus
   - Tähtaeg
   - Arve valuuta

10. Lisage lehel olevast ridade ruudustikust järgmised väljad.
    - Hankekategooria
    - Kogus
    - Ühiku hind
    - Rea netosumma
    - 1099-summa

11. Kui kõik väljad eelmisest kahest toimingust on lisatud, klõpsake nuppu **Valmis**. Leht peab sarnanema järgmisele illustratsioonile.
    
    [![Lisatud lisavälju kujutav illustratsioon.](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)

12. Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.

13. Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks

14. Töö salvestamiseks klõpsake nuppu **Avalda tööruum**

### <a name="workflow-actions"></a>Töövoo tegevused

Töövootoimingute lisamiseks kasutage lehte **VendMobileInvoiceHeaderDetails**. Selle lehe avamiseks asendage menüüelemendi nimi URL-is nii, nagu varem tegite. Seejärel avage mobiilne kujundaja nupult **Sätted** (hammasratas). Tehke järgmist töövootoimingute lisamiseks üksikasjade lehel. Teile peavad olema määratud sobivas olekus arved, mis teevad teile kättesaadavaks need töövootegevused, mille kujundamisega tegelete.

#### <a name="record-workflow-actions"></a>Töövoo tegevuste registreerimine
1.  Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.
2.  Valige eelnevalt loodud leht **Arve üksikasjad** ja klõpsake siis nuppu **Redigeeri**.
3.  Klõpsake vahekaardil **Tegevused** käsku **Lisa tegevus**.
4.  Sisestage tegevuse pealkiri, nt **Kinnitamine**, ja kirjeldus, nt **Arve kinnitamine**. Pange tähele, et sisestatud tegevuse pealkirjast saab tegevuse nimi, mida kasutajale mobiilirakenduses näidatakse.
5.  Klõpsake nuppu **Valmis**.
6.  Klõpsake nuppu **Vali väljad**.
7.  Läbige töövooprotsess lehel **VendMobileInvoiceHeaderDetails** ja tehke tegevus, mida soovisite registreerida. Veenduge, et sisestate selle protsessi käigus töövoo kommentaarid, nii et kommentaaride väli lisatakse samuti mobiiliversiooni.
8.  Pärast töövootegevuse käitamist klõpsake väljade valimise ülesande lõpetamiseks nuppu **Valmis**.
9.  Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.
10. Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks
11. Töö salvestamiseks klõpsake nuppu **Avalda tööruum**
12. Korrake eelmisi toiminguid kõigi vajalike töövootegevuste registreerimiseks. 

#### <a name="create-a-js-file"></a>Looge JS-fail
1. Avage Notepad või Microsoft Visual Studio ja kleepige sinna järgmine kood. Salvestage fail JS-failina. See kood teeb järgmist.
    - See peidab töövooga seotud lisaveerud, mille varem mobiili loendilehel lisasime. Lisasime need veerud selleks, et rakendusel oleks see teave kontekstis olemas ja see saaks teha järgmise toimingu.
    - Aktiivse töövooetapi põhjal rakendab see loogikat ainult nende tegevuste näitamiseks.

    > [!NOTE]
    > Lehtede ja muude juhtelementide nimed JS-koodis peavad olema samad, mis tööruumis.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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
    ```

2.  Laadige koodifail tööruumi üles, valides vahekaardi **Loogika**
3.  Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.
4.  Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks
5.  Töö salvestamiseks klõpsake nuppu **Avalda tööruum**

### <a name="vendor-invoice-attachments"></a>Hankija arve manused

1. Klõpsake nuppu **Sätted** (hammasratas) lehe ülemises paremas osas ja seejärel valikut **Mobiilirakendus**

2. Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**.

3. Valige eelnevalt loodud leht <strong>Arve üksikasjad** ja klõpsake siis nuppu **Redigeeri</strong>.

4. Määrake valiku **Dokumendihaldus** sätteks **Jah**, nagu allpool näidatud. **Märkus.** Kui puuduvad nõuded mobiilsel seadmel manuste näitamiseks, võite jätta selle valiku sätteks **Ei**, mis on vaikesäte.
   
   ![Dokumendihaldus.](./media/docmanagement-216x300.png)

5. Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.

6. Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks

7. Töö salvestamiseks klõpsake nuppu **Avalda tööruum**

### <a name="vendor-invoice-line-distributions"></a>Hankija arve rea jaotused

Selle stsenaariumi nõudmised kinnitavad, et olemas on ainult rea tasemel jaotused ja et arvel on alati ainult üks rida. Kuna see stsenaarium on lihtne, peab kasutaja kogemus mobiilsel seadmel olema samuti piisavalt lihtne, et kasutaja ei peaks jaotuste vaatamiseks mitme taseme võrra süvitsi minema. Hankija arved sisaldavad võimalust kuvada kõik jaotused arve päisest. Seda me mobiilistsenaariumi puhul vajamegi. Seetõttu kasutame selle mobiilistsenaariumi osa kujundamiseks lehte **VendMobileInvoiceAllDistributionTree**. 

> [!NOTE] 
> Nõuetega kursis olemine aitab meil stsenaariumi kujundamisel otsustada, millist konkreetset lehte kasutada ja kuidas täpselt kasutaja mobiilikogemust optimeerida. Teises stsenaariumis kasutame teist lehte jaotuste näitamiseks, kuna selle stsenaariumi nõuded on erinevad.

1.  Asendage menüüelemendi nimi URL-is nii, nagu enne tegite. Kuvatav leht peab sarnanema järgmisele illustratsioonile.

    [![Kõigi jaotuste leht.](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)

2.  Avage mobiilne kujundaja nupult **Sätted** (hammasratas).

3.  Klõpsake tööruumis redigeerimisrežiimi käivitamiseks nuppu **Redigeeri**. **Märkus.** Näete, et automaatselt loodi kaks uut lehte. Süsteem loob need lehed, kuna lülitasite eelmises jaotises sisse dokumendihalduse. Võite neid uusi lehti eirata.

4.  Klõpsake nuppu **Lisa leht**.

5.  Sisestage lehe pealkiri, nt **Arvestuse kuvamine** ja kirjeldus, nt **Arve arvestuse kuvamine**.

6.  Klõpsake nuppu **Valmis**.

7.  Klõpsake vahekaardil **Väljad** valikut **Vali väljad**, valige jaotuste lehelt järgmised väljad ja klõpsake seejärel nuppu **Valmis**:
    1.  Summa
    2.  Valuuta
    3.  Pearaamatukonto

    > [!NOTE] 
    > Me ei valinud jaotuste ruudustikust veergu **Kirjeldus**, kuna selle stsenaariumi nõuded kinnitasid, et laiendatud hind on ainus summa, mille jaoks jaotused olemas on. Seega ei vaja kasutaja teist välja summa tüübi määramiseks, mille jaoks jaotus on mõeldud. Kuid järgmises stsenaariumis **kasutame** seda teavet, kuna selle stsenaariumi nõuded määravad, et teistel summatüüpidel on jaotused (nt käibemaks).

8.  Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.

9.  Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks

10. Töö salvestamiseks klõpsake nuppu **Avalda tööruum**

#### <a name="adding-navigation-to-view-accounting-page"></a>Lehele „Raamatupidamise kuvamine” navigeerimise lisamine

Mobiilileht **Arvestuse kuvamine** pole praegu seotud ühegi mobiililehega, mille seni kujundanud oleme. Kuna kasutaja peab saama liikuda lehele **Arvestuse kuvamine** mobiilse seadme lehelt **Arve üksikasjad**, peame pakkuma võimalust liikuda lehelt **Arve üksikasjad** lehele **Arvestuse kuvamine**. Tekitame selle liikumisvõimaluse, kasutades JavaScripti kaudu lisaloogikat.

1.  Avage varem loodud JS-fail ja lisage read, mis tõstetakse esile järgmises koodis. See kood teeb kahte asja.
    1.  See aitab garanteerida, et kasutajad ei saa liikuda otse tööruumist lehele **Arvestuse kuvamine**.
    2.  See tekitab navigeerimisnupu lehelt **Arve üksikasjad** lehele **Arvestuse kuvamine**.

    > [!NOTE] 
    > Lehtede ja muude juhtelementide nimed JS-koodis peavad olema samad, mis tööruumis.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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
    ```
    
2.  Eelmise koodi ülekirjutamiseks laadige koodifail tööruumi üles, valides vahekaardi **Loogika**
3.  Redigeerimisrežiimist väljumiseks klõpsake nuppu **Valmis**.
4.  Klõpsake nuppu **Tagasi** ja seejärel nuppu **Valmis** tööruumist väljumiseks
5.  Töö salvestamiseks klõpsake nuppu **Avalda tööruum**

### <a name="validation"></a>Kinnitamine

Avage rakendus oma mobiilses seadmes ja looge ühendus oma eksemplariga. Veenduge, et logiksite sisse ettevõttesse, kus teile on määratud ülevaatamiseks hankija arved. Teil peaks olema võimalik teha järgmisi toiminguid.

-   Vaadake tööruumi **Minu kinnitused**.
-   Minge tööruumis **Minu kinnitused** süvitsi ja vaadake lehte **Minu hankija arved**.
-   Minge tööruumis **Minu hankija arved** süvitsi ja vaadake endale määratud arvete loendit.
-   Minge mõnes arves süvitsi ja vaadake arve päise üksikasju ja rea üksikasju.
-   Vaadake üksikasjade lehel linki manuste juurde ja minge selle lingi abil manuste loendisse ning vaadake manuseid.
-   Vaadake üksikasjade lehel linki lehele **Arvestuse kuvamine** ja minge selle lingi abil jaotuste lehele ning vaadake jaotusi.
-   Klõpsake üksikasjade lehe allosas menüüd **Tegevused** ja tehke töövooetappi puudutavad töövootegevused.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Keeruka arve kinnitamise stsenaariumi kujundamine Fabrikami jaoks
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
<td>Milliseid arve päise välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</td>
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
<td>Milliseid arve ridade välju soovib kasutaja mobiiliversioonis näha ja millises järjekorras?</td>
<td><ol>
<li>Hankekategooria</li>
<li>Kogus</li>
<li>Ühiku hind</li>
<li>Rea netosumma</li>
<li>1099-summa</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mitu arverida arvel on? Rakendage siin 80-20 reeglit ja optimeerige 80 protsendi jaoks.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Kas kasutajad soovivad arvestuse jaotusi (arvekoode) ülevaatamise ajal mobiilsel seadmel näha?</td>
<td>Jah</td>
</tr>
<tr class="odd">
<td>Kui palju arvestuse jaotusi (laiendatud hind, käibemaks, tasud jne) arve real on? Rakendage jällegi 80-20 reeglit.</td>
<td>Laiendatud hind: 2 Käibemaks: 2 Tasud: 2</td>
</tr>
<tr class="even">
<td>Kas arvete päises on ka arvestuse jaotused? Kui nii, siis kas need arvestuse jaotused peaksid seadmel kättesaadavad olema?</td>
<td>Pole kasutusel</td>
</tr>
<tr class="odd">
<td>Kas kasutajad soovivad seadmel arve manuseid näha?</td>
<td>Jah</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>Järgmised sammud

1. stsenaariumi puhul saab kasutada järgmisi variatsioone, tuginedes 2. stsenaariumi nõuetele. Selle jaotise abil saate parandada oma mobiilirakenduse kogemust.

1.  Kuna 2. stsenaariumi puhul eeldatakse suuremat arve ridade arvu, aitavad järgmised kujunduse muudatused kasutajakogemust mobiilsel seadmel optimeerida.
    1.  Arve ridade vaatamise asemel üksikasjade lehel (nagu 1. stsenaariumis) võivad kasutajad valida ridade vaatamise eraldi mobiililehel.
    2.  Kuna selles stsenaariumis eeldatakse mitut arve rida, siis kui mobiili jaotuste lehe kujundamiseks kasutatakse lehte **VendMobileInvoiceAllDistributionTree** (nagu 1. stsenaariumis), võib ridade seostamine jaotustega kasutajale segadust tekitada. Seetõttu kasutage jaotuste lehe kujundamiseks lehte **VendMobileInvoiceLineDistributionTree**.
    3.  Ideaaljuhul tuleks jaotusi näidata selles stsenaariumis arve rea kontekstis. Seega veenduge, et kasutaja saab jaotuste lehe vaatamiseks reas süvitsi minna. Kasutage lehe lingivõimalust süvaaruande koostamiseks, nagu tegite päise ja üksikasjade lehtedel 1. stsenaariumis.

2.  Kuna 2. stsenaariumi puhul eeldatakse mitut summa tüüpi (käibemaks, tasud jne), on kasulik näidata summa tüübi kirjeldust. (Jätsime selle teabe 1. stsenaariumist välja.)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
