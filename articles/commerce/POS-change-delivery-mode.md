---
title: Tarnerežiimi muutmine kassas
description: Selles teemas kirjeldatakse, kuidas konfigureerida ja kasutada tarnerežiimi muutmise toimingut kassas.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a88ca9cc8fc8cde6d738dbc4fcf474f1e27e05dd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796386"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="efb37-103">Tarnerežiimi muutmine kassas</span><span class="sxs-lookup"><span data-stu-id="efb37-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="efb37-104">Selles teemas kirjeldatakse, kuidas häälestada ja kasutada funktsiooni „tarnerežiimi muutmine” teie kassakeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="efb37-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="efb37-105">Dynamics 365 Commerce'i versioonis 10.0.10 ja uuemates versioonidess on saadaval toiming  **tarnerežiimi muutmine** (647) kassa ekraanipaigutustele lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="efb37-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="efb37-106">Tarnerežiimi muutmise funktsioon võimaldab muuta ühe või mitme saadetise konfigureeritud müügiridade tarnerežiimi kassakandel.</span><span class="sxs-lookup"><span data-stu-id="efb37-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="efb37-107">Commerce'i varasemates versioonides tuli läbida kogu **Saada kõik** ja **Saada valitud** konfiguratsioonivoog, kui sooviti muuta tarneviisi olemasoleval real, mis oli saatmiseks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="efb37-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="efb37-108">See protsess oli aeganõudev ja võis põhjustada juhuslikke muudatusi selle rea tarnepäritolus või tarnekuupäevades.</span><span class="sxs-lookup"><span data-stu-id="efb37-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="efb37-109">Uus funktsioon pakub alternatiivset viisi nende müügiridade tarnerežiimi tõhusaks uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="efb37-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="efb37-110">Lisateavet selle kohta, kuidas lisada kassanuppude ruudustiku nupule toimingut, vaadake teemast [Kassa ekraanipaigutused](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="efb37-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="efb37-111">Kui see funktsioon on kassas konfigureeritud, valige **Muuda tarnerežiimi**, teile kuvatakse loendileht, mis võimaldab teil valida selle kande read, mille tarnerežiimi soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="efb37-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="efb37-112">Saate valida ainult osad või kõik read või väljuda muudatusi tegemata.</span><span class="sxs-lookup"><span data-stu-id="efb37-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="efb37-113">Varem saadetiseks konfigureeritud müügiread on loendi ainsad read, mida saate muuta.</span><span class="sxs-lookup"><span data-stu-id="efb37-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="efb37-114">Kui soovite muuta komplekteerimise või tarnimiseks järeletulemisena määratud rida saadetiseks, peate kasutama toimingut **Saada kõik** või **Saada valitud**.</span><span class="sxs-lookup"><span data-stu-id="efb37-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="efb37-115">Seevastu kui soovite muuta saadetisena määratud rida komplekteerimiseks või tarnimiseks järeletulemiseks, peate kasutama toiminguid **Komplekteeri kõik**, **Komplekteeri valitud**, **Järeletulemine kõigile** või **Järeletulemine valitutele**.</span><span class="sxs-lookup"><span data-stu-id="efb37-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="efb37-116">Kui olete valinud muudetavad read, klõpsake valikul **Muuda tarnerežiimi**, et saaksite valida tarnerežiimi suvandeid.</span><span class="sxs-lookup"><span data-stu-id="efb37-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="efb37-117">Kui valisite muutmiseks mitu rida, kuvab kassa ainult need tarnerežiimid, mis on konfigureeritud kõigi valitud toodete puhul lubatuks.</span><span class="sxs-lookup"><span data-stu-id="efb37-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="efb37-118">Tarnerežiime saab konfigureerida nii, et need toetaksid kindlaid tooteid ja tarneaadresse.</span><span class="sxs-lookup"><span data-stu-id="efb37-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="efb37-119">Kui on üks tarnerežiim on lubatud ühe toote ja aadressi kombinatsioonile, kuid ei ole lubatud teisele, ei ole see tarnerežiim saadaval.</span><span class="sxs-lookup"><span data-stu-id="efb37-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="efb37-120">Kui soovite valida ühele tootele tarnerežiimi, mis ei ole toetatud teise toote puhul, peate tõenäolisel valima ned read ükshaaval ja muutma tarnerežiimi iga rea kohta eraldi.</span><span class="sxs-lookup"><span data-stu-id="efb37-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="efb37-121">Pärast uue tarnerežiimi valimist kuvatakse kandeleht.</span><span class="sxs-lookup"><span data-stu-id="efb37-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="efb37-122">Uute tarnerežiimi valikute ülevaatamiseks valige kannete loendist vahekaart **Tarne**.</span><span class="sxs-lookup"><span data-stu-id="efb37-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efb37-123">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="efb37-123">Additional resources</span></span>

[<span data-ttu-id="efb37-124">Kõnekeskuse tellimuste loomine</span><span class="sxs-lookup"><span data-stu-id="efb37-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="efb37-125">Kandemeilide kohandamine tarneviisi järgi</span><span class="sxs-lookup"><span data-stu-id="efb37-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]