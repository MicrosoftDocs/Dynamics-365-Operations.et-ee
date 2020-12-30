---
title: Klientide kulude korvamine
description: Selles artiklis kirjeldatakse, kuidas kliendigrupile korvamiskandeid luua. Kui kliendil on kreeditsaldo, saate kliendile saldosumma hüvitada.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ee884fb22c1a38e2d3022085fed7e3e6077d1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644533"
---
# <a name="reimburse-customers"></a>Klientide kulude korvamine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas kliendigrupile korvamiskandeid luua. Kui kliendil on kreeditsaldo, saate kliendile saldosumma hüvitada. 

Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.

| Eeltingimus                                                            | Kirjeldus |
|-------------------------------------------------------------------------|-------------|
| Juriidilise isiku minimaalse tagasimakse summa määramine.          | Sisestage lehe **Müügireskontro parameetrid** ala **Üldine** väljale **Minimaalne tagasimakse** miinimumsumma, mille saab kliendi ülemaksete puhul tagastada. |
| Valikuline: hankija konto lisamine igale kliendile, kellele saab tagasimakse teha. | Valige kliendi puhul hankija konto lehe **Kliendid** kiirkaardi **Mitmesugused üksikasjad** väljalt **Hankija konto**. |

Korvamiskannete loomisel luuakse kreeditsaldo summa kohta hankija arve. Korvamisprotsess eemaldab kreeditsaldo kliendi kontolt ja loob kliendile vastava hankija konto saldo.

1. Käivitage müügireskontros **Tagasimakse** protsess (**Müügireskontro \> Perioodilised ülesanded \> Tagasimaksed**).
2. Kõigi kannete rühmitamiseks pearaamatu dimensioonidest sõltumata seadke suvand **Summeeri klient** olekusse **Jah**. Ainult sarnaste pearaamatu dimensioonidega kannete rühmitamiseks seadke suvandi olekuks **Ei**.
3. Valige käsk **Kaasa laekumata deebetkannetega kliendid**, et valida kliendid, kellel on maksmata deebetsummad.
4. Kindlate kliendikontode hüvitamiseks valige kiirkaardil **Kaasatavad kirjed** suvand **Filtreeri** ja seejärel määratlege päringus kliendikontod.

    Kreeditsummad kantakse klientide hankijakontodele ja töödeldakse tavaliste maksetena. Kui kliendil ei ole hankija kontot, loob programm kliendi jaoks automaatselt ühekordse hankija konto.

5. Loodud hüvitamiskannete vaatamiseks kasutage **Tagasimakse** aruannet (**Müügireskontro \> Päringud ja aruanded \> Tagasimakse aruanne**).
6. Looge ostureskontros korvamisprotsessi tulemusena loodud hankija arvete makse. Lisateavet hankijatele maksmise kohta vt teemast [Hankija maksete ülevaade](../accounts-payable/Vendor-payments-workspace.md).
