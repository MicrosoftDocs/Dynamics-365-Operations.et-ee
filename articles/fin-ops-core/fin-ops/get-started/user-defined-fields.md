---
title: Kohandatud väljade loomine ja nendega töötamine
description: Selles teemas selgitatakse teile, kuidas kasutajaliidese luua kohandatud välju, et rakendus sobiks teie ettevõttega.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 5f74397bcdd59a1fe24f5b6046081cbd2bed461b
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693541"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="fc93f-103">Kohandatud väljade loomine ja nendega töötamine</span><span class="sxs-lookup"><span data-stu-id="fc93f-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc93f-104">Kuigi mitmete äriprotsesside haldamiseks on olemas lai valik valmisvälju, on ettevõttel mõnikord vaja süsteemis jälgida lisateavet.</span><span class="sxs-lookup"><span data-stu-id="fc93f-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="fc93f-105">Kuigi nende väljade lisamiseks arendustööriistas laiendustena saab kasutada programmeerijate abi, võimaldab kohandatud väljade funktsioon lisada väljasid otse kasutajaliidese kaudu, võimaldades teil kohandada rakendust oma ettevõttte vajadustele vastavaks veebibrauseri abil.</span><span class="sxs-lookup"><span data-stu-id="fc93f-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="fc93f-106">Kohandatud väljade lisamise võimalus on saadaval platvormivärskenduses 13 ja uuemates.</span><span class="sxs-lookup"><span data-stu-id="fc93f-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="fc93f-107">Ainult eriõigustega kasutajatel on juurdepääs sellele funktsioonile.</span><span class="sxs-lookup"><span data-stu-id="fc93f-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="fc93f-108">See video näitab, kui lihtne on lisada lehele kohandatud välja: [Kohandatud väljade lisamine](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="fc93f-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="fc93f-109">Kohandatud väljade loomine</span><span class="sxs-lookup"><span data-stu-id="fc93f-109">Creating custom fields</span></span>

