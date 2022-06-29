---
title: Eelarvekohase ostutellimuse loomine
description: Kasutage seda protseduuri, et luua ostutellimus, mida kontrollitakse saadaoleva eelarve osas.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016184"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Eelarvekohase ostutellimuse loomine

[!include [banner](../../includes/banner.md)]

Kasutage seda protseduuri, et luua ostutellimus, mida kontrollitakse saadaoleva eelarve osas.

## <a name="review-the-budget-control-configuration"></a>Vaadake üle eelarve juhtimise konfiguratsioon

1. Minge eelarve **> eelarve > eelarve > konfiguratsiooni**.
1. Valige vahekaart **Saadaolevad eelarvefondid**.
1. Valige vahekaart **Dokumendid ja töölehed**.
1. Valige vahekaart **Eelarve juhtimise reeglite** määratlemine.
1. Valige vahekaart **Eelarvegruppide** määratlemine.
1. Sulgege leht.

## <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Minge kõigi **ostutellimuste > hanketellimuste > hankese**.
1. Valige suvand **Uus**.
1. Sisestage või valige väärtus väljale **Hankija konto**.
1. Suurendage vahekaarti **Üldine**.
1. **Seadke kuupäev väljal** Raamatupidamise kuupäev.
1. Dialoogi **sulgemiseks ja uue ostutellimuse avamiseks valige OK**.
1. Valige ostutellimuse **ridade kiirkaardil** tööriistaribalt rea lisamine, **et** lisada uus rida ja täitke seejärel rida, nagu on vaja kauba lisamiseks tellimusse.
1. Valige ostutellimuse **ridade kiirkaardi** tööriistaribal Finantside **jaotamissummad \>**.
1. **Määrake konto** väljal Pearaamatu konto.
1. Sulgege leht.

## <a name="perform-budget-checking"></a>Eelarve kontrollimine

1. Jätkake tööd ostutellimusega, mille jaoks äsja lisate rea.
1. Ostutellimuse ridade **kiirkaardi** tööriistaribal valige finantside **eelarve \> kontrollimine**.
1. Valige ostutellimuse **ridade kiirkaardi** tööriistaribal Finantside **eelarve kontrolli \> tõrked või hoiatused**.
1. Avaneb **eelarvekontrolli tõrgete ja hoiatuste** dialoog. Kontrollige tšeki tulemusi ja klõpsake dialoogi sulgemiseks **nuppu** Sule.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]