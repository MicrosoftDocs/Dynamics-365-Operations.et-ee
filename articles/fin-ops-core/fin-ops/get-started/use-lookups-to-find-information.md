---
title: Teabe leidmine otsingute abil
description: Selles teemas saate teada otsingufunktsioonide kohta ja saate mõned näpunäited, et süsteemis otsinguid optimaalselt kasutada.
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adb8e1a0fef93fdd66a4cbac82689ff7a19aca4a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754772"
---
# <a name="find-information-by-using-lookups"></a><span data-ttu-id="9e8d1-103">Teabe leidmiseks otsingute abil</span><span class="sxs-lookup"><span data-stu-id="9e8d1-103">Find information by using lookups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e8d1-104">Paljudel väljadel otsingud, mis saavad aidata teil hõlpsalt õiget või soovitud väärtust leida.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-104">Many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="9e8d1-105">Otsingutele on lisatud mitmed täiustused, mis muudavad need juhtelemendid kasutatavamaks ja kasutajad produktiivsemaks.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-105">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="9e8d1-106">Selles teemas saate teada nende uute otsingufunktsioonide kohta ja saate mõned näpunäited, et süsteemis otsinguid optimaalselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-106">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>

## <a name="responsive-lookups"></a><span data-ttu-id="9e8d1-107">Hästi reageerivad otsingud</span><span class="sxs-lookup"><span data-stu-id="9e8d1-107">Responsive lookups</span></span>

<span data-ttu-id="9e8d1-108">Varasemates versioonides otsingu juhtelemendiga suheldes peaks kasutaja tegema rippmenüü avamiseks selge toimingu.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-108">In previous versions, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="9e8d1-109">Selleks võib sisestada juhtelementi tärni (\*), et filtreerida otsingut juhtelemendi praeguse väärtuse põhjal, klõpsates rippmenüü nuppu või kasutades kiirklahvi **Alt**+**Allanool**.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-109">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="9e8d1-110">Otsingu juhtelemente on muudetud järgmistel viisidel, et paremini ühtida praeguste veebitavadega.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-110">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

- <span data-ttu-id="9e8d1-111">Otsingu rippmenüüd avanevad nüüd automaatselt pärast väikest pausi tippimisel ja rippmenüü sisu filtreeritakse otsingu juhtelemendi väärtuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-111">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>

    <span data-ttu-id="9e8d1-112">Pange tähele, et rippmenüü automaatse avanemise vana käitumine pärast tärni (\*) sisestamist on aegunud.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-112">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>

- <span data-ttu-id="9e8d1-113">Pärast otsingu rippmenüü avamist toimub järgmine.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-113">After the lookup drop-down menu has opened, the following will occur:</span></span>

    - <span data-ttu-id="9e8d1-114">Kursor püsib otsingu juhtelemendis (selle asemel, et fookus liiguks rippmenüüsse), et saaksite jätkata juhtelemendi väärtusele muudatuste tegemist.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-114">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="9e8d1-115">Samas saab kasutaja endiselt kasutada klahve **Ülesnool** ja **Allanool**, et muuta rippmenüüs olevaid ridu, ja sisestusklahvi, et valida praegune rippmenüüs olev rida.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-115">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    - <span data-ttu-id="9e8d1-116">Rippmenüü sisu reguleeritakse pärast otsingu juhtelemendi väärtusele mis tahes muudatuste tegemist.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-116">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="9e8d1-117">Näiteks kaaluge otsinguvälja nimega **Linn**.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-117">For example, consider a lookup field called **City**.</span></span>

<span data-ttu-id="9e8d1-118">Kui fookus on väljal **Linn**, saate alustada soovitud linna otsimist, sisestades mõned tähed, nagu „col”.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-118">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span> <span data-ttu-id="9e8d1-119">Pärast tippimise lõpetamist avaneb automaatselt otsing, kus on filtreeritud need linnad, mis algavad tähejadaga „col”.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-119">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span>

<span data-ttu-id="9e8d1-120">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="9e8d1-120">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span>

<span data-ttu-id="9e8d1-121">Sellel hetkel on kursor endiselt otsinguväljal.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-121">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="9e8d1-122">Kui jätkate tippimist, et väärtus oleks „veer”, reguleerub otsingusisu automaatselt, et kajastada kõige värskemat väärtust juhtelemendis.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-122">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span>

![updateFilterLookupExample](./media/updatefilterlookupexample.png)

<span data-ttu-id="9e8d1-124">Isegi kui fookus on ikka otsingu juhtelemendis, saate kasutada ka klahve **Ülesnool** või **Allanool**, et tõsta esile rida, mida soovite valida.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-124">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="9e8d1-125">Kui vajutate klahvi **Enter**, valitakse otsingust esiletõstetud rida ja juhtelemendi väärtust värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-125">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span>

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="9e8d1-127">Rohkemate andmete kui vaid ID-de sisestamine</span><span class="sxs-lookup"><span data-stu-id="9e8d1-127">Typing in more than IDs</span></span>

