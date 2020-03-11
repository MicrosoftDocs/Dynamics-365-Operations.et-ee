---
title: Kohandatud väljade juurutamine mobiilirakenduses Microsoft Dynamics 365 Project Timesheet iOS-is ja Androidis
description: Selles teemas on toodud üldised mustrid laienduste kasutamiseks kohandatud väljade juurutamiseks.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080768"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="b0f64-103">Kohandatud väljade juurutamine mobiilirakenduses Microsoft Dynamics 365 Project Timesheet iOS-is ja Androidis</span><span class="sxs-lookup"><span data-stu-id="b0f64-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0f64-104">Selles teemas on toodud üldised mustrid laienduste kasutamiseks kohandatud väljade juurutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b0f64-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="b0f64-105">Hõlmab järgmisi teemasid.</span><span class="sxs-lookup"><span data-stu-id="b0f64-105">The following topics are covered:</span></span>

- <span data-ttu-id="b0f64-106">Mitmesugused andmetüübid, mida kohandatud välja raamistik toetab</span><span class="sxs-lookup"><span data-stu-id="b0f64-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="b0f64-107">Kirjutuskaitstud või redigeeritavate väljade kuvamine ajatabeli kannetel ja kasutaja esitatud väärtuste salvestamine andmebaasi</span><span class="sxs-lookup"><span data-stu-id="b0f64-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="b0f64-108">Kirjutuskaitstud väljade kuvamine ajatabeli päises</span><span class="sxs-lookup"><span data-stu-id="b0f64-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="b0f64-109">Kohandatud äriloogika integreerimine vaikeväärtuste sisestamiseks väljadesse ja lisakinnituse tegemiseks</span><span class="sxs-lookup"><span data-stu-id="b0f64-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="b0f64-110">Sihtrühm</span><span class="sxs-lookup"><span data-stu-id="b0f64-110">Audience</span></span>

