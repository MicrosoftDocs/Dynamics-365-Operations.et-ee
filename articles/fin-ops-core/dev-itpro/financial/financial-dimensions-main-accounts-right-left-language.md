---
title: Finantsdimensioonid ja põhikontod paremalt vasakule loetavates keeltes
description: See teema kirjeldab otsuseid, mida tuleb teha, kui kasutate paremalt vasakule keelt ja peate seadistama finantsdimensioonid ning põhikontod.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 508f4ed4de367770acddc77a6ff5e7e36fd20729
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748133"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="5408a-103">Finantsdimensioonid ja põhikontod paremalt vasakule loetavates keeltes</span><span class="sxs-lookup"><span data-stu-id="5408a-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5408a-104">See teema kirjeldab mõningaid juurutamisotsuseid, mida tuleb arvestada, kui kasutate paremalt vasakule keelt, ja peate seadistama finantsdimensioonid ja põhikontod.</span><span class="sxs-lookup"><span data-stu-id="5408a-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="5408a-105">Finantsdimensioonid ja põhikontod on juurutamise plaanimisfaasi põhikomponendid.</span><span class="sxs-lookup"><span data-stu-id="5408a-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="5408a-106">Pärast finantsdimensioonide ja põhikontode loomist süsteemis kasutatakse neid lehtedel **Konto struktuuride konfigureerimine**, **Täpsemad konto struktuurid** ja **Finantsdimensiooni konfiguratsioon rakenduste integreerimiseks**.</span><span class="sxs-lookup"><span data-stu-id="5408a-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="5408a-107">Nendel lehtedel määratletud tellimust kasutatakse andmete sisestamise ja tarbimise süsteemis.</span><span class="sxs-lookup"><span data-stu-id="5408a-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="5408a-108">Mõnes süsteemis kohas ilmuvad finantsdimensioonid ja põhikontod eraldi väljadel.</span><span class="sxs-lookup"><span data-stu-id="5408a-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="5408a-109">Teistes kohtades, nagu töölehed, finantsdimensioonid ja põhikontod, ilmuvad need ühe stringina.</span><span class="sxs-lookup"><span data-stu-id="5408a-109">In other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="5408a-110">Parimad tavad finantsdimensioonide ja põhikontode seadistamiseks paremalt vasakul süsteemis</span><span class="sxs-lookup"><span data-stu-id="5408a-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

- <span data-ttu-id="5408a-111">Kui valite kontoplaanide jaoks eraldaja, valige üks eraldaja suvanditest: kaks sidekriipsu (`--`), kaks pulka (`||`), kaks punkti (`..`) või kaks allkriipsu (`\\`).</span><span class="sxs-lookup"><span data-stu-id="5408a-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (`--`), double bar (`||`), double period (`..`), or double underscore (`\\`).</span></span>
- <span data-ttu-id="5408a-112">Finantsdimensiooni ja põhikonto väärtuste loomisel kasutage ainult numbreid ja paremalt vasakule keele märke.</span><span class="sxs-lookup"><span data-stu-id="5408a-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
- <span data-ttu-id="5408a-113">Vältige valitud kontoplaani eraldaja kasutamist finantsdimensiooni ja põhikonto väärtustes.</span><span class="sxs-lookup"><span data-stu-id="5408a-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="5408a-114">Neid parimaid tavasid järgides saate tagada kasutaja määratletud tellimuse pideva tähistamise kogu süsteemis.</span><span class="sxs-lookup"><span data-stu-id="5408a-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]