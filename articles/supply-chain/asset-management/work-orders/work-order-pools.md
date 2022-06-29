---
title: Töökäsu kaustad
description: See artikkel kirjeldab, kuidas töötada varahalduses töötellimuste kaustu.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dc9eaf82c2f3336f8c3400fcd3f1165ed4fa56d8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014935"
---
# <a name="work-order-pools"></a>Töökäsu kaustad

[!include [banner](../../includes/banner.md)]


Töökäsu kaustu saate kasutada töökäskude grupeerimiseks, millel on midagi ühist. Siin on mõned näited asjadest, mille jaoks saate luua töökäskude kaustu.

- Töömeeskonnad, näiteks hooldustööde meeskond A või hooldustööde meeskond B  

- Kutseoskused, nagu elektrikud või torumehed  

- Füüsilised asukohad  

- Ajagraafikud, nagu nädalad või muud perioodid  

Kui vaja, saate panna ühe töökäsu mitmesse töökäsukausta.


## <a name="create-a-work-order-pool"></a>Töökäsukaustade loomine

Loendilehel **Kõik töökäskude kaustad** või **Aktiivsed töökäskude kaustad** saate ülevaate oma töökäskude kaustadest ja luua uusi kaustu.

1. Valige **varahalduse töötellimuste** > **kaustu** > **Kõik töötellimuste kaustu või** aktiivsete **töötellimuste kaustu**.

2. Valige suvand **Uus**.

3. Väljale **Kaust** sisestage töökäsukausta ID.

4. Väljale **Nimi** sisestage nimi.

5. Seadke suvandi **Aktiive** väärtuseks **Jah**, et näidata, et töökäsukaust on aktiivne.

6. Seadke suvandi **Kustuta töökäsu seosed** väärtuseks **Jah**, kui töökäsud tuleb töökäskude kaustast automaatselt eemaldada.

7. Valige väljal **Kustuta töötsükli olek** tööoleku töötsükli olek. Näiteks saab töökäsu töötsükli olekuks määrata, et automaatselt kustutatakse seosed töökäskude kaustades.

    Saate alustada töökäskude lisamist oma töökäskude kausta kohe.

8. Tehke kiirkaardil **Töökäsud** valik **Lisa rida**.

9. Väljal **Töökäsk** valige töökäsk. Seotud väljad värskendatakse automaatselt.

10. Täiendavate töökäskude lisamiseks korrake samme 8 kuni 9.

11. Kui lisatud töökäsud tuleb teha kindlas järjekorras, saate käsu täpsustamiseks sisestada väljal **Sortimisjärjestus** numbrid **1**, **2**, **3** jne.

12. Töökäsukausta kõigi töökäskude loendi vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Töökäskude kaustade kuvamisega seotud** valik **Töökäsud**, et avada loendileht **Kõik töökäsud**.

13. Hooldusgraafiku, planeerimata töökäskude ja plaanitud töökäskude täiskoormuse arvutamiseks ja vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Töökäskude kaustade kuvamisega seotud** valik **Täiskoormus**, et avada dialoogiboks **Täiskoormuse arvutamine**.

14. Hooldusgraafikuga, planeerimata töökäskudega ja plaanitud töökäskudega seotud kaupade (varuosad ja muud nõutavad kaubad) prognooside arvutamiseks ja vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Töökäskude kaustade kuvamisega seotud** valik **Kauba prognoos**, et avada dialoogiboks **Kauba prognoosi arvutamine**.

15. Töökäsukausta töökäskudega seotud ostutaotluste loendi vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Hange** valik **Töökäsu ostutaotlus**, et avada loendileht **Töökäsu ostutaotlus**.

16. Töökäsukausta töökäskudega seotud ostutellimuste loendi vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Hange** valik **Töökäsu ost**, et avada loendileht **Töökäsu ost**.

>[!NOTE]
>Kui töökäsukaust ei ole enam teie tööplaanis oluline, määrake lehe **Töökäskude kaust** loendivaates selle kausta suvandi **Aktiivne** väärtuseks **Ei**.

Kõigi töötaja tellimuseridade kustutamiseks seadke suvandi **Kustuta töökäsu seosed** väärtuseks **Jah**. See suvand on kasulik näiteks juhul, kui soovite luua tühja kausta, mida saate hiljem kasutada teiste töökäskude jaoks. Kui olete hiljem valmis kasutama töökäsukausta uute töökäsusuhete loomiseks, pidage meeles, et suvandi **Kustuta töökäsu seosed** väärtuseks tuleb määrata **Ei**.

Alloleval joonisel on kujutatud loendilehe **Töökäskude kaust** näide.

![Joonis 1.](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Töökäsukaustale töökäsu lisamine

Nagu on kirjeldatud eelmises jaotises, saate töökäsu kaustale lisada töökäsu, kui loote selle kausta. Töökäsukausta saate töökäske lisada ka loendilehel **Kõik töökäsud** või **Aktiivsed töökäsud**.

1. Valige töökäsk ja seejärel tehke toimingupaani vahekaardi **Töökäsk** grupis **Hooldamine** valik **Töökäskude kaust**.

2. Valige loendist töökäsk ja klõpsake käsku **Töökäsukaust.**

3. Dialoogiaknas **Töökäskude kausta hooldamine** tehke väljal **Lisa/eemalda** valik **Lisa**.

4. Väljal **Kaust** valige töökäsukaust.

5. Valige nupp **OK**.

6. Selleks, et seada lisatud töökäsud töökäsukaustas kindlasse järjekorda, valige kaust loendilehel **Kõik töökäskude kaustad** või **Aktiivsed töökäskude kaustad** ja seejärel valige **Redigeeri**. Seejärel kasutage lehe **Töökäskude kaust** kiirkaardil **Töökäsud** välja **Sortimisjärjestus**, et kohandada kausta kuuluvate töökäskude sortimisjärjestust.

Töökäsukaustast mõne töökäsu eemaldamiseks korrake neid etappe, kuid valige 3. etapis **Eemalda**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]