---
title: Valuuta andmetüübi migreerimine topeltkirjutamise jaoks
description: Selles teemas kirjeldatakse, kuidas muuta kümnendkohtade arvu, mida topeltkirjutamine valuuta puhul toetab.
author: RamaKrishnamoorthy
ms.date: 12/08/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: e9dc3e6c5fbec9636370b64a9bbdcf8a5834d332
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061832"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Valuuta andmetüübi migreerimine topeltkirjutamise jaoks

[!include [banner](../../includes/banner.md)]



Saate suurendada valuutaväärtuste puhul toetatavate kümnendkohtade arvu kuni kümneni. Vaikepiirang on neli kümnendkohta. Kümnendkohtade arvu suurendades aitate vältida andmekadu siis, kui kasutate andmete sünkroonimiseks topeltkirjutamist. Kümnendkohtade arvu suurendamine on valikuline muudatus. Selle rakendamiseks peate paluma Microsoftilt abi.

Kümnendkohtade arvu muutmise protsessil on kaks sammu.

1. Taotlege Microsoftilt migreerimist.
2. Muutke kümnendkohtade arv teenuses Dataverse.

Rakendus Finance and Operations ja Dataverse peab toetama valuuta väärtustes sama arvu kümnendkohti. Vastasel juhul võib esineda andmekadu, kui seda teavet sünkroonitakse rakenduste vahel. Migreerimisprotsess muudab viisi, kuidas valuuta- ja vahetuskursiväärtuseid talletatakse, kuid mitte andmeid. Pärast migreerimise lõpule viimist saab valuutakoodide ja hinnakujunduse kümnendkohtade arvu suurendada ning andmed, mida kasutajad sisestavad ja vaatavad, võivad hõlmata täpsemaid kümnendkohti.

Migreerimine on valikuline. Kui rohkemate kümnendkohtade tugi võib teile kasuks tulla, soovitame teil migreerimist kaaluda. Organisatsioonid, millel pole vaja rohkem kui nelja kümnendkohaga väärtuseid, ei pea migreerima.

## <a name="requesting-migration-from-microsoft"></a>Microsoftilt migreerimise taotlemine

Olemasolevate valuutaveergude talletamise puhul teenuses Dataverse ei toetata rohkem kui nelja kümnendkohta. Seetõttu kopeeritakse valuutaväärtused migreerimise käigus andmebaasi uutele sisemistele veergudele. See protsess jätkub, kuni kõik andmed on migreeritud. Migreerimise lõpus asendatakse vanad talletustüübid sisemiselt uute talletustüüpidega, kuid andmeväärtused ei muutu. Valuutaveerud toetavad seejärel kuni kümmet kümnendkohta. Migreerimise käigus saab jätkata teenuse Dataverse kasutamist häirimatult.

Samal ajal muudetakse vahetuskursse nii, et need toetaks kuni 12 kümnendkohta praeguse kümnese piirangu asemel. See muudatus on vajalik, et kümnendkohtade arv oleks sama nii rakenduses Finance and Operations kui ka rakenduses Dataverse.

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

### <a name="tables-currency-column"></a>Tabelid: Valuuta veerg

Kindlate valuutaveergude jaoks konfigureeritav maksimaalne kümnendkohtade arv on neli.

### <a name="default-currency-decimal-precision"></a>Vaikevaluuta kümnendkoha täpsus
Vaikevaluuta kümnendkoha täpsuse eeldatava käitumise kohta ülemineku ja mittemigreerimise stsenaariumide puhul vaadake järgmist tabelit. 

| Loomiskuupäev  | Valuuta kümnendväli    | Olemasolev organisatsioon (valuuta väli pole üle viidud) | Olemasolev organisatsioon (valuuta väli migreeritud) | Uus organisatsioon lõi postituse ehituse 9.2.21062.00134 |
|---------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|------------------------------------------------|
| Valuuta väli loodud enne ehitamist 9.2.21111.00146  |     |  |       |
|    | Kasutajaliideses nähtav maksimaalne täpsus   | 4 numbrit    | 10 numbrit    | Pole    |
| | Maksimaalne täpsus on nähtav andmebaasi ja DB päringutulemuste kasutajaliideses         | 4 numbrit   | 10 numbrit   | Pole    |
| Valuuta väli loodud pärast ehitamist 9.2.21111.00146 |    |  |     |   |
|   | Kasutajaliideses nähtav maksimaalne kümnendkoha täpsus     | 4 numbrit   | 10 numbrit   | 10 numbrit     |
|          | Maksimaalne kümnendkoha täpsus on nähtav andmebaasi ja DB päringutulemuste kasutajaliideses | 10 numbrit. Kuid ainult 4 on olulised, kui kõik nullid ületavad nelja kümnendkoha numbrit. See võimaldab vajadusel organisatsiooni lihtsamat ja kiiremat migratsiooni. | 10 numbrit      | 10 numbrit     |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