<span data-ttu-id="b0f64-111">See teema on mõeldud arendajatele, kes integreerivad kohandatud välju mobiilirakendusse Microsoft Dynamics 365 Project Timesheet, mis on saadaval Apple iOS-is ja Google Androidis.</span><span class="sxs-lookup"><span data-stu-id="b0f64-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="b0f64-112">Eelduseks on, et lugejad on tuttavad X++ arendusega ja projekti ajatabeli funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="b0f64-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="b0f64-113">Andmeleping – klass TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="b0f64-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="b0f64-114">Klass **TSTimesheetCustomField** X++ andmelepingu klass, mis esitavad teavet ajatabeli funktsiooni kohandatud välja kohta.</span><span class="sxs-lookup"><span data-stu-id="b0f64-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="b0f64-115">Kohandatud välja objektide loendid edastatakse nii andmelepingusse TSTimesheetDetails kui ka andmelepingusse TSTimesheetEntry, et kuvada kohandatud väljad mobiilirakenduses.</span><span class="sxs-lookup"><span data-stu-id="b0f64-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="b0f64-116">**TSTimesheetDetails** – ajatabeli päise leping.</span><span class="sxs-lookup"><span data-stu-id="b0f64-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="b0f64-117">**TSTimesheetEntry** – ajatabeli kande leping.</span><span class="sxs-lookup"><span data-stu-id="b0f64-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="b0f64-118">Nende objektide grupid, millel sama projekti teave ja väärtus **timesheetLineRecId** moodustab rea.</span><span class="sxs-lookup"><span data-stu-id="b0f64-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="b0f64-119">fieldBaseType (tüübid)</span><span class="sxs-lookup"><span data-stu-id="b0f64-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="b0f64-120">Atribuut **FieldBaseType** objektis **TsTimesheetCustom** määrab rakenduses kuvatava välja tüübi.</span><span class="sxs-lookup"><span data-stu-id="b0f64-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="b0f64-121">Järgmisi suvandi **Tüübid** väärtusi toetatakse.</span><span class="sxs-lookup"><span data-stu-id="b0f64-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="b0f64-122">Tüübi väärtus</span><span class="sxs-lookup"><span data-stu-id="b0f64-122">Types value</span></span> | <span data-ttu-id="b0f64-123">Tüüp</span><span class="sxs-lookup"><span data-stu-id="b0f64-123">Type</span></span>              | <span data-ttu-id="b0f64-124">Märkmed</span><span class="sxs-lookup"><span data-stu-id="b0f64-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="b0f64-125">0</span><span class="sxs-lookup"><span data-stu-id="b0f64-125">0</span></span>           | <span data-ttu-id="b0f64-126">String (ja loetelu)</span><span class="sxs-lookup"><span data-stu-id="b0f64-126">String (and Enum)</span></span> | <span data-ttu-id="b0f64-127">Väli kuvatakse tekstiväljana.</span><span class="sxs-lookup"><span data-stu-id="b0f64-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="b0f64-128">1</span><span class="sxs-lookup"><span data-stu-id="b0f64-128">1</span></span>           | <span data-ttu-id="b0f64-129">Täisarv</span><span class="sxs-lookup"><span data-stu-id="b0f64-129">Integer</span></span>           | <span data-ttu-id="b0f64-130">Väärtus kuvatakse numbrina ilma komakohtadeta.</span><span class="sxs-lookup"><span data-stu-id="b0f64-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="b0f64-131">2</span><span class="sxs-lookup"><span data-stu-id="b0f64-131">2</span></span>           | <span data-ttu-id="b0f64-132">Tegelik</span><span class="sxs-lookup"><span data-stu-id="b0f64-132">Real</span></span>              | <span data-ttu-id="b0f64-133">Väärtus kuvatakse numbrina koos komakohtadega.</span><span class="sxs-lookup"><span data-stu-id="b0f64-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="b0f64-134">Tegeliku väärtuse kuvamiseks rakenduses valuutana kasutage atribuuti **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="b0f64-135">Saate kasutada atribuuti **numberOfDecimals** kuvatavate komakohtade arvu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="b0f64-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="b0f64-136">3</span><span class="sxs-lookup"><span data-stu-id="b0f64-136">3</span></span>           | <span data-ttu-id="b0f64-137">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="b0f64-137">Date</span></span>              | <span data-ttu-id="b0f64-138">Kuupäevavormingud määrab kasutaja säte **Kuupäeva, kellaaja ja numbri vorming**, mis on määratud valikuga **Keele ja riigi/regiooni eelistused** jaotises **Kasutaja suvandid**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="b0f64-139">4</span><span class="sxs-lookup"><span data-stu-id="b0f64-139">4</span></span>           | <span data-ttu-id="b0f64-140">Kahendmuutuja</span><span class="sxs-lookup"><span data-stu-id="b0f64-140">Boolean</span></span>           | |
| <span data-ttu-id="b0f64-141">15</span><span class="sxs-lookup"><span data-stu-id="b0f64-141">15</span></span>          | <span data-ttu-id="b0f64-142">GUID</span><span class="sxs-lookup"><span data-stu-id="b0f64-142">GUID</span></span>              | |
| <span data-ttu-id="b0f64-143">16</span><span class="sxs-lookup"><span data-stu-id="b0f64-143">16</span></span>          | <span data-ttu-id="b0f64-144">Int64</span><span class="sxs-lookup"><span data-stu-id="b0f64-144">Int64</span></span>             | |

