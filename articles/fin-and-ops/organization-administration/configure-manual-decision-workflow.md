---
title: "Töövoos käsitsi otsuse konfigureerimine"
description: "See teema selgitab, kuidas konfigureerida käsitsi otsuse atribuute."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6ea8b060741ea94af16861d5bb52894a577e5521
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="configure-a-manual-decision-in-a-workflow"></a>Töövoos käsitsi otsuse konfigureerimine

[!include[banner](../includes/banner.md)]


See teema selgitab, kuidas konfigureerida käsitsi otsuse atribuute.

Töövoo redaktoris käsitsi otsuse loomiseks paremklõpsake käsitsi otsust ja seejärel klõpsake suvandit **Atribuudid**, et avada lehekülg **Atribuudid**. Seejärel kasutage järgmisi protseduure, et konfigureerida käsitsi otsuse atribuudid.

## <a name="name-the-decision"></a>Andke otsusele nimi
Käsitsi otsusele nime sisestamiseks tehke järgmist.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Väljal **Nimi** sisestage käsitsi üksuse jaoks kordumatu nimi.

## <a name="enter-a-subject-line-and-instructions"></a>Sisestage teemarida ja juhendid
Sisestage teemarida ja juhendid kasutajatele, kes on määratud käsitsi otsusele. Näiteks kui konfigureerite ostutaotluste otsust, näeb kasutaja, kes on otsust määratud, teemarida ja juhiseid lehel **Ostutaotlused**. Teemarida kuvatakse lehe teateribal. Kasutaja saab seejärel juhiste vaatamiseks klõpsata teateriba. Teemarea ja juhiste sisestamiseks järgige neid etappe.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Sisestage teemarida vahekaardi **Juhised** väljale **Tööüksuse teema**.
3.  Teemarea isikupärastamiseks saate sisestada kohatäitjad. Kohatäitjad asendatakse teemarea kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks järgige neid etappe.
    1.  Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.
    2.  Klõpsake nuppu **Sisesta kohatäide**.
    3.  Ilmuvas loendis valige sisestamiseks kohatäitja.
    4.  Klõpsake nuppu **Sisesta**.

4.  Teemarea tõlgete lisamiseks järgige neid etappe.
    1.  Klõpsake valikut **Tõlked**.
    2.  Ilmuval lehel klõpsake valikut **Lisa**.
    3.  Ilmuvas loendis valige see keel, milles teksti sisestate.
    4.  Väljale **Tõlgitud tekst** sisestage tekst.
    5.  Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 3.
    6.  Klõpsake valikut **Sule**.

5.  Väljale **Tööüksuse juhised** sisestage juhised.
6.  Juhiste isikupärastamiseks saate sisestada kohatäitjad. Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks järgige neid etappe.
    1.  Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.
    2.  Klõpsake nuppu **Sisesta kohatäide**.
    3.  Ilmuvas loendis valige sisestamiseks kohatäitja.
    4.  Klõpsake nuppu **Sisesta**.

7.  Juhiste tõlgete lisamiseks järgige neid etappe.
    1.  Klõpsake valikut **Tõlked**.
    2.  Ilmuval lehel klõpsake valikut **Lisa**.
    3.  Ilmuvas loendis valige see keel, milles teksti sisestate.
    4.  Väljale **Tõlgitud tekst** sisestage tekst.
    5.  Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 6.
    6.  Klõpsake valikut **Sule**.

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Määrake otsuse võimalikud tulemused
Tavaliselt määratakse dokument otsustajale juhul, kui otsustajale esitatakse küsimus. Küsimuse vastus on tavaliselt **Jah** või **Ei** või **Tõene** või **Väär**. Käsitsi otsuse võimalike tulemuste määramiseks tehke järgmist.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Sisestage vahekaardi **Tulemused** väljale **Tulemus 1** tulemuse nimi või suvand.
3.  Tulemuse tõlgete lisamiseks järgige neid etappe.
    1.  Klõpsake valikut **Tõlked**.
    2.  Ilmuval lehel klõpsake valikut **Lisa**.
    3.  Ilmuvas loendis valige see keel, milles teksti sisestate.
    4.  Väljale **Tõlgitud tekst** sisestage tekst.
    5.  Klõpsake valikut **Sule**.

