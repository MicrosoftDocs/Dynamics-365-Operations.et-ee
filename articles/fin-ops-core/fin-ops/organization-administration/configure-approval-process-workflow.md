---
title: Töövoo kinnitusprotsesside konfigureerimine
description: Kinnitusprotsessi atribuutide konfigureerimiseks tehke järgmist.
author: ChrisGarty
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998ee15d828feefb0a9691138ae8001331283d5b866386500f5cf5de48291b43
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756317"
---
# <a name="configure-approval-processes-in-a-workflow"></a>Töövoo kinnitusprotsesside konfigureerimine

[!include [banner](../includes/banner.md)]

Kinnitusprotsessi atribuutide konfigureerimiseks tehke järgmist.

Kinnitusprotsessi konfigureerimiseks paremklõpsake töövooredaktoris kinnitamise elementi ja klõpsake seejärel valikut **Atribuudid**, et avada vorm **Atribuudid**.

## <a name="name-the-approval-process"></a>Kinnitusprotsessile nime andmine

Kinnitusprotsessi nime sisestamiseks tehke järgmist.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Väljale **Nimi** sisestage kinnitusprotsessile kordumatu nimi.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Määramine, millal süsteem dokumendiga automaatselt toimingu teeb

Saate konfigureerida süsteemi automaatselt dokumendiga tegelema, kui teatud tingimused on täidetud. Näiteks saab süsteem kinnitada kuluaruanded, mille kogusumma on väiksem kui 100 USA dollarit. Selleks et määrata, millal süsteem dokumendi puhul toimingu teeb, tehke järgmist.

1. Klõpsake vasakpoolsel paanil suvandit **Automaatsed tegevused**.
2. Märkige ruut **Luba automaatsed tegevused**.
3. Klõpsake valikut **Lisa tingimus**.
4. Sisestage tingimus.
5. Vajadusel lisage lisatingimused.
6. Kontrollimaks, kas teie sisestatud tingimused on õigesti konfigureeritud, tehke järgmist.

    1. Klõpsake valikut **Katseta**, et avada leht **Katseta töövoo tingimust**.
    2. Valige vormi alal kirje **Kontrolli tingimust**.
    3. Klõpsake nuppu **Test**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.
    4. Klõpsake valikut **OK** või **Tühista**, et naasta vormile **Atribuudid**.

7. Loendist **Automaatne tegevus** valige tegevus, mille süsteem peaks ülesande puhul tegema.

## <a name="specify-when-notifications-are-sent"></a>Määrake, millal teatisi saadetakse

Saate saata inimestele teatisi dokumendi kinnitamisel, tagasilükkamisel, delegeerimisel või laiendamisel või muudatuse taotlemisel. Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.

1. Vasakul paanil klõpsake suvandit **Teatised**.
2. Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.

    - **Delegeeri** – kui dokument on määratud kinnitamiseks teisele kasutajale.
    - **Laienda** – kui määratud kasutaja pole dokumendi puhul nõutavat toimingut eraldatud aja jooksul teinud.
    - **Kinnita** – kui dokument on kinnitatud.
    - **Lükka tagasi** – kui dokument on tagasi lükatud.
    - **Muudatuse taotlus** – kui määratud kasutaja on taotlenud esitatud dokumendi muutmist.

3. Valige 2. etapis valitud sündmuse rida.
4. Klõpsake vahekaarti **Teatise tekst**.
5. Sisestage tekstiväljale teatise nimi.
6. Teksti isikupärastamiseks saate sisestada kohatäitjad, mis asendatakse sobivate andmetega, kui need kuvatakse kasutajatele. Kohatäitja sisestamiseks tehke järgmist.

    1. Kohatäitja asukoha määramiseks klõpsake tekstiväljal soovitud kohta.
    2. Klõpsake nuppu **Sisesta kohatäide**.
    3. Valige kuvatavast loendist sisestatav kohatäitja.
    4. Klõpsake nuppu **Sisesta**.

7. Teatise tõlgete lisamiseks klõpsake valikut **Tõlked**. Kuvataval vormil tehke järgmist.

    1. Klõpsake käsku **Lisa**.
    2. Valige kuvatavast loendist keel, milles soovite teksti sisestada.
    3. Tekstiväljale **Tõlgitud tekst** sisestage tekst.
    4. Teksti isikupärastamiseks sisestage kohatäitjad.
    5. Klõpsake valikut **Sule**.