<span data-ttu-id="fc93f-110">Pärast selle lisateabe tuvastamist, mida rakenduses jälgida soovite, saate sobivale tabelile luua kohandatud välja ja selle uue välja lehele esitada.</span><span class="sxs-lookup"><span data-stu-id="fc93f-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="fc93f-111">Järgmised sammud kirjeldavad kohandatud välja loomist ja selle välja vormile asetamist.</span><span class="sxs-lookup"><span data-stu-id="fc93f-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="fc93f-112">Minge vormi juurde, kuhu on vaja uut välja.</span><span class="sxs-lookup"><span data-stu-id="fc93f-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="fc93f-113">Kuna lõppeesmärk on kohandatud välja vormile esitamine, on kohandatud väljade loomise sisendpunkt isikupärastamisvõimaluse sees.</span><span class="sxs-lookup"><span data-stu-id="fc93f-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="fc93f-114">Avage isikupärastamise tööriistariba, tehes valikud **Suvandid** ja **Vormi isikupärastamine**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="fc93f-115">Klõpsake suvandeid **Lisa** ja **Väli**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="fc93f-116">Valige vormi piirkond, kuhu soovite uue välja esitada.</span><span class="sxs-lookup"><span data-stu-id="fc93f-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="fc93f-117">Pärast valikuid kuvab dialoogiboks **Väljade lisamine** loendi olemasolevate väljadega, mida saab vormi valitud piirkonda lisada.</span><span class="sxs-lookup"><span data-stu-id="fc93f-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="fc93f-118">Veenduge, et soovitud väli ei ole juba loendis.</span><span class="sxs-lookup"><span data-stu-id="fc93f-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="fc93f-119">Vastasel korral saate lihtsalt loendist selle välja valida ja klõpsata käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="fc93f-120">Klõpsake kohandatud välja loomise alustamiseks loendi kohal asuvat nuppu **Uue välja loomine**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="fc93f-121">See avab dialoogiboksi **Uue välja loomine**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="fc93f-122">Kui te ei näe nuppu **Uue välja lisamine**, pole teil selle funktsiooni kasutamiseks vajalikku luba.</span><span class="sxs-lookup"><span data-stu-id="fc93f-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="fc93f-123">Sisestage dialoogiboksi **Uue välja loomine** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="fc93f-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="fc93f-124">Valige andmebaasi tabel, kuhu see väli tuleks lisada.</span><span class="sxs-lookup"><span data-stu-id="fc93f-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="fc93f-125">Pange tähele, et ripploendis kuvatakse ainult tabelid, mis toetavad kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="fc93f-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="fc93f-126">Toetatud tabelite tehnilisi üksikasju vaadake allpool asuvast jaotisest.</span><span class="sxs-lookup"><span data-stu-id="fc93f-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="fc93f-127">Valige uue välja andmetüüp.</span><span class="sxs-lookup"><span data-stu-id="fc93f-127">Select the data type for the new field.</span></span> <span data-ttu-id="fc93f-128">Saadaolevad andmetüübid on märkeruut, kuupäev, kuupäev ja kellaaeg, kümnendarv, arv, märkeloend ja tekst.</span><span class="sxs-lookup"><span data-stu-id="fc93f-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="fc93f-129">Andmetüübi tekst valimisel saate määrata ka väljale sisestatava teksti maksimaalse pikkuse.</span><span class="sxs-lookup"><span data-stu-id="fc93f-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="fc93f-130">Andmetüübi märkeloend valimisel saate valida ka väljale sisestatavad kehtivad väärtused.</span><span class="sxs-lookup"><span data-stu-id="fc93f-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="fc93f-131">Andke väljale nimi, silt ja spikritekst.</span><span class="sxs-lookup"><span data-stu-id="fc93f-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="fc93f-132">Nimi vastab andmebaasis oleva füüsilise välja nimele, silti ja spikriteksti kasutatakse välja esitamiseks kasutajaliidesel.</span><span class="sxs-lookup"><span data-stu-id="fc93f-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="fc93f-133">Kui see on ainus väli, mida soovite selle vormi jaoks luua, klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="fc93f-134">Kui soovite luua veel välju, klõpsake käsku **Salvesta ja uus** ja naaske 7. etappi.</span><span class="sxs-lookup"><span data-stu-id="fc93f-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="fc93f-135">Pange tähele, et praegu kehtib piirang **20 kohandatud välja tabeli kohta**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="fc93f-136">Dialoogiboksist **Uue välja loomine** lahkumisel naasete dialoogiboksi **Väljade lisamine**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="fc93f-137">Äsja lisatud kohandatud väljad märgitakse väljaloendis automaatselt vormile lisatavate väljadena.</span><span class="sxs-lookup"><span data-stu-id="fc93f-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="fc93f-138">Märgitud väljade lisamiseks vormi valitud piirkonda klõpsake käsku **Lisa**..</span><span class="sxs-lookup"><span data-stu-id="fc93f-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="fc93f-139">**Valikuline:** uute väljade teisaldamiseks valitud piirkonna soovitud asukohta lubage isikupärastamise tööriistaribal režiim **Teisaldamine**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="fc93f-140">Lisateavet eri isikupärastamisvõimaluste kasutamise kohta vormi teie isikliku kasutuse järgi kohandamiseks vaadake teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md)</span><span class="sxs-lookup"><span data-stu-id="fc93f-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="fc93f-141">Kohandatud väljade jagamine teiste kasutajatega</span><span class="sxs-lookup"><span data-stu-id="fc93f-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="fc93f-142">Pärast kohandatud välja loomist ja selle vormile esitamist võite soovida seda uue väljaga uuendatud lehevaatet jagada ka süsteemi teiste kasutatatega.</span><span class="sxs-lookup"><span data-stu-id="fc93f-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="fc93f-143">Seda saab toote isikupärastamisvõimalusi kasutades teha kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="fc93f-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="fc93f-144">Soovitatav on seda teha süsteemi administraatori kaudu, kes saab isikupärastamise avaldada kõigile kasutajatele või kasutajate alamkogumile.</span><span class="sxs-lookup"><span data-stu-id="fc93f-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="fc93f-145">Lisateavet vaadake teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="fc93f-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="fc93f-146">Teise võimalusena saate muudatused (nimega *isikupärastamised*) eksportida, saata need ühele või mitmele kasutajale ja igaüks neist saab muudatused importida.</span><span class="sxs-lookup"><span data-stu-id="fc93f-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="fc93f-147">Isikupärastamise tööriistariba suvand **Halda** võimaldab teil isikupärastamisi eksportida ja importida.</span><span class="sxs-lookup"><span data-stu-id="fc93f-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="fc93f-148">Kohandatud väljade haldamine</span><span class="sxs-lookup"><span data-stu-id="fc93f-148">Managing custom fields</span></span>

