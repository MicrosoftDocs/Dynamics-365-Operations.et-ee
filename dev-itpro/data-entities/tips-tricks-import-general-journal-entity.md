---
title: "Parimaid tavasid kasutades peažurnaali ettevõte kannete importimiseks"
description: "Sellest teemast leiate näpunäiteid andmete importimiseks peažurnaali abil üldist töölehe üksuse."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Parimaid tavasid kasutades peažurnaali ettevõte kannete importimiseks

Sellest teemast leiate näpunäiteid andmete importimiseks peažurnaali abil üldist töölehe üksuse.  

Ettevõte peažurnaali abil saate importida kanded, mis on konto või seda konto liigi kohta **pearaamatu, kliendi, hankija või Pank**. Kannet saab sisestada ühe reana, kasutades nii **konto** välja ja **vastaskonto** välja, või mitme rea kande, kus on **konto** välja kasutatakse (ja **vastaskonto** tühjaks igal real). Peažurnaali üksus ei toeta iga konto tüüp. Selle asemel on olemas muud üksused stsenaariumide puhul, kus on vajalikud erinevad kontotüüpide kombinatsioonid. Näiteks projekti kannete importimiseks kasutada projekti kulude töölehe üksuse. Iga üksus toetamiseks mõeldud konkreetsete stsenaariumide, mis tähendab, et täiendavate väljade võib saadaval üksuste stsenaariumid kuid mitte üksuste erineva stsenaariumi jaoks.

## <a name="setup"></a>Häälestus
Enne importimist peažurnaali üksuse abil, kontrollida järgnevalt:

-   **Numbriseeria seadistust töölehe partiinumber** - vaikimisi, kui kasutades peažurnaali üksus, töölehe partii number kasutab määratud pearaamatu parameetrite numbriseeriat. Kui määrate töölehe partiinumbri numbriseeria väärtuseks **Käsitsi**, ei rakendata vaikenumbrit. See seadistust ei toetata.
-   **Rahalise küljega konfiguratsiooni** -finantsdimensioonide järjekorra peate määratlema iga organisatsioon, kui üksuste kasutatakse kannete importimiseks. Tellimuse jaoks määratletud ning **pearaamatu mõõtmed integratsiooni** formaadis, kell **PR**&gt;**kontoplaani**&gt;**mõõdud**&gt;**rahalise küljega konfiguratsiooni rakenduste integreerimise**&gt;**valige andmete üksuste**. Imporditava pearaamatukonto segmendid peavad olema samas järjekorras. Vastasel korral tekib importimise ajal tõrge.

## <a name="general-journal-entity-setup"></a>Päevaraamatu üksuse seadistus
Kaks andmehaldus seadetest kuidas rakendatakse vaikimisi töölehe partiinumber või kande number:

-   **Komplekt töötlemine** (olemis andmed)
-   **Automaatselt loodud** (linna väljavastenduse)

Järgmistes jaotistes kirjeldatakse nende sätete mõju ja selgitatakse, kuidas töölehe partiinumbreid ja kandenumbreid luuakse.

### <a name="journal-batch-number"></a>Töölehe partiinumber

