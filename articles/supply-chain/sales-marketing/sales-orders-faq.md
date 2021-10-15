---
title: Korduma kippuvad küsimused müügitellimuste kohta
description: Sellel lehel käsitletakse korduma kippuvaid küsimusi, mis tekivad müügitellimustega töötamisel rakenduses Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571613"
---
# <a name="sales-order-faqs"></a>Müügitellimuse KKK-d

Sellel lehel käsitletakse korduma kippuvaid küsimusi, mis tekivad müügitellimustega töötamisel rakenduses Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kas saan nõudluse täitmiseks siduda ostutellimuse müügitellimusega?

Te saate luua ostutellimuse müügitellimuse põhjal. Lisateavet leiate teemast [Ostutellimuse loomine müügitellimuse põhjal](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Kas ma saan müügitellimuse või tagastustellimuse tühistada või kustutada?

Saate tühistada ainult müügitellimusi ja tagastustellimusi, mille olek on *Loodud*. Lisateavet vt teemast [Tagastustellimuse tühistamine](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kas saan taastada kustutatud arveldatud müügitellimuse?

Juhul kui arveldatud müügitellimus kustutati kogemata, saate selle taastada või vaadata selle üksikasju.

Minge **Kliendikonto \> Kannete \> Algdokument \> Kuva üksikasju**. Leidke otsitav arve üles ja valige see, et vaadata selle üksikasju. Need üksikasjad hõlmavad müügitellimuse viidet. Samuti peaks olema sellel lehel võimalik juurde pääseda müügitellimuse üksikasjadele.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Kuidas kustutada hüljatuks jäänud müügitellimuse kirjeid?

Hüljatud müügitellimuskirjete puhastamiseks käivitage perioodiline töö *Müügitellimuse kustutamine* ühes järgmistes kohtadest.

- Müük ja turundus \> Perioodilised ülesanded \> Puhastamine \> Müügitellimuste kustutamine
- Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Puhastamine \> Müügitellimuste kustutamine

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Kas on võimalik arvutada komisjonitasusid arvete puhul, mis on juba sisestatud?

Rakendus Supply Chain Management ei toeta praegu sisestatud arvete puhul komisjonitasude arvutamist.
