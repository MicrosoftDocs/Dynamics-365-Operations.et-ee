---
title: Tagastuste arvete värskendamine
description: See funktsioon toetab ka äriprotsesse organisatsioonides, mis valivad tagastus- ja müügitellimuste arveldamise ühel ajal ja sama inimese poolt.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d60e29aec1ebdec939aaafc978ee4de04b96136
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983839"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="f1b5e-103">Tagastuste arvete värskendamine</span><span class="sxs-lookup"><span data-stu-id="f1b5e-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f1b5e-104">Tagastustellimus on müügitellimuse tüüp, mis on märgitud kui tagastatud tellimus.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="f1b5e-105">Seetõttu kasutatakse tagastustellimuste arvete loomisel vormi **Tagastustellimused** asemel loendilehte **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="f1b5e-106">See funktsioon toetab ka äriprotsesse organisatsioonides, mis valivad tagastus- ja müügitellimuste arveldamise ühel ajal ja sama inimese poolt.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="f1b5e-107">Kuna tagastatud kauba arve on negatiivse summaga, nimetatakse seda kreeditarveks.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="f1b5e-108">Kui seadistate pakktöötluse jaoks arve värskendamise, peab **tagastatud tellimuse** tüüpi müügitellimusel olema tagastusrea olekuks **Saadud**, mis näitab, et tellimuse saateleht on värskendatud.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="f1b5e-109">Tagastustellimuse arve sisestamine</span><span class="sxs-lookup"><span data-stu-id="f1b5e-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="f1b5e-110">Klõpsake valikuid **Müügireskontro** \> **Üldine** \> **Müügitellimused** \> **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="f1b5e-111">Valige müügitellimus, mille puhul kuvatakse väljal **Tellimuse tüüp** väärtusena **Tagastatud tellimus**.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="f1b5e-112">Klõpsake toimingupaani vahekaardil **Arve** grupis **Loo** valikut **Arve**.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="f1b5e-113">Märkige vahekaardil **Parameetrid** ruut **Sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="f1b5e-114">Vaadake üle vormil kuvatud teave ja tehke vajalikud parandused.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="f1b5e-115">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-115">Click **OK**.</span></span> <span data-ttu-id="f1b5e-116">Kreeditarve sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1b5e-117">Vt ka</span><span class="sxs-lookup"><span data-stu-id="f1b5e-117">See also</span></span>

[<span data-ttu-id="f1b5e-118">Saatelehtede värskendamine tagastamisteks</span><span class="sxs-lookup"><span data-stu-id="f1b5e-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


