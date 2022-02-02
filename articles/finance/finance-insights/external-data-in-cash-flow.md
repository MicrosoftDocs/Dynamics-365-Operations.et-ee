---
title: Välisandmed likviidsuse planeerimistes
description: Selles teemas kirjeldatakse seadistuse etappe, mis tuleb lõpule viia, et välisandmeid saaks sisestada või importida likviidsuse prognoosi.
author: rcarlson
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 8284ccd7ac383c53960f7fd6a1333aeb0e7e6f3c
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969008"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Välisandmed likviidsuse planeerimistes

[!include [banner](../includes/banner.md)]

Välisandmeid saab sisestada või importida rahavoo prognoosidesse. See teema kirjeldab seadistuse etappe, mis on omased välisandmete kasutamisele ja võimaldavad kaasata välisandmed rahavoo prognoosimisse.

## <a name="external-data-setup"></a>Välisandmete häälestus

Kasutage vahekaarti Väline allikas likviidsuse prognoosi seadistamise lehel (Sularaha ja panga halduse likviidsuse prognoosimise häälestus), et sisestada sätted, mis toetavad väliste andmete **kasutamist** **·** **\>\>** likviidsuse eelarves.

Välisandmeid saab sisestada või importida rahavoo prognoosidesse. Enne välisandmete sisestamist või importimist tuleb seadistada välisallikad. Seadistage **vahekaardil** Välisallikas välised rahavoo kategooriad. Kategooria võib olla **väljaminev** või **sissetulev.** **Likviidsuse** peaks olema sisestustüübiks valitud. Valige juriidilise **isiku sätete ruudustikus juriidilised isikud ja vastavad põhikontod,** mille suhtes välised rahavookategooriad kehtivad.

Rahavoogude prognooside seadistamise kohta leiate lisateavet teemast [Rahavoogude prognoosimine](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Välisandmete sisemine

Väliste andmete sisestamiseks ja muutmiseks likviidsuse prognoosimiseks saate kasutada Exceli **kogemuses** avatud. Valige likviidsuse prognoosi häälestuse lehel nupp Välised andmed ja seejärel valige **suvand** Lisa **·** **välisandmed või** **redigeerige olemasolevaid** välisandmeid. Kui Microsoft Exceli fail on avatud, saate sisestada teavet järgmistele väljadele.

- **Kirje ID** (kordumatu)
- **Kirjeldus** (valikuline)
- **Välisallika** nimi– valige üks loendis väärtustest, mis määratleti finantsülevaadete häälestamisel.
- **Juriidiline isik**
- **Kuupäev**
- **Summa kandevaluutas**
- **Valuutakood**
- **Vaikedimensioon** (valikuline)
- **Dokumendi number** (valikuline)
- **Kontonumber** (valikuline)
- **Konto nimi** (valikuline)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Välisandmete importimine andmehalduse raamistikku kasutades

Saate rahavoo prognoosimiseks importida välisandmed, kasutades tööruumi **Andmehaldus** ja olemit, mille nimi on **Rahavoo prognoosimise välisallika kirje**.

Lisaks kui peate teisaldama häälestuse andmed ühest keskkonnast teise, siis on häälestamise tabelite jaoks saadaval järgmised nõutavad olemid.

- Likviidsuse planeerimise välise allika seadistus
- Likviidsuse planeerimise välise allika juriidilise isiku seadistus

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
