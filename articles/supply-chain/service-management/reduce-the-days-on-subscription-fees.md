---
title: Kordustellimuste tasude päevade vähendamine
description: Olemasoleva kordustellimuse tasu päevade arvu vähendamiseks saate luua uue kande, milles eemaldate ajaperioodi, mis ei pea enam olema kordustellimuse tasu intervalli osa.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae2486d08e89c06d76ab9945ccce25c5e97f1500
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010557"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Kordustellimuste tasude päevade vähendamine 

[!include [banner](../includes/banner.md)]


Olemasoleva kordustellimuse tasu päevade arvu vähendamiseks saate luua uue kande, milles eemaldate ajaperioodi, mis ei pea enam olema kordustellimuse tasu intervalli osa.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Päevade vähendamine kordustellimuse tasul

1.  Klõpsake valikuid **Teenuste haldus** \> **Üldine** \> **Teenuse kordustellimused** \> **Kõik teenuse kordustellimused**. Valige teenuse tellimus ja klõpsake tegevuspaanil nuppu **Kordustellimuse tasud**

2.  Valige väljas **Kordustellimuse tüüp** suvand **Vähendamispäevad**.

3.  Kasutage välja **Alates kuupäevast** ja välju **Lõppkuupäev** kordustellimuse tasu kuupäevade vahemiku määratlemiseks, mida soovite kordustellimuse tasu perioodist eemaldada, ja klõpsake siis nuppu **OK**.

Loodud kande vaatamiseks klõpsake välja **Kordustellimus** ja seejärel välja **Tasukanded**.

## <a name="example"></a>Näide

Kui kordustellimuse kande periood kestab 1. jaanuarist 31. jaanuarini ja te soovite perioodi vähendada 10 päeva võrra, looge uus kanne, milles vähendamisperiood kestab 1. jaanuarist 10. jaanuarini. (Vähendamisperiood võib olla ka 5. jaanuarist 15. jaanuarini või muu kümnepäevane periood.)

Kui väljal **Alates kuupäevast** on vähendusperiood 21. jaanuar (31 miinus 10), saate seadistada välja **Lõppkuupäev** mis tahes kuupäevani pärast 31. jaanuari, kuid tasukandest eemaldatakse ikka 10 päeva.

## <a name="see-also"></a>Vt ka

[Vähendamispäevade näide](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]