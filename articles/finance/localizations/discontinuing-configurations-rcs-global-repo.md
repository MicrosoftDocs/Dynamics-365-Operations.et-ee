---
title: Katkesta konfiguratsioonid RCS-i globaalses hoidlas
description: See artikkel kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas.
author: gionoder
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: b0605f56058e3c93ea088ee8386ba26c4ce2b65a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272332"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Katkesta konfiguratsioonid RCS-i globaalses hoidlas

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas RCS-i globaalses hoidlas konfiguratsioonist loobuda. Varem oli võimalik kustutada ainult need konfiguratsioonid, mida enam ei vajata. Nüüd saate väljastatud konfiguratsiooni RCS-i globaalses hoidlas märkida kui **Lõpetatud**. Saate sellega ka hallata järgmisi funktsioone: 
 
 - Esitage eelnevalt teatised, kui konfiguratsiooni konfigureerimine on kavandatud lõpetama.
 - Kaasab asenduskonfiguratsioonile rakendatavad üksikasjad.
 - Seadistage **Toetatud kuni** konfiguratsiooni jaoks lõppkuupäev, et kasutajat teavitada selle lõpetamisest.

Kui lõpetate konfiguratsiooniversiooni, saate määrata järgmise valikulise teabe:

  - **Asenduskonfiguratsioon**
  - **Asenduskonfiguratsiooni versioon**
  - **Vabas vormis märkus**: kasutage seda välja dokumentatsiooni linkide või viidete esitamiseks
  - **Toetatud kuni**: sellel väljal kuvatakse pakutav kuupäev, milleni praegust konfiguratsiooni/versiooni toetatakse. Seda kuupäeva tuleb käsitsi uuendada.
  
Konfiguratsiooni katkestamiseks viige lõpule järgmised sammud. 

1. Valige, kas soovite ühe versiooni või kõigi sama sättega versioonide ühe operatsiooniga lõpetada, seades **Kõigi versioonide** väärtuseks **Jah**. 
2. Seadke **Katkestamise** parameetri väärtuseks **Jah**.
3. Konfiguratsioonide katkestamiseks valige **Ok**. Muudatuste salvestamisel täidetakse väli **Lõpetatud kuupäev**.

![Katkesta konfiguratsiooniteave.](media/Discontinue-details-2.png)
  
Saate konfiguratsiooni tagasi valida **Ühiskasutuses** või korrigeerida igal ajal oma teabe sisestamist. Kui jagate konfiguratsiooni, määrake kuupäev, **Toetatud kuni**, mis näitab kogu muu lepinguga seotud teavet ja teie tulevasi plaane.

Kui soovite plaanitud katkestuse kohta teavet jagada, siis enne konfiguratsiooni tegeliku katkestamist saab kasutaja eeltäita kõik asendamisega seotud väljad, kuid jätta parameetri **Katkestamine** väärtuseks **Ei**.

> [!NOTE]
> Lõpetamine ei piira konfiguratsioonidega toiminguid. Saate jätkata konfiguratsioonide importimist, käivitamist või tuletamist, kuid need väljad on informatiivsed.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finantsid toetavad selle teabe kuvamist alates versioonist 10.0.14

Versiooniga 10.0.14 alustamisel toetab Dynamics 365 Finance teabe kuvamist. Lehel **Globaalne hoidla** saate vaadata ajateavet, mis on seotud hiljutise teabega. Vaikimisi filtreeritakse välja enamjaolt konfiguratsioonid.
  
Lehel **Imporditud konfiguratsioonid** (ERSolutionTable) kuvatakse konfiguratsioonid, mis on impordi ajal juba lõpetatud. Nende konfiguratsioonide puhul, mis pärast importimist enam ei tööta, saab teabe sünkroonida, käivitades töö **Impordi konfiguratsioonid**.


