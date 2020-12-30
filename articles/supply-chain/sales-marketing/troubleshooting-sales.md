---
title: Müügitellimuste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada müügitellimustega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426215"
---
# <a name="troubleshoot-sales-orders"></a>Müügitellimuste tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada müügitellimustega töötamisel tekkivaid probleeme.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Maksuteavet ei värskendata, kui muudan müügitellimuse päises asukohta.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui kohta, ladu või tarneaadressi muudetakse kas müügitellimuse päises või reatasemel, ei värskendata juhtumi maksuteavet ridade puhul automaatselt.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud. See probleem ilmneb seetõttu, et tarneaadressi, kohta ja ladu ei muudeta samuti automaatselt reatasemel. Peate need käsitsi värskendama.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Kui samas perioodis või kattuvates perioodides on kaks kaubanduslepet, valitakse alati sama lepperida.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui samas perioodis või kattuvates perioodides on määratletud kaks kaubanduslepet, valitakse sama kaubanduslepe iga kord, kui loote müügitellimuse ridu, mis sisaldavad neid kaupu.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui kindla kuupäevaga on rohkem kui üks kaubanduslepe, valitakse alati kõige madalama hinnaga kaubanduslepe. Lisateabe saamiseks laadige alla järgmine tehniline ülevaade: [kaubanduslepped rakenduses Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kas saan nõudluse täitmiseks siduda ostutellimuse müügitellimusega?

Te saate luua ostutellimuse müügitellimuse põhjal. Lisateavet leiate teemast [Ostutellimuse loomine müügitellimuse põhjal](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Ma ei saa tagastustellimust või müügitellimust tühistada ega kustutada.

Saate tühistada ainult müügitellimusi ja tagastustellimusi, mille olek on *Loodud*. Lisateavet vt teemast [Tagastustellimuse tühistamine](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Kui proovin müügitellimust tühistada, kuvatakse tõrge „Reserveeringuid ei saa eemaldada, kuna loodud on töö, mis sõltub nendest reserveeringutest”.

Kui töö on seotud müügitellimusega, ei saa müügitellimust tühistada enne töö tühistamist. See nõue kehtib ka juhul, kui müügitellimusega seotud töö on suletud.

Selle probleemi lahendamiseks tehke järgmist.

1. Tühistage töö ja pange varud tagasi soovitud asukohta. Valige müügitellimuse asjakohane koorem ja valige koorma real kas **Vähenda komplekteeritud kogust** või toimingupaanil **Tühista töö**.

    Töö olek on nüüd *Tühistatud* ning varude tagasipanemiseks asukohta, mida kirjeldati tühistamise ajal, luuakse automaatselt uus varude liikumise töö, mida ka kohe töödeldakse.

2. Kustutage koorem. Saadetis kustutatakse samuti.
3. Nüüd peaks olema teil võimalik müügitellimust tühistada.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Ma ei saa tühistada kontsernisisest ostutellimust, mis on seotud müügitellimusega.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui proovite tühistada müügitellimusega seotud kontsernisisest ostutellimust, võidakse kuvada järgmine tõrketeade: „Kogust ei saa vähendada, kuna järelejäänud värskendatud kogus muudab märki”.

### <a name="issue-resolution"></a>Probleemi lahendamine

See probleem parandati rakenduse Microsoft Dynamics 365 Supply Chain Management versioonis 10.0.13. Selles ja uuemates versioonides saate nüüd tühistada müügitellimusega seotud kontsernisiseseid ostutellimusi.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kas saan taastada kustutatud arveldatud müügitellimuse?

### <a name="issue-description"></a>Probleemi kirjeldus

Arveldatud müügitellimus kustutati kogemata ja te soovite selle taastada või vaadata selle üksikasju.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui kustutatud müügitellimus on juba arveldatud, valige **Kliendi konto \> Kanded \> Algdokument \> Kuva üksikasjad**. Leidke otsitav arve üles ja valige see, et vaadata selle üksikasju. Need üksikasjad hõlmavad müügitellimuse viidet. Samuti peaks olema sellel lehel võimalik juurde pääseda müügitellimuse üksikasjadele.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Müügitellimuse päise tähtaega pole andmeüksuses SalesOrderHeaderV2Entity.

Üksuses *SalesOrderHeaderV2Entity* pole tähtaja välja.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Ma pean kustutama hüljatud müügitellimuskirjed.

Hüljatud müügitellimuskirjete puhastamiseks käivitage perioodiline töö *Müügitellimuse kustutamine* ühes järgmistes kohtadest.

- Müük ja turundus \> Perioodilised ülesanded \> Puhastamine \> Müügitellimuste kustutamine
- Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Puhastamine \> Müügitellimuste kustutamine

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Kas on võimalik arvutada komisjonitasusid arvete puhul, mis on juba sisestatud?

Rakendus Supply Chain Management ei toeta praegu sisestatud arvete puhul komisjonitasude arvutamist.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Kontsernisiseses protsessis ei toetata kogumiüksust.

Kogumiüksus pole ostutellimuse jaoks saadaval, sest kogumiüksuse müügitellimuse ridu uurides võib märgata, et kogus on *0* (null) ja olek on *Tühistatud*. Selline käitumine on nii kavandatud. Müügitellimus ostab ainult kogumiüksuse komponente. See ei osta kogumiüksust ennast.

Kui peate kogumi ostma, kaaluge, kas peate selle märkima kogumiüksusena, kuna see funktsioon on tegelikult mõeldud tulu tuvastamise stsenaariumide jaoks. Lisateavet kogumiüksuste kohta leiate teemast [Kogumid](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).
