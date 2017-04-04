---
title: Projekti ressursieraldus
description: See teema pakub teavet projekti korralikke.
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
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Projekti ressursieraldus

See teema pakub teavet projekti korralikke.

Üks projektijuhid ja ressursihalduri ajal projekti kavandamise etapis on ressursside jaotus, kus nad tuleb kindlaks määrata ja projekti kallal õige ressursi reserveerimist. Microsoft Dynamics 365 toiminguteks, efektiivne võimalusi projektide sul määratleda rollid, mille käsitletakse ajutine ressursse, mida saab reserveerida konkreetse töövõtuga kaasnevaid või osa on kaasamine. Sedalaadi ressursieraldus võimaldab projektijuhtidel ja ressursihalduritel teha järgmisi toiminguid.

-   Määratleda ressursside sobitamise hõlbustamiseks rolli, millel on vajalikud kompetentsid.
-   Kasutage rollid esialgne tegevus ajakava, mis põhineb reserveeritud vahendeid.
-   Prognoosida kulusid ja määratleda algse eelarve, tuginedes projekti määratud rollidele ja ressurssidele.
-   Kasutada rollide kohta ressursi nõutakse iga tegevuse hindamiseks.
-   Hinnata kogu projekti töötsükli jaoks vajalike ressursside arvu.
-   Koostada projekti tööjaotuse struktuuri (WBS) esialgse ressursimäärangu abil.

