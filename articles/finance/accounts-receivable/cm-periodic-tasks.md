---
title: Perioodilised krediidihalduse ülesanded
description: See teema kirjeldab perioodilisi toiminguid, mis on vajalikud klientide krediidilimiitide haldamise protsessis.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b41b87cd3e2e80b87318c5c771d45a4d0e5d4b85
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971699"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="83fe2-103">Perioodilised kreedidihalduse ülesanded</span><span class="sxs-lookup"><span data-stu-id="83fe2-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83fe2-104">See teema kirjeldab perioodilisi toiminguid, mis on vajalikud klientide krediidilimiitide haldamise protsessis.</span><span class="sxs-lookup"><span data-stu-id="83fe2-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="83fe2-105">Värskenda riskiskoore</span><span class="sxs-lookup"><span data-stu-id="83fe2-105">Update risk scores</span></span>

<span data-ttu-id="83fe2-106">Kui ärid arenevad ja asjaolud muutuvad, võivad ka antud kliendi krediidiriskid muutuda.</span><span class="sxs-lookup"><span data-stu-id="83fe2-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="83fe2-107">Oma klientide jaoks sobivate krediidilimiitide säilitamiseks peate perioodiliselt läbi vaatama iga riskiskoori kriteeriumid ja värskendama iga kliendi punktisummad.</span><span class="sxs-lookup"><span data-stu-id="83fe2-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="83fe2-108">Järgmisi punktisummasid saate värskendada lehel **Riskiskooride värskendamine** (**Krediidihaldus ja võlanõuded \> Perioodilised ülesanded \> Krediidihaldus \> Riskiskooride värskendamine**).</span><span class="sxs-lookup"><span data-stu-id="83fe2-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="83fe2-109">Töödeldakse ka kõiki kasutaja määratletud arvutusi.</span><span class="sxs-lookup"><span data-stu-id="83fe2-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="83fe2-110">**Maksmise keskmine päevade arv** – see skoor on keskmine päevade arv, mis kliendil arvete maksmiseks kulub.</span><span class="sxs-lookup"><span data-stu-id="83fe2-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="83fe2-111">**Klient alates** – see skoor on aastate arv, mil klient on teie organisatsiooni klient.</span><span class="sxs-lookup"><span data-stu-id="83fe2-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="83fe2-112">**Äritegevuses alates** – see skoor on aastate arv, mil klient on äritegevuses olnud.</span><span class="sxs-lookup"><span data-stu-id="83fe2-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="83fe2-113">See kasutab väärtust väljal **Ettevõtluse algus** lehel **Kliendid**.</span><span class="sxs-lookup"><span data-stu-id="83fe2-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="83fe2-114">**Laekumata müügi päevad** – see skoor põhineb müügireskontro saldol, müügitulul ja eelmise 12-kuulise perioodi päevade arvul.</span><span class="sxs-lookup"><span data-stu-id="83fe2-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="83fe2-115">**Keskmine saldo** – see punktisumma põhineb eelmise 12-kuulise perioodi müügireskontro saldol.</span><span class="sxs-lookup"><span data-stu-id="83fe2-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="83fe2-116">**Krediidihalduse grupp**, **Konto olek** ja **Riik** – need punktisummad kasutavad kliendi teavet.</span><span class="sxs-lookup"><span data-stu-id="83fe2-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="83fe2-117">Kliendi saldo statistika värskendamine</span><span class="sxs-lookup"><span data-stu-id="83fe2-117">Update customer balance statistics</span></span>

<span data-ttu-id="83fe2-118">Saate käivitada protsessi **Kliendi saldo statistika värskendamine**, et värskendada saldo statistika arvutust, mis kuvatakse lehel **Saldo statistika päring**.</span><span class="sxs-lookup"><span data-stu-id="83fe2-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="83fe2-119">Seda teavet kasutatakse riskiskooride ja krediidistatistika kiirinfo väärtuste kuvamiseks lehel **Klient**.</span><span class="sxs-lookup"><span data-stu-id="83fe2-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="83fe2-120">Protsessi käivitamisel uuendatakse kliendi saldo statistikat ühe kliendi kohta.</span><span class="sxs-lookup"><span data-stu-id="83fe2-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="83fe2-121">Pakett-töö seadistamiseks mitme kliendi protsessi käitamiseks saate kasutada lehte **Saldo statistika arvutamine** (**Krediidihaldus \> Perioodilised ülesanded \> Saldo statistika arvutamine**).</span><span class="sxs-lookup"><span data-stu-id="83fe2-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
