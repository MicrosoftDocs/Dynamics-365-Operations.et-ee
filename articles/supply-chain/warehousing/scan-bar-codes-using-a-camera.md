---
title: Vöötkoodide skannimine kaamera abil teenuses Dynamics 365 for Finance and Operations – Ladustamine
description: Selles teemas selgitatakse, kuidas seadistada Dynamics 365 for Finance and Operationsi moodulit Ladustamine nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e78d0a82d3ca66a6912ea1a9517296ca241edf1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559031"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="2bf30-103">Vöötkoodide skannimine kaamera abil teenuses Dynamics 365 for Finance and Operations – Ladustamine</span><span class="sxs-lookup"><span data-stu-id="2bf30-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bf30-104">Selles teemas selgitatakse, kuidas seadistada Dynamics 365 for Finance and Operationsi moodulit Ladustamine nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.</span><span class="sxs-lookup"><span data-stu-id="2bf30-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="2bf30-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="2bf30-105">Prerequisites</span></span>
<span data-ttu-id="2bf30-106">Selle funktsiooni kasutamiseks peab teil olema installitud mooduli Ladustamine versioon 1.2.0.0 ja teie seadmel peab olema kaamera.</span><span class="sxs-lookup"><span data-stu-id="2bf30-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="2bf30-107">Pärast värskendamist rakenduse avamisel palutakse teilt lubada rakendusel Dynamics 365 for Finance and Operations – Ladustamine kaamerat kasutada.</span><span class="sxs-lookup"><span data-stu-id="2bf30-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="2bf30-108">Kui seadmel ei ole kaamerat, siis viibet ei kuvata ja te ei saa kaamerat skannerina kasutada.</span><span class="sxs-lookup"><span data-stu-id="2bf30-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="2bf30-109">Seadistamine</span><span class="sxs-lookup"><span data-stu-id="2bf30-109">Setup</span></span>
<span data-ttu-id="2bf30-110">Rakenduse Ladustamine kuvasätetes saate valida, kas kaamerat vöötkoodide skannimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="2bf30-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="2bf30-111">Kui lubate valiku **Kaamera kasutamine skannerina**, saate kaamerat kasutada igas sisendväljas, mille eelistatud sisestusrežiim on seatud väärtusele **Skannimine**.</span><span class="sxs-lookup"><span data-stu-id="2bf30-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="2bf30-112">Selleks et määrata, et sisendväli peab olema skannitav, valige rakenduses Dynamics 365 for Finance and Operations lehel **Laorakenduse väljanimed** rakenduses suvandi **Eelistatud sisestusrežiim** sätteks **Skannimine**.</span><span class="sxs-lookup"><span data-stu-id="2bf30-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="2bf30-113">Selle suvandi valimisel saab rakenduses Ladustamine kasutada kaamerat skannimiseks.</span><span class="sxs-lookup"><span data-stu-id="2bf30-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="2bf30-114">Teavet, kuidas rakenduses Ladustamine väljanimesid konfigureerida, leiate teemast [Väljanimede konfigureerimine rakenduses Ladustamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="2bf30-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="2bf30-115">Toetatud vöötkoodivormingud</span><span class="sxs-lookup"><span data-stu-id="2bf30-115">Supported bar code formats</span></span>
<span data-ttu-id="2bf30-116">Toetatud on levinuimad vöötkoodivormingud, sh kood 128, kood 39, kood 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodid.</span><span class="sxs-lookup"><span data-stu-id="2bf30-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="2bf30-117">Navigeerimine</span><span class="sxs-lookup"><span data-stu-id="2bf30-117">Navigation</span></span>
<span data-ttu-id="2bf30-118">Kaameraleht käivitub igal lehel, kus sisestusvälja eelistatud sisestusrežiim on seatud väärtusele Skannimine. Kaameralehel olles kasutage navigeerimiseks järgmiseid valikuid.</span><span class="sxs-lookup"><span data-stu-id="2bf30-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="2bf30-119">Ülesande ja üksikasjade lehele naasmiseks klõpsake tagasi nuppu.</span><span class="sxs-lookup"><span data-stu-id="2bf30-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="2bf30-120">Klõpsake ülesande ja üksikasjade lehel pliiatsi ikooni, et minna lehele, kus saate sisendit käsitsi tippida.</span><span class="sxs-lookup"><span data-stu-id="2bf30-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="2bf30-121">Klõpsake ülesande ja üksikasjade lehel kaamera ikooni, et minna tagasi kaameralehele.</span><span class="sxs-lookup"><span data-stu-id="2bf30-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="2bf30-122">Ülesande ja üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="2bf30-122">Task and details page</span></span> | <span data-ttu-id="2bf30-123">Kaameraleht</span><span class="sxs-lookup"><span data-stu-id="2bf30-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="2bf30-126">Kui klõpsate kaameralehel kaamera nuppu, kuvatakse see vöötkoodi tuvastamise ajal tuhmina.</span><span class="sxs-lookup"><span data-stu-id="2bf30-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="2bf30-127">Kui vöötkoodi 5 sekundi jooksul ei tuvastata, aegub protsess ja kaameranupp muutub uuesti kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="2bf30-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="2bf30-128">Seejärel saate proovida vöötkoodi uuesti skannida.</span><span class="sxs-lookup"><span data-stu-id="2bf30-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="2bf30-129">Kaamerat vöötkoodile suunates hoidke parima tulemuse saavutamiseks vöötkood sulgudega joondatuna.</span><span class="sxs-lookup"><span data-stu-id="2bf30-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="2bf30-130">Kui vöötkoodi skannimine õnnestub, läheb tulemus töötlemisele ja teid suunatakse järgmise etapi juurde.</span><span class="sxs-lookup"><span data-stu-id="2bf30-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="2bf30-131">Kui järgmine etapp sisaldab järjekordset sisendvälja, mille eelistatud sisestusrežiim on seatud väärtusele Skannimine, käivitub kaameraleht uuesti.</span><span class="sxs-lookup"><span data-stu-id="2bf30-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="2bf30-132">Kui järgmine etapp ei sisalda skannimisvälja, siis kaameraleht ei käivitu.</span><span class="sxs-lookup"><span data-stu-id="2bf30-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

