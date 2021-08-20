---
title: Parandushaldus
description: Grupeerige probleeme süstemaatiliselt nii, et see aitab pakkuda lahendusi, mis on minevikus edukad olnud.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa739685791596fe1a3dce3abff344b21b8d7f6dd5cefc525c7e749a75138a9b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774677"
---
# <a name="repair-management"></a>Parandushaldus       

[!include [banner](../includes/banner.md)]


Parandushalduse jaoks saate probleeme süstemaatiliselt grupeerida. See aitab pakkuda lahendusi, mis on minevikus edukad olnud.

Seadistage sümptomid, diagnoos ja lahenduse sätted. Kõiki neid saab rakendada, kui parandusse tuleb edaspidi samasugune kaup. Samuti saate seadistada paranduse etapid, ei saaksite jälgida parandustööde edenemist.

## <a name="setting-up-repair-management"></a>Parandushalduse seadistamine

Kasutage järgmisi seadistusvorme, et sisestada teavet, mida kasutatakse paranduse sümptomite, diagnoosi ja lahenduse määramiseks.

- **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Tingimused**.
- **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Sümptomialad**.
-  **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Diagnoosialad**.
- **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Lahendused**.
- **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Parandamise etapid**.

## <a name="symptoms-and-conditions"></a>Sümptomid ja tingimused

Sümptomid on see, kuidas klient probleemi kirjeldab. Sümptomid hõlmavad kliendi tähelepanekuid, mis viitavad parandamise vajadusele.

Saate seadistada sümptomite valdkonnad, sümptomite koodid ja tingimused. Sümptomite valdkond tähistab rikke piirkonda ja sümptomi kood tähistab rikke sümptomit. Tingimus kirjeldab olukorda või keskkonda, mis esineb probleemi tekkimisel.

**Näide**

Arvuti viiakse parandusse, kuna kasutamise tõttu pikema ajaperioodi jooksul kõvaketas ei tööta. Kõvaketta rike põhjustab sinise ekraaniga tõrke. Arvuti vastu võtnud tehnik sisestab järgmised sümptomid ja tingimused.

1.  Sümptomiala on kõvaketas

2.  Sümptomi kood on sinise ekraani tõrge

3.  Tingimus on, et kõvaketas ei tööta liiga pikaaegse kasutuse tõttu

## <a name="diagnosis-and-resolutions"></a>Diagnoos ja lahendused

Diagnoosi ja lahenduse väljad on paranduse seisukohalt väljendatud laused. Need on sammud, mis tehnik probleemi uurimiseks läbis.

Diagnoosi väli näitab operatsiooni, mis tuleb probleemi lahendamiseks sooritada. Diagnoosi kood näitab, kuidas probleemi käsitleti ja lahendus võib olla, et kaup parandati, asendati või tühistas klient tellimuse. Näiteks, kui arvuti on parandatud, võib diagnoosi väljal olla „defektne osa”, diagnoosi kood võib olla „uus videokaart installitud” ja lahendus võib olla „asendatud”.

## <a name="repair-stages"></a>Paranduse etapid

Paranduse etapid näitavad parandusprotsessi edenemist. Parandusetapil on lõpetamise parameeter **Lõpetatud**, mis näitab, et paranduse rida on lõpetatud ning lõpetamise kuupäev ja kellaaeg registreeritud.

## <a name="applying-repair-management"></a>Parandushalduse rakendamine

Parandushalduse rakendamiseks kauba suhtes tuleb kaubale teenustellimusel seadistada teenusobjekti seos. teenustellimusest saate seejärel luua parandusrea, mis sisaldab teavet antud probleemi kohta. Parandusreal määrate te teenusobjekti, mis on paranduses ja teabe sümptomite, diagnoosi ja täitmise kohta. Samuti saate luua parandusrea kohta märkuse.

Parandusrea saab luua parandusprotsessi iga sammu kohta.

## <a name="create-a-repair-line-on-a-service-order"></a>Parandusrea loomine teenustellimusele

1.  **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.

2.  Valige teenustellimus parandamist vajava teenusobjektiga.

3.  Valige **Paranda** \> **Parandusread**, et avada vorm **Parandusread**.

4.  Valige uue rea loomiseks **Uus**.

5.  Valige teenusobjekt. Saate valida ükskõik millise teenusobjekti, mis on teenustellimusel objektiseosena seadistatud.

6.  Valige ükskõik milline parandusreale vastav eelseadistatud sümptomi-, diagnoosi- ja täitmisväärtus ning kui vaja, valige vahekaart **Märkus**, et luua parandusreale märkus.

7.  Uue parandusrea salvestamiseks valige **Salvesta**. Välja **Loodud kuupäev ja kellaaeg** vormi **Parandusread** vahekaardil **Üldine** värskendatakse salvestamise ajal.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Edenemise jälgimine ja parandusprobleemi lahendamine

Saate paranduse edenemise jälgimiseks seadistada parandusrea parandusetapid.

Kui parandusprobleem on lahendatud, võite parandusrea sulgeda. Määrake parandusetapp etapile, kus atribuut **Lõpetatud** on lubatud. Lõpetamise ajaks registreeritakse reale praegune kuupäev ja kellaaeg.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Lahendatud probleemi parandusrea sulgemine

1.  Avage vorm **Parandusread**. Järgige käesolevas teemas eespool käsitletud parandusrea loomise protseduuri.

2.  Valige parandusrida koos parandusprobleemiga, mida soovite lõpetada.

3.  Väljas **Parandusetapp** valige etapp, millel on lubatud atribuut **Lõpetatud**.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]