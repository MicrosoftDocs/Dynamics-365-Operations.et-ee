---
title: Pangakonto täpsema vastavusseviimise ülevaade
description: Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu. Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.
author: panolte
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
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26b6e1e50e5a9b53ca6b5315de760f5bcec4769
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442461"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="803f7-104">Pangakonto täpsema vastavusseviimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="803f7-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="803f7-105">Selles artiklis kirjeldatakse täpsema panga vastavusseviimise protsessi voogu.</span><span class="sxs-lookup"><span data-stu-id="803f7-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="803f7-106">Täpsema panga vastavusseviimise funktsiooni abil saate importida pangaväljavõtteid, mida saab automaatselt pangakannetes vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="803f7-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="803f7-107">Pangakonto täpsema vastavusseviimise funktsioon võimaldab teil pangaväljavõtted importida.</span><span class="sxs-lookup"><span data-stu-id="803f7-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="803f7-108">Imporditud pangaväljavõtte saab seejärel automaatselt pangakannetest vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="803f7-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="803f7-109">Järgmiselt on toodud pangakonto täpsema vastavusseviimise voo etapid.</span><span class="sxs-lookup"><span data-stu-id="803f7-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="803f7-110">Pangaväljavõtte impordi seadistamine.</span><span class="sxs-lookup"><span data-stu-id="803f7-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="803f7-111">Pangaväljavõtete importimine andmeüksuse raamistiku kaudu.</span><span class="sxs-lookup"><span data-stu-id="803f7-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="803f7-112">Kolm tavapärast pangaväljavõtte vormingut on sisse ehitatud: ISO20022, BAI2 ja MT940.</span><span class="sxs-lookup"><span data-stu-id="803f7-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="803f7-113">Funktsiooni saab laiendada mis tahes vormingusse.</span><span class="sxs-lookup"><span data-stu-id="803f7-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="803f7-114">Pangakonto täpsema vastavusseviimise puhul kasutatava numbriseeria seadistamine ja pangakonto vastavusseviimise vastendusreeglite määratlemine.</span><span class="sxs-lookup"><span data-stu-id="803f7-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="803f7-115">Vastavusseviimise vastendusreegel on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja Microsoft Dynamics 365 Finance'i pangakande ridade filtreerimiseks vastavusseviimise protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="803f7-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="803f7-116">Olenevalt oma äritavast saate vastavusseviimise protsessi automatiseerimiseks ja optimeerimiseks seadistada rohkem kui ühe vastendusreegli.</span><span class="sxs-lookup"><span data-stu-id="803f7-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="803f7-117">Pangaväljavõtete vastavusseviimine Finance'i pangakannetega.</span><span class="sxs-lookup"><span data-stu-id="803f7-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="803f7-118">Vastavusseviimise töölehtede automaatne võrdlemine ja loomine.</span><span class="sxs-lookup"><span data-stu-id="803f7-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="803f7-119">Pangaväljavõtete ja Finance'i pangakannete kuvamine kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="803f7-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="803f7-120">Finance'i pangakannete automaatne sisestamine, kui need kuvatakse pangaväljavõttel, kuid ei kuvata rakenduses Finance.</span><span class="sxs-lookup"><span data-stu-id="803f7-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="803f7-121">Vastavusseviimiseks väljavõtte loomine.</span><span class="sxs-lookup"><span data-stu-id="803f7-121">Generate a reconciliation statement.</span></span>





