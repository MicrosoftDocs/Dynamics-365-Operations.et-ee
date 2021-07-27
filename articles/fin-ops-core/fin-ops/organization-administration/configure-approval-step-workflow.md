---
title: Töövoo kinnitusetappide konfigureerimine
description: See teema selgitab, kuidas konfigureerida kinnitusetapi atribuute.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 988340d9e5fc12c9329a587c7401fe039c8e5722
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350690"
---
# <a name="configure-approval-steps-in-a-workflow"></a>Töövoo kinnitusetappide konfigureerimine

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas konfigureerida kinnitusetapi atribuute.

Töövoo redaktoris kinnitamisetapi konfigureerimiseks paremklõpsake kinnitamisetappi ja klõpsake seejärel nuppu **Atribuudid**, et avada lehekülg **Atribuudid**. Seejärel kasutage järgmisi protseduure, et konfigureerida kinnitamisetapi atribuudid.

## <a name="name-the-step"></a>Sammule nime andmine
Sisestage kinnitusetapile nimi järgmisi juhiseid järgides.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Väljal **Nimi** sisestage kinnitusetapile kordumatu nimi.

## <a name="enter-a-subject-line-and-instructions"></a>Sisestage teemarida ja juhendid

Sisestage teemarida ja juhendid kasutajatele, kes on määratud kinnitusetapile. Näiteks kui konfigureerite kinnitusetappi ostutaotlustele, siis näeb kasutaja, kes on etapile määratud, teemarida ja juhiseid leheküljel **Ostutaotlused**. Teemarida kuvatakse lehe teateribal. Kasutaja saab seejärel juhiste nägemiseks klõpsata teateribal. Teemarea ja juhiste sisestamiseks järgige neid etappe.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Väljale **Tööüksuse teema** sisestage teemarida.
3. Teemarea isikupärastamiseks saate sisestada kohatäitjad. Kohatäitjad asendatakse teemarea kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks järgige neid etappe.

    1. Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.
    2. Klõpsake nuppu **Sisesta kohatäide**.
    3. Ilmuvas loendis valige sisestamiseks kohatäitja.
    4. Klõpsake nuppu **Sisesta**.

4. Teemarea tõlgete lisamiseks järgige neid etappe.

    1. Klõpsake valikut **Tõlked**.
    2. Ilmuval lehel klõpsake valikut **Lisa**.
    3. Ilmuvas loendis valige see keel, milles teksti sisestate.
    4. Väljale **Tõlgitud tekst** sisestage tekst.
    5. Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 3.
    6. Klõpsake valikut **Sule**.

5. Väljale **Tööüksuse juhised** sisestage juhised.
6. Juhiste isikupärastamiseks saate sisestada kohatäitjad. Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks järgige neid etappe.

    1. Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.
    2. Klõpsake nuppu **Sisesta kohatäide**.
    3. Ilmuvas loendis valige sisestamiseks kohatäitja.
    4. Klõpsake nuppu **Sisesta**.

7. Juhiste tõlgete lisamiseks järgige neid etappe.

    1. Klõpsake valikut **Tõlked**.
    2. Ilmuval lehel klõpsake valikut **Lisa**.
    3. Ilmuvas loendis valige see keel, milles teksti sisestate.
    4. Väljale **Tõlgitud tekst** sisestage tekst.
    5. Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 6.
    6. Klõpsake valikut **Sule**.

## <a name="assign-the-approval-step"></a>Määrake kinnitussamm

Järgige neid etappe, et määrata, kellele kinnitusetapp tuleb määrata.

1. Vasakul paanil klõpsake nuppu **Määramine**.
2. Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 3 etappi.

    <table>
    <thead>
    <tr>
    <th>Suvand</th>
    <th>Kasutajad, kellele kinnitamisetapp on määratud</th>
    <th>Täiendavad etapid</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Osaleja</td>
    <td>Kasutajad, kes on määratud teatud grupile või rollile</td>
    <td>
    <ol>
    <li>Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele etapp määrata.</li>
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele etapp määrata.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarhia</td>
    <td>Kasutaja spetsiifilises organisatsioonilises hierarhias</td>
    <td>
    <ol>
    <li>Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele etapp määrata.</li>
    <li>Süsteem peab hierarhiast tooma kasutajanimede vahemiku. Need nimed tähistavad kasutajaid, kellele etappi saab määrata. Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob. <ol>
    <li>Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</li>
    <li>Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>. Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</li>
    </ol>
    </li>
    <li>Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb etapp määrata. <ul>
    <li><strong>Määra kõikidele toodud kasutajatele</strong> – etapp määratakse kõikidele kasutajatele vahemikus.</li>
    <li><strong>Määra ainult viimati toodud kasutajale</strong> – etapp määratakse ainult viimasele kasutajale vahemikus.</li>
    <li><strong>Välista kasutajatelt järgmise tingimusega</strong> – etappi ei määrata vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele. Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Töövoo kasutaja</td>
    <td>Kasutajad praeguses töövoos</td>
    <td>
    <ul>
    <li>Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Kasutaja</td>
    <td>Kindlad kasutajad</td>
    <td>
    <ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>Loend <strong>Saadaolevad kasutajad</strong> hõlmab süsteemi kõiki kasutajaid. Valige kasutajad, kellele etapp määrata, ja liigutage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal reageerida või vastata dokumentidele, mis jõuavad kinnitusetappi. Tehke üks järgmistest valikutest:

    - **Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega vastata. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    - **Päevad** – sisestage päevade arv, kui kaua on kasutajal aega vastata. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    - **Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega vastata.
    - **Kuud** – valige päev ja nädal, mis ajaks kasutaja peab vastama Näiteks võite soovida kasutajalt vastust saada kuu kolmanda nädala reedeks.
    - **Aastad** – valige päev, nädal ja kuu, mis ajaks kasutaja peab vastama Näiteks võite soovida kasutajalt vastust detsembri kolmanda nädala reedeks.

    Kui kasutaja ei reageeri dokumendile määratud aja jooksul, siis on dokument hilinenud.. Hilinenud dokumenti laiendatakse nende valikute põhjal, mille valite lehe alal **Laiendus**.

