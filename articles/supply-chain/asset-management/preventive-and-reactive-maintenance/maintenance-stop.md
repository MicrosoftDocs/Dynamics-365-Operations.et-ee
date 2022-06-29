---
title: Hoolduskatkestuse tegevused
description: See artikkel selgitab, kuidas hoolduse ületunnitööd kasutatakse ülevaate saamiseks võimsusest, mida on vaja teatud varade hooldustööde täitmiseks teatud perioodi jooksul.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 42e8ba4e19333cb25464203a2583175ef082ad98
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016474"
---
# <a name="maintenance-downtime-activities"></a>Hoolduskatkestuse tegevused

[!include [banner](../../includes/banner.md)]

Hoolduskatkestust kasutatakse konkreetsele varale konkreetsel ajaperioodil tehtavateks hooldustöödeks vajaliku võimsuse ülevaate saamiseks. Näiteks võite luua hoolduskatkestuse registreerimise tootmiskoha 02 tootmishoone 29-A tootmisliinile 10. Hoolduskatkesutse registreeringul on algus- ja lõppkuupäev, mis näitab perioodi, mille jooksul hoolduse peatamisega seotud varad ei ole tootmise jaoks saadaval.

**Hoolduskatkestuse tegevused** on konkreetsel ajaperioodil seotud varade hooldusgraafiku ridade ja töökäsu hooldustööde ülevaade. Töökäsu hooldustöödega seotud ridadel on oodatav alguskuupäev hoolduse peatamise perioodi jooksul. Võite ekstraktida kasulikke andmeid ja teha planeeritud hooldustöödes muudatusi.

- Saate ülevaate tootmisseadmete (varade) nõutavatest väljalülitamise perioodidest.  
- Saate ülevaate planeeritud hooldusest (kellaajad) pädevuste järgi grupeerituna (vastutavad hooldustöötajate rühmad või hooldustöötajad), näiteks planeeritud hooldustööde tegemiseks vajalike elektrikute, seppade või teiste hooldustöötajate rühmade täiskoormus.  
- Reguleerige hooldusgraafiku ridu või varaga seotud töökäsu hooldustöid, näiteks muutke real alguse ja lõpu kellaaegu või valige teisi hooldustöötajaid hooldustöötajate ja hooldustöötajate rühmade töövoo optimeerimiseks.

Kui hoolduskatkestuse registreeringule on varad valitud, sisaldab hoolduskatkestuse registreering kõiki aktiivsete töökäskude avatud hooldusgraafiku ridu ja töökäsu hooldustöid.

## <a name="maintenance-downtime-activities"></a>Hoolduskatkestuse tegevused

Klõpsake **Varahalduse** > **hoolduse downtime activities All** > **maintenance downtime activities** (Kõik hoolduse downtime tegevused), et avada kõigi hoolduse downtime-tegevuste loend ja näha osa tegevustega seotud teabest. Üksikasjade vaate avamiseks klõpsake lingil veerus **Hoolduskatkestuse tegevused**. Järgneval illustratsioonil kuvatakse näidet loendist **Hoolduskatkestuse tegevused**.