8. Klõpsake vahekaarti **Adressaat**.
9. Määrake, kellele teatised saadetakse. Valige järgmises tabelis üks suvanditest ja seejärel järgige selle suvandi täiendavaid etappe, enne kui jätkate 10. etapiga.

    <table>
    <thead>
    <tr>
    <th>Suvand</th>
    <th>Teatise adressaadid</th>
    <th>Täiendavad etapid</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><strong>Osaleja</strong></td>
    <td>Kasutajad, kes on määratud teatud grupile või rollile</td>
    <td>
    <ol>
    <li>Pärast suvandi <strong>Osaleja</strong> valimist klõpsake vahekaarti <strong>Rollil põhinev</strong>.</li>
    <li>Loendis <strong>Osaleja tüüp</strong> valige grupi või rolli tüüp, millele teatisi saata.</li>
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Töövoo kasutaja</strong></td>
    <td>Kasutajad, kes osalevad praeguses töövoos</td>
    <td>
    <ol>
    <li>Kui olete valinud suvandi <strong>Töövoo kasutaja</strong>, klõpsake vahekaarti <strong>Töövoo kasutaja</strong>.</li>
    <li>Loendist <strong>Töövoo kasutaja</strong> valige töövoos osalev kasutaja.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Kasutaja</strong></td>
    <td>Kindlad kasutajad</td>
    <td>
    <ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. Korrake etappe 3–9 iga sündmuse puhul, mille 2. etapis valisite.

## <a name="specify-a-final-approver"></a> Lõpliku kinnitaja määramine

Saate määrata lõpliku kinnitaja stsenaariumite jaoks, kus kinnitaja on dokumendi kinnitamiseks esitanud isik ja kasutatakse nõuet "keela esitaja kinnitus". Lõpliku kinnitaja määramiseks tehke järgmist.

1. Paremklõpsake töövooredaktoris kinnitamise elementi ja valige seejärel **Atribuudid**, et avada vorm **Atribuudid**.
2. Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
3. Märkige ruut **Kasuta lõplikku kinnitajat**.
4. Valige loendist lõplikuks kinnitajaks määratav kasutaja.

## <a name="set-a-time-limit"></a>Ajalimiidi seadmine

Kui kinnitusprotsess tuleb teatud ajaks lõpule viia, tehke järgmist.

> [!NOTE]
> Neis etappides valitavad suvandid tühistavad iga kinnitusetapi aladel **Määramine** ja **Laiendus** valitud suvandid.

1. Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
2. Märkige ruut **Määra töövoo elemendi jaoks** **ajalimiit**.
3. Määrake väljal **Kestus**, mis ajaks peab kinnitusprotsess olema lõpule viidud. Tehke üks järgmistest valikutest:

    - **Tunnid** – sisestage tundide arv, mille jooksul tuleb kinnitusprotsess lõpule viia. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    - **Päevad** – sisestage päevade arv, mille jooksul tuleb kinnitusprotsess lõpule viia. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    - **Nädalad** – sisestage nädalate arv, mille jooksul tuleb kinnitusprotsess lõpule viia.
    - **Kuud** – valige päev ja nädal, milleks kinnitusprotsess peab olema lõpule viidud. Näiteks võite soovida, et kinnitusprotsess oleks lõpule viidud kuu kolmanda nädala reedeks.
    - **Aastad** – valige päev, nädal ja kuu, milleks kinnitusprotsess peab olema lõpule viidud. Näiteks võite soovida, et kinnitusprotsess oleks valmis detsembri kolmanda nädala reedeks.

4. Ajalimiidi ületamisel teeb süsteem dokumendiga tegevuse. Loendist **Tegevus** valige tegevus, mida süsteem peaks tegema.

## <a name="specify-which-actions-are-available-to-the-user"></a>Määrake, millised tegevused on kasutaja jaoks saadaval

Kasutaja peab talle määratud dokumendiga tegelema. Esitatud dokumendi puhul kasutajale saadaolevate tegevuste määramiseks tehke järgmist.

1. Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
2. Märkige ruut **Kinnita**, kui kasutaja võib dokumendi kinnitada.
3. Märkige ruut **Lükka tagasi**, kui kasutaja võib dokumendi tagasi lükata.
4. Märkige ruut **Taotle muudatust**, kui kasutaja võib taotleda dokumendile muudatuste tegemist.
5. Märkige ruut **Delegeeri**, kui kasutaja võib määrata dokumendile kinnitajaks teise kasutaja.

> [!NOTE]
> Märkeruut **Tegevuste aktiveerimine ettevõtteportaali töödeloendist** pole soovitatav.

## <a name="configure-the-approval-steps"></a> Kinnitusetappide konfigureerimine

Kinnitusprotsess koosneb kinnitusetappidest. Kinnitusprotsessi etappide lisamiseks ja konfigureerimiseks tehke järgmist.

1. Topeltklõpsake töövooredaktoris kinnitusprotsessi. Töövooredaktoris kuvatakse kinnitusprotsessi etapid.
2. Kinnitusetapi lisamiseks lohistage etapp alalt **Töövoo elemendid** lõuendile.
3. Kinnitusetapi konfigureerimiseks vaadake jaotist [Töövoos kinnitusetappide konfigureerimine](configure-approval-step-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]