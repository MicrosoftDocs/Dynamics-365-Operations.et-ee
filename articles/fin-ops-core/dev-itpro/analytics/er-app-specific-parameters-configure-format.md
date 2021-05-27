---
title: ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks
description: Selles teemas selgitatakse, kuidas saab konfigureerida elektroonilise aruandluse (ER) vorminguid juriidilise isiku kohta määratud parameetrite kasutamiseks.
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 0af3e1d589fd99cc722d8aedeb9596388a9e2e8c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018282"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Paljudes elektroonilise aruandluse (ER) vormingutes, mida loote, peate andmeid filtreerima, kasutades väärtuste kogumit, mis on omane igale teie eksemplari juriidilisele isikule (nt maksukoodide kogum maksukannete filtreerimiseks). Kui praegu on filtreerimine konfigureeritud ER-vormingus, kasutatakse andmete filtreerimisreeglite määratlemiseks ER-vormingu avaldistes väärtusi, mis sõltuvad juriidilisest isikust (nt maksukoode). Seetõttu on ER-vorming muudetud juriidilisele isikule omaseks, ja vajalike aruannete loomist peate looma tuletatud koopiad algsest ER-vormingust iga juriidilise isiku kohta, kus tuleb ER-vormingut käitada. Iga tuletatud ER-vormingut tuleb redigeerida, et tuua sellesse juriidilise isiku põhised väärtused, muuta alust iga kord, kui algversiooni (alust) värskendatakse, eksportida katsekeskkonnast ja importida tootmiskeskkonda, kui see tuleb juurutada kasutamiseks tootmises, jne. Seetõttu on seda tüüpi konfigureeritud ER-lahenduse hooldus keeruline ja aeganõudev mitmel põhjusel.

-   Mida rohkem on juriidilisi isikuid, seda rohkem ER-vormingu konfiguratsioone tuleb hooldada.
-   ER-konfiguratsioonide hoolduseks peavad ärikasutajatel olema ER-alased teadmised.

ER-i rakendusepõhiste parameetrite funktsiooniga saavad lauskasutajad konfigureerida andmete filtreerimist ER-vormingus, nii et see põhineb abstraktsete reeglite kogumil. Seda reeglite kogumit saab konfigureerida ER-vormingus saadaolevate andmeallikate kasutamiseks. Ärikasutajad saavad määrata reaalseid reegleid väljaspool ER-raamistikku, kasutades kasutajaliidest (UI), mis luuakse automaatselt vastava ER-vormingu ja praeguse juriidilise isiku andmete põhjal, millele pääseb ligi ER-vorgmingu andmeallikatega. ER-vormingu jaoks määratletud reeglite kogumit saab eksportida Dynamics 365 Finance’i (Finance) eksemplari praegusest juriidilisest isikust. Seda saab seejärel importida teise juriidilisse isikusse samas või mõnes teises Finance’i eksemplaris sama ER-vormingu reeglite kogumina.

## <a name="prerequisites"></a>Eeltingimused

Selle teema näidete läbimiseks peab teil ole juurdepääs teenuse Regulatory Configuration Services (RCS) eksemplarile, mis on eraldatud samale rentnikule kui rakendus Finance ühe järgmise rolli jaoks:

- Elektroonilise aruandluse arendaja
- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

Soovitame läbida etapid teemas [ARVUTATUD VÄLJATÜÜBI ER-andmeallikate parameetritega kõned](er-calculated-field-type.md). Kui olete need etapid juba läbinud, võite vahele jätta etapid järgmises jaotises **ER-konfiguratsioonide importimine RCS-i**.

## <a name="import-er-configurations-into-rcs"></a>ER-konfiguratsioonide importimine RCS-i

Laadige alla ja salvestage kohalikult järgmised ER-i konfiguratsioonid.

