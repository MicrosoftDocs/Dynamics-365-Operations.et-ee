---
title: Pangatöölehe liitüksuse värskendamine
description: Järgmised etapid on vajalikud, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565913"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="7698b-103">Pangatöölehe liitüksuse värskendamine</span><span class="sxs-lookup"><span data-stu-id="7698b-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7698b-104">Järgmised etapid on vajalikud, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="7698b-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="7698b-105">Kasutage järgmisi etappe, et lisada täiendav väli BankTransactionType liitüksusele BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="7698b-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="7698b-106">Kompileerige ja sünkroonige järgmised panga töölehe liitüksused, üksused ja vahetabelid.</span><span class="sxs-lookup"><span data-stu-id="7698b-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="7698b-107">Liitüksus\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="7698b-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="7698b-108">Üksus\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="7698b-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="7698b-109">Üksus\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="7698b-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="7698b-110">Tabel\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="7698b-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="7698b-111">Tabel\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="7698b-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="7698b-112">Andmehaldus\\andmeprojektid</span><span class="sxs-lookup"><span data-stu-id="7698b-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="7698b-113">Avage tüüp **Pangakanne**paigutuses **Lähteandmed**.</span><span class="sxs-lookup"><span data-stu-id="7698b-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="7698b-114">Lähteandmete vorming = XML-element</span><span class="sxs-lookup"><span data-stu-id="7698b-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="7698b-115">Üksuse nimi = Panga tööleht</span><span class="sxs-lookup"><span data-stu-id="7698b-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="7698b-116">Andmefaili üleslaadimise = uus faili SampleBankJournalCompositeEntity.xml versioon.</span><span class="sxs-lookup"><span data-stu-id="7698b-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="7698b-117">Klõpsake valikut **Jah**, et olemasolev fail üle kirjutada.</span><span class="sxs-lookup"><span data-stu-id="7698b-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="7698b-118">Klõpsake valikut **Jah**, et luua vastendus nullist.</span><span class="sxs-lookup"><span data-stu-id="7698b-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="7698b-119">Kontrollige, kas pangakande tüüp on vastendatud.</span><span class="sxs-lookup"><span data-stu-id="7698b-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="7698b-120">Klõpsake rea üksust **Kuva kaart**.</span><span class="sxs-lookup"><span data-stu-id="7698b-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="7698b-121">Kontrollige, kas pangekande tüüp on vastendatud valikult Allikas valikule Ajastamine.</span><span class="sxs-lookup"><span data-stu-id="7698b-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="7698b-122">Importige uus väljavõte.</span><span class="sxs-lookup"><span data-stu-id="7698b-122">Import the new statement.</span></span>




