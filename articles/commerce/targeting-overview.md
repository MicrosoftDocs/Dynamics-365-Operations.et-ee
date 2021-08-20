---
title: Seadme, turu ja geograafilise asukoha sihtimine
description: Selles teemas kirjeldatakse, kuidas luua, redigeerida ja hallata Microsoft Dynamics 365 Commerce saidikoosturi sihtrühmi ja sihtmärkeseadme-, turu- ja geolokatsiooniteabe abil.
author: sushma-rao
ms.date: 07/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 3ecc04c97b42b17f257aa40f665136c70de398748b9bda0da860c7000c062807
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730847"
---
# <a name="device-market-and-geolocation-targeting"></a>Seadme, turu ja geograafilise asukoha sihtimine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua, redigeerida ja hallata Microsoft Dynamics 365 Commerce saidikoosturi sihtrühmi ja sihtmärkeseadme-, turu- ja geolokatsiooniteabe abil.

Dynamics 365 Commerce võimaldab teil isikupärastada oma lehe sisu variatsioone (tuntud kui *sihtmärgid*) teatud kliendirühmadele (tuntud kui *sihtrühmad*) et aidata suurendada kasutajate kaasatust ja rahulolu. Esmalt saate luua kas sihtrühma või sihtmärgi. Kuid edukas sihtimiskogemus nõuab mõlemat komponenti.

Ärisaidi koostaja sihtrühmade loomine ja haldamine põhineb kliendiandmetel nagu näiteks asukoht, seadmeteave, sisselogimisolek ja muu dünaamiliselt tuletatud teave kliendi veebipäringutest. Samuti saate luua ja hallata e-commerce moodulite ja fragmentide sihtmärke Commerce saidi koostajas.

**Lahtiütlus:** vastutate selle funktsiooni kasutamise eest kooskõlas kõigi kohaldatavate seaduste ja määrustega, sealhulgas sihtimise ja profiilianalüüsiga seotud seaduste ja määrustega. 

## <a name="audiences"></a>Sihtrühmad

Sihtrühm on kasutajate rühm ja rühma kuuluvuse määrab dünaamiliste reeglite kogum. Need reeglid on lihtsad loogikatestid, mida käitatakse klienditaotlustes või muudes saadaolevates segmentides saadaoleva teabe alusel. JA/VÕI tehtemärkide abil saate kombineerida mitut reeglit.

Commerce toetab põhisegmente nagu seadmeteave, sisselogimisolek, soovitaja ja päringustringi parameetrid. Samuti toetab see laiendatavaid segmente ühenduste kaudu kolmandate osapoolte pakkujatega.

### <a name="basic-segments"></a>Põhisegmendid

Vaikimisi on saadaval järgmised segmendid, mida saab kaasata sihtrühma määratlustesse:

- **Sisselogitud olek** – testige, kas kasutaja on autenditud.
- **Seadme platvorm** – testige järgmisi seadmetüüpe:

    - Mobiil
    - Töölaud
    - Tahvelarvuti
    - Muud

- **Seadme OS** – järgmiste operatsioonisüsteemide test:

    - Windows
    - Linux
    - iOS
    - Android, muu

- **Päringustringi parameetrid** – saate testida võtmeväärtuse paari olemasolu päringu URL-i päringustringi parameetris. Näiteks URL-i `www.fabrikam.com/en-us/request?promo=true` jaoks võib kirjutada reegli, et testida, kas **promo** parameetri väärtus on **tõene**.
- **Küpsis** – testige küpsise väärtusi, mis on määratud domeenile taotluse URL-is. Näiteks võib Fabrikam.com taotlus sisaldada küpsist, mille nimi on **CustomLayout** ja väärtus **1**. Küpsisetest kontrollib küpsise olemasolu, kuid ei loo seda selgesõnaliselt. Eelmises näites peab JavaScript olema eelnevalt seadistatud **CustomLayout** küpsise mõnest muust moodulist või mõnest muust äriprotsessist.

    > [!NOTE]
    > Veenduge, et küpsiste kasutamine vastab kohaldatavatele seadustele.

- **Soovitaja** – kui kasutaja järgib lehe taotlemiseks linki, on soovitajaks lingi majutanud lehe URL.

### <a name="extensible-segments"></a>Laiendatavad segmendid

