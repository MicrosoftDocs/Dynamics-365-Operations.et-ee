---
title: Suhtelise tee kasutamine ER-mudelite ja -vormingute andmesidemetes
description: Elektrooniline aruandluse tööriist võimaldab teil määratleda elektroonilise vormingu struktuurid ja seejärel kirjeldada, kuidas neid struktuure tuleb täita.
author: kfend
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 54fb7d488dff1ad36e2d44b8bb9e0fa3fce7ea1b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276558"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Suhtelise tee kasutamine ER-mudelite ja -vormingute andmesidemetes

[!include[banner](../includes/banner.md)]

Elektrooniline aruandluse (ER) tööriist võimaldab kasutajatel määratleda elektroonilise vormingu struktuurid ja seejärel kirjeldada, kuidas neid struktuure tuleb täita, kasutades rakenduses olemasolevaid andmeid ja algoritme. Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) konfiguratsioonide loomine](electronic-reporting-configuration.md). Finantside ja toimingute andmete toomiseks ning selle abil elektroonilise dokumendi loomiseks andmevoo määramiseks peate tegema järgmist:

- Siduda konfigureeritud andmeallikad kujundatud domeenikohase andmemudeli elementidega. Mudeli struktuur ja valitud andmeallikad võivad olla osa keerukast hierarhilisest struktuurist. Selle tõttu võivad lõplikud sidumised olla üsna suured ja sisaldada mitut erinevat tüüpi elemente (nt seosed, tabelid ja meetodid). Sidumised võivad muutuda kehvemini loetavaks ning nende ülevaatamine ja mõistmine võib muutuda üsna keeruliseks, eriti mitteomanike jaoks. 
- Siduge andmemudeli elemendid vormingu komponentidega, et määratleda, millised andmed sisestatakse andmemudelist loodud vormingu väljundisse.

ER-i vastenduse kujundaja kasutatavuse parandamiseks on loodud [suhtelise teekonna](er-formula-language.md#relative-path) funktsioon. Vaikimisi on suhteline tee esitussuvand sisse lülitatud rakenduse mis tahes uue eksemplari jaoks, kus ER-i kujunduskogemus on lubatud (Microsoft Dynamics 365 Finantsid, Microsoft Regulatory Configuration Service). Rakendasime suhtelise tee parameetri, et kasutajad saaksid selle ER-i sidumise esitlusega töötades jätkata täieliku tee kasutamist.

[![Kasutaja parameetrid.](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Kui suhtelise tee kasutusparameeter on sisse lülitatud, asendab üks @-märk praeguse mudeli elemendi sidumisel tee emaüksuseni. Kogu sidumise tee muutub lühemaks, mis muudab kogu vastendamise ilmsemaks ja kergemini mõistetavaks. Enamasti ei ole ER-i kujundajas vaja kõigi andmemudelite sidumiste kuvamiseks täiendavat kerimist.

[![Mudelivastenduse kujundaja.](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Uue ER-i avaldise kujundamise alustamisel tuleb sisestada ainult üks märk, et määratleda seos emaüksuse väljaga.

[![Valemikoostaja.](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Kui otsustate muuta emamudeli üksuse andmeallikat absoluutse teekasutusega, peate selle mudelkauba ja kõik pesastatud üksused uue andmeallikaga käsitsi uuesti siduma. Kui suhtelise tee kasutamine on sisse lülitatud ja te valite emaüksusele sidumiseks uue andmeallika, pakutakse teile valikut kõik selle emaüksuse pesastatud üksused automaatselt ühe klõpsuga uuesti siduda.

[![Olemasoleva tee asendamise teade.](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Kui kinnitate pesastatud üksuste uuesti sidumise, paigutatakse uus emaüksus igale olemasolevat emaüksust sisaldava pesastatud üksuse teele.
See funktsioon ei lõhu ER-i raamistiku tagasiühilduvust. Selle uue funktsiooniga töötavad kõik varem kavandatud ER-i konfiguratsioonid ja värskendusi ega teisendusi pole vaja.

> [!NOTE]
> Kõik muudatused, mis kaasnevad pesastatud elementide sidumise massilise muutmisega mudelivastendustes, salvestatakse õigesti konfiguratsiooni deltas (muutuste jälg). See võimaldab klientidel muuta nende mudelivastenduste tuletatud versiooni aluse mis tahes uuele alusversioonile, mida on selle uue funktsiooniga muudetud.

## <a name="additional-resources"></a>Lisaressursid

[ER-i valemi keel](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

