---
title: Toote andmeüksused
description: Sellest teemast leiate teavet erinevate üksuste kohta, mida saab kasutada toote andmete importimiseks ja eksportimiseks.
author: cvocph
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: e05d5febdd57a25d796fb3d085390758f5e7ceca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007762"
---
# <a name="product-data-entities"></a>Toote andmeüksused

[!include [banner](../includes/banner.md)]

Toote andmete importimiseks ja eksportimiseks peate kasutama andmeüksuseid. Järgmises tabelis on toodud tootega seotud andmeüksuste üksikasjad ja selles kirjeldatakse iga eesmärki.

| Üksus | Rakendusobjektide puu (AOT) nimi (tüüp) | Märkmed |
|--------|-------------------------------------------|-------|
| Tooted V2 | `EcoResProductV2Entity` | Seda üksust kasutatakse ühiskasutuses toodete, eristatavate toodete ja tooteetalonide importimiseks ja eksportimiseks. See võimaldab uuendusi. See ei toeta komplektil põhinevaid SQL-toiminguid. See on avatud andmeprotokolli (OData) jaoks lubatud. |
| Väljastatud tooted V2 | `EcoResReleasedProductV2Entity` | Seda üksust kasutatakse väljatatud toodete, eristatavate toodete ja tooteetalonide importimiseks ja eksportimiseks. See võimaldab uuendusi. See nõuab, et ühiskasutuses toode oleks juba loodud. Uue väljastatud toote importimisel toimub ühiskasutuses toote vabastamine. Olemas on ka eraldi üksused, mida saab kasutada väljastatud tooteetalonide ja väljastatud eristatavate variantide importimiseks ja eksportimiseks. See üksus ei toeta kogumipõhiseid SQL-toiminguid ega kustutustoiminguid. See on OData jaoks lubatud. |
| Väljastatud toote loomine V2 | `EcoResReleasedProductCreationV2Entity` | Seda üksust kasutatakse jagatud toodete ja väljastatud toodete korraga importimiseks. Kuigi see toetab eksportimisi, ei soovitata seda kasutada, kuna üksuse eesmärk on toote loomine. See ei toeta värskendusi. See toetab piiratud väljade kogumit (toote loomise dialoogiboksis saadaolevad väljad). See ei toeta komplektil põhinevaid SQL-toiminguid. See ei ole OData kaudu kättesaadav. |
| Tootevariandid | `EcoResProductVariantEntity` | Seda üksust kasutatakse ühiskasutuses tootevariantide importimiseks ja eksportimiseks. See võimaldab uuendusi. See nõuab, et dimensiooniväärtused oleks juba loodud. Integratsioonivõti on tooteetalon pluss tootedimensioonid. See üksus ei toeta komplektil põhinevaid SQL-toiminguid. See on OData jaoks lubatud. See toetab kustutustoiminguid. Seda ei saa uute tootedimensioonide lisamise kaudu laiendada. |
| Tootevariandid tootenumbri ID järgi | `EcoResProductNumberIdentifiedProductVariantEntity` | Seda üksust kasutatakse ühiskasutuses tootevariantide importimiseks ja eksportimiseks. See võimaldab uuendusi. See nõuab, et dimensiooniväärtused oleks juba loodud. Integratsioonivõti on tootenumber (ent üksuse **Tootevariandid** integratsioonivõti on tooteetalon pluss tootedimensioonid). |
| Väljastatud tootevariandid | `EcoResReleasedProductVariantEntity` | Seda üksust kasutatakse väljastatud tootevariantide importimiseks ja eksportimiseks. See võimaldab uuendusi. See nõuab, et ühiskasutuses tootevariandid oleks juba loodud. Uue väljastatud tootevariandi importimisel toimub ühiskasutuses tootevariandi vabastamine. See üksus ei toeta komplektil põhinevaid SQL-toiminguid. See on OData jaoks lubatud. Kuigi see toetab kustutustoiminguid, mille kasutamine põhjustab hetkel andmete rikkumist praeguse platvormi vea tõttu. Seda üksust ei saa uute tootedimensioonide lisamise kaudu laiendada. |
| Väljastatud tootevariandid tootenumbri ID järgi | `EcoResProductNumberIdentifiedReleasedProductVariantEntity` | See üksus sarnaneb üksusele **Väljastatud tootevariandid**, kuid integratsioonivõti on tootenumber, mitte tooteetalon pluss tootedimensioonid. Seda saab uute tootedimensioonide lisamise kaudu laiendada. |
| Müüdavad väljastatud tooted | `EcoResSellableReleasedProductEntity` | Seda üksust kasutatakse ainult müüdavate toodete eksportimiseks. Müüdavad tooted on toote, mis omavat teavet, mida need müügitellimuses kasutamiseks vajavad. Samad reeglid kehtivad, kui toode valideeritakse funktsiooniga **Valideeri** lehel **Vabastatud tooted**. |
| Väljastatud eristatavad tooted V2 | `EcoResDistinctProductV2Entity` | Seda üksust kasutatakse eristatavate toodete eksportimiseks. Need eristatavad tooted võivad olla tooted, alamtüübi tooted ja tootevariandid. |
| Väljastatud tooteetalonid V2 | `EcoResProductMasterV2Entity` | Seda üksust kasutatakse tooteetalonide importimiseks ja eksportimiseks. See pole andmehalduse jaoks lubatud. |
| Kaup – vöötkood | `EcoResProductBarcodeEntityV3` | Seda üksust kasutatakse toodete ja vöötkoodide eksportimiseks. Selle üksuse korral pole lubatud muudatuste jälgimine, värskendamine ega kustutamine. Vöötkoodide muudatuste jälgimiseks, värskendamiseks või kustutamiseks kasutage üksust **Kauba ja vöötkoodi seos**. |
| Kauba ja vöötkoodi seos | `EcoResProductBarcodeAssociationEntity` | Seda üksust kasutatakse toodete ja vöötkoodide eksportimiseks. See võimaldab jälgida muudatusi, värskendada ja kustutada. Üksuse kasutamiseks peab funktsioon *Kauba ja vöötkoodi täiustused* olema lubatud [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Selle üksusevõti on `AssociationID`, mis loob seose vöötkoodi ja toote vahel. Selle võtme toe lisamiseks asustatakse tabel `InventitemBarcodeAssociation` olemasoleva kauba vöötkoodiandmetega, kui lülitate funktsiooni sisse. Tabel asustatakse pakett-töö kaudu ja kui vöötkoodi tabelil on palju kirjeid, võib pakett-töö käitamiseks kuluda palju aega. Seetõttu soovitame teil funktsioon lubada (ja seega pakett-töö käitada) ajal, mis sobib teie ettevõtte graafikuga. |
| Toote elutsükli olekud | `EcoResProductLifecycleSateEntity` | Seda üksust kasutatakse erinevate toote töötsükli olekute importimiseks ja eksportimiseks, mida saab tootele määrata. |

> [!NOTE]
> Saate kasutada andmeüksust **Väljastatud tooted V2** toodete süsteemi importimiseks ainult siis, kui ühiskasutuses toode on juba loodud. Vastasel juhul tuleb toodete süsteemi importimiseks kasutada andmeüksust **Toote loomine**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]