---
title: Väljastatud toote loomiseks ei saa malli rakendada
description: Väljastatud toote loomiseks ei saa malli rakendada.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026432"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="91dd8-103">Väljastatud toote loomiseks ei saa malli rakendada</span><span class="sxs-lookup"><span data-stu-id="91dd8-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="91dd8-104">KB number: 4612097</span><span class="sxs-lookup"><span data-stu-id="91dd8-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="91dd8-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="91dd8-105">Symptoms</span></span>

<span data-ttu-id="91dd8-106">Kui loote uue väljastatud toote dialoogiboksi **Uus väljastatud toode** abil, saate valida malli.</span><span class="sxs-lookup"><span data-stu-id="91dd8-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="91dd8-107">Mall peaks tagama uue väljastatud toote mitme välja vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="91dd8-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="91dd8-108">Kõiki välju ei seadistata aga pärast malli valimist.</span><span class="sxs-lookup"><span data-stu-id="91dd8-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="91dd8-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="91dd8-109">Cause</span></span>

<span data-ttu-id="91dd8-110">Paljud Microsoft Dynamics 365 Supply Chain Management lehed lasevad teil luua malli, mis määrab neile lehtedele näidatavad kirjetele algsätted.</span><span class="sxs-lookup"><span data-stu-id="91dd8-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="91dd8-111">Ühe neist mallidest saate luua valides **Kirje info** vahekaardil **Suvandid** vahekaardil tegevuspaanil.</span><span class="sxs-lookup"><span data-stu-id="91dd8-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="91dd8-112">Väljastatud tooted on siiski palju keerukamad kui enamike teist tüüpi kirjetest.</span><span class="sxs-lookup"><span data-stu-id="91dd8-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="91dd8-113">Kuigi saate malli loomiseks valida **Kirje teabe** **Väljastatud toote** lehel ja saate väljastatud toote loomisel selle malli valida, ei anna mall uue väljastatud toote jaoks oodatud välja väärtusi.</span><span class="sxs-lookup"><span data-stu-id="91dd8-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="91dd8-114">Seetõttu ei saa te väljastatud toodete puhul kasutada kirjeteabe malle.</span><span class="sxs-lookup"><span data-stu-id="91dd8-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="91dd8-115">Selle asemel peate looma sihtotstarbeline tootemallid.</span><span class="sxs-lookup"><span data-stu-id="91dd8-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="91dd8-116">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="91dd8-116">Resolution</span></span>

<span data-ttu-id="91dd8-117">Tootemalli loomiseks kasutage tegevuspaani toote vahekaardil **Malli** menüüd **Toote** vahekaardil mitte **Kirje info** nuppu **Seaded** vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="91dd8-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="91dd8-118">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="91dd8-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="91dd8-119">Valige tegevuspaani vahekaardi **Toode** jaotises **Uus** grupp, valige **Mall** ja siis valige kas **Loo isiklik mall** või **Loo ühismall** vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="91dd8-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
