---
title: Hooldustellimuste loomine automaatselt
description: Saate luua hoolduslepingutel põhinevaid hooldustellimusi hoolduslepingu kehtivusperioodiks.
author: kamaybac
ms.date: 05/01/2018
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
ms.openlocfilehash: 1acf4620556fe7ec5ae40f0a98b0a23602e2524a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565133"
---
# <a name="automatically-create-service-orders"></a>Hooldustellimuste loomine automaatselt 

[!include [banner](../includes/banner.md)]


Saate luua hoolduslepingutel põhinevaid hooldustellimusi hoolduslepingu kehtivusperioodiks.

Hoolduslepingust loodavad hooldustellimused lisatakse kõik hoolduslepingule.

Teenusetellimused luuakse automaatselt järgmistest sätetest:

  - Hoolduslepingu intervall, mis on hoolduslepingu ridadel seadistatud. Hoolduslepingu intervall näitab hooldustellimuste ridade loomist sagedust. Lisateavet vaadake jaotisest [Hooldusintervallid](service-intervals.md).

  - Periood, mille määratlete hooldusperioodi määramiseks väljadel **Alates kuupäevast** ja **Kuupäevani** vormil **Hooldustellimuste loomine**. Lisateavet vaadake jaotisest [Hooldustellimuste loomine automaatselt](create-service-orders-automatically.md)

  - Suvand **Hooldustellimuste ühendamine** hooldusleppe päises. See suvand määrab, kas hooldustellimuse read luuakse hoolduslepingu alusel ja mis ühendab hooldustellimused lähtuvalt töötajast, hooldustoimingust, hooldusobjektist või hoolduslepingust. Lisateavet vaadake jaotisest [Hooldustellimuste ühendamine](combine-service-orders.md).

  - Hoolduslepingu real olev suvand **Kellaaja aken**. Kellaaja aken määrab, kui kaugele saab hooldustellimus liikuda oma arvutatud kuupäeva suhtes. Lisateavet vaadake jaotisest [Kellaaja aknad](time-windows.md).


> [!NOTE]
> <P>Kui hooldustellimuse jaoks määratletud päev ei ole avatuna kalendris, mille valisite vormil <STRONG>Teenuste halduse parameetrid</STRONG>, kuvatakse teade kalendri konflikti kohta. Seda teadet võite ohutult eirata ning hooldustellimus luuakse ikkagi, kuigi kuupäev on kalendris suletud.</P>

## <a name="example-1"></a>Näide 1

Hooldusleping kestab 1. jaanuarist 2012 kuni 31. detsembrini 2012. Kui määratlete vormil **Hooldustellimuste loomine** hooldusperioodiks ajavahemiku 1. novembrist 2012 kuni 1. veebruarini 2013, siis luuakse hooldustellimusi ajavahemikus 1. novembrist 2012 kuni 31. detsembrini 2012.

## <a name="example-2"></a>Näide 2

Hooldusleping kestab 1. jaanuarist 2012 kuni 31. detsembrini 2012. Hoolduslepingule lisatakse kaks hoolduslepingu rida. Esimesel hoolduslepingu real on alguskuupäev 2. jaanuar 2012 ja lõppkuupäev 1. märts 2012. Teisel hoolduslepingu real on alguskuupäev 1. aprill 2012 ja lõppkuupäev 31. detsember 2012. Te määrate vormil **Hooldustellimuste loomine** perioodi, mis on ajavahemikus 1. oktoober 2012 kuni 31. detsember 2012. Seetõttu luuakse hooldustellimused ainult teisele lepingureale, sest esimese lepingurea alguskuupäev ja lõppkuupäev on enne hooldustellimuse perioodi, mille määratlesite.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]