| **Sisu kirjeldus**                        | **Faili nimi**                                        |
|------------------------------------------------|------------------------------------------------------|
| **ER-i andmemudeli** konfiguratsioonifaili näidis    | [Mudel parameetritega calls.version.1.xml õppimiseks](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| **ER-i metaandmete** konfiguratsioonifaili näidis      | [Metaandmed parameetritega calls.version.1.xml õppimiseks](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| **ER-i mudelivastenduse** konfiguratsioonifaili näidis | [Vastendamine parameetritega calls.version.1.xml õppimiseks](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| **ER-vormingu** konfiguratsiooni näidis             | [Vorming parameetritega calls.version.1.xml õppimiseks](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

Järgmiseks logige sisse oma RCS-eksemplari.

Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Enne selle protseduuri läbimist peate läbima etapid RCS-i teemas [Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1.  Valige vaikimisi armatuurlaual **Elektrooniline aruandlus**.
2.  Valige **Aruandluse konfiguratsioonid**.
3.  Importige varem allalaaditud ER-i konfiguratsioonid RCS-i järgmises järjekorras: andmemudel, metaandmed, mudeli vastendamine ja vorming. Tehke iga ER-i konfiguratsiooniga järgmist.

    1.  Valige **Exchange**.
    2.  Valige **Laadi XML-failist**.
    3.  Valige käsk **Sirvi**, et valida nõutava ER-i konfiguratsiooni jaoks XML-vormingus fail.
    4.  Valige nupp **OK**.

## <a name="review-the-er-solution-that-is-provided"></a>Vaadake läbi esitatud ER-lahendus

1.  Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.
2.  Valige üksus **Vorming parameetritega kõnede õppimiseks**.
3.  Valige **Kujundaja**.
4.  Valige **Laienda/ahenda**.

    ER-vorming **Vorming parameetritega kõnede õppimiseks** on mõeldud XML-vormingus maksudeklaratsiooni loomiseks, millel kujutatakse mitut maksustamistaset (tavaline, vähendatud ja puudub). Igal tasemel on erinev arv üksikasju.

    ![ER-vormingu mitu taset, vorming parameetritega kutsete saamiseks](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Laiendage vahekaardil **Vastendamine** üksusi **Mudel**, **Andmed** ja **Kokkuvõte**.

    Andmeallikas **Model.Data.Summary** tagastab maksukannete loendi. Need kanded on kokku võetud maksukoodi järgi. Selle andmeallika jaoks on arvutatud väli **Model.Data.Summary.Level** konfigureeritud tagastama iga kokku võetud kirje maksustamistaseme koodi. Iga maksukoodi kohta, mida saab käitusajal tuua andmeallikast **Model.Data.Summary**, tagastab arvutatud väli maksustamistaseme koodi (**Tavaline**, **Vähendatud**, **Puudub** või **Muu**) tekstväärtusena. Arvutatud välja **Model.Data.Summary.Level** kasutatakse andmeallika **Model.Data.Summary** kirjete filtreerimiseks ja filtreeritud andmete sisestamiseks igasse XML-elementi, mis kujutavad maksustamistaset, kasutades välju **Model.Data2.Level1**, **Model.Data2.Level2** ja **Model.Data2.Level3**.

    ![Mudel.Andmed.Kokkuvõte andmeallikas maksukannete loendist](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Arvutatud väli **Model.Data.Summary.Level** on konfigureeritud nii, et see sisaldab ER-i avaldist. Maksukoodid (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** ja **InVAT0**) on sellesse konfiguratsiooni püsiprogrammeeritud. Seetõttu oleneb see ER-vorming juriidilisest isikust, kus maksukoodid konfigureeriti.

    ![Mudel.Andmed.Kokkuvõte.Tasandi kalkuleeritud väli koos püsiprogrammeeritud maksukoodidega](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Muu maksukoodide kogumi toetamiseks iga juriidilise isiku jaoks peate järgima järgmisi etappe.

    - Looge ER-vormingust iga juriidilise isiku jaoks tuletatud versioon.
    - Värskendage maksukoode arvutatud väljas **Model.Data.Summary.Level**, lähtudes juriidilise isiku sättest.

6.  Sulgege **Vormingu koostaja** leht.

## <a name="create-a-derived-format"></a>Tuletatud vormingu loomine

Järgmiseks kasutage ER-i rakendusepõhiste parameetrite funktsiooni, et toetada erinevaid maksukoodide kogumeid iga juriidilise isiku jaoks ühes ER-vormingus.

1.  Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.
2.  Valige üksus **Vorming parameetritega kõnede õppimiseks**.
3.  Valige **Konfiguratsiooni loomine**.
4.  Valige suvand **Tuleta nimest: vorming parameetritega kõnede õppimiseks, Microsoft**.
5.  Sisestage väljale **Nimi** suvand **Vorming LE-andmete otsingu õppimiseks**.
6.  Valige **Konfiguratsiooni loomine**.

## <a name="configure-a-derived-format"></a>Tuletatud vormingu konfigureerimine

### <a name="add-a-format-enumeration"></a>Vormingu loetelu lisamine

Järgmiseks lisage uus ER-vormingu loetelu. Selle vormingu loetelu väärtused esitatakse ärikasutajatele, kes määravad juriidilise isikust sõltuvad maksukoodide kogumid mitmesuguste maksustamistasemete jaoks, mida ER-vormingus kasutatakse.

1.  Valige **Kujundaja**.
2.  Valige suvand **Vormingu loetelud**.
3.  Valige **Lisa**.
4.  Väljale **Nimi** sisestage väärtus **Maksustamistasemete loend**.
5.  Valige käsk **Salvesta**.
6.  Vahekaardil **Vormingu loetelu väärtused** valige käsk **Lisa**.
7.  Väljale **Nimi** sisestage väärtus **Tavaline maksustamine**.
8.  Valige uuesti käsk **Lisa**.
9.  Väljale **Nimi** sisestage väärtus **Vähendatud maksustamine**.
10. Valige uuesti käsk **Lisa**.
11. Väljale **Nimi** sisestage väärtus **Maksustamine puudub**.
12. Valige uuesti käsk **Lisa**.
13. Väljale **Nimi** sisestage **Muu**.

    ![Uus kirje Vormingu loetelude lehel](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Kuna ärikasutajad võivad kasutada erinevaid keeli juriidilisest isikust sõltuvate maksukoodide kogumite määramiseks, soovitame teil tõlkida selle loetelu väärtused keeltesse, mis on konfigureeritud eelistatud keeltena nende kasutajate jaoks Finance’is.

14. Valige kirje **Maksustamine puudub**.
15. Klõpsake välja **Silt**.
16. Valige käsk **Tõlgi**.
17. Sisestage paanil **Teksti tõlge** väljale **Sildi ID** väärtus **LBL_LEVELENUM_NO**.
18. Sisestage väljale **Tekst vaikekeeles** väärtus **Maksustamine puudub**.
19. Sisestage väljale **Keel** väärtus **DE**.
20. Sisestage väljale **Tõlgitud tekst** väärtus **keine Besteuerung**.
21. Valige käsk **Tõlgi**.

    ![Teksti tõlke välja libisemine](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Valige käsk **Salvesta**.
23. Sulgege leht **Vormingu loetelud**.

### <a name="add-a-new-lookup-data-source"></a>Uue andmeallika otsimise lisamine

Järgmiseks lisage uus andmeallikas määramaks, kuidas ärikasutajad määravad juriidilisest isikust sõltuvaid reegleid õige maksustamistaseme tuvastamiseks iga kokkuvõtliku kande kirje jaoks.

1.  Valige vahekaardil **Vastendamine** käsk **Lisa**.
2.  Valige suvand **Vormingu loetelu\otsing**.

    Tuvastasite äsja, et iga reegel, mille ärikasutajad määravad maksustamistaseme tuvastamiseks, tagastavad ER-vormingu loetelu väärtuse. Pange tähele, et andmeallika tüübile **Otsing** pääseb ligi jaotisest **Andmemudel** ja **Dynamics 365 for Operations** i plokkidest lisaks plokile **Vormingu loetelu**. Seetõttu saab ER-i andmemudeli loetelusid ja rakenduse loetelusid kasutada väärtuste määramiseks, mis tagastatakse seda tüüpi andmeallikate kohta. Lisateavet **otsingu** andmeallikate kohta leiate teemast [Otsingu andmeallikate konfigureerimine ER-i rakendusekohaste parameetrite funktsiooni kasutamiseks](er-lookup-data-sources.md).
    
3.  Väljale **Nimi** sisestage suvand **Valija**.
4.  Väljalt **Vormingu loetelu** valige väärtus **Maksustamistasemete loend**.

    Määrasite, et iga selles andmeallikas määratud reegli kohta peab ärikasutaja valima ühe vormingu loetelu **Maksustamistasemete loend** väärtuse tagastatud väärtusena.
    
5.  Valige suvand **Otsingu redigeerimine**.
6.  Valige suvand **Veerud**.
7.  Laiendage üksust **Mudel**.
8.  Laiendage üksust **Andmed**.
9.  Laiendage üksust **Maks**.
10. Valige üksus **Model.Data.Tax.Code**.
11. Valige nupp **Lisa** (paremnool).

    ![Veerud libisevad välja](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Määrasite äsja, et iga maksustamistaseme tuvastamise selles andmeallikas määratud reegli kohta peab ärikasutaja valima tingimuseks ühe maksukoodi. Maksukoodide loend, mida ärikasutaja saab valida, tagastatakse andmeallikaga **Model.Data.Tax**. Kuna see andmeallikas sisaldab välja **Nimi**, kuvatakse maksukoodi nimi iga maksukoodi väärtuse kohta otsingus, mis esitatakse ärikasutajale.
    
12. Valige nupp **OK**.

    ![Otsingukujundaja leht](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Ärikasutajad saavad lisada selle andmeallika kirjetena mitu reeglit. Iga kirje nummerdatakse rea koodi järgi. Reegleid hinnatakse rea numbrite kasvavas järjekorras.

    Kuna valisite välja **Maksukood** reeglite tingimusena selles otsingu andmeallikas, ja kuna **Maksukood** on seadistatud andmetüübi **String** väljana, hinnatakse iga reeglit käitusajal, võrreldes maksukoodi, mis edastatakse andmeallikale, maksukoodiga, mis määratletakse andmeallika selles kirjes.

    Kui leitakse konfigureeritud tingimusele vastav reegel, tagastab see andmeallikas reegli otsinguväärtuse kohta, mis on määratletud väljas **Otsingu tulemus**. Kui ühtegi reeglit ei leita, esitatakse kasutajale erand, et andmeallikas ei saa õiget väärtust tagastada.

13. Valige käsk **Salvesta**.
14. Sulgege leht **Otsingu koostaja**.
15. Valige nupp **OK**.

    Pange tähele, et kui lisasite uue andmeallika, tagastab see maksustamistaseme vormingu loetelu **Maksustamistasemete loend** väärtuse mis tahes maksukoodi kohta, mis edastatakse andmeallikale andmetüübi **String** parameetri **Kood** argumendina.
    
    ![Vormingukujundaja leht koos uue andmeallikaga](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Konfigureeritud reeglite hindamine oleneb väljade andmetüübist, mis on valitud määratlema nende reeglite tingimusi. Kui valite välja, mis on konfigureeritud väljaks andmetüübile **Numbriline** või **Kuupäev**, erinevad kriteeriumid kriteeriumitest, mida kirjeldati varem andmetüübi **String** kohta. Väljade **Numbriline** ja **Kuupäev** korral tuleb reegel määrata väärtuste vahemikuna. Reegli tingimust peetakse täidetuks, kui andmeallikale edastatud väärtus jääb konfigureeritud vahemikku.
    
    Järgmisel joonisel on näide seda tüüpi seadistuse kohta. Peale välja **Model.Data.Tax.Code** andmetüübi **String** korral kasutatakse otsingu andmeallika tingimuste määramiseks välja **Model.Tax.Summary.Base** andmetüübi **Tegelik** korral.
    
    ![Otsingukujundaja leht lisaveergudega](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Kuna selle otsingu andmeallika jaoks valitakse väljad **Model.Data.Tax.Code** ja **Model.Tax.Summary.Base**, konfigureeritakse selle andmeallika iga reeglit järgmiselt.
    
    -   Esitatud loendist tuleb tagastatud väärtuseks valida vormingu loetelu **Maksustamistasemete loend** väärtus.
    -   Selle reegli tingimuseks tuleb määrata maksukood. Kehtivad ainult andmeallika **Model.Data.Tax** esitatud maksukoodid.
    -   Reegli tingimuseks tuleb sisestada maksu baassumma miinimum- ja maksimumväärtused.

    Käitusajal hinnatakse selle andmeallika iga reeglit järgmiselt.
    -   Kas andmetüübi **String** kood, mis edastatakse sellele andmeallikale, on võrdne reegli maksukoodiga?
    -   Kas andmetüübi **Tegelik** väärtus, mis edastatakse sellele andmeallikale, jääb miinimum- ja maksimumväärtuse vahele?

    Reeglit peetakse kehtivaks, kui mõlemad tingimused on täidetud.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Lisatud otsingu andmeallika sildi tõlkimine

Kuna ärikasutajad võivad kasutada erinevaid keeli juriidilisest isikust sõltuvate maksukoodide kogumite määramiseks, soovitame teil tõlkida iga lisatud otsingu andmeallika sildi, et see kuvataks vastaval lehel iga kasutaja valitud keeles.

1.  Valige andmeallikas **Model.Data.Selector**.
2.  Valige suvand **Redigeeri**.
3.  Klõpsake välja **Silt**.
4.  Valige käsk **Tõlgi**.
5.  Sisestage paanil **Teksti tõlge** väljale **Sildi ID** väärtus **LBL_SELECTOR_DS**.
6.  Sisestage väljale **Tekst vaikekeeles** väärtus **Vali maksutase maksukoodi järgi**.
7.  Sisestage väljale **Keel** väärtus **DE**.
8.  Sisestage väljale **Tõlgitud tekst** väärtus **Steuerebene für Steuerkennzeichen auswählen**.
9.  Valige käsk **Tõlgi**.
10. Valige nupp **OK**.

    ![Andmeallika atribuudid libisevad välja](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Konfigureeritud otsingu kasutamiseks uue välja lisamine

1.  Laiendage üksust **Model.Data**.
2.  Valige üksus **Model.Data.Summary**.
3.  Valige **Lisa**.
4.  Valige üksus **Funktsioonid / Arvutatud väli**.
5.  Väljale **Nimi** sisestage väärtus **LevelByLookup**.
6.  Valige **Valemi redigeerimine**.
7.  Sisestage väljale **Valem** väärtus **Model.Selector(Model.Data.Summary.Code)**.
8.  Valige käsk **Salvesta**.

    ![Mudeleid lisama.Valija(Mudel.Andmed.Kokkuvõte.Kood) vormingudisaineri lehele](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Sulgege leht **Valemiredaktor**.
10. Valige nupp **OK**.

    ![Vormingukujundaja leht koos uue lisatud vorminguga](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Pange tähele, et lisatud arvutatud väli **LevelByLookup** tagastab iga kokkuvõtliku maksukande kirje kohta vormingu loetelu **Maksustamistasemete loend** väärtusena maksustamistaseme. Kirje maksukood edastatakse otsingu andmeallikale **Model.Selector** ja selle andmeallika reeglite kogumit kasutatakse õige maksustamistaseme valimiseks.

### <a name="add-a-new-format-enumeration-based-data-source&quot;></a>Uue vormingu loetelul põhineva andmeallika lisamine

Järgmiseks lisage uus andmeallikas, mis viitab varem lisatud vormingu loetelule. Selle andmeallika väärtusi kasutatakse hiljem ER-vormingu avaldises.

1.  Valige **Lisa juur**.
2.  Valige suvand **Vormingu loetelud \ Loetelu**.
3.  Väljale **Nimi** sisestage väärtus **Maksustamise tase**.
4.  Väljalt **Vormingu loetelu** valige väärtus **Maksustamistasemete loend**.
5.  Valige käsk **Salvesta**.

### <a name=&quot;modify-an-existing-field-to-start-to-use-the-lookup&quot;></a>Olemasoleva välja muutmine otsingu kasutamise alustamiseks

Järgmiseks muutke olemasolevat arvutatud välja nii, et see kasutaks konfigureeritud otsingu andmeallikat õige maksustamistaseme väärtuse tagastamiseks olenevalt maksukoodist.

1.  Valige üksus **Model.Data.Summary.Level**.
2.  Valige suvand **Redigeeri**.
3.  Valige **Valemi redigeerimine**.

    Pange tähele, et välja **Model.Data.Summary.Level** praegune avaldis sisaldab järgmisi püsiprogrammeeritud maksukoode:
    
    CASE (@.Code, &quot;VAT19&quot;, &quot;Regular&quot;, &quot;InVAT19&quot;, &quot;Regular&quot;, &quot;VAT7&quot;, &quot;Reduced&quot;, &quot;InVAT7&quot;, &quot;Reduced&quot;, &quot;THIRD&quot;, &quot;None&quot;, &quot;InVAT0&quot;, &quot;None&quot;, &quot;Other")

4.  Sisestage väljale **Valem** väärtus **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Pange tähele, et välja **Model.Data.Summary.Level** avaldis tagastab nüüd maksustamistaseme, lähtudes praeguse kirje maksukoodist ja reeglite kogumist, mille ärikasutaja konfigureerib otsingu andmeallikas **Model.Data.Selector**.
    
5.  Valige käsk **Salvesta**.
6.  Sulgege leht **Valemikoostaja**.
7.  Valige nupp **OK**.
8.  Valige käsk **Salvesta**.
9.  Sulgege **Vormingu koostaja** leht.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Tuletatud vormingu mustandversiooni lõpetamine

1.  Vahekaardil **Versioonid** valige **Muuda olekut**.
2.  Valige **Lõpeta**.
3.  Valige nupp **OK**.

## <a name="export-completed-version-of-modified-format"></a>Muudetud vormingu lõpuleviidud versiooni eksportimine

1.  Valige konfiguratsioonipuust üksus **Vorming LE-andmete otsingu õppimiseks**.
2.  Valige kiirkaardil **Versioonid** kirje, mille olek on **Lõpule viidud**.
3.  Valige **Exchange**.
4.  Valige **Ekspordi XML-failina**.
5.  Valige nupp **OK**.
6.  Veebibrauser laadib alla faili **Format to learn how to lookup LE data.xml**. Salvestage see fail lokaalselt.

Korrake selle jaotise etappe vormingu **Vorming LE-andmete otsingu õppimiseks** ülemüksuste jaoks ja salvestage lokaalselt järgmised failid:

-   Format to learn parameterized calls.xml
-   Mapping to learn parameterized calls.xml
-   Model to learn parameterized calls.xml

Selleks et õppida konfigureeritud ER-vormingut **Vorming LE-andmete otsingu õppimiseks** kasutama juriidilisest isikust sõltuvate maksukoodide kogumite seadistamiseks, et filtreerida maksukandeid eri maksustamistasemete järgi, läbige etapid teemas [ER-vormingu parameetrite seadistamine juriidilise isiku kohta](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Lisaressursid

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse vormingu parameetrite häälestus juriidilise isiku kohta](er-app-specific-parameters-set-up.md)

[Andmeallikate otsingu konfigureerimine kasutama ER-i rakendusepõhiseid parameetrite funktsioone](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
