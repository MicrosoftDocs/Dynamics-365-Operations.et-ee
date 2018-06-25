---
title: Parandushaldus
description: "Grupeerige probleeme süstemaatiliselt nii, et see aitab pakkuda lahendusi, mis on minevikus edukad olnud."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 937571968c6956ce3dba1427082b298983540f59
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="repair-management"></a>Parandushaldus       

[!include [banner](../includes/banner.md)]


Parandushalduse jaoks saate probleeme süstemaatiliselt grupeerida. See aitab pakkuda lahendusi, mis on minevikus edukad olnud.

Seadistage sümptomid, diagnoos ja lahenduse sätted. Kõiki neid saab rakendada, kui parandusse tuleb edaspidi samasugune kaup. Samuti saate seadistada paranduse etapid, ei saaksite jälgida parandustööde edenemist.

## <a name="setting-up-repair-management"></a>Parandushalduse seadistamine

Kasutage järgmisi seadistusvorme, et sisestada teavet, mida kasutatakse paranduse sümptomite, diagnoosi ja lahenduse määramiseks.

1.  Klõpsake valikuid **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Tingimused**.

2.  Klõpsake valikuid **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Sümptomialad**.

3.  Klõpsake valikuid **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Diagnoosialad**.

4.  Klõpsake valikuid **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Lahendused**.

5.  Klõpsake valikuid **Teenusehaldus** \> **Seadistamine** \> **Paranda** \> **Parandamise etapid**.

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

1.  Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.

2.  Valige teenustellimus parandamist vajava teenusobjektiga.

3.  Klõpsake valikuid **Paranda** \> **Parandusread**, et avada vorm **Parandusread**.

4.  Vajutage uue rea loomiseks klahve CTRL+N.

5.  Valige teenusobjekt. Saate valida ükskõik millise teenusobjekti, mis on teenustellimusel objektiseosena seadistatud.

6.  Valige ükskõik milline parandusreale vastav eelseadistatud sümptomi-, diagnoosi- ja täitmisväärtus ning kui vaja, klõpsake vahekaarti **Märkus**, et luua parandusreale märkus.

7.  Uue parandusrea salvestamiseks vajutage klahve Press CTRL+S. Välja **Loodud kuupäev ja kellaaeg** vormi **Parandusread** vahekaardil **Üldine** värskendatakse salvestamise ajal.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Edenemise jälgimine ja parandusprobleemi lahendamine

Saate paranduse edenemise jälgimiseks seadistada parandusrea parandusetapid.

Kui parandusprobleem on lahendatud, võite parandusrea sulgeda. Määrake parandusetapp etapile, kus atribuut **Lõpetatud** on lubatud. Lõpetamise ajaks registreeritakse reale praegune kuupäev ja kellaaeg.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Lahendatud probleemi parandusrea sulgemine

1.  Avage vorm **Parandusread**. Järgige käesolevas teemas eespool käsitletud parandusrea loomise protseduuri.

2.  Valige parandusrida koos parandusprobleemiga, mida soovite lõpetada.

3.  Väljas **Parandusetapp** valige etapp, millel on lubatud atribuut **Lõpetatud**.

  


