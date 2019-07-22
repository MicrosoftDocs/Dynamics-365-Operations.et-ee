---
title: Suhtelise tee kasutamine ER-mudelite ja -vormingute andmesidemetes
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6582cca9b912868f88de2770a17cbb6e67328660
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726548"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Suhtelise tee kasutamine ER-mudelite ja -vormingute andmesidemetes

[!include[banner](../includes/banner.md)]

Elektrooniline aruandluse (ER) tööriist võimaldab kasutajatel määratleda elektroonilise vormingu struktuurid ja seejärel kirjeldada, kuidas neid struktuure tuleb täita, kasutades rakenduses Dynamics 365 for Finance and Operations olemasolevaid andmeid ja algoritme. Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) konfiguratsioonide loomine](electronic-reporting-configuration.md). Andmevoo määramiseks rakenduse Finance and Operations andmete toomiseks ja selle kasutamiseks elektrooniliste dokumentide loomisel, tuleb teha järgmist.

- Siduda konfigureeritud andmeallikad kujundatud domeenikohase andmemudeli elementidega. Mudeli struktuur ja valitud andmeallikad võivad olla osa keerukast hierarhilisest struktuurist. Selle tõttu võivad lõplikud sidumised olla üsna suured ja sisaldada mitut erinevat tüüpi elemente (nt seosed, tabelid ja meetodid). Sidumised võivad muutuda kehvemini loetavaks ning nende ülevaatamine ja mõistmine võib muutuda üsna keeruliseks, eriti mitteomanike jaoks. 
- Siduge andmemudeli elemendid vormingu komponentidega, et määratleda, millised andmed sisestatakse andmemudelist loodud vormingu väljundisse.

ER-i vastenduse kujundaja kasutatavuse parandamiseks on loodud suhtelise teekonna funktsioon. Vaikimisi on suhtelise tee esindatuse suvand sisse lülitatud kõigi rakenduse Finance and Operations uute eksemplaride jaoks, kus on lubatud ER-i kujundamise kogemus (Microsoft Dynamics 365 for Finance and operations, Microsoft Regulatory Configuration Service). Rakendasime suhtelise tee parameetri, et kasutajad saaksid selle ER-i sidumise esitlusega töötades jätkata täieliku tee kasutamist.

[![Kasutaja parameetrid](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Kui suhtelise tee kasutusparameeter on sisse lülitatud, asendab üks @-märk praeguse mudeli elemendi sidumisel tee emaüksuseni. Kogu sidumise tee muutub lühemaks, mis muudab kogu vastendamise ilmsemaks ja kergemini mõistetavaks. Enamasti ei ole ER-i kujundajas vaja kõigi andmemudelite sidumiste kuvamiseks täiendavat kerimist.

[![Mudelivastenduse kujundaja](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Uue ER-i avaldise kujundamise alustamisel tuleb sisestada ainult üks märk, et määratleda seos emaüksuse väljaga.

[![Valemikoostaja](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Kui otsustate muuta emamudeli üksuse andmeallikat absoluutse teekasutusega, peate selle mudelkauba ja kõik pesastatud üksused uue andmeallikaga käsitsi uuesti siduma. Kui suhtelise tee kasutamine on sisse lülitatud ja te valite emaüksusele sidumiseks uue andmeallika, pakutakse teile valikut kõik selle emaüksuse pesastatud üksused automaatselt ühe klõpsuga uuesti siduda.

[![Olemasoleva tee asendamise teade](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Kui kinnitate pesastatud üksuste uuesti sidumise, paigutatakse uus emaüksus igale olemasolevat emaüksust sisaldava pesastatud üksuse teele.
See funktsioon ei lõhu ER-i raamistiku tagasiühilduvust. Selle uue funktsiooniga töötavad kõik varem kavandatud ER-i konfiguratsioonid ja värskendusi ega teisendusi pole vaja.

> [!NOTE]
> Kõik muudatused, mis kaasnevad pesastatud elementide sidumise massilise muutmisega mudelivastendustes, salvestatakse õigesti konfiguratsiooni deltas (muutuste jälg). See võimaldab klientidel muuta nende mudelivastenduste tuletatud versiooni aluse mis tahes uuele alusversioonile, mida on selle uue funktsiooniga muudetud.
