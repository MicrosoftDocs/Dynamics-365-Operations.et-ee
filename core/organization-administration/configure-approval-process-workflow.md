---
title: "Konfigureerida heakskiitmisprotsess töövoos"
description: "Kinnitusprotsessi atribuutide konfigureerimiseks tehke järgmist."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 579e393ef64bc5ad72d129ac08ac215c524d5c55
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-approval-process-in-a-workflow"></a>Konfigureerida heakskiitmisprotsess töövoos

Kinnitusprotsessi atribuutide konfigureerimiseks tehke järgmist.

Konfigureerimiseks töövoo redaktor heakskiitmisprotsess, Paremklõpsake elementi heakskiidu ja klõpsake **atribuudid** avamiseks ning **atribuudid** vormi.
Kinnitusprotsessile nime andmine
-------------------------

Kinnitusprotsessi nime sisestamiseks tehke järgmist.
1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Väljale **Nimi** sisestage kinnitusprotsessile kordumatu nimi.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Määramine, millal süsteem dokumendiga automaatselt toimingu teeb
Saate konfigureerida süsteemi automaatselt dokumendiga tegelema, kui teatud tingimused on täidetud. Näiteks saab süsteem kinnitada kuluaruanded, mille kogusumma on väiksem kui 100 USA dollarit. Selleks et määrata, millal süsteem dokumendi puhul toimingu teeb, tehke järgmist.
1.  Klõpsake vasakpoolsel paanil suvandit **Automaatsed tegevused**.
2.  Märkige ruut **Luba automaatsed tegevused**.
3.  Click **Add condition**.
4.  Sisestage tingimus.
5.  Vajadusel lisage lisatingimused.
6.  Kontrollimaks, kas teie sisestatud tingimused on õigesti konfigureeritud, tehke järgmist.
    1.  Klõpsake valikut **Katseta**, et avada leht **Katseta töövoo tingimust**.
    2.  Valige vormi alal kirje **Kontrolli tingimust**.
    3.  Klõpsake nuppu **Test**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.
    4.  Klõpsake **OK** või **tühistada** tagasi selle **atribuudid** vormi.

7.  Loendist **Automaatne tegevus** valige tegevus, mille süsteem peaks ülesande puhul tegema.

## <a name="specify-when-notifications-are-sent"></a>Määrake, millal teatisi saadetakse
Saate saata inimestele teatisi dokumendi kinnitamisel, tagasilükkamisel, delegeerimisel või laiendamisel või muudatuse taotlemisel. Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.
1.  Vasakul paanil klõpsake suvandit **Teatised**.
2.  Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.
    -   **Volitatud esindaja** – kui dokumendile on määratud teisele kasutajale kinnitamiseks.
    -   **Avalikku korda** – kui määratud kasutajale on tegutsenud dokumendiga õigel ajal.
    -   **Kinnitada** – kui dokument on kinnitatud.
    -   **Hülga** – kui dokument on tagasi lükatud.
    -   **Taotle muudatust** – kui määratud kasutajale on nõudnud dokument, mis esitati.

3.  Valige 2. etapis valitud sündmuse rida.
4.  Klõpsake vahekaarti **Teatise tekst**.
5.  Sisestage tekstiväljale teatise nimi.
6.  Teksti isikupärastamiseks saate sisestada kohatäitjad, mis asendatakse sobivate andmetega, kui need kuvatakse kasutajatele. Kohatäitja sisestamiseks tehke järgmist.
    1.  Kohatäitja asukoha määramiseks klõpsake tekstiväljal soovitud kohta.
    2.  Klõpsake nuppu **Sisesta kohatäide**.
    3.  Valige kuvatavast loendist sisestatav kohatäitja.
    4.  Klõpsake nuppu **Sisesta**.

7.  Tõlked teate lisamiseks klõpsake **tõlked**. Kuvataval vormil tehke järgmist.
    1.  Click **Add**.
    2.  Valige kuvatavast loendist keel, milles soovite teksti sisestada.
    3.  Tekstiväljale **Tõlgitud tekst** sisestage tekst.
    4.  Teksti isikupärastamiseks sisestage kohatäitjad.
    5.  Klõpsake valikut **Sule**.

