---
title: Avansisaaja kanded
description: Lugege, kuidas töötada avansisaaja kannetega rakenduses Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.reviewer: kfend
ms.custom: 262554
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: edbaebbfed66424ed37104cdd28a87f378b46b4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978300"
---
# <a name="advance-holder-transactions"></a>Avansisaaja kanded

[!include [banner](../includes/banner.md)]

Lugege, kuidas töötada avansisaaja kannetega.

Avansisaajast töötajate kandeid saab sisestada avansisaaja kontode abil. Igale avansisaajale määratud töötaja ID alusel saab jälgida kõiki avansisaajate kandeid. See number tuuakse avansisaaja kannete jaoks kontonumbrina lehtedel **Päevaraamatud** ja **Avansisaajate kanded**.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Ostutellimuse loomine ja sisestamine avansisaaja andmetega
Täpsemat teavet ostutellimuste kohta vt teemast [Ostutellimuse ülevaade](../../supply-chain/procurement/purchase-order-overview.md). Hankija arve loomisel ja sisestamisel avansisaaja andmetega sisestatakse avansisaaja saldod töövõtja saldokontole, mitte hankija saldokontole. Ostutellimusele avansisaaja andmete lisamiseks tehke järgmist.

-   Valige jaotises **Hind ja allahindlus** väljal **Maksetingimused** maksetingimus. <!---For more information about **Terms of payment**, see [Define vendor payment terms](../accounts-payable/tasks/define-vendor-payment-terms.md).--> Valige maksetingimus, millel on suvand **Avansisaajalt** valitud lehel **Maksetingimused**. Lisateavet avansisaajate maksetingimuste seadistamise kohta vt teemast [Avansisaajate ülevaade](emea-advance-holders.md).
-   Valige kiirkaardi **Hind ja allahindlus** väljal **Avansisaaja** ostutellimuse avansisaaja.

Ostutellimuse sisestusprotsess loob kaks hankija kannet vastandsummadega ja ühe avansisaaja kande. Ilma avansisaaja andmetega luuakse ainult üks hankija kanne.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Avansisaaja saldode tasakaalustamine panga kaudu
Avansisaaja saldode tasakaalustamisel panga kaudu luuakse päevaraamatus töölehe sisestused avansisaaja saldode sulgemiseks. Saate seadistada töölehe ja panga koodi lehe **Ostureskontro parameetrid** jaotises **Avansisaajad**. Lisateavet vt teemast [Avansisaajate ülevaade](emea-advance-holders.md). Avansisaaja saldo sulgemiseks panga kaudu avage **Ostureskontro** &gt; **Avansisaajad** &gt; **Avansisaajad**. Klõpsake toimingupaanil nuppu **Saldo** ja seejärel nuppu **Panga kaudu sulgemine**. Sisestage lehel **Panga kaudu sulgemine** järgmine teave.

| Väli                    | Kirjeldus |
|------------------------------|-------------------|
| **Maksekuupäev**          | Sisestage makse sisestamiseks nõutav kuupäev.|
| **Ülekantav summa** | Sisestage sulgemisel saldo summa. Vormi **Saldo** väljal **Summa** näidatud summa kuvatakse vaikimisi. |
| **Automaatne**                | Märkige ruut **Automaatne**, et luua ja sisestada lehel **Ostureskontro parameetrid** eelseadistatud tööleht.|

## <a name="settle-advance-holder-balances-via-cash"></a>Avansisaaja saldode tasakaalustamine kassa kaudu
Avansisaaja saldode tasakaalustamisel kassa kaudu luuakse saatelehe töölehel sisestused avansisaaja saldode sulgemiseks. Saate seadistada töölehe ja kassa koodi lehe **Ostureskontro parameetrid** vahekaardil **Avansisaajad**. Lisateavet vt teemast [Avansisaajate ülevaade](emea-advance-holders.md). Avansisaaja saldo sulgemiseks kassa kaudu avage **Ostureskontro** &gt; **Avansisaajad** &gt; **Avansisaajad**. Klõpsake toimingupaanil nuppu **Saldo** ja seejärel nuppu **Kassa kaudu sulgemine**. Sisestage lehel **Kassa kaudu sulgemine** järgmine teave.

| Väli                    | Kirjeldus
|------------------------------|-----------------|
| **Maksekuupäev**          | Sisestage makse sisestamiseks nõutav kuupäev.|
| **Ülekantav summa** | Sisestage sulgemisel saldo summa. Vormi **Saldo** väljal **Summa** näidatud summa kuvatakse vaikimisi. |
| **Automaatne**                | Märkige ruut **Automaatne**, et luua ja sisestada lehel **Ostureskontro parameetrid** eelseadistatud tööleht automaatselt.     |

Kui summa väljal **Ülekantav summa** on negatiivne. luuakse pärast saatelehe töölehe töötlemist avansisaajale väljaminekuorder, kui saldod on suletud. Kui summa väljal **Ülekantav summa** on positiivne, luuakse korvamisorder.

## <a name="additional-resources"></a>Lisaressursid

- [Avansimakse töötajale (Ida-Euroopa)](tasks/advance-payment-employee.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]