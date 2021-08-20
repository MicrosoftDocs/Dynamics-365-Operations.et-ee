---
title: Aadressiraamatute KKK
description: See teema sisaldab vastuseid korduma kippuvatele küsimustele, mis on seotud aadressiraamatutega.
author: msftbrking
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5809d4a29c4209d8fb42bdfd441a3a4fb201ca6c6318abc0315a02ead7c551de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759157"
---
# <a name="address-books-faq"></a>Aadressiraamatute KKK

[!include [banner](../includes/banner.md)]

## <a name="how-do-i-check-for-duplicate-records"></a>Kuidas topeltkirjeid kontrollida?

Saate kontrollida topeltkirjeid otse loendilehelt **Globaalne aadressiraamat**. Klõpsake tegumiribal vahekaardi **Osapool** grupis **Halda** valikut **Duplikaatide otsimine**. Seejärel valige väärtused, mida duplikaatide otsimisel kaasata.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Kas osapoolte kirjeid saab aadressiraamatusse hulgi lisada või sealt kustutada?

Jah, saate lisada aadressiraamatusse mitu osapoolekirjet ja ka mitu osapoole kirjet eemaldada.

- Mitme osapoole kirje lisamiseks aadressiraamatusse valige loendilehelt **Globaalne aadressiraamat** loendis olevad osapooled. Seejärel klõpsake tegumiribal vahekaardi **Osapool** grupis **Halda** valikut **Osapoolte määramine**. Valige aadressiraamatud, kuhu valitud osapoole kirjed lisada, ja seejärel klõpsake nuppu **OK**. Kõik valitud osapoole kirjed lisatakse valitud aadressiraamatutesse.
- Mitme osapoole kirje eemaldamiseks aadressiraamatust valige loendilehelt **Globaalne aadressiraamat** loendis olevad osapooled. Seejärel klõpsake tegumiribal vahekaardi **Osapool** grupis **Halda** valikut **Osapoolte eemaldamine**. Valige aadressiraamatud, millest osapooled eemaldada, ja klõpsake siis nuppu **OK**. Kõik valitud osapoole kirjed eemaldatakse valitud aadressiraamatutest.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Kas saan kirje osapoole tüüpi muuta või pean vana kirje kustutama ja uue looma?

Aeg-ajalt võib olla vaja kirje osapoole tüüpi muuta (isikust organisatsiooniks või organisatsioonist isikuks). Näiteks Nancy kuulub ettevõtte Fabrikam U.K. müügi töörühma. Londonis kohtab ta ärimessil kuut uut potentsiaalset klienti. Nancy loob igale potentsiaalsele kliendile potentsiaalse kliendi osapoole kirje. Kui Nancy kirjed salvestab, luuakse iga kirje ka globaalses aadressiraamatus. Fabrikam on määratud osapoole vaiketüübiks organisatsiooni, kuid kahe uue potentsiaalse kliendi kirje tüüp peaks olema isik. Seetõttu, kui Nancy ärimessilt naaseb, peab ta kahe potentsiaalse kliendi osapoole tüüpi muutma. Osapoole kirje osapoole tüübi muutmiseks tuleb esmalt luua globaalses aadressiraamatus uus õige tüübiga osapoole kirje. Seejärel saab vana osapoole kirje selle uue kirjega seostada. Pärast uue osapoolega seostamist kustutage algne osapoole kirje, millel on vale kirje tüüp.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Kuidas muuta osapoole kirje nime või aadressi?

Saate muuta osapoole kirje nime ja selle kirjega seotud aadresse igal ajal.

- Osapoole kirje nime muutmiseks avage osapoole kirje ja klõpsake siis tegumipaanil käsku **Redigeeri**. Sisestage kiirkaardil **Üldine** osapoolele uus nimi ja salvestage siis kirje.
- Osapoole kirje aadressi muutmiseks avage osapoole kirje ja valige siis kiirkaardilt **Aadressid** muudetav aadress. Klõpsake käsku **Redigeeri** ja seejärel tehke lehel **Muuda aadressi** vajalikud aadressi või selle parameetrite muudatused.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Kas saan ühendada mitu osapoole kirjet üheks kirjeks?

Mõnikord võib olla vaja ühendada mitu osapoole kirjet üheks kirjeks. See võib juhtuda, kui loote osapoole kirjeid tahtlikult või tahtmatult topelt. Osapoole kirjete ühendamisel tuleb valida üks kirje, mis alles jäetakse. Seejärel lisatakse teiste kirjete andmed sellesse kirjesse. Näiteks avastate, et Fabrikami andmed on salvestatud kolme osapoole kirjesse: A, B ja C. Otsustate hoida alles osapoole kirje A. Seetõttu lisatakse osapoole kirjetesse B ja C salvestatud andmed osapoole kirjesse A. On mõned olukorrad, kus osapoole kirjeid ei saa ühendada.

- Ühendada ei saa neid osapoole kirjeid, mis on seotud sama osapoole rolliga (nt kliendi või hankijaga) samas juriidilises isikus. Näiteks oletame, et osapool A on seotud kliendiga juriidilises isikus 123 ja osapool B on seotud teise kliendiga juriidilises isikus 123. Neid osapoole kirjeid ei saa ühendada, kuna nende ühendamisel oleks ühendatud osapoole kirje seotud mitme kliendiga samas juriidilises isikus ja see pole lubatud. Kuid kirjeid saab ühendada, kui osapool B on seotud hankijaga juriidilises isikus 123 või kliendiga teises juriidilises isikus.
- Ühendada ei saa sisemise osapoole organisatsioonikirjeid samas juriidilises isikus, töörühmas või tootmisüksuses.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Kas peaksin looma osapoole kirje globaalses aadressiraamatus või muus kohas, näiteks kliendi või hankija lehel?