![Joonis 1.](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Looge hoolduskatkestuse tegevus

1. Klõpsake **Varahalduse hoolduse** > **downtime activities All** > **maintenance downtime activities (Kõik hoolduse downtime tegevused**) või Active **maintenance downtime activities (Aktiivse hoolduse downtime tegevused**).

2. Klõpsake valikut **Uus**.

3. Sisestage ID väljale **Hoolduskatkestuse tegevused** ja nimi väljale **Nimi**.

4. Sisestage hoolduse peatamise periood väljadele **Alguskuupäev/-kellaaeg** ja **Lõppkuupäev/-kellaaeg**.

5. Klõpsake kiirkaardil **Hoolduskatkestuse tegevuste varad** > suvandit **Lisa rida**, et lisada hoolduskatkestuse tegevusele ükshaaval varasid.

6. Kui kõik varad on lisatud, klõpsake suvandit **Salvesta**. Alloleval joonisel on näide hoolduskatkestuse tegevusest ning seotud varadest ja hooldustöödest.

7. Valitud varadega seotud töökäsu hooldustööde ja avatud hooldusgraafiku read on näidatud kiirkaartidel **Tuleneva töökäsu hooldustööd** ja **Hooldusgraafiku read**. Kiirkaardi **Üldine** > rühma **Töökäsud** > väljal **Hooldusprognoosi tunnid** ja kiirkaardi **Üldine** > rühma **Hooldusgraafik** > väljal **Hooldusprognoosi tunnid** näete töökäsu hooldustööle ja hooldusgraafiku ridadele prognoositud tundide koguarvu.

Järgneval illustratsioonil kuvatakse näidet üksikasjade vaatest **Hoolduskatkestuse tegevuste**.

![Joonis 2.](media/20-preventive-maintenance.png)

>[!NOTE]
>Valitud varadega seotud töökäsu hooldustööd ja hooldusgraafiku read värskendatakse automaatselt, kui pärast hoolduskatkestuse tegevuse loomist luuakse uued töökäsud või hooldusgraafiku read. Näiteks, kui ajastate seotud varade hoolduskavad või hoolduskorrad kaks päeva pärast hoolduskatkestuse tegevuse loomist, lisatakse hoolduskatkestuse tegevusele automaatselt uued hooldusgraafiku read.

8. Valige jaotises **Kõik hoolduskatkestuse tegevused** > **Hoolduskatkestuse tegevused** > loendist hoolduskatkestuse tegevus ja klõpsake valikut **Täiskoormus**, et avada dialoogiaken **Täiskoormuse arvutamine**. Kasutage seda dialoogi näiteks kuupäevade, varade, varatüüpide ja hooldustöö tüüpide täiskoormuse ülevaate saamiseks. Pange tähele, et dialoogis kuvatavad kuupäevad on algus- ja lõppkuupäevad, mis on valitud jaotises **Hoolduskatkestuse tegevused**. See arvutus sisaldab hoolduskatkestuse tegevusega seotud varasid.

9. Redigeerige vajadusel algus- ja lõpuaegu dialoogis **Täiskoormuse arvutamine** ja valige kas soovite kaasata arvutusse töökäsud ja hooldusgraafikud. Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade täiskoormuse arvutusi te soovite. Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha varad, mis on valitud hoolduskatkestuse tegevuse all ning seetõttu võivad tunnid real olla alumisel tasemel asuvatest töö asukohtadest kokku liidetud. Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki täiskoormuse ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.

10. Arvutuse alustamiseks klõpsake **OK**. Tundide koguarvu näidatakse **Täiskoormuse** ülevaates. Klõpsake vahekaardi **Täiskoormus** > toimingupaani rühmades **Grupeerimisalus** asjakohaseid nuppe, et saada prognoositud tundide määramise kohta üksikasjalikum ülevaade. Alltoodud illustratsioonil kuvatakse näidet arvutuse **Täiskoormus** tulemustest.

![Joonis 3.](media/21-preventive-maintenance.png)

11. Kui soovite pärast täiskoormuse ülevaate saamist teha muudatusi töökäsu hooldustööde või hooldusgraafiku ridadel, minge tagasi **Hoolduskatkestuse tegevuste** üksikasjade kuvale ja valige read, mida soovite kohandada, vahekaartidelt **Tuleneva töökäsu hooldustööd** ja **Hooldusgraafiku read**.

12. Klõpsake nuppu **Reguleeri** ja värskendage valitud töökäsu hooldustööde või hooldusgraafikute ridade oodatavat algus-/lõppkuupäeva, teenindustaset või vastutavaid hooldustöötajaid.

13. Kui olete vajalikud muudatused teinud, klõpsake **OK**. 

>[!NOTE]
>Töökäsu hooldustööde ja hooldusgraafiku read, mis ei sisaldu pärast muudatusi hoolduskatkestuse perioodis eemaldatakse jaotisest **Hoolduskatkestuse tegevused** automaatselt.

14. Valige jaotises **Kõik hoolduskatkestuse tegevused** > **Hoolduskatkestuse tegevused** > loendist hoolduskatkestuse tegevus ja klõpsake valikut **Üksuse prognoos**, et avada dialoogiaken **Kauba prognoosi arvutamine**. Kasutage seda dialoogi üksuste (varuosade ja muude vajalike esemete) prognooside arvutamiseks ja nende grupeerimiseks, et saada ülevaade näiteks kuupäeva, vara, vara tüübi ja hooldustöö tüübi järgi. Pange tähele, et dialoogis kuvatavad kuupäevad on algus- ja lõppkuupäevad, mis on valitud jaotises **Hoolduskatkestuse tegevused**. See arvutus sisaldab hoolduskatkestuse tegevuses valitud varadega seotud varuosi ja esemeid.

15. Redigeerige vajadusel algus- ja lõpuaegu dialoogis **Kauba prognoosi arvutamine** ja valige kas soovite kaasata arvutusse töökäsud ja hooldusgraafikud. Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade täiskoormuse arvutusi te soovite. Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha varad, mis on valitud hoolduskatkestuse tegevuse all ning seetõttu võivad tunnid real olla alumisel tasemel asuvatest töö asukohtadest kokku liidetud. Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki täiskoormuse ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.

16. Arvutuse alustamiseks klõpsake **OK**. Kauba prognooside koguarvu näidatakse ülevaates **Kauba prognoos**. Klõpsake vahekaardi **Kauba prognoos** > toimingupaani rühmades **Grupeerimisalus** asjakohaseid nuppe, et saada prognoositud üksuste määramise kohta üksikasjalikum ülevaade. Alltoodud illustratsioonil kuvatakse näidet arvutuse **Kauba prognoos** tulemustest.

![Joonis 4.](media/22-preventive-maintenance.png)

- Võite kopeerida varasid ühest hoolduskatkestuse tegevusest teise. Valige jaotises **Kõik hoolduskatkestuse tegevused** nupp **Hoolduskatkestuse tegevuste kopeerimine** ja tehke oma valikud väljadel **Hoolduskatkestuse tegevustest** ja **Hoolduskatkestuse tegevuseni** ning klõpsake **OK**.
- Klõpsake jaotises **Kõik hoolduskatkestuse tegevused** nuppu **Hooldusgraafiku read** või nuppu **Aktiivsed töökäsud**, et avata seotud loendeid ja vaadata valitud hoolduskatkestuse tegevusega seotud ridu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]