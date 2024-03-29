---
title: Kellaaja aknad
description: Hooldustellimuse ridade planeerimise optimeerimiseks saate kasutada kellaaja aknaid.
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccbb9cf71ff1df7aa336deb5bf9d7dacb8004134
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862391"
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

## <a name="related-articles"></a>Seotud artiklid

[Kellaaja akende loomine](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]