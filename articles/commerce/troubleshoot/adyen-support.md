---
title: Adyeni probleemide tõrkeotsing rakenduse Dynamics 365 Payment Connector
description: See teema pakub tõrkeotsingu juhendeid, mis aitavad teil tuge saada, kui teil on Microsoft Dynamics 365 Payment Connector for Adyen rakendusega probleemid.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801815"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="8df6d-103">Adyeni probleemide tõrkeotsing rakenduse Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="8df6d-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8df6d-104">See teema pakub tõrkeotsingu juhendeid, mis aitavad teil tuge saada, kui teil on Microsoft Dynamics 365 Payment Connector for Adyen rakendusega probleemid.</span><span class="sxs-lookup"><span data-stu-id="8df6d-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="8df6d-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8df6d-105">Description</span></span>

<span data-ttu-id="8df6d-106">Teil on Adyeni Dynamics 365 Payment Connectoriga probleeme järgmistes valdkondades ja vajate Adyeni meeskonna tuge:</span><span class="sxs-lookup"><span data-stu-id="8df6d-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="8df6d-107">Müügikoha (POS), tänapäevase kassa (MPOS), kõnekeskuse või Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8df6d-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="8df6d-108">Adyeni makseteenuse pakkuja (PSP) viitenumber (nt, kui teil on küsimusi keeldumiste kohta, k.a käsitsi võtmesisestuse \[MKE\] kohta)</span><span class="sxs-lookup"><span data-stu-id="8df6d-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="8df6d-109">Mis ei tööta katse- või reaalajas kaupmehekeskkonnas</span><span class="sxs-lookup"><span data-stu-id="8df6d-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="8df6d-110">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="8df6d-110">Resolution</span></span>

<span data-ttu-id="8df6d-111">Kasutage järgmist e-kirja malli, et käivitada tugiprotsess Veebiteenuse meeskonnaga.</span><span class="sxs-lookup"><span data-stu-id="8df6d-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="8df6d-112">Tõrkeotsingu kiirendamiseks veenduge, et meil sisaldab kõiki vajalikke üksikasju.</span><span class="sxs-lookup"><span data-stu-id="8df6d-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="8df6d-113">Field</span><span class="sxs-lookup"><span data-stu-id="8df6d-113">Field</span></span>        | <span data-ttu-id="8df6d-114">Väärtus</span><span class="sxs-lookup"><span data-stu-id="8df6d-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="8df6d-115">Sihtkoht:</span><span class="sxs-lookup"><span data-stu-id="8df6d-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="8df6d-116">Koopia</span><span class="sxs-lookup"><span data-stu-id="8df6d-116">Cc</span></span>           | |
| <span data-ttu-id="8df6d-117">Teemarida</span><span class="sxs-lookup"><span data-stu-id="8df6d-117">Subject line</span></span> | <span data-ttu-id="8df6d-118">Microsoft Dynamics toetaotlus</span><span class="sxs-lookup"><span data-stu-id="8df6d-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="8df6d-119">Keha</span><span class="sxs-lookup"><span data-stu-id="8df6d-119">Body</span></span>         | <p><span data-ttu-id="8df6d-120">Tere tugi,</span><span class="sxs-lookup"><span data-stu-id="8df6d-120">Hi Support,</span></span></p><p><span data-ttu-id="8df6d-121">Esitage tugi järgmise probleemi puhul:</span><span class="sxs-lookup"><span data-stu-id="8df6d-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="8df6d-122">Kaupmehe konto</span><span class="sxs-lookup"><span data-stu-id="8df6d-122">Merchant account</span></span></li><li><span data-ttu-id="8df6d-123">Keskkond (Test/Prod)</span><span class="sxs-lookup"><span data-stu-id="8df6d-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="8df6d-124">Kanal (kassa/kõnekeskus/äri e-kaubandus)</span><span class="sxs-lookup"><span data-stu-id="8df6d-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="8df6d-125">KASSA viitenumber, kui väljaminek põhines konkreetsele kandele (SELLE viitenumbri leiate kviitungilt, Lülituse kliendialalt või kassaterminali kannete menüült.)</span><span class="sxs-lookup"><span data-stu-id="8df6d-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="8df6d-126">Veateate kuvatõmmis või foto(d), kui see on rakendatav</span><span class="sxs-lookup"><span data-stu-id="8df6d-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="8df6d-127">Sündmusevaaturi logid (.txt vormingus)</span><span class="sxs-lookup"><span data-stu-id="8df6d-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="8df6d-128">Proovitud väljastus- ja tõrkeotsinguetappide kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8df6d-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="8df6d-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8df6d-129">Additional resources</span></span>

[<span data-ttu-id="8df6d-130">Maksete aktsepteerimine Adyen konnektoriga Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8df6d-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="8df6d-131">Dynamics 365 maksekonnektor Adyeni jaoks</span><span class="sxs-lookup"><span data-stu-id="8df6d-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="8df6d-132">Dynamics 365 maksekonnektor Adyeni jaoks</span><span class="sxs-lookup"><span data-stu-id="8df6d-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
