---
title: TDS-i arvutuste valemikoostaja
description: Selles teemas antakse näide, kuidas allika järgi mahaarvatud maks (TDS) arvutatakse kandega seotud TDS-i grupis iga TDS-i maksukoodi jaoks määratud valemi alusel.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d0f644da640b56761a52baec9ff01c898e895d19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023169"
---
# <a name="formula-designer-for-tds-calculations"></a>TDS-i arvutuste valemikoostaja

[!include [banner](../includes/banner.md)]

See teema annab näite selle kohta, kuidas maks, mis on maha arvatud allikast (TDS), põhineb iga TDS-i maksukoodi jaoks määratud valemil. TDS-i maksukoodid määratletakse kandega seotud TDS-grupis. Enne TDS-valemite kujundamist viige lõpule TDS-i jaoks nõutav põhiseadistus, nagu on loetletud järgmistes sammudes. 

- Kinnipeetava maksu gruppide seadistamine **Kinnipeetava maksu grupid** lehel. 
- Seadistage TDS-i komponendid ja manustage TDS-i komponendigrupp TDS-i komponentidele, kasutades **Kinnipeetava maksu komponentide** lehte. 
- Seadistage TDS-i komponendid ja manustage TDS-i komponendigrupp TDS-i komponentidele, kasutades **Kinnipeetava maksu komponentide** lehte. 
- Kinnipeetava maksu gruppide seadistamine **Kinnipeetava maksu grupid** lehel. Seejärel lisage TDS-i maksukoodid maksugrupile ja määratlege valem, kasutades **valemikoosturi** lehte. 

**Näidisvalem**

Selles näites on TDS-i grupp, Rent on seotud hankijale A loodud ostuarvega. Arve summa on 100 000 $. Arve TDS-i arvutuse vaatamiseks vaadake järgmist tabelit.

| TDS grupid                                                   | TDS-grupiga seotud TDS-i maksukoodid | Väärtus              | Maksustatav alus (valemikoosturid) | Arvutusavaldis (valemi kujundaja) | Baassumma | Arvutatud TDS-summa |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Üür                                                         | TDS (TDS komponent-TDS)                | 10%                | Brutosumma                      |                                            | 100,000      | 10,000                 |
| Lisatasu (TDS-i komponendi lisatasu)                         | 10%                                     | V. a brutosumma | +TDS                              |                   10000                    | 1000        |                       |
| PE-Sess (TDS-i komponent – PE-Sess)                            | 2%                                      | V. a brutosumma | + TDS + lisatasu                    |                   11000                    | 220         |                       |
| SHE Cess (TDS-i komponent- SHE Cess)                          | 1%                                      | V. a brutosumma | +TDS+lisatasu                    |                   11000                    | 110         |                       |
| **Kogu** **TDS** **arve** **jaoks** **arvutatud** **arve** | **11,330**                               |                    |                                   |                                            |             |                       |

Kandekirjed luuakse järgmiselt.

| Konto           | Debiteeri  | Krediit |
| ----------------- | ------ | ------ |
| Üür              | 100,000 |        |
| Hankija A          |        | 100,000 |
| Hankija A          | 11,330  |        |
| TDS tasumine       |        | 10,000  |
| Lisatasu tasumine |        | 1000   |
| PE-Cess tasumine   |        | 220    |
| SHE Cess tasumine  |        | 110    |
