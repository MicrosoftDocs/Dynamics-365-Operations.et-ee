---
title: Töö stiili eelseadistustega
description: Selles teemas kirjeldatakse, kuidas töötada stiili eelseadistustega rakenduse Microsoft Dynamics 365 Commerce saidiehitajas.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 250f2386cefee8bef45df66c4eef31b4e7fc2686
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411742"
---
# <a name="work-with-style-presets"></a>Töö stiili eelseadistustega

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas töötada stiili eelseadistustega rakenduse Microsoft Dynamics 365 Commerce saidiehitajas.

## <a name="overview"></a>Ülevaade

Stiili eelseadistus kujutab endast kõikide autoriliste stiiliväärtuste kogumit üle kogu saidi teema. Seda saab kasutada selleks, et muuta kohe saidiehitaja kaudu saidi välimust. Stiili eelseadistused võimaldavad saidiehitaja autoritel muuta kiiresti kogu oma saidi stiiliväärtuste kogumit, seda eelvaates kuvada ja aktiveerida, pidamata seejuures kasutama kaskaadlaadistikke (CSS) ega juurutama teemasid. Fondi stiilid, nuppude stiilid ja saidi värvid on tüüpilised stiilimuutujate näited ning neid saab hallata stiili eelseadistuste kaudu.

Saidil saadaolevate stiilimuutujate kogumiku määravad kindlaks saidi rentnikus juurutatud teema ja mooduli teek. Dynamics 365 Commerce’i veebitarkvara arenduse komplekt (SDK) võimaldab arendajatel rakendada nii palju (või vähe) autorilisi stiilimuutujaid kui nad antud teema jaoks vajavad. Rohkemate stiilimuutujate lubamisel võib jätta arendaja saidi stiilidega seotud lõplikud otsused saidiehitaja autorite kätesse. Seetõttu saavad mittearendajad tööriistade kogumit kasutades saidi stiile uuendada ja kuvada vastava eelvaate. Võimalus on kasulik ka olukordades, kus otsesed teemade või CSS muudatused põhjustavad tarbetuid üldkulusid.

Teemad, kus on lubatud autorilised stiilimuutujad, eeldavad stiili eelseadistuse vaikesätet. Nad saavad valikuliselt lisada kasutatud teemapaketi osana täiendavaid eelseadistuste valikuid. Näiteks saab kasutada teemat, millel on ainult üks vaikimisi „kaasaegne hele“ stiili eelseadistus. Teise võimalusena saab kaasata vaike-eelseadistuse kõrval veel täiendavaid stiili eelseadistuste valikuid, nagu näiteks „kaasaegne tume“, „vanaaegne hele“ või „vanaaegne tume“. Need sisseehitatud teema eelseadistused on loodud arendajate poolt ning neid saab kasutada uute saidikujunduste alguspunktina.

Saidiehitajas saavad autorid teha valiku teema sisseehitatud eelseadistuste hulgast või luua ise stiili eelseadistusi ja kohandusi, kasutades lubatud stiilimuutujaid. Enne reaalajas saidil aktiveerimist saab saidiehitajas kuvada stiili eelseadistuse eelvaadet. Pärast autori stiilimuudatuste ülevaatust saab määrata stiili eelseadistuse reaalajas saidil olekusse „aktiivne“.

## <a name="preview-a-style-preset"></a>Stiili eelseadistuse eelvaade

Saidi stiili eelseadistuse eelvaate kuvamiseks saidiehitajas, toimige järgmiselt.

