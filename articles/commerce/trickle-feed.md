---
title: Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks
description: Selles teemas kirjeldatakse vähehaaval toimuvat tellimuse loomist kaupluse kannete jaoks Microsoft Dynamics 365 Commerce'is.
author: josaw1
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 900480c926df58cc1eaca052903384ceeadcccbdc3a0ede8a35f4b2a8ff87556
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719437"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks

[!include [banner](includes/banner.md)]

Dynamics 365 Retaili versioonis 10.0.4 ja varasemates versioonides on väljavõtte sisestamine päevalõpu toiming ja kõik kanded sisestatakse raamatutesse päeva lõpus. Mahukaid kandeid tuleb seejärel töödelda piiratud ajavahemikus, mis mõnikord põhjustab suurt koormust, lukustusi ja väljavõtte sisestamise tõrkeid. Lisaks ei saa jaemüüjad tuvastada päeva jooksul oma raamatutes tulu ega makseid.

Retaili versioonis 10.0.5 kasutusele võetud vähehaaval toimuva tellimuse loomisel töödeldakse kandeid kogu päeva jooksul ja päeva lõpus töödeldakse ainult maksevahendite finantsvastavusseviimist ja muid kassahalduse kandeid. See funktsioon jaotab müügitellimuste, arvete ja maksete loomise koormuse päeva peale ära, pakkudes suuremat jõudlust ning võimaldades tulu ja makseid kajastada raamatutes peaaegu reaalajas. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Vähehaaval toimuva sisestamise kasutamine
  
1. Jaemüügikannete vähehaaval toimuva sisestamise lubamiseks lubage funktsioonihalduse abil funktsioon **Retaili väljavõtted – vähehaaval toimuv**.

    > [!IMPORTANT]
    > Enne funktsiooni lubamist veenduge, et ükski väljavõte pole sisestamise ootel.

2. Praegune väljavõttedokument tükeldatakse kaheks tüübiks: kandeväljavõte ja finantsaruanne.

      - Kandeväljavõte kogub kõik sisestamata ja kinnitatud kanded ning loob müügitellimused, müügiarved, maksete ja allahindluste töölehed ning tulu-/kulukanded teie konfigureeritaval sagedusel. Peaksite selle protsessi konfigureerima nii, et seda käitataks suurel sagedusel, et dokumendid loodaks siis, kui kanded laaditakse peakontori P-töö kaudu. Selle kandeväljavõtte korral, mis juba loob müügitellimusi ja müügiarveid, pole tegelikult vaja konfigureerida pakett-tööd **Sisesta varud**. Saate oma võimalike ärinõuete täitmiseks seda siiski kasutada.  
      
     - Finantsaruanne on mõeldud loomiseks päeva lõpus ja see toetab ainult sulgemisviisi **Vahetus**. See aruanne piiratakse finantsvastavusseviimisega ja see loob töölehed ainult loendatud summa ja kandesumma vaheliste erinevuste summade jaoks eri maksevahendite puhul, samuti loob töölehed muude sularahahalduse kannete jaoks.   

3. Kandeväljavõtte arvutamiseks avage **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Kandeväljavõtete arvutamine partiina**. Kandeväljavõtete sisestamiseks partiina valige **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Kandeväljavõtete sisestamine partiina**.

4. Finantsaruande arvutamiseks valige **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Finantsaruande arvutamine partiina**. Finantsaruannete partiina sisestamiseks valige **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Finantsaruande sisestamine partiina**.

> [!NOTE]
> Menüükäsud **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Väljavõtete arvutamine partiina** ja **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Väljavõtete sisestamine partiina** eemaldatakse selle uue funktsiooniga.

Lisaks saab kandeväljavõtte ja finantsaruande tüüpe luua käsitsi. Avage **Retail ja Commerce > Kanalid > Kauplused** ja klõpsake valikut **Väljavõtted**. Klõpsake valikut **Uus** ja valige, millist tüüpi väljavõtte soovite luua. Lehel **Väljavõtted** olevad väljad ja lehe jaotises **Väljavõttegrupp** olevad tegevused kuvavad valitud väljavõttetüübi põhjal asjakohased andmed ja tegevused.


[!INCLUDE[footer-include](../includes/footer-banner.md)]