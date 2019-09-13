---
title: Hange
description: Selles teemas selgitatakse hanget varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875607"
---
# <a name="procurement"></a>Hange


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varahalduses saate ülevaate ostutaotluste ja ostutellimustega seotud töötellimuste kohta. Samuti on võimalik luua ostutellimus või ostutaotlus töötellimusest.

Loendis **Töökäsu ostutaotlus** (**Varahaldus** > **Tavaline** > **Hange** > **Töökäsu ostutaotlus**) näete töökäskudega seotud ostutaotlusi.

- Valige töökäsu töö **Töökäsu ostutaotlus** ja klõpsake **Ostutaotlus**, et avada seotud ostutaotlusi.  
- Valige töökäsu töö loendist **Töökäsu ostutaotlus** ja klõpsake **Töökäsk**, et avada seotud töökäske.  
- Valige töötellimuse töö loendist **Töökäsu ostutaotlus** ja klõpsake **Kaup, kus kasutatakse** nuppu, kui soovite saada ülevaate, kus valitud real olevat kaupa kasutatakse varahalduses seoses varade, hooldustöö tüübi vaikeväärtuste, varuosade ja töökorraldustega. 

![Joonis 1](media/08-work-orders.png)


Loendis **Töökäsu ostmine** (**Ettevõtte varahaldus** > **Tavaline** > **Hange** > **Töökäsu ostmine**) näete töökäskudega seotud ostutellimusi.

- Valige töökäsu töö loendist **Töökäsu ostutaotlus** ja klõpsake **Ostutellimus**, et avada seotud ostutellimusi.  
- Valige töökäsu töö loendist **Töökäsu ostutaotlus** ja klõpsake **Töökäsk**, et avada seotud töökäske.  
- Valige töötellimuse töö ostmise loendist **Töökäsu ostutaotlus** ja klõpsake **Kaup, kus kasutatakse** nuppu, kui soovite saada ülevaate, kus valitud real olevat kaupa kasutatakse varahalduses seoses varade, hooldustöö tüübi vaikeväärtuste, varuosade ja töökorraldustega. 

![Joonis 2](media/09-work-orders.png)


Ülaltoodud loendites paigutatakse tarnekuupäeva kontrolliga seotud ikoon igale reale paremale. Kui ikoon kuvab punases ringis hüüumärgi, tähendab see, et seotud ostutaotluse või ostutellimuse tarne võib edasi lükata.

Ostutellimuse puhul leitakse võimaliku viivituse arvutamiseks kasutatav kuupäev vormil **Ostutaotlused** > **Ostutellimuse päis** FastTab > **Nõutud kuupäeva** väljal. Seda kuupäeva võrreldakse töökäsu või töökäsu töö vaba kuupäevaga samal viisil nagu ostutellimuse kuupäeva.

Ostutellimuse puhul on võimaliku viivituse arvutamiseks kasutatav kuupäev ostutellimuse reaga seotud kuupäev, mis on näidatud vormil **Ostutellimus** > valige ostutellimuse rida > **Rea üksikasjad** FastTab > vahekaart **Seadistus** > **KInnitatud tarnekuupäev** väljal. Kui see väli ei ole täidetud, kasutatakse kuupäeva väljal **Tarnekuupäev** **Ostutellimuse** päises FastTab. Ühte neist kuupäevadest võrreldakse töökäsu või töökäsu töö vaba kuupäevaga järgneval viisil:

- Töötellimuse tegelik alguskuupäev või  

- Seotud töötellimuse töö planeeritud alguskuupäev või  

- Töötellimuse planeeritud alguskuupäev või  

- Töötellimuse eeldatav alguskuupäev või  


## <a name="create-purchase-order-from-a-work-order"></a>Ostutellimuse loomine töökäsu põhjal

**Kõigi töötellimuste**puhul saate valida töökäsu töö ja luua seotud ostutellimuse või ostutaotluse. Seda tehakse selleks, et tagada ostutellimuse või ostutaotluse ja töökäsu vaheline projekti seos.

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige loendis **Kõik töökäsud** või **Aktiivsed töökäsud** töötellimus, mille jaoks soovite ostutellimuse luua, ja klõpsake nuppu **Redigeeri.**

3. **Töökäsu** vormil > **Töökäsu hooldustööd** FastTab valige töökäsu töö, mille jaoks soovite ostutellimuse luua.

4. Klõpsake **Kauba ülesanded** > **Ostutellimus töökäsu tööst**.

5. Klõpsake loendi **Projekti ostutellimused** lehel käsku **Uus.**

6. Loo ostutellimus.

>[!NOTE]
>Ostutaotluse loomine on ostutellimuse loomisega peaaegu identne. Ainus erinevus on, et ülaltoodud protseduuri puhul klõpsate käsku **Kauba ülesanded** > **Ostutaotlus töökäskude tööst** sammul 2.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Töökäsku ja ostutellimuse või ostutaotluse vaheline projekti seos

Ostutellimuse rida või ostutaotluse rida on seotud töökäsu tööga töökäsu projekti ja seotud projekti tegevuse numbri kaudu. Kui loote ostutellimuse või ostutaotluse töökäsu tööst, on seotud projekti tegevuse number kohustuslik. Projekti tegevuse number sisestatakse ostutellimusele või ostutaotlusele automaatselt, kui sellega seotud töökäsk sisaldab töökäsu töid, mis kõik kasutavad sama hooldustööde tüüpi. Kui töökäsu tööd sisaldavad erinevaid hooldustööde tüüpe, tuleb projekti tegevuse number käsitsi sisestada.

Ostutellimuse reaga seotud tegevuse numbri vaatamiseks või sisestamiseks avage **töökäsu ostmine** > valige ostutellimuse kirje > klõpsake ostutellimusele veerus **Ostutellimus** > **Rea üksikasjad** FastTab > vahekaardi **Projekt** > väljal **Tegevuse number**.


![Joonis 3](media/10-work-orders.png)


Samal viisil avage töökäsu ostutaotluse reaga seotud tegevuse numbri vaatamiseks või sisestamiseks **Töökäsu ostutaotlus** > valige ostutaotluse kirje > klõpsake ostutaotlusele veerus **Ostutaotlus** > **Rea üksikasjad** FastTab > vahekaardi **Projekt** > väljal **Tegevuse number**.

