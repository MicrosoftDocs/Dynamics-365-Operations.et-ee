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
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d9c386b5da90918226e8b1a224bf628c65702b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988998"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="40b21-103">Põhivara likvideerimise sisestuskontod</span><span class="sxs-lookup"><span data-stu-id="40b21-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40b21-104">Selles teemas selgitatakse, kuidas seadistada pearaamatu sisestuskontosid varade likvideerimiseks.</span><span class="sxs-lookup"><span data-stu-id="40b21-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="40b21-105">Pearaamatusse tehtavate sisestuste seadistamiseks valige lehe Põhivara sisestusreeglid kiirkaardil Pearaamatukontod suvandid Likvideerimine – müük ja Likvideerimine – praak.</span><span class="sxs-lookup"><span data-stu-id="40b21-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="40b21-106">Mõlemat tüüpi kannete puhul toimub pearaamatukonto krediteerimine põhivara likvideerimisväärtuse ulatuses.</span><span class="sxs-lookup"><span data-stu-id="40b21-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="40b21-107">Deebetsumma sisestatakse vastaskontole , milleks võib olla näiteks pangakonto.</span><span class="sxs-lookup"><span data-stu-id="40b21-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="40b21-108">Põhivara müügi puhul kliendile kasutatakse vastaskonto asemel kliendi kontot.</span><span class="sxs-lookup"><span data-stu-id="40b21-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="40b21-109">Klõpsake suvandit Likvideerimine ja siis suvandit Müük või Praak, seejärel seadistage üksikasjalikud kontod põhivara raamatupidamisliku jääkväärtuse tühistamiseks.</span><span class="sxs-lookup"><span data-stu-id="40b21-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="40b21-110">Samuti saate sisestada teabe lehe Likvideerimisparameetrid väljadele Järelväärtus ja Müügiväärtuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="40b21-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="40b21-111">Väikese väärtusega vahendite kaustas vähendab põhivara likvideerimiskanne väikese väärtusega vahendite kausta raamatupidamislikku jääkväärtust ainult kasutatud summa võrra.</span><span class="sxs-lookup"><span data-stu-id="40b21-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="40b21-112">Kuid kui vara müük ületab väikese väärtusega vahendite kausta raamatupidamisliku jääkväärtuse, väheneb raamatupidamislik jääkväärtus nullini.</span><span class="sxs-lookup"><span data-stu-id="40b21-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>





