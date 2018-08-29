---
title: "Üldise töölehe üksuse abil kannete importimise head tavad"
description: "Selles teemas on näpunäited andmete päevaraamatusse importimise kohta, kasutades üksust Päevaraamat."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7bc24b5e3bc13d6dbb4313f25ff44d8fae0998cc
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="best-practices-for-importing-vouchers-by-using-the-general-journal-entity"></a>Üldise töölehe üksuse abil kannete importimise head tavad

[!include [banner](../includes/banner.md)]

Selles teemas on näpunäited andmete päevaraamatusse importimise kohta, kasutades üksust Päevaraamat.  

Saate kasutada üldise töölehe üksust, et importida kandeid, millel on konto või vastaskonto tüüp **Pearaamat, Klient, Hankija või Pank**. Kande saab sisestada ühe reana, kasutades nii välja **Konto** kui ka välja **Vastaskonto**, või mitmerealisena kandena, kus kasutatakse ainult välja **Konto** (ja valik **Vastaskonto** jäetakse igal real tühjaks). Üldine töölehe üksus ei toeta iga konto tüüpi. Selle asemel on olemas muud üksused stsenaariumide puhul, kus on vajalikud erinevad kontotüüpide kombinatsioonid. Näiteks projektikande importimiseks kasutage projektikulu töölehe üksust. Iga üksus on mõeldud konkreetsete stsenaariumide toetamiseks, mis tähendab, et nendele stsenaariumidele mõeldud üksustele, kuid mitte teistele stsenaariumidele mõeldud üksustele võib saadaval olla lisavälju.

## <a name="setup"></a>Häälestus
Enne üldise töölehe üksuse abil importimist kontrollige järgmist seadistust.

-   **Numbriseeria seadistus töölehe partiinumbri jaoks** – päevaraamatu üksuse abil importimisel kasutab töölehe partiinumber pearaamatu parameetrites määratletud numbriseeriat. Kui määrate töölehe partiinumbri numbriseeria väärtuseks **Käsitsi**, ei rakendata vaikenumbrit. See seadistust ei toetata.
-   **Finantsdimensiooni konfigureerimine** – kui üksusi kasutatakse kannete importimiseks, peab iga organisatsioon määratlema finantsdimensioonide järjekorra. Tellimus määratletakse vormingule **Pearaamatu dimensioonide integreerimine** valikus **Pearaamat** &gt; **Kontoplaan** &gt; **Dimensioonid** &gt; **Finantsdimensiooni konfiguratsioon rakenduste integreerimiseks** &gt; **Andmeüksuste valimine**. Imporditava pearaamatukonto segmendid peavad olema samas järjekorras. Vastasel korral tekib importimise ajal tõrge.

## <a name="general-journal-entity-setup"></a>Päevaraamatu üksuse seadistus
Kaks sätet andmehalduses mõjutavad vaiketöölehe partiinumbri ja kandenumbri rakendamist.

-   **Komplektipõhine töötlemine** (andmeüksuses)
-   **Automaatselt loodud** (välja vastendamisel)

Järgmistes jaotistes kirjeldatakse nende sätete mõju ja selgitatakse, kuidas töölehe partiinumbreid ja kandenumbreid luuakse.

### <a name="journal-batch-number"></a>Töölehe partiinumber

