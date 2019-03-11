---
title: Tegevussoovitused
description: Tegevussoovitus on süsteemi loodud soovitus olemasoleva plaanitud või kinnitatud tellimuse muutmiseks.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a417abc8b725f4d57ada595da57505ae1347bfc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "349649"
---
# <a name="action-messages"></a>Tegevussoovitused

[!include [banner](../includes/banner.md)]

Tegevussoovitus on süsteemi loodud soovitus olemasoleva plaanitud või kinnitatud tellimuse muutmiseks.

## <a name="introduction"></a>Sissejuhatus

Koondplaneerimise arvutus loob tegevusteated muutunud vajadustele reageerimiseks. Näiteks võib lähetuskuupäev või kogus olla muutunud müügitellimusel, millele olete nõudluse täitmiseks juba ostutellimuse loonud. Sel juhul loob koondplaneerimise arvutus vähemalt ühe tegevusteate ostutellimuse muutmiseks. Saate otsustada, kas teha soovitatud muudatused.

Saate seadistada, kuidas kaubale lisatavad laovarugrupi tegevusteated arvutatakse.

## <a name="select-action-messages"></a>Tegevusteadete valimine

Lehel **Laovarude grupid** saate valida tegevusteated, mida süsteem peaks koostama, ja laovarude grupid või kaubad, millele teated kehtivad. Saate valida järgmisi tegevusteateid.

| Sõnum             | Kirjeldus                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Varasem**         | Kui valite selle teate, loob süsteem vajaduse korral tegevusteated tellimuste määramiseks varasemale kuupäevale. Väljal **Ettemakse marginaal** saate määrata ka maksimaalse sissetuleku ja väljastamise päevade arvu ilma ettemakse tegevuseta. |
| **Lükka edasi**        | Kui valite selle teate, loob süsteem vajaduse korral tegevusteated tellimuste määramiseks hilisemale kuupäevale. Väljal **Edasilükkamise marginaal** saate määrata ka maksimaalse sissetuleku ja väljastamise päevade arvu ilma edasilükkamise tegevuseta.       |
| **Vähenda**        | Kui valite selle teate, peaks tootmistellimuste, ostutellimuste ja muude sissetulekukannete arv vähenema, et vältida laovarude ülejääke.                                                                                                   |
| **Kasv**        | Kui valite selle teate, peaks tootmistellimuste, ostutellimuste ja muude sissetulekukannete arv suurenema, et vältida laovarude puudujääke.                                                                                                    |
| **Tuletatud tegevused** | Kui valite selle teate, koostatakse tegevusteated tuletatud vajaduste jaoks, nt tegevused tootmise täitmiseks mõeldud komponentide tellimuste jaoks.                                                                                                   |





