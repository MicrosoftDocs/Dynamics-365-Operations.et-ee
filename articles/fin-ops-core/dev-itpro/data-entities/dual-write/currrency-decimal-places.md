---
title: Valuuta andmetüübi migreerimine topeltkirjutamise jaoks
description: See artikkel kirjeldab, kuidas muuta valuuta puhul topeltkirjutusega toega komakohtade arvu.
author: RamaKrishnamoorthy
ms.date: 12/08/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 327d6ced7fca4bdae1fd80928086dafed6b0f931
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289710"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Valuuta andmetüübi migreerimine topeltkirjutamise jaoks

[!include [banner](../../includes/banner.md)]



Saate suurendada valuutaväärtuste puhul toetatavate kümnendkohtade arvu kuni kümneni. Vaikepiirang on neli kümnendkohta. Kümnendkohtade arvu suurendades aitate vältida andmekadu siis, kui kasutate andmete sünkroonimiseks topeltkirjutamist. Kümnendkohtade arvu suurendamine on valikuline muudatus. Selle rakendamiseks peate paluma Microsoftilt abi.

Kümnendkohtade arvu muutmise protsessil on kaks sammu.

1. Taotlege Microsoftilt migreerimist.
2. Muutke kümnendkohtade arv teenuses Dataverse.

Finantside ja toimingute rakendus ning Dataverse need peavad toetama sama komakohtade arvu valuutaväärtustes. Vastasel juhul võib esineda andmekadu, kui seda teavet sünkroonitakse rakenduste vahel. Migreerimisprotsess muudab viisi, kuidas valuuta- ja vahetuskursiväärtuseid talletatakse, kuid mitte andmeid. Pärast migreerimise lõpule viimist saab valuutakoodide ja hinnakujunduse kümnendkohtade arvu suurendada ning andmed, mida kasutajad sisestavad ja vaatavad, võivad hõlmata täpsemaid kümnendkohti.

Migreerimine on valikuline. Kui rohkemate kümnendkohtade tugi võib teile kasuks tulla, soovitame teil migreerimist kaaluda. Organisatsioonid, millel pole vaja rohkem kui nelja kümnendkohaga väärtuseid, ei pea migreerima.

## <a name="requesting-migration-from-microsoft"></a>Microsoftilt migreerimise taotlemine

Olemasolevate valuutaveergude talletamise puhul teenuses Dataverse ei toetata rohkem kui nelja kümnendkohta. Seetõttu kopeeritakse valuutaväärtused migreerimise käigus andmebaasi uutele sisemistele veergudele. See protsess jätkub, kuni kõik andmed on migreeritud. Migreerimise lõpus asendatakse vanad talletustüübid sisemiselt uute talletustüüpidega, kuid andmeväärtused ei muutu. Valuutaveerud toetavad seejärel kuni kümmet kümnendkohta. Migreerimise käigus saab jätkata teenuse Dataverse kasutamist häirimatult.

Samal ajal muudetakse vahetuskursse nii, et need toetaks kuni 12 kümnendkohta praeguse kümnese piirangu asemel. See muudatus on vajalik, et komakohtade arv oleks nii finantside kui ka toimingute rakenduses ja komakohtade arvus sama Dataverse.

Migreerimine ei muuda andmeid. Pärast valuuta- ja vahetuskursivveergude teisendamist saavad administraatorid seadistada süsteemi kasutama valuutaveergude puhul kuni kümmet kümnendkohta, määrates kümnendkohtade arvu iga kande valuuta ning hinnakujunduse jaoks.

### <a name="request-a-migration"></a>Migreerimise taotlemine

Selle funktsiooni kättesaadavaks tegemiseks saatke e-kiri aadressile **CDSExpandDecimal@microsoft.com** ja lisage sellele järgmine teave.

+ **Teema:** taotlus laiendatud kümnendkohtade toe lubamiseks organisatsiooni \<organizationID\> puhul
+ **Sisu:** soovin, et minu organisatsiooni \<organizationID\> puhul lubataks laiendatud kümnendkohtade tugi.

Microsofti esindaja võtab teiega järgmisteks sammudeks ühendust kahe kuni kolme tööpäeva jooksul.

Kui taotlete migreerimist, peaksite teadma järgmiseid üksikasju ja neid arvesse võtma.

+ Andmete migreerimiseks kuluv aeg sõltub süsteemis olevate andmete hulgast. Suurte andmebaaside migreerimine võib kesta mitu päeva.
+ Andmebaasi maht suureneb migreerimise ajal ajutiselt, kuna indeksite jaoks on vaja täiendavat ruumi. Pärast migreerimise lõpule viimist vabaneb suurem osa täiendavast ruumist.
+ Kui migreerimise käigus ilmnevad tõrked, mis takistavad migreerimise lõpule viimist, saadab süsteem Microsofti tugiteenusele teate, et tugiteenuse töötajad saaksid sekkuda. Isegi kui migreerimise ajal ilmnevad tõrked, on teenus Dataverse täielikult tavapäraseks kasutamiseks saadaval.
+ Migreerimisprotsess on pöördumatu.

