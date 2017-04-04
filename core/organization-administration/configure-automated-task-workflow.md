---
title: "Konfigureerida automaat-tegumi töövoos"
description: "See teema selgitab, kuidas konfigureerida automatiseeritud ülesande atribuute."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5fbdfc037daec295028a9ac4ca4608f0abe84112
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-automated-task-in-a-workflow"></a>Konfigureerida automaat-tegumi töövoos

See teema selgitab, kuidas konfigureerida automatiseeritud ülesande atribuute.

Töövoo redaktoris automatiseeritud ülesande loomiseks paremklõpsake ülesannet ja seejärel klõpsake suvandit **Atribuudid**, et avada lehekülg **Atribuudid**. Seejärel kasutage järgmisi protseduure, et konfigureerida automatiseeritud ülesande atribuudid.

## <a name="name-the-task"></a>Ülesandele nime andmine
Sisestage automatiseeritud ülesandele nimi järgmisi juhiseid järgides.

1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Sisestage ülesande kordumatu nimi väljale **Nimi**.

## <a name="specify-when-notifications-are-sent"></a>Määrake, millal teatisi saadetakse
Saate saate inimestele teatisi, kui automatiseeritud ülesannet käitatakse või see tühistatakse. Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.

1.  Vasakul paanil klõpsake suvandit **Teatised**.
2.  Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.
    -   **Käivitamine** – teatised saadetakse ülesande käitamisel.
    -   **Tühistatud** – teatised saadetakse ülesande tühistamisel.

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
    <li>Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Töövoo kasutaja</td>
    <td>Kasutajad, kes osalevad praeguses töövoos</td>
    <td><ul>
    <li>Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Kasutaja</td>
    <td>Teatud Microsoft Dynamics 365 toimingud kasutajatele</td>
    <td><ol>
    <li>Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</li>
    <li>On <strong>saadaval kasutajate</strong> loend sisaldab kõiki Dynamics 365 toimingud kasutajatele. Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.



