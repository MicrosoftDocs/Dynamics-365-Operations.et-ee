---
title: Jaetoodete häälestamine
description: Selles artiklis kirjeldatakse, kuidas seadistada jaetooteid rakenduses Dynamics 365 Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 74fa3a87ac2993adca3edf003bbc39371ce8e289
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024771"
---
# <a name="set-up-retail-products"></a>Jaetoodete häälestamine

[!include [banner](includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas seadistada jaetooteid rakenduses Dynamics 365 Retail.

Enne kui saate tooteid oma jaemüügikanalitel edasimüügiks pakkuda, peate tooted rakenduses Dynamics 365 Retail looma ja konfigureerima. Retail loob organisatsiooni hõlmavaid tooteid tooteetalonis. Saate luua tooted, määratleda toote omadusi ja atribuute ning määrata tooted jaemüügikategooria hierarhiatesse. Selleks et teha tooted jaemüügikanalites kättesaadavaks ja lisada need aktiivsele sortimendile, peate tooted väljastama juriidilistele isikutele, kus need on saadaval. Jaemüügikanalite kaudu müüdavate toodete seadistamiseks täitke järgmised ülesanded.

1. Määratlege jaemüügi tootehierarhia. Retailii kategooriahierarhia funktsioonide kasutamisel saate määratleda jaemüügikategooria hierarhiad oma jaemüügikanalitesse levitatavate toodete grupeerimiseks ja kategoriseerimiseks. Kasutaja määratletavaid ja süsteemi atribuute saab määratleda kategooria tasemel. Seejärel, pärivad kõik kategooriale määratud tooted need atribuudid. Määratleda saab mitu kategooriahierarhiat ja iga toote saab määrata mitmele hierarhiale. Ühes hierarhias saab siiski iga toote määrata ainult ühte kategooriasse.
2. Lisage tooted ja tootevariandid tooteetalonile. Tooteetalonile lisatud tooted esindavad toodete globaalset loendit. Saate lisada tooteid käsitsi, ükshaaval või importida toote andmed hankijatelt.
3. Väljastage tooted juriidilistele isikutele. Jaemüügikanalitele saab kättesaadavaks teha ainult juriidilistele isikutele väljastatud tooteid. Toote algsel määratlemisel määratlege see organisatsiooniülesel tasemel. Seejärel saate valida ühe või mitu juriidilist isikut, kellele toode väljastada. Siis muutub toode kättesaadavaks teie organisatsiooni mitmele jaemüügikanalile. Selle funktsiooni abil saate luua toote ühekorraga, lisada ning värskendada toote atribuute ja omadusi ühes kohas ning seejärel levitada toodet kogu organisatsioonis jaemüügikanalitesse, kus see on saadaval.
4. Lisage tooted sortimentidesse. Sortiment kujutab endast teie jaemüügikanalites pakutavate toodete kogumit. Saate määratleda ühe või mitu sortimenti ja iga toote saab määrata ühte või mitmesse sortimenti. Toodete määramiseks jaemüügikanalitele määrake sortimentid nende jaemüügikanalitele. Sortimendi loomisel saate lisada tooteid, mida pole veel juriidilisele isikule väljastatud. Siiski peate tooted väljastama juriidilisele isikule enne, kui need saab jaemüügikanalitele kättesaadavaks teha.
5. Lisage tooted navigeerimishierarhiatele. Enne kui tooteid saab võrgus või kassas sirvida, tuleb need kategoriseerida jaemüügi navigeerimishierarhias.
6. Lisage kataloogidesse tooted. Kuigi see juhis on kassa jaoks valikuline, nõuavad võrgupoed, et tooteid kaasataks vähemalt ühte kataloogi.
