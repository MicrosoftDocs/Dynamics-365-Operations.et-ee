---
title: Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks
description: Selles teemas kirjeldatakse vähehaaval toimuvat tellimuse loomist kaupluse kannete jaoks Microsoft Dynamics 365 Retailis.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80233a73dbffc7380503cf03703758b187824c2a
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622662"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks (avalik eelvaade)

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

Dynamics 365 Retaili versioonis 10.0.4 ja varasemates versioonides on jaemüügiväljavõtte sisestamine päevalõpu toiming ja kõik kanded sisestatakse raamatutesse päeva lõpus. Mahukaid kandeid tuleb seejärel töödelda piiratud ajavahemikus, mis mõnikord põhjustab suurt koormust, lukustusi ja väljavõtte sisestamise tõrkeid. Lisaks ei saa jaemüüjad tuvastada päeva jooksul oma raamatutes tulu ega makseid.

Retaili versioonis 10.0.5 kasutusele võetud vähehaaval toimuv tellimuse loomise avalikus eelvaates töödeldakse kandeid kogu päeva jooksul ja päeva lõpus töödeldakse ainult maksevahendite finantsvastavusseviimist ja muid kassahalduse kandeid. See funktsioon jaotab müügitellimuste, arvete ja maksete loomise koormuse päeva peale ära, pakkudes suuremat jõudlust ning võimaldades tulu ja makseid kajastada raamatutes peaaegu reaalajas. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Vähehaaval toimuva sisestamise kasutamine
  
1. Jaemüügikannete vähehaaval toimuva sisestamise lubamiseks avage **Süsteemihaldus > Häälestamine > Litsentsi konfiguratsioon** ja keelake võti **Jaemüügi väljavõtted**.

2. Samal lehel lubage litsentsivõti **Jaemüügi väljavõtted (vähehaaval toimuv) – eelvaade**. Kui lubate selle võtme, veenduge, et ükski väljavõte pole sisestamise ootel. 

> [!Important]
> Enne kui lubate litsentsivõtme **Jaemüügi väljavõtted (vähehaaval toimuv) – eelvaade**, veenduge, et ükski väljavõte poleks sisestamise ootel.

3. Praegune väljavõttedokument tükeldatakse kaheks eri tüübiks: kandeväljavõte ja finantsaruanne.

      - Kandeväljavõte kogub kõik sisestamata ja kinnitatud jaemüügikanded ning loob müügitellimused, müügiarved, maksete ja allahindluste töölehed ning tulu-/kulukanded teie konfigureeritaval sagedusel. Peaksite selle protsessi konfigureerima nii, et seda käitataks suurel sagedusel, et dokumendid loodaks siis, kui jaemüügikanded laaditakse programmi Retail Headquarters P-töö kaudu. Selle kandeväljavõtte korral, mis juba loob müügitellimusi ja müügiarveid, pole tegelikult vaja konfigureerida pakett-tööd **Sisesta varud**. Saate oma võimalike ärinõuete täitmiseks seda siiski kasutada.  
      
     - Finantsaruanne on mõeldud loomiseks päeva lõpus ja see toetab ainult sulgemisviisi **Vahetus**. See aruanne piiratakse finantsvastavusseviimisega ja see loob töölehed ainult loendatud summa ja kandesumma vaheliste erinevuste summade jaoks eri maksevahendite puhul, samuti loob töölehed muude kassahalduse kannete jaoks.   

4. Kandeväljavõtte arvutamiseks klõpsake valikuid **Jaemüük > Jaemüügi IT > Kassa sisestamine > Kandeväljavõtete arvutamine partiina**. Kandeväljavõtete sisestamiseks partiina klõpsake valikuid **Jaemüük > Jaemüügi IT > Kassa sisestamine > Kandeväljavõtete sisestamine partiina**.

5. Finantsaruande arvutamiseks klõpsake valikuid **Jaemüük > Jaemüügi IT > Kassa sisestamine > Finantsaruannete arvutamine partiina**. Finantsaruannete sisestamiseks partiina klõpsake valikuid **Jaemüük > Jaemüügi IT > Kassa sisestamine > Finantsaruannete sisestamine partiina**.

> [!NOTE]
> Menüükäsud **Jaemüük > Jaemüügi IT > Kassa sisestamine > Väljavõtete arvutamine partiina** ja **Jaemüük > Jaemüügi IT > Kassa sisestamine > Väljavõtete sisestamine partiina** eemaldatakse selle uue funktsiooniga.

Lisaks saab kandeväljavõtte ja finantsaruande tüüpe luua käsitsi. Avage **Jaemüük > Kanalid > Kauplused** ja klõpsake valikut **Jaemüügi väljavõtted**. Klõpsake valikut **Uus** ja valige, millist tüüpi väljavõtte soovite luua. Lehel **Jaemüügi väljavõtted** olevad väljad ja lehe jaotises **Väljavõttegrupp** olevad tegevused kuvavad valitud väljavõttetüübi põhjal asjakohased andmed ja tegevused.
