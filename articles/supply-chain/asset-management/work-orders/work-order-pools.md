---
title: Töökäsu kaustad
description: Selles teemas kirjeldatakse, kuidas töötada varahalduses töökäsu kaustadega.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875610"
---
# <a name="work-order-pools"></a>Töökäsu kaustad


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Töökäsu kaustu saate kasutada töökäskude grupeerimiseks, millel on midagi ühist. Näiteks saate luua töökäsu kaustu

- töömeeskondadele, näiteks hooldustööde meeskond A, hooldustööde meeskond B  

- Kutseoskustele, näiteks elektrikud või torumehed  

- füüsilisele asukohale  

- ajagraafikutele, nt nädalad või muud perioodid  


Vajadusel saab ühe töökäsu paigutada mitmesse töökäsukausta.


## <a name="create-work-order-pool"></a>Töökäskude kaustade loomine

Kõigis **Töökäskude kaustades** või **Aktiivsete töökäskude** kaustades saate ülevaate oma töökäskude kaustadest ja luua uusi kaustu.

1. Klõpsake **Varahaldus** > **Ühised** > **Töökäskude kaustad** > **Kõik töökäskude kaustad** või **Aktiivsed töökäskude kaustad**.

2. Klõpsake valikut **Uus**.

3. Sisestage töökäsu ID väljale **Kaust** ja nimi väljale **Nimi**.

4. Valige Jah nupul **Aktiivne**, et näidata, et töökäsu kaust on aktiivne.

5. Kui soovite, et töökäsud töökäskude kaustast automaatselt eemaldatakse, märkige ruut **Kustuta töökäskude seosed**.

6. Valige väljal **Kustuta töötsükli olek** tööoleku töötsükli olek. Näiteks saab töökäsu töötsükli olekuks määrata, et automaatselt kustutatakse seosed töökäskude kaustades.

7. Saate alustada töökäskude lisamist oma töökäskude kausta kohe. Klõpsake kiirkaardil **Töökäsud** valikut **Lisa rida**.

8. Väljal **Töökäsu tüüp** valige töökäsu tüüp. Seotud väljad värskendatakse automaatselt.

9. Kui soovite lisada rohkem töökäske, korrake samme 7-8.

10. Väljal **Sorteerimisjärjestus**saate näidata, kas töökäsud tuleb täita kindlas järjekorras. Sisestage numbrid 1, 2, 3 jne, et näidata valitud töökäskude kindlat järjestust.

11. Klõpsake nuppu **Töökäsklused**, et näha loendit kõikidest töökäskude kausta kaasatud töökäskudest.

12. Klõpsake nuppu **Võimsuse koormus** avamaks **Võimsuse koormus**, et arvutada ja vaadata võimsuse koormust hooldusgraafiku, planeerimata töökäskude ja plaanitud töökäskude jaoks.

13. Klõpsake nuppu **kauba ennustus** avamaks **kauba ennustus**, et arvutada ja vaadata kaupade (varuosad ja muud vajalikud kaubad), mis on seotud hooldusgraafiku, planeerimata töökäskude ja plaanitud töökäskudega.

14. Klõpsake nuppu **Töökäsu ostutaotlus**, et avada loend **Töökäsu ostutaotlus** ja näha töökäsukaustas töökäskudega seotud ostutaotlusi.

15. Klõpsake nuppu **Töökäsu ostutaotlus**, et avada loend **Töökäsu ostutaotlus** ja näha töökäsukaustas töökäskudega seotud ostutellimusi.

>[!NOTE]
>Kui töökäsukaust ei ole enam teie tööplaani jaoks oluline, määrake selle kausta märkekast **Aktiivne** loendi **Töökäsukaust** vaates kui Ei.

Valige märkeruut **Kustuta töökäsu seosed**, kui soovite kustutada kõik töökäsu read, näiteks tühja kausta loomiseks, mida saate hiljem kasutada teiste töökäskude puhul. Pidage meeles tühjendada märkeruut **Kustuta töökäsu seosed**, kui soovite kasutada töökäsu kausta hiljem uute töökäskude seoste loomiseks.


![Joonis 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Töökäsukaustale töökäsu lisamine

Nagu on kirjeldatud ülemises jaotises, saate töökäsu kaustale lisada töökäsu, kui loote kausta. Töökäsu saate lisada ka töökäsukausta, mis pärineb ühest **Kõik töökäsud**.

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige loendist töökäsk ja klõpsake käsku **Töökäsukaust.**

3. Valige Lisa väljal **Lisa/eemalda**.

4. Valige töökäsukaust väljal **Kaust**.

5. Klõpsake valikut **OK**.

6. Pärast töökäsu lisamist töökäsukausta, kui soovite töökäsukausta lisada kindlasse seeriasse, avage üks töökäsukausta loendi lehtedest, valige kaust ja klõpsake käsku **Redigeeri** ning korrigeerige töökäskude sortimisjärjestust kaustas vormingul **Töökäsukaust** > kiirkaart **Töökäsud** > väli **Sortimisjärjestus**.

Kui soovite valitud töökäsu eemaldada töökäsukaustast, valige 3. etapis käsk Eemalda.

