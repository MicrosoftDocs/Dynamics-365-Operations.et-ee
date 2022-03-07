---
title: Dokumentide printimise ülevaade
description: Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil. See artikkel annab ülevaate dokumentide printimisest.
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c349e50826aa577ce6a3b8a68676d549f7fed1b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564401"
---
# <a name="document-printing-overview"></a>Dokumentide printimise ülevaade

[!include [banner](../includes/banner.md)]

Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil. See artikkel annab ülevaate dokumentide printimisest.

## <a name="printing-overview"></a>Printimise ülevaade

Rakendus pakub integreeritud teenuseid ja klientrakendusi, mis võimaldavad hõlpsalt luua, salvestada ning levitada äritegevust toetavaid dokumente. Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil. Peale selle saate eksportida lehti ja aruandeid otse kliendist kas PDF-failide või Microsoft Office’i dokumentidena. Lõpuks võimaldab jaotatud töökoormus teil printida äridokumente otse mobiilsest seadmest, kasutades võrguressursse. Kuigi printimisnõuded võivad erineda, peavad kõik valdkonnad tavaliselt äridokumentidest rakenduse abil looma paberdokumendid. Dokumentide printimine võrgusseadmetes hostitud rakendustest toob kaasa ainulaadsed probleemid. Järgmisena on toodud mõned näited.

- Printeridraiverid ei pruugi kasutaja seadmes saadaval olla.
- Kasutaja seade ei pruugi olla ettevõtte võrguga ühendatud.

Spetsiaalse hosti abil ja paari lihtsat etappi järgides saavad süsteemiadministraatorid konfigureerida juurutusi, mis võimaldavad kasutajatel printida võrguseadmetes otse ärirakendustest.

### <a name="application-printing-scenarios"></a>Rakenduse printimise stsenaariumid 

Järgmine tabel kirjeldab kolme esmase printimise stsenaariumi.

| Stsenaarium                        | Eesmärk                                                      | Lahendus |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Kuvatava printimine        | Saate printida seda, mida praegu brauseris kuvatakse.             | Brauseris luuakse veebilehe prinditav versioon. |
| 2. Interaktiivne printimine         | Saate printida täppisdokumendi kohalikult ühendatud seadmest. | Saate eksportida aruande PDF-versiooni ja selle brauseris alla laadida. |
| 3. Printimine võrgusseadmes | Saate saata täppisdokumendi domeeni printerisse.     | Täppisdokument saadetakse klientrakendusele, mis töötab kliendi domeenis hostitavas serveris. |

Kuna lahendused on erinevad olenevalt stsenaariumist, pakuvad rakendused sisseehitatud teenuseid ja tööriistu, mis aitavad kasutajatel saavutada oma eesmärke:

- **1. stsenaariumi** toetab HTML5 kliendi brauseri renderdus.
- **2. stsenaarium** kasutab klientrakendusi ja Microsoft 365 teenuseid.
- **3. stsenaarium** nõuab tuge klientrakendustest ja teenustest, mida hostitakse Microsoft Azure’is.

Lisaks platvormile, mis juurutatakse Azure’i tellimusse, pakuvad Finance and Operationsi rakendused klientidele integreeritud, esimese osapoole Azure’i rakendust, mis aitab neil printimiseks hõlpsamalt kasutada domeenis hostitud seadmeid.

## <a name="service-overview"></a>Hoolduse ülevaade
Ajal, mil hostitud rakenduste loodud dokmendid ootavad printimist võrku ühendatud seadmes, talletatakse neid Azure’i bloobimälus. [Dokumendi marsruudivaliku agendi installimine võrguprintimise lubamiseks](install-document-routing-agent.md) kasutab Azure’i autentimist, et luua turvaline kanal Azure’i teenustega.

**Käivitamisjärjekord**

1. Teenus Microsoft SQL Server Reporting Services (SSRS) loob aruande, mis talletatakse Azure’i bloobimälus. Seotud printerisätteid talletatakse koos dokumendiga.
2. Dokumendi marsruudivaliku agent esitab Azure’i teenusesiini järjekorda aktiivsete tööde päringu.
3. Dokumendi marsruudivaliku agent laadib dokumendi alla ja spuulib selle võrguprinterisse.

Kliendipõhine lahendus võimaldab klientidel hallata oma printimisvajaduste ulatust. Kliendid, kellel on suuremahulised printimise töökoormused, saavad installida mitu dokumendi marsruudivaliku agenti, et suurendada samaaegsete printimistoimingute arvu. Samuti võib mõnel kliendil olla vajalik ainult väga väheste dokumendi marsruudivaliku agentide installimine, et täita nende printimisvajadusi.

### <a name="service-components-for-network-printing"></a>Võrguprintimise teenusekomponendid

Järgmisel diagrammil on näidatud põhikomponendid, mis toetavad võrguprintimise toiminguid.

[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Pange tähele, et ühe printeri juurde saab registreerida mitu dokumendi marsruudivaliku agenti. Printimiseelistuste lahendamiseks kasutab hostitud teenus võrguteed, mis tuvastab kordumatult iga võrguprinteri. Sellest tulenevalt kuvatakse printer ka siis, kui selle on registreerinud mitu klienti, rakenduste saadaolevate printerite loendis ühe valikuna.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]