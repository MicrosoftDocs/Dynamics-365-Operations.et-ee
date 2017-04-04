---
title: dokumentideta
description: "Tegevussoovitus on süsteemi loodud soovitus olemasoleva plaanitud või kinnitatud tellimuse muutmiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 21 - 54
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f2ac69ddf485139b057dafa20e5f1a961fc32067
ms.lasthandoff: 03/29/2017


---

# <a name="undocumented"></a>dokumentideta

Tegevussoovitus on süsteemi loodud soovitus olemasoleva plaanitud või kinnitatud tellimuse muutmiseks.

### <a name="introduction"></a>Sissejuhatus

Koondplaneerimise arvutus loob tegevusteated muutunud vajadustele reageerimiseks. Näiteks võib lähetuskuupäev või kogus olla muutunud müügitellimusel, millele olete nõudluse täitmiseks juba ostutellimuse loonud. Sel juhul loob koondplaneerimise arvutus vähemalt ühe tegevusteate ostutellimuse muutmiseks. Saate otsustada, kas teha soovitatud muudatused.

Saate seadistada, kuidas kaubale lisatavad laovarugrupi tegevusteated arvutatakse.

 <a name="selecting-action-messages"></a> Tegevusteadete valimine
==========================

Lehel **Laovarude grupid **saate valida tegevusteated, mida süsteem peaks koostama, ja laovarude grupid või kaubad, millele teated kehtivad. Saate valida järgmisi tegevusteateid.

| Sõnum             | Kirjeldus                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Varasem**         | Kui valite selle teate, loob süsteem vajaduse korral tegevusteated tellimuste määramiseks varasemale kuupäevale. Väljal **Ettemakse marginaal** saate määrata ka maksimaalse sissetuleku ja väljastamise päevade arvu ilma ettemakse tegevuseta. |
| **Lükka edasi**        | Kui valite selle teate, loob süsteem vajaduse korral tegevusteated tellimuste määramiseks hilisemale kuupäevale. Väljal **Edasilükkamise marginaal** saate määrata ka maksimaalse sissetuleku ja väljastamise päevade arvu ilma edasilükkamise tegevuseta.       |
| **Vähenda**        | Kui valite selle teate, peaks tootmistellimuste, ostutellimuste ja muude sissetulekukannete arv vähenema, et vältida laovarude ülejääke.                                                                                                   |
| **Kasv**        | Kui valite selle teate, peaks tootmistellimuste, ostutellimuste ja muude sissetulekukannete arv suurenema, et vältida laovarude puudujääke.                                                                                                    |
| **Tuletatud tegevused** | Kui valite selle teate, koostatakse tegevusteated tuletatud vajaduste jaoks, nt tegevused tootmise täitmiseks mõeldud komponentide tellimuste jaoks.                                                                                                   |




