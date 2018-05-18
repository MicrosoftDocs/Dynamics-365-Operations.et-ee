---
title: "Töövoos käsitsi ülesande konfigureerimine"
description: "See teema selgitab, kuidas konfigureerida käsitsi ülesande atribuute."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 09bd86ff7a4aa8ae64cfa4a38fba643f9117d6eb
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-manual-task-in-a-workflow"></a>Töövoos käsitsi ülesande konfigureerimine

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas konfigureerida käsitsi ülesande atribuute.

Töövoo redaktoris käsitsi ülesande loomiseks paremklõpsake ülesannet ja seejärel klõpsake suvandit **Atribuudid**, et avada lehekülg **Atribuudid**. Seejärel kasutage järgmisi protseduure, et konfigureerida käsitsi ülesande atribuudid.

## <a name="name-the-task"></a>Ülesandele nime andmine
Sisestage käsitsi ülesandele nimi järgmisi juhiseid järgides.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Sisestage ülesande kordumatu nimi väljale **Nimi**.

## <a name="enter-a-subject-line-and-instructions"></a>Sisestage teemarida ja juhendid
Sisestage teemarida ja juhendid sellele ülesandele määratud kasutajate jaoks. Näiteks kui konfigureerite ostutaotluste ülesannet, näeb kasutaja, kes on ülesandele määratud, teemarida ja juhiseid leheküljel **Ostutaotlused**. Teemarida kuvatakse lehe teateribal. Kasutaja saab seejärel juhiste vaatamiseks klõpsata teateriba. Teemarea ja juhiste sisestamiseks järgige neid etappe.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Väljale **Tööüksuse teema** sisestage teemarida.
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

## <a name="assign-the-task"></a>Ülesande määramine
Järgige neid etappe, et valida, kellele käsitsi ülesanne määratakse.

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
    <th>Kasutajad, kellele ülesanne on määratud</th>
    <th>Täiendavad etapid</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Osaleja</td>
    <td>Kasutajad, kes on määratud teatud grupile või rollile</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele ülesanne määrata.</li>
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele ülesanne määrata.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarhia</td>
    <td>Kasutaja spetsiifilises organisatsioonilises hierarhias</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele ülesanne määrata.</li>
    <li>Süsteem peab hierarhiast tooma kasutajanimede vahemiku. Need nimed tähistavad kasutajaid, kellele saab ülesande määrata. Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob. <ol>
    <li>Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</li>
    <li>Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>. Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</li>
    </ol></li>
    <li>Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb ülesanne määrata. <ul>
    <li><strong>Määra kõikidele toodud kasutajatele</strong> – ülesanne määratakse kõikidele kasutajatele vahemikus.</li>
    <li><strong>Määra ainult viimati toodud kasutajale</strong> – ülesanne määratakse ainult viimasele kasutajale vahemikus.</li>
    <li><strong>Välista kasutajatelt järgmise tingimusega</strong> – ülesannet ei määrata vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele. Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</li>
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
    <td>Kindlad Microsoft Dynamics 365 for Finance and Operationsi kasutajad</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid. Valige kasutajad, kellele ülesanne määrata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Järjekord</td>
    <td>Tööüksuste järjekord</td>
    <td><ol>
    <li>Pärast suvandi <strong>Järjekord</strong> valimist klõpsake vahekaarti <strong>Järjekorral põhinev</strong>.</li>
    <li>Ülesande konkreetsesse järjekorda määramiseks tehke järgmist. <ol>
    <li>Valige loendis <strong>Järjekorra tüüp</strong> suvand <strong>Tööüksuste järjekord</strong>.</li>
    <li>Loendis <strong>Järjekorra nimi</strong> valige järjekord.</li>
    </ol></li>
    <li>Kui konkreetne tingimus peab määrama, millisesse järjekorda ülesanne määratakse, tehke järgmist. <ol>
    <li>Valige loendis <strong>Järjekorra tüüp</strong> suvand <strong>Tinglike tööüksuste järjekord</strong>.</li>
    <li>Loendis <strong>Järjekorra nimi</strong> valige suvand <strong>Tinglik järjekord</strong>.</li>
    </ol></li>
    </ol>
    <strong>Märkus.</strong> Suvandit kasutatakse ainult mõningate töövoogude puhul, nagu juhtumihaldus.</td>
    </tr>
    </tbody>
    </table>

3.  Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal ülesande lõpuleviimiseks. Tehke üks järgmistest valikutest:
    -   **Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Päevad** – sisestage päevade arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks.
    -   **Kuud** – valige päev ja nädal, mil kasutaja peab ülesande lõpule viima. Näiteks soovite võib-olla, et kasutaja täidaks ülesande kuu kolmanda nädala reedeks.
    -   **Aastad** – valige päev, nädal ja kuu, mil kasutaja peab ülesande lõpule viima. Näiteks soovite võib-olla, et kasutaja täidaks ülesande detsembri kolmanda nädala reedeks.

    Kui kasutaja ei vii ülesannet määratud aja jooksul lõpule, on ülesande tähtaeg ületatud. Hilinenud ülesannet saab eskaleerida suvandite põhjal, mille valite lehe jaotises **Laiendus**.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Määrake, mis juhtub tähtaja ületanud ülesandega