- <span data-ttu-id="b0f64-145">Kui atribuuti **stringOptions** pole objektis **TSTimesheetCustomField**, esitatakse kasutajale vabas vormis teksti väli.</span><span class="sxs-lookup"><span data-stu-id="b0f64-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="b0f64-146">Atribuuti **stringLength** saab kasutada kasutaja sisestatava stringi maksimaalse pikkuse määramiseks.</span><span class="sxs-lookup"><span data-stu-id="b0f64-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="b0f64-147">Kui atribuuti **stringOptions** pole objektis **TSTimesheetCustomField**, on need loendi elemendid ainsad väärtused, mida kasutajad saavad suvandi nuppudega (raadionuppudega) valida.</span><span class="sxs-lookup"><span data-stu-id="b0f64-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="b0f64-148">Sellisel juhul võib stringiväli toimida loetelu väärtusena kasutaja kirje jaoks.</span><span class="sxs-lookup"><span data-stu-id="b0f64-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="b0f64-149">Väärtuse salvestamiseks andmebaasi loeteluna vastendage enne andmebaasi salvestamist stringiväärtus käsitsi loetelu väärtusega, kasutades käsuliini (vt näidet allpool selle teema jaotises „Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi”).</span><span class="sxs-lookup"><span data-stu-id="b0f64-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="b0f64-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="b0f64-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="b0f64-151">Seda atribuuti saate kasutada tegelike väärtuste vormindamiseks valuutana.</span><span class="sxs-lookup"><span data-stu-id="b0f64-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="b0f64-152">See lähenemine on rakendatav ainult siis, kui väärtus **fieldBaseType** on **Tegelik**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="b0f64-153">**TSCustomFieldExtendedType:None** – vormindamist ei rakendata.</span><span class="sxs-lookup"><span data-stu-id="b0f64-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="b0f64-154">**TSCustomFieldExtendedType::Valuuta** – väärtus vormindatakse valuutana.</span><span class="sxs-lookup"><span data-stu-id="b0f64-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="b0f64-155">Kui valuuta vormindamine on aktiivne, saab välja **stringValue** kasutada valuutakoodi edastamiseks, mis tuleb rakenduses kuvada.</span><span class="sxs-lookup"><span data-stu-id="b0f64-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="b0f64-156">Väärtus on kirjutuskaitstud väärtus.</span><span class="sxs-lookup"><span data-stu-id="b0f64-156">The value is a read-only value.</span></span>

    <span data-ttu-id="b0f64-157">Väli **realValue** sisaldab rahasummat, mis tuleb andmebaasi salvestada.</span><span class="sxs-lookup"><span data-stu-id="b0f64-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="b0f64-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="b0f64-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="b0f64-159">Saate kasutada seda atribuuti, et määrata, kus peaks kohandatud väli rakenduses ilmuma.</span><span class="sxs-lookup"><span data-stu-id="b0f64-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="b0f64-160">**TSCustomFieldSection::Päis** – väli kuvatakse rakenduses jaotises **Kuva rohkem üksikasju**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="b0f64-161">Need väljad on alati kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="b0f64-161">These fields are always read-only.</span></span>
- <span data-ttu-id="b0f64-162">**TSCustomFieldSection::Rida** – väli kuvatakse kõikide valmis reaväljade järel ajatabeli kannetes.</span><span class="sxs-lookup"><span data-stu-id="b0f64-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="b0f64-163">Need väljad võivad olla redigeeritavad või kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="b0f64-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="b0f64-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="b0f64-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="b0f64-165">See atribuut tuvastab välja, kui rakenduse esitatud väärtused salvestatakse tagasi andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="b0f64-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="b0f64-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="b0f64-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="b0f64-167">See atribuut tuvastab välja, kui rakenduse esitatud väärtused salvestatakse tagasi andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="b0f64-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="b0f64-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="b0f64-168">isEditable (NoYes)</span></span>

<span data-ttu-id="b0f64-169">Määrake see atribuut väärtusele **Jah**, et määrata, kas välja ajatabeli kande jaotises saavad kasutajad redigeerida.</span><span class="sxs-lookup"><span data-stu-id="b0f64-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="b0f64-170">Määrake atribuudi väärtuseks **Ei**, et muuta väli kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="b0f64-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="b0f64-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="b0f64-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="b0f64-172">Määrake see atribuut väärtusele **Jah**, et määrata, kas väli ajatabeli kande jaotises peaks olema kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="b0f64-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="b0f64-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="b0f64-173">label (str)</span></span>