<span data-ttu-id="fc93f-149">Kõiki kohandatud välju saab süsteemis hallata süsteemihalduse moodulis oleva lehe **Kohandatud väljad** kaudu.</span><span class="sxs-lookup"><span data-stu-id="fc93f-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="fc93f-150">Sellel lehel saavad kasutajate juurdepääsu paljudele järgmistele võimalustele.</span><span class="sxs-lookup"><span data-stu-id="fc93f-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="fc93f-151">Süsteemi kõigi kohandatud väljade loendi vaatamine.</span><span class="sxs-lookup"><span data-stu-id="fc93f-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="fc93f-152">Olemasolevate kohandatud väljade piiratud redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="fc93f-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="fc93f-153">Kohandatud väljade kustutamine.</span><span class="sxs-lookup"><span data-stu-id="fc93f-153">Deleting custom fields.</span></span>
- <span data-ttu-id="fc93f-154">Kohandatud väljade esitamine andmeüksustele.</span><span class="sxs-lookup"><span data-stu-id="fc93f-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="fc93f-155">Kohandatud väljade siltide ja spikritekstide tõlgete pakkumine.</span><span class="sxs-lookup"><span data-stu-id="fc93f-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="fc93f-156">Kõigi kohandatud väljade vaatamine</span><span class="sxs-lookup"><span data-stu-id="fc93f-156">Viewing all custom fields</span></span>

<span data-ttu-id="fc93f-157">Leht **Kohandatud väljad** leht näitab kõiki süsteemis määratletud kohandatud välju.</span><span class="sxs-lookup"><span data-stu-id="fc93f-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="fc93f-158">Valige soovitud tabel ja leht näitab selle tabeliga seotud kohandatud väljade värskendatud loendit.</span><span class="sxs-lookup"><span data-stu-id="fc93f-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="fc93f-159">Kohandatud välja loendist valimine võimaldab teil vaadata välja üksikasju.</span><span class="sxs-lookup"><span data-stu-id="fc93f-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="fc93f-160">Kohandatud väljade redigeerimine</span><span class="sxs-lookup"><span data-stu-id="fc93f-160">Editing custom fields</span></span>

<span data-ttu-id="fc93f-161">Pärast kohandatud välja loomist saab lehel **Kohandatud väljad** muuta ainult selle välja teatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="fc93f-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="fc93f-162">Muuta *saate* järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="fc93f-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="fc93f-163">Silt</span><span class="sxs-lookup"><span data-stu-id="fc93f-163">Label</span></span>
- <span data-ttu-id="fc93f-164">Spikritekst</span><span class="sxs-lookup"><span data-stu-id="fc93f-164">Help text</span></span>
- <span data-ttu-id="fc93f-165">Pikkus tekstiväljade korral</span><span class="sxs-lookup"><span data-stu-id="fc93f-165">Length, for Text fields</span></span>

<span data-ttu-id="fc93f-166">Te *ei saa* muuta järgmisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="fc93f-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="fc93f-167">Välja nimi</span><span class="sxs-lookup"><span data-stu-id="fc93f-167">Field name</span></span>
- <span data-ttu-id="fc93f-168">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="fc93f-168">Data type</span></span>

