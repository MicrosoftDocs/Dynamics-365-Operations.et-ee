---
title: Vöötkoodide skannimine kaamera abil rakenduses Dynamics 365 for Finance and Operations – Warehousing
description: Selles teemas selgitatakse, kuidas seadistada rakendust Dynamics 365 for Finance and Operations – Warehousing nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9d3b807b18a0a9c7d24763a2a2a7ea9eccf9c2bb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205851"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a><span data-ttu-id="b3893-103">Vöötkoodide skannimine kaamera abil rakenduses Dynamics 365 Supply Chain Management – Ladustamine</span><span class="sxs-lookup"><span data-stu-id="b3893-103">Scan bar codes using a camera in Dynamics 365 Supply Chain Management - Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3893-104">Selles teemas selgitatakse, kuidas seadistada rakendust Dynamics 365 for Finance and Operations – Warehousing nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.</span><span class="sxs-lookup"><span data-stu-id="b3893-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="b3893-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="b3893-105">Prerequisites</span></span>
<span data-ttu-id="b3893-106">Selle funktsiooni kasutamiseks peab teil olema installitud rakenduse Ladustamine versioon 1.2.0.0 ja teie seadmel peab olema kaamera.</span><span class="sxs-lookup"><span data-stu-id="b3893-106">To use this feature, you need to have version 1.2.0.0 of the Warehousing app installed, and your device must have a camera.</span></span> <span data-ttu-id="b3893-107">Pärast värskendamist rakenduse avamisel palutakse teilt lubada rakendusel kaamerat kasutada.</span><span class="sxs-lookup"><span data-stu-id="b3893-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="b3893-108">Kui seadmel ei ole kaamerat, siis viibet ei kuvata ja te ei saa kaamerat skannerina kasutada.</span><span class="sxs-lookup"><span data-stu-id="b3893-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="b3893-109">Seadistamine</span><span class="sxs-lookup"><span data-stu-id="b3893-109">Setup</span></span>
<span data-ttu-id="b3893-110">Rakenduse Ladustamine kuvasätetes saate valida, kas kaamerat vöötkoodide skannimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="b3893-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="b3893-111">Kui lubate valiku **Kaamera kasutamine skannerina**, saate kaamerat kasutada igas sisendväljas, mille eelistatud sisestusrežiim on seatud väärtusele **Skannimine**.</span><span class="sxs-lookup"><span data-stu-id="b3893-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="b3893-112">Selleks et määrata, kas sisendväli peaks olema skannitav, määrake lehel **rakenduse Ladustamine väljade nimed** **Eelistatud sisestusrežiim** olekusse **Skannimine**.</span><span class="sxs-lookup"><span data-stu-id="b3893-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="b3893-113">Selle suvandi valimisel saab rakenduses Ladustamine kasutada kaamerat skannimiseks.</span><span class="sxs-lookup"><span data-stu-id="b3893-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="b3893-114">Teavet, kuidas rakenduses Ladustamine väljanimesid konfigureerida, leiate teemast [Väljanimede konfigureerimine rakenduses Ladustamine](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="b3893-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="b3893-115">Toetatud vöötkoodivormingud</span><span class="sxs-lookup"><span data-stu-id="b3893-115">Supported bar code formats</span></span>
<span data-ttu-id="b3893-116">Toetatud on levinuimad vöötkoodivormingud, sh kood 128, kood 39, kood 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodid.</span><span class="sxs-lookup"><span data-stu-id="b3893-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="b3893-117">Navigeerimine</span><span class="sxs-lookup"><span data-stu-id="b3893-117">Navigation</span></span>
<span data-ttu-id="b3893-118">Kaameraleht käivitub igal lehel, kus sisestusvälja eelistatud sisestusrežiim on seatud väärtusele Skannimine. Kaameralehel olles kasutage navigeerimiseks järgmiseid valikuid.</span><span class="sxs-lookup"><span data-stu-id="b3893-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="b3893-119">Ülesande ja üksikasjade lehele naasmiseks klõpsake tagasi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b3893-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="b3893-120">Klõpsake ülesande ja üksikasjade lehel pliiatsi ikooni, et minna lehele, kus saate sisendit käsitsi tippida.</span><span class="sxs-lookup"><span data-stu-id="b3893-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="b3893-121">Klõpsake ülesande ja üksikasjade lehel kaamera ikooni, et minna tagasi kaameralehele.</span><span class="sxs-lookup"><span data-stu-id="b3893-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="b3893-122">Ülesande ja üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="b3893-122">Task and details page</span></span> | <span data-ttu-id="b3893-123">Kaameraleht</span><span class="sxs-lookup"><span data-stu-id="b3893-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Kaameraga skannimise näidisülesande üksikasjade leht](./media/camera-scanning-example-task-detail-page50.png)          | ![Kaameraga skannimise näidise väiksem kaameraleht](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="b3893-126">Kui klõpsate kaameralehel kaamera nuppu, kuvatakse see vöötkoodi tuvastamise ajal tuhmina.</span><span class="sxs-lookup"><span data-stu-id="b3893-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="b3893-127">Kui vöötkoodi 5 sekundi jooksul ei tuvastata, aegub protsess ja kaameranupp muutub uuesti kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="b3893-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="b3893-128">Seejärel saate proovida vöötkoodi uuesti skannida.</span><span class="sxs-lookup"><span data-stu-id="b3893-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="b3893-129">Kaamerat vöötkoodile suunates hoidke parima tulemuse saavutamiseks vöötkood sulgudega joondatuna.</span><span class="sxs-lookup"><span data-stu-id="b3893-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="b3893-130">Kui vöötkoodi skannimine õnnestub, läheb tulemus töötlemisele ja teid suunatakse järgmise etapi juurde.</span><span class="sxs-lookup"><span data-stu-id="b3893-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="b3893-131">Kui järgmine etapp sisaldab järjekordset sisendvälja, mille eelistatud sisestusrežiim on seatud väärtusele Skannimine, käivitub kaameraleht uuesti.</span><span class="sxs-lookup"><span data-stu-id="b3893-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="b3893-132">Kui järgmine etapp ei sisalda skannimisvälja, siis kaameraleht ei käivitu.</span><span class="sxs-lookup"><span data-stu-id="b3893-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

