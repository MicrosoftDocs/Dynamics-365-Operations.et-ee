---
title: Mitte-vedaja tarneviiside peitmine POS-i saadetise valikutest
description: Selles teemas kirjeldatakse konfiguratsioonivalikut, mis võib takistada mitte-vedaja tarneviisi kuvamist valikutele, kui saadetise tellimused luuakse kassa rakenduses (POS).
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 75e7e8f183982f7829db78eb75b8c29c9ab95e89
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022329"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="68b46-103">Mitte-vedaja tarneviiside peitmine POS-i tarnevalikutest</span><span class="sxs-lookup"><span data-stu-id="68b46-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="68b46-104">Selles teemas kirjeldatakse konfiguratsioonivalikut, mis on saadaval kassarakenduse (POS) jaoks.</span><span class="sxs-lookup"><span data-stu-id="68b46-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="68b46-105">See konfiguratsioonivalik muudab tarneviisi valimise käitumist, kui saadetise tellimused luuakse POS-is.</span><span class="sxs-lookup"><span data-stu-id="68b46-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="68b46-106">Kui kasutajad loovad kliendi saadetise tellimused POS-is, saavad nad valida saadetise tarneviisi.</span><span class="sxs-lookup"><span data-stu-id="68b46-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="68b46-107">See funktsioon on saadaval olenemata sellest, kas kogu tellimus on saadetud või ainult valitud read.</span><span class="sxs-lookup"><span data-stu-id="68b46-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="68b46-108">Vaikimisi kuvatakse dialoogiboksis, kus on valitud tarneviis, kõik kehtivad tarneviisisid kanali, kauba ja tarneaadressi kombinatsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="68b46-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="68b46-109">Need tarneviisid on määratletud peakontori lehel **Tarneviisid** (**Müük ja turundus \> Seadistus \> Jaotus \> Tarneviisid**).</span><span class="sxs-lookup"><span data-stu-id="68b46-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="68b46-110">Dialoogiboksis võidakse valimiseks kuvada ka "mitte-vedaja" tarneviisid, näiteks **Järeletulemine** või **Kättesaamine**.</span><span class="sxs-lookup"><span data-stu-id="68b46-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="68b46-111">Siiski on lisatud funktsioon, mis võimaldab teil peita mitte-vedaja tarneviisid dialoogiboksis.</span><span class="sxs-lookup"><span data-stu-id="68b46-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="68b46-112">Selle funktsiooni sisselülitamiseks määrake vahekaardi **Klienditellimused** lehel **Kaubandusparameetrid** suvandi **Kuva tellimuste lähetamiseks ainult vedajarežiimi valikud** olekuks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="68b46-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="68b46-113">Pärast selle funktsiooni sisselülitamist ja sobivate jaotustööde käitamist teabe sünkroonimiseks kanali andmebaasiga, ei kuvata POS-is saadetise tellimuste loomisel mitte-vedaja tarneviise enam valimiseks.</span><span class="sxs-lookup"><span data-stu-id="68b46-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
