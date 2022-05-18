---
title: Tarnehind vs Transpordihaldus
description: Microsoft Dynamics 365 Supply Chain Management pakub transpordi, transpordihalduse (TMS) ja tarnehinnaga töötamiseks kahte erinevat moodulit. Selles teemas summeeritakse kahe mooduli ühised funktsioonid ja tõstetakse esile erinevused nende vahel.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8c59d7d1887986d308cb591ece077cff9f4648a5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690368"
---
# <a name="landed-cost-vs-transportation-management"></a>Tarnehind vs Transpordihaldus

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management pakub kahte erinevat moodulit transpordiga töötamiseks, **Transpordihaldus** (TMS) ja **Tarnehind**. Selles teemas summeeritakse kahe mooduli ühised funktsioonid ja tõstetakse esile erinevused nende vahel. Seda teavet saate kasutada otsustamiseks, milline moodul teie äritavadega kõige paremini sobib. Mõned äritavad töötavad koos TMS-iga paremini, teised aga töötavad kõige paremini tarnehinnaga. Seejärel, sõltuvalt teie äritegevuse nõuetest, võite valida ainult ühe mooduli kasutamise või võite kaks moodulit kombineerida.

See teema ei ole täielik ülevaade mõlema mooduli kõigi funktsioonidest. Selle asemel tõstetakse esile saadav funktsionaalsus vastavalt kauba transportimisele hankijalt teie ettevõtte lattu, kus seda saab tarbida.

## <a name="terminology-reference-data-and-reporting-differences"></a>Terminoloogia, viiteandmed ja aruandluse erinevused

### <a name="terminology-comparison"></a>Terminoloogia võrdlus

TMS-i ja tarnehind kasutavad sarnaste mõistete jaoks erinevaid termineid. Järgmises tabelis võetakse kokku need terminid ja nende kasutamine kahes moodulis.

| TMS termin | Tarnehinna termin | Märkmed |
|----------|------------------|-------|
| **Laadi**<p>*Koorem* on saadetiste kogum, mida transporditakse samaaegselt samas transpordiüksuses (nt veokis või laevas). Koormad võivad olla kas sissetulevad või väljaminevad.</p> | **Reis**<p>Tavaliselt on *reisiks* üks laev, mis reisib ühe *reisi* jooksul. Reisil võib olla mitu *saatmiskonteinerit* ja see võib sisaldada ka teie organisatsiooni erinevate juriidiliste üksuste sissetulevaid tellimusi. Reisid võivad olla ainult saabuvad.</p> | TMS kasutab ka terminit *reisi number*, mis viitab teabeväljale, kuhu saate sisestada ID. TMS-i väljaga pole siiski seostatud ühtki funktsiooni ja see ei ole seotud *reisi* mõistega tarnehind. |
| **Marsruut**<p>*Marsruut* on füüsiline tee transpordi lähtekohast sihtkohta.</p> | **Teekond**<p>*Reis* on füüsiline tee transpordi lähtekohast sihtkohta. Iga reis peab olema määratud teekonnale.</p> | |
| **Marsruudi segmendid**<p>Marsruudil võib olla mitu *marsruudi segmenti*, millest igaüks esindab reisi ühte etappi. Marsruut võib sisaldada mitut vedajat või teenust, millest igaüks loetakse marsruudi segmendiks.</p> | **Etapid**<p>Marsruudil võib olla mitu *lüli*, millest igaüks esindab reisi ühte etappi. Üks lüli võib olla transpordi, maksude käsitlemise või muu tegevuse osa.</p> | |
| **Konteinerid**<p>*Konteiner* võib olla mis tahes pakend, mida TMS kasutab.</p> | **Saatmiskonteinerid**<p>*Saatmiskonteiner* on sõnasõnalt füüsiline saatmiskonteiner, mida teame konteinerlaevadelt.</p> | |
| **Kaubaartiklite koodid**<p>TMS-is (ja teistes kohtades teenuses Supply Chain Management), tähistavad *kaubakoodid* kaubatüüpe. Need võivad mõjutada tariifisid, ohtlike materjalide käsitsemist jne.</p> | **Kaubaartiklite koodid**<p>Tarnehinna puhul *kabakoodid* luuakse juriidilise isiku tasemel. Neid kasutatakse enamasti aruandluses.</p> | Tarnehindvõib kasutada ka kaubakoode, mida kasutatakse TMS-i ja muude kohtade jaoks teenuses Supply Chain Management. Tarnehinna kaubakoode kasutatakse siiski ainult Tarnehinna puhul. |