4. Kui määrate kinnitusetapi mitmele kasutajale või kasutajate grupile, valige vahekaardil **Lõpetamispoliitika** üks järgmistest suvanditest.

    - **Üksikkinnitaja** – dokumendile rakenduva toimingu määrab esimene isik, kes vastab. Näiteks Sam on edastanud kuluaruande summale 15 000 USA dollarit. Kuluaruanne on praegu määratud Suele, Jole ja Billile. Kui Sue reageerib dokumendile esimesena, rakendatakse tema võetud meetmeid dokumendil. Kui Sue lükkab dokumendi tagasi, lükatakse dokument tagasi ja saadetakse uuesti Samile. Kui Sue kinnitab dokumendi, saadetakse see Annile kinnitamiseks.

        ![Töövoog, millel on kinnitamisprotsess.](./media/workflow_multipleusersinstep.gif)

    - **Enamik kinnitajaid** – tegevus, mis rakendatakse dokumendile, määratakse siis, kui enamik kinnitajaid vastab. Näiteks Sam on edastanud kuluaruande summale 15 000 USA dollarit. Kuluaruanne on praegu määratud Suele, Jole ja Billile. Kui Sue ja Jo kinnitavad dokumendi esimesena, siis rakendatakse nende võetud meetmeid dokumendil.

        - Kui Sue kinnitab dokumendi, kuid Jo lükkab selle tagasi, lükatakse dokument tagasi ja saadetakse tagasi Samile.
        - Kui Sue ja Jo mõlemad kinnitavad dokumendi, saadetakse see Annile kinnitamiseks.

    - **Kinnitajate protsent** – tegevus, mis rakendatakse dokumendile, määratakse siis, kui teatud protsent kinnitajaid vastavad. Näiteks Sam on edastanud kuluaruande summale 15 000 USA dollarit. Kuluaruanne on praegu määratud Suele, Jole ja Billile ja te sisestasite protsendiks **50**. Kui Sue ja Jo kinnitavad dokumendi esimesena, siis rakendatakse nende tehtud toiming dokumendile, kuna nad täidavad kinnitajate 50-protsendilist nõuet.

        - Kui Sue kinnitab dokumendi, kuid Jo lükkab selle tagasi, lükatakse dokument tagasi ja saadetakse tagasi Samile.
        - Kui Sue ja Jo mõlemad kinnitavad dokumendi, saadetakse see Annile kinnitamiseks.

    - **Kõik kinnitajad** – kõik kinnitajad peavad dokumendi kinnitama. Vastasel juhul ei saa töövoog jätkuda. Näiteks Sam on edastanud kuluaruande summale 15 000 USA dollarit. Kuluaruanne on praegu määratud Suele, Jole ja Billile. Kui Sue ja Jo kinnitavad dokumendi, kuid Bill lükkab selle tagasi, lükatakse dokument tagasi ja saadetakse tagasi Samile. Kui Sue, Jo ja Bill kõik kinnitavad dokumendi, saadetakse see Annile kinnitamiseks.

## <a name="specify-when-the-approval-step-is-required"></a>Määrake, millal on kinnitamisetapp vajalik

Saate määrata, millal kinnitamisetapp on vajalik. Kinnitamisetapp võib alati olla vajalik või see võib olla vajalik ainult juhul, kui teatud tingimused on täidetud.

### <a name="the-approval-step-is-always-required"></a>Kinnitamisetapp on alati vajalik

Järgige neid etappe, kui kinnitusetapp on alati vajalik.

