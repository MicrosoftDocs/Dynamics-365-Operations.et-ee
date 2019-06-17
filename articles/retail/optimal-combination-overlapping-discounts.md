<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="et-EE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kattuvate allahindluste optimaalse kombinatsiooni määratlemine</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kui allahindlused kattuvad, siis peate määrama kattuvate allahindluste kombinatsiooni, mis annab kõige suurema koondallahindluse kõige väiksema kande koondsumma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kui allahindluse summa ostetavate toodete hinna alusel erineb, nt tavapärase „ostke 1, saate X protsenti allahindlust” (BOGO) jaeallahindluse korral, saab selles protsessist kombinatoorse optimeerimise küsimus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kattuvate allahindluste optimaalse kombinatsiooni määratlemine</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kui allahindlused kattuvad, siis peate määrama kattuvate allahindluste kombinatsiooni, mis annab kõige suurema koondallahindluse kõige väiksema kande koondsumma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kui allahindluse summa ostetavate toodete hinna alusel erineb, nt tavapärase „ostke 1, saate X protsenti allahindlust” (BOGO) jaeallahindluse korral, saab sellest protsessist kombinatoorse optimeerimise küsimus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">See artikkel kehtib Microsoft Dynamics AX 2012 R3 KB-ga 3105973 (välja antud 2. novembril 2015) või uuema ja Microsoft Dynamics 365 for Retaili puhul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kattuvate allahindluste kombinatsiooni õigeaegse rakendamise määramiseks oleme võtnud kasutusele kattuvate allahindluste rakendamise meetodi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nimetame seda uut meetodit <bpt id="p1">**</bpt>marginaali väärtuse hindamiseks<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marginaali väärtuse hindamist kasutatakse, kui aeg, mis on vajalik kattuvate allahindluste võimalike kombinatsioonide hindamiseks, ületab lehel <bpt id="p1">**</bpt>Jaemüügi parameetrid<ept id="p1">**</ept> konfigureeritava läve.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marginaali väärtuse hindamise meetodis arvutatakse iga kattuva allahindluse väärtus, kasutades jagatud toodete allahindluse väärtust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seejärel rakendatakse kattuvad allahindlused kõrgeimast suhtelisest väärtusest madalaima suhtelise väärtuseni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uue meetodi üksikasjad leiate selle artikli edasisest jaotisest „Marginaali väärtus”.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marginaali väärtuse hindamist ei kasutata, kui toote allahindluse summasid ei mõjuta kande teine toode.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Näiteks ei kasutata seda meetodit kahe lihtsa allahindluse või lihtsa allahindluse ja üksiku toote koguse allahindluse puhul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allahindluse näited</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Saate luua ühisele tootekogumile piiramatu arvu jaeallahindlusi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kuid kuna piirang puudub, võivad tekkida jõudluse probleemid, kui püüate arvutada allahindlusi, mida tuleks erinevatel toodetel kasutada.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Järgmised näited illustreerivad seda probleemi üksikasjalikumalt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1. näites alustame kahe toote ja kahe kattuva allahindlusega.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seejärel näitame 2. näites, kuidas probleem toodete lisamisel edasi areneb.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1. näide: kaks toodet ja kaks allahindlust</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selles näites on vaja kahte toodet mõlema allahindluse jaoks kvalifitseerumiseks ja neid allahindlusi ei saa kombineerida.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selle näite allahindlused on <bpt id="p1">**</bpt>parima hinna<ept id="p1">**</ept> allahindlused.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Mõlemad tooted kvalifitseeruvad mõlemale allahindlusele.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Siin on kaks allahindlust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source><target logoport:matchpercent="0" state="translated">Kahe parima hinna allahindluse näide</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Igasuguse kahe toote puhul oleneb nendest kahest allahindlusest parem kahe toote hindadest.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kui mõlema toote hinnad on võrdsed või peaaegu võrdsed, on 1. allahindlus parem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kui ühe toote hind on teise toote omast oluliselt madalam, on 2. allahindlus parem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Siin on matemaatiline reegel nende kahe allahindluse hindamiseks teineteise suhtes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source><target logoport:matchpercent="0" state="translated">Allahindluste hindamise reegel</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kui 1. toote hind võrdub kahe kolmandikuga 2. toote hinnast, on kaks allahindlust võrdsed.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selles näites varieerub 1. allahindluse puhul kehtiv allahindluse protsent mõnest protsendist (kui kahe toote hinnad on väga erinevad) kuni maksimaalselt 25 protsendini (kui kahel tootel on sama hind).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2. allahindluse kehtiv allahindluse protsent on fikseeritud.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">See on alati 20 protsenti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kuna 1. allahindluse kehtival allahindluse protsendil on vahemik, mis võib olla rohkem või vähem kui 2. allahindlus, siis sõltub parim allahindlus kahe allahindlusega toote hindadest.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selles näites toimub arvutamine kiiresti, kuna ainult kahele tootele rakendatakse ainult kahte allahindlust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Võimalikke kombinatsioone on ainult kaks: üks 1. allahindluse rakendamine või üks 2. allahindluse rakendamine.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Puuduvad permutatsioonid, mida arvutada.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Iga allahindluse väärtus arvutatakse kahe toote abil ja kasutatakse parimat allahindlust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2. näide: neli toodet ja kaks allahindlust</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Järgmiseks kasutame nelja toodet ja sama kahte allahindlust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kõik neli toodet kvalifitseeruvad mõlemale allahindlusele.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Võimalikke kombinatsioone on kaksteist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lõpuks rakendatakse kahte allahindlust kandele ühes kolmest kombinatsioonist: 1. allahindlust rakendatakse kaks korda ja 2. allahindlust kaks korda või 1. allahindlust rakendatakse üks kord ja 2. allahindlust 1 kord.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Võimalike kombinatsioonide illustreerimiseks vaatame kahte erinevat nelja toote kogumit, millel on erinevad hinnad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kõigil neljal tootel on sama hind 15.00 dollarit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sellisel juhul on parim allahindluste kombinatsioon kaks 1. allahindluse rakendamist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaks toodet on täishinnaga ja kaks 50 protsenti soodsamad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Allahindlusega koondsumma on kande puhul 45 $ (15 + 15 + 7.50 + 7.50), mis on 15 $ (25 protsenti) odavam kui allahindluseta koondsumma 60 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2. allahindlus on ainult 12 $ (20 protsenti).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaks toodet maksavad kumbki 20 $, üks toode maksab 15 $ ja üks toode 5 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sellisel juhul on parim allahindluste kombinatsioon ühekordne 2. allahindluse ja ühekordne 1. allahindluse rakendamine.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Järgmine tabel illustreerib allahindlusi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tabelite lugemiseks kasutage ühte toodet realt ja ühte toodet veerust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Näiteks kui kombineerite 1. allahindluse tabelis kaks 20 $ toodet, saate 10 $ allahindlust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kui kombineerite 2. allahindluse tabelis 15 $ toote ja 5 $ toote, saate 4 $ allahindlust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source><target logoport:matchpercent="0" state="translated">Näide, kus kasutatakse nelja toodet sama kahe allahindluse jaoks</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kõigepealt leiame suurima allahindluse, mis on saadaval mis tahes kahe toote puhul, kasutades ükskõik kumba allahindlust.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaks tabelit näitavad allahindluse summat kõigi kahe toote kombinatsioonide kohta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tabelite varjutatud osad kujutavad olukordi, kus toode on paaris iseendaga, mida ei saa teha, või kahe toote pöördsidumine, mis annab sama allahindluse summa ja mida võib eirata.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tabeleid vaadates näete, et 1. allahindlus kahe 20 $ kauba puhul on suurim allahindlus, mis on kummagi allahindluse puhul kõigi nelja toote kohta saadaval.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(See allahindlus on esimeses tabelis rohelisena esile tõstetud.) See jätab alles ainult 15 $ toote ja 5 $ toote.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kahte tabelit uuesti vaadates näete, et nende kahe toote puhul on 1. allahindlus 2.50 $, samas kui 2. allahindlus on 4 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seega valime 2. allahindluse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kogu allahindlus on 14 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selle arutluskäigu hõlpsamaks visualiseerimiseks on siin veel kaks tabelit, mis näitavad kehtivat allahindluse protsenti kõigi võimalike kahe toote kombinatsioonide korral nii 1. kui ka 2. allahindluse puhul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisatud on vaid pool kombinatsioonide loendist, kuna nende kahe allahindluse puhul pole kahele tootele allahindluse rakendamise järjekord oluline.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Suurim kehtiv allahindlus (25 protsenti) on rohelisega esile tõstetud ja vähim kehtiv allahindlus (10 protsenti) on punasega esile tõstetud.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source><target logoport:matchpercent="0" state="translated">Mõlema allahindluse kehtiv allahindluse protsent kõikide kahe toote kombinatsioonide korral</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kui hinnad erinevad ja konkureerib vähemalt kaks allahindlust, on ainus viis parima allahindluste kombinatsiooni garanteerimiseks hinnata mõlemaid allahindlusi ja võrrelda neid.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Võimalikud kombinatsioonid kokku</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">See jaotis jätkab eelmise jaotise näitega.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisame veel tooteid ja veel ühe allahindluse ja vaatame, kui palju kombinatsioone tuleb arvutada ja võrrelda.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Järgmistes tabelites on võimalike allahindluste kombinatsioonide arv tootekoguse kasvades.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tabel näitab, mis juhtub siis, kui kattuvaid allahindlusi on kaks, nagu eelmises näites, ja kui kattuvaid allahindlusi on kolm.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Võimalike allahindluste kombinatsioonide arv, mida tuleb hinnata, ületab peagi ka selle piiri, mida isegi kiire arvuti suudab jaetehingute jaoks piisavalt kiiresti arvutada ja võrrelda.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Võimalike allahindluste kombinatsioonide arv tootekoguse kasvades</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kui rakendatakse veelgi suuremaid koguseid või rohkem kattuvaid allahindlusi, ulatub võimalike allahindluste kombinatsioonide arv kiiresti miljonitesse ja aeg, mis on parima võimaliku kombinatsiooni hindamiseks ja valimiseks vajalik, muutub kiiresti märgatavaks.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jaehinna mootoris on tehtud mõningaid optimeerimisi hinnatavate kombinatsioonide koguarvu vähendamiseks.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kuid kuna kattuvate allahindluste ja tehingute koguste arv ühes kandes pole piiratud, tuleb kattuvate allahindluste korral alati suurt hulka kombinatsioone hinnata.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">See ongi probleem, mille lahendamisega marginaali väärtuse hindamismeetod tegeleb.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marginaali väärtuse meetod</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Astmeliselt suureneva hinnatavate kombinatsioonide arvu probleemi lahendamiseks on olemas optimeerimine, mis arvutab tootekogumi korral, millele saab rakendada vähemalt kahte allahindlust, iga allahindluse väärtuse jagatud toote kohta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nimetame seda väärtust jagatud toodete allahindluse <bpt id="p1">**</bpt>marginaali väärtuseks<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Marginaali väärtus on kogu allahindluse summa keskmine tootepõhine suurenemine, kui jagatud tooted lisatakse igale allahindlusele.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Marginaali väärtus arvutatakse allahindluse kogusummast (DTotal), lahutades allahindluse summa ilma jagatud toodeteta (DMinus<ph id="ph1">\\</ph> Shared) ja jagades selle vahe jagatud toodete arvuga (ProductsShared).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source><target logoport:matchpercent="0" state="translated">Valem marginaali väärtuse arvutamiseks</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Pärast seda, kui on arvutatud jagatud tootekogumi iga allahindluse marginaali väärtus, rakendatakse allahindlused jagatud toodetele alates kõrgeimast marginaaliväärtusest kuni madalaima marginaaliväärtuseni (ammendavalt).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selle meetodi puhul ei võrrelda kõiki järelejäänud allahindluse võimalusi iga kord pärast üksiku allahindluse rakendamist.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Selle asemel võrreldakse kattuvaid allahindlusi üks kord ja seejärel rakendatakse need järjekorras.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisavõrdlusi ei tehta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Saate läve konfigureerida, et minna üle marginaali väärtuse meetodile lehe <bpt id="p2">**</bpt>Jaemüügi parameetrid<ept id="p2">**</ept> vahekaardil <bpt id="p1">**</bpt>Allahindlus<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koondallahindluse arvutamiseks vastuvõetav aeg erineb jaemüügivaldkondade lõikes.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kuid see aeg jääb üldjuhul kümnete millisekundite ja ühe sekundi vahele.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>