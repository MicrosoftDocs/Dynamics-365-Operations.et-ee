---
title: "Töövoo atribuutide konfigureerimine"
description: "See teema selgitab, kuidas konfigureerida töövoo mitmesuguseid atribuute."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 713204bc1e9c757bda48d556ea5b0f66ed79a5c9
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017


---

# <a name="configure-the-properties-of-a-workflow"></a>Töövoo atribuutide konfigureerimine

[!include[banner](../includes/banner.md)]


See teema selgitab, kuidas konfigureerida töövoo mitmesuguseid atribuute.

Avage töövoo töövoo atribuutide töövoo konfigureerimiseks. Klõpsake töövoo redaktori lõuendit ja seejärel suvandit **Atribuudid**, et avada leht **Atribuudid**. Seejärel saate järgmiste protseduuride abil konfigureerida töövoo mitmesuguseid atribuute.

## <a name="name-the-workflow"></a>Töövoole nime andmine
Tehke töövoole nime sisestamiseks järgmist.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Väljal **Nimi** sisestage töövoole kordumatu nimi. Näiteks kui loote ostutaotluse töövoo iga riigi/regiooni jaoks, kus tegutsete, võite määrata ostutaotluse töövoo nimeks **Hispaania ostutaotlused** või **Hispaania ostutaotlused**.

## <a name="specify-the-workflow-owner"></a>Töövoo omaniku määramine
Töövoo omanik on isik, kes haldab töövoogu. Töövoo omaniku määramiseks tehke järgmist.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Loendist **Omanik** valige isik, kes töövoogu haldab.

## <a name="select-an-email-template"></a>Valige meilimall
Tehke järgmist, et valida meilimall, mida kasutatakse töövoo kohta teatiste loomiseks.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Valige mall loendist **Töövoo teatiste meilimallid**.

## <a name="enter-instructions-for-users"></a>Kasutajale juhiste sisestamine
Võite sisestada juhised kasutajatele, kes saadavad dokumendid töötlemiseks ja kinnitamiseks. Kasutajaid nimetatakse ka *algatajateks*. Näiteks loote ostutaotluse töövoo ja sisestate juhised. Juhiseid saavad vaadata kasutajad, kes sisestavad ostutaotlusi lehele **Ostutaotlused**. Juhiste vaatamiseks klõpsab algataja töövoo teateribal ikooni. Kasutajatele juhiste sisestamiseks tehke järgmist.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Sisestage juhised väljale **Saatmisjuhised**.
3.  Juhiste isikupärastamiseks saate sisestada kohatäitjad. Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks tehke järgmist.
    1.  Kohatäitja asukoha määramiseks klõpsake välja **Saatmisjuhised**.
    2.  Klõpsake nuppu **Sisesta kohatäide**.
    3.  Ilmuvas loendis valige sisestamiseks kohatäitja.
    4.  Klõpsake nuppu **Sisesta**.

4.  Juhiste tõlgete lisamiseks järgige neid etappe.
    1.  Klõpsake valikut **Tõlked**.
    2.  Ilmuval lehel klõpsake valikut **Lisa**.
    3.  Ilmuvas loendis valige keel, milles teksti sisestate.
    4.  Väljale **Tõlgitud tekst** sisestage tekst.
    5.  Teksti isikupärastamiseks saate sisestada kohatäitjad. Vaadake kohatäitjate sisestamise juhiseid 3. toimingust.
    6.  Klõpsake valikut **Sule**.

## <a name="specify-when-this-workflow-is-used"></a>Määrake töövoo kasutamise aeg.
Sama tüübi järgi saate luua mitmeid töövooge. Näiteks võite luua ostutellimuse töövoo iga riigi või regiooni jaoks, kus tegutsete, nagu Taani ostutellimused või Hispaania ostutellimused. Kui teil on mitu samal tüübil põhinevat töövoogu, peate määrama, millal iga töövoogu kasutatakse. Eelmise näite puhul määrate järgmised tingimused.

-   Taani ostutaotlusi kasutatakse siis, kui riik/regioon on DK
-   Hispaania ostutaotlusi peab kasutama siis, kui riik/regioon on ES

Määrake nende toimingute abil, millal konfigureeritavat töövoogu kasutatakse.

