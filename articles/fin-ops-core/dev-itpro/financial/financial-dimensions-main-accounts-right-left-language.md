---
title: Finantsdimensioonid ja põhikontod paremalt vasakule loetavates keeltes
description: See teema kirjeldab mõningaid juurutamisotsuseid, mida tuleb arvestada, kui kasutate paremalt vasakule keelt, ja peate seadistama finantsdimensioonid ja põhikontod.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 36e0af4f1b4fa0013490a2acc2bfcac0de05f5dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185332"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="9f6a3-103">Finantsdimensioonid ja põhikontod paremalt vasakule loetavates keeltes</span><span class="sxs-lookup"><span data-stu-id="9f6a3-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f6a3-104">See teema kirjeldab mõningaid juurutamisotsuseid, mida tuleb arvestada, kui kasutate paremalt vasakule keelt, ja peate seadistama finantsdimensioonid ja põhikontod.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="9f6a3-105">Finantsdimensioonid ja põhikontod on juurutamise plaanimisfaasi põhikomponendid.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="9f6a3-106">Pärast finantsdimensioonide ja põhikontode loomist süsteemis kasutatakse neid lehtedel **Konto struktuuride konfigureerimine**, **Täpsemad konto struktuurid** ja **Finantsdimensiooni konfiguratsioon rakenduste integreerimiseks**.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="9f6a3-107">Nendel lehtedel määratletud tellimust kasutatakse andmete sisestamise ja tarbimise süsteemis.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="9f6a3-108">Mõnes süsteemis kohas ilmuvad finantsdimensioonid ja põhikontod eraldi väljadel.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="9f6a3-109">Teistes kohtades, nagu töölehed, finantsdimensioonid ja põhikontod, ilmuvad need ühe stringina.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="9f6a3-110">Parimad tavad finantsdimensioonide ja põhikontode seadistamiseks paremalt vasakul süsteemis</span><span class="sxs-lookup"><span data-stu-id="9f6a3-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="9f6a3-111">Kui valite kontoplaanide jaoks eraldaja, valige üks eraldaja suvanditest: kaks sidekriipsu (--), kaks pulka (||), kaks punkti (..) või kaks allkriipsu (\_\_).</span><span class="sxs-lookup"><span data-stu-id="9f6a3-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="9f6a3-112">Finantsdimensiooni ja põhikonto väärtuste loomisel kasutage ainult numbreid ja paremalt vasakule keele märke.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="9f6a3-113">Vältige valitud kontoplaani eraldaja kasutamist finantsdimensiooni ja põhikonto väärtustes.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="9f6a3-114">Neid parimaid tavasid järgides saate tagada kasutaja määratletud tellimuse pideva tähistamise kogu süsteemis.</span><span class="sxs-lookup"><span data-stu-id="9f6a3-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>



