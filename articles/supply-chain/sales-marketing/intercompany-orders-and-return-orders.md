---
title: Kontsernisisesed tellimused ja tagastustellimused
description: See teema selgitab kontsernisiseseid tellimusi ja tagastustellimusi
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 103225595e82bdedec6d97e5ebe5b61498377065
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548225"
---
# <a name="intercompany-orders-and-return-orders"></a>Kontsernisisesed tellimused ja tagastustellimused

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kontsernisiseseid ostutellimusi, müügitellimusi, tagastustellimusi, ostulepinguid ja müügilepinguid luuakse ning värskendatakse.

## <a name="about-intercompany-orders"></a>Kontsernisisestest tellimustest

Kontsernisisese müügitellimuse loomisel loob rakendus Microsoft Dynamics 365 Supply Chain Management vastava ostutellimuse automaatselt. Sarnaselt kutsub kontsernisisese ostutellimuse loomine esile vastava kontsernisisese müügitellimuse automaatse loomise.

See kehtib nii kaheharuliste tellimuste (kahe omavahel seotud ettevõtte vahelised kanded) ja enamiku kolmeharuliste ettevõtete korral (kui kontsernisisene kanne pärineb koos müügitellimusega väliskliendilt).

## <a name="intercompany-order-example"></a>Kontsernisisese tellimuse näide

Teil on kaks omavahel seotud ettevõtet. Ettevõte A on müügi allettevõte, ettevõte B on jaotusüksus. Kontsernisisesed müügitellimused ja ostutellimused luuakse automaatselt järgmiste stsenaariumite järgi:

- Kui ettevõte A loob ostutellimuse ja tarnijaks on ettevõte B, luuakse kontsernisisene müügitellimus automaatselt ettevõttes B. Kaheharuline ahel koosned ettevõte A ostutellimusest ja ettevõtte B kontsernisisesest müügitellimusest.
- Kui ettevõte B loob müügitellimuse ja klient on ettevõte A, luuakse ettevõttes A automaatselt kontsernisisene ostutellimus. Kaheharuline tellimuseahel koosneb ettevõtte B müügitellimusest ja ettevõtte A kontsernisisesest ostutellimusest.
- Kui ettevõte A loob kõigepealt müügitellimuse väliskliendile, saab luua ostutellimuse automaatselt ettevõttes A. See omakorda kutsub esile kontsernisisese müügitellimuse automaatse loomise ettevõttes B. Kolmeharuline tellimuseahel koosneb müügitellimusest ja ostutellimusest ettevõttes A ning kontsernisisesest müügitellimusest ettevõttes B.

## <a name="about-intercompany-return-orders"></a>Kontsernisisesest tagastustellimustest

Kontsernisiseseid kaupu saab tagastada suuresti samamoodi kui tavalisi tagastusi. Kontsernisiseste kaupadega luuakse väliskliendi kaupade tagastustellimuse puhul siiski kontsernisisene ostutellimus. See viib omakorda automaatselt kontsernisisese müügi tagastustellimuse loomisele. Saate kontsernisisese kauba tagastada ka ilma väliskliendi tagastustellimuseta.

Tavaliste tagastustellimustega sarnaselt algatatakse kontsernisisesed tagastustellimused lehel **Loo tagastustellimus**.

Rakenduses Microsoft Dynamics 365 Supply Chain Management värskendatakse kontsernisiseseid müügi- ja ostulepinguid automaatselt, et need kajastaksid tagastatud kaupa. Selle kauba müügi- või ostulepingu kohustust korrigeeritakse automaatselt kajastama muudatust koguses või summas, kui kaup tagastatakse.

## <a name="intercompany-return-order-example"></a>Kontsernisisese tagastustellimuse näide

Ettevõte A loob ostutellimuse, mis seotakse kontsernisisese kauba puhul ostulepinguga. Kontsernisisene müügitellimus luuakse automaatselt ettevõttes B, mis on seotud vastava müügilepinguga. Ostuleping ja müügileping on seotud nagu kontsernisisesed lepingud.

Ettevõte A tagastab kontsernisisese kauba ettevõttele B. Ettevõte B loob kaubale tagastustellimuse ja ettevõttes A luuakse automaatselt ostu tagastustellimus. Algsete tellimustega seotud ostu- ja müügilepingu kohustusi korrigeeritakse automaatselt, et need kajastaksid muutust koguses ja summas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