Kui kasutaja ei vii käsitsi ülesannet määratud aja jooksul lõpule, on ülesande tähtaeg ületatud. Hilinenud ülesannet saab eskaleerida või automaatselt muule kasutajale määrata. Järgige neid toiminguid hilinenud ülesande eskaleerimiseks.

1.  Vasakul paanil klõpsake valikut **Laiendus**.
2.  Laiendustee loomiseks märkige ruut **Laiendustee kasutamine**. Süsteem määrab ülesande automaatselt laiendamistee nimekirjas olevatele kasutajatele. Näiteks tähistab järgmine tabel laiendusteed.

    | Seeria | Laiendustee      |
    |----------|----------------------|
    | 1        | Määra isikule: Donna     |
    | 2        | Määra isikule: Erin      |
    | 3        | Lõpptegevus: lükka tagasi |

    Sellise näite korral määrab süsteem hilinenud ülesande Donnale. Kui Donna ei täida ülesannet selleks ettenähtud aja jooksul, määrab süsteem ülesande Erinile. Kui Erin ei täida ülesannet määratud aja jooksul, lükkab süsteem töötlemiseks edastatud dokumendi tagasi.
3.  Laiendustee kasutajale lisamiseks klõpsake valikut **Laienduse lisamine**. Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 4. etapiga.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Suvand</th>
    <th>Kasutajad, kellele ülesanne eskaleeritakse</th>
    <th>Täiendavad etapid</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarhia</td>
    <td>Kasutaja spetsiifilises organisatsioonilises hierarhias</td>
    <td><ol>
    <li>Kui olete valinud vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong> suvandi <strong>Hierarhia</strong>, valige hierarhia tüüp, millele ülesanne eskaleerida.</li>
    <li>Süsteem peab hierarhiast tooma kasutajanimede vahemiku. Need nimed tähistavad kasutajaid, kellele saab ülesannet eskaleerida. Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob. <ol>
    <li>Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</li>
    <li>Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>. Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</li>
    </ol></li>
    <li>Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb ülesanne eskaleerida. <ul>
    <li><strong>Määra kõikidele toodud kasutajatele</strong> – ülesanne eskaleeritakse kõikidele kasutajatele vahemikus.</li>
    <li><strong>Määra ainult viimati toodud kasutajale</strong> – ülesanne eskaleeritakse ainult viimasele kasutajale vahemikus.</li>
    <li><strong>Välista kasutajatelt järgmise tingimusega</strong> – ülesannet ei eskaleerita vahemiku ühelegi kasutajale, kes vastavad teatud tingimusele. Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</li>
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
    <li>Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid. Valige kasutajad, kellele ülesanne eskaleerida, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal ülesande lõpuleviimiseks. Tehke üks järgmistest valikutest:
    -   **Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Päevad** – sisestage päevade arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks.
    -   **Kuud** – valige päev ja nädal, mil kasutaja peab ülesande lõpule viima. Näiteks soovite võib-olla, et kasutaja täidaks ülesande kuu kolmanda nädala reedeks.
    -   **Aastad** – valige päev, nädal ja kuu, mil kasutaja peab ülesande lõpule viima. Näiteks soovite võib-olla, et kasutaja täidaks ülesande detsembri kolmanda nädala reedeks.

5.  Korrake etappe 3 kuni 4 iga kasutaja puhul, kes tuleb laiendusteele lisada. Saate muuta kasutajate järjekorda.
6.  Kui kasutajad eskaleerimisteel ei täida ülesannet määratud aja jooksul, teeb süsteem ülesandega tegevuse. Süsteemi tegevuse määramiseks valige rida **Tegevus** ja seejärel valige tegevus vahekaardi **Lõpptegevus**.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Määrake, millal süsteem ülesandega automaatselt toimingu teeb
Saate konfigureerida süsteemi, nii et see teeks käsitsi ülesandega toimingu, kui teatud tingimused on täidetud. Näiteks peab ülesande nõuete kohaselt kuluaruannete osakonna liige üle vaatama sissetulekud, mis saadetakse koos kuluaruandega. Ettevõtte poliitika kohaselt tuleb ülesanne täita juhul, kui kuluaruande kogusumma on suurem kui 100 USA dollarit. Sel juhul saate konfigureerida süsteemi nii, et ülesande olekuks määratakse automaatselt **Lõpule viidud**, kui summa on väiksem kui 100. Järgige neid toiminguid, et määrata, millal süsteem käsitsi ülesande puhul tegevuse teeb.

