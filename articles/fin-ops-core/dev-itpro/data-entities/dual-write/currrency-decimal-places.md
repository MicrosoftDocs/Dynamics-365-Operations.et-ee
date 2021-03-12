---
title: Valuuta andmetüübi migreerimine topeltkirjutamise jaoks
description: Selles teemas kirjeldatakse, kuidas muuta kümnendkohtade arvu, mida topeltkirjutamine valuuta puhul toetab.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 5d39bf28dba951a1483412d967c8c6fc6dbcc610
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744371"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Valuuta andmetüübi migreerimine topeltkirjutamise jaoks

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Saate suurendada valuutaväärtuste puhul toetatavate kümnendkohtade arvu kuni kümneni. Vaikepiirang on neli kümnendkohta. Kümnendkohtade arvu suurendades aitate vältida andmekadu siis, kui kasutate andmete sünkroonimiseks topeltkirjutamist. Kümnendkohtade arvu suurendamine on valikuline muudatus. Selle rakendamiseks peate paluma Microsoftilt abi.

Kümnendkohtade arvu muutmise protsessil on kaks sammu.

1. Taotlege Microsoftilt migreerimist.
2. Muutke kümnendkohtade arv teenuses Dataverse.

Rakendus Finance and Operations ja teenus Dataverse peavad toetama valuutaväärtuste puhul sama kümnendkohtade arvu. Vastasel juhul võib esineda andmekadu, kui seda teavet sünkroonitakse rakenduste vahel. Migreerimisprotsess muudab viisi, kuidas valuuta- ja vahetuskursiväärtuseid talletatakse, kuid mitte andmeid. Pärast migreerimise lõpule viimist saab valuutakoodide ja hinnakujunduse kümnendkohtade arvu suurendada ning andmed, mida kasutajad sisestavad ja vaatavad, võivad hõlmata täpsemaid kümnendkohti.

Migreerimine on valikuline. Kui rohkemate kümnendkohtade tugi võib teile kasuks tulla, soovitame teil migreerimist kaaluda. Organisatsioonid, millel pole vaja rohkem kui nelja kümnendkohaga väärtuseid, ei pea migreerima.

## <a name="requesting-migration-from-microsoft"></a>Microsoftilt migreerimise taotlemine

Olemasolevate valuutaveergude talletamise puhul teenuses Dataverse ei toetata rohkem kui nelja kümnendkohta. Seetõttu kopeeritakse valuutaväärtused migreerimise käigus andmebaasi uutele sisemistele veergudele. See protsess jätkub, kuni kõik andmed on migreeritud. Migreerimise lõpus asendatakse vanad talletustüübid sisemiselt uute talletustüüpidega, kuid andmeväärtused ei muutu. Valuutaveerud toetavad seejärel kuni kümmet kümnendkohta. Migreerimise käigus saab jätkata teenuse Dataverse kasutamist häirimatult.

Samal ajal muudetakse vahetuskursse nii, et need toetaks kuni 12 kümnendkohta praeguse kümnese piirangu asemel. See muudatus on vajalik selleks, et kümnendkohtade arv oleks sama nii rakenduses Finance and Operations kui ka teenuses Dataverse.

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

![Valuuta süsteemisätted](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Ärihaldus: valuutad

Kui teil on vaja, et konkreetse valuuta täpsus erineks hinnakujunduses kasutatavast valuuta täpsusest, saate seda muuta. Avage **Sätted \> Ärihaldus**, valige **Valuutad** ja seejärel valuuta, mida soovite muuta. Seejärel seadke veeru **Valuuta täpsus** väärtuseks soovitud kümnendkohtade arv, nagu on näidatud järgmisel illustratsioonil.

![Konkreetse lokaadi valuutasätted](media/specific-currency.png)

### <a name="tables-currency-column"></a>tabelid: valuutaveerg

Kindlate valuutaveergude jaoks konfigureeritav maksimaalne kümnendkohtade arv on neli.