### <a name="some-reference-data-isnt-shared"></a>Mõned viiteandmed pole ühiskasutuses

TMS-i ja Tarnehind ei jaga viiteandmeid üksuste nagu kulude seadistamine, teekonnad ja etapid puhul. Kui kasutate mõlemat moodulit, peate ühiskasutuseta viiteandmed uuesti looma.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Kontsernisisesed aruanded ei tööta transiidis olevate kaupadega

Järgmised aruanded ei tööta koos transiidis kaupade funktsiooniga, mida pakub Tarnehind:

- [Raport kontsernisisesed kaubad kogu transiidis](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Raport kontsernisisesed kaubad kogu transiidis](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Need aruanded eeldavad, et kaubad pannakse transiiti kohe, kui väljastatakse müügi saateleht, ja et need võetakse transiidist arvestusse saatelehe alusel. Kuid transiidis kaupu ei töödelda sel viisil. Seega, kui kasutate kaubad transiidis ja kontsernisisesed funktsioonid koos, on mõlema aruande tulemused valed.

## <a name="using-the-two-modules-together"></a>Kahe mooduli kasutamine koos

Te saate kasutada TMS-i nii sissetulevate kui ka väljaminevate tegevuste jaoks. Kuigi Tanehinnal on suurem osa samadest põhifunktsioonidest nagu TMS sissetulevate tegevuste puhul, lisab see ka mõned funktsioonid. Seetõttu võite soovida kasutada TMS-i väljaminevate tegevuste jaoks ja Tarnehinda sissetulevate tegevuste jaoks.

Üldiselt ei ole soovitatav kasutada sissetulevate operatsioonide jaoks mõlemat moodulit koos. Peaksite kasutama moodulit, mis vastab teie vajadustele kõige paremini. Kui kasutate neid kahte moodulit koos, ei tohi te nende vahel lähtedokumente jagada. Näiteks ärge kasutage sama ostutellimust nii TMS-i koorma kui ka Tarnehinna reisi puhul. Eriti peate tagama, et te ei seadistaks süsteemi sissetulevaid koormaid automaatselt looma. Kui ostutellimuste kaubad on kaasatud reisi, ei saa neid koorma osana käsitseda.

## <a name="goods-in-transit"></a>Transiidis olevad kaubad

Üks Tarnehinna põhifunktsiooni on võime töödelda transiidis olevaid kaupu. Transiidis olevate kaupade töötlemine annab teile finantsomandi saadetud kaubadele enne, kui need on füüsiliselt sihtlaos vastu võetud. Transiidis olevad kaubad on sageli nõutavad rahvusvahelises kaubanduses.

### <a name="tms-goods-in-transit-features"></a>TMS kaubad transiidifunktsioonis

TMS ei toeta praegu transiidis olevate kaupade töötlemist.

### <a name="landed-cost-goods-in-transit-features"></a>Tarnehind kaubad transiidifunktsioonis

Transiidis olevate kaupade töötlemine on Tarnehinna esmane funktsioon ja pakub järgmist funktsionaalsust:

- **Transiidilaos kaubad** – transiitlaos ladustatavad kaubad saab seostada iga teenuse Supply Chain Management laoga. Kaubad kantakse üle transiidilao kaupadeks pärast algse ostutellimuse arveldamist. Kaubad, mida seal füüsiliselt hoiustatakse, ei muutu tarbimiseks kättesaadavaks enne, kui nad on füüsiliselt kätte saadud. Seetõttu saate kaupade finantsomandi ostutellimuse arveldamisega.
- **Transiidis olevate kaupade pearaamatukonto** – Tarnehind lisab ostutellimuse sisestusreeglitele konkreetse pearaamatu sisestuskonto, et töödelda transiidis olevaid kaupu. Need kaubad pearaamatu transiidikontol toimivad kontona "Arveldamata kaubad". Kui algne ostutellimus arveldatakse ja luuakse transiidis olevate kauade tellimus, sisestatakse ostutellimuse kulu pearaamatu transiidis kaupade kontole seni, kuni kaubad jõuavad füüsilisse lõppasukohta.
- **Jälgimise kontrolli uuendused** – transiidis olevad kaubad tellimused toetavad Tarnehinna jälgimisfunktsiooni. Jälgimise kontroll võimaldab teil uuendada kaupade eeldatavat saabumiskuupäeva transiidi ajal. Jälgimiskontroll värskendab seejärel reisi ja seotud ostutellimuse read. Eeldatav tarnekuupäev on siis koondplaneerimise ja logistika jaoks saadaval.
- **Üla-/alakannete käivitamine** – kui reisireal eeldatava kauba ja laos vastu võetud kaupade vahel tekib hälve, lahendab Tarnehind selle üla-ja/või alakannete loomisega. Seejärel saate neid kandeid hallata nii, nagu soovite neid töödelda, kas ostutellimuse või liikumise töölehe kaudu. Üla- ja alakanded annavad lingi tagasi reisi juurde, algse ostutellimuse juurde ja hälbe uue liikumise töölehe või ostutellimuse juurde.
- **Transiidis tellimused** – Tarnehind loob uue lähtedokumendi, mida nimetatakse *kaubad transiidi tellimuses*. Transiidis olevate kaupade tellimus võimaldab teil arveldada algse ostutellimuse kaupade finantsomandi saamiseks. Ostutellimuse arveldamisel luuakse uus lähtedokument igale ostutellimuse reale, millel on varude dimensioonide kombinatsioon. Kaubad teisaldatakse siis füüsiliselt transiitlattu , kus neid hoitakse vastavalt transiidi tellimuses olevate kaupade tellimusele ja neid ei saa tarbida, kui transiittellimustega kaubad ei ole vastu võetud.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Mitmesugused kulud ja saatmiskulud

Üks olulisemaid kaupade lähetamise ja saadetise haldamise aspekte on saadetistega seotud üldkulude tuvastamine. Need üldkulud pole ostutellimuse ja saadetise või reisiga seotud otsesed varude kulud. Selle asemel on need lisakulud, mis lisanduvad kaupade liikumisel hankijalt teie organisatsioonile. Need kulud võivad hõlmata veokulusid, mis on seotud kaupade saatmisega ühest füüsilisest asukohast teise või maksukulusid, mis on seotud kaupade impordiga välismaiselt hankijalt.

Tarnehind käsitseb neid kulusid luues uut tüüpi kulustruktuuri, mida nimetatakse *automaatsed kulud*. TMS tegeleb nende kuludega lisakulude funktsiooni abil.

### <a name="tms-charge-and-cost-features"></a>TMS-i tasu ja kulufunktsioonid

TMS kasutab lisakulusid seotud lähtedokumendi ridadele eraldatud koormate lisakulude haldamiseks. Need lisakulud saab seadistada kas ostutellimuse rea või ostutellimuse päise tasemel.

TMS-is saab lisakulusid jaotada või jagada saadetise kaalu, mahu või koguse järgi. Tasusid saab jagada veose- või lisakulude järgi. TMS-is täiendavate eraldamismeetodite kasutamiseks on vaja edasist arendust.

### <a name="landed-cost-charge-and-cost-features"></a>Tarnehinna kulu ja kulufunktsioonid

Tarnehind pakub kulufunktsioonide komplekti, mis käsitsevad kaupade saatmisega seotud lisakulusid. Neid kulusid nimetatakse automaatseteks kuludeks ja neid rakendatakse algse lähetuse arveldamisel hinnangulise kulu summa abil. Iga kulutüüpi hallatakse eraldi sisestamisel. Pärast tegelike üldkulude arvete sisestamist uuendatakse hinnangulised kulud automaatselt, et kajastada tegelikke kulusid.

Lisaks saab kauba saatmisega seotud üldkulude eest arve esitada reisi ajal päritolusadamast või mis tahes ajal pärast kauba kättesaamist. See võimalus pakub kaupade tarbimisele suurema paindlikkuse.

Järgmises loendis antakse Tarnehinna kulude ja kulu funktsioonide kohta mõned mõisted:

- **Kuluala** – kulud saab määrata reisi eri tasemetele või *kulualadele*. Kulu saab rakendada reisi tasemel ja jagada reisi iga kauba vahel. Kulusid saab rakendada ka konteineri, ostutellimuse, kauba või üleviimistellimuse tasemel. Iga kulu saab eri aladel eraldi hallata ja jagatakse kuluks kauba kohta.
- **Eraldamismeetodid** – Tarnehinna puhul on saadaval mitmed meetodid. Kulutasusid saab jaotada koguse, dollari summa, väärtuse, kaalu, mahu, mõõtude või kasutaja määratud mahulise mõõdu järgi.
- **Kliiringu/hälbe kontroll** – kulud seadistatakse Tarnehinna puhul eraldi kulukoodi tüübina. Iga kulukoodi tüüp võimaldab teil määrata arvelduskonto hinnanguliste kulude tasude jaoks ning tekkepõhise ja ostuhinna erinevused arvestavad ka hinnanguliste kulude ja tegelike kulude erinevusi. Kui hinnangulised kulud on algselt sisestatud, on kliiringukontol krediit. Pärast tegelike arvete sisestamist sisestatakse tegelikud omahinnad ja hinnangulised kulud debiteeritakse kliiringukontolt.

## <a name="matching-freight-bills-and-invoices"></a>Veosearvete ja arvete sobitamine

### <a name="tms-bill-and-invoice-matching-features"></a>TMS-i arve ja arve sobitamise funktsioonid

TMS võib sobitada veoarveid, mis sisaldavad eeldatavaid kulusid ja arveid koos veose tegeliku kuluga. Arveid saab võtta vastu elektrooniliselt või paberkandjal. Hinnanguliste kulude ja tegeliku kulu vastav hälve ei mõjuta varude hindamist.

Lisateavet vt teemast [Kooskõlasta veos transpordihalduses](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Tarnehinna arve ja arve sobitamise funktsioonid

Tarnehind võib viia kaubaveoarved kokku hinnanguliste kulude tasudega ja esitada arve tegelike kulude kohta hinnangulistest kuludest lähtuvalt. Arveldamise ajal on veokulud arve päevikus ja hinnangulised kulud viiakse kliiringukontolt välja. Lisaks kirjendatakse tegelikud kulud tasumisele kauba eest müüdud kaupade maksumusega koos eeldatavate tasude ja tegelike tasude erinevustega. Selline käitumine võimaldab paindlikkust arveldusprotsessis.

## <a name="tracking"></a>Jälitamine

Nii TMS-i kui ka Tarnehinna oluline omadus on oskus kaupu jälgida ja tuvastada nende asukoht teekonna jooksul lähtekohast kuni lõppsihtlaoni. Jälgimine võimaldab teil jälgida ja uuendada infot, kus kaubad asuvad ja millal nad peaks tarbimiseks lattu saabuma. Lisaks infole kaupade oleku kohta teekonna jooksul annab Tarnehind iga reisi etapi jaoks eeldatavad ja tegelikud kuupäevad.

### <a name="tms-tracking-features"></a>TMS-i jälgimisfunktsioonid

TMS pakub piiratud funktsioone sissetulevate koormuste jälgimiseks. See näitab kuupäevi ja võimaldab integratsiooni üles ehitada, et leida täpne asukoht (nt **Transpordi oleku** lehel).

Iga marsruudi lõigu jaoks saate sisestada hinnangulised graafikud ja saabumisajad.

### <a name="landed-cost-tracking-features"></a>Tarnehinna jälgimise funktsioonid

Tarnehind võib võimaldada jälgimise kontrolli igale reisile, lähtesadamast kuni lõppsihtkohani. Jälgimise kontroll seadistab reisi oleku. Staatus näitab, kas kaubad on liikumises, tollikontrollis või kohalikult kättetoimetamisel teel lõppsihtkoha lattu. Oleku saab määrata ostutellimuse rea, konteineri ja reisi päise tasemel. Seetõttu on teil täpsem kontroll.

Lisaks on reisi iga etapiga seotud kinnitatud eeldatav kuupäev, mis põhineb kindlaksmääratud tarneajal. Kinnitatud ja eeldatavad kohaletoimetamise kuupäevad lisatakse ostutellimuste reale ja kaupadele transiiditellimustes ning neid saab kasutada koondplaneeringu ja logistika jaoks. Lisaks eeldatavatele kuupäevadele saab tegelikke kuupäevi uuendada. Reisi järgnevad etapid uuendatakse seejärel vastavalt.

## <a name="multi-leg-journeys"></a>Mitme etapiga teekonnad

Teekonna mõiste näitab, kus kaubad protsessis asuvad ja kontrollib kaupade olekut transiidi ajal. Kaubad võivad läbida teekonna mitut etappi ja te saate seostada erinevad kulud kindla etapiga. Näited hõlmavad veokulusid laevasõidul ja kohalikke transpordikulusid kaupade transportimisel sadamast sihtkohta.

### <a name="tms-multi-leg-journey-features"></a>TMS-i mitmeetapilised reisifunktsioonid

TMS-is saab marsruute jaotada marsruudisegmentideks, et tähistada mitmeosalisi sõite. TMS saab eraldada kohapealseid hindu ja juurdepääsutasusid üksikutele marsruudilõikudele.

Lisateavet vt teemast [Mitme peatusega veose transpordi marsruutide planeerimine](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Tarnehinna mitmeetapilise teekonna funktsioonid

Tarnehind pakub raamistiku kaupade liikumiseks lähtekohast sihtkohta läbi mitmete etappide, mis on teekonna peatused või sammud. Erinevatel etappidel saab luua reisimallid, mis määratlevad, kuidas kaubad hankijalt teie organisatsioonile liiguvad.

Iga teekonna etapi puhul saate määratleda iga ostutellimuse rea oleku ja sellega seotud täitmisajad. Hinnangulise kohaletoimetamise kuupäeva tuvastamiseks kasutatakse kõigi etappide kombineeritud tarneaega. Mitmeosaliste reiside taotlemiseks on siiski vaja transiiditöötluses oleva kauba olemasolu. Kaupade teekonda hallatakse tabelis, mis on Tarnehinnapõhine tabel.

## <a name="receiving-by-container"></a>Vastuvõtmine konteineri järgi

Võib olla oluline hallata, kuidas kaupu jagatakse ja laevale ladustatakse. Laevas saab kaupu hoida ühes või mitmes konteineris. Kaupade kättesaadmisel on nad konteinerites ja ühe teekonna erinevad konteinereid võidakse kätte saada erinevatel kellaaegadel või erinevatel kuupäevadel.

Nii TMS kui ka Tarnehind pakuvad funktsioone konteineris kaupade vastuvõtmise haldamiseks. TMS kasutab saadetiste konteineriga seotud kaupade, ostutellimuste ja ülekandetellimuste haldamiseks koormate mõistet. TMS toetab vastuvõtmist pakendistruktuuri alusel, mis saadetakse eelteate (ASN) kaudu. Tarnehind kasutab laevakonteinerite mõistet ostutellimuste töötlemiseks ja laeva konteineriga seotud üldkulude kontrollimiseks.

### <a name="tms-receiving-by-container-features"></a>TMS-i funktsioon Vastuvõtmine konteineri järgi

TMS toetab sissetulevaid ASN-e, kõiki laohalduse mobiilirakenduse Warehouse Management kaudu vastuvõtmise variante ja kõiki teenuse Supply Chain Management kliendi kaudu vastuvõtmise meetodeid.

### <a name="landed-cost-receiving-by-container-features"></a>Tarnehinna funktsioon Vastuvõtmine konteineri järgi

Konteineri alusel vastuvõtmise toetamiseks loob Tarnehind konteinerikirjed ja seostab ostutellimused konkreetse saatmiskonteineriga, kasutades selle konteineri ID-d. Üldkulusid saab seejärel rakendada sellele saatmiskonteinerile ja jagada nii, et need on seotud vastavate ostutellimustega.

Tarnehinnas saab konteinereid kätte uut tüüpi kviitungiga, mida nimetatakse *kauba transiidi kviitungiks*, saabumispäevikute või mobiilseadmetes vastuvõtmise kaudu. Saabumispäevikute kasutamisel saab koguseid initsialiseerida transiiditellimusel olevatelt kaupadelt või konteineris olevatest ostutellimuse algsetest ridadest. Tarnehind võimaldab laohalduse mobiilirakenduse Warehouse Management kaudu vastuvõtuks kahte tüüpi töötüüpe.

Tarnehind ei anna kaupade elektrooniliseks vastuvõtmiseks ASN-i. Lisaks ei toeta see laohalduse mobiilirakenduse Warehouse Management voogusid, mis töötlevad koormuse vastuvõtmist, numbrimärkide vastuvõtmist või seganumbrimärkide vastuvõtmist.

## <a name="rate-shopping-by-vendor"></a>Hankija järgi "hinna ostmine"

"Hinna ostmine" võimaldab ettevõttel valida madalaima hinna, kõige kiirema marsruudi või mõlema kaalutluste kombinatsiooni põhjal transpordi hankija.

### <a name="tms-rate-shopping-features"></a>TMS-i "hinna ostmise" funktsioonid

TMS võimaldab teil tuvastada sissetulevate ja väljaminevate tellimuste tarnija- ja marsruutimislahendusi. Näiteks saate tuvastada kiireima marsruudi või soodsaima transpordihinna.

TMS pakub täielikku "hinna ostlemist" ja kaubaveo optimeerimist tariifimarsruudi töölaua kaudu, paindlikke hindamisvõimalusi hindamismootori kaudu, reitingumootori API-d väliste osapooltega integreerimiseks ja mahukaalu toetamist.

Lisateavet leiate jaotisest [Transpordihalduse mootorid](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Tarnehinna hinna ostmise funktsioonid

Tarnehind pakub hankija järgi hinna ostmiseks ainult piiratud tuge. Ehkki saate sisestada ekspedeerija väärtusi, ei võrdle Tarnehind neid mitme hankija vahel.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Juhi sisse- ja väljaregistreerimine koos kohtumiste ajastamisega

Juhi sisse- ja väljaregistreerimise funktsioonid võimaldavad süsteemil jälgida saabumist ja vältida ummikuid laadimiskohtade juures.

### <a name="tms-driver-check-incheck-out-features"></a>TMS-i juhi sisse- ja väljaregistreerimise funktsioon

TMS võimaldab teil luua *kohtumisi*. Kohtumine tähistab sündmusi, mis toimuvad dokis ostutellimuse vastuvõtmiseks, müügitellimuse saatmiseks või sissetuleva või väljamineva laadimise töötlemiseks kindlal kuupäeval ja kindlal kellaajal. Kohtumised tagavad dokkide olemasolu kauba peale- ja mahalaadimiseks ning aitavad ära hoida olukordi, kus mitu vedajat saabuvad korraga ühte kohta.

Süsteem toetab seda, et autojuhid saavad kindla doki uksele sisseregistreerida.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Tarnehinna juhi sisse- ja väljaregistreerimise funktsioon

Tarnehind võib talletada konteineri tarnimiskuupäeva ja -kellaaja hinnangulisi väärtuseid.

## <a name="transfer-orders-and-additional-costs"></a>Üleviimistellimused ja lisakulud

Sageli peavad ettevõtted saama kaupu ladude vahel üle kanda. Kui seda tüüpi ülekanne toimub, on kulud sellega seotud ja te võite soovida neid kulusid ära tunda. Tarnehinnas saab üleviimistellimusi lisada teekonnale või laevale, et jälgida kaupade liikumist ühest laost või asukohast teise, hinnata tarneaega ja eeldatavat tarnekuupäeva ning lisada kaupade üleviimise üldkulud.

### <a name="tms-transfer-order-cost-features"></a>TMS-i üleviimistellimuse kulufunktsioonid

TMS toetab ülekannetega seotud veotasude loomist. Ehkki neid kulusid saab vaadata üleviimistellimusest, ei lisata nende kuludele tarnehinda. Veose vastavusseviimist toetatakse nendel kuludel põhineva veoarve loomise kaudu. Seejärel vastendatakse see veoarve hankija veoarvega.

### <a name="landed-cost-transfer-order-cost-features"></a>Tarnehinna üleviimistellimuse kulufunktsioonid

Tarnehind võimaldab lisada üleviimistellimusi laevale või teekonnale. Sel viisil saate teekonnale saatekulud lisada üleviimistellimuse laekumise ajal varude arveldustena. Üldkulude eest saab arveldada tegelikke kulusid ja neid saab jälgida reisi järgi, et uuendada müüdud kaupade maksumust. Kuigi üleviimistellimused ei kasuta standardses vabastuses transiittöötluses kaupu, saab neid lisada reisidele. Tarnehind lisatakse iga kauba kogukulule.