4.  Sisestage väljale väljale **Tulemus 2** tulemuse nimi või suvand.
5.  Tulemuse tõlgete lisamiseks järgige neid etappe.
    1.  Klõpsake valikut **Tõlked**.
    2.  Ilmuval lehel klõpsake valikut **Lisa**.
    3.  Ilmuvas loendis valige see keel, milles teksti sisestate.
    4.  Väljale **Tõlgitud tekst** sisestage tekst.
    5.  Klõpsake valikut **Sule**.

## <a name="specify-when-notifications-are-sent"></a>Määrake, millal teatisi saadetakse
Saate saata inimestele teatisi, kui otsus langetatakse, delegeeritakse või eskaleeritakse. Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.

1.  Vasakul paanil klõpsake suvandit **Teatised**.
2.  Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.
    -   **\[1. valik\]** – määratud kasutaja on valinud suvandi **\[1. valik\]**.
    -   **\[2. valik\]** – määratud kasutaja on valinud suvandi **\[2. valik\]**.
    -   **Delegeerimine** – määratud kasutaja määras otsuse muule kasutajale.
    -   **Eskaleerimine** – määratud kasutaja ei teinud otsust määratud aja jooksul.

3.  Valige 2. etapis valitud sündmuse rida.
4.  Sisestage teatise tekst vahekaardil **Teatise tekst** olevale tekstiväljale.
5.  Teatise isikupärastamiseks võite sisestada kohatäitjad. Kohatäitjad asendatakse teatise kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks järgige neid etappe.
    1.  Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.
    2.  Klõpsake nuppu **Sisesta kohatäide**.
    3.  Ilmuvas loendis valige sisestamiseks kohatäitja.
    4.  Klõpsake nuppu **Sisesta**.

6.  Teatise tõlgete lisamiseks järgige neid etappe.
    1.  Klõpsake valikut **Tõlked**.
    2.  Ilmuval lehel klõpsake valikut **Lisa**.
    3.  Ilmuvas loendis valige see keel, milles teksti sisestate.
    4.  Väljale **Tõlgitud tekst** sisestage tekst.
    5.  Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 5.
    6.  Klõpsake valikut **Sule**.

7.  Määrake vahekaardil **Adressaat**, kellele teatised saadetakse. Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 8. etapiga.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Suvand</th>
    <th>Teatise adressaadid</th>
    <th>Täiendavad etapid</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Osaleja</td>
    <td>Kasutajad, kes on määratud teatud grupile või rollile</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele teatisi saata.</li>
    <li>Loendis <strong>Osaleja</strong> valige grupp, millele teatisi saata.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Töövoo kasutaja</td>
    <td>Kasutajad praeguses töövoos</td>
    <td><ul>
    <li>Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Kasutaja</td>
    <td>Kindlad Microsoft Dynamics 365 for Finance and Operationsi kasutajad</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid. Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.

## <a name="assign-a-decision"></a>Otsuse määramine
Järgige neid etappe, et valida, kellele käsitsi otsus määratakse.