-   Seadistus **Kogumipõhine töötlemine** päevaraamatu üksusel ei mõjuta seda, kuidas töölehe partiinumbreid luuakse.
-   Kui välja **Töölehe partiinumber** väärtuseks on määratud **Automaatselt loodud**, luuakse uus töölehe partiinumber igale imporditavale reale. Selline käitumine ei ole soovitatav. Säte **Automaatselt loodud** on projekti importimise all jaotises **Kuva kaart** vahekaardil **Vastendamise andmed**.
-   Kui välja **Töölehe partiinumber** väärtuseks ei ole määratud **Automaatselt loodud**, luuakse töölehe partiinumber järgmiselt.
    -   Kui imporditud failis määratletud töölehe partiinumber vastab olemasolevale sisestamata päevaraamatule, imporditakse kõik vastava töölehe partiinumbriga read olemasolevale töölehele. Ridu ei impordita kunagi sisestatud töölehe partiinumbrisse. Selle asemel luuakse uus number.
    -   Kui imporditud failis määratletud töölehe partiinumber ei vasta olemasolevale sisestamata päevaraamatule, rühmitatakse kõik sama töölehe partiinumbriga read uue töölehe alla. Näiteks kõik read, mille töölehe partiinumber on 1, imporditakse uuele töölehele ja kõik read, mille töölehe partiinumber on 2, imporditakse teisele uuele töölehele. Töölehe partiinumber luuakse päevaraamatu parameetrites määratletud numbriseeria abil.

### <a name="voucher-number"></a>Kande number

-   Kui kasutate päevaraamatu üksuse seadistust **Kogumipõhine töötlemine**, tuleb imporditud failis esitada kande number. Igale päevaraamatu kandele määratakse imporditud failis antud kande number, isegi kui kanne pole tasakaalustatud. Kui soovite kasutada komplektipõhist töötlemist, kuid soovite kasutada ka numbriseeriat, mis on kandenumbritele määratletud, on 2016. aasta veebruari väljalaske jaoks tehtud kiirparandus. Kiirparanduse number on 3170316 ja selle saab laadida alla teenusest Lifecycle Services (LCS). Lisateavet leiate jaotisest [Kiirparanduste allalaadimine teenusest Lifecycle Services](../migration-upgrade/download-hotfix-lcs.md).
    -   Selle funktsiooni lubamiseks määrake töölehe nimel, mida importimisteks kasutatakse, valiku **Numbrite eraldamine sisestamisel** väärtuseks **Jah**.
    -   Imporditud failis tuleb sellegipoolest kandenumber määratleda. Kuid see number on ajutine ja kandenumber kirjutab selle töölehe sisestamisel üle. Peate veenduma, et töölehe read oleksid ajutise kandenumbriga õigesti grupeeritud. Näiteks sisestamise käigus leitakse kolm rida, millel on ajutine kandenumber 1. Kõigi kolme rea ajutine kandenumber kirjutatakse numbriseerias üle järgmise numbriseerias oleva numbriga. Kui need kolm rida ei ole tasakaalustatud kirje, siis kannet ei sisestata. Järgmiseks, kui leitakse ridu, mille ajutine kandenumber on 2, kirjutab selle numbri üle numbriseeria järgmine kandenumber jne.

<!-- -->

-   Kui te ei kasuta sätet **Komplektipõhine töötlemine**, ei pea te imporditud failis kandenumbrit sisestama. Kandenumbrid luuakse importimise ajal töölehe nime seadistuse põhjal (**Ainult üks kanne**, **Seoses saldoga** jne). Näiteks kui töölehe nimi on määratletud valikuga **Saldoga seoses**, saab esimene rida uue kande vaikenumbri. Seejärel hindab süsteem rida, et määratleda, kas deebetsummad võrduvad kreeditsummadega. Kui real on olemas vastaskonto, saab järgmine imporditav rida uue kande numbri. Kui vastaskontot pole, hindab süsteem iga uue rea importimisel, kas deebetsummad on kreeditsummadega võrdsed.
-   Kui väljale **Kande number** on määratud väärtus **Automaatselt loodud**, siis importimine ei õnnestu. Seadistust **Automaatselt loodud** väljal **Kande number** ei toetata.

Vaikimisi kasutab üksus Päevaraamat kogumipõhist töötlemist. Pärast oma organisatsiooni ärinõuete hindamist tuleb sätet **Kogumipõhine töötlemine** muuta, klõpsates valikut **Andmeüksused** tööruumis **Andmehaldus**. Kogumipõhist töötlemist kasutatakse impordiprotsessi kiirendamiseks. Kui te kogumipõhist töötlemist ei kasuta, on üksuse Päevaraamat importimine aeglasem.




