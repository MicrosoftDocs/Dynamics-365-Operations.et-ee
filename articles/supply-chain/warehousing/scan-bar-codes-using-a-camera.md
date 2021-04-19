---
title: Vöötkoodide skannimine kaamera abil mobiilirakenduses Warehouse Management
description: Selles teemas selgitatakse, kuidas seadistada mobiilirakendust Warehouse Management nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831214"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="df768-103">Vöötkoodide skannimine kaamera abil mobiilirakenduses Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="df768-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df768-104">Selles teemas selgitatakse, kuidas seadistada mobiilirakendust Warehouse Management nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.</span><span class="sxs-lookup"><span data-stu-id="df768-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="df768-105">Seadistus</span><span class="sxs-lookup"><span data-stu-id="df768-105">Setup</span></span>

<span data-ttu-id="df768-106">Mobiilirakenduse Warehouse Management kuvasätetes saate valida, kas kaamerat vöötkoodide skannimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="df768-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="df768-107">Kui lubate valiku **Kaamera kasutamine skannerina**, saate kaamerat kasutada igas sisendväljas, mille eelistatud sisestusrežiim on seatud väärtusele **Skannimine**.</span><span class="sxs-lookup"><span data-stu-id="df768-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="df768-108">Selleks et määrata, kas sisendväli peaks olema skannitav, määrake lehel **rakenduse Ladustamine väljade nimed** **Eelistatud sisestusrežiim** olekusse **Skannimine**.</span><span class="sxs-lookup"><span data-stu-id="df768-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="df768-109">Selle suvandi valimisel saab mobiilirakenduses Warehouse Management kasutada kaamerat skannimiseks.</span><span class="sxs-lookup"><span data-stu-id="df768-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="df768-110">Lisateavet vt [Mobiilirakenduse Warehouse Management väljade konfigureerimine](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="df768-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="df768-111">Toetatud vöötkoodivormingud</span><span class="sxs-lookup"><span data-stu-id="df768-111">Supported bar code formats</span></span>

<span data-ttu-id="df768-112">Toetatud on levinuimad vöötkoodivormingud, sh kood 128, kood 39, kood 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodid.</span><span class="sxs-lookup"><span data-stu-id="df768-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="df768-113">Navigeerimine</span><span class="sxs-lookup"><span data-stu-id="df768-113">Navigation</span></span>

<span data-ttu-id="df768-114">Kaameraleht käivitub igal lehel, kus **sisestusvälja eelistatud sisestusrežiim** on seatud väärtusele *Skannimine*. Kaameralehel olles kasutage navigeerimiseks järgmiseid valikuid.</span><span class="sxs-lookup"><span data-stu-id="df768-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="df768-115">**Ülesande ja üksikasjade** lehele naasmiseks valige tagasi nuppu.</span><span class="sxs-lookup"><span data-stu-id="df768-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="df768-116">Valige **ülesande ja üksikasjade** lehel pliiatsi ikooni, et minna lehele, kus saate sisendit käsitsi tippida.</span><span class="sxs-lookup"><span data-stu-id="df768-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="df768-117">Valige **ülesande ja üksikasjade** lehel kaamera ikooni, et minna tagasi kaameralehele.</span><span class="sxs-lookup"><span data-stu-id="df768-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="df768-118">Kui valite kaameralehel kaamera nuppu, kuvatakse see vöötkoodi tuvastamise ajal tuhmina.</span><span class="sxs-lookup"><span data-stu-id="df768-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="df768-119">Kui vöötkoodi 5 sekundi jooksul ei tuvastata, aegub protsess ja kaameranupp muutub uuesti kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="df768-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="df768-120">Seejärel saate proovida vöötkoodi uuesti skannida.</span><span class="sxs-lookup"><span data-stu-id="df768-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="df768-121">Kaamerat vöötkoodile suunates hoidke parima tulemuse saavutamiseks vöötkood sulgudega joondatuna.</span><span class="sxs-lookup"><span data-stu-id="df768-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="df768-122">Kui vöötkoodi skannimine õnnestub, läheb tulemus töötlemisele ja teid suunatakse järgmise etapi juurde.</span><span class="sxs-lookup"><span data-stu-id="df768-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="df768-123">Kui järgmine etapp sisaldab järjekordset sisendvälja, mille eelistatud sisestusrežiim on seatud väärtusele Skannimine, käivitub kaameraleht uuesti.</span><span class="sxs-lookup"><span data-stu-id="df768-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="df768-124">Kui järgmine etapp ei sisalda skannimisvälja, siis kaameraleht ei käivitu.</span><span class="sxs-lookup"><span data-stu-id="df768-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]