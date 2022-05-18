---
title: Teenusetellimusele aadressi lisamine
description: Teemas kirjeldatakse, kuidas lisada teenusetellimusele kliendi aadressi.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 560d0c58aebe652e668cc0ec3ed05d84f004872e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672874"
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