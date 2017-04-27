---
title: Kviitungimallid ja printimine
description: "See artikkel kirjeldab, kuidas vormikavandeid luua ja muuta, et kontrollida kviitungite, arvete ja muude dokumentide printimise viisi. Microsoft Dynamics 365 for Operationsi moodulis Jaemüük on vormi kavandi kujundaja funktsioon, millega saab hõlpsalt ja graafiliselt luua ja muuta mitmesuguseid vormi kavandeid."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabaacbc7187b38a1745c2139a9eb7760f2be987
ms.lasthandoff: 03/31/2017


---

# <a name="receipt-templates-and-printing"></a>Kviitungimallid ja printimine

[!include[banner](includes/banner.md)]


See artikkel kirjeldab, kuidas vormikavandeid luua ja muuta, et kontrollida kviitungite, arvete ja muude dokumentide printimise viisi. Microsoft Dynamics 365 for Operationsi moodulis Jaemüük on vormi kavandi kujundaja funktsioon, millega saab hõlpsalt ja graafiliselt luua ja muuta mitmesuguseid vormi kavandeid.

**Oluline!** Peate seadistama vormipaigutused ja kviitungiprofiilid, et printida kviitungid ja muud dokumendid Retail Modern POS-i ja pilvekassa kaudu Kviitungiprofiilile saab lisada mitu vormipaigutust. Seejärel saate riistvara profiili muutes kviitungi profiilile printeri määrata.

## <a name="set-up-a-receipt-format"></a>Kviitungivormingu seadistamine
1.  Klõpsake valikuid **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kviitungi vormingud**.
2.  Uue vormikavandi loomiseks või olemasolevate vormikavandite hulgast sobiva valimiseks klõpsake lehel **Kviitungi vorming** nuppu **Uus**.
3.  Sisestage väljale **Kviitungi vorming** vormikavandi identifikaator ja valige seejärel kviitungi tüüp, mille jaoks seda kavandit kasutatakse. Kviitungile saate ka kirjelduse ja lühikese nime väljal **Pealkiri** sisestada.
4.  Prindikäitumise määratlemiseks valige suvand kiirkaardilt **Üldine**.
    -   **Prindi alati** – kviitung prinditakse automaatselt nagu ette nähtud.
    -   **Ära prindi** – kviitungit ei prindita.
    -   **Küsi kasutajalt** – kasutajalt küsitakse kviitungi printimise kohta.
    -   **Nagu on nõutud** – seda valikut kasutatakse ainult ostukviitungite puhul. Kui see suvand on valitud, saab kasutaja vajadusel ostukviitungi leheküljelt **Muuda** printida.

## <a name="design-a-receipt-format"></a>Kviitungi vormingu kujundamine
Kasutage vormi paigutust, et luua graafiliselt vormidokumendi paigutus. Lehel **Kviitungi vormingu kujundaja** on kolm jaotist: **Päis**, **Read** ja **Jalus**. Teatud tüüpi vormikavandid kasutavad kõigi kolme jaotise elemente, samas kui muud tüübid kasutavad ainult ühe või kahe jaotise elemente. Iga jaotise jaoks saadaolevate elementide vaatamiseks klõpsake lehekülje vasakul küljel oleva navigeerimispaani vastavat nuppu.

1.  Klõpsake valikuid **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kviitungi vormingud**.
2.  Valige leheküljel **Kviitungi vorming** vormikavand ja klõpsake seejärel valikut **Kujundaja**.
3.  Retaili kujundaja hosti installimiseks klõpsake käsku **Käita**.
4.  Ühe klõpsuga kujundaja installi käitamiseks klõpsake Internet Exploreri akna alumisse ossa ilmuval teavitusribal käsku **Ava**. (Teistes brauserites võib teavitusriba ilmuda kusagile mujale.) Installi edenemist näitab edenemisnäidik.
5.  Pärast installi lõpetamist sisestage kujundaja käivitamiseks oma Microsoft Dynamics 365 for Operationsi kasutajanimi ja parool ning klõpsake valikut **Sisselogimine**.
6.  Kui teie identimisteave on kinnitatud ja kujundaja käivitunud, saate hakata kviitungi vorminguid looma või olemasolevaid muutma.
7.  Vormi elementide loomiseks valige jaotis **Päis**, **Read** või **Jalus** ja seejärel lohistage see element jaotisest tööruumi. Enamik elemente sisaldavad muutujaid, mis täidetakse automaatselt andmebaasist pärit andmetega. Muud elemendid, nagu **Tekst**, võimaldavad printida kohandatud teksti. **Märkus.** Iga jaotise hõlmatava ridade arvu määramiseks kohandage jaotise alumises paremas nurgas olevat arvu. Sektsiooni muutmise lihtsustamiseks suurendage sektsiooni kõrgust, lohistades sektsiooni allosas olevat suuruse muutmise riba. Jaotise kõrgus tööruumis ei mõjuta tegeliku kviitungi ridade arvu.
8.  Pärast elemendi tööruumi lohistamist määrake atribuudid lehe alumise paani **Objektiteave **osa jaoks. Sisestage üks või mitu järgmist sätet.
    -   **Joonda** – seadke välja joondus olekusse **Vasakul** või **Paremal**.
    -   **Täitemärk** – määrake tühimärkide märk. Vaikimisi kasutatakse tühja ruumi, kuid te võite sisestada suvalise märgi.
    -   **Eesliide** – sisestage väärtus, mis ilmub välja alguses. See säte rakendub ainult kavandi jaotisele **Read**.
    -   **Märgid** – määrake muutujat sisaldava elemendi välja maksimaalne märkide arv. Kui väljal olev tekst on pikem kui määratud märkide arv, kärbitakse teksti väljale mahutamiseks.
    -   **Muutuja** – see ruut märgitakse automaatselt, kui element sisaldab muutujat ja seda ei saa kohandada.
    -   **Fondi tüüp** – seadke fondi laadiks **Tavaline** või **Paks**. Paksus kirjas tähed kasutavad kaks korda rohkem ruumi kui tavalises kirjas tähed. Seetõttu võidakse mõnda märki kärpida.
    -   **Kustuta** – klõpsake seda nuppu valitud osa eemaldamiseks vormi kavandist.

## <a name="assign-receipt-profiles"></a>Kviitungi profiilide määramine
Kviitungi profiilid määratakse riistvaraprofiili abil otse printeritele.

1.  Riistvaraprofiili avamiseks järgige seda rada: **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa profiilid** &gt; **Riistvaraprofiil**.
2.  Valige printer ja seejärel määrake väljal **Kviitungi profiil **kassaaparaadis kasutatava kviitungi profiil.

**Märkus.** Kui kasutate kahte printerit, saate üht printerit standardsete 40-veeruliste termoparberil kviitungite printimiseks kasutada. Teist printerit kasutatakse tavaliselt rohkem teavet nõudvate kogu lehe suuruste kviitungi tüüpide puhul. Selliste kviitungite hulka kuuluvad kliendi tellimuse kviitungid ja kliendiarved.