<span data-ttu-id="fc93f-169">Märkeloendi väljade korral saate kohandatud väljade kehtivaid väärtusi ümberjärjestada ja uusi väärtusi lisada; märkeloendi välja olemasolevaid väärtusi ei saa aga eemaldada.</span><span class="sxs-lookup"><span data-stu-id="fc93f-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="fc93f-170">Pärast konkreetse tabeli väljade redigeerimist klõpsake muutuste salvestamiseks käsku **Rakenda muudatused**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="fc93f-171">Kohandatud väljade esitamine andmeüksustele</span><span class="sxs-lookup"><span data-stu-id="fc93f-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="fc93f-172">Samuti võib oluline olla kohandatud väljade lubamine andmeüksustel nähtav olla.</span><span class="sxs-lookup"><span data-stu-id="fc93f-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="fc93f-173">Andmeüksusi kasutatakse funktsioonis [Office’i integreerimise ülevaade](../../dev-itpro/office-integration/office-integration.md) ja andmete importimisel/eksportimisel.</span><span class="sxs-lookup"><span data-stu-id="fc93f-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="fc93f-174">Kohandatud välja andmeüksusel esitamiseks tehke läbi järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="fc93f-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="fc93f-175">Valige kohandatud väli vormil **Kohandatud väljad**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="fc93f-176">Asjakohaste üksuste vaatamiseks laiendage jaotist **Üksused**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="fc93f-177">Klõpsake nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="fc93f-178">Muutke välja **Lubatud** nii, et seda valitaks iga üksuse korral, mis peab välja esitama.</span><span class="sxs-lookup"><span data-stu-id="fc93f-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="fc93f-179">Valikute salvestamiseks klõpsake käsku **Rakenda muudatused**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="fc93f-180">Kohandatud väljade teistes keeltes kuvamise lubamine</span><span class="sxs-lookup"><span data-stu-id="fc93f-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="fc93f-181">Kuna kohandatud väljadele võivad ligipääsu vajada eri keelte kasutajad, suudab leht **Kohandatud väljad** kohandatud välja silti ja spikriteksti teistesse keeltesse tõlkida.</span><span class="sxs-lookup"><span data-stu-id="fc93f-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="fc93f-182">Järgmised etapid kirjeldavad kohandatud väljade teistesse keeltesse tõlkimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="fc93f-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="fc93f-183">Valige kohandatud väli lehel **Kohandatud väljad**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="fc93f-184">Valige toimingupaanil nupp **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="fc93f-185">See avab on rippmenüü selle välja jaoks olemasolevate tõlgetega.</span><span class="sxs-lookup"><span data-stu-id="fc93f-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="fc93f-186">Rippmenüü **Keel** näitab keeli, mille jaoks tõlge on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="fc93f-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="fc93f-187">Kui soovite olemasolevat tõlget redigeerida, valige menüüst soovitud keel ning muutke sildi ja spikriteksti väärtusi.</span><span class="sxs-lookup"><span data-stu-id="fc93f-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="fc93f-188">Muul juhul klõpsake nuppu **Lisa keel**, valige menüüst soovitud keel ning sisestage sildi ja spikriteksti tõlgitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="fc93f-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="fc93f-189">Kui olete lõpetanud, klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="fc93f-190">Kohandatud väljade kustutamine</span><span class="sxs-lookup"><span data-stu-id="fc93f-190">Deleting custom fields</span></span>

<span data-ttu-id="fc93f-191">Harvadel juhtudel võite otsustada, et kohandatud välja ei ole enam vaja.</span><span class="sxs-lookup"><span data-stu-id="fc93f-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="fc93f-192">Sel juhul saab süsteemiadministraator välja lehelt **Kohandatud väljad** kustutada.</span><span class="sxs-lookup"><span data-stu-id="fc93f-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="fc93f-193">Selleks veenduge, et valitud on õige väli, klõpsake käsku **Kustuta**, klõpsake kustutamise kinnitamiseks nuppu **Jah** ning lõpuks klõpsake käsku **Rakenda muudatused**.</span><span class="sxs-lookup"><span data-stu-id="fc93f-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="fc93f-194">Seda toimingut ei saa tagasi võtta ning väljaga seotud andmed kustutatakse jäädavalt andmebaasist.</span><span class="sxs-lookup"><span data-stu-id="fc93f-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="fc93f-195">Lisa</span><span class="sxs-lookup"><span data-stu-id="fc93f-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="fc93f-196">Kes saab kohandatud välju luua?</span><span class="sxs-lookup"><span data-stu-id="fc93f-196">Who can create custom fields?</span></span>

