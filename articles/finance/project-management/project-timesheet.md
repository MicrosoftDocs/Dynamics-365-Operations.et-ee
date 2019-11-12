---
title: Mobiilirakendus Project Timesheet
description: Selles teemas kirjeldatakse mobiilirakendust Microsoft Dynamics 365 Project Timesheet. Mobiilirakendus Project Timesheet võimaldab kasutajatel mobiilses seadmes projektide ajatabeleid sisestada ja kinnitada.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 753c2a2905835a03b6befe817d32f993d35a5d73
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552321"
---
# <a name="project-timesheet-mobile-application"></a>Mobiilirakendus Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Mobiilirakendus Microsoft Dynamics 365 Project Timesheet võimaldab kasutajatel mobiilses seadmes (iPhone või Android) projektide ajatabeleid sisestada ja kinnitada. See mobiilirakendus tõstab esile rakenduse Dynamics 365 Finance Projektihalduse ja -arvestuse ala ajatabelite funktsiooni, mis parendab kasutajate tootlikkust ning tõhusust ja hõlbustab projektide ajatabelite õigeaegset sisestamist ning kinnitamist.

## <a name="download-and-install-the-mobile-app"></a>Laadige alla ja installige mobiilirakendus

Laadige alla ja installige mobiilirakendus Microsoft Dynamics 365 Project Timesheet Androidile või iPhone'ile oma mobiilseadme poest.

## <a name="enable-the-app"></a>Lubage rakendus 

Finance’i peab mobiilirakendus Project Timesheet olema lubatud. Funktsiooni lubamiseks liikuge jaotisesse **Projektihalduse ja -arvestuse parameetrid \> Ajatabel** ja valige parameeter **Luba Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Logige rakendusse sisse

1.  Käivitage rakendus oma mobiilses seadmes.

2.  Sisestage oma Finance’i URL

3.  Esimesel sisselogimisel küsitakse teilt kasutajanime ja parooli. Sisestage oma identimisteave.

4.  Teid logitakse sisse teie vaikeettevõttesse.

## <a name="submit-a-project-timesheet"></a>Sisestage projekti ajatabel

Rakenduses saate luua ja esitada projekti ajatabeli. Uue ajatabeli alusena saab kasutada eelmise ajatabeli teavet, salvestatud ridu või projekti määramisi. Kui teid on määratud delegaadiks, saate sisestada ka teise töötaja ajatabeli. Ajatabeli loomiseks delegaadina valige nupp **Menüü** ja seejärel valige ressursi nimi.

Ajatabeli leht loob ajatabeli perioodiks uue ajatabeli, võttes aluseks praeguse kuupäeva. Kuvatakse töönädal. Kui ajatabeli periood hõlmab mitu nädalat, saate töönädala vahekaartidest valida teise töönädala.
Kui praeguse kuupäeva jaoks on ajatabel olemas, kuvatakse see. Kui peate muu ajatabeli perioodi jaoks looma uue ajatabeli, valige nupp **Menüü** ja seejärel valige **Uus ajatabel**.

Projektiteabe saate sisestada klõpsates tegevust **Lisa aeg** või **Kopeeri aeg kohast**. Tegevus **Kopeeri aeg kohast** kopeerib projektirea teabe, kuid mitte tunde. Menüü **Kopeeri aeg kohast** hõlmab järgmisi suvandeid.

- **Kopeeri olemasolevast ajatabelist** – kopeerige ajatabeli ridu olemasolevast ajatabelist.

- **Kopeeri lemmikust** – looge uusi ajatabeli ridu lemmikutena valitud ajatabeli sätetest.

- **Kopeeri määrangust** – looge uusi ajatabeli ridu määratud projektidest.

Kuvatud projektiteave sõltub mobiiliparameetritest, mille te lehel **Projektihalduse ja -arvestuse parameetrid** määrasite.

Väljal **Juriidiline isik** valige juriidiline isik, millele projekti tööd tehti. Väli **Juriidiline isik** on saadaval ainult juhul, kui kontsernisisese ajatabeli tugi on teie juriidilise isiku puhul lubatud.

Valige ajatabeli jaoks klient, kes on projektiga seotud. Androidi esialgse väljaande puhul ei ole kliendipõhised kanded toetatud, kuna peate esmalt valima projekti. Kui valisite esmalt projekti, sisestatakse väljale **Klient** väärtus automaatselt.

Väljal **Projekt** valige projekt, mille jaoks aega sisestate. Väljale **Klient** sisestatakse automaatselt väärtus.

Kliendi- ja projektiotsingud võimaldavad otsida nii klientidest kui projektidest.

Vajaduse korral valige teave väljades **Kategooria**, **Tegevus**, **Rea atribuut**, **Käibemaksugrupp** ja **Kauba käibemaksugrupp**.  Neid välju saab allutada.

Välja **Rea atribuut** väärtuseks seatakse projektihalduse ja -arvestuse parameetrite alusel vaikeväärtus. Kui parameetrid projekt/kategooria ja kategooria/ressurss on lubatud, seatakse välja **Rea atribuut** väärtuseks vaikeväärtus, mille olete selle kinnitamise jaoks määranud. Kui parameetrid projekt/kategooria ja kategooria/ressurss ei ole lubatud, muutub väli **Rea atribuut** vaikeväärtuseks vastavalt lehe **Projektihalduse ja -arvestuse parameetrid** väljale **Luba vaikereaatribuut**. Välja **Rea atribuut** väärtust saab allutada.

Valige päev, et lisada aeg. Sisestage enda iga päev töötatud tundide arv.

Sisestatavate tundide kohta kommentaaride lisamiseks klõpsake suvandit **Lisa kommentaare** ja seejärel sisestage kommentaarid sisemiste kasutajate, klientide või mõlema jaoks.
Sisemisi kommentaare saavad vaadata projektijuhid. Klientidele mõeldud kommentaarid lisatakse arvetele.

Rea lemmikuna salvestamiseks märkige ruut ja klõpsake suvandit **Salvesta lemmikuna**.

Mobiilirakenduses ei ole finantsdimensioon ja manused toetatud.

Ajatabeli lõpetamiseks jätkake projektiridade lisamist vajadust mööda.

Klõpsake suvandit **Esita** ajatabeli saatmiseks kinnitamiste töövoogu.

## <a name="review-timesheets"></a>Vaadake ajatabeleid üle

Ülevaatamist vajavate ajatabelite loend on saadaval menüüs. See valik on saadaval ainult siis, kui teid on määratud töövoo kinnitajaks. Toetatud on nii päise kui rea kinnitamine. Kinnitamine rea tasemel võimaldab valida kinnitamiseks üht või mitut rida. Pärast ajatabeli teabe üle vaatamist, klõpsake suvandit **Kinnita**, **Delegeeri** või **Tagasta**, et töövoogu jätkata.
