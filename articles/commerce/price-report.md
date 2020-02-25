---
title: Jaemüügihinna aruanded
description: Selles teemas antakse ülevaade hinnaaruande funktsioonist, mida saab kasutada tootesortimendi puhul tulevaste hinnamuutuste kuvamiseks.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 91c0a96abdd7df9e85e63ca6b1b47a57f3f401eb
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022306"
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
