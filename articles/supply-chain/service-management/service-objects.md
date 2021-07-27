---
title: Teeninduse objektide ülevaade
description: Hooldusobjektid on kliendi varad ja tooted, millega seoses saab hooldust osutada.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a078b2573a08dfd4ac2232bb22f2d694cab090e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335864"
---
# <a name="service-objects-overview"></a>Teeninduse objektide ülevaade

[!include [banner](../includes/banner.md)]

Hooldusobjektid on kliendi varad ja tooted, millega seoses saab hooldust osutada. Olenevalt teie poolt pakutavast teenuse tüübist võivad objektid olla materiaalsed või immateriaalsed.

-  Materiaalsed objektid on nt masin või hoone, mille hooldamine seisneb füüsilistes ülesannetes.

    Materiaalne hooldusobjekt võib olla ka laokaup, mille loote vormil Väljastatud toote üksikasjad. Olenevalt varude dimensioonigrupist, mille kaubaga seote, saate hooldusobjekti luua kauba seerianumbrit sisaldavate üksikasjade tasemele. See on kasulik, kui peate jälgima konkreetset kaupa, mida hooldusobjekt kajastab.

    Materiaalne hooldusobjekt võib olla ka kaup, mis ei ole otseselt seotud ettevõtte otsese toote- või tarneahelaga. Näiteks võib tööriistakomplekt, mida kasutatakse hooldustellimuses remontimiseks, olla hooldusobjekt, mis ei sisaldu varudes. Sel juhul ei registreerita seda laokaubana.

-  Immateriaalsed objektid on mittefüüsilised asjad, nt kontokogumid või juriidiline dokument, millega saate hooldustoiminguid teha.

## <a name="example-of-an-intangible-service-object"></a>Immateriaalse hooldusobjekti näide

Ettevõte A haldab mitme väikeettevõtte finantsandmeid. Üks ettevõtte A klient on kohalik jalgpallimeeskond, millele ettevõte A osutab iganädalast raamatupidamise teenust ja viib kord aastas läbi klubi kontode auditi. Klubi kontod on seadistatud vormil Hooldusobjektid ja määratletud hooldusleppe objektina. Objektil on kaks hooldusleppe rida. 1. rida on nädalase intervalliga iganädalane raamatupidamine ja 2. rida on iga-aastane audit, millele on määratud aastane intervall.

## <a name="related-topics"></a>Seotud teemad

[Hooldusobjektide loomine](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]