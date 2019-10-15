---
title: Olekuga Tühi tšekkide loomine
description: Selles teemas selgitatakse, kuidas luua lehel Tšekid pangakontole tühje tšekke.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: af79dd4831f2e7fc71c296922d73a9e42f7955b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175899"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="8c51b-103">Olekuga Tühi tšekkide loomine</span><span class="sxs-lookup"><span data-stu-id="8c51b-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8c51b-104">Selles teemas selgitatakse tühjade tšekkide loomist.</span><span class="sxs-lookup"><span data-stu-id="8c51b-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="8c51b-105">Näiteks võite luua tühja tšeki selleks, et kirjendada tšekki, mis on kahjustatud ja mida ei saa makse tegemiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="8c51b-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="8c51b-106">Lehel **Tšekid** saate teha tšekkide hooldustoiminguid.</span><span class="sxs-lookup"><span data-stu-id="8c51b-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="8c51b-107">Näiteks saate luua uusi tšekinumbreid ja tšekke kustutada.</span><span class="sxs-lookup"><span data-stu-id="8c51b-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="8c51b-108">Saate luua ka tšekke, mille olek on **Tühi**.</span><span class="sxs-lookup"><span data-stu-id="8c51b-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="8c51b-109">Pärast tühja tšeki loomist ei saa seda süsteemist kustutada ega uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="8c51b-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="8c51b-110">Funktsioon on lehel **Tšekid** saadaval ainult siis, kui lülitate lehel **Funktsioonihaldus** sisse funktsiooni **Lehel Tšekid olekuga Tühi tšekkide loomine**.</span><span class="sxs-lookup"><span data-stu-id="8c51b-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="8c51b-111">Kui funktsioon ei ole sisse lülitatud, saab tšekke olekuga **Tühi** luua ainult dialoogiaknas **Tšekiga maksmine** Ostureskontro maksete loomise protsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="8c51b-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="8c51b-112">Lehe **Tšekid** avamiseks avage **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod** ning valige Tegumiribal vahekaardil **Maksete haldamine** grupis **Seostuv teave** üksus **Tšekid**.</span><span class="sxs-lookup"><span data-stu-id="8c51b-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="8c51b-113">Teise variandina võite avada **Sularaha- ja pangahaldus \> Päringud ja aruanded \> Tšekid**.</span><span class="sxs-lookup"><span data-stu-id="8c51b-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="8c51b-114">Seejärel valige olekuga **Tühi** tšeki loomiseks tegumiribal **Tühjade tšekkide loomine**.</span><span class="sxs-lookup"><span data-stu-id="8c51b-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="8c51b-115">Kui süsteem loob tühja tšekki, on seotud pangakonto ajutiselt inaktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="8c51b-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="8c51b-116">See käitumismudel vähendab ohtu, et makse luuakse samaaegselt tühja tšeki loomisega.</span><span class="sxs-lookup"><span data-stu-id="8c51b-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="8c51b-117">Kui töötlemine on lõpule viidud, aktiveeritakse seotud pangakonto uuesti.</span><span class="sxs-lookup"><span data-stu-id="8c51b-117">When the processing is completed, the associated bank account is reactivated.</span></span>
