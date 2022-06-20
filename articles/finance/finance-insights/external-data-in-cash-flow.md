---
title: Välisandmed likviidsuse planeerimistes
description: See artikkel kirjeldab seadistuse etappe, mis tuleb lõpule viia, et välisandmeid saaks sisestada või importida likviidsuse prognoosi.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0cb05770dc2fbd4e13af261b5f0a0e117a2f6d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846940"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Välisandmed likviidsuse planeerimistes

[!include [banner](../includes/banner.md)]

Välisandmeid saab sisestada või importida rahavoo prognoosidesse. See artikkel kirjeldab seadistuse etappe, mis on spetsiifilised välisandmete kasutamisele ja mis võimaldavad välisandmete kaasamist likviidsuse prognoosi.

## <a name="external-data-setup"></a>Välisandmete häälestus

Kasutage vahekaarti **Väline** allikas likviidsuse **prognoosi** häälestuse lehel (**\>\> Sularaha ja panga halduse likviidsuse prognoosimise häälestus**), et sisestada sätted, mis toetavad väliste andmete kasutamist likviidsuse prognoosides.

Välisandmeid saab sisestada või importida rahavoo prognoosidesse. Enne välisandmete sisestamist või importimist tuleb seadistada välisallikad. Seadistage **vahekaardil Välisallikas** välised rahavoo kategooriad. Kategooria võib olla väljaminev **või sissetulev** **.** **Likviidsuse** peaks olema sisestustüübiks valitud. Valige juriidilise **isiku sätete ruudustikus** juriidilised isikud ja vastavad põhikontod, mille suhtes välised rahavookategooriad kehtivad.

Likviidsuse prognoosimise kohta lisateabe saamiseks vt likviidsuse [prognoosimist](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Välisandmete sisemine

Väliste andmete sisestamiseks ja muutmiseks likviidsuse prognoosimiseks saate kasutada Exceli **kogemuses avatud**. Valige likviidsuse **prognoosi** tööruumi lehel nupp **Välised** andmed ja **seejärel valige suvand Lisa välisandmed või** redigeerige **olemasolevaid välisandmeid**. Kui Microsoft Exceli fail on avatud, saate sisestada teavet järgmistele väljadele.

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
