---
title: Klienditeatiste edastamine meili teel
description: Selles teemas selgitatakse, kuidas seadistada reegleid, mis saadavad eelmääratletud sündmuste toimumisel meiliteatisi.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: fe422d645c8f2c0c564af30624090828e10ea4bf
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567248"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="ef77b-103">Kliendi teatiste teatamine meili teel</span><span class="sxs-lookup"><span data-stu-id="ef77b-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef77b-104">Saate määratleda kohandatud teatiste reeglid, mis jälgivad andmete filtreeritud vaateid ja saadavad eelmääratletud sündmuste toimumisel meiliteatise.</span><span class="sxs-lookup"><span data-stu-id="ef77b-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="ef77b-105">Meiliteatiste saatmise suvand on saadaval kõigi toetatud teatisetüüpide puhul ja saate need sisse lülitada ka olemasolevate teatisereeglite puhul.</span><span class="sxs-lookup"><span data-stu-id="ef77b-105">The option to send email notifications is available for all supported alert types and you can also turn them on for existing alert rules.</span></span>

<span data-ttu-id="ef77b-106">Saate sisseehitatud juhtelementide abil luua teatisereeglid, mis jälgivad süsteemi pakett-tööde filtreeritud vaateid.</span><span class="sxs-lookup"><span data-stu-id="ef77b-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="ef77b-107">Jälgides välja **Olek** väärtust, saate konfigureerida ka teatisereeglid, mis saadavad meili pakett-töö nurjumise korral.</span><span class="sxs-lookup"><span data-stu-id="ef77b-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="ef77b-108">Pärast nende teatisereeglite loomist ei pea te äriandmete muudatuste leidmiseks enam aruandeid kontrollima.</span><span class="sxs-lookup"><span data-stu-id="ef77b-108">After you create these alert rules, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="ef77b-109">Selle asemel saate lasta arukal muudatuste tuvastamise teenusel lasta neid enda eest jälgida.</span><span class="sxs-lookup"><span data-stu-id="ef77b-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="ef77b-110">Klienditeatised sõltuvad meili alamsüsteemist, mis on esitatud Microsoft Office’iga integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="ef77b-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="ef77b-111">Soovitame kasutada Simple Mail Transfer Protocoli (SMTP) pakkujat, et meiliedastus ei toetuks ainult kohalikule meilikliendile.</span><span class="sxs-lookup"><span data-stu-id="ef77b-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="ef77b-112">Teatiste saatmiseks meili teel peavad kliendid konfigureerima integreeritud meiliteenused.</span><span class="sxs-lookup"><span data-stu-id="ef77b-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="ef77b-113">Meiliteatised saadetakse adressaatidele teatiseomanike nimel.</span><span class="sxs-lookup"><span data-stu-id="ef77b-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="ef77b-114">Lisateavet meili konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="ef77b-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="ef77b-115">Järgmisel pildil on näidatud dialoogiboks **Teatisereegli loomine**, milles on nüüd ka valik **Saada meil**.</span><span class="sxs-lookup"><span data-stu-id="ef77b-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="ef77b-116">[![Dialoogiboks Teatisereegli loomine, kus suvandi Saada meil sätteks on valitud Jah](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="ef77b-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="ef77b-117">Kui suvandi **Saada meil** sätteks on valitud **Jah**, jätkub teatiste edastamine tegevuskeskusest.</span><span class="sxs-lookup"><span data-stu-id="ef77b-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="ef77b-118">Teatiste meilimallid</span><span class="sxs-lookup"><span data-stu-id="ef77b-118">Alert notification email templates</span></span>

<span data-ttu-id="ef77b-119">Teenus saadab meiliteatised eelmääratletud meilimalle kasutades, mis edastavad teatise põhiandmed.</span><span class="sxs-lookup"><span data-stu-id="ef77b-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="ef77b-120">Järgmisel pildil on näidatud teatiste struktuur, kui need on meili teel vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="ef77b-120">The following image shows the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="ef77b-121">[![Mallipõhised teatised kirje loomise, välja muutmise ja malli kustutamise kohta](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="ef77b-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]