---
title: Kviitungivormingute häälestamine ja kujundamine
description: See artikkel kirjeldab, kuidas vormikavandeid luua ja muuta, et kontrollida kviitungite, arvete ja muude dokumentide printimise viisi. Dynamics 365 Commerce is on vormi kavandi kujundaja funktsioon, millega saab hõlpsalt ja graafiliselt luua ning muuta mitmesuguseid vormi kavandeid.
author: BrianShook
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dac0ad75ff35367b5d6ac84c75c68e22e2cb0cb1
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779397"
---
# <a name="set-up-and-design-receipt-formats"></a>Kviitungivormingute häälestamine ja kujundamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas vormikavandeid luua ja muuta, et kontrollida kviitungite, arvete ja muude dokumentide printimise viisi. Dynamics 365 Commerce sisaldab vormi kavandi kujundaja funktsioon, millega saab hõlpsalt ja graafiliselt luua ja muuta mitmesuguseid vormi kavandeid.

> [!IMPORTANT]
> Peate seadistama vormipaigutused ja kviitungiprofiilid, et printida Retail Modern POS-ist ja pilvekassast kviitungeid ja muid dokumente. Kviitungiprofiilile saab lisada mitu vormipaigutust. Seejärel saate riistvara profiili muutes kviitungi profiilile printeri määrata.

## <a name="set-up-a-receipt-format"></a>Kviitungivormingu seadistamine

1. Avage **Jaemüük ja kaubandus** &gt; **Kanali häälestus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kviitungi vormingud**.
2. Uue vormikavandi loomiseks või olemasolevate vormikavandite hulgast sobiva valimiseks klõpsake lehel **Kviitungi vorming** nuppu **Uus**.
3. Sisestage väljale **Kviitungi vorming** vormikavandi identifikaator ja valige seejärel kviitungi tüüp, mille jaoks seda kavandit kasutatakse. Kviitungile saate ka kirjelduse ja lühikese nime väljal **Pealkiri** sisestada.
4. Prindikäitumise määratlemiseks valige suvand kiirkaardilt **Üldine**.

    - **Prindi alati** – kviitung prinditakse automaatselt nagu ette nähtud.
    - **Ära prindi** – kviitungit ei prindita.
    - **Küsi kasutajalt** – kasutajalt küsitakse kviitungi printimise kohta.
    - **Nagu on nõutud** – seda valikut kasutatakse ainult ostukviitungite puhul. Kui see suvand on valitud, saab kasutaja vajadusel ostukviitungi leheküljelt **Muuda** printida.

## <a name="print-images"></a>Piltide printimine

Kviitungi kujundaja sisaldab muutujat **Logo**. Selle muutuja abil saate määrata pildi, mis tuleks kviitungitele printida. Pildid, mis trükitakse kviitungitele muutuja **Logo** abil peaksid olema monokroomise bitmapi (.bmp) failitüübiga. Kui kviitungi kujundaja on määranud bitmapi kujutise, kuid seda ei prindita kviitungi printerile saatmisel, võib põhjuseks olla üks järgmistest probleemidest:

- Faili suurus on liiga suur või pildi pikslimõõtmed ei ühildu printeriga. Sel juhul proovige vähendada pildifaili eraldusvõimet või mõõtmeid.
- Mõned objektide linkimise ja müügipunkti sisestamise (OPOS) printeri draiverid ei rakenda meetodit **PrintMemoryBitmap**, mida riistvarajaamad kasutavad logopiltide printimiseks. Sel juhul proovige lisada lipu **HardwareStation.Extension.config** fail oma pühendatud või jagatud riistvarajaama:

    `<add name="HardwareStation.UsePrintBitmapMethod" value="true"/>`

## <a name="design-a-receipt-format"></a>Kviitungi vormingu kujundamine

Kasutage vormi paigutust, et luua graafiliselt vormidokumendi paigutus. Lehel **Kviitungi vormingu kujundaja** on kolm jaotist: **Päis**, **Read** ja **Jalus**. Teatud tüüpi vormikavandid kasutavad kõigi kolme jaotise elemente, samas kui muud tüübid kasutavad ainult ühe või kahe jaotise elemente. Iga jaotise jaoks saadaolevate elementide vaatamiseks klõpsake lehekülje vasakul küljel oleva navigeerimispaani vastavat nuppu.

