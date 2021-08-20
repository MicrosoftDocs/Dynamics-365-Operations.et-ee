---
title: Põhivara soetamiste soovitamine
description: See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99202763ae32d02f94f1590783727d4f2cf7a7bbe45963d0e175bfc449b134d9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742925"
---
# <a name="propose-fixed-asset-acquisitions"></a>Põhivara soetamiste soovitamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust. See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid. Põhivara soetamiseks põhivara soovituse töölehe kaudu peate esmalt looma põhivarakirje ja seejärel määratlema soetusmaksumuse vararaamatus.

## <a name="create-an-asset-acquisition-proposal"></a>Vara soetussoovituse loomine

Viige vara soetussoovituse loomiseks lõpule järgmised sammud. 

1. Avage navigeerimispaneelil **Moodulid > Põhivarad > Töölehe kanded > Põhivarade tööleht**.
2. Valige suvand **Uus**.
3. Sisestage või valige väärtus väljal **Nimi**.
4. Toimingupaanil valige nupp **Alused**.
5. Valige **Soovitused**.
6. Valige **Soetussoovitus**.
7. Valige **Filter**. Eelmiste väärtuste eemaldamiseks klõpsake nuppu **Lähtesta**.
8. Valige rida **Põhivara number**.
9. Sisestage või valige väärtus väljal **Kriteeriumid**. Seadistage ülejäänud kriteeriumid põhivarade puhul, mida soovite selle soovitusega soetada.  
10. Paanilt väljumiseks valige kaks korda nuppu **OK**.
- Kontrollige, kas kanderead loodi.  
- Soetussoovitusse kaasatakse ainult põhivarad, mille soetamiskuupäev ja soetusmaksumus on raamatus seadistatud.  
11. Looge raamatud lehel **Raamatud**.
12. Valige **Sisesta**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Lisage soetussoovitusse vaike-finantsdimensioonid

Soetuskande saab luua Exceli lisandmoodulite abil, minnes **Põhivarad > Töölehe kirjed > Põhivara tööleht**. Looge uus tööleht ja liikuge lehekülje jaotisesse **Read** ja valige Exceli ikoon ning seejärel valige põhivara töölehe rida. Süsteem loob ja avab tööleheridu tähistava Exceli malli. Saate mallis lisada andmeid lisatavatele tööleheridadele ja seejärel selle teabe süsteemis avaldada. 

Kui valitud vararaamatu ja vastavate põhivarade jaoks on seadistatud vaikedimensioonid, mis sisestati Exceli malli, võetakse vaike-finantsdimensioonid põhivararaamatu koondandmetest, kui tööleht avaldatakse Excelist süsteemi. Finantsdimensioonide lisamiseks põhivararaamatusse automaatselt põhivara töölehe avaldamisel Exceli lisandmoodulist, peavad vaikedimensioonid olema eelnevalt seadistatud.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
