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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456810"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Valuuta andmetüübi migreerimine topeltkirjutamise jaoks

[!include [banner](../../includes/banner.md)]

Saate suurendada valuutaväärtuste puhul toetatavate kümnendkohtade arvu kuni kümneni. Vaikepiirang on neli kümnendkohta. Kümnendkohtade arvu suurendades aitate vältida andmekadu siis, kui kasutate andmete sünkroonimiseks topeltkirjutamist. Kümnendkohtade arvu suurendamine on valikuline muudatus. Selle rakendamiseks peate paluma Microsoftilt abi.

Kümnendkohtade arvu muutmise protsessil on kaks sammu.

1. Taotlege Microsoftilt migreerimist.
2. Muutke kümnendkohtade arv teenuses Common Data Service.

Rakendus Finance and Operations ja teenus Common Data Service peavad toetama valuutaväärtuste puhul sama kümnendkohtade arvu. Vastasel juhul võib esineda andmekadu, kui seda teavet sünkroonitakse rakenduste vahel. Migreerimisprotsess muudab viisi, kuidas valuuta- ja vahetuskursiväärtuseid talletatakse, kuid mitte andmeid. Pärast migreerimise lõpule viimist saab valuutakoodide ja hinnakujunduse kümnendkohtade arvu suurendada ning andmed, mida kasutajad sisestavad ja vaatavad, võivad hõlmata täpsemaid kümnendkohti.

Migreerimine on valikuline. Kui rohkemate kümnendkohtade tugi võib teile kasuks tulla, soovitame teil migreerimist kaaluda. Organisatsioonid, millel pole vaja rohkem kui nelja kümnendkohaga väärtuseid, ei pea migreerima.

## <a name="requesting-migration-from-microsoft"></a>Microsoftilt migreerimise taotlemine

Olemasolevate valuutaväljade talletamise puhul teenuses Common Data Service ei toetata rohkem kui nelja kümnendkohta. Seetõttu kopeeritakse valuutaväärtused migreerimise käigus andmebaasi uutele sisemistele väljadele. See protsess jätkub, kuni kõik andmed on migreeritud. Migreerimise lõpus asendatakse vanad talletustüübid sisemiselt uute talletustüüpidega, kuid andmeväärtused ei muutu. Valuutaväljad toetavad seejärel kuni kümmet kümnendkohta. Migreerimise käigus saab jätkata teenuse Common Data Service kasutamist häirimatult.

Samal ajal muudetakse vahetuskursse nii, et need toetaks kuni 12 kümnendkohta praeguse kümnese piirangu asemel. See muudatus on vajalik selleks, et kümnendkohtade arv oleks sama nii rakenduses Finance and Operations kui ka teenuses Common Data Service.

Migreerimine ei muuda andmeid. Pärast valuuta- ja vahetuskursiväljade teisendamist saavad administraatorid seadistada süsteemi kasutama valuutaväljade puhul kuni kümmet kümnendkohta, määrates kümnendkohtade arvu iga kande valuuta ning hinnakujunduse jaoks.

### <a name="request-a-migration"></a>Migreerimise taotlemine

Selle funktsiooni kättesaadavaks tegemiseks saatke e-kiri aadressile **CDSExpandDecimal@microsoft.com** ja lisage sellele järgmine teave.

+ **Teema:** taotlus laiendatud kümnendkohtade toe lubamiseks organisatsiooni \<organizationID\> puhul
+ **Sisu:** soovin, et minu organisatsiooni \<organizationID\> puhul lubataks laiendatud kümnendkohtade tugi.

Microsofti esindaja võtab teiega järgmisteks sammudeks ühendust kahe kuni kolme tööpäeva jooksul.

Kui taotlete migreerimist, peaksite teadma järgmiseid üksikasju ja neid arvesse võtma.

+ Andmete migreerimiseks kuluv aeg sõltub süsteemis olevate andmete hulgast. Suurte andmebaaside migreerimine võib kesta mitu päeva.
+ Andmebaasi maht suureneb migreerimise ajal ajutiselt, kuna indeksite jaoks on vaja täiendavat ruumi. Pärast migreerimise lõpule viimist vabaneb suurem osa täiendavast ruumist.
+ Kui migreerimise käigus ilmnevad tõrked, mis takistavad migreerimise lõpule viimist, saadab süsteem Microsofti tugiteenusele teate, et tugiteenuse töötajad saaksid sekkuda. Isegi kui migreerimise ajal ilmnevad tõrked, on teenus Common Data Service täielikult tavapäraseks kasutamiseks saadaval.
+ Migreerimisprotsess on pöördumatu.

## <a name="changing-the-number-of-decimal-places"></a>Kümnendkohtade arvu muutmine

Kui migreerimine on lõpule viidud, saab teenus Common Data Service talletada numbreid, millel on rohkem kümnendkohti. Administraatorid saavad valida mitut kümnendkohta kasutatakse kindlate valuutakoodide ja hinnakujunduse puhul. Microsoft Power Appsi, Power BI ja Power Automate'i kasutajad saavad seejärel vaadata ja kasutada numbreid, millel on rohkem kümnendkohti.

Selle muudatuse tegemiseks peate värskendama Power Appsis järgmised sätted.

+ **Süsteemisätted: valuuta täpsus hinnakujunduse puhul** – väli **Määra valuuta täpsus, mida kasutatakse hinnakujunduse jaoks terves süsteemis** määratleb, kuidas valuuta organisatsiooni puhul käitub, kui valitud on **Hinnakujunduse täpsus**.
+ **Ärihaldus: valuutad** – väli **Valuuta täpsus** võimaldab teil määrata kindla valuuta jaoks kohandatud kümnendkohtade arvu. Tervet organisatsiooni hõlmav säte pole ideaalne.

Sellel on mõned piirangud.

+ Te ei saa üksuses valuutavälja konfigureerida.
+ Saate määrata rohkem kui neli kümnendkohta ainult **Hinnakujunduse** ja **Kande valuuta** tasemetes.

### <a name="system-settings-currency-precision-for-pricing"></a>Süsteemisätted: valuuta täpsus hinnakujunduse puhul

Pärast migreerimise lõpule viimist saavad administraatorid määrata valuuta täpsuse. Avage **Sätted \> Haldus** ja valige **Süsteemisätted**. Seejärel muutke vahekaardil **Üldine** välja **Määra valuuta täpsus, mida kasutatakse hinnakujunduse jaoks terves süsteemis** väärtust, nagu on näidatud järgmisel illustratsioonil.

![Valuuta süsteemisätted](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Ärihaldus: valuutad

Kui teil on vaja, et konkreetse valuuta täpsus erineks hinnakujunduses kasutatavast valuuta täpsusest, saate seda muuta. Avage **Sätted \> Ärihaldus**, valige **Valuutad** ja seejärel valuuta, mida soovite muuta. Seejärel seadke välja **Valuuta täpsus** väärtuseks soovitud kümnendkohtade arv, nagu on näidatud järgmisel illustratsioonil.

![Konkreetse lokaadi valuutasätted](media/specific-currency.png)

### <a name="entities-currency-field"></a>Üksused: valuutaväli

Kindlate valuutaväljade jaoks konfigureeritav maksimaalne kümnendkohtade arv on neli.