---
title: Katkesta konfiguratsioonid RCS-i globaalses hoidlas
description: See teema kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 25ad0744e7c3320505c13c465d440b6a364da47c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840288"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Katkesta konfiguratsioonid RCS-i globaalses hoidlas

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas. Varem oli võimalik kustutada ainult need konfiguratsioonid, mida enam ei vajata. Nüüd saate väljastatud konfiguratsiooni RCS-i globaalses hoidlas märkida kui **Lõpetatud**. Saate sellega ka hallata järgmisi funktsioone: 
 
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

![Katkesta konfiguratsiooniteave](media/Discontinue-details-2.png)
  
Saate konfiguratsiooni tagasi valida **Ühiskasutuses** või korrigeerida igal ajal oma teabe sisestamist. Kui jagate konfiguratsiooni, määrake kuupäev, **Toetatud kuni**, mis näitab kogu muu lepinguga seotud teavet ja teie tulevasi plaane.

Kui soovite plaanitud katkestuse kohta teavet jagada, siis enne konfiguratsiooni tegeliku katkestamist saab kasutaja eeltäita kõik asendamisega seotud väljad, kuid jätta parameetri **Katkestamine** väärtuseks **Ei**.

> [!NOTE]
> Lõpetamine ei piira konfiguratsioonidega toiminguid. Saate jätkata konfiguratsioonide importimist, käivitamist või tuletamist, kuid need väljad on informatiivsed.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finantsid toetavad selle teabe kuvamist alates versioonist 10.0.14

Alates versioonist 10.0.14 toetab Dynamics 365 Finance lõpetamisteabe kuvamist. Lehel **Globaalne hoidla** saate vaadata ajateavet, mis on seotud hiljutise teabega. Vaikimisi filtreeritakse välja enamjaolt konfiguratsioonid.
  
Lehel **Imporditud konfiguratsioonid** (ERSolutionTable) kuvatakse konfiguratsioonid, mis on impordi ajal juba lõpetatud. Nende konfiguratsioonide puhul, mis pärast importimist enam ei tööta, saab teabe sünkroonida, käivitades töö **Impordi konfiguratsioonid**.