<span data-ttu-id="b0f64-174">See atribuut määrab sildi, mis kuvatakse rakenduses välja kõrval.</span><span class="sxs-lookup"><span data-stu-id="b0f64-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="b0f64-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="b0f64-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="b0f64-176">See atribuut on rakendatav ainult siis, kui **fieldBaseType** on seatud väärtusele **String**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="b0f64-177">Kui määratud on **stringOptions**, määratakse loendis olevate stringidega määratud suvandi nuppudega (raadionuppudega) valitavad stringiväärtused.</span><span class="sxs-lookup"><span data-stu-id="b0f64-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="b0f64-178">Kui ühtegi stringi pole olemas, lubatakse stringiväljas vabas vormis teksti kanne (vt näidet allpool selle teema jaotises „„Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi”).</span><span class="sxs-lookup"><span data-stu-id="b0f64-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="b0f64-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="b0f64-179">stringLength (int)</span></span>

<span data-ttu-id="b0f64-180">See atribuut määrab stringivälja maksimaalse pikkuse.</span><span class="sxs-lookup"><span data-stu-id="b0f64-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="b0f64-181">See on rakendatav ainult siis, kui **fieldBaseType** on seatud väärtusele **String**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="b0f64-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="b0f64-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="b0f64-183">See atribuut määrab komakohtade arvu, mida tegeliku välja kohta näidatakse.</span><span class="sxs-lookup"><span data-stu-id="b0f64-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="b0f64-184">See on rakendatav ainult siis, kui **fieldBaseType** on seatud väärtusele **Tegelik**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="b0f64-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="b0f64-185">orderSequence (int)</span></span>

<span data-ttu-id="b0f64-186">See atribuut reguleerib järjekorda, milles kohandatud välju rakenduses kuvatakse, kui määratud on rohkem kui üks kohandatud väli.</span><span class="sxs-lookup"><span data-stu-id="b0f64-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="b0f64-187">Pikemate arvudega väljad kuvatakse enne.</span><span class="sxs-lookup"><span data-stu-id="b0f64-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="b0f64-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="b0f64-188">booleanValue (boolean)</span></span>

<span data-ttu-id="b0f64-189">Tüübi **Boolean** väljade jaoks saadab see atribuut välja Booleani väärtust serveri ja rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="b0f64-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="b0f64-190">guidValue (guid)</span></span>

<span data-ttu-id="b0f64-191">Tüübi **GUID** väljade jaoks saadab see atribuut välja globaalse ainuidentifikaatori (GUID) väärtust serveri ja rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="b0f64-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="b0f64-192">int64Value (int64)</span></span>

<span data-ttu-id="b0f64-193">Tüübi **Int64** väljade jaoks saadab see atribuut välja int64 väärtust serveri ja rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="b0f64-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="b0f64-194">intValue (int)</span></span>

<span data-ttu-id="b0f64-195">Tüübi **Int** väljade jaoks saadab see atribuut välja int väärtust serveri ja rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="b0f64-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="b0f64-196">realValue (real)</span></span>

<span data-ttu-id="b0f64-197">Tüübi **Tegelik** väljade jaoks saadab see atribuut välja tegelikku väärtust serveri ja rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="b0f64-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="b0f64-198">stringValue (str)</span></span>

<span data-ttu-id="b0f64-199">Tüübi **String** väljade jaoks saadab see atribuut välja stringi väärtust serveri ja rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="b0f64-200">Seda kasutatakse ka tüübi **Tegelik** väljade jaoks, mis on vormindatud valuutana.</span><span class="sxs-lookup"><span data-stu-id="b0f64-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="b0f64-201">Nende väljade jaoks kasutatakse atribuuti valuutakoodi saatmiseks rakendusse.</span><span class="sxs-lookup"><span data-stu-id="b0f64-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="b0f64-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="b0f64-202">dateValue (date)</span></span>

<span data-ttu-id="b0f64-203">Tüübi **Kuupäev** väljade jaoks saadab see atribuut välja kuupäeva väärtust serveri ja rakenduse vahel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="b0f64-204">Kohandatud välja kuvamine ja salvestamine ajatabeli kande jaotises</span><span class="sxs-lookup"><span data-stu-id="b0f64-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="b0f64-205">All on mobiilirakenduse kuvatõmmis ajatabeli kande loomisest.</span><span class="sxs-lookup"><span data-stu-id="b0f64-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="b0f64-206">See näitab valmis välju ja kohandatud välja suvandi Ajakirje jaotises Kontrollstring, mille loetelu väärtus Teine suvand on juba määratud.</span><span class="sxs-lookup"><span data-stu-id="b0f64-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Kontrollstringi kohandatud väli rakenduses](media/timesheet-entry.jpg)



