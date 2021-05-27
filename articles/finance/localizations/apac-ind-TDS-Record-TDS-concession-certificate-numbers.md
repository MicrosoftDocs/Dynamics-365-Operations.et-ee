---
title: TDS-i kontsessioonisertifikaadi numbrite kirjendamine
description: See teema kirjeldab, kuidas kirjendada mahaarvatud makseallika (TDS) kontsessiooniserdi numbrites, mis väljastatakse hankijatele.
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023166"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="8ed83-103">TDS-i kontsessioonisertifikaadi numbrite kirjendamine</span><span class="sxs-lookup"><span data-stu-id="8ed83-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ed83-104">See teema kirjeldab, kuidas kirjendada mahaarvatud makseallika (TDS) kontsessiooniserdi numbrites, mis väljastatakse hankijatele.</span><span class="sxs-lookup"><span data-stu-id="8ed83-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="8ed83-105">Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Kinnipeetava maksu mööndused**.</span><span class="sxs-lookup"><span data-stu-id="8ed83-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="8ed83-106">Valige **Maksutüübi** väljal **TDS** et kirjendada TDS-maksutüübi kontsessiooniserdid.</span><span class="sxs-lookup"><span data-stu-id="8ed83-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="8ed83-107">Vahekaardil **Ülevaade** valige rea loomiseks **Alt+N**.</span><span class="sxs-lookup"><span data-stu-id="8ed83-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="8ed83-108">[![Uue rea päis](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="8ed83-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="8ed83-109">Väljal **Kinnipeetava maksu kood** valige TDS-maksukood, mille jaoks hankija kontsessioonisertifikaadid välja antakse.</span><span class="sxs-lookup"><span data-stu-id="8ed83-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="8ed83-110">Sisestage väljale **Kinnipeetava maksu nimi** kinnipeetava maksu koodi nimi.</span><span class="sxs-lookup"><span data-stu-id="8ed83-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="8ed83-111">Määratlege **Alates** ja **Kuni kuupäevani** kontsessiooniserdi kehtivuse periood, mis kasutab TDS-i maksukoodi hankija TDS-i kontsessiooni alusel arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="8ed83-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="8ed83-112">Väljale **Märkused** sisestage kõik märkused.</span><span class="sxs-lookup"><span data-stu-id="8ed83-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="8ed83-113">Sisestage **Jaotise** väljale juriidilise sektsiooni kood, mille alusel TDS-i kontsessiooni sert on saadaval.</span><span class="sxs-lookup"><span data-stu-id="8ed83-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="8ed83-114">Kui sektsiooni kood on 197, kuvatakse väärtus "A" nii vormi 26Q veerus "Mahaarvamise mittevähenduse põhjus / väiksem mahaarvamine" kui ka veerus "Mahaarvamise mittevähenduse põhjus / väiksem mahaarvamine/brutokasumine (kui see on olemas)" vormis 27Q.</span><span class="sxs-lookup"><span data-stu-id="8ed83-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="8ed83-115">Kui sektsiooni kood on 197A, kuvatakse mõlemas kohas väärtus "B".</span><span class="sxs-lookup"><span data-stu-id="8ed83-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="8ed83-116">Valige **Serddi** kiirkaart TDS-i kontsessiooniserdi numbrite kirjendamiseks hankijate jaoks.</span><span class="sxs-lookup"><span data-stu-id="8ed83-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="8ed83-117">Väljal **Hankija konto** valige hankija konto, mille jaoks TDS-i kontsessiooni sert välja antakse.</span><span class="sxs-lookup"><span data-stu-id="8ed83-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="8ed83-118">Määratlege **Alates** ja **Kuni** väljaddel kuupäevani TDS-i kontsessiooniserdi kehtivusperiood.</span><span class="sxs-lookup"><span data-stu-id="8ed83-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="8ed83-119">TDS-i arvutamine kontsessiooni alusel põhineb perioodil, mil sert on hankija jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="8ed83-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="8ed83-120">Väljale **Sert** sisestage TDS-i kontsessiooniserdi number.</span><span class="sxs-lookup"><span data-stu-id="8ed83-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="8ed83-121">[![Serdi kiirkaart](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="8ed83-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="8ed83-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8ed83-122">Close the page.</span></span>
