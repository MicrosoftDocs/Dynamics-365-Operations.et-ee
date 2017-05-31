---
title: Projekti ressursieraldus
description: Selles teemas antakse teavet projekti ressursieralduse kohta.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5c00c63e3c55e818934c36b818c90025002092d4
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="project-resourcing"></a>Projekti ressursieraldus

[!include[banner](../includes/banner.md)]


Selles teemas antakse teavet projekti ressursieralduse kohta.

Üks väljakutse projektijuhtide ja ressursihaldurite jaoks projekti plaanimisetapis on ressursside eraldamine, mille käigus nad peavad projektiga töötamiseks õige ressursi välja selgitama ja reserveerima. Microsoft Dynamics 365 for Operationsis saab projektide ressursieralduse võimaluste abil määratleda rolle, mida käsitletakse ajutiste ressurssidena, mille saab reserveerida konkreetsele tegevusele või tegevuse osale. Sedalaadi ressursieraldus võimaldab projektijuhtidel ja ressursihalduritel teha järgmisi toiminguid.

-   Määratleda ressursside sobitamise hõlbustamiseks rolli, millel on vajalikud kompetentsid.
-   Kasutada rolle reserveeritud ressurssidel põhineva algse tegevuse ajakava määratlemiseks.
-   Prognoosida kulusid ja määratleda algse eelarve, tuginedes projekti määratud rollidele ja ressurssidele.
-   Kasutada rolle iga tegevuse puhul vajalike ressursireserveeringute prognoosimiseks.
-   Hinnata kogu projekti töötsükli jaoks vajalike ressursside arvu.
-   Koostada projekti tööjaotuse struktuuri (WBS) esialgse ressursimäärangu abil.

