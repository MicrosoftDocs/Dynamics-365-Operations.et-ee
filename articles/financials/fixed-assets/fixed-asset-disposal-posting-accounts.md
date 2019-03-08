---
title: Põhivara likvideerimise sisestuskontod
description: Selles teemas selgitatakse, kuidas seadistada pearaamatu sisestuskontosid varade likvideerimiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8e00c00b0cb7058858fde3774941911ce20fb6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "367175"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="54b9b-103">Põhivara likvideerimise sisestuskontod</span><span class="sxs-lookup"><span data-stu-id="54b9b-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54b9b-104">Selles teemas selgitatakse, kuidas seadistada pearaamatu sisestuskontosid varade likvideerimiseks.</span><span class="sxs-lookup"><span data-stu-id="54b9b-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="54b9b-105">Pearaamatusse tehtavate sisestuste seadistamiseks valige lehe Põhivara sisestusreeglid kiirkaardil Pearaamatukontod suvandid Likvideerimine – müük ja Likvideerimine – praak.</span><span class="sxs-lookup"><span data-stu-id="54b9b-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="54b9b-106">Mõlemat tüüpi kannete puhul toimub pearaamatukonto krediteerimine põhivara likvideerimisväärtuse ulatuses.</span><span class="sxs-lookup"><span data-stu-id="54b9b-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="54b9b-107">Deebetsumma sisestatakse vastaskontole , milleks võib olla näiteks pangakonto.</span><span class="sxs-lookup"><span data-stu-id="54b9b-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="54b9b-108">Põhivara müügi puhul kliendile kasutatakse vastaskonto asemel kliendi kontot.</span><span class="sxs-lookup"><span data-stu-id="54b9b-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="54b9b-109">Klõpsake suvandit Likvideerimine ja siis suvandit Müük või Praak, seejärel seadistage üksikasjalikud kontod põhivara raamatupidamisliku jääkväärtuse tühistamiseks.</span><span class="sxs-lookup"><span data-stu-id="54b9b-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="54b9b-110">Samuti saate sisestada teabe lehe Likvideerimisparameetrid väljadele Järelväärtus ja Müügiväärtuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="54b9b-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="54b9b-111">Väikese väärtusega vahendite kaustas vähendab põhivara likvideerimiskanne väikese väärtusega vahendite kausta raamatupidamislikku jääkväärtust ainult kasutatud summa võrra.</span><span class="sxs-lookup"><span data-stu-id="54b9b-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="54b9b-112">Kuid kui vara müük ületab väikese väärtusega vahendite kausta raamatupidamisliku jääkväärtuse, väheneb raamatupidamislik jääkväärtus nullini.</span><span class="sxs-lookup"><span data-stu-id="54b9b-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>





