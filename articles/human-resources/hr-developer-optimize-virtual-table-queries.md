---
title: Dataverse'i virtuaalsete tabelite päringute optimeerimine
description: Dataverse virtuaalsete tabelipäringute jõudluse optimeerimine ja tõrkeotsing
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054904"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="156e4-103">Dataverse'i virtuaalsete tabelite päringute optimeerimine</span><span class="sxs-lookup"><span data-stu-id="156e4-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="156e4-104">Väljasta</span><span class="sxs-lookup"><span data-stu-id="156e4-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="156e4-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="156e4-105">Overview</span></span>

<span data-ttu-id="156e4-106">Dataverse virtuaalsete tabelite kasutamisel integratsioonide ja muude andmeühenduste arendamiseks Dynamics 365 Human Resources rakendusega saate kogeda jõudlusprobleeme virtuaalsete tabelitega seotud päringutega.</span><span class="sxs-lookup"><span data-stu-id="156e4-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="156e4-107">Aeglane päringu täitmine võib toimuda erinevate klientide või liideste vahel.</span><span class="sxs-lookup"><span data-stu-id="156e4-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="156e4-108">Näiteks võib ilmneda probleem järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="156e4-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="156e4-109">Virtuaalse tabeli päringu esitamisel Dataverse Web API kaudu</span><span class="sxs-lookup"><span data-stu-id="156e4-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="156e4-110">Power Api loomine virtuaalse tabeli vastu</span><span class="sxs-lookup"><span data-stu-id="156e4-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="156e4-111">Power BI aruande koostamisel virtuaalsele tabelile</span><span class="sxs-lookup"><span data-stu-id="156e4-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="156e4-112">Kõik need liidesed võivad jõudlusprobleemi esile tuua.</span><span class="sxs-lookup"><span data-stu-id="156e4-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="156e4-113">Personaliosakonna Dataverse virtuaaltabelite aeglase jõudluse üheks põhjuseks on tabeli [navigeerimisatribuutidega](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) seotud virtuaalse tabeli võõrvõtme veerud.</span><span class="sxs-lookup"><span data-stu-id="156e4-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="156e4-114">Kui virtuaalse tabeli jaoks luuakse navigeerimisatribuudid, lisatakse tabelisse võõrvõtme veerg, mis tähistab seotud virtuaalse tabeli võtmeveeru võtme väärtust.</span><span class="sxs-lookup"><span data-stu-id="156e4-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="156e4-115">Näiteks lisatakse veerg **_mshr_fk_person_id_value** olemile **mshr_hcmworkerbaseentity**, mille **mshr_dirpersonentity** olemi välisvõtme atribuut.</span><span class="sxs-lookup"><span data-stu-id="156e4-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="156e4-116">Kuna nende võõrvõtmete veergude väärtusi säilitatakse tabelis, võib väärtuste toomine avaldada negatiivset mõju virtuaalse tabeli päringu jõudlusele.</span><span class="sxs-lookup"><span data-stu-id="156e4-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="156e4-117">Võimalikud sümptomid</span><span class="sxs-lookup"><span data-stu-id="156e4-117">Potential symptoms</span></span>

