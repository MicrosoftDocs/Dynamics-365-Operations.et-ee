---
title: "Laotöölehed"
description: "Selles artiklis kirjeldatakse, kuidas kasutada laotöölehti eri tüüpi füüsiliste laokannete sisestamiseks."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 6dfb82acb5dafd365d878949b35d4fe6ff58793d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="inventory-journals"></a>Laotöölehed

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Selles artiklis kirjeldatakse, kuidas kasutada laotöölehti eri tüüpi füüsiliste laokannete sisestamiseks.

Laotöölehti kasutatakse rakenduses Microsoft Dynamics 365 for Finance and Operationsis mitmesuguste füüsiliste laokannete sisestamiseks, nt väljaminekute ja sissetulekuste, varude liikumiste, koosluste loomise ja füüsiliste varude vastavusseviimise sisestamiseks. Kõiki neid laotöölehti kasutatakse sarnasel viisil, kuid need on jagatud erinevateks tüüpideks.

## <a name="types-of-inventory-journals"></a>Laotöölehtede tüübid
Saadaval on järgmist tüüpi laotöölehti.

-   Liikumine
-   Lao korrigeerimine
-   Ülekanne
-   Kooslus
-   Kauba saabumine
-   Materjalid tootmisse
-   Inventuur
-   Märgistusega inventuur

### <a name="movement"></a>Liikumine

Varude liikumise töölehe kasutamisel saate lisada kaubale varude lisamisel maksumuse, kuid peate eraldama lisakulu käsitsi konkreetsele pearaamatukontole, määrates töölehe loomisel pearaamatu vastaskonto. Varude töölehe tüüp on abiks, kui soovite kanda kauba teise osakonna kuludesse või kui soovite eemaldada kaupu varudest kuludesse kandmiseks.

### <a name="inventory-adjustment"></a>Lao korrigeerimine

Varude korrigeerimistöölehe kasutamisel saate lisada kaubale kulu varude lisamisel. Lisakulud sisestatakse automaatselt konkreetsele pearaamatukontole kaubagrupi sisestusreeglite seadistuse alusel. Kasutage seda varude töölehe tüüpi laokoguste kasumite ja kahjumite uuendamiseks, kui kaup peaks säilitama oma pearaamatu vastaskonto vaikeväärtuse. Varude korrigeerimise töölehe sisestamisel sisestatakse lao sissetulek või väljaminek, muudetakse laoväärtusi ja luuakse pearaamatu kanded.

### <a name="transfer"></a>Ülekanne

Üleviimistöölehti saab kasutada kaupade üleviimiseks ladustamiskohtade, partiide või tootevariantide vahel ilma kulusid seostamata. Näiteks võite viia kaupu ühest laost teise sama ettevõtte raames. Üleviimistöölehe kasutamisel tuleb määrata varude dimensioonid „kust” ja „kuhu” (nt väärtuste Laoala ja Ladu puhul). Määratletud varude dimensioonide vaba kaubavaru muudetakse vastavalt. Varude üleviimised kajastavad materjali viivitamatut liikumist. Transiidis olevaid varusid ei jälgita. Kui transiidis olevaid varusid tuleb jälgida, tuleb selle asemel kasutada üleviimistellimust. Üleviimistöölehe sisestamisel luuakse iga töölehe rea jaoks kaks varude kannet.

-   Lao väljaminek asukohast „kust”
-   Lao sissetulek asukohas „kuhu”

### <a name="bom"></a>Kooslus

Kui kinnitate koosluse lõpetatuks, saate luua koosluse töölehe. Koosluse töölehe kasutamisel saate kooslust otse sisestada. Sisestamine loob tootele lao sissetuleku koos seotud koosluse ja koosluses sisalduvate toodete lao väljaminekuga. See varude töölehe tüüp on abiks lihtsate või mahukate tootmisstsenaariumide korral, kui protsesse ei vajata.

### <a name="item-arrival"></a>Kauba saabumine

Saate kasutada kauba saabumistöölehte kaupade sissetuleku registreerimiseks (nt ostutellimustelt). Kauba saabumistöölehe saab luua saabumise haldamise käigus lehelt **Saabumisülevaade** või töölehe sisestuse saab luua käsitsi lehelt **Kauba saabumine**. Kui lubate kauba saabumise töölehe nime puhul komplekteerimiskohtade otsimise, otsib Finance and Operations saadud kaupade asukohta ja kui ruumi on, loob sissetulevatele kaupadele sihtkohad.

### <a name="production-input"></a>Materjalid tootmisse

Tootmise sisendtöölehed toimivad kauba saabumistöölehtede sarnaselt, kuid neid kasutatakse tootmistellimuste puhul.

### <a name="counting"></a>Inventuur

Inventuuritöölehtede abil saate korrigeerida praegust vaba kaubavaru, mis on kaupade või kaubagruppide puhul registreeritud, ja seejärel sisestada tegeliku füüsilise inventuuri nii, et saate teha vajalikke korrigeerimisi erinevuste tasakaalustamiseks. Saate seostada inventuuripoliitikad inventuurigruppidega, et aidata rühmitada erinevate omadustega kaupu, nii et need kaubad saaks lisada inventuuri töölehele. Näiteks saate seadistada inventuurigrupid nii, et need loeksid kaupu, millel on konkreetne sagedus, või loeksid kaupu siis, kui varud langevad teatud tasemele. Teavet inventuurigruppide määratlemise kohta leiate jaotisest [Laoinventuuri protsesside määratlemine (tegevuse juhis)](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Märgistusega inventuur

Märgistusega inventuuritöölehti kasutatakse inventuuripartiile numbrisildi määramiseks. Sildil peaks olema sildi number, kaubakood ja kauba kogus. Et tagada sildi ühekordne kasutamine ja kõigi siltide kasutamine, peaks igal kaubakoodil olema oma numbriseeriaga kordumatu sildikomplekt. Igale sildile saab määrata olekuväärtused.

-   **Kasutatud** – selle sildi kaubakoodi loetakse.
-   **Tühistatud** – selle sildi kaubakood on tühistatud.
-   **Puudub** – selle sildi kaubakood puudub.

Märgistusega inventuuritöölehe sisestamisel luuakse märgistusega inventuuri tööleheridade põhjal uus inventuuritööleht. Märgistusega inventuuri kohta leiate lisateavet jaotisest [Märgistusega inventuur](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Töölehtedega töötamine
Töölehele pääseb korraga juurde ainult üks kasutaja. Kui mitu kasutajat peab töölehe ridade loomiseks samal ajal töölehtedele juurde pääsema, peavad kasutajad valima töölehed, mida hetkel ei kasutata, et vältida teabe ülekirjutamist. Olukordades, kus mitu osakonda kasutavad sama töölehe tüüpi, on kasulik luua mitu töölehe nime (nt üks osakonna kohta). Abiks võib olla ka töölehtede jagamine nii, et iga sisestusprotsess sisestatakse eraldi kordumatule laotöölehele. Laokannetega seostuvate sisestusprotsesside puhul saab luua ühe töölehe perioodiliste laokorrektsioonide tarvis ja teise töölehe inventuuri tegemiseks.

## <a name="posting-journal-lines"></a>Töölehe ridade sisestamine
Saate enda loodud tööleheread igal ajal sisestada, kuni olete lukustanud kauba täiendavate kannete eest. Töölehele sisestatud andmed jäävad sellele töölehele isegi juhul, kui sulgete töölehe ilma ridu sisestamata.

