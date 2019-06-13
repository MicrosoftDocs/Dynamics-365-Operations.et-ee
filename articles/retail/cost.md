<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="et-EE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="0" state="translated">Hajutatud tellimuste haldamise (DOM) kulukonfiguratsioon</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Selles teemas kirjeldatakse Microsoft Dynamics 365 for Retaili hajutatud tellimuste haldamise (DOM) funktsiooni kulukonfiguratsiooni.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Hajutatud tellimuste haldamise (DOM) kulukonfiguratsioon</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="0" state="translated">Organisatsioonid kasutavad tellimuse täitmise alusena kasutatava optimaalse asukoha määratlemiseks mitut kulukomponenti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="0" state="translated">Mõned neist kulukomponentidest on lähetuskulu, käsitluskulu ja pakenduskulu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="0" state="translated">Täitmisasukoha määratlemiseks arvutatakse nende kulude kombinatsioon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="0" state="translated">Kui Microsoft Dynamics 365 for Retaili hajutatud tellimuste haldamise (DOM) esimene iteratsioon optimeeris tellimuste määramist täitmisasukohtadele, võttis see arvesse ainult vahemaad.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="0" state="translated">Kuigi vahemaa saab olla kuluga vastastikuses seoses, pole see siiski sama mis kulu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="0" state="translated">Näiteks maksab öine saatmisviis rohkem kui sama vahemaaga kolmepäevane või seitsmepäevane tarne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="0" state="translated">Kulukonfiguratsiooni funktsioon võimaldab jaemüüjatel määratleda ja konfigureerida täiendavad kulukomponendid, mis arvutatakse ja mida võetakse arvesse selleks, et määratled tellimuseridade täitmiseks alusena kasutatav optimaalne asukoht.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="0" state="translated">Kui kulukomponendi on konfigureeritud, kasutab DOM-i solver tellimuse täitmise jaoks optimaalse asukoha määratlemiseks ainult neid kulumääratlusi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="0" state="translated">See ei võta kuluna arvesse vahemaakomponenti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Kui kulukomponente pole aga konfigureeritud, kasutab DOM-i solver tellimuse täitmise jaoks optimaalse asukoha määratlemiseks kuluna vahemaakomponenti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Kulukomponentide seadistamine</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">Süsteemis saab määratleda kaks olulist kulukomponenti: <bpt id="p1">**</bpt>Lähetamine<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>Muud<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="0" state="translated">Mõlemad kulukomponenditüübid toetavad mitut arvutusbaasi, nagu on näha järgmises tabelis.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">Kulukomponendi tüüp</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Arvutuse alus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Lähetamine</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Lihtne</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Astmeline</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Muud</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Müügitellimus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Müügirida</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Koht</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Kulukomponendi tüüp Lähetamine</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="0" state="translated">Selles jaotises selgitatakse, seadistada kulukomponendi tüübi <bpt id="p1">**</bpt>Lähetamine<ept id="p1">**</ept> ja lähetuskulude arvutuse aluse kombinatsioone.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="0" state="translated">Lisaks selgitatakse, kuidas kasutab DOM-i solver iga kombinatsiooni.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="0" state="translated">Kulukomponendi tüüp = lähetamine; arvutuse alus = lihtne</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="0" state="translated">Kulukomponendi tüübi <bpt id="p1">**</bpt>Lähetamine<ept id="p1">**</ept> ja arvutuse aluse <bpt id="p2">**</bpt>Lihtne<ept id="p2">**</ept> kombinatsiooni kasutades põhineb tarneviisi lähetuskulu kas fikseeritud kulul või vahemaal.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="62" state="translated" state-qualifier="fuzzy-match">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kulutegur<ept id="p1">**</ept> – sisestage kuluteguri kordumatu identifikaator.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kirjeldus<ept id="p1">**</ept> – sisestage kuluteguri nimi ja kirjeldus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Alguskuupäev<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>Lõppkuupäev<ept id="p2">**</ept> – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="0" state="translated">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Aktiivne<ept id="p1">**</ept> – näidake, kas kulutegur on aktiivne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="0" state="translated">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Ettevõte<ept id="p1">**</ept> – määrake juriidiline isik, mille jaoks kulutegur konfigureeritakse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="0" state="translated">Kõik arvutuskriteeriumite read peavad olema ette nähtud sama juriidilise isiku jaoks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Tarneviisid<ept id="p1">**</ept> – määrake tarneviisid, mille jaoks kulu konfigureeritakse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Arvutustüüp<ept id="p1">**</ept> – määrake, kuidas tuleb kulu konkreetse tarneviisi jaoks arvutada.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="62" state="translated" state-qualifier="fuzzy-match">Toetatakse kaht arvutustüüpi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Fikseeritud<ept id="p1">**</ept> – tarneviisi jaoks kasutataks fikseeritud kulu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="0" state="translated">Kui valite selle arvutustüübi, määratleb väli <bpt id="p1">**</bpt>Kulu<ept id="p1">**</ept> fikseeritud kulu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Vahemaaühiku kohta<ept id="p1">**</ept> – tarneviisi kulu arvutamiseks korrutatakse väljal <bpt id="p2">**</bpt>Kulu<ept id="p2">**</ept> määratud kuluväärtus tarneaadressi ja asukohtade vahelise vahemaaga.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kulu<ept id="p1">**</ept> – määrake kuluväärtus, mida kasutatakse koos väljaga <bpt id="p2">**</bpt>Arvutuse tüüp<ept id="p2">**</ept> tarneviisi kulu arvutamiseks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Kulukomponendi tüüp = lähetamine; arvutuse alus = astmeline</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">Kulukomponendi tüübi <bpt id="p1">**</bpt>Lähetamine<ept id="p1">**</ept> ja arvutuse aluse <bpt id="p2">**</bpt>Astmeline<ept id="p2">**</ept> kombinatsiooni kasutades põhineb tarneviisi lähetuskulu kas fikseeritud kulul või vahemaal.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="0" state="translated">Selles kombinatsioonis põhineb vahemaa vahemaade astmelisel vahemikul.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kulutegur<ept id="p1">**</ept> – sisestage kuluteguri kordumatu identifikaator.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kirjeldus<ept id="p1">**</ept> – sisestage kuluteguri nimi ja kirjeldus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Vaikekulu<ept id="p1">**</ept> – määrake kulu, mida tuleks kasutada tarneviisi puhul, kui vahemaa tarneaadressi ja asukoha vahel ei lange kokku tarneviisi ühegi astmelise vahemaaga.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Alguskuupäev<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>Lõppkuupäev<ept id="p2">**</ept> – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiivne<ept id="p1">**</ept> – näidake, kas kulutegur on aktiivne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Ettevõte<ept id="p1">**</ept> – määrake juriidiline isik, mille jaoks kulutegur konfigureeritakse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Kõik arvutuskriteeriumite read peavad olema ette nähtud sama juriidilise isiku jaoks.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Tarneviisid<ept id="p1">**</ept> – määrake tarneviisid, mille jaoks kulu konfigureeritakse.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Vahemaa tüüp<ept id="p1">**</ept> – määrake, kas astmelise vahemaa määratlus on vahemaa linnulennul või mööda maad mõõdetav vahemaa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Vahemaaühikud<ept id="p1">**</ept> – määrake ühik, milles astmelist vahemaad mõõdetakse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Vahemaa lähtekoht<ept id="p1">**</ept> – määrake astmelise vahemaa algvahemik.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Vahemaa sihtkoht<ept id="p1">**</ept> – määrake astmelise vahemaa lõppvahemik.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Arvutustüüp<ept id="p1">**</ept> – määrake, kuidas tuleb kulu konkreetse tarneviisi ja astmelise vahemaa jaoks arvutada.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Toetatakse kaht arvutustüüpi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Fikseeritud<ept id="p1">**</ept> – tarneviisi jaoks kasutataks fikseeritud kulu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Kui valite selle arvutustüübi, määratleb väli <bpt id="p1">**</bpt>Kulu<ept id="p1">**</ept> fikseeritud kulu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Vahemaaühiku kohta<ept id="p1">**</ept> – tarneviisi ja astmelise vahemaa kulu arvutamiseks korrutatakse väljal <bpt id="p2">**</bpt>Kulu<ept id="p2">**</ept> määratud kuluväärtus tarneaadressi ja asukohtade vahelise vahemaaga.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kulu<ept id="p1">**</ept> – määrake kuluväärtus, mida kasutatakse koos väljaga <bpt id="p2">**</bpt>Arvutuse tüüp<ept id="p2">**</ept> tarneviisi kulu arvutamiseks.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="0" state="translated">Astmeliste vahemaade määratlemise korral kontrollib süsteem, ega kuskil pole puuduvaid ega kattuvaid vahemaid.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="0" state="translated">Tarneviisi jaoks kasutatav vahemaatüüp peab olema kõigil astmelistel vahemaadel sama.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Muu kulukomponendi tüüp</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">Selles jaotises selgitatakse, seadistada lähetuskulude jaoks kulukomponendi tüübi <bpt id="p1">**</bpt>Muud<ept id="p1">**</ept> ja lähetamisega mitteseotud kulude muu kulutüübi kombinatsioone.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Lisaks selgitatakse, kuidas kasutab DOM-i solver iga kombinatsiooni.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="0" state="translated">Kulukomponendi tüüp = muud; muu kulutüüp = müügitellimus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="0" state="translated">Kulukomponendi tüübi <bpt id="p1">**</bpt>Muud<ept id="p1">**</ept> ja muu kulutüübi <bpt id="p2">**</bpt>Müügitellimus<ept id="p2">**</ept> kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks müügitellimuse tasemel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kulutegur<ept id="p1">**</ept> – sisestage kuluteguri kordumatu identifikaator.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kirjeldus<ept id="p1">**</ept> – sisestage kuluteguri nimi ja kirjeldus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Alguskuupäev<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>Lõppkuupäev<ept id="p2">**</ept> – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiivne<ept id="p1">**</ept> – näidake, kas kulutegur on aktiivne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Kulu<ept id="p1">**</ept> – määrake lähetamisega mitteseotud kulu kuluväärtus müügitellimuse tasemel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Kulukomponendi tüüp = muud; muu kulutüüp = müügirida</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">Kulukomponendi tüübi <bpt id="p1">**</bpt>Muud<ept id="p1">**</ept> ja muu kulutüübi <bpt id="p2">**</bpt>Müügirida<ept id="p2">**</ept> kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks müügitellimuse rea tasemel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kulutegur<ept id="p1">**</ept> – sisestage kuluteguri kordumatu identifikaator.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kirjeldus<ept id="p1">**</ept> – sisestage kuluteguri nimi ja kirjeldus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Alguskuupäev<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>Lõppkuupäev<ept id="p2">**</ept> – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiivne<ept id="p1">**</ept> – näidake, kas kulutegur on aktiivne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kulu<ept id="p1">**</ept> – määrake lähetamisega mitteseotud kulu kuluväärtus müügitellimuse rea tasemel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Kulukomponendi tüüp = muud; muu kulutüüp = asukoht</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Kulukomponendi tüübi <bpt id="p1">**</bpt>Muud<ept id="p1">**</ept> ja muu kulutüübi <bpt id="p2">**</bpt>Asukoht<ept id="p2">**</ept> kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks asukohtade rühma või üksikasukoha jaoks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kulutegur<ept id="p1">**</ept> – sisestage kuluteguri kordumatu identifikaator.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kirjeldus<ept id="p1">**</ept> – sisestage kuluteguri nimi ja kirjeldus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Alguskuupäev<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>Lõppkuupäev<ept id="p2">**</ept> – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiivne<ept id="p1">**</ept> – näidake, kas kulutegur on aktiivne.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Täitmisgrupp<ept id="p1">**</ept> – määrake nende asukohtade grupp, mille jaoks lähetamisega mitteseotud kulu määratletakse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Täitmisasukoht<ept id="p1">**</ept> – määrake asukoht, mille jaoks lähetamisega mitteseotud kulu määratletakse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Asukohapõhiste arvutuskriteeriumite jaoks ei saa ühel ja samal real määrata täitmisgruppi ja täitmisasukohta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kulu<ept id="p1">**</ept> – määrake lähetamisega mitteseotud kulu kuluväärtus täitmisgrupi tasemel või täitmisasukoha tasemel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="0" state="translated">Et DOM võtaks neid kulusid käitamisel arvesse, peate lisama kuluteguri asjakohasele täitmisprofiilile.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>