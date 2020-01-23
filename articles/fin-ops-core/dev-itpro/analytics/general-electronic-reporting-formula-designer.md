---
title: Valemikoostaja elektroonilises aruandluses (ER)
description: See teema sisaldab teavet selle kohta, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0028d1f64aced1bbff91b18456c81adbb95bce30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914814"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Valemikoostaja elektroonilises aruandluses (ER)

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas kasutada elektroonilises aruandluses (ER) valemikoostajat. ER-is kindla elektroonilise dokumendi vormingu koostamisel saate kasutada valemeid andmete teisendamiseks, et vastata selle dokumendi täitmise ja vormindamise nõuetele. Need valemid sarnanevad Microsoft Exceli valemitega. Valemites toetatakse erinevat tüüpi funktsioone: tekst, kuupäev ja kellaaeg, matemaatiline, loogika, teave ja andmetüübi teisendamise funktsioonid ning samuti teised ettevõtte domeenipõhised funktsioonid.

## <a name="formula-designer-overview"></a>Valemikoostaja ülevaade

ER toetab valemikoostajat. Seega saate koostamise ajal konfigureerida avaldisi, misa saab kasutada käitamisel järgmisteks ülesanneteks.

- Muutke rakenduse andmebaasist saadud andmeid. Need peavad olema sisestud ER-i andmemudelisse, mis on kavandatud ER-vormingute andmeallikaks. (Näiteks võivad need teisendused hõlmata filtreerimist, grupeerimist ja andmetüübi konversiooni.)
- Andmete vormindamine, mis tuleb saata loodavale elektroonilisele dokumendile kindla ER-vormingu paigutuse ja tingimuste järgi. (Näiteks võidakse vormindada kooskõlas nõutava keele, kultuuri või kodeeringuga).
- Elektrooniliste dokumentide loomise protsessi juhtimine. (Näiteks saavad avaldised olenevalt andmete töötlemisest vormingu teatud elementide arvestamist lubada või keelata. Nad saavad ka katkestada dokumentide loomisprotsessi või saata lõppkasutajatele sõnumeid.)

**Valemikoostaja** lehe saate avada järgmiste tegevuste käigus.

- Andmeallika kaupade sidumine andmemudeli komponentidega.
- Andmeallika kaupade sidumine vormingu komponentidega.
- Andmeallikate osana esinevate arvutatud väljade täielik haldamine.
- Kasutaja sisendparameetrite nähtavustingimuste määratlemine.
- Vormingu teisenduste kujundamine.
- Vormingu komponentide lubamistingimuste määratlemine.
- Vormingu failikomponentide failinimede määratlemine.
- Protsessi juhtimise kinnituste tingimuste määratlemine.
- Protsessi juhtimise kinnituste teate tekstide määratlemine.

## <a name="Binding">Andmete sidumine</a>

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis teisendab andmeid, mis saadakse andmeallikatest, nii et käitamisel saab sisestada andmeid andmete tarbijas järgmiselt.

- Rakenduse andmeallikatest ja käitamisaja parameetritest ER-i andmemudelisse
- ER-i andmemudelist ER-i vormingusse;
- Rakenduse andmeallikatest ja käitamisaja parameetritest ER-i vormingusse

Järgmisel joonisel on seda tüüpi avaldise kujundus. Selles näites ümardab avaldis tabelis Intrastat välja **Intrastat.AmountMST** väärtuse kahe kümnendkohani ja annab siis ümardatud väärtuse.