1.  Vasakul paanil klõpsake nuppu **Määramine**.
2.  Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 3 etappi.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Suvand</th>
    <th>Kasutajad, kellele otsus on määratud</th>
    <th>Täiendavad etapid</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Osaleja</td>
    <td>Kasutajad, kes on määratud teatud grupile või rollile</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele otsus määrata.</li>
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele otsus määrata.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarhia</td>
    <td>Kasutaja spetsiifilises organisatsioonilises hierarhias</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele otsus määrata.</li>
    <li>Süsteem peab hierarhiast tooma kasutajanimede vahemiku. Need nimed tähistavad kasutajaid, kellele saab otsuse määrata. Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob. <ol>
    <li>Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</li>
    <li>Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>. Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</li>
    </ol></li>
    <li>Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb otsus määrata. <ul>
    <li><strong>Määra kõikidele toodud kasutajatele</strong> – otsus määratakse kõikidele kasutajatele vahemikus.</li>
    <li><strong>Määra ainult viimati toodud kasutajale</strong> – otsus määratakse ainult viimasele kasutajale vahemikus.</li>
    <li><strong>Välista kasutajatelt järgmise tingimusega</strong> – otsust ei määrata vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele. Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Töövoo kasutaja</td>
    <td>Kasutajad praeguses töövoos</td>
    <td><ul>
    <li>Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Kasutaja</td>
    <td>Konkreetsed Finance and Operationsi kasutajad</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid. Valige kasutajad, kellele otsus määrata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Järjekord</td>
    <td>Tööüksuste järjekord</td>
    <td><ol>
    <li>Pärast suvandi <strong>Järjekord</strong> valimist klõpsake vahekaarti <strong>Järjekorral põhinev</strong>.</li>
    <li>Otsuse konkreetsesse järjekorda määramiseks tehke järgmist. <ol>
    <li>Valige loendis <strong>Järjekorra tüüp</strong> suvand <strong>Tööüksuste järjekord</strong>.</li>
    <li>Loendis <strong>Järjekorra nimi</strong> valige järjekord.</li>
    </ol></li>
    <li>Kui konkreetne tingimus peab määrama, millisesse järjekorda otsus määratakse, tehke järgmist. <ol>
    <li>Valige loendis <strong>Järjekorra tüüp</strong> suvand <strong>Tinglike tööüksuste järjekord</strong>.</li>
    <li>Loendis <strong>Järjekorra nimi</strong> valige suvand <strong>Tinglik järjekord</strong>.</li>
    </ol></li>
    </ol>
    <strong>Märkus.</strong> Suvandit kasutatakse ainult mõningate töövoogude puhul, nagu juhtumihaldus.</td>
    </tr>
    </tbody>
    </table>

3.  Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal otsuse tegemiseks. Tehke üks järgmistest valikutest:
    -   **Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega otsuse tegemiseks. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Päevad** – sisestage päevade arv, kui kaua on kasutajal aega otsuse tegemiseks. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega otsuse tegemiseks.
    -   **Kuud** – valige päev ja nädal, mil kasutaja peab otsuse tegema. Näiteks soovite võib-olla, et kasutaja teeks otsuse kuu kolmanda nädala reedeks.
    -   **Aastad** – valige päev, nädal ja kuu, mil kasutaja peab otsuse tegema. Näiteks soovite võib-olla, et kasutaja teeks otsuse detsembri kolmanda nädala reedeks.

    Kui kasutaja ei tee otsust määratud aja jooksul, on otsuse tähtaeg ületatud. Hilinenud otsust eskaleeritakse nende valikute põhjal, mille valite lehe alal **Laiendus**.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Määrake, mis juhtub tähtaja ületanud otsusega
Kui kasutaja ei tee otsust määratud aja jooksul, on otsuse tähtaeg ületatud. Hilinenud otsuse saab eskaleerida või automaatselt muule kasutajale määrata. Järgige neid etappe otsuse eskaleerimiseks, kui see on hilinenud.

1.  Vasakul paanil klõpsake valikut **Laiendus**.
2.  Laiendustee loomiseks märkige ruut **Laiendustee kasutamine**. Süsteem määrab otsuse automaatselt laiendamistee nimekirjas olevatele kasutajatele. Näiteks tähistab järgmine tabel laiendusteed.
    | Seeria | Laiendustee            |
    |----------|----------------------------|
    | 1        | Määra isikule: Donna           |
    | 2        | Määra isikule: Erin            |
    | 3        | Lõplik tegevus: \[1. valik\] |

    Sellise näite korral määrab süsteem hilinenud otsuse Donnale. Kui Donna ei tee otsust selleks ettenähtud aja jooksul, määrab süsteem otsuse Erinile. Kui Erin ei tee otsust selleks ettenähtud aja jooksul, valib süsteem otsuseks suvandi **\[1. valik\]**.
