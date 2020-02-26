---
title: Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks
description: Selles teemas kirjeldatakse vähehaaval toimuvat tellimuse loomist kaupluse kannete jaoks Microsoft Dynamics 365 Commerceis.
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
ms.openlocfilehash: 3f691017ad06d3416e4ba0e86d7a0bc207aba5bd
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004270"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks (avalik eelvaade)

[!include [banner](includes/banner.md)]



Dynamics 365 Retaili versioonis 10.0.4 ja varasemates versioonides on väljavõtte sisestamine päevalõpu toiming ja kõik kanded sisestatakse raamatutesse päeva lõpus. Mahukaid kandeid tuleb seejärel töödelda piiratud ajavahemikus, mis mõnikord põhjustab suurt koormust, lukustusi ja väljavõtte sisestamise tõrkeid. Lisaks ei saa jaemüüjad tuvastada päeva jooksul oma raamatutes tulu ega makseid.

Retaili versioonis 10.0.5 kasutusele võetud vähehaaval toimuv tellimuse loomise avalikus eelvaates töödeldakse kandeid kogu päeva jooksul ja päeva lõpus töödeldakse ainult maksevahendite finantsvastavusseviimist ja muid kassahalduse kandeid. See funktsioon jaotab müügitellimuste, arvete ja maksete loomise koormuse päeva peale ära, pakkudes suuremat jõudlust ning võimaldades tulu ja makseid kajastada raamatutes peaaegu reaalajas. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Vähehaaval toimuva sisestamise kasutamine
  
1. Kannete vähehaaval toimuva sisestamise lubamiseks avage **Süsteemihaldus > Häälestamine > Litsentsi konfiguratsioon** ja keelake võti **Väljavõtted**.

2. Samal lehel lubage litsentsivõti **Väljavõtted (vähehaaval toimuv) – eelvaade**. Kui lubate selle võtme, veenduge, et ükski väljavõte pole sisestamise ootel. 

    > [!Important]
    > Enne kui lubate litsentsivõtme **Väljavõtted (vähehaaval toimuv) – eelvaade**, veenduge, et ükski väljavõte poleks sisestamise ootel.

3. Praegune väljavõttedokument tükeldatakse kaheks eri tüübiks: kandeväljavõte ja finantsaruanne.

      - Kandeväljavõte kogub kõik sisestamata ja kinnitatud kanded ning loob müügitellimused, müügiarved, maksete ja allahindluste töölehed ning tulu-/kulukanded teie konfigureeritaval sagedusel. Peaksite selle protsessi konfigureerima nii, et seda käitataks suurel sagedusel, et dokumendid loodaks siis, kui kanded laaditakse peakontori P-töö kaudu. Selle kandeväljavõtte korral, mis juba loob müügitellimusi ja müügiarveid, pole tegelikult vaja konfigureerida pakett-tööd **Sisesta varud**. Saate oma võimalike ärinõuete täitmiseks seda siiski kasutada.  
      
     - Finantsaruanne on mõeldud loomiseks päeva lõpus ja see toetab ainult sulgemisviisi **Vahetus**. See aruanne piiratakse finantsvastavusseviimisega ja see loob töölehed ainult loendatud summa ja kandesumma vaheliste erinevuste summade jaoks eri maksevahendite puhul, samuti loob töölehed muude sularahahalduse kannete jaoks.   

4. Kandeväljavõtte arvutamiseks klõpsake valikuid **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Kandeväljavõtete arvutamine partiina**. Kandeväljavõtete sisestamiseks partiina klõpsake valikuid **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Kandeväljavõtete sisestamine partiina**.

5. Finantsaruande arvutamiseks klõpsake valikuid **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Finantsaruande arvutamine partiina**. Finantsaruannete partiina sisestamiseks klõpsake valikuid **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Finantsaruande sisestamine partiina**.

> [!NOTE]
> Menüükäsud **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Väljavõtete arvutamine partiina** ja **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Väljavõtete sisestamine partiina** eemaldatakse selle uue funktsiooniga.

Lisaks saab kandeväljavõtte ja finantsaruande tüüpe luua käsitsi. Avage **Jaemüük ja kaubandus > Kanalid > Kauplused** ja klõpsake valikut **Väljavõtted**. Klõpsake valikut **Uus** ja valige, millist tüüpi väljavõtte soovite luua. Lehel **Väljavõtted** olevad väljad ja lehe jaotises **Väljavõttegrupp** olevad tegevused kuvavad valitud väljavõttetüübi põhjal asjakohased andmed ja tegevused.
