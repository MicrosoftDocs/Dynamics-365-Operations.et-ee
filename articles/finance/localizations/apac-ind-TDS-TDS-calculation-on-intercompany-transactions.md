---
title: TDS-i arvutamine kontsernisisestelt kannetelt
description: Selles teemas kirjeldatakse protsessi, mida kasutatakse allikas (TDS) maha arvatud maksu arvutamiseks kontsernisisestel kannetel faasides.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023181"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="6220c-103">TDS-i arvutamine kontsernisisestelt kannetelt</span><span class="sxs-lookup"><span data-stu-id="6220c-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6220c-104">Selles teemas kirjeldatakse protsessi, mida kasutatakse allikas (TDS) maha arvatud maksu arvutamiseks kontsernisisestel kannetel faasides.</span><span class="sxs-lookup"><span data-stu-id="6220c-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="6220c-105">Kontsernisisese ostutellimuse või müügitellimuse loomisel kasutatakse TDS-i summa arvutamiseks kliendile või hankijale määratud TDS-i vaikegruppi.</span><span class="sxs-lookup"><span data-stu-id="6220c-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="6220c-106">TDS-i summa sisestatakse tagasisaadav või ostureskontrole pärast arve sisestamist.</span><span class="sxs-lookup"><span data-stu-id="6220c-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="6220c-107">Algsele ostutellimusele või müügitellimusele luuakse automaatselt kontsernisisene müügi- või ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="6220c-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="6220c-108">TDS-i vaikegrupp kuvatakse kontsernisisesel tellimusel nii, et TDS-i saab arvutada.</span><span class="sxs-lookup"><span data-stu-id="6220c-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="6220c-109">Saate sisseostjate gruppi muuta.</span><span class="sxs-lookup"><span data-stu-id="6220c-109">You can change the TDS group.</span></span> <span data-ttu-id="6220c-110">Arve saab sisestada ainult siis, kui automaatselt loodud kontsernisisese tellimuse arve netosumma vastab algsel tellimusel olevale arve netosummale.</span><span class="sxs-lookup"><span data-stu-id="6220c-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="6220c-111">(Netosumma on arve summa pärast TDS-i mahaarvamist.)</span><span class="sxs-lookup"><span data-stu-id="6220c-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="6220c-112">Näiteks müügiarve luuakse summale 50 000 ja sellega on seotud **10%** TDS-grupist.</span><span class="sxs-lookup"><span data-stu-id="6220c-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="6220c-113">Sisestatud arve summa on 45 000 ja müügiarve sisestatud TDS-i summa on 5000.</span><span class="sxs-lookup"><span data-stu-id="6220c-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="6220c-114">Kontsernisisese müügitellimuse jaoks luuakse ostutellimus automaatselt ning sellega on seotud **10%** TDS-grupist.</span><span class="sxs-lookup"><span data-stu-id="6220c-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="6220c-115">Kui muudate TDS-grupi **15%** ei saa arvet sisestada, kuna automaatselt loodud kontsernisisese müügitellimuse arve netosumma ei vasta algse müügitellimuse arve netosummale.</span><span class="sxs-lookup"><span data-stu-id="6220c-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="6220c-116">Automaatselt sisestatakse kontsernisisese arve jaoks loodud maksetööleht.</span><span class="sxs-lookup"><span data-stu-id="6220c-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="6220c-117">Maksetöölehte saab sisestada ainult siis, kui selle netomakse summa ühtib algse maksetöölehe netomakse summaga.</span><span class="sxs-lookup"><span data-stu-id="6220c-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