<span data-ttu-id="9e8d1-128">Andmete sisestamisel on loomulik, et nime osas proovivad kasutajad olemit tähistava identifikaatori asemel tuvastada olemit, nagu klient või hankija.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-128">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="9e8d1-129">Paljud (kuid mitte kõik) otsingud lubavad nüüd kontekstilist andmesisestust.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-129">Many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="9e8d1-130">See mitmekülgne funktsioon võimaldab kasutajal sisestada otsingu juhtelementi ID või vastava nime.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-130">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span>

<span data-ttu-id="9e8d1-131">Näiteks müügitellimuse loomisel arvestage välja **Kliendi konto**.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-131">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="9e8d1-132">See väli näitab kliendi puhul suvandit **Konto ID**, kuid tavaliselt eelistab kasutaja müügitellimuse loomisel sisestada väärtuse **Konto ID** asemel väärtust **Konto nimi**, näiteks väärtuse „US-003” asemel väärtust „Hulgimüük”.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-132">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="9e8d1-133">Kui kasutaja alustas otsingu juhtelementi suvandi **Konto ID** sisestamisega, avaneks rippmenüü automaatselt, nagu on kirjeldatud eelmises jaotises ja kasutaja näeks otsingut sellisena, nagu allpool on näidatud.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-133">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="9e8d1-134">[![Kontekstuaalne otsing kliendi konto ID sisestamisel](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="9e8d1-134">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="9e8d1-135">Siiski saab kasutaja nüüd sisestada ka suvandi **Konto nimi** alguse.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-135">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="9e8d1-136">Selle tuvastamisel näeb kasutaja seejärel järgmist otsingut.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-136">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="9e8d1-137">Pange tähele, kuidas veerg **Nimi** teisaldatakse otsingus esimesse veergu ja kuidas otsingut sorditakse ja filtreeritakse veeru **Nimi** põhjal.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-137">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="9e8d1-138">[![Kontekstuaalne otsing kliendi nime sisestamisel](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="9e8d1-138">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="9e8d1-139">Täpsema filtreerimise ja sortimise jaoks ruudustiku veerupäiste kasutamine</span><span class="sxs-lookup"><span data-stu-id="9e8d1-139">Using grid column headers for more advanced filtering and sorting</span></span>

<span data-ttu-id="9e8d1-140">Eelmises kahes jaotises kirjeldatud otsingu täiustused parandavad suuresti kasutaja võimet navigeerida otsingu ridades, põhinedes otsingu välja **ID** või **Nimi** otsingule „algab väärtusega”.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-140">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="9e8d1-141">Samas on olukordi, kus õige rea leidmiseks on vajalik täpsem filtreerimine (või sortimine).</span><span class="sxs-lookup"><span data-stu-id="9e8d1-141">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="9e8d1-142">Sellistes olukordades peab kasutaja kasutama otsingus ruudustiku veerupäistes olevaid filtreerimis- ja sortimissuvandeid.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-142">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="9e8d1-143">Näiteks arvestage müügitellimuse rida sisestavat töötajat, kes peab tootena määrama õige „kaabli” asukoha.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-143">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="9e8d1-144">Sõna „kaabel” sisestamine juhtelementi **Kaubakood** ei ole abiks, kuna puuduvad tootenimed, mis algavad sõnaga „kaabel”.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-144">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span>

![emptyitemlookup](./media/emptyitemlookup.png)

<span data-ttu-id="9e8d1-146">Selle asemel peab kasutaja eemaldama otsingu juhtelemendi väärtuse, avama otsingu rippmenüü ja filtreerima rippmenüü, kasutades ruudustiku veeru päist, nagu allpool on näidatud.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-146">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="9e8d1-147">Hiirt (või puudutamist) kasutav kasutaja saab lihtsalt klõpsata (või puudutada) mis tahes veerupäist, et saada juurdepääs selle veeru filtreerimise ja sortimise suvanditele.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-147">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="9e8d1-148">Klaviatuuri kasutaja peab lihtsalt vajutama teist korda klahvikombinatsiooni **Alt**+**Alla** **Allanool**, et liigutada fookus rippmenüüle, pärast mida saab kasutaja tabeldusklahvi abil õigesse veergu liikuda ja vajutada seejärel klahvikombinatsiooni **Ctrl**+**G**, et avada ruudustiku veeru päise rippmenüüd.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-148">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span>

<span data-ttu-id="9e8d1-149">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="9e8d1-149">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span>

<span data-ttu-id="9e8d1-150">Pärast filtri rakendamist (vaadake allolevat pilti) saab kasutaja leida ja valida rea tavapärasel viisil.</span><span class="sxs-lookup"><span data-stu-id="9e8d1-150">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span>

![filtereditemlookup](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]