---
title: Teenuseobjektide ülevaade
description: Selles teemas antakse ülevaade sellest, kuidas teenuseobjektidega töötada.
author: kamaybac
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad758d32c6e9de0758c6fddb57a7dea886ab73d4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986431"
---
# <a name="service-objects-overview"></a>Teenuseobjektide ülevaade

[!include [banner](../includes/banner.md)]

Teenuse objektid on kliendi varad ja tooted, millega seoses saab hooldust osutada. Olenevalt teie poolt pakutavast teenuse tüübist võivad objektid olla materiaalsed või immateriaalsed.

-  Materiaalsed objektid on nt masin või hoone, mille hooldamine seisneb füüsilistes ülesannetes.

    Materiaalne hooldusobjekt võib olla ka laokaup, mille loote vormil Väljastatud toote üksikasjad. Olenevalt varude dimensioonigrupist, mille kaubaga seote, saate hooldusobjekti luua kauba seerianumbrit sisaldavate üksikasjade tasemele. See on kasulik, kui peate jälgima konkreetset kaupa, mida hooldusobjekt kajastab.

    Materiaalne hooldusobjekt võib olla ka kaup, mis ei ole otseselt seotud ettevõtte otsese toote- või tarneahelaga. Näiteks võib tööriistakomplekt, mida kasutatakse hooldustellimuses remontimiseks, olla hooldusobjekt, mis ei sisaldu varudes. Sel juhul ei registreerita seda laokaubana.

-  Immateriaalsed objektid on mittefüüsilised asjad, nt kontokogumid või juriidiline dokument, millega saate hooldustoiminguid teha.

## <a name="example-of-an-intangible-service-object"></a>Immateriaalse hooldusobjekti näide

Ettevõte A haldab mitme väikeettevõtte finantsandmeid. Üks ettevõtte A klient on kohalik jalgpallimeeskond, millele ettevõte A osutab iganädalast raamatupidamise teenust ja viib kord aastas läbi klubi kontode auditi. Klubi kontod on seadistatud vormil Hooldusobjektid ja määratletud hooldusleppe objektina. Objektil on kaks hooldusleppe rida. 1. rida on nädalase intervalliga iganädalane raamatupidamine ja 2. rida on iga-aastane audit, millele on määratud aastane intervall.

## <a name="related-topics"></a>Seotud teemad

[Hooldusobjektide loomine](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]