1. Avage saidi vasakpoolsel navigeerimispaanil **Saidi sätted \> Kujundus**.
1. Valige kujundusredaktori ülaosas paikneval vahekaardil **Stiili eelseadistused** loetelust **Saadaolevad eelseadistused** sobiv eelseadistus ja seejärel valige eelseadistuse redaktori avamiseks **Kuva**.

    Kui loetelus **Saadaolevad eelseadistused** ei ole hetkel ühtki eelseadistust, siis vaadake kohandatud stiili eelseadistuse loomise kohta teavet teemast [Kohandatud stiili eelseadistuse loomine](#create-a-custom-style-preset).

    > [!NOTE]
    > Teemasse kaasatud eelseadistused on tähistatud märgiga **Sisseehitatud**. Sisseehitatud eelseadistused on kirjutuskaitstud. Sisseehitatud eelseadistuse kopeerimiseks uue kohandatud eelseadistusena, valige eelseadistuse juures kolmikpunkti nupp (**...**) ja seejärel **Salvesta kui**.

1. Klõpsake käsuribal käsul **Eelvaade**.
1. Valige oma saidilt URL, mida stiili eelseadistuse eelvaate jaoks kasutada ja valige **OK**.
1. Valige eelvaateks kanalipõhine ja lokaadipõhine URL-i variant, klõpsates variandi nimel. Avaneb uus eelvaate brauseriaken, kus rakendatakse määratletud lehele valitud stiili eelseadistus.

> [!NOTE]
> Eelvaate URL on püsiv ja autenditud. Seega saate seda kopeerida, kleepida ja saata teistele autenditud töökaaslastele ülevaatuseks, enne kui muudate selle reaalajas saidil olekusse „aktiivne“. Eelvaate URL on kasulik ka stiilide kontrollimiseks erinevates seadmetes, erinevates brauserites ja erinevatel ekraanidel.

> [!TIP]
> Stiili eelseadistust redigeerides võib olla abiks vastava eelvaate brauseriakna avatuna hoidmine eraldi brauseriaknas, et saaksite tehtud muudatused kiiresti kinnitada. Pärast eelseadistuse muudatuste salvestamist, värskendage kasutajakogemuse kontrollimiseks eelvaate brauseriaken.

## <a name="create-a-custom-style-preset"></a>Kohandatud stiili eelseadistuse loomine

Saidiehitajas kohandatud stiili eelseadistuse loomiseks toimige järgmiselt.

1. Avage saidi vasakpoolsel navigeerimispaanil **Saidi sätted \> Kujundus**.
1. Avage kujundusredaktori ülaosas vahekaart **Stiili eelseadistused**, valige käsuribal suvand **Uus eelseadistus**.
1. Sisestage uue eelseadistuse nimi ja kirjeldus ja seejärel valige **Salvesta**. Loodud on uus kohandatav eelseadistus, mis kasutab lähtepunktina teema vaikeväärtusi.

> [!NOTE]
> Lisaks saate luua uue kohandatud stiili eelseadistuse mis tahes olemasoleva eelseadistuse alusel, vajutades antud eelseadistuse juures kolmikpunkti nuppu (**...**) ja valides **Salvesta kui**. Teise võimalusena saate valida eelseadistuse redaktoris käsuribal **Salvesta kui**.

## <a name="modify-global-and-module-type-style-values"></a>Globaalset ja mooduli tüüpi stiiliväärtuste muutmine

Mõned teema stiilimuutujad on ühiskasutuses mitmes moodulitüübis. Neid stiilimuutujaid kutsutakse *globaalseteks* stiilimuutujateks. Näited hõlmavad peamisi saidivärve, vaikefondistiile ja nupustiile. Globaalsete muutujate seadistamisega võite muuta mitme erineva moodulitüübi ilmet.

Mõned stiiliväärtused võivad olla omased ainult ühele moodulitüübile või võivad vastava valiku korral alistada vaikimisi globaalse väärtuse. Kui saidi teemas on rakendatud moodulitüübi stiilimuutujaid, siis saavad saidiehitaja autorid kohandada moodulitüübi stiili globaalsetest sätetest sõltumatult. Moodulitüübi muutujad võivad teema globaalseid stiilimuutujaid võimendada või need alistada.

> [!NOTE]
> Saidi stiiliväärtuste hierarhia toimib järgmiselt. Paremal pool paiknevad stiiliväärtused alistavad endast vasakule jäävad stiiliväärtused.
>
> Teema vaikeväärtused \< Globaalsed stiiliväärtused \< Moodulitüübi stiiliväärtused \< CSS alistamine

Saidiehitajas stiili eelseadistuse globaalse või moodulitüübi väärtuste muutmiseks toimige järgmiselt.

1. Avage saidi vasakpoolsel navigeerimispaanil **Saidi sätted \> Kujundus**.
1. Valige kujundusredaktori ülaosas vahekaardil **Stiili eelseadistused** mis tahes stiili eelseadistuse juures **Kuva**, et avada eelseadistuse redaktor.
1. Valige **Eelvaade** ja järgige avamiseks brauseri täisaknas eelseadistuse eelvaate avamiseks URLi valikujuhiseid. Jätke eelvaate brauseriaken lahti.
1. Valige eelseadistuse redaktoris paremal ülanurgas **Redigeeri**.
1. Kasutage redaktoris mõningate globaalsete stiiliväärtuste muutmiseks stiilimuutujate juhtelemente.
1. Valige redaktori ülaosas vahekaardist **Globaalne** paremale jääval vahekaardil **Moodulid** moodulitüüp, mille stiili tuleb muuta.
1. Kasutage moodulitüübi teatud väärtuste muutmiseks stiili juhtelemente.
1. Kui olete valmis kuvama muudatuste eelvaadet, siis valige käsuribal **Salvesta**.
1. Naaske avatud eelvaate brauseriakna juurde ja värskendage seda. Eelvaate kuvamine brauseri täisaknas on kasulik, kuna võimaldab kontrollida stiilimuudatusi erinevates vaate katkestuspunktides, erinevates brauserites ja erinevate seadmete platvormidel.
1. Kui kõik muudatused on lõpule viidud ja kinnitatud, siis valige redaktori paremal ülaosas **Lõpeta redigeerimine**.

> [!NOTE]
> Kui redigeerite stiili eelseadistust, mis on parasjagu teie saidil aktiivne, siis kuvatakse redaktoris sinine märge **Aktiivne**. See märk näitab, et eelseadistus on parasjagu teie veebisaidil reaalajas kasutusel. Kui muudate aktiivset eelseadistust, siis valige antud muudatuste reaalajas saiti ülekandmiseks käsk **Avalda**.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Reaalajas saidil uue stiili eelseadistuse aktiveerimine

Stiili eelseadistuse oma saidil uue aktiivse eelseadistusena seadistamiseks toimige järgmiselt.

- Valige ühes järgmistest asukohtades **Määra aktiivseks nupp**.

    - Stiili eelseadistuse redaktori käsuriba
    - Põhivaates mis tahes saadaoleva eelseadistuse kolmpunktmenüü (**...**) vahekaardil **Stiili eelseadistused** jaotises **Saidi sätted \> Kujundus**

Eelseadistuse stiiliväärtused muudetakse aktiivseks üle kogu avalikkusele suunatud veebisaidi.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[CSS-i alistusfailidega töötamine](css-override-files.md)

[Leheikooni lisamine](add-favicon.md)

[Tervitussõnumi lisamine](add-welcome-message.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]