---
title: Mitmekeelsete aruannete kujundamine elektroonilises aruandluses
description: See artikkel selgitab, kuidas saate kasutada elektroonilise aruandluse (ER) silte mitmekeelsete aruannete loomiseks.
author: kfend
ms.date: 05/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 5575ba3154521e3855ce6b97c5b37d3c4868e3e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285481"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Mitmekeelsete aruannete kujundamine elektroonilises aruandluses

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Ärikasutajana saate kasutada raamistikku [Elektrooniline aruandlus (ER)](general-electronic-reporting.md), et konfigureerida väljaminevate dokumentide vorminguid, mis tuleb luua eri riikide või regioonide õigusnõuete järgi. Kui nõuete järgi tuleb väljaminevad dokumendid luua eri riikide või regioonide jaoks mitmes keeles, saate konfigureerida ühe ER-i vormingu, mis sisaldab keelest sõltuvaid ressursse. Sel viisil saate vormingut kasutada mitmeid kordi, et luua väljaminevaid dokumente eri riikide või regioonide jaoks. Soovi korral võite kasutada üht ER-i vormingut, et luua väljaminev dokument eri keeltes asjakohastele klientidele, hankijatele, tütarettevõtetele või teistele pooltele.

Te saate konfigureerida ER-i andmemudeleid ja mudelivastendusi konfigureeritud ER-i vormingute andmeallikateks, et määratleda andmevoog, mis täpsustab, millised rakenduse andmed loodud dokumentidesse lisatakse. ER-i konfiguratsiooni [pakkujana](general-electronic-reporting.md#Provider) saate avaldada konfigureeritud andmemudelid, mudelivastendused ja vormingud ER-lahenduse komponentidena kindlate [väljaminevate](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) dokumentide loomiseks. Samuti saate lubada klientidel avaldatud ER-i lahendust [üles laadida](general-electronic-reporting-manage-configuration-lifecycle.md), et seda oleks võimalik kasutada ja kohandada. Kui te arvate, et kliendid võivad rääkida teises keeles, saate konfigureerida ER-i komponente nii, et need sisaldaksid keelest sõltuvaid ressursse. Sel viisil on võimalik kujundamise ajal esitada muudetava ER-i komponendi sisu kliendi eelistatud keeles.

Saate konfigureerida keelest sõltuvaid ressursse ER-i siltidena. Seejärel saate silte kasutada ER-i komponentide konfigureerimiseks järgmistel eesmärkidel.

- Kujundamise ajal

    - Esitage konfigureeritud ER-i komponentide sisu kasutaja eelistatud keeles.

- Käitusajal

    - Looge väljaminevate dokumentide jaoks keelest sõltuv sisu.
    - Lisage hoiatus-ja tõrketeated kasutaja eelistatud keeles.
    - Paluge kasutaja eelistatud keeles täita kohustuslikud väljad.

ER-i silte saab konfigureerida igas ER-i [konfiguratsioonis](general-electronic-reporting.md#Configuration), mis sisaldab eri komponente. Silte on võimalik hallata ER-i andmemudelite, ER-i mudelivastenduste ja ER-i vormingukomponentide konfigureeritud loogikast sõltumatult.

Iga ER-i silt on tuvastatav ID abil, mis on seda silti sisaldavas ER-i konfiguratsioonis kordumatu. Iga silt võib sisaldada sildi teksti iga keele jaoks, mida praegune Microsoft Dynamics 365 Finantsid toetab. Toetatud keeled hõlmavad rakendatud kohanduste keeli.

## <a name="entry"></a>Kirje

ER-i andmemudeli, ER-i mudelivastenduse või ER-i vormingu loomisel kuvatakse suvand **Tõlgi** iga kord, kui valite välja, mis võib sisaldada tõlgitavat sisu. Selle suvandi valimisel saate valitud välja siduda ER-i sildiga <a name="TextTranslationPane">paanil</a> **Teksti tõlge**. Saate valida olemasoleva ER-i sildi või lisada uue ER-i sildi, kui see ei ole veel saadaval. ER-i sildi valimisel või lisamisel saate lisada seotud teksti iga keele jaoks, mida toetatakse praeguses Finance'i eksemplaris.

Järgmisel illustratsioonil on näha, kuidas toimib tõlkimine muudetavas ER-i andmemudelis. Selles näites on muudetava **Arve mudeli** välja **PurchaseOrder** atribuut **Kirjeldus** tõlgitud Austria saksa (DE-AT) ja jaapani (JA) keelde.

![ER-i sildi tõlkimine ER-i andmemudeli kujundajas.](./media/er-multilingual-labels-refer.png)

Tõlkida saab ainult selliste siltide teksti, mis asuvad muudetavas ER-i komponendis. Näiteks kui valite ER-i mudelivastenduse andmeallikas oleva sildiatribuudi puhul suvandi **Tõlgi** ning valite seejärel ER-i emaandmemudelis oleva ER-i sildi, näete te sildi sisu, aga ei saa seda muuta. Sellistel juhtudel pole väli **Tõlgitud tekst** kättesaadav, nagu on näidatud järgmisel illustratsioonil.

![ER-i sildi tõlke ülevaatamine ER-i mudelivastenduse kujundajas.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Te ei saa kasutada kujundajaid, et kustutada silt, mis on sisestatud muudetavasse ER-i komponenti.

## <a name="scope"></a>Ulatus

ER-i siltidele saab viidata ER-i komponentide mitmes tõlgitavas atribuudis.

### <a name="data-model-component"></a>Andmemudeli komponent

ER-i andmemudeli konfigureerimisel saate sellele lisada ER-i silte. ER-i andmemudelisse lisatava ER-sildiga saab siduda mudeliüksuse atribuute **Silt** ja **Kirjeldus**, iga mudeli välju ja iga <a id="LinkModelEnum"></a>mudeli loendamisväärtust.

![Kirjeldusatribuudi tõlkimine ER-i andmemudeli kujundajas.](./media/er-multilingual-labels-refer.png)

Kui ER-i andmemudel konfigureeritakse sel viisil, esitatakse selle sisu ER-i andmemudeli kujundaja kasutajatele nende eelistatud keeles. Seetõttu on mudeli haldamine lihtsam. Järgmistel illustratsioonidel on näha, kuidas see funktsioon töötab kasutajate puhul, kelle eelistatud keeleks on seatud DE-AT ja JA.

![ER-i andmemudeli kujundaja paigutus kasutaja puhul, kes on määranud eelistatud keeleks DE-AT.](./media/er-multilingual-labels-refer-de.png)

![ER-i andmemudeli kujundaja paigutus kasutaja puhul, kes on määranud eelistatud keeleks JA.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Mudelivastenduse komponent

Kuna ER-mudeli vastendamine põhineb ER-andmemudelil, kuvatakse viidatud andmemudeli elementide sildid mudeli vastendamise kujundajas kasutaja eelistatud keeles. Järgmisel illustratsioonil on näha, kuidas selgitatakse muudetavas mudelivastenduses välja **PurchaseOrder** tähendust konfigureeritud andmemudelisse lisatud atribuudi **Kirjeldus** sildi abil. Pange tähele, et silt on esitatud kasutaja eelistatud keeles (selles näites DE-AT).

![ER-i mudelivastenduse kujundaja paigutus kasutaja puhul, kes on määranud eelistatud keeleks DE-AT.](./media/er-multilingual-labels-show-mapping.png)

Kui andmeallika **Kasutaja sisendparameeter** atribuut **Silt** on konfiguratsioonis seotud ER-i sildiga, esitatakse sellele andmeallikale vastav parameetriväli käitusajal kasutaja dialoogiboksis kasutaja eelistatud keeles.

### <a name="format-component"></a>Vormingu komponent

ER-i vormingu konfigureerimisel saate sellele lisada ER-i silte. Iga konfigureeritud andmeallika atribuute **Silt** ja **Spikritekst** on võimalik siduda ER-i sildiga, mis lisatakse ER-i vormingusse. Iga **vormingu** loeteluväärtuse **sildi** ja kirjelduse atribuute saab linkida ka ER-sildiga, millele on juurdepääs redigeeritavast <a id="LinkFormatEnum"></a> ER-vormingust.

> [!NOTE]
> Samuti saate need atribuudid siduda sellise ER-i emaandmemudeli ER-sildiga, mis taaskasutab mudeli silte igas ER-i vormingus, mis on selle ER-i andmemudeli jaoks konfigureeritud.

Kui ER-i vorming konfigureeritakse sel viisil, esitatakse vormingu sisu ER-i toimingute kujundaja kasutajatele nende eelistatud keeles. Seetõttu on vormingu haldamine ja konfigureeritud loogika analüüsimine lihtsam.

Kuna ER-i vorming põhineb ER-i andmemudelil, siis esitatakse andmemudeli elementides viidatud sildid ER-i vormingu kujundajas kasutaja eelistatud keeles.

Kui andmeallika **Kasutaja sisendparameeter** atribuut **Silt** on seotud ER-i sildiga, esitatakse parameetrile vastav väli käitusajal kasutaja dialoogiboksis viibana. Järgmistel illustratsioonidel on näha, kuidas siduda andmeallika **Kasutaja sisendparameeter** atribuut **Silt** kujundamise ajal ER-sildiga, et kasutajatelt küsitaks parameetrit käitusajal eri kasutaja eelistatud keeltes (näitena on toodud Ameerika Ühendriikide inglise (EN-US) keel ja keel DE-AT).

![Kasutaja sisendparameetri atribuutide tõlkimine ER-i toimingute kujundajas.](./media/er-multilingual-labels-refer-format.png)

![ER-i hankija makse töötlemine käitusajal kasutaja eelistatud keeles EN-US.](./media/er-multilingual-labels-show-runtime-en.png)

![ER-i hankija makse töötlemine käitusajal kasutaja eelistatud keeles DE-AT.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Avaldised

Sildi kasutamiseks ER-i [avaldises](er-formula-language.md) peate kasutama süntaksit **@"GER\_LABEL:X"**, kus eesliide **@** näitab, et operand viitab sildile, **GER\_LABEL** näitab, et kaasatud on ER-i silt, ja **X** on ER-sildi ID.

![Viidet ER-i sildile sisaldava ER-i avaldise konfigureerimine ER-i vormingu kujundajas.](./media/er-multilingual-labels-expression1.png)

Süsteemi (rakenduse) sildile viitamiseks kasutage süntaksit **@"X"**, kus eesliide **@** näitab, et operand viitab sildile, ja **X** on süsteemi sildi ID.

![Viidet rakenduse sildile sisaldava ER-i avaldise konfigureerimine ER-i vormingu kujundajas.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Mudeli vastendamine

ER-i mudelivastenduse avaldist saab konfigureerida sildi abil. Kui seda vastendust kasutab ER-i vorming, mis käivitati väljamineva dokumendi loomiseks, sisaldab käivitamise kontekst keelekoodi. Konfigureeritud avaldise silt täidetakse sildi tekstiga, mis on konfigureeritud selle konteksti keele jaoks.

Kui viidatud sildil ei ole mudelivastendust kasutava vormingu käivitamise konteksti keele jaoks tõlget, kasutatakse selle asemel sildi teksti keeles EN-US.

#### <a name="format"></a>Vorming

ER-i vormingu ER-i avaldist saab konfigureerida siltide abil. Kui see vorming käivitatakse väljamineva dokumendi loomiseks, sisaldab käivitamise kontekst keelekoodi. Konfigureeritud avaldise silt täidetakse sildi tekstiga, mis on konfigureeritud selle konteksti keele jaoks.

![Muudetava ER-i avaldise ER-i sildi tõlkimine ER-i vormingu kujundajas.](./media/er-multilingual-labels-refer-in-expression.png)

![ER-i sildile viitava andmeseose näide ER-i toimingute kujundajas.](./media/er-multilingual-labels-refer-in-binding.png)

Aruande loomiseks kasutaja eelistatud keeles saate konfigureerida ER-i vormingu komponendi **FAIL**.

![ER-i toimingute kujundajas komponendi FAIL seadistamine aruande loomiseks kasutaja eelistatud keeles.](./media/er-multilingual-labels-language-context-user.png)

Kui konfigureerite ER-i vormingu sel viisil, luuakse aruanne ER-i siltidest võetud sobiva teksti põhjal. Järgmistel illustratsioonidel on näha aruannete näited kasutaja keeltes EN-US ja DE-AT.

![Aruande eelvaade, mis on loodud kasutaja eelistatud keeles EN-US.](./media/er-multilingual-labels-report-preview-en.png)

![Aruande eelvaade, mis on loodud kasutaja eelistatud keeles DE-AT.](./media/er-multilingual-labels-report-preview-de.png)

Kui viidatud sildil ei ole vormingu käivitamise konteksti keele jaoks tõlget, kasutatakse selle asemel sildi teksti keeles EN-US.

> [!TIP]
> Väljamineva faili loomist **saate** kasutada **faili komponentide kausta** ja eristatavaid tüüpe redigeeritavas ER-vormingus. Loodud failile nime loomiseks konfigureerige komponendi failinime parameetrile [ER-avaldis.](er-formula-language.md)**·** Silte saate kasutada konfigureeritud avaldises. Kuna faili **nime** parameeter on vaikimisi keelest prognoosiv, kuvatakse kõikide selles avaldises viidatavate siltide tekst käitusajal EN-US vaikekeeles. Versioonis 10.0.28 **ja uuemates versioonides saate siiski lubada parameetri Keele-eelistuse rakendada avaldise "Faili nimi" funktsioonile**. Failinime **avaldis** võtab seejärel **arvutamisel** arvesse keele-eelistuste parameetrit.

## <a name="language"></a>Keel

ER toetab eri viise, kuidas määrata loodud aruande keel. Saate valida vahekaardi **Vorming** väljal **Keele-eelistused** järgmiste väärtuste vahel.

- **Ettevõtte eelistus** – looge aruanne ettevõtte määratud keeles.

    ![Ettevõtte eelistatud keele määramine loodud aruande keeleks ER-i toimingute kujundajas.](./media/er-multilingual-labels-language-context-company.png)

- **Kasutaja eelistus** – looge aruanne kasutaja eelistatud keeles.
- **Selgelt määratletud** – looge aruanne keeles, mis määratakse kujundamise ajal.

    ![Kujundamise ajal määratletud keele määramine loodud aruande keeleks ER-i toimingute kujundajas.](./media/er-multilingual-labels-language-context-fixed.png)

- **Käitusajal määratletud** – looge aruanne keeles, mis määratakse käitusajal. Kui valite selle väärtuse, konfigureerige väljal **Keel** ER-i avaldis, mis tagastab keele koodi, nt vastava kliendi keel.

    ![ER-i toimingute kujundajas käitusajal määratletud keele määramine loodud aruande keeleks.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Kultuuripõhine vormindamine

ER toetab erinevaid viise, kuidas määrata loodud aruande kultuuri. Seetõttu saab kuupäeva, kellaaja ja numbriväärtuste puhul kasutada õiget kultuurispetsiifilist vormingut. ER-vormingu kujundamisel saate vahekaardi **Vorming** väljal **Kultuuri-eelistused** valida ühe järgmistest väärtustest iga vormingukomponendi kohta **tavapärase\\faili**, **Exceli\\faili**, **PDF-\\faili** või **PDF\\Mergeri** tüübi kohta:

- **Kasutaja eelistus** – vormindage väärtused vastavalt kasutaja eelistatud kultuurile. See kultuur on määratletud **kasutaja suvandite** lehe vahekaardi **Eelistused** väljal **Kuupäev, kellaaeg ja numbrivorming**.

    ![Kasutaja eelistatud kultuuri määratlemine ER-i toimingukujundajas loodud aruande kultuuriks.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Eraldi määratletud** – vormindage väärtused vastavalt kujunduse jooksul määratud kultuurile.

    ![Disaini ajal määratud kultuuri määratlemine ER-i toimingukujundajas loodud aruande kultuuriks.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Käitusajal määratletud** – vormindage väärtused vastavalt käitusaja jooksul määratud kultuurile. Kui valite selle väärtuse vahekaardi **Vastendamine** väljal **Kuupäev, kellaaeg ja numbrivorming**, konfigureerige ER-avaldis, mis tagastab kultuuri koht kultuurikoodi, nt vastava kliendi kultuuri.

    ![Käituse ajal määratud kultuuri määratlemine ER-i toimingukujundajas loodud aruande kultuuriks.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> ER-i komponent, mille jaoks määratlete kindla kultuuri, võib sisaldada tütar-ER-komponente, mis on konfigureeritud tekstiväärtuse sisestamiseks. Vaikimisi kasutatakse emakomponendi kultuuri nende komponentide väärtuste vormindamiseks. Järgmiste sisseehitatud ER-funktsioonide abil saate konfigureerida nende komponentide seoseid ja rakendada väärtuse vormindamiseks alternatiivset kultuuri:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> Versioonis 10.0.20 ja uuemates formaadikomponentides kasutatakse **Common\\failitüüpi** ja **Exceli\\failitüüpi**, et vormindada väärtusi loodud dokumendist [PDFi teisendamisel](electronic-reporting-destinations.md#OutputConversionToPDF).

## <a name="translation"></a>Tõlge

Saate lisada vajalikud ER-i sildid muudetavale ER-i komponendile. ER-i sildi lisamisel saab seda tõlkida kahel viisil: käsitsi ja automaatselt.

### <a name="manual-translation"></a>Käsitsi tõlkimine

Kui lisate **Teksti tõlkimise** [paanil](#TextTranslationPane) ER-i sildi, saate selle käsitsi tõlkida kõigisse keeltesse, mida toetatakse praeguses Finance'i eksemplaris. Valige eelistatud keel jaotise **Süsteemikeel** või **Kasutaja keel** väljal **Keel**, sisestage sobiv tekst asjakohasele väljale **Tõlgitud tekst** ja valige seejärel käsk **Tõlgi**. Seda protsessi tuleb korrata iga vajaliku keele ja iga lisatud sildi puhul.

### <a name="automatic-translation"></a>Automaatne tõlkimine

ER-i komponente konfigureeritakse sellise ER-i konfiguratsiooni mustandiversioonis, milles asub muudetav ER-i komponent.

![ER-i konfiguratsioonide leht, mis annab juurdepääsu mustandi olekus konfiguratsiooni versioonile.](./media/er-multilingual-labels-configurations.png)

Nagu selles artiklis varem kirjeldatud, saate lisada nõutavad ER-sildid redigeeritavale ER-komponendile. Sel viisil saate täpsustada ER-i siltide teksti keeles EN-US. Seejärel saate eksportida ER-i komponendi sildid sisseehitatud ER-i funktsiooni abil. Valige muudetavat ER-i komponenti sisaldava ER-i konfiguratsiooni mustandiversioon ja valige seejärel **Vahetus \> Ekspordi sildid**.

![ER-i konfiguratsioonide leht, mis võimaldab eksportida ER-i silte valitud konfiguratsiooni versioonist.](./media/er-multilingual-labels-export.png)

Saate eksportida kas kõik sildid või sildid ühe keele jaoks, mille määrate ekspordi alguses. Sildid eksporditakse ZIP-failina, mis sisaldab XML-faile. Iga XML-fail sisaldab silte ühe keele jaoks.

![Eksporditava faili näidis, mis sisaldab ER-i silte keele DE-AT jaoks.](./media/er-multilingual-labels-in-xml.png)

Seda vormingut kasutatakse siltide automaatseks tõlkimiseks välise tõlketeenuse abil, nt [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md). Tõlgitud siltide kättesaamisel saate need importida tagasi sellise ER-i konfiguratsiooni mustandiversiooni, mis sisaldab neid silte omavaid ER-i komponente. Valige muudetavat ER-i komponenti sisaldava ER-i konfiguratsiooni mustandiversioon ja valige **Vahetus \> Laadi sildid**.

![ER-i konfiguratsioonide leht, mis võimaldab importida ER-i silte valitud konfiguratsiooni versiooni.](./media/er-multilingual-labels-load.png)

Tõlgitud sildid imporditakse valitud ER-i konfiguratsiooni. Selles ER-i konfiguratsioonis leiduvad tõlgitud sildid asendatakse. Kui ER-i konfiguratsioonis pole mõnda tõlgitud silti, siis see lisatakse.

## <a name="lifecycle"></a>Töötsükkel

Muudetava ER-i komponendi silte hoitakse koos komponendi muu sisuga ER-i konfiguratsiooni sobivas versioonis.

ER-i aluskomponendi siltidele saab viidata ER-i komponendi tuletatud versioonis, mille te loote oma muudatuste tutvustamiseks.

> [!TIP]
> ER-lahenduse kujundamisel saate esitatud andmetest tuletada oma ER [andmemudeli](er-overview-components.md#data-model-component) komponendi. Selles tuletatud andmemudelis saate tutvustada oma ER-silte ja kasutada neid kõigis ER-vormingutes, mis kasutavad andmeallikana andmemudelit. Seejärel saate tuletatud ER-vormingu [komponendi](er-overview-components.md#format-component) tuletada antud ER-i andmemudeli asemel antud komponendist. Versioonis 10.0.28 ja uuemates versioonides saate lubada täiustatud juurdepääsu ER andmemudeli tüübi siltidele kasvava ER-i andmemudeli siltidele tuletatud ER-vormingu komponentides isegi siis, **kui tuletatud ER-i komponendi jaoks valitud ER-andmemudel** erineb sellest, mida kasutati ER-põhikomponendis.
>
> Kui tuletatud komponendis ja selle kasvavas komponendis kasutatakse sama sildinime, kasutatakse kõige asjakohasema sildi tõlget.

ER-i versioonimine kontrollib sildi määramist ER-komponendi mis tahes atribuudile. Sildi määramise muudatused salvestatakse sellise muudetava ER-i komponendi muudatusloendisse (delta), mis on loodud antud ER-komponendi tuletatud versioonina. Need muudatused kinnitatakse, kui tuletatud versioon muutub uue alusversiooni aluseks.

## <a name="functions"></a>Funktsioonid

Sisseehitatud ER-i funktsioonil [LISTOFFIELDS](er-functions-list-listoffields.md) on juurdepääs ER-i siltidele, mis on konfigureeritud mõne ER-i komponendi jaoks.

Nagu selles artiklis varem kirjeldatud, **·** **saab** iga mudeli või vormingu ER-loetelu väärtuse sildi ja kirjelduse atribuudid linkida vastavas ER-komponendis [...](#LinkModelEnum)[juurdepääsetava](#LinkFormatEnum) ER-sildiga. Saate konfigureerida ER-i avaldise, milles kutsute ER-i loendamist argumendina kasutades välja funktsiooni **LISTOFFIELDS**. Avaldis tagastab loendi, mis sisaldab kirjet selle funktsiooni argumendina määratletud ER-i loendi iga väärtuse kohta. Iga kirje sisaldab ER-i loendamisväärtusega seotud ER-i sildi väärtust.

- Atribuudiga **Silt** seotud ER-i sildi väärtus salvestatakse tagastatud kirje väljale **Silt**.
- Atribuudiga **Kirjeldus** seotud ER-i sildi väärtus salvestatakse tagastatud kirje väljale **Kirjeldus**.

## <a name="performance"></a><a name=performance></a>Jõudlus

Kui konfigureerite ER-vormingu komponenti, et luua aruanne eelistatud [keeles](#language), või importida sissetulev dokument, kus sisu sõelutakse eelistatud keele järgi, on soovitatav lubada funktsioonihalduse tööruumis **praeguse kasutaja eelistatud keel** funktsioon [Funktsioonihalduse](../../fin-ops/get-started/feature-management/feature-management-overview.md) tööruumis. See funktsioon aitab parandada jõudlust, eriti ER-vormingu komponentide puhul, mis sisaldavad mitmeid viiteid ER-i valemite ja sidumiste [siltidele](general-electronic-reporting-formula-designer.md#TestFormula) ning palju kinnitusreegliid eelistatud keelekasutajateadete loomiseks.

Kui muudate ER-i **konfiguratsiooniversiooni** **oleku** mustandist olekusse Lõpetatud, kui konfiguratsiooniversioon sisaldab ER-silte, talletatakse need sildid rakenduse andmebaasis. Ladustamisskeem sõltub ER-siltide **talletamisfunktsiooni kiirendamise olekust**:

- Kui funktsioon pole lubatud, **talletatakse kõik sildid tabeli ERSOLUTIONVERSIONTABLE** VÄLJALE LABELXML **üksiku** XML-ilõiguna.
- Kui see funktsioon on lubatud, luuakse iga keele kohta eraldi **kirje tabelis ERSOLUTIONVERSIONLABELSTABLE**. Selle **tabeli** sisu väli talletab keele sildid tihendatud XML-ilõiguna.

Funktsioonihalduse tööruumis pole **soovitatav lubada ER-siltide** talletamisfunktsiooni **kiirendamine**. See funktsioon aitab parandada võrgu ribalaiust ja üldist süsteemi jõudlust, sest enamasti kasutatakse üksiku ER-i konfiguratsiooniga töötades ühe keele ER-silte.

Valitud ladustamisskeemi rakendamiseks kõigi ER-i konfiguratsioonide siltide säilitamiseks praeguses finantseksemplaris viige lõpule järgmised sammud.

1. Avage organisatsiooni **haldus perioodiline** > **rakendage** > **valitud silte, mis talletavad skeemi kõigi ER konfiguratsioonide jaoks**.
2. Valige nupp **OK**.


## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse funktsioonid](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
