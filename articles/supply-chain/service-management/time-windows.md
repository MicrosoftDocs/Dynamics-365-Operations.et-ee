---
title: Kellaaja aknad
description: Hooldustellimuse ridade planeerimise optimeerimiseks saate kasutada kellaaja aknaid.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d79e3d3756b8dc402d6f293437209b2e108be38e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426418"
---
# <a name="time-windows"></a>Kellaaja aknad  

[!include [banner](../includes/banner.md)]

Hooldustellimuse ridade planeerimise optimeerimiseks saate kasutada kellaaja aknaid. Süsteemi saate seadistada nii, et see loob hooldustellimusi automaatselt. Kellaaja aknas määratud kriteeriumite põhjal saate võimalikult palju hooldustellimuse ridu ühendada võimalikult väheste hooldustellimustega.

Ajaaken määrab, kui kaugele hooldustellimus saab oma arvutatud kuupäeva suhtes liikuda. Arvutatud kuupäev on kuupäev, millal hooldustellimuse rida oli plaanitud toimuma. Kuupäev põhineb selle intervallisättel ning hooldusperioodil, mille määrasite lehel **Hooldustellimuste loomine**. Kellaaja akna määrate järgmises tabelis olevaid väärtusi kasutades.

| Meetod | Kirjeldus                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nädal   | Kuupäev, mil hooldustellimuse rida saab liigutada igale esialgse arvutatud päevaga sama nädala vabale päevale.                                                                                                                                                                                    |
| Kuu  | Kuupäev, mil hooldustellimuse rida saab liigutada igale esialgse arvutatud päevaga sama kuu vabale päevale. Hooldustellimuse rea arvutatud kuupäev on näiteks 15. veebruar 2017. Hooldustellimuse rida saab planeerida igale nädalapäevale vahemikus 1. veebruar ja 28. veebruar 2017. |
| Käsitsi | Te määrate maksimaalse päevade arvu selle järgi, kui palju enne või pärast esialgset arvutatud kuupäeva hooldustellimuse rida liigutada tohib.                                                                                                                                                                           |

Kui hooldusleppe rea jaoks ei ole kellaaja akent määratud, tuleb hooldusleppest tulenev hooldustellimuse rida teostada sellel kuupäeval, millele see oli esialgselt planeeritud.

## <a name="related-topics"></a>Seotud teemad

[Kellaaja akende loomine](create-time-windows.md)