[![Projekti elutsükkel](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Projekti plaanimise jätkumisel saab plaanitud ressursid asendada komplekteeritud ressurssidega. Projektijuht saab minna ka tagasi ja värskendada ressursieralduse reserveerimisi igas projekti etapis.

## <a name="set-up-project-resources"></a>Projekti ressursside seadistamine
Peate seadistama kalendri ja seostama selle töötajaga. Kalendrit kasutatakse projekti ja sellele reserveeritud ressursside tööaja plaanimiseks. Kalendri seadistamisel saavad projektijuhid ressursside optimeerimise käigus ressursse ühtlustada. Kalendrigraafiku alusel saab ressurssidele piiranguid seada. Kalendri saab seadistada lehel **Kalendrid**. 

Töötaja seadistamisel projekti ressursina saate valida töötajate hulgast, kes töötavad ettevõttes, millele ressursse seadistate, või teie organisatsiooni teiste ettevõtete töötajate hulgast. Need on kontsernisisesed ressursid. Järgmistes protseduurides selgitatakse, kuidas seadistada töötajat ettevõttes projektiressursina ja kuidas seadistada kontsernisisest projektiressurssi.

### <a name="set-up-a-worker-as-a-project-resource"></a>Töötaja seadistamine projekti ressursina

1.  Valige lehel **Töötajad** loendist **Töötajad** töötaja, kelle projekti ressursina lisate, ja avage töötaja kirje..
2.  Klõpsake tegumiribal valikuid **Projekt** &gt; **Seadistus** &gt; **Projekti seadistus**.
3.  Valige kalender ja sulgege siis leht.

Saate määrata eelmäärangu tüübina ressursile ka vaikeprojekte. Eelmääranguid saab kasutada, kui ressursihaldur või projektijuht teab ette, milliste projektidega ressurss töötama hakkab. Eelmäärangud võivad põhineda ka projekti sponsori või kliendi soovil. Projekti eelmääramiseks valige lehelt **Projektide määramine** vahekaardil **Projektid** loendis **Järelejäänud projektid** sobiv projekt.

### <a name="set-up-an-intercompany-resource"></a>Kontsernisisese ressursi seadistamine

Töötaja seadistamisel kontsernisisese ressursina peate tegema seadistuse välja laenavas ettevõttes ja laenuks võtvas ettevõttes. 

**Välja laenavas ettevõttes tehke järgmist.**

1.  Kontrollige Dynamics 365 for Operationsis, kas välja laenav ettevõte on valitud, ja läbige siis eespool kirjeldatud protseduur „Töötaja seadistamine projekti ressursina”.
2.  Avage **Pearaamat **&gt; **Sisestamise seadistus **&gt; **Kontserni raamatupidamine**. Klõpsake **Uus**.
3.  Valige väljalt **Juriidilise isiku ID **välja laenav ettevõte. Täitke vajalikul viisil ülejäänud väljad ja klõpsake siis käsku **Salvesta**.
4.  Avage **Projektihaldus ja raamatupidamine **&gt; **Seadistus **&gt; **Hinnad ** &gt; **Ülekande hind**.** **
5.  Klõpsake vormil **Ülekande hind **valikut **Uus** ja valige väljalt **Laenuks võttev juriidiline isik **vastav ettevõte.
6.  Kui soovite laenata laenuks võtvale ettevõttele ainult selle ressursi, mille jaotise alguses väljal **Ressurss** lõite, siis valige loodud ressursi nimi. Kui soovite teha laenuks võtvale ettevõttele kättesaadavaks kõik ettevõtte ressursid, siis jätke väli **Ressurss **tühjaks.
7.  Avage **Projektihaldus ja raamatupidamine **&gt; **Seadistus **&gt; **Projektihalduse ja raamatupidamise parameetrid** ja määrake vahekaardil **Kontsernisisene **välja **Luba kontsernisisene ressursside plaanimine ja ajatabelid **väärtuseks **Jah**.

**Laenuks võtvas ettevõttes tehke järgmist.**

1.  Avage **Projektihaldus ja raamatupidamine** &gt; **Projekti ressursid** &gt; **Ressursside loend**.
2.  Sisestage otsingufiltrisse eelmises protseduuris välja laenava ettevõtte jaoks loodud ressursi nimi, et kontrollida, kas see nimi sisaldub laenuks võtva ettevõtte ressursiloendis.

## <a name="manage-resource-competencies"></a>Ressursi kompetentside haldamine
Ressursi kompetentsid on ressursihalduse oluline osa. Kompetentse saab kasutada alusena ressursside määratlemiseks, kellel on õige oskuste, hariduse, tunnistuste ja projektikogemuse tasakaal. See teave tuleb igale ressursile määrata ja regulaarselt värskendada. Nii saate maksimeerida võimalusi, kui projekti ressursimääramise käigus konkreetsed ressursikompetentsid vastendatakse. [![Oskuste, tunnistuste, hariduse ja projektikogemuse näited](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Järgmistes protseduurides selgitatakse ressursi mõningate pädevuste seadistamist. 

Töötaja kompetentside seadistamiseks kasutatakse loendilehte **Töötajad** moodulis Inimressursid või loendilehte **Ressursid** moodulis Projektihaldus ja raamatupidamine. Järgmiste protseduuride puhul kasutatakse loendilehte **Töötajad** moodulis Inimressursid.

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
1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Tööruumid** &gt; **Projektihaldus**.
2.  Klõpsake valikut **Uus projekt** ja sisestage seejärel järgmised väärtused.
    -   **Projekti tüüp** – aeg ja materjal
    -   **Projekti nimi** – XYZ täiendusfaas 2
    -   **Projektigrupp** – TM\_WIP
    -   **Projektilepingu ID** – 00000002
3.  Klõpsake valikut **Loo projekt**.

### <a name="assign-a-resource-to-a-project"></a>Ressursi määramine projektile

1.  Klõpsake valikuid **Inimressursid** &gt; **Töötajad** &gt; **Töötajad**.
2.  Valige loendist **Töötajad** selle töötaja kirje, kelle jaoks eelnevalt kompetentsid seadistasite, ja avage töötaja kirje.
3.  Klõpsake tegumiriba vahekaardil **Projekt** grupis **Seadistus** valikut **Projektide määramine**.
4.  Klõpsake lehel **Ressursi kinnitamise projekti määrangud** vahekaarti **Projektid**.
5.  Filtreerige jaotises **Lisa projekt valitud projektidele** projekti XYZ täiendusfaas 2
6.  Valige paanilt **Järelejäänud projektid** projekt ja klõpsake siis noolt selle lisamiseks paanile **Valitud projektid**.
7.  Sulgege leht.

Vajaduse korral saate ka ressursile kategooriaid määrata. Kategooria tüüp on kulu või tulu. Selle määrab teie organisatsioon. Kui ressursile pole määratud ühtegi kategooriat, otsib Dynamics 365 for Operations üles kulu ja tulu tunnihindade vaikekategooria.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekti ressursi ja rolli omaduste seadistamine

Projektijuht saab kasutada projekti ressursieralduse funktsiooni projekti jaoks vajalike rollide loomiseks. Rolle saab kasutada siis, kui kinnitatud ressursid on ressursside reserveerimise ajal veel teadmata. Rolle saab reserveerida ajutiselt plaanitud ressurssidena, et saaksite projekti plaanimise etappe jätkata. 

[![Rolli näide](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Stsenaarium:** Contoso palgati täitma aja ja materjali projekti, millel on kinnitatud projekti põhikiri. Noorem-projektijuht täidab veel projekti ulatust. Ressursihaldur tuvastab praegu konkreetseid ressursse, mis uue projektiga töötamiseks reserveeritakse. Üks rollidest, mida projekti sponsor projekti olulise iseloomu tõttu soovis, on vanem-projektijuht. Ressursihaldur peab uue ressursi hankima ja määratlema rolli süsteemis, juhul kui noorem-projektijuht vajab projekti plaanimise käigus teavet ressursi kohta. 

Järgmised juhised näitavad, kuidas ressursihaldur saab vanem-projektijuhi rolli seadistada ja seostada sellega ressursi omadused. Hiljem saab rolli kasutada vajalikele ressursi kompetentsidele vastavate olemasolevate ressursside otsimiseks.

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Seadistus** &gt; **Ressursid** &gt; **Rollide seadistamine**.
2.  Klõpsake valikut **Uus** ja sisestage seejärel järgmised väärtused.
    -   **Rolli ID** – vanem-projektijuht
    -   **Kirjeldus** – vanem-projektijuht
3.  Klõpsake käsku **Loo**.
4.  Valige roll **Vanem-projektijuht** ja klõpsake siis valikut **Omaduste konfigureerimine**.
5.  Valige väljalt **Omaduse tüüp** väärtus **Oskus**.
6.  Sisestage väljale **Olemasolev omadus** oskus, mida otsite.
7.  Valige väljalt **Omaduse tüüp** väärtus **Tunnistus**.
8.  Sisestage väljale **Olemasolev omadus** tunnistuse tüüp, mida otsida.
9.  Klõpsake nuppu **OK** ja sulgege leht.

### <a name="assign-a-project-resource-to-a-project"></a>Projekti ressursi määramine projektile

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Üldine** &gt; **Projektid** &gt; **Kõik projektid** ja avage projekt **XYZ täiendusfaas 2**.
2.  Klõpsake vahekaardil **Projektimeeskond ja plaanimine** käsku **Lisa**.
3.  Valige väljalt **Roll** väärtus **Meeskonnaliige**.
4.  Klõpsake valikut **Kalendrist reserveerimine**.
5.  Klõpsake lehel **Ressursi saadavus** valikut **Kuva sätted**.
6.  Sisestage lehele **Kuvasätete kohandamine** järgmised väärtused.
    -   **Kuupäevavahemiku kuva jaoks vormindamine** – päev
    -   **Kuva saadavuse kirjeldused** – jah
    -   **Kuva järelejääv võimsus** – jah
7.  Valige ressursiloendist ressurss.
8.  Klõpsake valikuid **Fikseeritud reserveerimine** &gt; **Kogujõudlus**.
9.  Sulgege leht.

### <a name="assign-a-resource-to-a-default-role"></a>Vaikerollile ressursi määramine

Projekti- või ressursihaldurite abistamiseks võite minna veel rohkem süvitsi ressurssides, mida projektile reserveerida saab. Saate seostada vaikerolli olemasoleva ressursiga või äsja omandatud ressursiga. Näiteks kui Daniel palgati, olid tal kogemuse ja oskused ärianalüütiku rolli täitmiseks. Ressursihaldur määras selle rolli Danieli vaikerolliks. Seetõttu lisas ressursihaldur Danieli projektidega töötavate analüütikute kausta. 

Ressursi reserveerimise ajal saavad projektijuhid filtreerida rolli ressursse, mis on projektidega töötamiseks saadaval. Nad saavad kasutada neid andmeid ühe kriteeriumina, kui nad teevad ressursside täitmisel mitmel kriteeriumil põhinevaid analüüse. Samuti saavad nad lisada filtrile muid ressursiomadusi, et otsida antud projekti jaoks konkreetsete oskuste, hariduse ja kogemustega ressursse. 

**Stsenaarium:** kinnitatud projekt on alanud ja vanem-projektijuhi roll reserveeriti plaanitud ressursina projekti plaanimisetapi käigus. Ressursihaldur on nüüd hankinud ressursi vanem-projektijuhi rolli täitmiseks.

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Projekti ressursid** &gt; **Ressursside loend**.
2.  Valige loendist **Ressurss** väärtus **Daniel Goldschmidt**.
3.  Klõpsake valikuid **Projekti ressurss** &gt; **Halda** &gt; **Ressursiroll**.
4.  Klõpsake valikut **Uus** ja sisestage seejärel järgmised väärtused.
    -   **Jõustub** – (praegune kuupäev)
    -   **Aegub** – mitte kunagi
    -   **Roll** – vanem-projektijuht
5.  Klõpsake nuppu **Salvesta** ja sulgege seejärel leht.
6.  Lisage vahekaardile **Kompetentsid** oskus **ProjectMgmt** ja tunnistus **PMP**.

## <a name="set-up-role-based-pricing"></a>Rollipõhise hinnakujunduse seadistamine
Rollidele saab seadistada kõik kulud, müügi- ja sisehinnad.

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Seadistus** &gt; **Hinnad** &gt; **Müügihind (tund)**.
2.  Klõpsake **Uus**.
3.  Sisestage jõustumiskuupäev.
4.  Valige roll veerust **Roll**.
5.  Sisestage veergu **Hinnakujundus** valitud ressursi rolli hind.

## <a name="form-a-project-team"></a>Projektimeeskonna koostamine
Projektis eelnevalt seadistatud rollide kasutamiseks peab projektijuht need rollid projektiga seostama. Projektile saab määrata mitu rolli ja segaduse vältimiseks märgistab Dynamics 365 for Operations need rollid reserveerimise ajal automaatselt. Näiteks kui projektijuht vajab kolme tarkvarainseneri, luuakse automaatselt kolm tarkvarainseneri rolli, mille sildid on tarkvarainsener 1, tarkvarainsener 2 ja tarkvarainsener 3. Kui rollile olid eelnevalt määratud rolli omadused, rakendatakse need ressursi otsingute käigus filtrina. Otsingu täiendavaks täpsustamiseks saab omadusi lisada. 

Kuvasätteid saab samuti kohandada, et anda parem vaade ressursi saadavuse kohta. On olemas valikud saadavuse kuvamiseks tunnis, päevas, nädalas, kuus, kvartalis ja aastas. On olemas ka valik näidata ressursside olemasolevat ja järelejäänud mahtu. Sellest valikust on kasu aja juhtimisel, kui hindate tegevuste jaoks saadaolevat aega või ressursi kättesaadavust. 

Projektijuht võib valida lehelt rolli ja siis, kui on olemas vajadusele vastav kättesaadav ressurss, valida ressursi reserveerimise rolli täitmiseks. Pange tähele, et ressursse pole plaanimise etapi selles osas vaja reserveerida. WBS-i loomisel saate asendada rollid projekti komplekteeritud ressurssidega. Kui rollid asendatakse WBS-is komplekteeritud ressurssidega, värskendab ressursi seadistus automaatselt projektimeeskonna loendit ja plaanimist. 

[![Projekti töörühma loend, mis sisaldab nii rolle kui ka tegelikke ressursse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektijuhil on mitmesuguseid võimalusi projektile ressursi reserveerimiseks, nt **Järelejäänud võimsus**, **Täisvõimsus**, **Võimsuse protsent** ja **Tundide määramine**. Neid reserveerimisvalikuid saab ressursi määrangute muutumisel igal ajal tühistada. Toetatakse kahte reserveerimise tüüpi:

-   **Fikseeritud reserveerimine** – ressursi reserveerimine kinnitati töötamiseks tegevusega määratud perioodil.
-   **Esialgne reserveerimine** – ressurss reserveeriti esialgselt töötamiseks tegevusega määratud perioodil.

Järgmine protseduur selgitab, kuidas projektimeeskonda koostada.

### <a name="create-a-project-team"></a>Projektimeeskonna koostamine

1.  Valige loendilehelt **Kõik projektid** projekt ja klõpsake siis käsku **Redigeeri**.
2.  Sisestage vahekaardile **Projektimeeskond ja plaanimine** väljal **Graafiku lõppkuupäev** graafiku alguskuupäev pluss üks kuu. Näiteks kui graafiku alguskuupäev on 24. juuni 2017 (24/06/2017), sisestage **24/07/2017**.
3.  Klõpsake käsku **Lisa**.
4.  Valige paanilt **Projektile rollide lisamine** väljal **Roll**väärtus **Vanem-projektijuht**.
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

**Ressursi võimsuse kokkuvõtete sünkroonimine**

Sünkroonimisprotsess on mõeldud kogu ressursikalendri teabe sünkroonimiseks. See teave sisaldab peamist kalendriteavet kõigi muudatuste kohta projekti ressursikalendri võimsuse tabelis. Kui projektile lisatakse uusi ressursse, aitab sünkroonimine tagada, et värskendatud kalendriteave oleks saadaval. See sünkroonimine võib toimuda igal ajal. 

Soovitame kasutada partiid. Need valikud on võimsuse reserveerimiste sünkroonimisel saadaval.

-   Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Perioodiline** &gt; **Võimsuse sünkroonimine** &gt; **Ressursside võimsuse kokkuvõtete sünkroonimine**.

| Suvand | Kirjeldus                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jah    | sünkroonitakse kõik ressursi andmed kalendri ja peamise kalendri teabega ning asendatakse kogu teabe projekti ressursi võimsuse kalendris.                                                  |
| Ei     | sünkroonitakse ressursi andmed, tuginedes kuupäevavahemiku koodile ja määratud algus- ning lõppkuupäevale. See valik ei eemalda olemasolevaid andmeid ja värskendab ainult äsja lisatud ressursside teavet. |

[![Sünkroonimisprotsess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Rollide seadistamine WBS-i mallidel
Projektijuhid saavad seadistada WBS-i malle, mida saab rakendada uutele projektidele WBS-i loomisel. Projektijuhid saavad malli loomisel rolle lisada. Kasutage järgmist protseduuri rolli määramiseks WBS-i mallile.** **

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Seadistus** &gt; **Projektid** &gt; **Tööjaotuse struktuuri mallid**.
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
<td>Saate lisada automaatselt plaanitud ressursse, kasutades toiminguga seostatud rolle. Dynamics 365 for Operations soovitab automaatselt plaanitud ressursse, kasutades mitmel kriteeriumil põhinevat otsustamise analüüsi, mis põhineb rollidel. Pärast toimingutele WBS-is rollide ja panuse (tunnid) määramist ja struktuuri vabastamist klõpsake valikut <strong>Meeskonna automaatne loomine</strong>. Vajalik arv plaanitud ressursse lisatakse WBS-i ja vahekaardile <strong>Projekti ja meeskonna plaanimine</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurss (ripploend)</td>
<td>Lehel <strong>Ressursi määramise käivitamine </strong>saate valida ressursid fikseeritult või esialgselt reserveerimiseks, tuginedes määratud kestusele. Saate reguleerida kuvasätteid ressursi tegevuste vaatamiseks ja nende kestuse määramiseks. Saate valida ja määrata ressursse tööpaketi tasemel, kasutades järgmisi valikuid.
<ul>
<li><strong>Kinnita</strong> – ülesandele määratud ressursi muudatuste kinnitamine.</li>
<li><strong>Tühista</strong> – ülesandele määratud ressursi muudatuste tühistamine.</li>
<li><strong>Määra automaatselt</strong> – valitakse olemasolev komplekteeritud ressurss valitud toimingule vastava rolliga.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Projektid** &gt; **Kõik projektid**.
2.  Valige loendist projekt **XYZ täiendusfaas 2**.
3.  Klõpsake valikuid **Plaan** &gt; **Tegevused** &gt; **Tööjaotuse struktuur**.
4.  Klõpsake valikuid **Uus** järgmiste esimese taseme tegevuste lisamiseks WBS-i.
    -   Algatamine
    -   Planeerimine
    -   Teostamine
    -   Seire ja juhtimine
    -   Sule

5.  Määrake kuupäevad ja panus (tunnid) nii, nagu järgmisel ekraanipildil näidatud.[![Kuupäevade ja panuse seadistamine](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
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
16. Klõpsake valikuid **Esialgne määramine** &gt; **Täisvõimsus**.
17. Klõpsake nuppu **Salvesta** ja sulgege leht. 

> [!NOTE] 
> Te ei saa hoiatust, et määratud ressurss on nüüd 2, kuna ressursside arvuks jääb 1.
18. Kinnitage lehel **Tööjaotuse struktuur**WBS-is ressursi määrang ja klõpsake siis käsku **Salvesta**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressursi täitmine plaanitud ressursside puhul
Projektijuht saab plaanida projekti jaoks vajalikke ressursirolle. Ressursihaldur näeb neid plaanitud ressursse taotlustena lehel **Ressursi täitmine** ja saab määrata tegelikke ressursse.

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Projektid** &gt; **Kõik projektid**.
2.  Valige loendist projekt **XYZ täiendusfaas 2**.
3.  Klõpsake valikut **Projekt**.
4.  Klõpsake valikut **Redigeeri**.
5.  Klõpsake vahekaardil **Projektimeeskond ja plaanimine**** **käsku **Lisa**.
6.  Valige dialoogiboksist **Lisa rollid** roll **Tarkvaraarendaja**.
7.  Klõpsake käsku **Loo**.
8.  Sulgege projekti leht.
9.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Projekti ressursid** &gt; **Ressursi täitmine**.
10. Valige **Tarkvaraarendaja 1** projektile **XYZ täiendusprojekti faas 2**.
11. Valige töötaja ja klõpsake seejärel nuppu **Määra**.
12. Veenduge, et rida **Tarkvaraarendaja 1** oleks projekti **XYZ täiendusprojekti faas 2** puhul eemaldatud.
13. Vahekaardil **Projektimeeskond ja plaanimine** projekti **XYZ täiendusfaas 2** puhul veenduge, et töötaja, kelle 11. toimingus valisite, on lisatud kui **Tarkvaraarendaja**.

## <a name="requests-for-project-resources"></a>Projekti ressursside taotlused
Projekti ressursi plaanimise funktsioon toetab ressursihaldureid ainult komplekteeritud ressursside jagamisel tegevustele või projektidele. Selle funktsiooni lubamiseks tehke järgmised toimingud või veenduge, et need oleksid tehtud.

-   Häälestage numbriseeriad.
-   Seadistage projektihalduse ja raamatupidamise töövood.
-   Lubage ressursi taotluse töövoog.

Kui olete eespool nimetatud toiminguid kontrollinud või need ära teinud, saate teha vajaduse korral järgmisi toiminguid.

-   Luua esialgselt reserveeritud komplekteeritud ressursist ressursitaotlust.
-   Jälgida ressursitaotlusi.
-   Täita ressursitaotlusi.
-   Taotleda WBS-ilt komplekteeritud ressurssi.
-   Reserveerida projektile ressursse ilma komplekteeritud ressursi taotluseta.

## <a name="monitor-project-teams"></a>Jälgida projektimeeskondi
1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Projektid** &gt; **Kõik projektid**.
2.  Klõpsake projektide loendis linki **Projekti ID** projekti **XYZ täiendusfaas 2** puhul.
3.  Veenduge, et kiirkaardil **Projektimeeskond ja plaanimine** loetletud projektiressursid on õiged.