1. Avage **Jaemüük ja kaubandus** &gt; **Kanali häälestus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kviitungi vormingud**.
2. Valige leheküljel **Kviitungi vorming** vormikavand ja klõpsake seejärel valikut **Kujundaja**.
3. Commerce’i kujundaja hosti installimiseks klõpsake käsku **Käita**.
4. Ühe klõpsuga kujundaja installi käivitamiseks klõpsake Internet Explorer i akna alaossa ilmuval teavitusribal käsku **Ava**. (Teistes brauserites võib teavitusriba ilmuda kusagile mujale.) Installi edenemist näitab edenemisnäidik.
5. Pärast installi lõpulejõudmist sisestage kujundaja käivitamiseks oma Commerce’i kasutajanimi ja parool ning klõpsake suvandit **Logi sisse**.
6. Kui teie identimisteave on kinnitatud ja kujundaja käivitunud, saate hakata kviitungi vorminguid looma või olemasolevaid muutma.
7. Vormi elementide loomiseks valige jaotis **Päis**, **Read** või **Jalus** ja seejärel lohistage see element jaotisest tööruumi. Enamik elemente sisaldavad muutujaid, mis täidetakse automaatselt andmebaasist pärit andmetega. Muud elemendid, nagu **Tekst**, võimaldavad printida kohandatud teksti.

    > [!NOTE]
    > Iga jaotise hõlmatava ridade arvu määramiseks kohandage jaotise alumises paremas nurgas olevat arvu. Sektsiooni muutmise lihtsustamiseks suurendage sektsiooni kõrgust, lohistades sektsiooni allosas olevat suuruse muutmise riba. Jaotise kõrgus tööruumis ei mõjuta tegeliku kviitungi ridade arvu.

8. Pärast elemendi tööruumi lohistamist määrake atribuudid lehe alumise paani **Objektiteave** osa jaoks. Sisestage üks või mitu järgmist sätet.

    - **Joonda** – seadke välja joondus olekusse **Vasakul** või **Paremal**.
    - **Täitemärk** – määrake tühimärkide märk. Vaikimisi kasutatakse tühja ruumi, kuid te võite sisestada suvalise märgi.
    - **Eesliide** – sisestage väärtus, mis ilmub välja alguses. See säte rakendub ainult kavandi jaotisele **Read**.
    - **Märgid** – määrake muutujat sisaldava elemendi välja maksimaalne märkide arv. Kui väljal olev tekst on pikem kui määratud märkide arv, kärbitakse teksti väljale mahutamiseks.
    - **Muutuja** – see ruut märgitakse automaatselt, kui element sisaldab muutujat ja seda ei saa kohandada.
    - **Fondi tüüp** – seadke fondi laadiks **Tavaline** või **Paks**. Paksus kirjas tähed kasutavad kaks korda rohkem ruumi kui tavalises kirjas tähed. Seetõttu võidakse mõnda märki kärpida.
    - **Fondi suurus** – seadke fondi suuruseks **Tavaline** või **Suur**. Suured tähed on tavalistest kaks korda suuremad. Seega võib suurte tähtede kasutamine põhjustada kviitungil teksti kattumise.
    - **Kustuta** – klõpsake seda nuppu valitud osa eemaldamiseks vormi kavandist.

## <a name="assign-receipt-profiles"></a>Kviitungi profiilide määramine

Kviitungi profiilid määratakse riistvaraprofiili abil otse printeritele.

1. Avage riistvaraprofiil, klõpsates suvandit **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa profiilid** &gt; **Riistvaraprofiil**.
2. Valige printer ja seejärel määrake väljal **Kviitungi profiil** kassaaparaadis kasutatava kviitungi profiil.

> [!NOTE]
> Kui kasutate kahte printerit, saate üht printerit standardsete 40-veeruliste termoparberil kviitungite printimiseks kasutada. Teist printerit kasutatakse tavaliselt rohkem teavet nõudvate kogu lehe suuruste kviitungi tüüpide puhul. Selliste kviitungite hulka kuuluvad kliendi tellimuse kviitungid ja kliendiarved.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