[![Projekti elutsükkel](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Kui projekti planeerimise tulu, kavandatud ressursid võib asendada rahalisi ressursse. Projektijuht saate tagasi minna ja värskendada resourcing broneerimine ükskõik millisel projekti etappi.

## <a name="set-up-project-resources"></a>Projekti ressursside seadistamine
Peate seadistama kalendri ja seostama selle töötajaga. Kalendrit saab ajastada projekt ja projekti ressursse, mis on reserveeritud tööaja. Kalendri seadistamisel saavad projektijuhid ressursside optimeerimise käigus ressursse ühtlustada. Kalendrigraafiku alusel saab ressurssidele piiranguid seada. Seadistage kalendri kohta ning **kalendrid** lehel. 

Töötaja projekti ressursina seadistamisel saate valida mille seadistate ressursside ettevõttes töötajate või valige töötajate teistest ettevõtetest oma organisatsioonis. Need on Kontserni ressursse. Järgmised protseduurid selgitavad, kuidas luua töötaja ettevõtte projekti ressursina ja IC projekti ressursside seadistamise.

### <a name="set-up-a-worker-as-a-project-resource"></a>Töötaja seadistamine projekti ressursina

1.  Kohta ning **töötajate** lehekülg, mis on **töötajate** nimekirja, valige lisatava projekti ressursina töötaja ja avage töötaja kirje.
2.  Kohta ning tegevus paanil klõpsake **projekti**&gt;**Setup**&gt;**projekti seadistus**.
3.  Valige ja seejärel sulgege leht.

Saate määrata eelmäärangu tüübina ressursile ka vaikeprojekte. Eelmääranguid saab kasutada, kui ressursihaldur või projektijuht teab ette, milliste projektidega ressurss töötama hakkab. Eelmäärangud võivad põhineda ka projekti sponsori või kliendi soovil. Projekti eelmääramiseks valige lehelt **Projektide määramine** vahekaardil **Projektid** loendis **Järelejäänud projektid** sobiv projekt.

### <a name="set-up-an-intercompany-resource"></a>Saate seadistada IC ressurss

Kontsernisisese ressursina töötaja seadistamisel peate täitma setup laenuandja äriühingu ja laenusaaja äriühingu. 

**Aastal laenuandja äriühing:**

1.  Dynamics 365 toiminguteks, veenduge, et laenuandja äriühing on valitud ja seejärel sooritage eeltoodule protseduur "Luua projekti ressursina töötaja."
2.  Mine ** PR *&gt; ** kont **&gt;**kontserni raamatupidamise**. Click **New**.
3.  Aastal ning ** juriidiline isik ID ** number laenuandja äriühing,. Täitke ülejäänud väljad vastavalt vajadusele ja klõpsake **salvestamine**.
4.  Minna ning ** projektijuhtimine ja raamatupidamine *&gt; ** seadistamine **&gt;**eest ** &gt;**siirdehinna**.** **
5.  Kohta ning ** korrigeerimistelt ** kujul, klõpsake **uus**, ja on ** laenamine juriidilise ** number õige firma,.
6.  Kui soovite ainult laenu laenusaaja äriühingu ressurss, mida olete loonud käesoleva alguses ning **ressurss** number, loodud ressursi nimi. Kui soovite kättesaadavaks kõik ressursid ettevõttes laenusaajale äriühingule, jätke selle ** ressursi ** väli tühi.
7.  Mine ** projektijuhtimine ja raamatupidamine **&gt; ** seadistamine **&gt;**projektijuhtimine ja kuluarvestuse parameetrid**, ja selle ** kontsernisisese ** tab, määrata selle ** kontsernisisese Ressursiplaanimine ja ajatabelite ** välja **Jah**.

**Laenusaaja äriühingu:**

1.  Mine **projektijuhtimine raamatupidamis- ja**&gt;**projekti vahendite**&gt;**loendi**.
2.  Otsingu filtrit, sisestage eelmise korra kontrollimaks, et nimi sisaldub Ressursiloendis laenusaaja äriühingu laenuandja äriühing loodud ressursi nimi.

## <a name="manage-resource-competencies"></a>Ressursi kompetentside haldamine
Ressursi kompetentsid on oluline osa ressursside haldamine. Kompetentse saab kasutada alusena ressursside määratlemiseks, kellel on õige oskuste, hariduse, tunnistuste ja projektikogemuse tasakaal. See teave tuleb igale ressursile määrata ja regulaarselt värskendada. Nii saate maksimeerida võimalusi, kui projekti ressursimääramise käigus konkreetsed ressursikompetentsid vastendatakse. [![Oskusi, kinnitamine, haridus ja projekti kogemust](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Järgmistes protseduurides selgitatakse ressursi mõningate pädevuste seadistamist. 

Töötaja kompetentside seadistamiseks kasutatakse loendilehte **Töötajad** moodulis Inimressursid või loendilehte **Ressursid** moodulis Projektihaldus ja raamatupidamine. Järgmiste protseduuride puhul on **töötajate** kasutatakse loendilehe inimkapitali.

### <a name="set-up-competencies-certificates"></a>Kompetentside seadistamine: tunnistused

1.  Valige loendilehelt **Töötajad** selle töötaja rida, kellele tunnistuse andmeid lisate.
2.  Klõpsake tegumiriba vahekaardil **Töötaja** grupis **Kompetentsid** valikut **Tunnistused**.
3.  Klõpsake **Uus**.
4.  Tehke väljal **Tunnistuse tüüp** valik **PMP**.
5.  Tehke väljal **Alguskuupäev** valik **10/1/2015**.
6.  Klõpsake nuppu **Salvesta** ja sulgege seejärel leht.

### <a name="set-up-competencies-skills"></a>Kompetentside seadistamine: oskused

1.  Veenduge lehel **Töötajad**, et eelmises protseduuris kasutatud töötaja on endiselt valitud. Seejärel klõpsake tegumiriba vahekaardil **Töötaja** grupis **Kompetentsid** valikut **Oskused**.
2.  Klõpsake **Uus**.
3.  Tehke väljal **Oskus** valik **Projektihaldus**.
4.  Tehke väljal **Tase** valik **5 Ekspert**.
5.  Tehke väljal **Taseme kuupäev** valik **1-/14/2014**.
6.  Sisestage väljale **Kogemus aastates** väärtus **10**.
7.  Klõpsake nuppu **Salvesta** ja sulgege seejärel leht.

## <a name="create-a-new-project"></a>Loo uus projekt
1.  Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**tööruumide**&gt;**projektijuhtimine**.
2.  Klõpsake valikut **Uus projekt** ja sisestage seejärel järgmised väärtused.
    -   **Projekti tüüp** - aja- ja materjalikulu
    -   **Projekti nimi** -XYZ uuendada faas 2
    -   **Projektigrupi** -TM\_WIP
    -   **Projekti lepingu** -00000002
3.  Klõpsake valikut **Loo projekt**.

### <a name="assign-a-resource-to-a-project"></a>Ressursi määramine projektile

1.  Klõpsake **töötajate**&gt;**töötajate**&gt;**töötajate**.
2.  Valige loendist **Töötajad** selle töötaja kirje, kelle jaoks eelnevalt kompetentsid seadistasite, ja avage töötaja kirje.
3.  Klõpsake tegumiriba vahekaardil **Projekt** grupis **Seadistus** valikut **Projektide määramine**.
4.  Klõpsake lehel **Ressursi kinnitamise projekti määrangud** vahekaarti **Projektid**.
5.  Aastal ning **lisada projekti valitud projektide**, filter projekti, XYZ uuendada faas 2
6.  Valige paanilt **Järelejäänud projektid** projekt ja klõpsake siis noolt selle lisamiseks paanile **Valitud projektid**.
7.  Sulgege leht.

Vajaduse korral saate ka ressursile kategooriaid määrata. Kategooria tüüp on kulu või tulu. Selle määrab teie organisatsioon. Kui Ressursi nr omistatud kategooriad, Dynamics 365 operatsioonide otsida tund hindade, kulude ja tulude vaikekategooria.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekti ressursi ja rolli omaduste seadistamine

Projektijuht saab kasutada projekti ressursieralduse funktsiooni projekti jaoks vajalike rollide loomiseks. Ülesanded saab kui kinnitatud ressursse on veel teadmata, kui ressursside broneerimist. Rollid ajutiselt reserveerimist kui kavandatud ressursid, et jätkata projekti kavandamise etappe. 

[![Näiteks on osa](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Stsenaarium:** Contoso palgati täitma aja ja materjali projekti, millel on kinnitatud projekti põhikiri. Noorem-projektijuht täidab veel projekti ulatust. Ressursihaldur on praegu kindlakstegemisel, mis uue projekti kallal, reserveeritakse varud. Üks projekti sponsor taotletud projekti kriitiline olemus on vanem projektijuht. Ressursihaldur peab omandama uut ressurssi ja määratlema rolli süsteemis juhul junior projektijuht tuleb ressursi teave projekti planeerimise ajal. 

Järgmised juhised kirjeldavad, kuidas ressursihaldur seadistage Senior project manager roll ja ressursi omaduste seostamine. Hiljem saab rolli kasutada vajalikele ressursi kompetentsidele vastavate olemasolevate ressursside otsimiseks.

1.  Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**Setup**&gt;**ressursid**&gt;**Setup rollid**.
2.  Klõpsake valikut **Uus** ja sisestage seejärel järgmised väärtused.
    -   **Rolli ID** -vanemprojektijuht
    -   **Kirjeldus** -vanemprojektijuht
3.  Klõpsake käsku **Loo**.
4.  Valige roll **Vanem-projektijuht** ja klõpsake siis valikut **Omaduste konfigureerimine**.
5.  Valige väljalt **Omaduse tüüp** väärtus **Oskus**.
6.  Sisestage väljale **Olemasolev omadus** oskus, mida otsite.
7.  Valige väljalt **Omaduse tüüp** väärtus **Tunnistus**.
8.  Sisestage väljale **Olemasolev omadus** tunnistuse tüüp, mida otsida.
9.  Klõpsake nuppu **OK** ja sulgege leht.

### <a name="assign-a-project-resource-to-a-project"></a>Projekti ressursi määramine projektile

1.  Klõpsake **projektijuhtimine ja raamatupidamine**&gt;**ühine**&gt;**projektide**&gt;**kõik projektid**, ja avada selle **XYZ uuendada faas 2** projekti.
2.  Klõpsake vahekaardil **Projektimeeskond ja plaanimine** käsku **Lisa**.
3.  Valige väljalt **Roll** väärtus **Meeskonnaliige**.
4.  Klõpsake valikut **Kalendrist reserveerimine**.
5.  Klõpsake lehel **Ressursi saadavus** valikut **Kuva sätted**.
6.  Sisestage lehele **Kuvasätete kohandamine** järgmised väärtused.
    -   **Vormingu kuupäev range vaatan** - päev
    -   **Kuva kättesaadavus kirjeldused** - Jah
    -   **Kuva võimsus jääb** - Jah
7.  Valige ressursiloendist ressurss.
8.  Klõpsake **raamat**&gt;**maht täis**.
9.  Sulgege leht.

### <a name="assign-a-resource-to-a-default-role"></a>Vaikerollile ressursi määramine

Aidata projekti või ressursi juhtide, saab puurida alla täiendavaid ressursse, mida saab reserveerida projekti. Saate seostada vaikerolli olemasoleva ressursiga või äsja omandatud ressursiga. Näiteks, kui Daniel oli palgatud, tal oli kogemusi ja oskusi äri analüütik rolli. Ressursihaldur määrata seda rolli nagu Daniel's vaikerolli. Seetõttu ressursihaldur on Daniel äri analüütikud, kes on valmis teha projektide parki. 

Ressursside broneerimine projektijuhid saate filtreerida ning roll olemasolevate vahendite töötada projekte. Nad saavad kasutada neid andmeid ühe kriteeriumina, kui nad teevad ressursside täitmisel mitmel kriteeriumil põhinevaid analüüse. Samuti saavad nad lisada filtrile muid ressursiomadusi, et otsida antud projekti jaoks konkreetsete oskuste, hariduse ja kogemustega ressursse. 

**Stsenaarium:** heaks on alanud ja Senior project manager roll oli planeeritud ressursina reserveeritud ajal projekti kavandamise etapis. Ressursihaldur on nüüd hankinud ressursi vanem-projektijuhi rolli täitmiseks.

1.  Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**projekti vahendite**&gt;**loendi**.
2.  Valige loendist **Ressurss** väärtus **Daniel Goldschmidt**.
3.  Klõpsake **projekti ressursi**&gt;**Säilita**&gt;**ressursi roll**.
4.  Klõpsake valikut **Uus** ja sisestage seejärel järgmised väärtused.
    -   **Tõhus** - (tänane kuupäev)
    -   **Kehtib kuni** - kunagi
    -   **Rolli** -vanemprojektijuht
5.  Klõpsake nuppu **Salvesta** ja sulgege seejärel leht.
6.  Lisage vahekaardile **Kompetentsid** oskus **ProjectMgmt** ja tunnistus **PMP**.

## <a name="set-up-role-based-pricing"></a>Rollipõhise hinnakujunduse seadistamine
Rollidele saab seadistada kõik kulud, müügi- ja sisehinnad.

1.  Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**install**&gt;**eest**&gt;**müügi hind (tund)**.
2.  Click **New**.
3.  Sisestage jõustumiskuupäev.
4.  Valige roll veerust **Roll**.
5.  Sisestage veergu **Hinnakujundus** valitud ressursi rolli hind.

## <a name="form-a-project-team"></a>Moodustavad projektimeeskonna
Rollid, mis on eelnevalt seadistatud projekti kasutamiseks peab projektijuhi rollid seostada projekti. Projekti jaoks saab määrata erinevaid rolle ja Dynamics 365 operatsioonide automaatselt märgistab need rollid broneerimine vältimiseks. Näiteks kui projektijuht nõuab kolme tarkvara inseneride, kolme tarkvara insener rolli, mis on tarkvara insener 1, tarkvara insener 2 ja tarkvara insener 3 oma siltide luuakse automaatselt. Kui rollile olid eelnevalt määratud rolli omadused, rakendatakse need ressursi otsingute käigus filtrina. Otsingu täiendavaks täpsustamiseks saab omadusi lisada. 

Kuvasätteid saab samuti kohandada, et anda parem vaade ressursi saadavuse kohta. On olemas valikud saadavuse kuvamiseks tunnis, päevas, nädalas, kuus, kvartalis ja aastas. On olemas ka valik näidata ressursside olemasolevat ja järelejäänud mahtu. Sellest valikust on kasu aja juhtimisel, kui hindate tegevuste jaoks saadaolevat aega või ressursi kättesaadavust. 

Projektijuht saate valida lehe osa ja siis, kui on olemas ressurss, mis sobib nõude, valige rolli ressurssi reserveerida. Pange tähele, et ressursse ei pea olema sel hetkel reserveeritud ajal kogu. A WBS loomisel saate asendada rahalisi vahendeid projekti rollid. Kui rollid on asendatud WBS rahalisi ressursse, ressursi seadistus uuendab projektimeeskond loetelu ja ajastamine. 

[![Projekti meeskond nimekirja, mis sisaldab nii rollid kui reaalsete võimalustega](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektijuhil on mitmesuguseid võimalusi projektile ressursi reserveerimiseks, nt **Järelejäänud võimsus**, **Täisvõimsus**, **Võimsuse protsent** ja **Tundide määramine**. Neid reserveerimisvalikuid saab ressursi määrangute muutumisel igal ajal tühistada. Toetatakse kahte reserveerimise tüüpi:

-   **Raamat** – ressursside reserveerimiseks heaks ning heaks tööd määratud ajaks kaasamine.
-   **Pehme raamat** – ressursside broneerimine pidi vaikselt tööd määratud ajaks kaasamine.

Järgmine protseduur selgitab, kuidas projektimeeskonda koostada.

### <a name="create-a-project-team"></a>Projektimeeskonna koostamine

1.  Valige loendilehelt **Kõik projektid** projekt ja klõpsake siis käsku **Redigeeri**.
2.  Kohta ning **projekti meeskond ja planeerimise** vahekaardil, et **lõppkuupäev** sisestage alguskuupäev pluss üks kuu. Näiteks kui ajakava alguskuupäev on 24 juuni 2017 (24/06/2017), sisestage **24/07/2017**.
3.  Click **Add**.
4.  Valige paanilt **Projektile rollide lisamine** väljal **Roll **väärtus **Vanem-projektijuht**.
5.  Klõpsake valikut **Vajalikud kompetentsid**.
6.  Lehel **Omaduste valimine** on vaikimisi valitud omadused, mille eelnevalt vanem-projektijuhi rollile määrasite. Klõpsake nupul **OK**.
7.  Sisestage lehe **Rollide lisamine projektidele** väljale **Ressursside arv** väärtus **1**.
8.  Väljal **Ressurss** näitab otsing kõiki ressursse, millel on vajalikud kompetentsid. Valige **Daniel Goldschmidt** ja seejärel klõpsake käsku **Loo**.
9.  Klõpsake lehel **Projekt** käsku **Lisa**.
10. Valige paanilt **Projektile rollide lisamine** väljal **Roll** väärtus **Meeskonnaliige**. Sisestage väljale **Ressursside arv** väärtus **5**.
11. Klõpsake käsku **Loo**.
12. Klõpsake lehel **Projektid** valikut **Täida ressurss**.

## <a name="resource-capacity-synchronization"></a>Ressursi võimsuse sünkroonimine
Ressursi sünkroonimise protsessid aitavad tagada, et kalendri ja aluskalendri teave arvestab projekti ressursiplaanimisega. Kalendri muutmisel teevad protsessid projektiressursside plaanimises vajalikud värskendused. Protsessid aitavad ka jõudlust parandada, kuna kalendri ressursiteavet sünkroonitakse juba eelnevalt, tänu millele ressursi plaanimise teabe värskendamine toimub kiiremini. Soovitame plaanida protsessid ühekordsete asemel partiina. Vastasel korral on olemas oht, et keegi unustab hõlmavad kuupäevad, millal teavet viimati sünkrooniti. Kui hõlmavaid kuupäevi ei kasutata, võivad kuupäevade sünkroonimisel tekkida vahed.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalendri sünkroonimine](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Sünkroonimisprotsess on mõeldud kogu ressursikalendri teabe sünkroonimiseks. See teave sisaldab peamist kalendriteavet kõigi muudatuste kohta projekti ressursikalendri võimsuse tabelis. Uute vahendite lisamisel projekti sünkroonimise aitab uuendatud kalendri teabe kättesaadavuse tagamiseks. See sünkroonimine võib toimuda igal ajal. 

Soovitame kasutada partiid. Need valikud on võimsuse reserveerimiste sünkroonimisel saadaval.

-   Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**perioodiline**&gt;**maht sünkroonimise**&gt;**sünkroonida ressursside võimsuse Reklaamstendid**.

| Suvand | Kirjeldus                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jah    | sünkroonitakse kõik ressursi andmed kalendri ja peamise kalendri teabega ning asendatakse kogu teabe projekti ressursi võimsuse kalendris.                                                  |
| Ei     | sünkroonitakse ressursi andmed, tuginedes kuupäevavahemiku koodile ja määratud algus- ning lõppkuupäevale. See valik ei eemalda olemasolevaid andmeid ja värskendab ainult äsja lisatud ressursside teavet. |

[![Sünkroonimine](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Rollide seadistamine WBS-i mallidel
Projektijuhid saavad seadistada WBS-i malle, mida saab rakendada uutele projektidele WBS-i loomisel. Projektijuhid lisada rollid malli loomisel. Järgmise toimingu abil saate määrata rolli WBS template.* * **

1.  Klõpsake **projektijuhtimine ja raamatupidamine**&gt;**Setup**&gt;**projekti**&gt;**töö jaotus struktuuri malle**.
2.  Klõpsake valitud WBS-i malli valikut **Üksikasjad**.
3.  Valige loendist toiming ja seejärel valige väljalt **Roll** ülesandele määramiseks roll.

### <a name="work-with-a-wbs"></a>WBS-iga töötamine

Saate luua uue WBS-i või kopeerida WBS-i olemasolevalt WBS-i mallilt. Projektijuht saab hõlpsasti ressursse hallata, määrates WBS-is uutele toimingutele rollid. Rollid saab asendada pärast ressursi hankimist või pärast seda, kui on tuvastatud kinnitatud ressurss, kes toiminguga tööle hakkab. See paindlikkus laseb projektijuhtidel järgmisi toiminguid teha.

-   Tuvastada WBS-i tööpakettide jaoks vajalike ressursside arvu.
-   Prognoosida projekti kulusid.
-   Määratleda esialgset eelarvet.
-   Prognoosida tegevuse kestust, tuginedes rollidele ja ressurssidele.
-   Töötada välja projektijuhtimise plaane, tuginedes olemasolevale projektiteabele.

WBS-i on lisatud valikuid, et ressursieralduse funktsiooni paremini kasutada.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Suvand</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressursi määramised</td>
<td>Saate vaadata WBS-i toimingutele määratud ressursse, kuupäevi, tundide arvu ja reserveerimise tüüpi.</td>
</tr>
<tr class="even">
<td>Meeskonna automaatne loomine</td>
<td>Saate lisada automaatselt plaanitud ressursse, kasutades toiminguga seostatud rolle. Dynamics 365 operatsioonide automaatselt välja planeeritud vahendeid kasutades mitme kriteeriumiga otsuste analüüs, mis põhineb rollid. Pärast toimingutele WBS-is rollide ja panuse (tunnid) määramist ja struktuuri vabastamist klõpsake valikut <strong>Meeskonna automaatne loomine</strong>. Vajalik arv plaanitud ressursse lisatakse WBS-i ja vahekaardile <strong>Projekti ja meeskonna plaanimine</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurss (ripploend)</td>
<td>Lehel <strong>Ressursi määramise käivitamine </strong>saate valida ressursid fikseeritult või esialgselt reserveerimiseks, tuginedes määratud kestusele. Saate reguleerida kuvasätteid ressursi tegevuste vaatamiseks ja nende kestuse määramiseks. Saate valida ja määrata ressursse tööpaketi tasemel, kasutades järgmisi valikuid.
<ul>
<li><strong>Kinnita</strong> – ülesandele määratud ressursi muudatuste kinnitamine.</li>
<li><strong>Tühista</strong> – ülesandele määratud ressursi muudatuste tühistamine.</li>
<li><strong>Määrata automaatselt</strong> – selle suvandi valimine on saadaval personaliga ressurss koos valitud ülesandega kattuv roll.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**projekti**&gt;**kõik projektid**.
2.  Valige loendist projekt **XYZ täiendusfaas 2**.
3.  Klõpsake **kava**&gt;**tegevuse**&gt;**töö liigendamise struktuuriga**.
4.  Klõpsake valikuid **Uus** järgmiste esimese taseme tegevuste lisamiseks WBS-i.
    -   Algatamine
    -   Planeerimine
    -   Teostamine
    -   Seire ja juhtimine
    -   Sule

5.  Määra kuupäevad ja vaeva (tundi), nagu näidatud järgmisel pildil. [![Kuupäevad ja vaeva](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Valige ülesande rida **Algatamine** ja seejärel tehke väljal **Roll** valik **Vanem-projektijuht**.
7.  Klõpsake valikut **Avalda**.
8.  Samal real, väljal **Ressurss** valige **Daniel Goldschmidt**.
9.  Klõpsake valikut **Kinnita**.
10. Valige ülesande rida **Plaanimine** ja seejärel tehke väljal **Roll** valik **Ärianalüütik**.
11. Klõpsake käsku **Avalda** ja seejärel valikut **Meeskonna automaatne loomine**.
12. Klõpsake kuvatavas dialoogiboksis valikut **Jah**.
13. Veenduge, et väljal **Ressurss** oleks väärtus **Ärianalüütik 1**.
14. Ressursi **Ärianalüütik 1** puhul avage otsing ja klõpsake valikut **Ressursi määramise vormi käivitamine**.
15. Valige ülesande jaoks töötaja.
16. Klõpsake **pehme määra**&gt;**maht täis**.
17. Klõpsake nuppu **Salvesta** ja sulgege leht. 

> [!NOTE] 
> Te ei saa hoiatuse, millele määratud ressurss on nüüd 2, sest ressursside jääb 1.
18. Kinnitage lehel **Tööjaotuse struktuur **WBS-is ressursi määrang ja klõpsake siis käsku **Salvesta**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressursi täitmine plaanitud ressursside puhul
Projektijuht saab plaanida projekti jaoks vajalikke ressursirolle. Ressursihaldur näeb neid plaanitud ressursse taotlustena lehel **Ressursi täitmine** ja saab määrata tegelikke ressursse.

1.  Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**projekti**&gt;**kõik projektid**.
2.  Valige loendist projekt **XYZ täiendusfaas 2**.
3.  Klõpsake valikut **Projekt**.
4.  Klõpsake valikut **Redigeeri**.
5.  Kohta ning **projekti meeskonna ja planeerimise** jaotises ** ** klõpsake **lisa**.
6.  Valige dialoogiboksist **Lisa rollid** roll **Tarkvaraarendaja**.
7.  Klõpsake käsku **Loo**.
8.  Sulgege projekti leht.
9.  Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**projekti vahendite**&gt;**ressursi täitmine**.
10. Valige **Tarkvaraarendaja 1** projektile **XYZ täiendusprojekti faas 2**.
11. Valige töötaja ja klõpsake seejärel nuppu **Määra**.
12. Veenduge, et rida **Tarkvaraarendaja 1** oleks projekti **XYZ täiendusprojekti faas 2** puhul eemaldatud.
13. Vahekaardil **Projektimeeskond ja plaanimine** projekti **XYZ täiendusfaas 2** puhul veenduge, et töötaja, kelle 11. toimingus valisite, on lisatud kui **Tarkvaraarendaja**.

## <a name="requests-for-project-resources"></a>Projekti taotlusi
Projekti ressursside planeerimise funktsioon toetab ainult ressursihalduri jaotada rahalisi vahendeid kohustusi või projektid. Selle funktsiooni lubamiseks järgmistes või veenduge, et nad on lõpetanud.

-   Häälestage numbriseeriad.
-   Saate seadistada projektide juhtimise ja raamatupidamise töövood.
-   Võimaldavad ressursi taotluse töövoo.

Kui on tõendatud või täitmist eespool nimetatud ülesannetele, saate täita järgmisi ülesandeid vastavalt vajadusele.

-   Pehme broneeriti personaliga ressurss ressursi määramise loomine
-   Jälgida ressursi taotlusi.
-   Ressursi taotlusi täita.
-   Taotleda rahalisi ressursse WBS.
-   Raamat taotluseta personaliga ressurss projekti ressursse.

## <a name="monitor-project-teams"></a>Monitor projektimeeskonnad
1.  Klõpsake **projektijuhtimine raamatupidamis- ja**&gt;**projekti**&gt;**kõik projektid**.
2.  Klõpsake projektide loendis linki **Projekti ID** projekti **XYZ täiendusfaas 2** puhul.
3.  Veenduge, et kiirkaardil **Projektimeeskond ja plaanimine** loetletud projektiressursid on õiged.