<span data-ttu-id="fc93f-197">Süsteemi kaitsmiseks saavad kohandatud välju vaikimisi luua vaid süsteemiadministraatorid.</span><span class="sxs-lookup"><span data-stu-id="fc93f-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="fc93f-198">Sellegipoolest saavad süsteemiadministraatorid turberolli **Käitusaja kohandamise lauskasutaja** abil anda kohandatud väljade loomise õigusi lauskasutajatele, kelle osas organisatsioon õiguste andmist vajalikuks peab.</span><span class="sxs-lookup"><span data-stu-id="fc93f-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="fc93f-199">Ilma selle turberollita kasutajad ei saa kohandatud välju luua, kuid saavad süsteemi teiste kasutajate loodud kohandatud välju vaadata ja neid mõjutada.</span><span class="sxs-lookup"><span data-stu-id="fc93f-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="fc93f-200">Millised tabelid toetavad kohandatud välju?</span><span class="sxs-lookup"><span data-stu-id="fc93f-200">What tables support custom fields?</span></span>

<span data-ttu-id="fc93f-201">Jõudluse tõttu ja tehnilistel põhjustel võimaldavad praegu kohandatud väljade lisamist vaid järgmisi tingimusi täitvad tabelid.</span><span class="sxs-lookup"><span data-stu-id="fc93f-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="fc93f-202">Tabel peab olema märgistatud ühena järgmistest gruppidest.</span><span class="sxs-lookup"><span data-stu-id="fc93f-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="fc93f-203">Grupeeri</span><span class="sxs-lookup"><span data-stu-id="fc93f-203">Group</span></span>
    - <span data-ttu-id="fc93f-204">Töölehe päis</span><span class="sxs-lookup"><span data-stu-id="fc93f-204">WorksheetHeader</span></span>
    - <span data-ttu-id="fc93f-205">Peamine</span><span class="sxs-lookup"><span data-stu-id="fc93f-205">Main</span></span>
    - <span data-ttu-id="fc93f-206">Muud</span><span class="sxs-lookup"><span data-stu-id="fc93f-206">Miscellaneous</span></span>
    - <span data-ttu-id="fc93f-207">Parameeter</span><span class="sxs-lookup"><span data-stu-id="fc93f-207">Parameter</span></span>
    - <span data-ttu-id="fc93f-208">Viide</span><span class="sxs-lookup"><span data-stu-id="fc93f-208">Reference</span></span>
    - <span data-ttu-id="fc93f-209">Kande päis</span><span class="sxs-lookup"><span data-stu-id="fc93f-209">TransactionHeader</span></span>

- <span data-ttu-id="fc93f-210">Tabel ei saa teist tabelit laiendada.</span><span class="sxs-lookup"><span data-stu-id="fc93f-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="fc93f-211">Tabel ei saa olla märgistatud süsteemitabelina.</span><span class="sxs-lookup"><span data-stu-id="fc93f-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="fc93f-212">Tabel ei saa olla ajutine tabel.</span><span class="sxs-lookup"><span data-stu-id="fc93f-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="fc93f-213">Kas ma saan arendustööriistades viidata kohandatud väljadele?</span><span class="sxs-lookup"><span data-stu-id="fc93f-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="fc93f-214">Kohandatud välju saab hallata ainult kasutajaliidese kaudu ja neile ei saa koodi alusel viidata.</span><span class="sxs-lookup"><span data-stu-id="fc93f-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 
