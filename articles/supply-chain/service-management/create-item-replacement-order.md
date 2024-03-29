---
title: Kauba asendamise tellimuse loomine
description: Kauba asendustellimused luuakse tavaliselt pärast toote tagastamist ja kontrollimist.
author: josaw1
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14751fb0e0632ca986d6eddf55c93d44fbd68276
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015460"
---
# <a name="create-an-item-replacement-order"></a>Kauba asendamise tellimuse loomine 

[!include [banner](../includes/banner.md)]


Kauba asendustellimused luuakse tavaliselt pärast toote tagastamist ja kontrollimist. Kui kaup tuleb siiski asendada enne tagastamist või kui originaalkaupa ei tagastata, saate luua kauba asendustellimuse kohe pärast tagastustellimuse loomist.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Looge asendustellimus pärast tagastatava kauba kättesaamist.

1.  Klõpsake müügi **ja turunduse müügi** \> **tagastused** \> **kõik tagastustellimused**.

2.  Looge uus tagastustellimus või valige tagastustellimus loendist, et avada vorm **Tagastustellimus – RMA-kood: %1, %2**.

3.  Klõpsake valikut **Tagastusrida** ja valige seejärel **Asenduskaup**.

4.  Valige kirje, millega tagastatud kaup asendada. Sisestage kauba täpsustused ja klõpsake seejärel **Rakenda**.

5.  Tagastustellimusele saatelehe loomiseks klõpsake valikut **Saateleht**. Müügitellimus luuakse valitud asenduskaubale.
    
    Pärast müügitellimuse loomist asenduskaubale otsitakse müügilepinguid automaatselt ja kui on kehtiv müügileping, rakendatakse see müügitellimusele.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Asendustellimuse loomine enne tagastatava kauba kättesaamist

1.  Klõpsake müügi **ja turunduse müügi** \> **tagastused** \> **kõik tagastustellimused**.

2.  Looge uus tagastustellimus või valige tagastustellimus loendist, et avada vorm **Tagastustellimus – RMA-kood: %1, %2**.

3.  Klõpsake valikut **Otsi müügitellimust**, kui soovite tuvastada tagastatud kauba müügitellimuse. Täitke vorm **Otsi müügitellimust** ja klõpsake seejärel **OK**, et vorm sulgeda ja naasta vormile **Tagastustellimus – RMA-kood: %1, %2**. Tagastatud kauba müügitellimuse rida kopeeritakse tagastustellimusse.

4.  klõpsake vormi **Loo müügitellimus** avamiseks valikut **Asendustellimus**.

5.  Märkige ruut **Kopeeri tagastustellimuse read**, et kanda üle üksikasjad tagastustellimuselt, mille te selle müügitellimuse juurde vormil **Tagastustellimus – RMA number: %1, %2** valisite.

6.  Sisestage või muutke üksikasju vastavalt vajadusele.
    
    Kui tuvastasite müügitellimuse 3. etapis ja kui tagastatud kauba müügitellimuse rida on lingitud müügilepinguga, kuvatakse väljal **Müügilepingu ID** automaatselt kauba asendustellimuse kehtiva müügilepingu identifikaator.

7.  Klõpsake **OK**, et sulgeda vorm **Müügitellimuse loomine**, ja avage vorm **Müügitellimus**, kus saate jätkata uue müügitellimuse teabe sisestamist. Mis tahes kehtiva tagastustellimuse read kopeeritakse uude müügitellimusse. 
    
    Kui müügilepingu identifikaator kuvatakse automaatselt väljal **Müügilepingu ID**, siis on müügileping kauba asendustellimuse puhul müügitellimuse päisega lingitud. Kui müügilepingus on kehtiv kohustus, mis pole veel täidetud, ja müügitellimus luuakse enne müügilepingu aegumist, luuakse müügilepingu ja müügitellimuse ridade vahel link. Seetõttu kopeeritakse müügilepingu teave, nagu kaubahind, uuele müügitellimuse reale. 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]