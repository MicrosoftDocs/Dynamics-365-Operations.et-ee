---
title: "Pangakonto täpsema vastavusseviimise ülevaade"
description: "Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 33150777222faa97af7488c59ab13cb0fb9e8e2c
ms.contentlocale: et-ee
ms.lasthandoff: 06/29/2017


---

# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="9f115-104">Pangakonto täpsema vastavusseviimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="9f115-104">Advanced bank reconciliation overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9f115-105">Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu.</span><span class="sxs-lookup"><span data-stu-id="9f115-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="9f115-106">Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="9f115-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="9f115-107">Pangakonto täpsema vastavusseviimise funktsioon võimaldab teil pangaväljavõtted importida.</span><span class="sxs-lookup"><span data-stu-id="9f115-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="9f115-108">Imporditud pangaväljavõtte saab seejärel automaatselt pangakannetest vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="9f115-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="9f115-109">Järgmiselt on toodud pangakonto täpsema vastavusseviimise voo etapid.</span><span class="sxs-lookup"><span data-stu-id="9f115-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="9f115-110">Pangaväljavõtte impordi seadistamine.</span><span class="sxs-lookup"><span data-stu-id="9f115-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="9f115-111">Pangaväljavõtete importimine andmeüksuse raamistiku kaudu.</span><span class="sxs-lookup"><span data-stu-id="9f115-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="9f115-112">Kolm tavapärast pangaväljavõtte vormingut on sisse ehitatud: ISO20022, BAI2 ja MT940.</span><span class="sxs-lookup"><span data-stu-id="9f115-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="9f115-113">Funktsiooni saab laiendada mis tahes vormingusse.</span><span class="sxs-lookup"><span data-stu-id="9f115-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="9f115-114">Pangakonto täpsema vastavusseviimise puhul kasutatava numbriseeria seadistamine ja pangakonto vastavusseviimise vastendusreeglite määratlemine.</span><span class="sxs-lookup"><span data-stu-id="9f115-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="9f115-115">Vastavusseviimise vastendusreegel on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja Microsoft Dynamics 365 for Finance and Operationsi, Enterprise edition, pangakande ridade filtrimiseks vastavusseviimise protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="9f115-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="9f115-116">Olenevalt oma äritavast saate vastavusseviimise protsessi automatiseerimiseks ja optimeerimiseks seadistada rohkem kui ühe vastendusreegli.</span><span class="sxs-lookup"><span data-stu-id="9f115-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="9f115-117">Pangaväljavõtete vastavusseviimine Finance and Operationsi pangakannetega.</span><span class="sxs-lookup"><span data-stu-id="9f115-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="9f115-118">Vastavusseviimise töölehtede automaatne võrdlemine ja loomine.</span><span class="sxs-lookup"><span data-stu-id="9f115-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="9f115-119">Pangaväljavõtete ja Finance and Operationsi pangakannete kuvamine kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="9f115-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="9f115-120">Finance and Operationsi pangakannete automaatne sisestamine, kui need kuvatakse pangaväljavõttel, kuid ei kuvata Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="9f115-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="9f115-121">Vastavusseviimiseks väljavõtte loomine.</span><span class="sxs-lookup"><span data-stu-id="9f115-121">Generate a reconciliation statement.</span></span>






