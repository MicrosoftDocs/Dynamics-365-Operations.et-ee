---
title: "Töövoo elemendid"
description: "Selles teemas kirjeldatakse mitmesuguseid elemente, millest töövoog koosneb."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 15cac09a97305c1b467cbb97da2d4b8a864ccbc7
ms.contentlocale: et-ee
ms.lasthandoff: 11/14/2017

---

# <a name="workflow-elements"></a>Töövoo elemendid

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse mitmesuguseid elemente, millest töövoog koosneb.

Töövoog koosneb elementidest. Järgmised jaotised kirjeldavad iga elemenditüüpi.

## <a name="tasks"></a>Ülesanded

*Ülesanne* on tööühik, mille peab tegema. Töövoogu saab lisada kaht tüüpi ülesandeid: käsitsi ja automatiseeritud.

### <a name="manual-task"></a>Käsitsi tehtav ülesanne

*Käsitsi ülesanne* on tööühik, mille peab tegema kasutaja. Näiteks võivad kuluaruande töövool olla käsitsi ülesanded, mis nõuavad määratud kasutajatelt järgmiste tegevuste lõpuleviimist.

- Koos kuluaruandega esitatud kviitungite läbivaatus.
- Töötaja ülemuse kutsumine.

### <a name="automated-task"></a>Automatiseeritud ülesanne

*Automatiseeritud ülesanne* on tööühik, mille peab tegema süsteem. Inimeste tehtavad toimingud pole vajalikud. Näiteks võivad müügitellimuse töövool olla automatiseeritud ülesanded, mis nõuavad süsteemilt järgmiste tegevuste lõpuleviimist.

- Krediidikontrolli teostamine.
- Kliendi jaoks kliendikirje loomine, kui seda veel pole.

## <a name="approval-processes"></a>Kinnitusprotsessid

*Kinnitusprotsess* on eraldi etappidest koosnev protsess. Kasutaja saab igas kinnitusetapis teostada järgmisi toiminguid.

- Kinnitage dokument.
- Lükake dokument tagasi.
- Taotlege dokumendi muutmist.
- Määrake dokument teisele kasutajale kinnitamiseks.

## <a name="line-item-workflow-elements"></a>Rea kauba töövoo elemendid

Töövoo saab luua kas dokumentide või dokumendi reakaupade töötlemiseks. Näiteks olete loonud kinnitustöövoo ajatabelite jaoks. (Viitame sellele töövoole kui *dokumenditöövoole*.) Saate sellele dokumendi töövoo elemendile lisada *rea kauba töövoo*. Rea kauba elemendi käitamisel esitatakse dokumendi iga reakaup töötlemiseks. Võite lasta kõiki rea kaupu töödelda sama rea kauba töövooga või lasta iga reakaupa töödelda eraldi rea kauba töövooga. Oletagem, et töötaja on esitanud ajatabeli, mis sarnaneb järgmisel joonisel toodule.

![Töövoog rea kaupadega](./media/workflow_lineitemworkflow.gif)

Selles stsenaariumis võib olla vaja luua järgmised reaüksuse töövood.

- **Rea kauba töövoog 1** – seda töövoogu kasutatakse rea kaupade töötlemiseks, kui projekti ID on 1111.
- **Rea kauba töövoog 2** – seda töövoogu kasutatakse rea kaupade töötlemiseks, kui projekti ID on 2222.
- **Rea kauba töövoog 3** – seda töövoogu kasutatakse rea kaupade töötlemiseks, kui projekti ID on 3333.

## <a name="flow-control-elements"></a>Voo juhtelemendid

Järgmised elemendid võimaldavad teil kujundada töövood, mis on alternatiivsed harud või samal ajal töötavad harud.

### <a name="manual-decision"></a>Käsitsi otsus

*Käsitsi otsus* on punkt, milles töövoog jaguneb kaheks haruks. Kasutaja peab tegema otsuse, mis määrab, millist haru kasutatakse esitatud dokumendi töötlemiseks.

### <a name="conditional-decision"></a>Tingimuslik otsus

*Tingimuslik otsus* on samuti punkt, milles töövoog jaguneb kaheks haruks. Siiski otsustab süsteem, millist haru kasutatakse esitatud dokumendi töötlemiseks. Selle otsuse tegemiseks hindab süsteem dokumenti, et teha kindlaks, kas see vastab määratud tingimustele.

### <a name="parallel-activity"></a>Paralleeltegevus

*Paralleeltegevus* on töövoo element, mis sisaldab kaht või enamat töövoo haru, mis töötavad samal ajal.

### <a name="subworkflow"></a>Alamtöövoog

*Alamtöövoog* on teise töövoo kontekstis käitatav töövoog.