3.  Laiendustee kasutajale lisamiseks klõpsake valikut **Laienduse lisamine**. Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 4. etapiga.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Suvand</th>
    <th>Kasutajad, kellele otsus eskaleeritakse</th>
    <th>Täiendavad etapid</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarhia</td>
    <td>Kasutaja spetsiifilises organisatsioonilises hierarhias</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele otsus eskaleerida.</li>
    <li>Süsteem peab hierarhiast tooma kasutajanimede vahemiku. Need nimed tähistavad kasutajaid, kellele saab otsust eskaleerida. Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob. <ol>
    <li>Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</li>
    <li>Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>. Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</li>
    </ol></li>
    <li>Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb otsus eskaleerida. <ul>
    <li><strong>Määra kõikidele toodud kasutajatele</strong> – otsus eskaleeritakse kõikidele kasutajatele vahemikus.</li>
    <li><strong>Määra ainult viimati toodud kasutajale</strong> – otsus eskaleeritakse ainult viimasele kasutajale vahemikus.</li>
    <li><strong>Välista kasutajatelt järgmise tingimusega</strong> – otsust ei eskaleerita vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele. Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Töövoo kasutaja</td>
    <td>Kasutajad praeguses töövoos</td>
    <td><ul>
    <li>Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Kasutaja</td>
    <td>Konkreetsed Finance and Operationsi kasutajad</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid. Valige kasutajad, kellele otsust eskaleerida, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal otsuse tegemiseks. Tehke üks järgmistest valikutest:
    -   **Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega otsuse tegemiseks. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Päevad** – sisestage päevade arv, kui kaua on kasutajal aega otsuse tegemiseks. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega otsuse tegemiseks.
    -   **Kuud** – valige päev ja nädal, mil kasutaja peab otsuse tegema. Näiteks soovite võib-olla, et kasutaja teeks otsuse kuu kolmanda nädala reedeks.
    -   **Aastad** – valige päev, nädal ja kuu, mil kasutaja peab otsuse tegema. Näiteks soovite võib-olla, et kasutaja teeks otsuse detsembri kolmanda nädala reedeks.

5.  Korrake etappe 3 kuni 4 iga kasutaja puhul, kes tuleb laiendusteele lisada. Saate muuta kasutajate järjekorda.
6.  Kui kasutajad eskaleerimisteel ei tee otsust määratud aja jooksul, langetab otsuse süsteem. Süsteemi valitava suvandi määramiseks valige rida **Tegevus** ja seejärel valige suvand vahekaardi **Lõpptegevus**.

## <a name="set-a-time-limit"></a>Ajalimiidi seadmine
Kui otsus tuleb teha teatud ajaks, tehke järgmist. **Märkus.** Selle protseduuri käigus valitud suvandid alistavad lehe jaotistes **Määramine** ja **Eskaleerimine** valitud suvandid.

1.  Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
2.  Märkige ruut **Määra töövoo elemendi jaoks ajalimiit**.
3.  Määrake väljal **Kestus**, mis ajaks peab otsus olema tehtud. Tehke üks järgmistest valikutest:
    -   **Tunnid** – sisestage tundide arv. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Päevad** – sisestage päevade arv. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Nädalad** – sisestage nädalate arv.
    -   **Kuud** – valige päev ja nädal, mis ajaks kasutaja peab otsuse tegema. Näiteks soovite võib-olla, et otsus oleks tehtud kuu kolmanda nädala reedeks.
    -   **Aastad** – valige päev, nädal ja kuu, mis ajaks kasutaja peab otsuse tegema. Näiteks soovite võib-olla, et otsus oleks tehtud detsembri kolmanda nädala reedeks.

4.  Ajalimiidi ületamisel langetab otsuse süsteem. Loendist **Tegevus** valige suvand, mille süsteem peaks valima.





