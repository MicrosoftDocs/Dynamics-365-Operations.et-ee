---
title: Töövooatribuutide konfigureerimine
description: See artikkel selgitab, kuidas konfigureerida töövoo erinevaid atribuute.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec604ed9614b80b3b24c670911b4ea480d6131e2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876437"
---
# <a name="configure-workflow-properties"></a>Töövooatribuutide konfigureerimine

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

See artikkel selgitab, kuidas konfigureerida töövoo erinevaid atribuute.

Avage töövoo töövoo atribuutide töövoo konfigureerimiseks. Klõpsake töövoo redaktori lõuendit ja seejärel suvandit **Atribuudid**, et avada leht **Atribuudid**. Seejärel saate järgmiste protseduuride abil konfigureerida töövoo mitmesuguseid atribuute.

## <a name="name-the-workflow"></a>Töövoole nime andmine

Tehke töövoole nime sisestamiseks järgmist.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Väljal **Nimi** sisestage töövoole kordumatu nimi. Näiteks kui loote ostutaotluse töövoo iga riigi/regiooni jaoks, kus tegutsete, võite määrata ostutaotluse töövoo nimeks **Hispaania ostutaotlused** või **Hispaania ostutaotlused**.

## <a name="specify-the-workflow-owner"></a>Töövoo omaniku määramine

Töövoo omanik on isik, kes haldab töövoogu. Töövoo omaniku määramiseks tehke järgmist.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Loendist **Omanik** valige isik, kes töövoogu haldab.

## <a name="select-an-email-template"></a>Valige meilimall

Tehke järgmist, et valida meilimall, mida kasutatakse töövoo kohta teatiste loomiseks.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Valige mall loendist **Töövoo teatiste meilimallid**.

## <a name="enter-instructions-for-users"></a>Kasutajale juhiste sisestamine

Võite sisestada juhised kasutajatele, kes saadavad dokumendid töötlemiseks ja kinnitamiseks. Kasutajaid nimetatakse ka *algatajateks*. Näiteks loote ostutaotluse töövoo ja sisestate juhised. Juhiseid saavad vaadata kasutajad, kes sisestavad ostutaotlusi lehele **Ostutaotlused**. Juhiste vaatamiseks klõpsab algataja töövoo teateribal ikooni. Kasutajatele juhiste sisestamiseks tehke järgmist.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Sisestage juhised väljale **Saatmisjuhised**.
3. Juhiste isikupärastamiseks saate sisestada kohatäitjad. Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks tehke järgmist.

    1. Kohatäitja asukoha määramiseks klõpsake välja **Saatmisjuhised**.
    2. Klõpsake nuppu **Sisesta kohatäide**.
    3. Ilmuvas loendis valige sisestamiseks kohatäitja.
    4. Klõpsake nuppu **Sisesta**.

4. Juhiste tõlgete lisamiseks järgige neid etappe.

    1. Klõpsake valikut **Tõlked**.
    2. Ilmuval lehel klõpsake valikut **Lisa**.
    3. Ilmuvas loendis valige keel, milles teksti sisestate.
    4. Väljale **Tõlgitud tekst** sisestage tekst.
    5. Teksti isikupärastamiseks saate sisestada kohatäitjad. Vaadake kohatäitjate sisestamise juhiseid 3. toimingust.
    6. Klõpsake valikut **Sule**.

> [!NOTE]
> Kohatäiteid ei saa kopeerimise ja kleepimise abil lisada, kuna sihtteavet ei kleebita õigesti. Kasutage kohatäidete lisamiseks liidest.

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a>Määrake, millal seda töövoogu kasutatakse aktiveerimistingimuste kaudu

Sama töövoo tüübi järgi saate luua mitmeid töövooge. Kui teil on mitu samal tüübil põhinevat töövoogu, peate määrama, millal iga töövoogu aktiveerimistingimuste abil kasutatakse. Kui aktiveerimistingimused ei ole täidetud, kasutatakse vaikimisi töövoogu. Kui töövoo tüübi jaoks on määratletud ainult üks töövoo konfiguratsioon, kasutatakse töövoo konfiguratsiooni sõltumata aktiveerimistingimustest.

Näiteks võite luua ostutellimuse töövoo iga riigi või regiooni jaoks, kus tegutsete, nagu Taani ostutellimused või Hispaania ostutellimused, järgmistel tingimustel.

- Taani ostutaotlusi kasutatakse siis, kui riik/regioon on DK
- Hispaania ostutaotlusi peab kasutama siis, kui riik/regioon on ES

Määrake nende toimingute abil, millal konfigureeritavat töövoogu kasutatakse.

