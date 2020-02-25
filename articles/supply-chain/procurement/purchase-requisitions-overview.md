---
title: Ostutaotluse ülevaade
description: Teema kirjeldab ostutaotluste töövoogu ja erinevaid olekuid, mis ostutaotlusel olla võivad.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a51d443e40dbf948a06657293dcca77dc177896
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003649"
---
# <a name="purchase-requisition-overview"></a>Ostutaotluse ülevaade

[!include [banner](../includes/banner.md)]

Teema kirjeldab ostutaotluste töövoogu ja erinevaid olekuid, mis ostutaotlusel olla võivad.

Olenevalt organisatsiooni seadistusest, saate luua organisatsiooni kasutatavatele toodetele ostutaotlusi. Ostutaotlus on sisedokument, mis annab ostuosakonnale volituse kaupu või teenuseid osta.  

Pärast ostutaotluse kinnitamist saab seda kasutada ostutellimuse loomiseks. Ostutellimused on välised dokumendid, mille ostuosakond hankijatele edastab.

## <a name="creating-purchase-requisitions"></a>Ostutaotluste loomine
Ostutaotluse saate luua leheküljel **Minu ostutaotlused** ja valida kaubad ja teenused, mida vajate. Saate valida kaupu organisatsiooni loodud hankekataloogist või taotleda kataloogist puuduvaid tooteid, valides hankekategooria ja sisestades toote üksikasjad.  

Enne ostutaotluse ülevaatuseks edastamist tuleb töövood konfigureerida. Töövoogu kasutades saate ostutaotlust ülevaatuse protsessis algsest olekust **Mustand** lõplikku olekusse **Kinnitatud** liigutada.

### <a name="purchase-requisition-statuses"></a>Ostutellimuse olekud

Ostutaotluse loomisel määratakse taotlusele olek. Olek määratakse ka igale ostutaotlusele lisatud reale. Ostutaotluse töövoogu ülevaatuseks esitamisel värskendatakse töövooprotsessis liikudes ostutaotluse ja iga rea olekut.  

Ostutaotluse töövooprotsessi saate konfigureerida selliselt, et ostutaotlus liiguks ülevaatuse protsessis ühe dokumendina. Teise võimalusena saab ostutaotluse ridu eraldi sobivatele läbivaatajatele suunata. Kui ostutaotluse ridu vaadatakse üle eraldi, saab iga ostutaotluse rea olekut vastavalt ülevaatuse protsessis liikumisele värskendada. Kui kõikide ridade ülevaatuse protsess on lõppenud ja ostutaotlusse ei jää ühtki ülevaatusetappi, siis värskendatakse kogu ostutaotluse olekut.

### <a name="purchase-requisition-workflow"></a>Ostutaotluse töövoog

Järgmine diagramm näitab ostutaotlusele ja ostutaotluse reale määratud olekut töövooprotsessis liikumisel.  

