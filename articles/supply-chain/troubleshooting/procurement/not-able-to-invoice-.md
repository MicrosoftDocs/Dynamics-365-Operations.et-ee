---
title: Te ei saa arvet esitada kliendile suunatud müügitellimuse kohta
description: Pärast valiku Sisesta arve automaatne lubamist ei saa te enam algset müügitellimust ja algset otsetarnega ostutellimust esitada.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026435"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="da558-103">Te ei saa arvet esitada kliendile suunatud müügitellimuse kohta</span><span class="sxs-lookup"><span data-stu-id="da558-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="da558-104">KB number: 4611793</span><span class="sxs-lookup"><span data-stu-id="da558-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="da558-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="da558-105">Symptoms</span></span>

<span data-ttu-id="da558-106">Pärast valiku **Sisesta arve automaatne** hankijale lubamist ei saa te enam algset müügitellimust ja algset **otsetarnega** ostutellimust esitada.</span><span class="sxs-lookup"><span data-stu-id="da558-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="da558-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="da558-107">Resolution</span></span>

<span data-ttu-id="da558-108">Kontsernisiseste ja otsetarnete tellimuste arvete sünkroonimiskäitumist kontrollivad ja jõustavad parameetrid, mida on kirjeldatud jaotises [Parameetrite seadistamine ettevõttevahelise tellimuse postitamiseks](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="da558-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="da558-109">Pärast nende parameetrite seadistamist peate esmalt esitama arve ettevõttevahelise müügitellimuse kohta.</span><span class="sxs-lookup"><span data-stu-id="da558-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="da558-110">Seejärel sünkroonitakse algsed müügitellimused ja ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="da558-110">The original sales orders and purchase orders will then be synchronized.</span></span>