## <a name="changing-the-number-of-decimal-places"></a>Kümnendkohtade arvu muutmine

Kui migreerimine on lõpule viidud, saab teenus Dataverse talletada numbreid, millel on rohkem kümnendkohti. Administraatorid saavad valida mitut kümnendkohta kasutatakse kindlate valuutakoodide ja hinnakujunduse puhul. Microsoft Power Appsi, Power BI ja Power Automate'i kasutajad saavad seejärel vaadata ja kasutada numbreid, millel on rohkem kümnendkohti.

Selle muudatuse tegemiseks peate värskendama Power Appsis järgmised sätted.

+ **Süsteemisätted: valuuta täpsus hinnakujunduse puhul** – veerg **Määra valuuta täpsus, mida kasutatakse hinnakujunduse jaoks terves süsteemis** määratleb, kuidas valuuta organisatsiooni puhul käitub, kui valitud on **Hinnakujunduse täpsus**.
+ **Ärihaldus: valuutad** – veerg **Valuuta täpsus** võimaldab teil määrata kindla valuuta jaoks kohandatud kümnendkohtade arvu. Tervet organisatsiooni hõlmav säte pole ideaalne.

Sellel on mõned piirangud.

+ Te ei saa tabelis valuutaveergu konfigureerida.
+ Saate määrata rohkem kui neli kümnendkohta ainult **Hinnakujunduse** ja **Kande valuuta** tasemetes.

### <a name="system-settings-currency-precision-for-pricing"></a>Süsteemisätted: valuuta täpsus hinnakujunduse puhul

Pärast migreerimise lõpule viimist saavad administraatorid määrata valuuta täpsuse. Avage **Sätted \> Haldus** ja valige **Süsteemisätted**. Seejärel muutke vahekaardil **Üldine** veergu **Määra valuuta täpsus, mida kasutatakse hinnakujunduse jaoks terves süsteemis** väärtust, nagu on näidatud järgmisel illustratsioonil.

![Valuuta süsteemisätted.](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Ärihaldus: valuutad

Kui teil on vaja, et konkreetse valuuta täpsus erineks hinnakujunduses kasutatavast valuuta täpsusest, saate seda muuta. Avage **Sätted \> Ärihaldus**, valige **Valuutad** ja seejärel valuuta, mida soovite muuta. Seejärel seadke veeru **Valuuta täpsus** väärtuseks soovitud kümnendkohtade arv, nagu on näidatud järgmisel illustratsioonil.

![Konkreetse lokaadi valuutasätted.](media/specific-currency.png)

### <a name="tables-currency-column"></a>Tabelid: valuuta veerg

Kindlate valuutaveergude jaoks konfigureeritav maksimaalne kümnendkohtade arv on neli.

### <a name="default-currency-decimal-precision"></a>Vaikevaluuta kümnendarvuline täpsus
Migreerimise ja mittesiirde stsenaariumide vaikimisi valuuta kümnendarvu täpsuse eeldatava käitumise jaoks vaadake järgmist tabelit. 

| Loomise kuupäev  | Valuuta kümnendkoht    | Olemasolev org (valuutavälja ei migreerita) | Olemasolev org (ülekantud valuutaväli) | Uus org. loomise järgselt 9.2.21062.00134 |
|---------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|------------------------------------------------|
| Enne valuutarea loomist 9.2.21111.00146  |     |  |       |
|    | Maksimaalne täpsus, mis on nähtav kasutajaliideses.   | 4 numbrit    | 10 numbrit    | Pole    |
| | Maksimaalne täpsus, mis on nähtav andmebaasis ja andmebaasi päringutulemuste kasutajaliideses         | 4 numbrit   | 10 numbrit   | Pole    |
| Pärast valuutakursi loomist loodud 9.2.21111.00146 |    |  |     |   |
|   | Kasutajaliideses nähtav kümnendarvuline täpsus     | 4 numbrit   | 10 numbrit   | 10 numbrit     |
|          | Maksimaalne kümnendarvuline täpsus, mis on nähtav andmebaasi ja andmebaasi päringutulemuste kasutajaliideses | 10 numbrit. Kuid ainult 4 on oluline, kui kõik nullid on väljaspool nelja kümnendkohta. See võimaldab vajadusel organisatsiooni lihtsamat ja kiiremat siirdet. | 10 numbrit      | 10 numbrit     |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