[![Ostutaotluse päise ja rea olekud](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Ostutaotluse päise ja rea olekute seosed

Ostutaotluse üldise oleku määrab ostutaotluse ridade olek. Seepärast tuleb kõigi ostutaotluse ridade ülevaatuse protsess lõpetada enne, kui kogu ostutaotluse ülevaatuse protsessi saab lõpetada. Järgmine tabel kirjeldab ostutaotluse päisele ja ridadele määratud olekut töövooprotsessis liikumisel.

<table>
<thead>
<tr class="header">
<th>Ostutaotluse olek</th>
<th>Ostutaotluse rea olek</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mustand</td>
<td>Mustand</td>
<td>Ostutaotlus ja ostutaotluse rida on loodud, kuid need pole ülevaatuseks esitatud. Tagasilükatud ostutaotlusi ja ostutaotluse ridu, mille olek on <strong>Mustand</strong>, saab muuta. Ostutellimuse või ostutellimuse rea olek on <strong>Mustand</strong> ka siis, kui see on tagasi kutsutud, kuid pole veel ülevaatamiseks uuesti esitatud. <strong>Märkus.</strong> Saate ostutellimuse esitada või tagasi kutsuda dokumendi tasemel. Esitada või tühistada ei ole võimalik üksikut ostutaotluse rida.</td>
</tr>
<tr class="even">
<td>Ülevaatamisel</td>
<td><ul>
<li>Ülevaatamisel</li>
<li>Tagasi lükatud</li>
</ul></td>
<td>Kui töövoog on konfigureeritud ostutaotluse ridu eraldi ülevaatajatele saatma, võib igal real olla olek <strong>Ülevaatusel</strong> või <strong>Tagasilükatud</strong>. Ostutaotluse olekut värskendatakse, kui kõigi ostutellimuse ridade ülevaatuse protsess on lõpetatud ja ostutaotlusse ei jää ühtki ülevaatusetappi.
<ul>
<li><strong>Ülevaatusel</strong> – ostutaotluse read on esitatud ülevaatuseks. Kuni kõik ostutaotluse read ei ole üle vaadatud, jääb rea, mille töövooprotsess on lõpule viidud, olekuks endiselt <strong>Ülevaatusel</strong>.</li>
<li><strong>Tagasi lükatud</strong> – ostutaotluse rida on tagasi lükatud. Tagasilükatud ostutaotluse ridu saab muuta ja uuesti esitada.</li>
</ul>
Tagasilükatud ostutaotluse rea uuesti esitamisel algab kõigi ülevaatusel olevate ostutaotluse ridade ülevaatuse protsess algusest. </br><strong>Märkus.</strong> Tühistada on võimalik ka juba esitatud ostutaotlust. Ostutaotluse tühistamisel tühistatakse ka kõik teised ostutaotluse read. Tühistatud ostutaotluse ridu saab kustutada.</td>
</tr>
<tr class="odd">
<td>Tagasi lükatud</td>
<td>Tagasi lükatud</td>
<td>Ostutaotlus ja kõik ostutaotluse read on tagasi lükatud. Tagasilükatud ostutaotlusi ja ostutaotluse ridu saab uuesti esitada.</td>
</tr>
<tr class="even">
<td>Kinnitatud</td>
<td><ul>
<li>Kinnitatud</li>
<li>Tühistatud</li>
<li>Suletud</li>
</ul></td>
<td>Kõigi ostutaotluse ridade ülevaatuse protsess on lõpetatud ja ostutaotlusel ei ole enam ühtki ülevaatusetappi.
<ul>
<li><strong>Kinnitatud</strong> – ostutaotluse rea ülevaatuse protsess on lõpetatud ja rida on kinnitatud.</li>
<li><strong>Tühistatud</strong> – ostutaotluse rida kinnitati, kuid see on tühistatud, kuna see ei ole enam vajalik. Tühistada saab ainult kinnitatud ostutaotluse ridu.</li>
<li><strong>Suletud</strong> – ostutaotluse rida on kinnitatud ja taotluse eesmärgist lähtuvalt on loodud dokumendid.
<ul>
<li>Kui taotluse eesmärk on tarbimine, on ostutaotluse reale ostutellimus loodud.</li>
<li>Kui taotluse eesmärk on täiendamine, on loodud üks või mitu täitmisdokumenti.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Tühistatud</td>
<td>Tühistatud</td>
<td>Ostutaotlus ja kõik ostutaotluse read on tühistatud.</br> <strong>Märkus.</strong> Kui te ei vaja enam ostutaotluse real olnud kaupa, kuid ostutaotluse rida on juba kinnitatud, peate selle ostutaotluse rea tühistama. Tühistada saab ainult kinnitatud ostutaotluse ridu. Kui mõni ostutaotluse rida on ülevaatusel, on ostutaotluse olek <strong>Ülevaatusel</strong>. Sellisel juhul saate ostutaotluse tühistada ja vastava ostutaotluse rea kustutada.</td>
</tr>
<tr class="even">
<td>Suletud</td>
<td><ul>
<li>Suletud</li>
<li>Tühistatud</li>
</ul></td>
<td>Ostutaotlus on suletud ning üks või mitu täitmisdokumenti on loodud.
<ul>
<li><strong>Suletud</strong> – ostutaotluse rida on kinnitatud ja taotluse eesmärgist lähtuvalt on loodud dokumendid.
<ul>
<li>Kui taotluse eesmärk on tarbimine, on ostutaotluse reale ostutellimus loodud.</li>
<li>Kui taotluse eesmärk on täiendamine, on loodud üks või mitu täitmisdokumenti.</li>
</ul></li>
<li><strong>Tühistatud</strong> – ostutaotluse rida kinnitati, kuid see on tühistatud, kuna see ei ole enam vajalik. Tühistada saab ainult kinnitatud ostutaotluse ridu.</li>
</ul>
<strong>Märkus.</strong> Kui te ei vaja enam suletud ostutaotluse real olnud kaupa, peate tühistama rea ostutaotluse reale loodud täitmisdokumendil.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Kulude jaotamine mitme finantskonto vahel
Saate jaotada ostutaotlusesse lisatud toote kulu mitme finantskonto vahel. Kui teie organisatsioon kasutab dimensioone (nt kulukeskused ja osakonnad), saate jaotada toote kulu finantskontode dimensioonideks.

## <a name="requisition-purposes"></a>Taotluse eesmärgid
Taotluse eesmärgid teevad taotluses nõutu täitmisprotsessi paindlikumaks. Taotluse loomisel saate sellele määrata ühe kahest eesmärgist: tarbimine või täiendamine. Olenevalt taotluse eesmärgist ja organisatsiooni seadistusest luuakse taotluse nõudluse täitmiseks kas ostutellimus, üleviimistellimus, tootmistellimuse või kanban.  

Organisatsiooni jaoks loodava taotluse jaoks saadaolevaid eesmärke saate juhtida hankepoliitikates.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Taotlused, mille eesmärk on tarbimine

Tarbimise eesmärgil loodav taotlus tähistab nõudlust kaupade või teenuste järele, mida kasutatakse organisatsioonisiseselt. Seda tüüpi taotluse loodud nõudluse täidab alati ostutellimus. Kui Supply Chain Management on seadistatud automaatselt ostutellimusi looma, luuakse ostutellimused pärast ostutaotluse kinnitamist.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Taotlused, mille eesmärk on täiendamine

Täiendamise eesmärgil loodud taotlus esindab nõuet varude täiendamiseks. Näiteks võite luua taotluse kaupade täiendamiseks nii, et neid saaks müüa konkreetses jaemüügiasukohas kindlal ajal. Seda sorti taotluses nõutut saab täita ostutellimuse, üleviimiskorralduse, tootmistellimuse või kanbaniga.  

Kui taotluse eesmärk on täiendamine, väljendatakse nõuet koguse, mitte rahasummana. Seega ei kehti pandiõiguse arvestuse, eelarvekontrolli, põhivara määramise ärireeglite (BRAD), projekti raamatupidamise ega mingid seotud reeglid. Täiendamise taotluse nõuet saavad täita ainult tooted, mis ladustatakse ja vabastatakse määratud juriidilisele isikule. Täiendamise eesmärgil saadaolevate toodete määratlemiseks kasutage lehekülge **Täiendamise kategooria juurdepääsupoliitika reegel**.  

Täiendamise eesmärgiga ostutaotluste kasutamiseks peate koondplaneerimise seadistama selliselt, et kaasataks taotluses nõutu. Nõutule määratletakse automaatselt täitmise meetod vastavalt teie organisatsioonis kehtestatud tarnepoliitikale ja planeeritakse kasutades koondplaneerimist.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Ostutaotlused ja pakkumiskutsed
Mõnel juhul tuleb ostutaotluses nõutud toodete hankija ja hinna tuvastamiseks käivitada pakkumiskutse protsess. Pakkumiskutse saab luua, kui ostutaotlus on ülevaatusel. Kui võtate pakkumise vastu, kantakse taotlusele üle teave hankija, hinna jms kohta.  

Ostutaotluse saate ootele panna, valides leheküljel **Ostutaotluse üksikasjad** ruudu **Ootel**. Ostutaotluse töötlemist jätkatakse ainult siis, kui tühjendate ruudu märgistuse.  

> [!NOTE]
> E-hankes ostutaotlusele loodud pakkumiskutse võib lubada hankijatel alternatiivseid ridu lisada. Sellisel juhul kajastab ostutaotlus kinnitatud alternatiive.

## <a name="demand-consolidation"></a>Nõudluse konsolideerimine
Mitme ostutaotluse rea konsolideerimisega saate parandada oma positsiooni hankijatega läbirääkimiste pidamisel, et saada soodsamaid hindu, vähendada tarne- ja käsitlemiskulusid ning ka üldkulusid.  

Ostutaotluse read on nõudluse konsolideerimise jaoks sobilikud vaid juhul, kui järgmised väited vastavad tõele.

-   Ostutaotlus on kinnitatud.
-   Ostutaotlus vastab ostupoliitika reegli käsitsi töötlemise ja nõudluse konsolideerimise kriteeriumitele.

Käsitsi töötlemise kriteeriumidele vastavad kinnitatud ostutaotluse read on loetletud leheküljel **Vabastatud kinnitatud ostutaotlused**. Kui ostutaotluse rida vastab ka nõude konsolideerimise kriteeriumitele, võib rea lisada konsolideerimisvõimalusse.  

Konsolideerimisvõimalus on grupeeritud ostutaotluse ridade kogum, mis võimaldab ostuspetsialistil saavutada hankijatega parima kokkuleppe. Konsolideerimisvõimalusse valitud ostutaotluse read kuvatakse leheküljel **Ostutaotluse konsolideerimine**. Vajadusel saate sellel lehel olevaid ridu muuta. Samuti saate konsolideerimisvõimalusele uusi ridu lisada või olemasolevaid eemaldada.  

Pärast konsolideerimisvõimalusse taotluse ridade lisamist ja vajalike muudatuste tegemist saate luua ostutellimuse konsolideeritud ostutaotluse ridade alusel.  

> [!NOTE]
> Ostutaotluse reale leheküljel **Ostutaotluse konsolideerimine** tehtud muudatused kajastuvad loodavas ostutellimuses. Ostutaotluses olev rida siiski ei muutu, et selle ajalugu säiliks.  

Ostutaotluse ridu, mis ei ole konsolideerimise jaoks sobilikud või mida ei valita konsolideerimisvõimaluse jaoks, tuleb ostutellimuse loomiseks käsitsi töödelda.

### <a name="consolidating-purchase-requisition-lines"></a>Ostutaotluse ridade konsolideerimine

Nõutud kaupade konsolideerimise protsess algab siis, kui ostutaotlus on töövoos kinnitatud ja eelarve reserveeringud ja eelpandiõigused on kirjendatud, juhul kui teie organisatsioonis on konfigureeritud eelarve juhtimine. Järgmine diagramm näitab nõutud kaupade konsolideerimise protsessi voogu.  

[![Nõutud kaupade konsolideerimise protsessivoog](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Kinnitatud ostutaotluse ridade konsolideerimiseks tehke järgmist.

1.  Vaadake üle kinnitatud taotluse read, mis on käsitsi töötlemise jaoks kinni peetud ja nõutud kaupade konsolideerimise jaoks sobilikud.
2.  Valige konsolideerimisvõimalusse lisatavad ostutaotluse read.
3.  Looge uus konsolideerimisvõimalus või lisage taotluse read olemasolevasse konsolideerimisvõimalusse.
4.  Tehke taotluse ridadel vajalikud muudatused ja eemaldage taotluse realt kaubad, mida te ei soovi enam konsolideerimisvõimalusse kaasata.
5.  Looge konsolideerimisvõimaluses konsolideeritud taotluse ridade või ostutaotluse ridade jaoks ostutellimused.


<a name="additional-resources"></a>Lisaressursid
--------

[Tarbimistaotluse loomine](tasks/create-requisition-consumption.md)

[Ostutaotluse töövoog](purchase-requisitions-workflow.md)



