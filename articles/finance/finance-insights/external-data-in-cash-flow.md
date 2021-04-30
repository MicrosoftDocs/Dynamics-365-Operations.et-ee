---
title: Rahavoo prognoosimises välisandmete kasutamine (eelversioon)
description: See teema kirjeldab seadistuse etappe, mille peate täitma, et välisandmeid saaks sisestada või importida rahavoo prognoosidesse.
author: rcarlson
ms.date: 05/01/2020
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
ms.openlocfilehash: ddfc0670a5fca24d996e9ab605e267f9f3f26f19
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897884"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Rahavoo prognoosimises välisandmete kasutamine (eelversioon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Välisandmeid saab sisestada või importida rahavoo prognoosidesse. See teema kirjeldab seadistuse etappe, mis on omased välisandmete kasutamisele ja võimaldavad kaasata välisandmed rahavoo prognoosimisse.

## <a name="external-data-setup"></a>Välisandmete häälestus

Kasutage vahekaarti **Väline allikas** lehel **Rahavoo prognoosi häälestamine** (**Sularaha- ja pangahaldus \> Rahavoo prognoosimine**), et sisestada sätted, mis toetavad rahavoo prognoosimises välisandmete kasutamist.

Lisateavet häälestamise kohta vaadake jaotisest [Rahavoo prognoosimine](../cash-bank-management/cash-flow-forecasting.md).

Rahavoo prognoosimisse välisandmete sisestamiseks saate kasutada välisandmete sisestamiseks ja muutmiseks Excelis avamise kasutuskogemust. Valige nupp **Välisandmed** ja valige seejärel kas **Lisa välisandmed** või **Redigeeri olemasolevaid välisandmeid**. Kui Microsoft Exceli fail on avatud, saate sisestada teavet järgmistele väljadele.

- **Kirje ID**
- **Kirjeldus** (valikuline)
- **Välise allika nimi** – valige loendist üks väärtustest, mille finantsülevaadete seadistamisel määrasite.
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

#### <a name="privacy-notice"></a>Privaatsusavaldus
Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]