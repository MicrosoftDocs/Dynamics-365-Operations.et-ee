---
title: IoT-lahenduse juurutamine Azure’is
description: Andurandmeteave kasutab koos sellega ühendatud andurite andmeid Microsoft Azure. See artikkel selgitab, kuidas juurutada asju internetti (IoT) lahendust oma Azure’i kordustellimuses.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 284aba91aa436ed1dfc02b5a93b4358ffc518017
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428988"
---
# <a name="deploy-an-iot-solution-on-azure"></a>IoT-lahenduse juurutamine Azure’is

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Andurandmeteave kasutab koos sellega ühendatud andurite andmeid Microsoft Azure. Selleks, et lubada Azure’ist andmeid kätte saada ja neid oma seadmetega Dynamics 365 Supply Chain Management jagada, peate oma Azure’i kordustellimusele juurutama lahenduse Internet of Things (IoT). Järgmine aarhitektuurdiagramm annab ülevaate lahendusest ja selle komponentidest.

![Anduri andmeteabe aarhitektuurdiagramm.](media/sdi-architecture.png "Koosteandmete teabe aarhitektuurdiagramm")

Järgige neid samme, et juurutada nõutavad ressursid Azure’is.

1. Logige administraatorina tarneahela haldusse sisse.
1. Minge süsteemihalduse **häälestamise \> andinfo \> juurutamiseks ja \> ühendage Azure’i ressursid** juurutusviisardi avamiseks.
1. Lugege teavet **tervituslehelt** ja valige siis **Edasi**.
1. Lugege teavet **lehel IoT näidislahenduse juurutamine Azure’i** **ja seejärel valige jaotises Juhised** suvand **Juuruta**.
1. Avatakse uus brauseri vahekaart ja teid võetakse Azure’i portaali nii, et saate azure’i ressursse juurutada. Kui teid küsitakse, logige sisse, kasutades oma Azure’i kordustellimuse mandaate.
1. Valige oma **kordustellimus** kohandatud juurutuse **lehel** kordustellimuse väljal.
1. Valige välja **Ressursigrupp** all suvand **Loo uus**, et luua juurutatud Azure’i komponentidele ressursigrupp.
1. Kuvatavas ripploendis **väljal Nimi** sisestage uue ressursigrupi nimi (nt *IoT-demo*). Seejärel valige **OK**.
1. Seadistage järgmised väljad.

    - **Ressursigrupp** – valige äsja loodud ressursigrupp.
    - **Regioon** : valige piirkond, ideaaljuhul piirkond, kus teie tarneahela halduskeskkond juurutatakse. Pidage silmas, et Azure’i piirkondadel on erinev hinnakujundus. Oma piirkonna hinnangulised kulud saate vaadata, kasutades Anduri [andmeteabe hinna kalkulaatorit](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **Tarneahela halduse keskkonna URL** – sisestage oma tarneahela halduskeskkonna URL.
    - **Taaskasuta olemasolevat Azure’i IoT keskust** – jätke see ruut tühjaks.

1. Valige **Järgmine: Ülevaade + Loomine**.
1. Kohandatud juurutamise **lehel** kontrollige, kas kinnitamine on läbitud, ja valige käsk **Loo**.
1. Juurutamise **lehel jälgitakse** juurutamise edenemist. Juurutamise protsess võib kesta kuni 30 minutit. Kui juurutamise **leht näitab**, et juurutamine on lõpule viidud, valige ressursigrupi nime link, et avada leht, mis näitab grupis juurutatud ressursside loendit.
1. Leidke ressursiloendist kirje, kus välja **Tüüp väärtuseks** on määratud Hallatud *identiteet*. **Valige veerus** Nimi nimi ressursi üksikasjade lehe avamiseks.
1. Kopeerige väärtus väljale Kliendi **ID** (näiteks klõpsates nuppu Kopeeri **lõikelauale**).
1. Minge tagasi brauseri vahekaardile, kus tarneahela haldus töötab, *kuid ärge sulgege Vahekaarti Azure’i portaali jaoks*. **Viisardilehe IoT näidislahenduse juurutamine peaks** siiski olema avatud. 
1. Valige **Edasi**.
1. Kleebige **Connect Azure’i** ressursside **Azure AD lehel rakenduse kliendi ID väljal** **kopeeritud kliendi ID** väärtus.
1. Minge tagasi brauseri vahekaardile, kus Azure’i portaal on avatud, *kuid ärge sulgege tarneahela haldamise vahekaarti*. Ressursi üksikasjade leht peaks siiski olema avatud.
1. Valige brauseri nupp Tagasi **,** et naasta uues ressursigrupis ressursside loendisse.
1. Ressursiloendist otsige kirje, kus välja Tüüp väärtuseks **on** seatud *Azure’i vahemälu taasesitatud jaoks*. **Valige veerus** Nimi nimi ressursi üksikasjade lehe avamiseks.
1. Valige vasakul navigeerimispaanil **Juurdepääsuvõtmed**.
1. Kopeerige **pääsuvõtmete** lehel väärtus, **mis kuvatakse esmase ühendusstringi (StackExchange.Redis)** jaoks (**näiteks klõpsates nuppu Kopeeri lõikelauale**).
1. Minge tagasi brauseri vahekaardile, kus tarneahela haldus töötab. Connect **Azure’i ressursside** leht peaks siiski olema avatud.
1. Kleebige **kopeeritud esmase ühendusstringi** **(StackExchange.Redis)** väärtus uuesti lao ühenduse stringile.
1. Valige **Lõpeta**.

Azure’i ressursid Azure’i andmeteabe jaoks on nüüd juurutatud teie Azure’i kordustellimuses.

> [!NOTE]
> Mis tahes ajal saate vaadata või redigeerida ühendusteavet, mis on salvestatud tarneahela halduses, avades **andmeteabe parameetrite lehe**. Lisateavet vt Anduri andmeteabe [parameetritest](sdi-parameters.md).
