---
title: Funktsionaalsed lüngad varude väärtuse/vananemise aruannete ja nende ladustamise versioonide vahel
description: Funktsionaalsed lüngad varude väärtuse/vananemise aruannete ja nende ladustamise versioonide vahel
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a72e2d32e755e137cebbc0bf7afb0bed08fb93f2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476144"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Funktsionaalsed lüngad varude väärtuse/vananemise aruannete ja nende ladustamise versioonide vahel

[Lao vananemise aruande ladustamise](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage.md) ja [Varude väärtuse salvestamise aruande](/dynamics365/supply-chain/cost-management/inventory-value-report-storage.md) funktsioonid võimaldavad Supply Chain Managementil kuvada suuremahulisi laokandeid. Igal juhul salvestatakse aruande tulemused sirvimiseks ja eksportimiseks, erinevalt nende aruannete mitteladustatavatest versioonidest. Kuid mõned funktsioonid, mis on olemas nende aruannete mitteladustatavates versioonides, pole ladustamisversioonides olemas. Järgmised jaotised summeerivad erinevused ja annavad lahendused.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Ladustamise aruanded ei sisalda vahesummasid, isegi kui need on aruande kavandis lubatud.

Vahesummad võivad põhjustada probleeme, kui tulemus eksporditakse, eriti siis, kui kasutajad muudavad kirje järjestust.

Vahesummade kontrollimiseks saate tulemuse eksportida Microsoft Excel-isse. Teise võimalusena, kui soovite kontrollida vahekokkuvõtteid Supply Chain Managementi siseselt, kasutage [Funktsioonide haldust](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lubada *Uue ruudustiku juhtelemendi* ja *Rühmitamise ruudustiku* funktsioonid, mis annavad palju paindlikuma viisi, et vaadata iga grupi jaoks veeru alusel vahekokkuvõtet. Lisateavet vt jaotisest [Ruudustiku võimalused](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities.md).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Varude väärtuse ladustamise aruanne ei toeta pearaamatu konto teavet.

Saate kasutada protsessi saldot, et saada lao kontode saldo ja võrrelda seda **Varude väärtuse ladustamise** aruandega.