<span data-ttu-id="b0f64-208">All on mobiilirakenduse kuvatõmmis, kus kasutaja valib ühe loetelu suvandi, mis on saadaval kohandatud välja Kontrollstring jaoks.</span><span class="sxs-lookup"><span data-stu-id="b0f64-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="b0f64-209">Need kaks suvandit, Esimene suvand ja Teine suvand, kuvatakse raadionuppudena.</span><span class="sxs-lookup"><span data-stu-id="b0f64-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="b0f64-210">Praegu on valitud teine suvand.</span><span class="sxs-lookup"><span data-stu-id="b0f64-210">The second option is currently selected.</span></span>

![Kontrollstringi kohandatud välja suvandi nupud (raadionupud)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="b0f64-212">Tabeli TSTimesheetLine laiendamine, nii et sellel on kohandatud väli</span><span class="sxs-lookup"><span data-stu-id="b0f64-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="b0f64-213">Tavalises stsenaariumis on tõenäoline, et ajatabeli kande jaotise kohandatud välja andmed salvestatakse tabelisse TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="b0f64-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="b0f64-214">Kuid muid tabeleid saab kasutada, kui andmeid saab võtta olemasoleva kirje TSTimesheetTrans põhjal või kui sellel pole konkreetset kirje konteksti (nt kui väli on projekti parameetrites määratud kirjutuskaitstuks).</span><span class="sxs-lookup"><span data-stu-id="b0f64-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="b0f64-215">Pange tähele, et kohandatud väljadel ei pea olema toetavaid andmebaasikirjeid.</span><span class="sxs-lookup"><span data-stu-id="b0f64-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="b0f64-216">Neid saab dünaamiliselt luua X++ loogika põhjal.</span><span class="sxs-lookup"><span data-stu-id="b0f64-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="b0f64-217">See lähenemine võib olla kasulik kirjutuskaitstud stsenaariumide korral (näidet dünaamiliselt loodud kohandatud välja väärtuste kohta vaadake jaotisest „Käsuliini kasutamine klassil TSTimesheetDetails, meetod buildCustomFieldListForHeader ajatabeli üksikasjade täitmiseks”).</span><span class="sxs-lookup"><span data-stu-id="b0f64-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="b0f64-218">All on kuvatõmmis rakendusobjektide puu rakendusest Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b0f64-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="b0f64-219">See kuvab tabeli TSTimesheetLine laienduse, kuhu on kohandatud väljana lisatud väli TestLineString.</span><span class="sxs-lookup"><span data-stu-id="b0f64-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Reastring](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="b0f64-221">Käsuliini kasutamine klassi TSTimesheetSettings meetodil buildCustomFieldList välja kuvamiseks ajatabeli kande jaotises</span><span class="sxs-lookup"><span data-stu-id="b0f64-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="b0f64-222">See kood reguleerib välja kuvasätteid rakenduses.</span><span class="sxs-lookup"><span data-stu-id="b0f64-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="b0f64-223">Näiteks reguleerib see välja tüüpi, silti, seda, kas väli on kohustuslik, ja millises jaotises väli ilmub.</span><span class="sxs-lookup"><span data-stu-id="b0f64-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="b0f64-224">Järgmises näites on näha stringiväli ajakirjetel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="b0f64-225">Sellel väljal on kaks suvandit, **Esimene suvand** ja **Teine suvand**, mis on saadaval suvandi nuppude (raadionuppude) kaudu.</span><span class="sxs-lookup"><span data-stu-id="b0f64-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="b0f64-226">Väli rakenduses on seotud väljaga **TestLineString**, mis lisatakse tabelile TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="b0f64-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="b0f64-227">Pange tähele, et kasutatud on meetodit **TSTimesheetCustomField::newFromMetatdata()** kohandatud välja atribuutide lähtestamise lihtsustamiseks: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ja **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="b0f64-228">Saate neid parameetreid ka eelistuste järgi käsitsi seadistada.</span><span class="sxs-lookup"><span data-stu-id="b0f64-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="b0f64-229">Käsuliini kasutamine klassi TSTimesheetEntry meetodil buildCustomFieldListForEntry väärtuste sisestamiseks ajatabeli kandesse</span><span class="sxs-lookup"><span data-stu-id="b0f64-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="b0f64-230">Meetodit **buildCustomFieldListForEntry** kasutatakse väärtuste sisestamiseks salvestatud ajatabeli ridadele mobiilirakenduses.</span><span class="sxs-lookup"><span data-stu-id="b0f64-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="b0f64-231">See kasutab kirjet TSTimesheetTrans parameetrina.</span><span class="sxs-lookup"><span data-stu-id="b0f64-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="b0f64-232">Välju sellest kirjest saab kasutada kohandatud välja väärtuse täitmiseks rakenduses.</span><span class="sxs-lookup"><span data-stu-id="b0f64-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="b0f64-233">Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi</span><span class="sxs-lookup"><span data-stu-id="b0f64-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="b0f64-234">Kohandatud välja salvestamiseks tagasi andmebaasi tavakasutuse korral peate laiendama mitut meetodit.</span><span class="sxs-lookup"><span data-stu-id="b0f64-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="b0f64-235">Meetodit **timesheetLineNeedsUpdating** kasutatakse määramaks, kas kasutaja on rakenduses rea kirjet muutnud ja kas see tuleb andmebaasi salvestada.</span><span class="sxs-lookup"><span data-stu-id="b0f64-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="b0f64-236">Kui jõudlus pole probleem, saab seda meetodit lihtsustada, et see annaks alati tulemuseks **tõene**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="b0f64-237">Meetodeid **populateTimesheetLineFromEntryDuringCreate** ja **populateTimesheetLineFromEntryDuringUpdate** saab laiendada, nii et need sisestavad väärtused andmebaasikirjesse TSTimesheetLine olemasolevast andmelepingu kirjest TSTimesheetEntry.</span><span class="sxs-lookup"><span data-stu-id="b0f64-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="b0f64-238">Järgnevas näites pange tähele, kuidas on X++ koodiga tehtud vastendamine andmebaasi välja ja kandevälja vahel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="b0f64-239">Meetodit **populateTimesheetWeekFromEntry** saab laiendada ka siis, kui objektiga **TSTimesheetEntry** vastendatud kohandatud väli peab värskendama andmebaasi tabelit TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="b0f64-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="b0f64-240">Järgmises näites salvestatakse kasutaja valitud väärtus **firstOption** või **secondOption** andmebaasi toorstringi väärtusena.</span><span class="sxs-lookup"><span data-stu-id="b0f64-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="b0f64-241">Kui andmebaasi väli on tüüp **Loetelu**, saan neid väärtusi käsitsi vastendada loetelu väärtusega ja seejärel salvestada need loetelu välja andmebaasi tabelis.</span><span class="sxs-lookup"><span data-stu-id="b0f64-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="b0f64-242">Kohandatud välja kuvamine ajatabeli päise jaotises</span><span class="sxs-lookup"><span data-stu-id="b0f64-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="b0f64-243">All on mobiilirakenduse kuvatõmmis ajatabelit vaatavast kasutajast.</span><span class="sxs-lookup"><span data-stu-id="b0f64-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="b0f64-244">Ülevalt paremast nurgast on valitud nupp Lisateave, mis kuvab suvandi Kuva rohkem üksikasju.</span><span class="sxs-lookup"><span data-stu-id="b0f64-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Käsk Kuva rohkem üksikasju](media/show-more.png)

<span data-ttu-id="b0f64-246">All on mobiilirakenduse kuvatõmmis ajatabeli jaotisest Rohkem.</span><span class="sxs-lookup"><span data-stu-id="b0f64-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="b0f64-247">Ajatabeli päise jaotisesse on lisatud kohandatud väli nimega Selle ajatabeli tulususmäär (arvutatud kohandatud väli).</span><span class="sxs-lookup"><span data-stu-id="b0f64-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="b0f64-248">Kohandatud väljale on määratud kirjutuskaitstud väärtus 0,667.</span><span class="sxs-lookup"><span data-stu-id="b0f64-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Jaotis Rohkem](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="b0f64-250">Tabeli TSTimesheetTable laiendamine, nii et sellel on kohandatud väli</span><span class="sxs-lookup"><span data-stu-id="b0f64-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="b0f64-251">Tavalises stsenaariumis on tõenäoline, et päise jaotise kohandatud välja andmed võetakse tabelist TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="b0f64-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="b0f64-252">Kuid muid tabeleid saab kasutada, kui andmeid saab võtta olemasoleva kirje TSTimesheetTable põhjal või kui sellel pole konkreetset kirje konteksti (nt kui väli on projekti parameetrites määratud kirjutuskaitstuks).</span><span class="sxs-lookup"><span data-stu-id="b0f64-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="b0f64-253">Pange tähele, et kohandatud väljadel ei pea olema toetavaid andmebaasikirjeid.</span><span class="sxs-lookup"><span data-stu-id="b0f64-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="b0f64-254">Neid saab dünaamiliselt luua X++ loogika põhjal.</span><span class="sxs-lookup"><span data-stu-id="b0f64-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="b0f64-255">Järgmises näites on näha see lähenemine.</span><span class="sxs-lookup"><span data-stu-id="b0f64-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="b0f64-256">Päise jaotises olevad väljad on rakenduses alati kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="b0f64-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="b0f64-257">Käsuliini kasutamine klassi TSTimesheetSettings meetodil buildCustomFieldList välja kuvamiseks päise jaotises</span><span class="sxs-lookup"><span data-stu-id="b0f64-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="b0f64-258">See kood reguleerib välja kuvasätteid rakenduses.</span><span class="sxs-lookup"><span data-stu-id="b0f64-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="b0f64-259">Näiteks reguleerib see välja tüüpi, silti, seda, kas väli on kohustuslik, ja millises jaotises väli ilmub.</span><span class="sxs-lookup"><span data-stu-id="b0f64-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="b0f64-260">Järgmises näites on näha arvutatud väärtus rakenduse päise jaotises.</span><span class="sxs-lookup"><span data-stu-id="b0f64-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="b0f64-261">Käsuliini kasutamine klassi TSTimesheetDetails meetodil buildCustomFieldListForHeader ajatabeli üksikasjade täitmiseks</span><span class="sxs-lookup"><span data-stu-id="b0f64-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="b0f64-262">Meetodit **buildCustomFieldListForHeader** kasutatakse ajatabeli päise üksikasjade sisestamiseks salvestatud ajatabeli ridadele mobiilirakenduses.</span><span class="sxs-lookup"><span data-stu-id="b0f64-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="b0f64-263">See kasutab kirjet TSTimesheetTable parameetrina.</span><span class="sxs-lookup"><span data-stu-id="b0f64-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="b0f64-264">Välju sellest kirjest saab kasutada kohandatud välja väärtuse täitmiseks rakenduses.</span><span class="sxs-lookup"><span data-stu-id="b0f64-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="b0f64-265">Järgmises näites ei loeta andmebaasist ühtki väärtust.</span><span class="sxs-lookup"><span data-stu-id="b0f64-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="b0f64-266">Selle asemel kasutab see X++ loogikat arvutatud väärtuse loomiseks, mis kuvatakse seejärel rakenduses.</span><span class="sxs-lookup"><span data-stu-id="b0f64-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="b0f64-267">Muud konfigureeritavuse/laiendatavuse võimalused</span><span class="sxs-lookup"><span data-stu-id="b0f64-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="b0f64-268">Lisakinnituse lisamine rakendusele</span><span class="sxs-lookup"><span data-stu-id="b0f64-268">Adding additional validation for the app</span></span>

<span data-ttu-id="b0f64-269">Ajatabeli funktsiooni olemasolev loogika andmebaasi tasemel töötab endiselt ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="b0f64-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="b0f64-270">Salvestamise või esitamise toimingu lõpetamise katkestamiseks ja konkreetse tõrketeate kuvamiseks saate lisada koodile käsuliini laienduse kaudu suvandi **kuvatakse tõrge (teade kasutajale)**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="b0f64-271">Siin on kolm näidet kasulikest laiendatavatest meetoditest.</span><span class="sxs-lookup"><span data-stu-id="b0f64-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="b0f64-272">Kui **validateWrite** tabelis TSTimesheetLine annab ajatabeli rea salvestamise ajal tulemuse **väär**, kuvatakse mobiilirakenduses tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="b0f64-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="b0f64-273">Kui **validateSubmit** tabelis TSTimesheetTable annab ajatabeli esitamise ajal rakenduses tulemuse **väär**, kuvatakse kasutajale tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="b0f64-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="b0f64-274">Käitatakse siiski loogika, mis täidab väljad (näiteks **Rea atribuut**) meetodi **insert** ajal tabelis TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="b0f64-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="b0f64-275">Valmis väljade peitmine ja märkimine kirjutuskaitstuteks konfiguratsiooni kaudu</span><span class="sxs-lookup"><span data-stu-id="b0f64-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="b0f64-276">Projekti parameetrites saate muuta valmis väljad mobiilirakenduses kirjutuskaitstuks või neid peita.</span><span class="sxs-lookup"><span data-stu-id="b0f64-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="b0f64-277">Määrake suvandid jaotises **Mobiili ajatabelid** vahekaardil **Ajatabel** lehel **Projektihalduse ja -arvestuse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projekti parameetrid](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="b0f64-279">Laienduste kaudu valimiseks saadaolevate tegevuste muutmine</span><span class="sxs-lookup"><span data-stu-id="b0f64-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="b0f64-280">Projekti jaoks valimiseks saadaolevad tegevused täidetakse meetoditega **getActivitiesForProject()** ja **getActivityQuery()** klassis **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="b0f64-281">Selle käitumise muutmiseks saate kasutada käsuliini, et vastendada oma äristsenaarium tegevustega, mis on valimiseks saadaval konkreetse projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="b0f64-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="b0f64-282">Projekti vaikekategooria sisestamine ajatabeli kannetele</span><span class="sxs-lookup"><span data-stu-id="b0f64-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="b0f64-283">Projekti vaikekategooria sisestamine ajatabeli kannetele toimub kolmel tasemel.</span><span class="sxs-lookup"><span data-stu-id="b0f64-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="b0f64-284">Käitumise laiendamiseks ühel või kõigil tasemetel võite kasutada käsuliini soovitud tulemuse saavutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b0f64-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="b0f64-285">Arvutamisel kasutatakse järgmist hierarhiat:</span><span class="sxs-lookup"><span data-stu-id="b0f64-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="b0f64-286">Rakendus üritab võtta vaikekategooria projektiressursist.</span><span class="sxs-lookup"><span data-stu-id="b0f64-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="b0f64-287">See vaikekategooria määratakse meetodites **getCurrentUserResource** ja **getDelegatedResourcesForCurrentUser** klassis **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="b0f64-288">Kui projektiressursi tasemel ei pakuta vaikekategooriat, üritab rakendus võtta seda projekti tegevusest.</span><span class="sxs-lookup"><span data-stu-id="b0f64-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="b0f64-289">See vaikekategooria määratakse meetodis **getActivitiesForProject** klassis **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="b0f64-290">Kui projekti tegevuse tasemel ei pakuta vaikekategooriat, võetakse vaikekategooria projekti parameetritest.</span><span class="sxs-lookup"><span data-stu-id="b0f64-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="b0f64-291">See vaikekategooria määratakse meetodis **getProjectDetailsbyRule** klassis **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="b0f64-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
