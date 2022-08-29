---
title: Jaemüügihinna aruanded
description: See artikkel annab ülevaate hinnaaruande funktsioonist, mida saab kasutada tootesortimendi eesolevate hinnamuutuste kuvamiseks.
author: ShalabhjainMSFT
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 09350d15660978126d36199a3b4e93f6be5fe157
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269023"
---
# <a name="retail-price-reports"></a>Jaemüügihinna aruanded

[!include [banner](includes/banner.md)]


Klientidele konkurentsivõimeliste hindade pakkumiseks muudavad jaemüüjad sageli toodete hinda. Kauplusejuhatajad soovivad hõlpsat juurdepääsu hiljutistele või tulevastele hinnamuutustele, et saaksid plaanida poeriiulitel olevate hinnasiltide värskendamiseks vajalikke ressursse. Rakenduse Retail versioonis 10.0 saab kaupluse juhataja avada aruande **Hind**, navigeerides jaotisse **Kõik kauplused \> Kauplus \> Hinnaaruanne** ja vaadates kauplusega seotud toodete värskendatud hindu. 

Hinnaaruande lubamiseks peab parameeter **Luba kaupluse hinnaaruanne** olema sisse lülitatud. See parameeter asub vahekaardil **Kaubanduse parameetrid \> Allahindlused \> Mitmesugust**. Lehe **Hinnaaruanne** avamisel kuvatakse dialoogiboks mitmesuguste konfiguratsioonidega. Allpool on loetletud saadaolevad konfiguratsioonid.

| Konfiguratsioon | Kirjeldus |
|---|---|
| Alguskuupäev/lõppkuupäev| Kuupäevavahemik, mille kohta tuleb hinnaaruanne luua. Kestus on praegu kuni 7 päeva. |
| Kanal| Kauplus, mille kohta tuleb hinnaaruanne luua. |
| Kuva tooted ja saadaolevad varud| Kui valite selle suvandi sätteks **Jah**, kuvatakse hinnad ainult nende toodete kohta, millel on kaupluses praegu füüsilised varud saadaval. |
| Kuva tootevariantide hinnad | Kui valite selle suvandi sätteks **Jah**, kuvatakse koos tooteetalonidega tootevariantide hinnad. See väli tuleks olekusse **Sees** lülitada ainult siis, kui teil on variandikohaseid hindu, kuna ridade arv muutub väga suureks. Tulevastes väljaannetes lubame dimensioonipõhised hinnad, nii et kaupluse juhataja saab valida dimensioonid, mille kohta hinnad tuleb kuvada. |
| Kuva hinnamuudatustega tooted | Kui valite selle suvandi sätteks **Jah**, kuvatakse hinnad ainult nende kuupäevade kohta, millal hind on muutunud. Hind *üks päev enne* valitud **alguskuupäeva** kuvatakse alati, nii et kaupluse juht saab hõlpsasti tuvastada tooted, mille hind pole kogu valitud ajaperioodi jooksul muutunud, ja kuvada ka praeguse hinna. |

Kui aruanne on loodud, saab selle Exceli failina alla laadida, et kasutada täiendavaid filtreerimisvalikuid. Hinnaaruannet saab kasutada ka toodete varasemate hindade kontrollimiseks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
