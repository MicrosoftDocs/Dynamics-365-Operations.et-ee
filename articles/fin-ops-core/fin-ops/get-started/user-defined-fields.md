---
title: Kohandatud väljade loomine ja nendega töötamine
description: Selles teemas selgitatakse, kuidas luua kohandatud välju, et rakendus sobiks nende ettevõttega.
author: jasongre
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 9146921c47e89c5895a1a727de874b0ffbc93c37
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812501"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="a2e2a-103">Kohandatud väljade loomine ja nendega töötamine</span><span class="sxs-lookup"><span data-stu-id="a2e2a-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2e2a-104">Kuigi mitmete äriprotsesside haldamiseks on olemas lai valik valmisvälju, on ettevõttel mõnikord vaja süsteemis jälgida lisateavet.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="a2e2a-105">Selle vajaduse rahuldamiseks saate luua kohandatud välju, et rakendus sobiks nende ettevõttega, kui teil selle funktsiooni kasutamise load.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-105">To accommodate this need, you can create custom fields to tailor the application to fit your business, provided you have permissions to the feature.</span></span>

<span data-ttu-id="a2e2a-106">Kohandatud väljade lisamise võimalus on saadaval platvormivärskenduses 13 ja uuemates.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-106">The ability to add custom fields is available in platform update 13 and later.</span></span>

