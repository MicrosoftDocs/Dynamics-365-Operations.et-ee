---
title: Ladude seadistamine üleviimistellimuste jaoks
description: Selles teemas kirjeldatakse ladude seadistamist üleviimistellimuste jaoks.
author: Mirzaab
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 9e4ea0f9720bd4e5d2724b507aa32525ac25fa52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823211"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Ladude seadistamine üleviimistellimuste jaoks 

[!include [banner](../includes/banner.md)]

Ladudevahelisi üleviimistellimusi toetava hierarhia loomiseks saate kasutada laotasemeid. Tuginedes sellele sättele, arvutab koondplaneerimine välja iga laotaseme kaubavajadused ning loob määratud lähtelaole plaanitud tellimusi nende täitmiseks.

1.  Klõpsake valikuid **Varude haldus > Seadistus > Laovarude jaotamine > Laod**.

2.  Valige ladu, mille soovite uuesti täita.

3.  Märkige kiirkaardil **Koondplaneerimine** ruut **Taastäitmine**.

4.  Valige väljal **Pealadu** ladu, mille soovite määrata taastäitmislaoks. Koondplaneerimine arvutab välja valitud lao üleviimisvajadused ja loob väljal **Pealadu** valitud pealaole plaanitud üleviimistellimuse.
   
    > [!NOTE]
    > <P>Kui jätate ruudu <STRONG>Taastäitmine</STRONG> tühjaks, määratakse valitud laole laotase vastavalt väärtusele <STRONG>Pealadu</STRONG>, kuid <STRONG>Pealadu</STRONG> ei seadistata taastäitmislaona.</P>

5.  Uue seadistuse rakendamiseks sulgege leht.


> [!TIP]
> <P>Kui soovite määrata taastäitmiseks lao, peate lao lehel <STRONG>Varude dimensioonid seadistama</STRONG> varude dimensioonina. Sellel lehel valige lao puhul väli <STRONG>Aktiivne</STRONG> ja väli <STRONG>Laovarude planeerimine dimensioonide kaupa</STRONG>.</P>

## <a name="set-up-transport-lead-time"></a>Transpordi täitmisaja seadistamine

Peate ka seadistama transpordi täitmisaja ladude vahel lehel **Transpordipäevad**. 
1. Minge jaotisse **Varude haldus > Seadistus > Jaotus > Transpordipäevad**.
2. Valige väljal **Vastuvõtupunkt** säte **ladu**.
3. Valige **Lähetav ladu**, **Vastuvõttev ladu** ja **Transpordi päevas**. 
4. (Valikuline) Saate määrata ka tarneviisist oleneva transpordiaja vahekaardil **Transpordipäevi tarneviisi kohta**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]