-   Seadistus **Kogumipõhine töötlemine** päevaraamatu üksusel ei mõjuta seda, kuidas töölehe partiinumbreid luuakse.
-   Kui välja **Töölehe partiinumber** väärtuseks on määratud **Automaatselt loodud**, luuakse uus töölehe partiinumber igale imporditavale reale. Selline käitumine ei ole soovitatav. Säte **Automaatselt loodud** on projekti importimise all jaotises **Kuva kaart** vahekaardil **Vastendamise andmed**.
-   Kui välja **Töölehe partiinumber** väärtuseks ei ole määratud **Automaatselt loodud**, luuakse töölehe partiinumber järgmiselt.
    -   Kui imporditud failis määratletud töölehe partiinumber kattub mõne olemasoleva, konteerimata päevasele töölehele Microsoft Dynamics 365 toiminguteks, imporditakse kõik read, mis on vastavaid töölehe partiinumber olemasoleva töölehe. Ridu ei impordita kunagi sisestatud töölehe partiinumbrisse. Selle asemel luuakse uus number.
    -   Kui töölehe partiinumber, mis määratletakse imporditud fail ei vasta mõne olemasoleva, konteerimata päevasele töölehele Dynamics 365 toiminguteks, kõik read, mis on sama töölehe partiinumber on rühmitatud all uuele töölehele. Näiteks kõik read, mille töölehe partiinumber on 1, imporditakse uuele töölehele ja kõik read, mille töölehe partiinumber on 2, imporditakse teisele uuele töölehele. Töölehe partiinumber luuakse päevaraamatu parameetrites määratletud numbriseeria abil.

### <a name="voucher-number"></a>Kande number

-   Kui kasutate päevaraamatu üksuse seadistust **Kogumipõhine töötlemine**, tuleb imporditud failis esitada kande number. Igale päevaraamatu kandele määratakse imporditud failis antud kande number, isegi kui kanne pole tasakaalustatud. Kui soovitud komplekt töötlemine, kuid soovite kasutada määratletud numbriseeria kandenumbrite Dynamics 365 toiminguteks, kiirparandus on esitatud veebruar 2016 vabastamiseks. Kiirparanduse number on 3170316 ja selle saab laadida alla teenusest Lifecycle Services (LCS). Lisateavet leiate jaotisest [Kiirparanduste allalaadimine teenusest Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   Selle funktsiooni kohta töölehe nimi, mida kasutatakse impordi Dynamics 365 korral määrata **numbri eraldamine sisestamisel** et **Jah**.
    -   Imporditud failis tuleb sellegipoolest kandenumber määratleda. Aga see number on ajutine ja kirjutatakse Dynamics 365 toimingute kandenumbri puhul, kui tööleht on sisestatud. Peate veenduma, et töölehe read oleksid ajutise kandenumbriga õigesti grupeeritud. Näiteks konteerimisel, kolm rida leitakse mis on ajutine kande number 1. Kõik kolm rida ajutise kandenumber kirjutatakse numbriseeria järgmine number. Kui need kolm rida ei ole tasakaalustatud kirje, siis kannet ei sisestata. Järgmiseks, kui leitakse ridu, mille ajutine kandenumber on 2, kirjutab selle numbri üle numbriseeria järgmine kandenumber jne.

<!-- -->

-   Kui te ei kasuta selle **komplekt töötlemine** seadmine, võite jätta imporditud failis kande numbrit. Kandenumbrid luuakse importimise ajal töölehe nime seadistuse põhjal (**Ainult üks kanne**, **Seoses saldoga** jne). Näiteks kui töölehe nimi on määratletud valikuga **Saldoga seoses**, saab esimene rida uue kande vaikenumbri. Seejärel hindab süsteem rida, et määratleda, kas deebetsummad võrduvad kreeditsummadega. Kui real on olemas vastaskonto, saab järgmine imporditav rida uue kande numbri. Kui vastaskontot pole, hindab süsteem iga uue rea importimisel, kas deebetsummad on kreeditsummadega võrdsed.
-   Kui väljale **Kande number** on määratud väärtus **Automaatselt loodud**, siis importimine ei õnnestu. Seadistust **Automaatselt loodud** väljal **Kande number** ei toetata.

Vaikimisi kasutab üksus Päevaraamat kogumipõhist töötlemist. Pärast oma organisatsiooni ärinõuete hindamist tuleb sätet **Kogumipõhine töötlemine** muuta, klõpsates valikut **Andmeüksused** tööruumis **Andmehaldus**. Kogumipõhist töötlemist kasutatakse impordiprotsessi kiirendamiseks. Kui te kogumipõhist töötlemist ei kasuta, on üksuse Päevaraamat importimine aeglasem.