<span data-ttu-id="a2e2a-107">See video näitab, kui lihtne on lisada lehele kohandatud välja: [Kohandatud väljade lisamine](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="a2e2a-107">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="a2e2a-108">Kohandatud väljade loomine</span><span class="sxs-lookup"><span data-stu-id="a2e2a-108">Creating custom fields</span></span>

<span data-ttu-id="a2e2a-109">Pärast selle lisateabe tuvastamist, mida rakenduses jälgida soovite, saate sobivale tabelile luua kohandatud välja ja selle uue välja lehele esitada.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-109">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="a2e2a-110">Järgmised sammud kirjeldavad kohandatud välja loomist ja selle välja vormile asetamist.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-110">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="a2e2a-111">Minge vormi juurde, kuhu on vaja uut välja.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-111">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="a2e2a-112">Kuna lõppeesmärk on kohandatud välja vormile esitamine, on kohandatud väljade loomise sisendpunkt isikupärastamisvõimaluse sees.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-112">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="a2e2a-113">Avage isikupärastamise tööriistariba, tehes valikud **Suvandid** ja **Vormi isikupärastamine**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-113">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="a2e2a-114">Klõpsake suvandeid **Lisa** ja **Väli**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-114">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="a2e2a-115">Valige vormi piirkond, kuhu soovite uue välja esitada.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-115">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="a2e2a-116">Pärast valikuid kuvab dialoogiboks **Väljade lisamine** loendi olemasolevate väljadega, mida saab vormi valitud piirkonda lisada.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-116">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="a2e2a-117">Veenduge, et soovitud väli ei ole juba loendis.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-117">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="a2e2a-118">Vastasel korral saate lihtsalt loendist selle välja valida ja klõpsata käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-118">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="a2e2a-119">Klõpsake kohandatud välja loomise alustamiseks loendi kohal asuvat nuppu **Uue välja loomine**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-119">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="a2e2a-120">See avab dialoogiboksi **Uue välja loomine**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-120">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="a2e2a-121">Kui te ei näe nuppu **Uue välja lisamine**, pole teil selle funktsiooni kasutamiseks vajalikku luba.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-121">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="a2e2a-122">Sisestage dialoogiboksi **Uue välja loomine** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-122">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="a2e2a-123">Valige andmebaasi tabel, kuhu see väli tuleks lisada.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-123">Select the database table where this field should be added.</span></span> <span data-ttu-id="a2e2a-124">Pange tähele, et ripploendis kuvatakse ainult tabelid, mis toetavad kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-124">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="a2e2a-125">Toetatud tabelite tehnilisi üksikasju vaadake allpool asuvast jaotisest.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-125">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="a2e2a-126">Valige uue välja andmetüüp.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-126">Select the data type for the new field.</span></span> <span data-ttu-id="a2e2a-127">Saadaolevad andmetüübid on märkeruut, kuupäev, kuupäev ja kellaaeg, kümnendarv, arv, märkeloend ja tekst.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-127">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="a2e2a-128">Andmetüübi tekst valimisel saate määrata ka väljale sisestatava teksti maksimaalse pikkuse.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-128">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="a2e2a-129">Andmetüübi märkeloend valimisel saate valida ka väljale sisestatavad kehtivad väärtused.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-129">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="a2e2a-130">Andke väljale nimi, silt ja spikritekst.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-130">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="a2e2a-131">Nimi vastab andmebaasis oleva füüsilise välja nimele, silti ja spikriteksti kasutatakse välja esitamiseks kasutajaliidesel.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-131">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="a2e2a-132">Kui see on ainus väli, mida soovite selle vormi jaoks luua, klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-132">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="a2e2a-133">Kui soovite luua veel välju, klõpsake käsku **Salvesta ja uus** ja naaske 7. etappi.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-133">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="a2e2a-134">Pange tähele, et praegu kehtib piirang **20 kohandatud välja tabeli kohta**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-134">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="a2e2a-135">Dialoogiboksist **Uue välja loomine** lahkumisel naasete dialoogiboksi **Väljade lisamine**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-135">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="a2e2a-136">Äsja lisatud kohandatud väljad märgitakse väljaloendis automaatselt vormile lisatavate väljadena.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-136">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="a2e2a-137">Märgitud väljade lisamiseks vormi valitud piirkonda klõpsake käsku **Lisa**..</span><span class="sxs-lookup"><span data-stu-id="a2e2a-137">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="a2e2a-138">**Valikuline:** uute väljade teisaldamiseks valitud piirkonna soovitud asukohta lubage isikupärastamise tööriistaribal režiim **Teisaldamine**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-138">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="a2e2a-139">Lisateavet eri isikupärastamisvõimaluste kasutamise kohta vormi teie isikliku kasutuse järgi kohandamiseks vaadake teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md)</span><span class="sxs-lookup"><span data-stu-id="a2e2a-139">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="a2e2a-140">Kohandatud väljade jagamine teiste kasutajatega</span><span class="sxs-lookup"><span data-stu-id="a2e2a-140">Sharing custom fields with other users</span></span>

<span data-ttu-id="a2e2a-141">Pärast kohandatud välja loomist ja selle vormile esitamist võite soovida seda uue väljaga uuendatud lehevaatet jagada ka süsteemi teiste kasutatatega.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-141">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="a2e2a-142">Seda saab toote isikupärastamisvõimalusi kasutades teha kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-142">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="a2e2a-143">Soovitatav on seda teha süsteemi administraatori kaudu, kes saab isikupärastamise avaldada kõigile kasutajatele või kasutajate alamkogumile.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-143">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="a2e2a-144">Lisateavet vaadake teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="a2e2a-144">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="a2e2a-145">Teise võimalusena saate muudatused (nimega *isikupärastamised*) eksportida, saata need ühele või mitmele kasutajale ja igaüks neist saab muudatused importida.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-145">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="a2e2a-146">Isikupärastamise tööriistariba suvand **Halda** võimaldab teil isikupärastamisi eksportida ja importida.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-146">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="a2e2a-147">Kohandatud väljade haldamine</span><span class="sxs-lookup"><span data-stu-id="a2e2a-147">Managing custom fields</span></span>

<span data-ttu-id="a2e2a-148">Kõiki kohandatud välju saab süsteemis hallata süsteemihalduse moodulis oleva lehe **Kohandatud väljad** kaudu.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-148">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="a2e2a-149">Sellel lehel saavad kasutajate juurdepääsu paljudele järgmistele võimalustele.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-149">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="a2e2a-150">Süsteemi kõigi kohandatud väljade loendi vaatamine.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-150">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="a2e2a-151">Olemasolevate kohandatud väljade piiratud redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-151">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="a2e2a-152">Kohandatud väljade kustutamine.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-152">Deleting custom fields.</span></span>
- <span data-ttu-id="a2e2a-153">Kohandatud väljade esitamine andmeüksustele.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-153">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="a2e2a-154">Kohandatud väljade siltide ja spikritekstide tõlgete pakkumine.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-154">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="a2e2a-155">Kõigi kohandatud väljade vaatamine</span><span class="sxs-lookup"><span data-stu-id="a2e2a-155">Viewing all custom fields</span></span>

<span data-ttu-id="a2e2a-156">Leht **Kohandatud väljad** leht näitab kõiki süsteemis määratletud kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-156">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="a2e2a-157">Valige soovitud tabel ja leht näitab selle tabeliga seotud kohandatud väljade värskendatud loendit.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-157">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="a2e2a-158">Kohandatud välja loendist valimine võimaldab teil vaadata välja üksikasju.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-158">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="a2e2a-159">Kohandatud väljade redigeerimine</span><span class="sxs-lookup"><span data-stu-id="a2e2a-159">Editing custom fields</span></span>

<span data-ttu-id="a2e2a-160">Pärast kohandatud välja loomist saab lehel **Kohandatud väljad** muuta ainult selle välja teatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-160">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="a2e2a-161">Muuta *saate* järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-161">You *can* modify these attributes:</span></span>

- <span data-ttu-id="a2e2a-162">Silt</span><span class="sxs-lookup"><span data-stu-id="a2e2a-162">Label</span></span>
- <span data-ttu-id="a2e2a-163">Spikritekst</span><span class="sxs-lookup"><span data-stu-id="a2e2a-163">Help text</span></span>
- <span data-ttu-id="a2e2a-164">Pikkus tekstiväljade korral</span><span class="sxs-lookup"><span data-stu-id="a2e2a-164">Length, for Text fields</span></span>

<span data-ttu-id="a2e2a-165">Te *ei saa* muuta järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-165">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="a2e2a-166">Välja nimi</span><span class="sxs-lookup"><span data-stu-id="a2e2a-166">Field name</span></span>
- <span data-ttu-id="a2e2a-167">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="a2e2a-167">Data type</span></span>

<span data-ttu-id="a2e2a-168">Märkeloendi väljade korral saate kohandatud väljade kehtivaid väärtusi ümberjärjestada ja uusi väärtusi lisada; märkeloendi välja olemasolevaid väärtusi ei saa aga eemaldada.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-168">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="a2e2a-169">Pärast konkreetse tabeli väljade redigeerimist klõpsake muutuste salvestamiseks käsku **Rakenda muudatused**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-169">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="a2e2a-170">Kohandatud väljade esitamine andmeüksustele</span><span class="sxs-lookup"><span data-stu-id="a2e2a-170">Exposing custom fields on data entities</span></span>

<span data-ttu-id="a2e2a-171">Samuti võib oluline olla kohandatud väljade lubamine andmeüksustel nähtav olla.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-171">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="a2e2a-172">Andmeüksusi kasutatakse funktsioonis [Office’i integreerimise ülevaade](../../dev-itpro/office-integration/office-integration.md) ja andmete importimisel/eksportimisel.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-172">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="a2e2a-173">Kohandatud välja andmeüksusel esitamiseks tehke läbi järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-173">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="a2e2a-174">Valige kohandatud väli vormil **Kohandatud väljad**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-174">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="a2e2a-175">Asjakohaste üksuste vaatamiseks laiendage jaotist **Üksused**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-175">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="a2e2a-176">Klõpsake nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-176">Click the **Edit** button.</span></span>
4. <span data-ttu-id="a2e2a-177">Muutke välja **Lubatud** nii, et seda valitaks iga üksuse korral, mis peab välja esitama.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-177">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="a2e2a-178">Valikute salvestamiseks klõpsake käsku **Rakenda muudatused**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-178">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="a2e2a-179">Kohandatud väljade teistes keeltes kuvamise lubamine</span><span class="sxs-lookup"><span data-stu-id="a2e2a-179">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="a2e2a-180">Kuna kohandatud väljadele võivad ligipääsu vajada eri keelte kasutajad, suudab leht **Kohandatud väljad** kohandatud välja silti ja spikriteksti teistesse keeltesse tõlkida.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-180">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="a2e2a-181">Järgmised etapid kirjeldavad kohandatud väljade teistesse keeltesse tõlkimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-181">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="a2e2a-182">Valige kohandatud väli lehel **Kohandatud väljad**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-182">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="a2e2a-183">Valige toimingupaanil nupp **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-183">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="a2e2a-184">See avab on rippmenüü selle välja jaoks olemasolevate tõlgetega.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-184">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="a2e2a-185">Rippmenüü **Keel** näitab keeli, mille jaoks tõlge on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-185">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="a2e2a-186">Kui soovite olemasolevat tõlget redigeerida, valige menüüst soovitud keel ning muutke sildi ja spikriteksti väärtusi.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-186">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="a2e2a-187">Muul juhul klõpsake nuppu **Lisa keel**, valige menüüst soovitud keel ning sisestage sildi ja spikriteksti tõlgitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-187">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="a2e2a-188">Kui olete lõpetanud, klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-188">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="a2e2a-189">Kohandatud väljade kustutamine</span><span class="sxs-lookup"><span data-stu-id="a2e2a-189">Deleting custom fields</span></span>

<span data-ttu-id="a2e2a-190">Harvadel juhtudel võite otsustada, et kohandatud välja ei ole enam vaja.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-190">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="a2e2a-191">Sel juhul saab süsteemiadministraator välja lehelt **Kohandatud väljad** kustutada.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-191">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="a2e2a-192">Selleks veenduge, et valitud on õige väli, klõpsake käsku **Kustuta**, klõpsake kustutamise kinnitamiseks nuppu **Jah** ning lõpuks klõpsake käsku **Rakenda muudatused**.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-192">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="a2e2a-193">Seda toimingut ei saa tagasi võtta ning väljaga seotud andmed kustutatakse jäädavalt andmebaasist.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-193">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="a2e2a-194">Lisa</span><span class="sxs-lookup"><span data-stu-id="a2e2a-194">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="a2e2a-195">Kes saab kohandatud välju luua?</span><span class="sxs-lookup"><span data-stu-id="a2e2a-195">Who can create custom fields?</span></span>

<span data-ttu-id="a2e2a-196">Süsteemi kaitsmiseks saavad kohandatud välju vaikimisi luua vaid süsteemiadministraatorid.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-196">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="a2e2a-197">Sellegipoolest saavad süsteemiadministraatorid turberolli **Käitusaja kohandamise lauskasutaja** abil anda kohandatud väljade loomise õigusi lauskasutajatele, kelle osas organisatsioon õiguste andmist vajalikuks peab.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-197">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="a2e2a-198">Ilma selle turberollita kasutajad ei saa kohandatud välju luua, kuid saavad süsteemi teiste kasutajate loodud kohandatud välju vaadata ja neid mõjutada.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-198">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="a2e2a-199">Millised tabelid toetavad kohandatud välju?</span><span class="sxs-lookup"><span data-stu-id="a2e2a-199">What tables support custom fields?</span></span>

<span data-ttu-id="a2e2a-200">Jõudluse tõttu ja tehnilistel põhjustel võimaldavad praegu kohandatud väljade lisamist vaid järgmisi tingimusi täitvad tabelid.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-200">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="a2e2a-201">Tabel peab olema märgistatud ühena järgmistest gruppidest.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-201">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="a2e2a-202">Grupeeri</span><span class="sxs-lookup"><span data-stu-id="a2e2a-202">Group</span></span>
    - <span data-ttu-id="a2e2a-203">Töölehe päis</span><span class="sxs-lookup"><span data-stu-id="a2e2a-203">WorksheetHeader</span></span>
    - <span data-ttu-id="a2e2a-204">Peamine</span><span class="sxs-lookup"><span data-stu-id="a2e2a-204">Main</span></span>
    - <span data-ttu-id="a2e2a-205">Muud</span><span class="sxs-lookup"><span data-stu-id="a2e2a-205">Miscellaneous</span></span>
    - <span data-ttu-id="a2e2a-206">Parameeter</span><span class="sxs-lookup"><span data-stu-id="a2e2a-206">Parameter</span></span>
    - <span data-ttu-id="a2e2a-207">Viide</span><span class="sxs-lookup"><span data-stu-id="a2e2a-207">Reference</span></span>
    - <span data-ttu-id="a2e2a-208">Kande päis</span><span class="sxs-lookup"><span data-stu-id="a2e2a-208">TransactionHeader</span></span>

- <span data-ttu-id="a2e2a-209">Tabel ei saa teist tabelit laiendada.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-209">The table cannot extend another table.</span></span>
- <span data-ttu-id="a2e2a-210">Tabel ei saa olla märgistatud süsteemitabelina.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-210">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="a2e2a-211">Tabel ei saa olla ajutine tabel.</span><span class="sxs-lookup"><span data-stu-id="a2e2a-211">The table cannot be a temporary table.</span></span>