1. Vasakul paanil klõpsake suvandit **Aktiveerimine**.
2. Märkige ruut **Määra töövoo käitamise tingimused**.
3. Klõpsake **Lisa tingimus**.
4. Sisestage tingimus.
5. Sisestage täiendavad vajalikud tingimused.
6. Vaadake läbi mõningate sihtkirjetega töövoog, et kinnitada, kas tingimus kaasab ja välistab kirjeid õigesti.

## <a name="specify-when-notifications-are-sent"></a>Määrake, millal teatisi saadetakse

Kui dokument esitatakse töötlemiseks, luuakse töövooeksemplar. Saate saata kasutajatele teatisi, kui töövool põhinevad töövooeksemplarid käivitatakse, viiakse lõpule, katkestatakse või peatatakse tõrke tõttu. Tehke järgmist, et määrata, millal teatisi saadetakse.

1. Vasakul paanil klõpsake suvandit **Teatised**.
2. Märkige ruut iga sündmuse juures, mille puhul saadetakse teatis.

    - **Käivitatud** – teatis saadetakse töövooeksemplari käivitamisel.
    - **Peatatud** – teatis saadetakse juhul, kui töövooeksemplar on tõrke tõttu peatatud.
    - **Lõpule viidud** – teatis saadetakse töövooeksemplari lõpuleviimisel.
    - **Taastamatu** – teatis saadetakse juhul, kui töövooeksemplar on taastamatu tõrke tõttu peatatud.
    - **Katkestatud** – teatis saadetakse töövooeksemplari katkestamisel.

3. Valige 2. etapis valitud sündmuse rida.
4. Sisestage teatise tekst vahekaardil **Teatise tekst**.
5. Teksti isikupärastamiseks saate sisestada kohatäitjad. Kohatäitjad asendatakse teksti kasutajatele kuvamisel sobivate andmetega. Kohatäitja sisestamiseks tehke järgmist.

    1. Kohatäitja asukoha määramiseks klõpsake välja.
    2. Klõpsake nuppu **Sisesta kohatäide**.
    3. Ilmuvas loendis valige sisestamiseks kohatäitja.
    4. Klõpsake nuppu **Sisesta**.
    5. Tavapärane **Teatise teksti** kaasatav kohatäide on „Viimased märkmed: %Workflow.Last note%”, mis kuvab kõiki eelmise etapi kommentaare.

6. Teksti tõlgete lisamiseks järgige neid etappe.

    1. Klõpsake valikut **Tõlked**.
    2. Ilmuval lehel klõpsake käsku **Lisa**.
    3. Ilmuvas loendis valige keel, milles teksti sisestate.
    4. Väljale **Tõlgitud tekst** sisestage tekst.
    5. Teksti isikupärastamiseks saate sisestada kohatäitjad. Vaadake kohatäitjate sisestamise juhiseid 5. toimingust.
    6. Klõpsake valikut **Sule**.

7. Vahekaardil **Adressaat** määrake järgmiste valikute abil, kellele teatisi saadetakse.

    <table>
    <thead>
    <tr>
    <th>Suvand</th>
    <th>Teatised saadetakse neile kasutajatele</th>
    <th>Teatiste saatmiseks tehke järgmist</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Osaleja</td>
    <td>Kasutajad, kes on määratud teatud grupile või rollile</td>
    <td>
    <ol>
    <li>Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Osaleja</strong>.</li>
    <li>Valige vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong> grupi või rolli tüüp, millele teatisi saata.</li>
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Töövoo kasutaja</td>
    <td>Töövoos osalevad kasutajad</td>
    <td>
    <ol>
    <li>Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Töövoo kasutaja</strong>.</li>
    <li>Valige töövoos osaleja vahekaardi <strong>Töövoo kasutaja</strong> loendist <strong>Töövoo kasutaja</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Kasutaja</td>
    <td>Kindlad kasutajad</td>
    <td>
    <ol>
    <li>Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Kasutaja</strong>.</li>
    <li>Vahekaardi <strong>Kasutaja</strong> loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid. Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Sisestage märkusi töövoogu tehtud muudatuste kohta.

Töövoos tehtud muudatuste kohta kommentaaride sisestamiseks tehke järgmist.

1. Vasakul paanil klõpsake nuppu **Märkused**.
2. Sisestage kommentaarid väljale **Sisestage kommentaarid töövoo kohta**.
3. Vaadake kommentaarid üle. Pärast kommentaaride lisamist ei saa neid muuta.
4. Klõpsake käsku **Lisa**, et lisada kommentaar jaotisesse **Kommentaaride ajalugu**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]