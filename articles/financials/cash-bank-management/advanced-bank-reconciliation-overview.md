---
title: Pangakonto täpsema vastavusseviimise ülevaade
description: Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c76b38e957c1c76a80c76782f45405573b7f191
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842605"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="2a418-104">Pangakonto täpsema vastavusseviimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="2a418-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a418-105">Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu.</span><span class="sxs-lookup"><span data-stu-id="2a418-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="2a418-106">Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="2a418-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="2a418-107">Pangakonto täpsema vastavusseviimise funktsioon võimaldab teil pangaväljavõtted importida.</span><span class="sxs-lookup"><span data-stu-id="2a418-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="2a418-108">Imporditud pangaväljavõtte saab seejärel automaatselt pangakannetest vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="2a418-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="2a418-109">Järgmiselt on toodud pangakonto täpsema vastavusseviimise voo etapid.</span><span class="sxs-lookup"><span data-stu-id="2a418-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="2a418-110">Pangaväljavõtte impordi seadistamine.</span><span class="sxs-lookup"><span data-stu-id="2a418-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="2a418-111">Pangaväljavõtete importimine andmeüksuse raamistiku kaudu.</span><span class="sxs-lookup"><span data-stu-id="2a418-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="2a418-112">Kolm tavapärast pangaväljavõtte vormingut on sisse ehitatud: ISO20022, BAI2 ja MT940.</span><span class="sxs-lookup"><span data-stu-id="2a418-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="2a418-113">Funktsiooni saab laiendada mis tahes vormingusse.</span><span class="sxs-lookup"><span data-stu-id="2a418-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="2a418-114">Pangakonto täpsema vastavusseviimise puhul kasutatava numbriseeria seadistamine ja pangakonto vastavusseviimise vastendusreeglite määratlemine.</span><span class="sxs-lookup"><span data-stu-id="2a418-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="2a418-115">Vastavusseviimise vastendusreegel on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja Microsoft Dynamics 365 for Finance and Operationsi pangakande ridade filtreerimiseks vastavusseviimise protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="2a418-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="2a418-116">Olenevalt oma äritavast saate vastavusseviimise protsessi automatiseerimiseks ja optimeerimiseks seadistada rohkem kui ühe vastendusreegli.</span><span class="sxs-lookup"><span data-stu-id="2a418-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="2a418-117">Pangaväljavõtete vastavusseviimine Finance and Operationsi pangakannetega.</span><span class="sxs-lookup"><span data-stu-id="2a418-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="2a418-118">Vastavusseviimise töölehtede automaatne võrdlemine ja loomine.</span><span class="sxs-lookup"><span data-stu-id="2a418-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="2a418-119">Pangaväljavõtete ja Finance and Operationsi pangakannete kuvamine kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="2a418-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="2a418-120">Finance and Operationsi pangakannete automaatne sisestamine, kui need kuvatakse pangaväljavõttel, kuid ei kuvata Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="2a418-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="2a418-121">Vastavusseviimiseks väljavõtte loomine.</span><span class="sxs-lookup"><span data-stu-id="2a418-121">Generate a reconciliation statement.</span></span>





