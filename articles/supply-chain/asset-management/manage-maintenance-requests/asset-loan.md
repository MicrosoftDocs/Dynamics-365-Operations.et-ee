---
title: Varade laenud
description: Selles teemas kirjeldatakse, kuidas registreerida laenuvarasid varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 355e3d3e0e952db14a03810145528f9701804ca2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022328"
---
# <a name="asset-loans"></a><span data-ttu-id="8f457-103">Varade laenud</span><span class="sxs-lookup"><span data-stu-id="8f457-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8f457-104">Kui teie ettevõte saab varasid remondi- või hooldustööde jaoks kas sisemistest asukohtadest või klientidelt ja kui te ajutiselt laenate varasid nendele asukohtadele või klientidele, saab varahaldus jälgida varalaene.</span><span class="sxs-lookup"><span data-stu-id="8f457-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="8f457-105">Vara laenude registreerimine hooldustaotluse korral</span><span class="sxs-lookup"><span data-stu-id="8f457-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="8f457-106">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Kõik hooldustaotlused** või **Aktiivsed hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="8f457-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="8f457-107">Valige hoolduspäring, kuhu soovite varalaenu registreerida, ja seejärel valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="8f457-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="8f457-108">Lehel **Taotle** valige **Saada laenuvara**.</span><span class="sxs-lookup"><span data-stu-id="8f457-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="8f457-109">Valige vara ja sisestage eeldatav tagastuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="8f457-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="8f457-110">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f457-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="8f457-111">Laenuvara saate saata ainult siis, kui sama vara tüüpi vara on saadaval.</span><span class="sxs-lookup"><span data-stu-id="8f457-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="8f457-112">Varal, mida laenate peab olema vara elutsükli olek, mis võimaldab seda kasutada laenuvarana, nt **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="8f457-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="8f457-113">Kui vara laen on registreeritud, värskendatakse vara elutsükli olekut automaatselt, nt **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="8f457-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="8f457-114">Kõigi teistele asukohtadele või klientidele laenatud varade loendi vaatamiseks valige **Varahaldus**\>**Üldine**\>**Varalaen**\>**Kõik varalaenud**.</span><span class="sxs-lookup"><span data-stu-id="8f457-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="8f457-115">Kui vara jaoks on valitud märkeruut **Lõpetatud**, on vara teie ettevõttele registreeritud kui tagastatud.</span><span class="sxs-lookup"><span data-stu-id="8f457-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Hooldusnõuete haldamine](media/06-manage-maintenance-requests.png)

<span data-ttu-id="8f457-117">Lehel **Aktiivsed varalaenud** saate vaadata loendit kõigist laenuvaradest, mis pole veel teie ettevõttele tagastatud.</span><span class="sxs-lookup"><span data-stu-id="8f457-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="8f457-118">Registreeri laenuvarad kui tagastatud</span><span class="sxs-lookup"><span data-stu-id="8f457-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="8f457-119">Valige **Varahaldus**\>**Üldine**\>**Varalaen**\>**Aktiivsed varalaenud**.</span><span class="sxs-lookup"><span data-stu-id="8f457-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="8f457-120">Valige varalaen, mida soovite registreerida kui tagastatud ja seejärel valige **Tagasta varalaen**.</span><span class="sxs-lookup"><span data-stu-id="8f457-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="8f457-121">Väljale **Tagastatud** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="8f457-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="8f457-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f457-122">Select **OK**.</span></span>
5. <span data-ttu-id="8f457-123">Värskendage loendilehte **Aktiivsed varalaenud** ja märkate, et varalaenu ei kuvata enam loendis.</span><span class="sxs-lookup"><span data-stu-id="8f457-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