[![Andmete sidumise avaldis](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Järgmine joonis näitab, kuidas seda tüüpi avaldist saab kasutada. Selles näites on koostatud avaldise tulem sisestatud andmemudeli **Maksu aruandluse mudel** komponendile **Transaction.InvoicedAmount**.

[![Kasutatav andmete sidumise avaldis](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Käitusajal ümardab koostatud valem `ROUND (Intrastat.AmountMST, 2)` välja **AmountMST** väärtuse tabeli Intrastat iga kirje puhul kahe kümnendkohani. Seejärel sisestab see ümardatud väärtuse andmemudeli **Maksu aruandlus** komponenti **Transaction.InvoicedAmount**.

## <a name="Transformation">Andmete vormindamine</a>

ER-i valemikoostajat saab kasutada määratlemaks avaldist, mis vormindab andmeid, mis saadakse andmeallikatest, nii et andmeid saab saata elektroonilise dokumendi loomise osana. Teil võib olla vorming, mida tuleb rakendada tüüpilise reeglina, mida tuleb vormingu puhul taaskasutada. Sel juhul saate seda vormingut kasutada ühe korra vormingu konfiguratsioonis nimega teisendusena, millel on vormindamisavaldis. Selle nimelise teisenduse saab siduda paljude vormingu komponentidega, mille väljund peab olema vormindatud loodud vormindamisavaldise järgi.

Järgmisel joonisel on seda tüüpi teisenduse kujundus. Selles näites kärbib teisendus **TrimmedString** andmetüübi *String* sissetulevad andmed, eemaldades algus- ja lõputühikud. Seejärel tagastab see kärbitud stringiväärtuse.

[![Teisendus](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Järgmine joonis näitab, kuidas seda tüüpi teisendust saab kasutada. Selles näites saadavad mitu vormingu komponenti teksti käitusajal väljundina loodavale elektroonilisele dokumendile. Kõik need vormingukomponendid viitavad teisendusele **TrimmedString** nime järgi.

[![Kasutatav teisendamine](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kui vormingu komponendid (näiteks komponendi **partyName** puhul eelmises näites) viitavad teisendusele **TrimmedString**, saadab teisendus teksti väljundina loodavasse elektroonilisse dokumenti. See tekst ei sisalda algus- ega lõputühikuid.

Kui teil on vorming, mida tuleb rakendada eraldi, saab selle kasutusele võtta kindla vormingu komponendi sidumise üksiku avaldisena. Järgmisel joonisel on seda tüüpi avaldis. Selles näites on vormingu komponent **partyType** seotud andmeallikaga avaldise kaudu, mis teisendab sissetulevad andmeallika andmed väljalt **Model.Company.RegistrationType** suurtäheliseks tekstiks. Seejärel saadab avaldis selle teksti väljundina elektroonilisse dokumenti.

[![Vorminduse rakendamine üksikule komponendile](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="Validation">Protsessi voo juhtimine</a>

ER-i valemikoostajat saab kasutada elektrooniliste dokumentide loomise protsessivoo juhtimiseks kasutatavate avaldiste määratlemiseks. Saate teha järgmisi toiminguid.

- Määratlege tingimused, mis määravad, millal tuleb dokumendi loomise protsess peatada.
- Määrake avaldised, mis loovad kasutajale sõnumeid peatatud protsesside kohta või heidavad käivitamislogi sõnumeid aruande loomise protsessi jätkamise kohta.
- Määrake loodavate elektrooniliste dokumentide failinimed ja juhtige nende loomise tingimusi.

Iga protsessi voo juhtimise reegel on koostatud üksiku kinnitusena. Järgmisel joonisel on seda tüüpi kinnitus. Siin on selles näites oleva konfiguratsiooni selgitus.

- Kinnitamist hinnatakse, kui XML-faili loomisel luuakse **INSTAT**-sõlm.
- Kui kannete loend on tühi, lõpetab kinnitamine käivitamisprotsessi ja tagastab väärtuse **FALSE**.
- Kinnitamine annab tõrketeate, mis sisaldab SYS70894 teksti kasutaja eelistatud keeles.

[![Kinnitamine](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER-i valemikoostajat saab kasutada ka faili nime loomiseks loodavale elektroonilisele dokumendile ja faili loomise protsessi juhtimiseks. Järgmisel joonisel on seda tüüpi protsessi voo juhtimise kujundus. Siin on selles näites oleva konfiguratsiooni selgitus.

- Andmeallika **model.Intrastat** kirjete loend on jagatud partiideks. Iga partii sisaldab 1000 kirjet.
- Väljund loob zip-faili, mis sisaldab ühte XML-vormingus faili iga loodud partii kohta.
- Avaldis annab vastuseks failinime loodavatele elektroonilistele dokumentidele, liites faili nime ja failinime laiendi. Teise partii ja kõikide järgnevate partiide puhul sisaldab faili nimi järelliitena partii ID-d.
- Avaldis lubab (andes vatuseks väärtuse **TRUE**) faili loomise protsessi partiidele, mis sisaldavad vähemalt ühte kirjet.

[![Protsessi voo juhtimine](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="Enabled">Dokumendi sisu juhtelement</a>

ER-valemi koostajaga saab seadistada väljendeid, millega valitakse, mis andmeid pannakse käitusajal loodud elektroonilistesse dokumentidesse. Väljendid võivad lubada või keelata vormingu teatud elementide väljundit vastavalt töödeldavatele andmetele ja seadistatud loogikale. Neid väljendeid saab sisestada ühes vormingus elemendi jaoks lehe **Tegevuste kujundaja** vahekaardi **Vastendamine** väljal **Lubatud**. Saate sisestada avaldisi loogika tingimusena, mis tagastab väärtuse *Kahendmuutuja*.

- Kui tingimus annab tulemuse **True**, käitatakse praegust vormingu elementi.
- Kui tingimus annab tulemuse **False**, jäetakse praegune vormingu element vahele.

Järgmisel joonisel on näidatud seda tüüpi avaldised. (Näitena on kasutatud Microsofti pakutavat **ISO20022 krediidiedastuse (NO)** versiooni 11.12.11 vormingu seadistust). **XMLHeader** vormingu komponent on konfigureeritud kirjeldama krediidi edastamise sõnumi ülesehitust vastavalt ISO 20022 XML sõnumi standarditele. Vormingu komponent **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** on konfigureeritud lisama XML elemendi **Ustrd** loodud sõnumile ja panema rahaülekande teabe struktureerimata vormingus järgmiste XML elementide tekstina.

- Komponenti **PaymentNotes** kasutatakse maksemärkmete teksti loomiseks.
- Komponent **DelimitedSequence** loob komaga eraldatud arve numbreid, mida kasutatakse praeguse krediidiedastuse tasakaalustamiseks.

[![Komponendid PaymentNotes ja DelimitedSequence](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Komponendid **PaymentNotes** ja **DelimitedSequence** sildistatakse küsimärki kasutades. Küsimärk näitab, et komponendi kasutamine on tingimuslik. Sellisel juhul põhineb komponentide kasutamine järgmistel kriteeriumitel.
>
> - Väljend `@.PaymentsNotes <> ""`, mis on määratletud komponendi **PaymentNotes** võimaldab (annab tulemuse **TRUE**) XML elemendi **Ustrd** täitmist maksemärkmete tekstiga, kui see tekst pole praeguse krediidiedastuse jaoks tühi.
>
>    [![Komponendi PaymentNotes avaldis](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Avaldis `@.PaymentsNotes = ""`, mis määratletakse komponendi **DelimitedSequence** jaoks, võimaldab (annab tulemuse **TRUE**) XML elemendi **Ustrd** täitmist komaga eraldatud arve numbrite loendiga, mida kasutatakse praeguse krediidiedastuse arveldamiseks, kui selle krediidiedastuse maksemärkmete tekst on tühi.
>
>    [![Komponendi DelimitedSequence avaldis](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Vastavalt sellele seadistusele sisaldab iga deeboitori makse (XML-elemendi **Ustrd**) jaoks loodud sõnum kas maksemärkmete teksti või sellise teksti puudumisel komaga eraldatud arve numbreid, mida kasutatakse makse arveldamiseks.

## <a name="TestFormula">Konfigureeritud valemite valideerimine</a>

Lehel **Valemi kujundaja** valige suvand **Katse**, et valideerida konfigureeritud valemi töötamisviis.

[![Valemi valideerimiseks suvandi Katse valimine](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Kui nõutavad on valemi argumentide väärtused, saate avada dialoogiboksi **Testavaldis** lehelt **Valemikoostaja**. Enamikul juhtudel tuleb need argumendid käsitsi määratleda, kuna konfigureeritud sidumisi kujundamise ajal ei käitata. Vahekaart **Katsetulemus** lehel **Valemi kujundaja** näitab konfigureeritud valemi käivitamise tulemust.

Järgmine näide näitab, kuidas saate testida väliskaubanduse domeeni jaoks konfigureeritud valemit veendumaks, et Intrastati kaubakood sisaldaks ainult numbreid.

Selle valemi testimisel saate kasutada dialoogiboksi **Testavaldis**, et määrata testimiseks Intrastati kaubakoodi väärtus.

[![Testimiseks Intrastati kaubakoodi määramine](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Pärast seda, kui määrate Intrastati kaubakoodi ja valite **OK**, kuvatakse vahekaardil **Katsetulemus** lehel **Valemi koostaja** konfigureeritud valemi käivitamise tulemus. Seejärel saate hinnata, kas tulemus on vastuvõetav. Kui tulemus ei ole vastuvõetav, saate valemit värskendada ja seda uuesti katsetada.

[![Katsetulemus](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Osasid valemeid ei saa kujundamise ajal testida. Näiteks võib valem tagastada andmetüübi tulemuse, mida ei saa vahekaardil **Katsetulemus** kuvada. Sellisel juhul kuvatakse tõrketeade, mis teatab, et valemit ei saa katsetada.

[![Tõrketeade](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse valemi keel](er-formula-language.md)
