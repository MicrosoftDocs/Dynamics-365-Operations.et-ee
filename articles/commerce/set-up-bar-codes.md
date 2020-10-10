---
title: Vöötkoodide häälestamine
description: Selles artiklis kirjeldatakse vöötkoodide kasutamist rakenduses Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0785f499a3e106e36b803ae61a9acbdbb072ce17
ms.sourcegitcommit: 28a771d81322e72d88db63a20ff360de084a6087
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3835058"
---
# <a name="set-up-bar-codes"></a>Vöötkoodide häälestamine

[!include [banner](includes/banner.md)]

Selles artiklis kirjeldatakse vöötkoodide kasutamist rakenduses Dynamics 365 Commerce.

Vöötkoode saate kasutada toodete ostmiseks ja müümiseks, tootevariantide jälgimiseks ning klientide ja töötajate seadistamiseks. Samuti saate vöötkoodide abil väljastada ja heaks kiita kuponge, kinkekaarte ja kreeditarveid. Saate seadistada tooteid, et neil oleks standardsed või kohandatud ettevõttesisesed vöötkoodid. Toodetel võib olla rohkem kui üks vöötkood. Näiteks võib tootel olla mitu vöötkoodi, kui tegemist on erinevate tootjate toodetega või kui sellel on suuruse, stiili või värvi alusel eristatavaid variante. Vöötkoodid võivad sisaldada toote kaalu või hinda. Vöötkoodide maskid on mallid vöötkoodide loomiseks.

> [!NOTE]
> Kui määrate igale variandi kombinatsioonile kordumatu vöötkoodi, saate vöötkoodi kassaaparaadis skannida ja lasta programmil määrata, millist toote varianti müüakse. Samuti saate müügistatistikat variandi kaupa koguda ja kuvada. Igale suuruse, värvi ja stiili grupile saab määrata kordumatu numbri, mis selle grupi vöötkoodis tuvastab. Commerce kasutab vöötkoodi maski vöötkoodide automaatseks loomiseks igale variandikombinatsioonile. Kui suurusi, värve ja stiile on palju, võib see funktsioon kasulik olla, kuna kombinatsioonide arv suureneb oluliselt iga lisatud variandikoodiga. Kui seda funktsiooni ei kasutata, tuleb vöötkoodid määrata igale toote varianti tähistavale kombinatsioonile käsitsi.

Vöötkoode saate luua käsitsi või automaatselt. Vöötkoodide loomiseks tehke järgmised tegevused loetletud järjekorras.

1. [Vöötkoodi maski tähemärkide seadistamine](set-up-bar-code-masks.md).
2. [Vöötkoodi maskide seadistamine](set-up-bar-code-masks.md).
3. Konfigureerige vöötkoodi seadistused.
4. [Looge toodetele vöötkoodid](../supply-chain/pim/tasks/create-bar-code-product.md).

## <a name="additional-resources"></a>Lisaressursid

[Vöötkoodi maskide häälestamine](set-up-bar-code-masks.md)