Saate sisestada osapoole kirjeid globaalsesse aadressiraamatusse või vastava üksuse lehele. Ühes asukohas kirje lisamisel lisatakse alati sama kirje ka teise asukohta. Näiteks kui lisate kliendi osapoole kirje globaalsesse aadressiraamatusse, lisatakse see kirje ka lehele **Klient**. Samamoodi, kui lisate kliendi osapoole kirje lehele **Klient**, lisatakse kirje ka globaalsesse aadressiraamatusse. Juhinduge järgmistest põhimõtetest otsustamisel, kuhu uued osapoole kirjed sisestada tuleks.

- **Osapoole kirje loomine, kui te üksuse tüüpi ei tea** – kui peate looma osapoole kirje, kuid ei tea üksuse tüüpi (näiteks te ei tea, kas üksus on klient või müügivõimalus), looge kirje globaalses aadressiraamatus. Hiljem saate valida üksuse tüübi.
- **Osapoole kirje loomine, kui teate üksuse tüüpi** – kui teate osapoole üksuse tüüpi, saate luua kirje selle tüübi puhul kehtival lehel. Näiteks kliendi kirje looge lehel **Klient**. Kui loote ja salvestate kirje lehekülje sobiva üksuse lehel, luuakse kirje automaatselt globaalses aadressiraamatus.

## <a name="can-i-translate-address-information-for-party-records"></a>Kas saan tõlkida osapoole kirjete aadressiteavet?

Saate seadistada aadressiteabe tõlkeid, nii et teave kuvatakse programmis teie kasutajakeeles (süsteemikeeles), kuid dokumentidel (nt müügitellimustel) muus keeles. Saate sisestada riigi/piirkonna nimede, aadressi eesmärkide ja nimeseeriate tõlkeid. Näiteks oletame, et teie süsteemikeel on taani keel ja loote müügitellimuse Prantsusmaal asuvale kliendile. Sel juhul saate vaadata kliendikirjet programmis taani keeles, kuid kuvada prinditud müügitellimusel aadressiteabe prantsuse keeles. Tõlgete seadistamisel tuleb sisestada iga loendis oleva üksuse tõlke. Kõik üksused, millele te tõlget ei sisesta, kuvatakse süsteemikeeles. Näiteks oletame, et teie süsteemikeel on taani keel ja saadate dokumendi Hispaanias asuvale kliendile. Kui te pole sisestanud aadressiteabele hispaaniakeelseid (ESP) tõlkeid, kuvatakse see teave taani keeles nii programmis kui ka prinditud dokumendil.

## <a name="after-importing-addresses-when-i-access-the-records-why-am-i-unable-to-edit-imported-addresses"></a>Pärast aadresside importimist, kui pääsen juurde kirjetele, miks ma ei saa imporditud aadresse redigeerida?

Aadresside importimisel on olemas väli sildiga **IsLocationOwner**, mis näitab, kas asukohaga seotud osapool (aadress) on aadressi omanik. Kui osapool on aadressi omanik, saab aadressi redigeerida, kui pääseb juurde globaalse aadressiraamatu osapoole kaudu või koondkirje vormilt (nt klient, hankija või töötaja). Kui osapool ei ole aadressi omanik, ei saa kirjet varem loetletud vormidelt redigeerida. Aadresside importimisel peaks **isLocationOwner** olema seadistatud väärtusele **Jah** kui soovite, et aadress oleks seostatud osapoole abil redigeeritav. Siiski on aegu, mil see väli võib olla valesti imporditud. Probleemi lahendamiseks saab asukoha omanikku globaalses aadressiraamatus värskendada osapoole kirjest või **kinnita asukoha omanik** lehelt. Üksiku osapoole kirje värskendamiseks minge **Globaalne aadressiraamat > Aadress**. Valige **Redigeeri** et käivitada leht **Redigeeri aadress**, et muuta omaniku asukohta. Valige **Asukoha omaniku muutmine** et näha eelmise asukoha omanikku, kus praegu valitud osapool on uus asukoha omanik. Kui eelmise asukoha omanik on tühi, tähendab see, et asukoha omanikku ei loodud. Suvandi **Täpsemalt** valimine avab lehe **Halda aadresse** kus saab seada ka asukoha omaniku. Valige uuendatav asukoht ja seejärel valige **Määra asukoha omanik** käsk menüüst. Mitme kirje asukoha omaniku värskendamiseks minge **Globaalne aadressiraamat > Asukohad > Kinnitage asukoha omanikud**. Loend sisaldab asukohti, mis on lingitud ühe osapoolega, kuid see osapool pole omanik. Kui valite **Kinnita omanik** määratakse seotud aadressi **omanikuks pakutud omava osapoole ID** et olla seotud aadressi omanik. Kui osapool on määratud omanikuks, on lingitud aadress osapoole kirjest redigeeritav. Asukoha omaniku muutmiseks peate lehel **Turvalisuse konfiguratsioon** määrama privileegi **Määra asukoha omanik**.  Vaikimisi on antud süsteemiadministraatorile see privileeg.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