<span data-ttu-id="156e4-118">Näide, kus seda mõju võite näha, on päringutes olemi Töötaja ( **mshr_hcmworkerentity**) või Baastöötaja (**mshr_hcmworkerbaseentity**) vastu.</span><span class="sxs-lookup"><span data-stu-id="156e4-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="156e4-119">Jõudluse probleem võib ilmneda mitmel erineval viisil:</span><span class="sxs-lookup"><span data-stu-id="156e4-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="156e4-120">**Aeglane päringu tegevus**: virtuaaltabeli vastane päring võib tagastada oodatud tulemused, kuid päringu täitmise lõpuleviimiseks kulub oodatust kauem aega.</span><span class="sxs-lookup"><span data-stu-id="156e4-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="156e4-121">**Päringu aegumine**: päring võib aeguda ja tagastada järgmise tõrke: "Finance and Operations kutsumiseks saadi luba, kuid Finance and Operations tagas tõrke tüübiga InternalServerError."</span><span class="sxs-lookup"><span data-stu-id="156e4-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="156e4-122">**Ootamatu tõrge**: päring võib tagastada tõrketüübi 400 järgmise teatega: "Ilmnes ootamatu tõrge."</span><span class="sxs-lookup"><span data-stu-id="156e4-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Vea tüüp 400 HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="156e4-124">**Ahendamine**: päring võib serveri ressursse üle kasutada ja muutuda ahendamiseks.</span><span class="sxs-lookup"><span data-stu-id="156e4-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="156e4-125">Sel juhul tagastab päring järgmise tõrke: "Finance and Operations kutsumiseks hangiti luba ,kuid Finance and Operations tagastas tõrge tüübiga 429."</span><span class="sxs-lookup"><span data-stu-id="156e4-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="156e4-126">Lisateavet personaliosakonna ahendamise kohta leiate teemast [Ahendamise KKK](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="156e4-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Vea tüüp 429 HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="156e4-128">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="156e4-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="156e4-129">Andmepäringusse kaasatud veergude arvu piiramine</span><span class="sxs-lookup"><span data-stu-id="156e4-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="156e4-130">Virtuaalsete tabelite puhul on üks meetoditest, millel on kõige suurem potentsiaal päringu jõudluse parandamiseks, päringus valitud veergude arvu piiramine.</span><span class="sxs-lookup"><span data-stu-id="156e4-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="156e4-131">Päringu toimivuse optimeerimise üldjuhend on piirata päringus tagastatud veerge ainult nende omadustega, mida vajate.</span><span class="sxs-lookup"><span data-stu-id="156e4-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="156e4-132">See kehtib eriti virtuaalsete tabelite võõrvõtmete veergude kohta.</span><span class="sxs-lookup"><span data-stu-id="156e4-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="156e4-133">Kui te ei vaja integratsiooniks või aruandeks võõrvõtmete veergude väärtusi, siis struktureerige päring, et valida ainult need veerud, mida vajate (v.a võõrvõtme veerud).</span><span class="sxs-lookup"><span data-stu-id="156e4-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="156e4-134">Veergude valimine OData päringus</span><span class="sxs-lookup"><span data-stu-id="156e4-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="156e4-135">Dataverse Web API kaudu virtuaalsest tabelist päringu tegemisel saate piirata päringusse kaasatud veergude arvu, kasutades **$select** süsteemipäringut ja määratleda veerud, mille kohta vajate tulemite tagastamist.</span><span class="sxs-lookup"><span data-stu-id="156e4-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="156e4-136">Jõudluse maksimeerimiseks jätke päringust välja võõrvõtme veerud (need, millel on **_mshr_FK_** eesliide).</span><span class="sxs-lookup"><span data-stu-id="156e4-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="156e4-137">Näiteks järgmine päring **mshr_hcmworkerbaseentity** olemi vastu sisaldab ainult **$select** päringu suvandiklauslis sisalduvaid veerge, v.a võõrvõtme väärtused.</span><span class="sxs-lookup"><span data-stu-id="156e4-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="156e4-138">See pakub olulisi täiustusi jõudluses päringu üle, mis sisaldab kõiki tabeliveerge.</span><span class="sxs-lookup"><span data-stu-id="156e4-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="156e4-139">Soovitus piirata valitud veergude arvu kehtib ka siis, kui kasutate **$expand** päringu suvandit päringu laiendamiseks seotud virtuaalsetele tabelitele navigeerimisatribuutide kaudu.</span><span class="sxs-lookup"><span data-stu-id="156e4-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="156e4-140">Näiteks järgmine päring sisaldab olemit **mshr_hcmworkerbaseentity** koos laiendatud veergudega olemist **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="156e4-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="156e4-141">Pange tähele, **$select** päringu suvand on kaasatud ka päringu **$expand** suvandi klauslisse.</span><span class="sxs-lookup"><span data-stu-id="156e4-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="156e4-142">Kasutades seda meetodit andmete toomiseks päringu **$select** valikuga päringu **$expand** valikus, näete tavaliselt suuremat jõudluse parendust, kui navigeerimisaviis üksuste vahel on mitu-ühele suhe.</span><span class="sxs-lookup"><span data-stu-id="156e4-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="156e4-143">Te ei pruugi näha sama kahanemist päringu täitmisajas ühe-mitmele suhte laiendamisel.</span><span class="sxs-lookup"><span data-stu-id="156e4-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="156e4-144">Lisateavet Dataverse virtuaaltabelite seose definitsiooni kohta vt [Tabeliseosed](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="156e4-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="156e4-145">Lisateavet Dataverse Web API **$select** ja **$expand** kasutamise kohta vt teemast [Seotud üksusekirjete hankimine päringuga](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="156e4-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="156e4-146">Veergude valimine rakenduses Power BI</span><span class="sxs-lookup"><span data-stu-id="156e4-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="156e4-147">Kui teil tekib Power BI aruande Dataverse virtuaalse tabeli suhtes aruande ülesehitamisel mis tahes peatse jõudlusel, saate parandada jõudlust, välistades võõrvõtme veerud aruande tabelist valitud veergudest.</span><span class="sxs-lookup"><span data-stu-id="156e4-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="156e4-148">Näiteks kui kasutate aruande loomiseks olemi **mshr_hcmworkerbaseentity** vastu rakendust Power BI Desktop, saate kasutada järgmisi samme aruande päringusse kaasamiseks veergude valimiseks.</span><span class="sxs-lookup"><span data-stu-id="156e4-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="156e4-149">Power BI Desktop rakenduses valige toiminguribaripploendis **Too andmed** valige väärtus **Veel...**.</span><span class="sxs-lookup"><span data-stu-id="156e4-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="156e4-150">Sisestage aknas **Hangi andmed** otsinguboksi **Common Data Service**, valige ühendus **Common Data Service** ja valige käsk **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="156e4-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="156e4-151">Akna Common Data Service väljas **Serveri URL** sisestage oma Dataverse keskkonna organisatsiooni URI ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="156e4-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Sisestage Dataverse'i keskkonna URI](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="156e4-153">Laiendage aknas Navigator sõlm **Olemid**.</span><span class="sxs-lookup"><span data-stu-id="156e4-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="156e4-154">Otsinguboksis sisestage **mshr_hcmworkerbaseentity** ja valige olem.</span><span class="sxs-lookup"><span data-stu-id="156e4-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="156e4-155">Valige **Andmete transformeermine**.</span><span class="sxs-lookup"><span data-stu-id="156e4-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="156e4-156">Valige Power Query Editor aknas **Täpsem redaktor**.</span><span class="sxs-lookup"><span data-stu-id="156e4-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="156e4-157">Aknas **Täpsem redaktor** uuendage päringut nii, et see otsiks välja järgmisena, lisades või eemaldades kõik vajalikud veerud massiivile.</span><span class="sxs-lookup"><span data-stu-id="156e4-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Päringu värskendamine Power Query Editor täpsemas redaktoris](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="156e4-159">Valige suvand **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="156e4-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="156e4-160">Kui olete enne päringu värskendamist päringult saanud tõrke tüübist 429, peate võib-olla enne päringu värskendamist ootama uuesti prooviperioodi, et see saaks täielikult lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="156e4-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="156e4-161">Klõpsake Power Query Editor tegevusribal nuppu **Sule ja rakenda**.</span><span class="sxs-lookup"><span data-stu-id="156e4-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="156e4-162">Siis saate alustada Power BI aruande ülesehimist virtuaaltabelist valitud veergude suhtes.</span><span class="sxs-lookup"><span data-stu-id="156e4-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="156e4-163">Veergude valimine rakenduses Power Apps</span><span class="sxs-lookup"><span data-stu-id="156e4-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="156e4-164">Sarnaselt Dataverse Web API ja Power BI päringutega saate parandada Power Apps Dataverse virtuaaltabelitel põhineva päringu jõudlust, jättes rakendusest välja seotud tabelite veerud.</span><span class="sxs-lookup"><span data-stu-id="156e4-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="156e4-165">Kui lehele on lisatud seotud tabeli veerge, sisaldab andmete toomiseks loodud päringu URL ka seotud tabeli võõrvõti atribuute.</span><span class="sxs-lookup"><span data-stu-id="156e4-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="156e4-166">See, nagu ülaltoodud [OData päringu veergude valimise](#selecting-columns-in-power-apps) näites, vähendab jõudlust täiendavate andmeotsingute tõttu.</span><span class="sxs-lookup"><span data-stu-id="156e4-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="156e4-167">Selle probleemi lahendamiseks saate kinnitada, et ükski seotud tabelite andmeväli ei ole teie Power App'i andmevormile kaasatud.</span><span class="sxs-lookup"><span data-stu-id="156e4-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="156e4-168">Valige puuvaate paanil ekraanile andmevorm.</span><span class="sxs-lookup"><span data-stu-id="156e4-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="156e4-169">Valige paanil **Atribuudid** suvand **Redigeeri** atribuudis **Väljad**.</span><span class="sxs-lookup"><span data-stu-id="156e4-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="156e4-170">Kontrollige **andme** paanil, et ükski valitud väli ei ole andmeallika virtuaaltabeli väljaks.</span><span class="sxs-lookup"><span data-stu-id="156e4-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="156e4-171">Näiteks kui üks rakenduse lehel kaasatud andmeväljadest viitab teisele tabelile, nt **ThisItem.Worker.Name**, kus **töötaja** on seotud tabel, võib andmete toomisel jõudlust vähendada.</span><span class="sxs-lookup"><span data-stu-id="156e4-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="156e4-172">Saate kasutada [Power Apps Monitori](/powerapps/maker/monitor-overview), et Power App'i andmete toomiseks kaasaks päringusse ainult vajalikud veerud.</span><span class="sxs-lookup"><span data-stu-id="156e4-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="156e4-173">Toimingu getRows jaoks loodud URL-i saate vaadata, kindlustamaks, et teie rakendusele valitud veerud on andmete toomisel optimaalsed.</span><span class="sxs-lookup"><span data-stu-id="156e4-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Kasutage Power Apps Monitor funktsiooni funktsiooni getData toimingu analüüsimiseks.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="156e4-175">Andmepäringu filtreerimine</span><span class="sxs-lookup"><span data-stu-id="156e4-175">Filtering the data query</span></span>

<span data-ttu-id="156e4-176">Teine meetod päringu täitmise jõudluse parandamiseks on päringutulemites tagastatud kirjete arvu piiramine.</span><span class="sxs-lookup"><span data-stu-id="156e4-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="156e4-177">Seda saate teha tulemuste filtreerimisega, et tagada ainult vajalike kirjete saamine.</span><span class="sxs-lookup"><span data-stu-id="156e4-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="156e4-178">Lisateavet päringuandmete filtreerimise kohta vt [filtreerimistulemustest](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).</span><span class="sxs-lookup"><span data-stu-id="156e4-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="156e4-179">Päringu lehekülje suuruse piiramine</span><span class="sxs-lookup"><span data-stu-id="156e4-179">Limiting the page size of the query</span></span>

<span data-ttu-id="156e4-180">Suurte andmekomplektiga töötamisel saate päringutulemused jagada mitmeks leheks, lisades andmepäringutele `odata.maxpagesize` eelispäise.</span><span class="sxs-lookup"><span data-stu-id="156e4-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="156e4-181">Lisateavet saalimise kohta vt[Määrake lehel tagastamiseks üksuste arv](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="156e4-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="156e4-182">Vt ka</span><span class="sxs-lookup"><span data-stu-id="156e4-182">See also</span></span>

- [<span data-ttu-id="156e4-183">Dataverse'i virtuaalsete tabelite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="156e4-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="156e4-184">Human Resourcesi virtuaalsete tabelite KKK</span><span class="sxs-lookup"><span data-stu-id="156e4-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="156e4-185">Ahendamise KKK</span><span class="sxs-lookup"><span data-stu-id="156e4-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]