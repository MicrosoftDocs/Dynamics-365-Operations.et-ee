---
title: Mitmekeelsete aruannete kujundamine elektroonilises aruandluses
description: Selles teemas selgitatakse, kuidas saate kasutada elektroonilise aruandluse (ER) silte mitmekeelsete aruannete kujundamiseks ja loomiseks.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26a912aa2002f1d60dd650248bd3c68e45e68596
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810663"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Mitmekeelsete aruannete kujundamine elektroonilises aruandluses

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Ärikasutajana saate kasutada raamistikku [Elektrooniline aruandlus (ER)](general-electronic-reporting.md), et konfigureerida väljaminevate dokumentide vorminguid, mis tuleb luua eri riikide või regioonide õigusnõuete järgi. Kui nõuete järgi tuleb väljaminevad dokumendid luua eri riikide või regioonide jaoks mitmes keeles, saate konfigureerida ühe ER-i [vormingu](general-electronic-reporting.md#FormatComponentOutbound), mis sisaldab keelest sõltuvaid ressursse. Sel viisil saate vormingut kasutada mitmeid kordi, et luua väljaminevaid dokumente eri riikide või regioonide jaoks. Soovi korral võite kasutada üht ER-i vormingut, et luua väljaminev dokument eri keeltes asjakohastele klientidele, hankijatele, tütarettevõtetele või teistele pooltele.

Te saate konfigureerida ER-i andmemudeleid ja mudelivastendusi konfigureeritud ER-i vormingute andmeallikateks, et määratleda andmevoog, mis täpsustab, millised rakenduse andmed loodud dokumentidesse lisatakse. ER-i konfiguratsiooni[pakkujana](general-electronic-reporting.md#Provider) saate [avaldada](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) konfigureeritud [andmemudeleid](general-electronic-reporting.md#data-model-and-model-mapping-components), [mudelivastendusi](general-electronic-reporting.md#data-model-and-model-mapping-components) ja [vorminguid](general-electronic-reporting.md#FormatComponentOutbound) ER-i lahenduse komponentidena, et luua kindlaid väljaminevaid dokumente. Samuti saate lubada klientidel avaldatud ER-i lahendust [üles laadida](general-electronic-reporting-manage-configuration-lifecycle.md), et seda oleks võimalik kasutada ja kohandada. Kui te arvate, et kliendid võivad rääkida teises keeles, saate konfigureerida ER-i komponente nii, et need sisaldaksid keelest sõltuvaid ressursse. Sel viisil on võimalik kujundamise ajal esitada muudetava ER-i komponendi sisu kliendi eelistatud keeles.

Saate konfigureerida keelest sõltuvaid ressursse ER-i siltidena. Seejärel saate silte kasutada ER-i komponentide konfigureerimiseks järgmistel eesmärkidel.

- Kujundamise ajal

    - Esitage konfigureeritud ER-i komponentide sisu kasutaja eelistatud keeles.

- Käitusajal

    - Looge väljaminevate dokumentide jaoks keelest sõltuv sisu.
    - Lisage hoiatus-ja tõrketeated kasutaja eelistatud keeles.
    - Paluge kasutaja eelistatud keeles täita kohustuslikud väljad.

ER-i silte saab konfigureerida igas ER-i [konfiguratsioonis](general-electronic-reporting.md#Configuration), mis sisaldab eri komponente. Silte on võimalik hallata ER-i andmemudelite, ER-i mudelivastenduste ja ER-i vormingukomponentide konfigureeritud loogikast sõltumatult.

Iga ER-i silt on tuvastatav ID abil, mis on seda silti sisaldavas ER-i konfiguratsioonis kordumatu. Iga silt võib sisaldada silditeksti igas keeles, mida toetatakse praeguses Microsoft Dynamics 365 Finance'i eksemplaris. Toetatud keeled hõlmavad rakendatud kohanduste keeli.

## <a name="entry"></a>Kirje

ER-i andmemudeli, ER-i mudelivastenduse või ER-i vormingu loomisel kuvatakse suvand **Tõlgi** iga kord, kui valite välja, mis võib sisaldada tõlgitavat sisu. Selle suvandi valimisel saate valitud välja siduda ER-i sildiga <a name="TextTranslationPane">paanil</a> **Teksti tõlge**. Saate valida olemasoleva ER-i sildi või lisada uue ER-i sildi, kui see ei ole veel saadaval. ER-i sildi valimisel või lisamisel saate lisada seotud teksti iga keele jaoks, mida toetatakse praeguses Finance'i eksemplaris.

Järgmisel illustratsioonil on näha, kuidas toimib tõlkimine muudetavas ER-i andmemudelis. Selles näites on muudetava **Arve mudeli** välja **PurchaseOrder** atribuut **Kirjeldus** tõlgitud Austria saksa (DE-AT) ja jaapani (JA) keelde.

![ER-i sildi tõlkimine ER-i andmemudeli kujundajas](./media/er-multilingual-labels-refer.png)

Tõlkida saab ainult selliste siltide teksti, mis asuvad muudetavas ER-i komponendis. Näiteks kui valite ER-i mudelivastenduse andmeallikas oleva sildiatribuudi puhul suvandi **Tõlgi** ning valite seejärel ER-i emaandmemudelis oleva ER-i sildi, näete te sildi sisu, aga ei saa seda muuta. Sellistel juhtudel pole väli **Tõlgitud tekst** kättesaadav, nagu on näidatud järgmisel illustratsioonil.

![ER-i sildi tõlke ülevaatamine ER-i mudelivastenduse kujundajas](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Te ei saa kasutada kujundajaid, et kustutada silt, mis on sisestatud muudetavasse ER-i komponenti.

## <a name="scope"></a>Ulatus

ER-i siltidele saab viidata ER-i komponentide mitmes tõlgitavas atribuudis.

### <a name="data-model-component"></a>Andmemudeli komponent

ER-i andmemudeli konfigureerimisel saate sellele lisada ER-i silte. ER-i andmemudelisse lisatava ER-sildiga saab siduda mudeliüksuse atribuute **Silt** ja **Kirjeldus**, iga mudeli välju ja iga <a id="LinkModelEnum"></a>mudeli loendamisväärtust.

![Kirjeldusatribuudi tõlkimine ER-i andmemudeli kujundajas](./media/er-multilingual-labels-refer.png)

Kui ER-i andmemudel konfigureeritakse sel viisil, esitatakse selle sisu ER-i andmemudeli kujundaja kasutajatele nende eelistatud keeles. Seetõttu on mudeli haldamine lihtsam. Järgmistel illustratsioonidel on näha, kuidas see funktsioon töötab kasutajate puhul, kelle eelistatud keeleks on seatud DE-AT ja JA.

![ER-i andmemudeli kujundaja paigutus kasutaja puhul, kes on oma eelistatud keeleks seadnud keele DE-AT](./media/er-multilingual-labels-refer-de.png)

![ER-i andmemudeli kujundaja paigutus kasutaja puhul, kes on oma eelistatud keeleks seadnud keele JA](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Mudelivastenduse komponent

Kuna ER-i mudelivastendus põhineb ER-i andmemudelil, siis esitatakse viidatud andmemudeli elementide sildid mudelivastenduse kujundajas kasutaja eelistatud keeles. Järgmisel illustratsioonil on näha, kuidas selgitatakse muudetavas mudelivastenduses välja **PurchaseOrder** tähendust konfigureeritud andmemudelisse lisatud atribuudi **Kirjeldus** sildi abil. Pange tähele, et silt on esitatud kasutaja eelistatud keeles (selles näites DE-AT).

![ER-i mudelivastenduse kujundaja paigutus kasutaja puhul, kes on oma eelistatud keeleks seadnud keele DE-AT](./media/er-multilingual-labels-show-mapping.png)

Kui andmeallika **Kasutaja sisendparameeter** atribuut **Silt** on konfiguratsioonis seotud ER-i sildiga, esitatakse sellele andmeallikale vastav parameetriväli käitusajal kasutaja dialoogiboksis kasutaja eelistatud keeles.

### <a name="format-component"></a>Vormingu komponent

ER-i vormingu konfigureerimisel saate sellele lisada ER-i silte. Iga konfigureeritud andmeallika atribuute **Silt** ja **Spikritekst** on võimalik siduda ER-i sildiga, mis lisatakse ER-i vormingusse. Iga <a id="LinkFormatEnum"></a>vormingu loendamisväärtuse atribuute **Silt** ja **Kirjeldus** saab samuti siduda ER-i sildiga, millele pääseb juurde muudetavas ER-i vormingus.

> [!NOTE]
> Samuti saate need atribuudid siduda sellise ER-i emaandmemudeli ER-sildiga, mis taaskasutab mudeli silte igas ER-i vormingus, mis on selle ER-i andmemudeli jaoks konfigureeritud.

Kui ER-i vorming konfigureeritakse sel viisil, esitatakse vormingu sisu ER-i toimingute kujundaja kasutajatele nende eelistatud keeles. Seetõttu on vormingu haldamine ja konfigureeritud loogika analüüsimine lihtsam.

Kuna ER-i vorming põhineb ER-i andmemudelil, siis esitatakse andmemudeli elementides viidatud sildid ER-i vormingu kujundajas kasutaja eelistatud keeles.

Kui andmeallika **Kasutaja sisendparameeter** atribuut **Silt** on seotud ER-i sildiga, esitatakse parameetrile vastav väli käitusajal kasutaja dialoogiboksis viibana. Järgmistel illustratsioonidel on näha, kuidas siduda andmeallika **Kasutaja sisendparameeter** atribuut **Silt** kujundamise ajal ER-sildiga, et kasutajatelt küsitaks parameetrit käitusajal eri kasutaja eelistatud keeltes (näitena on toodud Ameerika Ühendriikide inglise (EN-US) keel ja keel DE-AT).

![Kasutaja sisendparameetri atribuutide tõlkimine ER-i toimingute kujundajas](./media/er-multilingual-labels-refer-format.png)

![ER-i hankija makse töötlemine käitusajal kasutaja eelistatud keeles EN-US](./media/er-multilingual-labels-show-runtime-en.png)

![ER-i hankija makse töötlemine käitusajal kasutaja eelistatud keeles DE-AT](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Avaldised

Sildi kasutamiseks ER-i [avaldises](er-formula-language.md) peate kasutama süntaksit **@"GER\_LABEL:X"**, kus eesliide **@** näitab, et operand viitab sildile, **GER\_LABEL** näitab, et kaasatud on ER-i silt, ja **X** on ER-sildi ID.

![Viidet ER-i sildile sisaldava ER-i avaldise konfigureerimine ER-i vormingu kujundajas](./media/er-multilingual-labels-expression1.png)

Süsteemi (rakenduse) sildile viitamiseks kasutage süntaksit **@"X"**, kus eesliide **@** näitab, et operand viitab sildile, ja **X** on süsteemi sildi ID.

![Viidet rakenduse sildile sisaldava ER-i avaldise konfigureerimine ER-i vormingu kujundajas](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Mudeli vastendamine

ER-i mudelivastenduse avaldist saab konfigureerida sildi abil. Kui seda vastendust kasutab ER-i vorming, mis käivitati väljamineva dokumendi loomiseks, sisaldab käivitamise kontekst keelekoodi. Konfigureeritud avaldise silt täidetakse sildi tekstiga, mis on konfigureeritud selle konteksti keele jaoks.

Kui viidatud sildil ei ole mudelivastendust kasutava vormingu käivitamise konteksti keele jaoks tõlget, kasutatakse selle asemel sildi teksti keeles EN-US.

#### <a name="format"></a>Vorming

ER-i vormingu ER-i avaldist saab konfigureerida siltide abil. Kui see vorming käivitatakse väljamineva dokumendi loomiseks, sisaldab käivitamise kontekst keelekoodi. Konfigureeritud avaldise silt täidetakse sildi tekstiga, mis on konfigureeritud selle konteksti keele jaoks.

![Muudetava ER-i avaldise ER-i sildi tõlkimine ER-i vormingu kujundajas](./media/er-multilingual-labels-refer-in-expression.png)

![ER-i sildile viitava andmeseose näide ER-i toimingute kujundajas](./media/er-multilingual-labels-refer-in-binding.png)

Aruande loomiseks kasutaja eelistatud keeles saate konfigureerida ER-i vormingu komponendi **FAIL**.

![ER-i toimingute kujundajas komponendi FAIL seadistamine aruande loomiseks kasutaja eelistatud keeles](./media/er-multilingual-labels-language-context-user.png)

Kui konfigureerite ER-i vormingu sel viisil, luuakse aruanne ER-i siltidest võetud sobiva teksti põhjal. Järgmistel illustratsioonidel on näha aruannete näited kasutaja keeltes EN-US ja DE-AT.

![Aruande eelvaade, mis on loodud kasutaja eelistatud keeles EN-US](./media/er-multilingual-labels-report-preview-en.png)

![Aruande eelvaade, mis on loodud kasutaja eelistatud keeles DE-AT](./media/er-multilingual-labels-report-preview-de.png)

Kui viidatud sildil ei ole vormingu käivitamise konteksti keele jaoks tõlget, kasutatakse selle asemel sildi teksti keeles EN-US.

## <a name="language"></a>Keel

ER toetab eri viise, kuidas määrata loodud aruande keel. Saate valida vahekaardi **Vorming** väljal **Keele-eelistused** järgmiste väärtuste vahel.

- **Ettevõtte eelistus** – looge aruanne ettevõtte määratud keeles.

    ![Ettevõtte eelistatud keele määramine loodud aruande keeleks ER-i toimingute kujundajas](./media/er-multilingual-labels-language-context-company.png)

- **Kasutaja eelistus** – looge aruanne kasutaja eelistatud keeles.
- **Selgelt määratletud** – looge aruanne keeles, mis määratakse kujundamise ajal.

    ![Kujundamise ajal määratletud keele määramine loodud aruande keeleks ER-i toimingute kujundajas](./media/er-multilingual-labels-language-context-fixed.png)

- **Käitusajal määratletud** – looge aruanne keeles, mis määratakse käitusajal. Kui valite selle väärtuse, konfigureerige väljal **Keel** ER-i avaldis, mis tagastab keele koodi, nt asjaomase kliendi keel.

    ![ER-i toimingute kujundajas käitusajal määratletud keele määramine loodud aruande keeleks](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="translation"></a>Tõlge

Saate lisada vajalikud ER-i sildid muudetavale ER-i komponendile. ER-i sildi lisamisel saab seda tõlkida kahel viisil: käsitsi ja automaatselt.

### <a name="manual-translation"></a>Käsitsi tõlkimine

Kui lisate **Teksti tõlkimise** [paanil](#TextTranslationPane) ER-i sildi, saate selle käsitsi tõlkida kõigisse keeltesse, mida toetatakse praeguses Finance'i eksemplaris. Valige eelistatud keel jaotise **Süsteemikeel** või **Kasutaja keel** väljal **Keel**, sisestage sobiv tekst asjakohasele väljale **Tõlgitud tekst** ja valige seejärel käsk **Tõlgi**. Seda protsessi tuleb korrata iga vajaliku keele ja iga lisatud sildi puhul.

### <a name="automatic-translation"></a>Automaatne tõlkimine

ER-i komponente konfigureeritakse sellise ER-i konfiguratsiooni mustandiversioonis, milles asub muudetav ER-i komponent.

![ER-i konfiguratsioonide leht, mis annab juurdepääsu mustandi olekus konfiguratsiooni versioonile](./media/er-multilingual-labels-configurations.png)

Nagu selles teemas eespool kirjeldatud, saate lisada muudetavale ER-i komponendile vajalikud ER-i sildid. Sel viisil saate täpsustada ER-i siltide teksti keeles EN-US. Seejärel saate eksportida ER-i komponendi sildid sisseehitatud ER-i funktsiooni abil. Valige muudetavat ER-i komponenti sisaldava ER-i konfiguratsiooni mustandiversioon ja valige seejärel **Vahetus \> Ekspordi sildid**.

![ER-i konfiguratsioonide leht, mis võimaldab eksportida ER-i silte valitud konfiguratsiooni versioonist](./media/er-multilingual-labels-export.png)

Saate eksportida kas kõik sildid või sildid ühe keele jaoks, mille määrate ekspordi alguses. Sildid eksporditakse ZIP-failina, mis sisaldab XML-faile. Iga XML-fail sisaldab silte ühe keele jaoks.

![Eksporditava faili näidis, mis sisaldab ER-i silte keele DE-AT jaoks](./media/er-multilingual-labels-in-xml.png)

Seda vormingut kasutatakse siltide automaatseks tõlkimiseks välise tõlketeenuse abil, nt [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md). Tõlgitud siltide kättesaamisel saate need importida tagasi sellise ER-i konfiguratsiooni mustandiversiooni, mis sisaldab neid silte omavaid ER-i komponente. Valige muudetavat ER-i komponenti sisaldava ER-i konfiguratsiooni mustandiversioon ja valige **Vahetus \> Laadi sildid**.

![ER-i konfiguratsioonide leht, mis võimaldab importida ER-i silte valitud konfiguratsiooni versiooni](./media/er-multilingual-labels-load.png)

Tõlgitud sildid imporditakse valitud ER-i konfiguratsiooni. Selles ER-i konfiguratsioonis leiduvad tõlgitud sildid asendatakse. Kui ER-i konfiguratsioonis pole mõnda tõlgitud silti, siis see lisatakse.

## <a name="lifecycle"></a>Töötsükkel

Muudetava ER-i komponendi silte hoitakse koos komponendi muu sisuga ER-i konfiguratsiooni sobivas versioonis.

ER-i aluskomponendi siltidele saab viidata ER-i komponendi tuletatud versioonis, mille te loote oma muudatuste tutvustamiseks.

ER-i versioonimine kontrollib sildi määramist ER-komponendi mis tahes atribuudile. Sildi määramise muudatused salvestatakse sellise muudetava ER-i komponendi muudatusloendisse (delta), mis on loodud antud ER-komponendi tuletatud versioonina. Need muudatused kinnitatakse, kui tuletatud versioon muutub uue alusversiooni aluseks.

## <a name="functions"></a>Funktsioonid

Sisseehitatud ER-i funktsioonil [LISTOFFIELDS](er-functions-list-listoffields.md) on juurdepääs ER-i siltidele, mis on konfigureeritud mõne ER-i komponendi jaoks.

Nagu selles teemas eespool kirjeldatud, saab asjakohases ER-i komponendis kättesaadava ER-i sildiga siduda iga [mudeli](#LinkModelEnum) või [vormingu](#LinkFormatEnum) ER-i loendamisväärtuse atribuute **Silt** ja **Kirjeldus**. Saate konfigureerida ER-i avaldise, milles kutsute ER-i loendamist argumendina kasutades välja funktsiooni **LISTOFFIELDS**. Avaldis tagastab loendi, mis sisaldab kirjet selle funktsiooni argumendina määratletud ER-i loendi iga väärtuse kohta. Iga kirje sisaldab ER-i loendamisväärtusega seotud ER-i sildi väärtust.

- Atribuudiga **Silt** seotud ER-i sildi väärtus salvestatakse tagastatud kirje väljale **Silt**.
- Atribuudiga **Kirjeldus** seotud ER-i sildi väärtus salvestatakse tagastatud kirje väljale **Kirjeldus**.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse funktsioonid](er-formula-language.md#functions)