1.  Vasakul paanil klõpsake suvandit **Aktiveerimine**.
2.  Märkige ruut **Määra töövoo käitamise tingimused**.
3.  Klõpsake **Lisa tingimus**.
4.  Sisestage tingimus.
5.  Sisestage täiendavad vajalikud tingimused.
6.  Tehke järgmist kontrollimaks, kas teie sisestatud tingimused on õigesti määratud.
    1.  Klõpsake nuppu **Test**.
    2.  Lehel **Testi töövoo tingimus** alas **Kontrolli tingimust** valige kirje.
    3.  Klõpsake nuppu **Test**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele. Näiteks kui loote Hispaania jaoks ostutaotluse töövoogu, näete lehe jaotises **Kontrolli tingimust** ostutaotluste loendit. Kui klõpsate käsul **Katseta**, kontrollib süsteem valitud ostutaotlust, et määrata, kas riik/regioon on ES.
    4.  Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.

## <a name="specify-when-notifications-are-sent"></a>Määrake, millal teatisi saadetakse
Kui dokument esitatakse töötlemiseks, luuakse töövooeksemplar. Saate saata kasutajatele teatisi, kui töövool põhinevad töövooeksemplarid käivitatakse, viiakse lõpule, katkestatakse või peatatakse tõrke tõttu. Tehke järgmist, et määrata, millal teatisi saadetakse.

1.  Vasakul paanil klõpsake suvandit **Teatised**.
2.  Märkige ruut iga sündmuse juures, mille puhul saadetakse teatis.
    -   **Käivitatud** – teatis saadetakse töövooeksemplari käivitamisel.
    -   **Peatatud** – teatis saadetakse juhul, kui töövooeksemplar on tõrke tõttu peatatud.
    -   **Lõpule viidud** – teatis saadetakse töövooeksemplari lõpuleviimisel.
    -   **Taastamatu** – teatis saadetakse juhul, kui töövooeksemplar on taastamatu tõrke tõttu peatatud.
    -   **Katkestatud** – teatis saadetakse töövooeksemplari katkestamisel.

3.  Valige 2. etapis valitud sündmuse rida.
4.  Sisestage teatise tekst vahekaardil **Teatise tekst**.
5.  Teksti isikupärastamiseks saate sisestada kohatäitjad. Kohatäitjad asendatakse teksti kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks tehke järgmist.
    1.  Kohatäitja asukoha määramiseks klõpsake välja.
    2.  Klõpsake nuppu **Sisesta kohatäide**.
    3.  Ilmuvas loendis valige sisestamiseks kohatäitja.
    4.  Klõpsake nuppu **Sisesta**.

6.  Teksti tõlgete lisamiseks järgige neid etappe.
    1.  Klõpsake valikut **Tõlked**.
    2.  Ilmuval lehel klõpsake käsku **Lisa**.
    3.  Ilmuvas loendis valige keel, milles teksti sisestate.
    4.  Väljale **Tõlgitud tekst** sisestage tekst.
    5.  Teksti isikupärastamiseks saate sisestada kohatäitjad. Vaadake kohatäitjate sisestamise juhiseid 5. toimingust.
    6.  Klõpsake valikut **Sule**.

7.  Vahekaardil **Adressaat** määrake järgmiste valikute abil, kellele teatisi saadetakse.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Suvand</th>
    <th>Teatised saadetakse neile kasutajatele</th>
    <th>Teatiste saatmiseks tehke järgmist</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Osaleja</td>
    <td>Kasutajad, kes on määratud teatud grupile või rollile</td>
    <td><ol>
    <li>Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Osaleja</strong>.</li>
    <li>Valige vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong> grupi või rolli tüüp, millele teatisi saata.</li>
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Töövoo kasutaja</td>
    <td>Töövoos osalevad kasutajad</td>
    <td><ol>
    <li>Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Töövoo kasutaja</strong>.</li>
    <li>Valige töövoos osaleja vahekaardi <strong>Töövoo kasutaja</strong> loendist <strong>Töövoo kasutaja</strong>.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Kasutaja</td>
    <td>Konkreetsed Finance and Operationsi kasutajad</td>
    <td><ol>
    <li>Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Kasutaja</strong>.</li>
    <li>Vahekaardi <strong>Kasutaja</strong> loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Dynamics 365 for Finance and Operationsi kasutajaid. Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Sisestage märkusi töövoogu tehtud muudatuste kohta.
Töövoos tehtud muudatuste kohta kommentaaride sisestamiseks tehke järgmist.

1.  Vasakul paanil klõpsake nuppu **Märkused**.
2.  Sisestage kommentaarid väljale **Sisestage kommentaarid töövoo kohta**.
3.  Vaadake kommentaarid üle. Pärast kommentaaride lisamist ei saa neid muuta.
4.  Klõpsake käsku **Lisa**, et lisada kommentaar jaotisesse **Kommentaaride ajalugu**.