8.  Klõpsake vahekaarti **Adressaat**.
9.  Määrake, kellele teatised saadetakse. Valige järgmises tabelis üks suvanditest ja seejärel järgige selle suvandi täiendavaid etappe, enne kui jätkate 10. etapiga.

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
    <td><strong>Osaleja</strong></td>
    <td>Kasutajad, kes on määratud teatud grupile või rollile</td>
    <td><ol>
    <li>Pärast suvandi <strong>Osaleja</strong> valimist klõpsake vahekaarti <strong>Rollil põhinev</strong>.</li>
    <li>Loendis <strong>Osaleja tüüp</strong> valige grupi või rolli tüüp, millele teatisi saata.</li>
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><strong>Töövoo kasutaja</strong></td>
    <td>Kasutajad, kes osalevad praeguses töövoos</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Töövoo kasutaja</strong>, klõpsake vahekaarti <strong>Töövoo kasutaja</strong>.</li>
    <li>Loendist <strong>Töövoo kasutaja</strong> valige töövoos osalev kasutaja.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><strong>User</strong></td>
    <td>Teatud Microsoft Dynamics 365 toimingud kasutajatele</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>On <strong>saadaval kasutajate</strong>: loend sisaldab kõiki Microsoft Dynamics 365 toimingud kasutajatele. Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad:</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. Korrake etappe 3–9 iga sündmuse puhul, mille 2. etapis valisite.

## <a name="specify-a-final-approver"></a> Lõpliku kinnitaja määramine
Teil võib olla vajalik määrata lõplik kinnitaja olukordades, kus kinnitaja on isik, kes esitas dokumendi kinnitamiseks. Lõpliku kinnitaja määramiseks tehke järgmist.
1.  Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
2.  Märkige ruut **Kasuta lõplikku kinnitajat**.
3.  Valige loendist lõplikuks kinnitajaks määratav kasutaja.

## <a name="set-a-time-limit"></a>Ajalimiidi seadmine
Kui kinnitusprotsess tuleb teatud ajaks lõpule viia, tehke järgmist.
| **Märkus. **                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Neis etappides valitavad suvandid tühistavad iga kinnitusetapi aladel **Määramine** ja **Laiendus** valitud suvandid. |

1.  Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
2.  Märkige ruut **Määra töövoo elemendi jaoks** **ajalimiit**.
3.  Määrake väljal **Kestus**, mis ajaks peab kinnitusprotsess olema lõpule viidud. Tehke üks järgmistest valikutest:
    -   **Tunnid** – sisestage tundide arv, mille jooksul tuleb kinnitusprotsess lõpule viia. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Päevad** – sisestage päevade arv, mille jooksul tuleb kinnitusprotsess lõpule viia. Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.
    -   **Nädalad** – sisestage nädalate arv, mille jooksul tuleb kinnitusprotsess lõpule viia.
    -   **Kuud** – valige päev ja nädal, milleks kinnitusprotsess peab olema lõpule viidud. Näiteks võite soovida, et kinnitusprotsess oleks lõpule viidud kuu kolmanda nädala reedeks.
    -   **Aastad** – valige päev, nädal ja kuu, milleks kinnitusprotsess peab olema lõpule viidud. Näiteks võite soovida, et kinnitusprotsess oleks valmis detsembri kolmanda nädala reedeks.

4.  Ajalimiidi ületamisel teeb süsteem dokumendiga tegevuse. Loendist **Tegevus** valige tegevus, mida süsteem peaks tegema.

## <a name="specify-which-actions-are-available-to-the-user"></a>Määrake, millised tegevused on kasutaja jaoks saadaval
Kasutaja peab talle määratud dokumendiga tegelema. Esitatud dokumendi puhul kasutajale saadaolevate tegevuste määramiseks tehke järgmist.
1.  Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.
2.  Valige selle **kinnitamine** ruut kui kasutaja saab dokumendi heakskiitmiseks.
3.  Valige selle **tagasi lükata** ruut kasutaja saab dokumendi hüljata.
4.  Valige selle **Taotle muudatust** ruut kasutaja saab taotleda dokumendi muutmist.
5.  Valige selle **esindaja** ruut kui kasutaja saab määrata dokumendi teisele kasutajale kinnitamiseks.

**Märkus**. Märkeruut **Tegevuste aktiveerimine ettevõtteportaali töödeloendist** pole soovitatav.

## <a name="configure-the-approval-steps"></a> Kinnitusetappide konfigureerimine
Kinnitusprotsess koosneb kinnitusetappidest. Kinnitusprotsessi etappide lisamiseks ja konfigureerimiseks tehke järgmist.
1.  Topeltklõpsake töövooredaktoris kinnitusprotsessi. Töövooredaktoris kuvatakse kinnitusprotsessi etapid.
2.  Kinnitusetapi lisamiseks lohistage etapp alalt **Töövoo elemendid** lõuendile.
3.  Kinnitusetapi konfigureerimiseks vt teemat [Kinnitusetapi konfigureerimine](http://axhelp.dynamics.com/en/wiki/configure-an-approval-step/).