Commerce võimaldab teil laiendada saadaolevate segmentide loendit, luues ühenduse muude tootjate segmentimispakkujatega. Segmentimisteenuse pakkuja kirjeldab saadaolevate segmentide tüüpe. Lisateavet geolokatsiooni või segmentimise pakkujaga ühenduse loomise kohta leiate teemast [Konnektorite konfigureerimine ja lubamine](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Kui väline pakkuja on lubatud, võib see luua ühenduse teenusega, millel on ettearvamatu jõudlus. Parema kasutajakogemuse tagamiseks, kui kasutaja taotleb sihtimist sisaldavat lehte ja see leht viitab sihtrühmale, kes kontrollib kolmanda osapoole segmendipakkujat, kuvatakse lehe vaikeversioon.
> - Küpsiste lubamiseks peab kasutaja nõustuma. Seejärel küsib kasutaja brauser kõigilt segmentidelt asjaomastelt pakkujatelt ja tulemused pannakse küpsisesse, mis tagastatakse kasutajale. Lehele järgnevad taotlused kasutavad seda teavet kasutajale suunatud sisu edastamiseks. Lisateavet küpsiste nõuetele vastavuse kohta leiate teemast [Küpsiste vastavus](cookie-compliance.md).

**Lahtiütlemine**: kui selle funktsiooni lubate, jagatakse teie andmeid teie valitud kolmandate osapoolte süsteemidega. Saate määrata, milliseid andmeid, kui üldse, kolmandale osapoolele esitate. Te mõistate, et kolmanda osapoole andmekäitlus- ja vastavusstandardid võivad erineda Microsoft Dynamics 365 Commerce standarditest. Teie privaatsus on Microsoftile oluline. Lisateabe saamiseks lugege meie [privaatsus- ja küpsiseteadet](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>Sihtrühma loomine saidikoosturis

Sihtrühma loomiseks Commerce'i saidiehitajas, toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanil suvand **Sihtrühm**.
1. Valige suvand **Uus**.
1. Sisestage sihtrühmale nimi. Soovi korral saate lisada ka silte ja kirjeldust.
1. Valige **Loo** ja seejärel **Lisa uus reegliplokk**. Reegliplokk on reeglite kogum, mis on ühendatud AND-tingimustega. Samuti saate luua mitu reegliplokki, mille vahel on VÕI-tingimused.
1. Valige oma segmentidele andmeallikas ja seejärel määrake segmendi nimi, tehtemärk ja väärtused. Reegliplokis saate luua ja kustutada rohkem reegleid või luua ja kustutada terveid reegliplokke. Reegliplokke saate vastavalt vajadusele teisaldada ka üles või alla.

    > [!NOTE]
    > Loendis võib olla kuni 100 väärtust ja iga loendiüksus võib sisaldada kuni 50 märki.

1. Kui olete publiku konfiguratsiooniga rahul, valige **Lõpeta redigeerimine**. Seejärel saate valida **Avalda**, et muuta sihtrühm reaalajas sihtmärgis kasutamiseks kättesaadavaks. Teise võimalusena võite avaldada sihtrühma koos sihtmärgiga. 

Sihtrühma redigeerimiseks valige selle hüperlink **Sihtrühmad** vahekaardil ja seejärel valige käsk **Redigeeri** kuvatavas publikuredaktoris. Sihtrühmale viitavate sihtmärkide ja lehtede loendi kuvamiseks valige sihtrühma loendivaates sihtrühm ja seejärel valige **Kuva määrangud**. Sihtrühma kustutamiseks sihtrühma loendivaates või sihtrühma redaktoris tühistage selle avaldamine, kui see on juba avaldatud, ja seejärel valige käsuribal käsk **Kustuta**.

> [!NOTE]
> Sihtrühmad on Commerce saidi koostaja saiditaseme kontseptsioon. Sama sihtrühma saate jagada mitme sihtmärgi vahel.

## <a name="targets"></a>Sihtmärgid

Sihtmärk on kasutajakogemus, mida näidatakse ühe või mitme valitud sihtrühma liikmetele. See võib sisaldada ühe või mitme mooduli variatsioone leheküljel või fragmendis. 

Saate määratleda oma sihtmärkide ajakava, et määrata, kui kaua need peaksid aktiivseks jääma. Pange tähele, et see toiming on eraldiseisev avaldamisrühma plaanimise toimingust, mis määratleb, millal sisukogum avaldatakse. Samuti saate vaadata oma sihtmärkide eelvaadet, et näha, millised need valitud sihtrühmade liikmetele välja näevad. Lisaks saate seada oma sihtmärgid tähtsuse järjekorda, et määrata, milline sihtmärk tuleks konflikti korral kuvada.

### <a name="create-a-target"></a>Sihtmärgi loomine

Commerce'i saidiehitajas lehemoodulite sihtkesta loomiseks toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanil suvand **Lehed**. Seejärel valige selle lehe hüperlink, millel on moodulid, mida soovite sihtida.
1. Lehe redigeerimiseks vaatamiseks valige **Redigeeri**.
1. **Sihtrühma** menüüs valige **Uus sihtrühm** et luua uus sihtkest. Saate luua lehel vastavalt vajadusele mitu sihtmärki.
1. Sisestage uue eelseadistuse nimi ja kirjeldus ja seejärel valige **Järgmine**.
1. Valige **Lisa** sihtrühmade kaasamiseks, kes näevad sihitud sisu, või et välistada sihtrühma. Seejärel valige **Järgmine**.

    > [!NOTE]
    > Sihtrühma määramine on sihtmärgi loomisel valikuline samm. Kuid enne sihtmärgi avaldamist peate kaasama vähemalt ühe sihtrühma, et tagada sihtrühmade sihtsisu nägemine.

1. Määratlege sihtmärgi kuvamise ajaaken, valides ajavööndi ning algus- ja lõppkuupäevad ning kellaajad. Saate seada sihtmärgi nii, et seda kuvataks akna ajal kogu aeg, või valida kindlad päevad ja kellaajad. Kui olete lõpetanud, valige **Järgmine**.

    > [!NOTE]
    > Teie määratud kellaajad ja ajavöönd on globaalsed. Kui soovite sihtida erinevaid asukohti erinevatel aegadel või erinevates ajavööndites, peate looma erinevad sihtmärgid ja määratlema iga asukoha jaoks soovitud ajakava.

1. Vaadake üksikasjad üle ja kui kõik tundub õige, valige **Loo sihtkogemus** ja seejärel **Mine sihtmärgini**. Sihtkest on loodud. Nüüd saate sellele mooduleid lisada.
1. Valige sihtmärgile moodul, valige kolmikpunkt (**...**) ja seejärel valige **Lisa praegusele sihtmärgile**. Kui sihite emamoodulit, saavad kõik selle tütred selle sihtmärgi osaks. Sihtmoodulid on esile tõstetud roheliselt.
1. Tehke sihtmoodulile vajalikud sisuvärskendused ja lisage sihtmärgile vastavalt vajadusele veel mooduleid. Siis valige oma muudatuste salvestamiseks **Salvesta**.
1. Enne sihtmärgi avaldamist valige selle läbivaatamiseks käsuribal kindlasti **Eelvaade**. Tehke siis üks järgmistest valikutest:

    - **Põhieelvaade** – valige see suvand ainult valitud variatsiooni (vaikelehe või sihtmärgi) eelvaate kuvamiseks ilma seostatud sihtrühmadeta.
    - **Täpsem eelvaade** – valige see suvand, kui lehel on mitu sihtmärki ja soovite nende eelvaadet vaadata kasutajana, kes kuulub valitud sihtrühmade kogusse, või kindlal kuupäeval/kellaajal. Valige **Järgmine** asjakohaste sihtrühmade loendist valimiseks. Filtri saate eemaldada ka kõigi sihtrühmade hulgast valimiseks.

1. Kui olete sihtkonfiguratsiooniga rahul, peate lehe avaldama, et sihtmärk läheks live`i. Valige **Avalda** sihtmärgi kohese töö jätkamiseks. Teise võimalusena võite lehe reaalajas käivitamise ajastamiseks kasutada avaldamisrühma. Lisateavet avaldamisrühmade kohta leiate teemast [Avaldamisrühmadega töötamine](publish-groups.md).

Võite sihtida ka fragmente. Protseduur on sarnane. Kuid juhises 1 valite vasakul navigeerimispaanil lehtede asemel **Fragmendid** mitte **Lehed**.

> [!NOTE]
> Et vältida negatiivset mõju mõõdikutele, võite lehel või fragmendis valida kas katse või sihtmärgi. Sul ei saa olla mõlemat, nii eksperimenti kui sihtmärki.

### <a name="manage-targets"></a>Halda sihtmärke

Sihtmärkide redigeerimiseks, dubleerimiseks või kustutamiseks vaikelehele või fragmendile tehke järgmist.

1. Valige rippmenüüst **Sihtmärk** ja seejärel **Halda sihtmärke**.
1. Valige redigeeritav, dubleeritav või kustutatav sihtmärk.
1. Kui teil on samas moodulis mitu sihtmärki või kui mitmel sihtmärgil on vastuolulised ajakavad, valige **Prioritiseeri sihtmärgid**, et määrata nende kuvamise järjekord. Kui lisate lehele või fragmendile rohkem kui ühe sihtmärgi, kuvatakse teavitusribal nupp **Prioritiseeri sihtmärgid**, et tuletada meelde sihtmärkide prioritiseerimist. Kui prioriteeti pole määratud, valitakse vaikimisi viimane sihtmärk.

### <a name="localize-targets"></a>Sihtmärkide lokaliseerimine

Lehekülgedel ja fragmentides olevad sihtmärgid kaasatakse automaatselt XLIFF-failide eksportimisel ja importimisel lokaliseerimise eesmärgil. Kui aga lokaadid pole vajalikud, saate nende sihtmärgid pärast lokaliseeritud XLIFF-failide importimist kustutada.

> [!NOTE]
> Sihtmärke hallatakse kanali ja lokaadi kaupa. Ühes kanalis või lokaadis sihtmärkidele tehtavaid muudatusi ei edastata automaatselt teistesse kanalitesse ega lokaadi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
