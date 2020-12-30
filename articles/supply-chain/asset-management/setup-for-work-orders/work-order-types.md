---
title: Töökäsu tüübid
description: Selles teemas selgitatakse töökäskude tüüpe varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e43908e3f13c9e4fd6fab6f1e17a171866b803
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426362"
---
# <a name="work-order-types"></a>Töökäsu tüübid

[!include [banner](../../includes/banner.md)]

 

Töötellimuse tüüpe kasutatakse töötellimuste kategoriseerimiseks. Näiteks võivad teil olla töökäsud, mis on seotud ennetava hoolduse või parandava hooldusega.

Töökäsu tüüp määratleb alluvuse töökäsu elutsükli mudeliga. Töökäsu elutsükli mudel määratleb töökäsu elutsükli olekud, mida saab seadistada töökäsule. (Töökäsu elutsükli oleku näideteks on **Loodud**,**Töös** ja **Lõpetatud**.)

Lisateavet töökäsu elutsükli olekute ja projekti etappide kohta vt [Töökäsu elutsükli olekud](work-order-lifecycle-states.md).

1. Valige **Varahaldus**\>**Seadistus**\>**Töökäsud** \>**Töökäskude tüübid**.
2. Valige uue töökäsu loomiseks **Uus**.
3. Sisestage väljale **Töökäsu tüüp** töökäsu tüübi ID.
4. Väljale **Nimi** sisestage nimi.
5. Valige väljal **Töökäsu töötsükli mudel** töötsükli mudel.
5. Seadistage suvand **Üks hooldustöötaja** valikule **Jah**, kui kõik töökäskude tööd, mis on seotud selle tüübi töökäsu, tuleb planeerida samale hooldustöötajale.
6. Valige väljal **Kulu tüüp** vastavalt **Korrigeeriv**, **Ennetav** või **Investeering**. Kõigil töökäskude töödel peab olema sama kulutüüp.
7. Määrake jaotises **Kohustuslik** asjakohased valikud kui **Jah**, et määrata, milline tõrkega seotud või hoolduse seisakuga seotud teave lisatakse seda tüüpi töökäsule.

    > [!NOTE]
    > Jaotise **Kohustuslik** valikud on seotud valikutega FastTabil **Kinnita** leheküljel **Töökäskude töötsüklite olekud** (**Varahaldus**\> **Seadistus** \> **Töökäsud**\> **Töötsükli olekud).**

8. Valige käsk **Salvesta**.

![Töökäsu tüübid](media/16-setup-for-work-orders.png)
