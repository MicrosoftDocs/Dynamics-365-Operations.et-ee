<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="valid-checker.md" target-language="et-EE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>valid-checker.125a66.1fc894206f9d90fce1e2eab292ac241e9d943e23.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1fc894206f9d90fce1e2eab292ac241e9d943e23</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\valid-checker.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jaemüügikande süsteemsuskontroll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the retail transaction consistency checker functionality in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli funktsiooni teenuses Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jaemüügikande süsteemsuskontroll</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli funktsiooni, mis lasti välja teenuse Microsoft Dynamics 365 for Finance and Operations versioonis 8.1.3.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Süsteemsuskontroll tuvastab ja isoleerib vastuolulised kanded enne, kui väljavõtte sisestuse protsess need peale võtab.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When a statement is posted in Microsoft Dynamics 365 for Retail, posting can fail due to inconsistent data in the retail transaction tables.</source><target logoport:matchpercent="0" state="translated">Microsoft Dynamics 365 for Retailis võib väljavõtte sisestamine nurjuda, kuna jaemüügikannete tabelites on vastuolulised andmed.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Andmete probleemi võivad põhjustada ettenägematud probleemid kassarakenduses (POS) või kolmanda osapoole kassasüsteemidest valesti imporditud kanded.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples of how these inconsistencies may appear include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Need vastuolud võivad ilmuda näiteks järgmistel juhtudel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The transaction total on the header table does not match the transaction total on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Päisetabelis olev kande kogusumma ei kattu kande ridade kogusummaga.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The line count on the header table does not match with the number of lines in the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Päisetabeli ridade arv ei kattu kandetabeli ridade arvuga.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Taxes on the header table do not match the tax amount on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Päisetabeli maksud ei kattu ridade maksusummaga.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kui väljavõtte sisestamise protsess laadib vastuolulised kanded, luuakse vastuolulised müügiarved ja maksetöölehed ning kogu väljavõtte sisestamise protsess nurjub.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sellises olekus väljavõtete taastamine hõlmab keerukaid andmeparandusi mitmes kandetabelis.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The retail transaction consistency checker prevents such issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jaemüügikande süsteemsuskontroll takistab selliseid probleeme.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following chart illustrates the posting process with the transaction consistency checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Järgmine diagramm illustreerib kande süsteemsuskontrolliga sisestusprotsessi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">![</bpt>Statement posting process with retail transaction consistency checker<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Statement posting process with retail transaction consistency checker<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Väljavõtte sisestamise protsess jaemüügikande süsteemsuskontrolliga<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Väljavõtte sisestamise protsess jaemüügikande süsteemsuskontrolliga<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Validate store transactions<ept id="p1">**</ept> batch process checks the consistency of the retail transaction tables for the following scenarios.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Pakktöötluse funktsioon <bpt id="p1">**</bpt>Kinnita kaupluse kanded<ept id="p1">**</ept> kontrollib jaemüügi kandetabelite järjepidevust järgmiste stsenaariumide suhtes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Customer account<ept id="p1">**</ept> – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kliendi konto<ept id="p1">**</ept> – kontrollib, kas jaemüügi kandetabelites märgitud kliendikonto on peakontori kliendi koondandmetes olemas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Line count<ept id="p1">**</ept> – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Ridade arv<ept id="p1">**</ept> – kontrollib, kas kande päisetabelis märgitud ridade arv kattub müügikande tabeli ridade arvuga.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Price includes tax<ept id="p1">**</ept> – Validates that the <bpt id="p2">**</bpt>Price includes tax<ept id="p2">**</ept> parameter is consistent across transaction lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Hind sisaldab maksu<ept id="p1">**</ept> – kontrollib kas parameeter <bpt id="p2">**</bpt>Hind sisaldab maksu<ept id="p2">**</ept> on kõigil kanderidadel ühtne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Gross amount<ept id="p1">**</ept> – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Brutosumma<ept id="p1">**</ept> – kontrollib, kas päises olev brutosumma vastab ridadel olevate netosummade kogusummale pluss maksusummale.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Net amount<ept id="p1">**</ept> – Validates that the net amount on the header is the sum of the net amounts on the lines.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Netosumma<ept id="p1">**</ept> – kontrollib, kas päises olev netosumma vastab ridadel olevate netosummade kogusummale.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Under / Over payment<ept id="p1">**</ept> – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Üle-/alamakse<ept id="p1">**</ept> – kontrollib, ega päises oleva brutosumma ja maksesumma vahe ei ületa üle-/alamakse konfiguratsiooni maksimumi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Discount amount<ept id="p1">**</ept> – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Allahindluse summa<ept id="p1">**</ept> – kontrollib, kas allahindluse summa allahindlustabelites ja allahindluse summa jaemüügi kanderidade tabelites on ühtne ja kas päises olev allahindluse summa päises on ridadel olevate allahindluse summade kogusumma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Line discount<ept id="p1">**</ept> – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Rea allahindlus<ept id="p1">**</ept> – kontrollib, kas rea kandereal olev rea allahindlus on kandereale vastavas allahindluse tabelis olevate kõigi ridade summa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Gift card item<ept id="p1">**</ept> – Retail doesn't support the return of gift card items.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kinkekaardi kaup<ept id="p1">**</ept> – Retail ei toeta kinkekaardikaupade tagastamist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</source><target logoport:matchpercent="0" state="translated">Kinkekaardil oleva saldo saab aga sularahaks teisendada. Väljavõtte sisestamise protsess nurjub iga kinkekaardikauba puhul, mida töödeldakse sularahaks teisendamise rea asemel tagastusreana.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</source><target logoport:matchpercent="0" state="translated">Kinkekaardikaupade valideerimisprotsess aitab tagada, et ainsad tagastatavad kinkekaardi reakaubad jaemüügi kandetabelites oleksid kinkekaardi sularahaks teisendamise read.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Negative price<ept id="p1">**</ept> – Validates that there are no negative price transaction lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Negatiivne hind<ept id="p1">**</ept> – kontrollib, ega kuskil pole negatiivse hinna kanderidu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Item &amp; Variant<ept id="p1">**</ept> – Validates that items and variants on the transaction lines exist in the item and variant master file.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kaup ja variant<ept id="p1">**</ept> – kontrollib, kas kanderidadel olevad kaubad ja variandid on olemas ka kauba ja variandi põhifailis.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Set up the consistency checker</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Süsteemsuskontrolli seadistamine</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configure the "Validate store transactions" batch process, at <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS posting<ept id="p1">**</ept>, for periodic runs.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Seadistage pakktöötluse funktsiooni „Kontrolli kaupluse kandeid” regulaarne käitamine jaotises <bpt id="p1">**</bpt>Jaemüük <ph id="ph1">\&gt;</ph> Jaemüügi IT <ph id="ph2">\&gt;</ph> Kassa sisestamine<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pakett-tööd saab ajastada kaupluse organisatsiooni hierarhia alusel, sarnaselt protsesside „Väljavõtte arvutamine partiina” ja „Väljavõtte sisestamine partiina” seadistamisega.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Soovitame konfigureerida pakktöötluse nii, et seda käitataks mitu korda päevas, ja ajastada käitamise iga P-töö lõpus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Results of validation process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kontrollimisprotsessi tulemused</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The results of the validation check by the batch process are tagged on the appropriate retail transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pakktöötluse kontrolli tulemused märgistatakse sobivas jaemüügikandes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Validation status<ept id="p1">**</ept> field on the retail transaction record is either set to <bpt id="p2">**</bpt>Successful<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Error<ept id="p3">**</ept>, and the date of the last validation run appears on the <bpt id="p4">**</bpt>Last validation time<ept id="p4">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jaemüügikande kirje väljal <bpt id="p1">**</bpt>Kinnitamise olek<ept id="p1">**</ept> on märge <bpt id="p2">**</bpt>Õnnestus<ept id="p2">**</ept> või <bpt id="p3">**</bpt>Tõrge<ept id="p3">**</ept> ning viimase kontrollimise kuupäev kuvatakse väljal <bpt id="p4">**</bpt>Viimase kinnitamise aeg<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the <bpt id="p1">**</bpt>Validation errors<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kontrollimistõrkega seotud täpsema tõrketeksti vaatamiseks valige asjakohane jaemüügikande kirje ja seejärel klõpsake nuppu <bpt id="p1">**</bpt>Valideerimistõrked<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kandeid, mille kontroll nurjub või mis ei ole veel kontrollitud, ei lisata väljavõtetesse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Protsessi „Väljavõtte arvutamine” ajal teavitatakse kasutajaid, kui teatud kandeid ei saanud väljavõttesse kaasata.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If a validation error is found, the only way to fix the error is to contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ainus viis valideerimistõrke lahendamiseks on võtta ühendust Microsofti toega.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a future release, capability will be added so that users can fix the records that failed through the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tulevases versioonis lisatakse funktsioonid, mis võimaldavad kasutajatel nurjunud kirjeid kasutajaliidese kaudu parandada.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Logging and auditing capabilities will also be made available to trace the history of the modifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Samuti tulevad saadavale logimise ja auditeerimise funktsioonid, mis võimaldavad muudatuste ajalugu jälgida.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Additional validation rules to support more scenarios will be added in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tulevases versioonis lisatakse täiendavad kinnitusreeglid, mis toetavad rohkem stsenaariume.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>