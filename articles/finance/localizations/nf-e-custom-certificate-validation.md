---
title: NF-e kohandatud serdi kontrollimine
description: Selles teemas antakse teavet NF-e kohandatud serdi lubamise ja kasutamise kohta.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442300"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="7004c-103">NF-e kohandatud serdi kontrollimine</span><span class="sxs-lookup"><span data-stu-id="7004c-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7004c-104">NF-e kohandatud serdi kontrollimise funktsiooni sisselülitamisel lubab kohandatud kontrollimine ühenduse veebiteenustega.</span><span class="sxs-lookup"><span data-stu-id="7004c-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="7004c-105">See ühendus on vajalik, et edastada NF-e ja lasta SEFAZ-il see autoriseerida.</span><span class="sxs-lookup"><span data-stu-id="7004c-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="7004c-106">Serdi V5 atribuudi **Serveri autentimise eesmärk** väljastab Brasiilia juurserdiamet.</span><span class="sxs-lookup"><span data-stu-id="7004c-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="7004c-107">See atribuut on vaikimisi välja lülitatud ja tuleb lubada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="7004c-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="7004c-108">Mõnel juhul võib automaatne serdi värskendamine selle atribuudi ära keelata.</span><span class="sxs-lookup"><span data-stu-id="7004c-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="7004c-109">Sellisel juhul on TLS-ühendus mõjutatud ning pole enam usaldusväärne.</span><span class="sxs-lookup"><span data-stu-id="7004c-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="7004c-110">Samuti on mõjutatud võime väljastada NF-e-sid tootmiskeskkondades maakondade Minas Gerais (MG) ja Paraná (PR) jaoks.</span><span class="sxs-lookup"><span data-stu-id="7004c-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="7004c-111">See värskendus võimaldab serte kontrollida teisel viisil, mis tähendab, et on võimalik luua turvaline ühendus.</span><span class="sxs-lookup"><span data-stu-id="7004c-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


