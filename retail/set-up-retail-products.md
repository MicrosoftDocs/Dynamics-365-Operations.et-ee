---
title: "Jaetoodete häälestamine"
description: "Selles artiklis kirjeldatakse, kuidas luua Microsoft Dynamics 365 toiminguteks - jaemüügi tooted."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 116c49174989ff14982027cc235640c2ad7322f2
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-retail-products"></a>Jaetoodete häälestamine

Selles artiklis kirjeldatakse, kuidas luua Microsoft Dynamics 365 toiminguteks - jaemüügi tooted.

Enne toodete edasimüügiks pakute jaemüügiprotsessi, tuleb luua ja konfigureerida toodete Dynamics 365 toimingute AX - jaemüügi jaoks. Jaemüügi kasutab toote funktsioonid Dynamics 365 operatsioonide toote kapten üle kogu asutuse kehtivad toodete loomiseks. Saate luua tooted, määratleda toote omadused ja atribuudid ning määrata tooted jaemüügikategooria hierarhiatesse. Selleks et teha tooted jaemüügikanalites kättesaadavaks ja lisada need aktiivsele sortimendile, peate tooted väljastama juriidilistele isikutele, kus need on saadaval. Jaemüügikanalite kaudu müüdavate toodete seadistamiseks täitke järgmised ülesanded.

1.  Määratlege jaemüügi tootehierarhia. Kategooria hierarhia funktsioone kasutades Dynamics 365 toimingute puhul saate määratleda jaemüügi kategooria hierarhiate rühma ja toodete jaemüügiprotsessi laiali kategoriseerida. Kasutaja määratletavaid ja süsteemi atribuute saab määratleda kategooria tasemel. Seejärel, pärivad kõik kategooriale määratud tooted need atribuudid. Määratleda saab mitu kategooriahierarhiat ja iga toote saab määrata mitmele hierarhiale. Ühes hierarhias saab siiski iga toote määrata ainult ühte kategooriasse.
2.  Lisage tooted ja tootevariandid tooteetalonile. Tooteetalonile lisatud tooted esindavad toodete globaalset loendit. Saate lisada tooteid käsitsi, ükshaaval või importida toote andmed hankijatelt.
3.  Väljastage tooted juriidilistele isikutele. Jaemüügikanalitele saab kättesaadavaks teha ainult juriidilistele isikutele väljastatud tooteid. Toote algsel määratlemisel määratlege see organisatsiooniülesel tasemel. Seejärel saate valida ühe või mitu juriidilist isikut, kellele toode väljastada. Siis muutub toode kättesaadavaks teie organisatsiooni mitmele jaemüügikanalile. Selle funktsiooni abil saate luua toote ühekorraga, lisada ning värskendada toote atribuute ja omadusi ühes kohas ning seejärel levitada toodet kogu organisatsioonis jaemüügikanalitesse, kus see on saadaval.
4.  Lisage tooted sortimentidesse. Sortiment kujutab endast teie jaemüügikanalites pakutavate toodete kogumit. Saate määratleda ühe või mitu sortimenti ja iga toote saab määrata ühte või mitmesse sortimenti. Toodete määramiseks jaemüügikanalitele määrake sortimentid nende jaemüügikanalitele. Sortimendi loomisel saate lisada tooteid, mida pole veel juriidilisele isikule väljastatud. Siiski peate tooted väljastama juriidilisele isikule enne, kui need saab jaemüügikanalitele kättesaadavaks teha.
5.  Lisada navigeerimishierarhiat. Enne toodete võimalik sirvida online või peasilindri Müügikoht (POS), tuleb need liigitada jaemüügi navigeerimine hierarhia.
6.  Toodete lisamiseks kataloogid. Kuigi see on vabatahtlik POS, online kauplustes nõuda, et tooted lisada vähemalt üks kataloog.