1. Vasakul paanil klõpsake nuppu **Tingimus**.
2. Valige suvand **Käivita see samm alati**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Kinnitussamm on vajalik teatud tingimustes

Teie konfigureeritav kinnitusetapp on vajalik ainult teatud tingimustel. Näiteks kui konfigureerite kinnitusetappi ostutaotluse töövoole, võite soovida, et kinnitusetapp esineb ainult siis, kui ostutaotluse summa on rohkem kui 10 000 USA dollarit. Järgige neid etappe, et määrata, millal kinnitamisetapp on vajalik.

1. Vasakul paanil klõpsake nuppu **Tingimus**.
2. Valige suvand **Käivita see samm üksnes siis, kui järgmine tingimus on täidetud**.
3. Sisestage tingimus.
4. Sisestage täiendavad vajalikud tingimused.
5. Kinnitamaks, et teie sisestatud tingimused on õigesti konfigureeritud, järgige neid etappe.

    1. Klõpsake nuppu **Test**.
    2. Lehel **Testi töövoo tingimus** alas **Kontrolli tingimust** valige kirje.
    3. Klõpsake nuppu **Test**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.
    4. Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Määrake, mis juhtub, kui dokument on hilinenud

Kui kasutaja ei reageeri dokumendile määratud aja jooksul, siis on dokument hilinenud. Hilinenud dokumenti saab laiendada või automaatselt kinnitamiseks teisele kasutajale määrata. Järgige neid etappe dokumendi laiendamiseks, kui see on hilinenud.

1. Vasakul paanil klõpsake valikut **Laiendus**.
2. Laiendustee loomiseks märkige ruut **Laiendustee kasutamine**. Süsteem määrab dokumendi automaatselt laiendamistee nimekirjas olevatele kasutajatele. Näiteks tähistab järgmine tabel laiendusteed.

    | Seeria | Laiendustee      |
    |----------|----------------------|
    | 1        | Määra isikule: Donna     |
    | 2        | Määra isikule: Erin      |
    | 3        | Lõpptegevus: lükka tagasi |

    Sellise näite korral määrab süsteem hilinenud dokumendi Donnale. Kui Donna ei vasta määratud aja jooksul, siis määrab süsteem dokumendi Erinile. Kui Erin ei vasta määratud aja jooksul, siis lükkab süsteem dokumendi tagasi.

3. Laiendustee kasutajale lisamiseks klõpsake valikut **Laienduse lisamine**. Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 4 etappi.

    <table>
    <thead>
    <tr>
    <th>Suvand</th>
    <th>Kasutajad, kellele dokument on laiendatud</th>
    <th>Täiendavad etapid</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarhia</td>
    <td>Kasutaja spetsiifilises organisatsioonilises hierarhias</td>
    <td>
    <ol>
    <li>Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele dokument laiendada.</li>
    <li>Süsteem peab hierarhiast tooma kasutajanimede vahemiku. Need nimed tähistavad kasutajaid, kellele dokumenti saab laiendada. Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob. <ol>
    <li>Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</li>
    <li>Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>. Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</li>
    </ol>
    </li>
    <li>Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb dokument määrata. <ul>
    <li><strong>Määra kõikidele toodud kasutajatele</strong> – dokument laiendatakse kõikidele kasutajatele vahemikus.</li>
    <li><strong>Määra ainult viimati toodud kasutajale</strong> – dokumenti laiendatakse ainult viimasele kasutajale vahemikus.</li>
    <li><strong>Välista kasutajatelt järgmise tingimusega</strong> – dokumenti ei laiendata vahemiku ühelegi kasutajale, kes vastavad teatud tingimusele. Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Töövoo kasutaja</td>
    <td>Kasutajad praeguses töövoos</td>
    <td>
    <ul>
    <li>Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Kasutaja</td>
    <td>Kindlad kasutajad</td>
    <td>
    <ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid. Valige kasutajad, kellele dokumenti laiendada ja liigutage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal dokumentidele reageerida või vastata. Tehke üks järgmistest valikutest:

    - **Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega vastata. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    - **Päevad** – sisestage päevade arv, kui kaua on kasutajal aega vastata. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    - **Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega vastata.
    - **Kuud** – valige päev ja nädal, mis ajaks kasutaja peab vastama Näiteks võite soovida kasutajalt vastust saada kuu kolmanda nädala reedeks.
    - **Aastad** – valige päev, nädal ja kuu, mis ajaks kasutaja peab vastama Näiteks võite soovida kasutajalt vastust detsembri kolmanda nädala reedeks.

5. Korrake etappe 3 kuni 4 iga kasutaja puhul, kes tuleb laiendusteele lisada. Saate muuta kasutajate järjekorda.
6. Kui kasutajad laiendusteel ei reageeri määratud aja jooksul, siis reageerib süsteem dokumendile automaatselt. Süsteemi tegevuse määramiseks valige rida **Tegevus** ja seejärel valige tegevus vahekaardi **Lõpptegevus**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]