1.  Klõpsake vasakpoolsel paanil suvandit **Automaatsed tegevused**.
2.  Märkige ruut **Luba automaatsed tegevused**.
3.  Klõpsake **Lisa tingimus**.
4.  Sisestage tingimus.
5.  Sisestage täiendavad vajalikud tingimused.
6.  Kinnitamaks, et teie sisestatud tingimused on õigesti konfigureeritud, järgige neid etappe.
    1.  Klõpsake nuppu **Test**.
    2.  Lehel **Testi töövoo tingimus** alas **Kontrolli tingimust** valige kirje.
    3.  Klõpsake nuppu **Test**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.
    4.  Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.

7.  Loendist **Automaatse lõpuleviimise tegevus** valige tegevus, mille süsteem peaks ülesande puhul tegema.

## <a name="specify-when-notifications-are-sent"></a>Määrake, millal teatisi saadetakse
Võite saata inimestele teatisi käsitsi ülesande delegeerimisel, eskaleerimisel, lõpuleviimisel või tagasilükkamisel või muudatuse taotlemisel. Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.

1.  Vasakul paanil klõpsake suvandit **Teatised**.
2.  Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.
    -   **Delegeerimine** – ülesanne määrati muule kasutajale.
    -   **Eskaleerimine** – määratud kasutaja ei viinud toimingut määratud aja jooksul lõpule.
    -   **Lõpule viidud** – määratud kasutaja viis ülesande lõpule.
    -   **Tagasi lükatud** – määratud kasutaja lükkas esitatud dokumendi tagasi.
    -   **Muudatuse taotlus** – määratud kasutaja taotles esitatud dokumendi muutmist.

3.  Valige 2. etapis valitud sündmuse rida.
4.  Sisestage teatise tekst vahekaardil **Teatise tekst** olevale tekstiväljale.
5.  Teatise isikupärastamiseks võite sisestada kohatäitjad. Kohatäitjad asendatakse teatise kasutajatele kuvamisel sobiva teabega. Kohatäitja sisestamiseks järgige neid etappe.
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
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</li>
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
    <li>Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid. Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.

## <a name="set-a-time-limit"></a>Ajalimiidi seadmine
Kui käsitsi ülesanne tuleb teatud ajaks lõpule viia, tehke järgmist. 

**Märkus.** Selle protseduuri käigus valitud suvandid alistavad lehe jaotistes **Määramine** ja **Eskaleerimine** valitud suvandid.

1.  Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
2.  Märkige ruut **Määra töövoo elemendi jaoks ajalimiit**.
3.  Määrake väljal **Kestus**, mis ajaks peab ülesanne olema lõpule viidud. Tehke üks järgmistest valikutest:
    -   **Tunnid** – sisestage tundide arv, mille jooksul tuleb ülesanne lõpule viia. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Päevad** – sisestage päevade arv, mille jooksul tuleb ülesanne lõpule viia. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Nädalad** – sisestage nädalate arv, mille jooksul tuleb ülesanne lõpule viia.
    -   **Kuud** – valige päev ja nädal, mil kasutaja peab ülesande lõpule viima. Näiteks soovite võib-olla, et ülesanne oleks täidetud kuu kolmanda nädala reedeks.
    -   **Aastad** – valige päev, nädal ja kuu, mil kasutaja peab ülesande lõpule viima. Näiteks soovite võib-olla, et ülesanne oleks täidetud detsembri kolmanda nädala reedeks.

4.  Ajalimiidi ületamisel teeb süsteem ülesandega tegevuse. Loendist **Tegevus** valige tegevus, mida süsteem peaks tegema.

## <a name="specify-which-actions-are-available-to-the-user"></a>Määrake, millised tegevused on kasutaja jaoks saadaval
Kui kasutajale määratakse käsitsi ülesanne, tuleb kasutajal teha sellega tegevus. Järgige neid toiminguid, et määrata, millised tegevused on kasutaja jaoks ülesande puhul saadaval. **Märkus.** Saadaolevad tegevused erinevad olenevalt ülesande kujundusest.

1.  Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
2.  Märkige ruut **Lõpule viidud**, kui soovite anda kasutajale õiguse märkida ülesande olekuks **Lõpule viidud**.
3.  Märkige ruut **Lükka tagasi**, kui soovite anda kasutajale õiguse lükata esitatud dokument tagasi.
4.  Märkige ruut **Taotle muudatust**, kui soovite anda kasutajale õiguse taotleda muudatuste tegemist talle edastatud dokumendis.
5.  Märkige ruut **Delegeeri**, kui soovite anda kasutajale õiguse delegeerida ülesanne teisele kasutajale.
6.  Märkige ruut **Määra ümber**, kui soovite anda kasutajale õiguse määrata ülesanne ümber teisele kasutajale tööüksuste järjekorras.
7.  Märkige ruut **Vabasta**, kui soovite anda kasutajale õiguse määrata ülesanne ümber teisele kasutajale tööüksuste järjekorras. Muu kasutaja saab ülesande täita.





