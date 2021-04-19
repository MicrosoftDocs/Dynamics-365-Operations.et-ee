---
title: Teenusetellimusele aadressi lisamine
description: Teemas kirjeldatakse, kuidas lisada teenusetellimusele kliendi aadressi.
author: ShylaThompson
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a54ec439fc88dc9688bbb3d6b833b5d80482f024
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824650"
---
# <a name="add-an-address-to-a-service-order"></a>Teenusetellimusele aadressi lisamine    

[!include [banner](../includes/banner.md)]


Teemas kirjeldatakse, kuidas lisada teenusetellimusele kliendi aadressi. Teenustellimuse loomisel edastatakse aadressiteave projektilt, millele on lisatud teenustellimus. Siiski saate valida alternatiivse asukoha klientide, hankijate, laoalade, ladude, teenusetellimuste ja projektide aadresside hulgast, mis on juba rakendusse Microsoft Dynamics AX sisestatud.

Saate ka luua uue aadressi. Vaikimisi kantakse uus aadress projekti üle. Siiski saate määrata, et uus aadress on asjakohane vaid teenuse selle eksemplari jaoks. Sel juhul ei kanta uut aadressi projekti üle.

## <a name="create-a-customer-address-for-a-service-order"></a>Kliendi aadressi loomine teenusetellimuse jaoks

Teenusetellimusele aadressi lisamiseks tehke järgmist.

1.  Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.

2.  Avage teenusetellimus, mille jaoks soovite aadressi luua.

3.  Klõpsake **tegumiribal** käsku **Redigeeri** ja seejärel valikut **Päisevaade**.

4.  Klõpsake kiirkaardil **Aadress** käsku **Lisa aadress**.

5.  Sisestage vormil **Uus aadress** aadressi jaoks kordumatu nimi ja täitke ülejäänud väljad. 
    

    > [!WARNING]
    > <P>Kui sisestate olemasoleva aadressi nime, kirjutab ülejäänud väljadele sisestatud teave üle olemasoleva aadressi teabe.</P>


6.  Klõpsake **OK**, et kopeerida uus aadress teenusetellimusse.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Teenustellimusele muu aadressi määramine

Teenusetellimusele alternatiivse aadressi lisamiseks tehke järgmist.

1.  Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.

2.  Avage teenusetellimus, mille jaoks soovite alternatiivse aadressi sisestada.

3.  Klõpsake **tegumiribal** käsku **Redigeeri** ja seejärel valikut **Päisevaade**.

4.  Klõpsake kiirkaardil **Aadress** käsku **Muu aadress**.

5.  Valige vormi **Aadressi valik** väljal **Kirje tüüp** suvand **Hooldustellimused**.

6.  Valige aadress ja klõpsake **OK**, et kopeerida see teenusetellimusse.


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]