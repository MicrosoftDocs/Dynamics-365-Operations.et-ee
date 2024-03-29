---
title: Laotöölehed
description: Selles artiklis kirjeldatakse, kuidas kasutada laotöölehti eri tüüpi füüsiliste laokannete sisestamiseks.
author: yufeihuang
ms.date: 04/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 182c0ac9146c44b08698f8f9d15a3610bf0b7cea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849412"
---
# <a name="inventory-journals"></a>Laotöölehed

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas kasutada laotöölehti eri tüüpi füüsiliste laokannete sisestamiseks.

Laotöölehti kasutatakse Supply Chain Managementis mitmesuguste füüsiliste laokannete sisestamiseks, nt väljaminekute ja sissetulekuste, varude liikumiste, koosluste loomise ja füüsiliste varude vastavusseviimise sisestamiseks. Kõiki neid laotöölehti kasutatakse sarnasel viisil, kuid need on jagatud erinevateks tüüpideks.

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

Varude liikumise töölehe kasutamisel saate lisada kaubale varude lisamisel maksumuse, kuid peate eraldama lisakulu käsitsi konkreetsele pearaamatukontole, määrates töölehe loomisel pearaamatu vastaskonto. See varude töölehe tüüp on abiks, kui soovite vaikimisi sisestuskontod üle kirjutada.

### <a name="inventory-adjustment"></a>Lao korrigeerimine

Varude korrigeerimistöölehe kasutamisel saate lisada kaubale kulu varude lisamisel. Lisakulud sisestatakse automaatselt konkreetsele pearaamatukontole kaubagrupi sisestusreeglite seadistuse alusel. Kasutage seda varude töölehe tüüpi laokoguste kasumite ja kahjumite uuendamiseks, kui kaup peaks säilitama oma pearaamatu vastaskonto vaikeväärtuse. Varude korrigeerimise töölehe sisestamisel sisestatakse lao sissetulek või väljaminek, muudetakse laoväärtusi ja luuakse pearaamatu kanded.

### <a name="transfer"></a>Ülekanne

Üleviimistöölehti saab kasutada kaupade üleviimiseks ladustamiskohtade, partiide või tootevariantide vahel ilma kulusid seostamata. Näiteks võite viia kaupu ühest laost teise sama ettevõtte raames. Üleviimistöölehe kasutamisel tuleb määrata varude dimensioonid „kust” ja „kuhu” (nt väärtuste Laoala ja Ladu puhul). Määratletud varude dimensioonide vaba kaubavaru muudetakse vastavalt. Varude üleviimised kajastavad materjali viivitamatut liikumist. Transiidis olevaid varusid ei jälgita. Kui transiidis olevaid varusid tuleb jälgida, tuleb selle asemel kasutada üleviimistellimust. Üleviimistöölehe sisestamisel luuakse iga töölehe rea jaoks kaks varude kannet.

-   Lao väljaminek asukohast „kust”.
-   Lao sissetulek asukohas „kuhu”.

### <a name="bom"></a>Kooslus

Kui kinnitate koosluse lõpetatuks, saate luua koosluse töölehe. Koosluse töölehe kasutamisel saate kooslust otse sisestada. Sisestamine loob tootele lao sissetuleku koos seotud koosluse ja koosluses sisalduvate toodete lao väljaminekuga. See varude töölehe tüüp on abiks lihtsate või mahukate tootmisstsenaariumide korral, kui protsesse ei vajata.

### <a name="item-arrival"></a>Kauba saabumine

Saate kasutada kauba saabumistöölehte kaupade sissetuleku registreerimiseks (nt ostutellimustelt). Kauba saabumistöölehe saab luua saabumise haldamise käigus lehelt **Saabumisülevaade** või töölehe sisestuse saab luua käsitsi lehelt **Kauba saabumine**. Kui lubate kauba saabumise töölehe nime puhul komplekteerimiskohtade otsimise, otsib Supply Chain Management saadud kaupade asukohta ja kui ruumi on, loob sissetulevatele kaupadele sihtkohad.

### <a name="production-input"></a>Materjalid tootmisse

Tootmise sisendtöölehed toimivad kauba saabumistöölehtede sarnaselt, kuid neid kasutatakse tootmistellimuste puhul.

### <a name="counting"></a>Inventuur

Inventuuritöölehtede abil saate korrigeerida praegust vaba kaubavaru, mis on kaupade või kaubagruppide puhul registreeritud, ja seejärel sisestada tegeliku füüsilise inventuuri nii, et saate teha vajalikke korrigeerimisi erinevuste tasakaalustamiseks. Saate seostada inventuuripoliitikad inventuurigruppidega, et aidata rühmitada erinevate omadustega kaupu, nii et need kaubad saaks lisada inventuuri töölehele. Näiteks saate seadistada inventuurigrupid nii, et need loeksid kaupu, millel on konkreetne sagedus, või loeksid kaupu siis, kui varud langevad teatud tasemele. Teavet inventuurigruppide määratlemise kohta leiate jaotisest [Laoinventuuri protsesside määratlemine](tasks/define-inventory-counting-processes.md).

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

## <a name="data-entity-support-for-inventory-journals"></a>Andmeüksuse tugi laotöölehtedele

Andmeüksused toetavad järgmist tüüpi integratsioonistsenaariume:
-    sünkroonne teenus (OData);
-  asünkroonne integreerimine.

Lisateavet vt jaotisest [Andmeüksused](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).

> [!NOTE]
> Kõigis laotöölehtedes pole OData lubatud, seetõttu ei saa te andmete avaldamiseks, värskendamiseks ja Supply Chain Managementi tagasi importimiseks kasutada Exceli andmekonnektorit. 

Veel üks töölehe andmeüksuste erinevus on võimalus kasutada liitüksuseid, mis sisaldavad nii päist kui ka rea andmeid. Praegu saate liitüksuseid kasutada järgneva jaoks.
-   Varude korrigeerimistööleht
-   Varude liikumise tööleht

Need kaks laotöölehte toetavad andmehalduse importimisprojekti osana ainult stsenaariumit *Laovaru lähtestamine*.
-  Kui töölehe päise number pole määratud, kuid töölehe tüübile on määratud numbriseeria, loob importimistöö töölehe päised 1000 rea kohta automaatselt. Näiteks 2020 rea importimise tulemuseks on järgmised kolm töölehe päist.
    -  Päis 1: sisaldab 1000 rida
    -  Päis 2: sisaldab 1000 rida
    -  Päis 3: sisaldab 20 rida
-  Eeldatakse, et iga varude dimensiooni kohta on olemas kordmatu reateave, mis võib olla toote-, laoala- või jälgimisdimensioon. Seetõttu ei saa importida töölehe ridu, kus sama importimisprojekti raames on ridade erinevuseks ainult kuupäevaväli.

## <a name="additional-resources"></a>Lisaressursid

[Andmeüksused](../../fin-ops-core/dev-itpro/data-entities/data-entities.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]