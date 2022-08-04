---
title: Ühendatud toote kasutusfunktsionaalsus
description: See artikkel kirjeldab tooteandmete integreerimist finantside ja toimingute rakenduste ning rakenduste vahel Dataverse.
author: t-benebo
ms.date: 06/23/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1546cdaf3c63a7ff9a330ae8609595aaf48fbc48
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111482"
---
# <a name="unified-product-experience"></a>Ühendatud toote kasutusfunktsionaalsus

[!include [banner](../../includes/banner.md)]



Kui ettevõtte ökosüsteem koosneb Dynamics 365 rakendustest (nt Finance, Supply Chain Management ja Sales), kasutavad ettevõtted sageli neid rakendusi tooteandmete hankimiseks. Selle põhjuseks on asjaolu, et need rakendused pakuvad vastupidavat tooteinfrastruktuuri, mida täiendavad keerukad hinnakujunduskontseptsioonid ja täpsed vaba kaubavaru andmed. Ettevõtted, kes kasutavad välist toote elutsükli haldussüsteemi (PLM) süsteemi tooteandmete otsimiseks, saavad finantside ja toimingute rakenduste tooteid suunata teistele Dynamics 365 rakendustele. Ühtne tootekogemus viib integreeritud Dataverse toote andmemudeli sisse nii, et kõik rakenduse kasutajad, Power Platform sh kasutajad, saavad kasutada finantside ja toimingute rakendustest pärit rikas tooteandmeid.

Siin on toote andmemudel müügist.

![Toodete andmemudel CE-s.](media/dual-write-product-4.jpg)

Siin on finantside ja toimingute rakenduste toote andmemudel.

![Finantside ja toimingute toodete andmemudel.](media/dual-write-products-5.jpg)

Need kaks tooteandmemudelit on integreeritud ühisesse andmeteenusesse Dataverse, nagu allpool näidatud.

![Dynamics 365 rakenduste toodete andmemudel.](media/dual-write-products-6.jpg)

Topeltkirjutustabeli vastendus toodetele on mõeldud andmete liikumiseks ainult ühel viisil ja reaalajas finantside ja toimingute rakendustest rakendustesse Dataverse. Kuid toote infrastruktuur on tehtud avatuks, et muuta see vajadusel kahesuunaliseks. Kuid võite seda oma vastutusel kohandada, kuna Microsoft ei soovita seda lähenemist.

## <a name="templates"></a>Mallid

Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimis- ja laoala dimensioonid. Nagu järgmine tabel näitab, luuakse tabeli kaartide kogum, et sünkroonida tooteid ja seotud teavet.

Finance and Operations rakendused | Muud Dynamics 365 rakendused | Kirjeldus
-----------------------|--------------------------------|---
[Kõik tooted](mapping-reference.md#138) | msdyn_globalproducts | Kõikide toodete tabel sisaldab kõiki finantside ja toimingute rakendustes saadaolevaid tooteid (nii väljastatud tooteid kui ka väljastatud tooteid).
[CDS väljastatud eristatavad tooted](mapping-reference.md#213) | Toode | Tabel **Toode** sisaldab veerge, mis määratlevad toote. See hõlmab üksikuid tooteid (alamtüübiga tooted) ja tootevariante. Järgmises tabelis on vastendused.
[Värvid](mapping-reference.md#170) | msdyn\_productcolors
[Konfiguratsioonid](mapping-reference.md#171) | msdyn\_productconfigurations
[Tellimuse vaikesätted](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Tootekategooriad](mapping-reference.md#166) | msdyn_productcategories | Iga tootekategooria ning teave selle struktuuri ja omaduste kohta sisaldub tootekategooria tabelis.
[Tootekategooria määramised](mapping-reference.md#167) | msdyn_productcategoryassignments | Toote määramiseks kategooriasse võib kasutada tootekategooria määramiste tabelit.
[Tootekategooria hierarhiad](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Tootehierarhiate abil saate tooteid kategoriseerida või grupeerida. Kategooriahierarhiad on saadaval Dataverse’is toote kategooriahierarhia tabeli kasutamisel.
[Tootekategooria hierarhia rollid](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Tootehierarhiaid saab kasutada erinevate rollide jaoks D365 finantsis ja toimingutes. Need määravad, millist kategooriat igas rollis kasutatakse, kus kasutatakse tootekategooria rolli tabelit.
[Toote vaiketellimissätted V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Tootedimensiooni grupid](mapping-reference.md#173) | msdyn\_productdimensiongroups | Tootedimensioon määratleb, millised tootedimensioonid määratlevad toote.
[Tooteetaloni värvid](mapping-reference.md#187) | msdyn_sharedproductcolors | Tabel **Ühiskasutatav tootevärv** näitab värve, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Dataverse.
[Tooteetaloni konfiguratsioonid](mapping-reference.md#188) | msdyn_sharedproductconfigurations | Tabel **Ühiskasutatava toote konfiguratsioon** näitab konfiguratsioone, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Dataverse.
[Tooteetaloni suurused](mapping-reference.md#190) | msdyn_sharedproductsizes | Tabel **Ühiskasutatava toote suurus** näitab suurust, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Dataverse.
[Tooteetaloni laadid](mapping-reference.md#191) | msdyn_sharedproductstyles | Tabel **Ühiskasutatava toote stiil** näitab stiili, mida konkreetne tooteetalon võib sisaldada. Andmete järjepidevuse tagamiseks on see kontseptsioon üle viidud ühisesse andmeteenusesse Dataverse.
[Tootenumbriga tuvastatud vöötkood](mapping-reference.md#164) | msdyn\_productbarcodes | Toote vöötkoode kasutatakse toodete unikaalseks identifitseerimiseks.
[Tootepõhised ühikute teisendused](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Väljastatud tooted V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | Tabel **msdabel\_ sharedproductdetails** sisaldab finantside ja toimingute rakenduste veerge, mis määratlevad toote ja sisaldavad toote finants- ja haldusteavet.
[Suurused](mapping-reference.md#174) | msdyn\_productsizes
[Laoala dimensioonigrupid](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Toote laoala dimensiooni grupp tähistab meetodit, mida kasutatakse toote paigutuse määratlemiseks laos.
[Laadid](mapping-reference.md#178) | Msdstyle tootestiilid \_
[Jälgimisdimensioonigrupid](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | Toote jälgimisdimensiooni grupp tähistab meetodit, mida kasutatakse toote jälgimiseks laos.
[Ühikud](mapping-reference.md#219) | uoms
[Ühiku teisendused](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Toodete integreerimine

Selles mudelis esindab teenuse Dataverse toodet kahe tabeli kombinatsioon: **Toode** ja **msdyn\_sharedproductdetails.** Esimene tabel sisaldab toote määratlust (toote ainuidentifikaator, toote nimetus ja kirjeldus), teine tabel sisaldab veerge, mis on talletatud toote tasemel. Nende kahe tabeli kombinatsiooni kasutatakse toote määratlemiseks vastavalt varude arvestusühiku mõistele (SKU). Igal väljastatud tootel on oma teave nimetatud tabelites (toote ja ühiskasutatava toote üksikasjad). Kõigi toodete (vabastatud ja mittevabastatud) jälgimiseks kasutatakse tabelit **Globaalsed tooted**.

Kuna toode on esindatud SKUna, saab eristatavate toodete, tooteetalonide ja toote variantide mõisteid jäädvustada teenuses Dataverse järgmisel viisil:

- **Tooted, mille alamtüübi tooteks** on nende endi määratletud tooted. Dimensioone ei ole vaja määrata. Näitena võib tuua konkreetse raamatu. Nende toodete puhul luuakse **Toote** tabelis üks rida ja tabelis **msdyn\_sharedproductdetails** üksuses teine rida. Tooteperekonna rida pole loodud.
- **Tooteetalone** kasutatakse geneeriliste toodetena, mis hoiavad definitsiooni ja reegleid, mis määravad äriprotsesside käitumise. Nende mõistete põhjal saab luua erinevaid tooteid, mida nimetatakse tootevariantideks. Näiteks T-särk on tooteetalon ja selle dimensioonideks võivad olla värv ja suurus. VaVälja saab anda variante, millel on nendest mõõtmetest erinevad kombinatsioonid, näiteks väike sinine T-särk või keskmine roheline T-särk. Integreerimisel luuakse tootetabelis üks rida ühe variandi kohta. See rida sisaldab variandikohast teavet (nt erinevaid dimensioone). Toote üldine teave talletatakse tabelis **msdyn\_sharedproductdetails**. (Seda üldteavet hoitakse tooteetalonis.) Tooteetalon sünkroonitakse teenusega Dataverse niipea, kui väljaantud tooteetalon on loodud (kuid enne variantide väljaandmist).
- **Eristatavad tooted** viitavad kõigile toodete alamtüübi tootele ja kõigile tootevariantidele.

![Toodete andmemudel.](media/dual-write-product.png)

Kui topeltkirjutusfunktsioon on lubatud, sünkroonitakse finantside ja toimingute tooted teistes Dynamics 365 toodetes olekus **Mustand**. Need lisatakse esimesele hinnakirjale, millel on sama valuuta, mida kasutatakse kliendikogemuse rakenduses ja hinnakirja nimes kasutatakse tähestikulist sortimist. Teisisõnu lisatakse need Dynamics 365 rakenduse esimesele hinnaloendile, mis vastab teie juriidilise tabeli valuutale, kus toode finantside ja toimingute rakenduses välja lastakse. Kui antud valuuta puhul hinnakirja pole, luuakse hinnakiri automaatselt ja toode määratakse sellele.

Topeltkirjutuse rakenduse praegune rakendus, mis seostab vaikehinnaloendi üksusega, otsib finantside ja toimingute rakendusega seotud valuutat ja leiab kliendi kaasamise rakendusest esimese hinnaloendi, kasutades hinnakirja nimes tähestikulist sortimist. Kui teil on selle valuuta jaoks mitu hinnakirja, tuleb hinnakirja nime muuta varasemaks tähestikulises järjestuses varasemaks nimeks, kui selle valuuta jaoks on mitu hinnakirja. Kui antud valuuta jaoks hinnakiri puudub, luuakse uus hinnakiri.

Finantside ja toimingute rakenduste vaikimisi tooted sünkroonitakse teiste Dynamics 365 rakendustega olekus **Mustand**. Toote sünkroonimiseks olekuga **Aktiivne**, et saaksite seda kasutada näiteks otse müügitellimuse pakkumistes, tuleb valida järgmine säte: **Süsteem > Haldus > Süsteemihaldus > Süsteemi sätted > Müük** ja seejärel suvand **Loo tooteid aktiivses olekus = jah**.

Kui tooted on sünkroonitud, peate sisestama **finantside** ja toimingute rakenduses välja Müügiüksus väärtuse, sest see on valiku Müük kohustuslik väli.

Dynamics 365 Sales loodud tooteperesid ei toetata toodete topeltkirjutusega sünkroonimist.

Toodete sünkroonimine toimub finantside ja toimingute rakendusest rakendustesse Dataverse. See tähendab Dataverse, et tootetabeli veergude väärtusi saab muuta, kuid sünkroonimise käivitamisel (kui toote veergu muudetakse finantside ja toimingute rakenduses), Dataverse kirjutab see väärtused üle rakenduses.

Finance and Operations rakendused | Klientide kaasamise rakendused |
---|---
[CDS väljastatud eristatavad tooted](mapping-reference.md#213) | Toode |
[Väljastatud tooted V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Kõik tooted](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Tootedimensioonid

Tootedimensioonid on tootevarianti identifitseerivad omadused. Tootevariantide määratlemiseks vastendatakse Dataverse ka nelja tootedimensiooniga (värv, suurus, stiil ja konfiguratsioon). Järgmisel joonisel on näidatud tootedimensiooni värvi andmetabelit. Sama mudelit rakendatakse suurustele, stiilidele ja konfiguratsioonidele.

![Tootedimensioonide andmemudel.](media/dual-write-product-two.png)

Finance and Operations rakendused | Klientide kaasamise rakendused |
---|---
[Värvid](mapping-reference.md#170) | msdyn\_productcolors
[Suurused](mapping-reference.md#174) | msdyn\_productsizes
[Laadid](mapping-reference.md#178) | Msdstyle tootestiilid \_
[Konfiguratsioonid](mapping-reference.md#171) | msdyn\_productconfigurations

Kui tootel on erinevad tootedimensioonid (nt tooteetalonil on suurus ja värv tootedimensioonidena), määratletakse iga eristatav toode (st iga tootevariant) nende dimensioonide kombinatsioonina. Näiteks toode number B0001 on eriti väike must T-särk ja toode number B0002 on väike must T-särk. Sel juhul määratletakse tootedimensioonide olemasolevad kombinatsioonid. Näiteks eelmise näite T-särk võib olla eriti väike ja must, väike ja must, keskmine ja must või suur ja must, kuid see ei saa olla eriti suur ja must. Teisisõnu on määratud tootedimensioonid, mida tooteetalon saab kasutada, ja nende väärtuste alusel saab variante väljastada.

Tootedimensioonide jälgimiseks, mida tooteetalon saab võtta, luuakse ja vastendatakse iga tootedimensiooni jaoks järgmised tabelid jaotises Dataverse. Lisateavet vt teemast [Tooteteabe ülevaade](../../../../supply-chain/pim/product-information.md).

Finance and Operations rakendused | Klientide kaasamise rakendused |
---|---
[Tooteetaloni värvid](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Tooteetaloni konfiguratsioonid](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Tooteetaloni suurused](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Tooteetaloni laadid](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Tootenumbriga tuvastatud vöötkood](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Tellimuse vaikesätted ja tootespetsiifilise vaiketellimuse sätted

Tellimuse vaikesätted määratlevad tegevuskoha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ja standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi. See teave on saadaval Dataverse’is, kasutades tellimuse vaikesätteid ja tootespetsiifilisi tellimuse vaikesätete üksust. Lisateavet funktsioonide kohta saate lugeda tellimuse vaikesätete [artiklist](../../../../supply-chain/production-control/default-order-settings.md).

Finance and Operations rakendused | Klientide kaasamise rakendused |
---|---
[Tellimuse vaikesätted](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Toote vaiketellimissätted V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mõõtühik ja mõõtühiku teisendused

Mõõtühikud ja selle vastav teisendus on saadaval Dataverse’is, mis järgivad diagrammil kuvatavat andmemudelit.

![Mõõtühiku andmemudel.](media/dual-write-product-three.png)

Mõõtühiku mõiste on finantside ja toimingute rakenduste ning teiste Dynamics 365 rakenduste vahel integreeritud. Iga finantsi ja operatsioonide rakenduse ühikuklassi jaoks luuakse ühikugrupp Dynamics 365 rakenduses, mis sisaldab ühiku klassi kuuluvaid ühikuid. Iga ühikurühma jaoks luuakse ka vaikimisi baasühik.

Finance and Operations rakendused | Klientide kaasamise rakendused |
---|---
[Tootepõhised ühikute teisendused](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Ühikud](mapping-reference.md#219) | uoms
[Ühiku teisendused](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Ühikute andmete vastendamise esialgne sünkroonimine finantside ja toimingute ning Dataverse

### <a name="initial-synchronization-of-units"></a>Ühikute esialgne sünkroonimine

Kui topeltkirjutus on lubatud, sünkroonitakse finantside ja toimingute rakenduste ühikud teiste Dynamics 365 rakendustega. Finantside ja toimingute rakenduste abil sünkroonitud ühikugruppidel Dataverse on lipp, mis näitab, et neid hallatakse väliselt.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Ühtivad ühikute ja ühikuklasside/gruppide andmed finantstest ja toimingutest ning teistest Dynamics 365 rakendustest

Kõigepealt on oluline tähele panna, et ühiku integreerimisvõti on msdyn_symbol. Seetõttu peab see väärtus olema kordumatu Dataverse’is või muudes Dynamics 365 rakendustes. Kuna teistes Dynamics 365 rakendustes on selleks paar "Ühikugrupi ID" ja "Nimi", mis määratlevad üksuse ainulaadsuse, peate arvestama erinevate stsenaariumitega ühtivate ühikuandmete Dataverse jaoks finantside ja toimingute rakenduste ning.

Ühikute vastendamiseks/kattumiseks finantside ja toimingute rakendustes ning teistes Dynamics 365 rakendustes:

+ **Üksus kuulub teiste Dynamics 365 rakenduste ühikugruppi, mis vastab seotud ühiku klassile finantside ja toimingute rakendustes**. Sellisel juhul tuleb teistes Dynamics 365 msdyn_symbol veeru nimi täita finantside ja toimingute rakenduste ühikusümboliga. Seega kui andmed viiakse vastavusse, siis seatakse ühikute grupp teistes Dynamics 365 rakendustes väliselt hallatavaks.
+ **Ühik kuulub teiste Dynamics 365 rakenduste ühikugruppi, mis ei vasta finantside ja operatsioonide rakenduste seostatud ühiku klassile (finantside ja toimingute rakendustes puudub olemasolev ühiku klass muude Dynamics 365 rakenduste ühikuklassi jaoks).** Sellisel juhul tuleb väli msdyn_symbol täita suvalise stringiga. Pange tähele, et see väärtus peab olema kordumatu teistes Dynamics 365 rakendustes.

Finantside ühikute ja ühikuklasside jaoks ei ole toiminguid teistes Dynamics 365 rakendustes olemas:

Osana topeltkirjutusega finantside ja toimingute rakenduste ühikugruppidest ja selle vastavatest üksustest luuakse ja sünkroonitakse teistes Dynamics 365 Dataverse rakendustes ja ühikugrupiks seatakse "Väliselt hooldatud". Täiendavat alglaadimist pole vaja.

Ühikute jaoks teistes Dynamics 365 rakendustes, mida pole finantside ja toimingute rakendustes olemas:

Veerg msdyn_symbol tuleb täita kõikide ühikute kohta. Ühikuid saab alati luua finantside ja toimingute rakendustes vastavas ühikuklassis (kui see on olemas). Kui ühiku klassi pole olemas, tuleb kõigepealt luua ühiku klass (pidage meeles, et te ei saa luua ühiku klassi finantside ja operatsioonide rakendustes, v.a laiendi kaudu, kui laiendate enum) sobides muu Dynamics 365 rakenduste ühikugrupiga. Seejärel saate luua ühiku. Pange tähele, et ühiku sümbol finantside ja toimingute rakendustes peab olema msdyn_symbol ühiku muudes Dynamics 365 rakendustes määratud ühik.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Tootepoliitika: dimensioon, jälgimise ja laoala grupid

Tootepoliitikad on poliitikakogumid, mida kasutatakse toodete ja selle omaduste määratlemiseks laos. Tootedimensiooni gruppi, toote jälgimisdimensiooni gruppi ja laoala dimensiooni gruppi võib leida tootepoliitikana.

Finance and Operations rakendused | Klientide kaasamise rakendused |
---|---
[Tootedimensiooni grupid](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Laoala dimensioonigrupid](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Jälgimisdimensioonigrupid](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Tootehierarhiad

Finance and Operations rakendused | Klientide kaasamise rakendused |
---|---
[Tootekategooria määramised](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Tootekategooria hierarhiad](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Tootekategooria hierarhia rollid](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>Toodete integreerimisvõti

Dynamics 365 finantside ja integratsioonivõtmete toodete vahelise Dataverse kordumatuks tuvastamiseks kasutatakse tooteid.
Toodete integreerimisvõti on **(productnumber)**, millega tuvastatakse toode Dataverse’is. Selles on liidetud järgmised üksused: **(ettevõte, msdyn_productnumber)**. Ettevõte **näitab** finantside ja toimingute juriidilist isikut msdyn_productnumber **näitab** finantside ja toimingute kindla toote tootenumbrit.

Teiste Dynamics 365 rakenduste kasutajate jaoks tuvastatakse toode kasutajaliideses veeruga **msdyn_productnumber** (pange tähele, et välja silt on **Tootenumber**). Toote vormil kuvatakse nii ettevõte kui ka msydn_productnumber. Kuid veergu (productnumber), toote kordumatut võtit, ei kuvata.

Kui koostate rakendusi teenuses Dataverse, peaksite olema tähelepanelik, et kasutaksite integratsiooni võtmena suvandit **productnumber** (kordumatu toote ID). Ärge kasutage varianti **msdyn_productnumber**, kuna see pole kordumatu.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Toodete esialgne sünkroonimine ja andmete migratsioon finantsidelt Dataverse ja toimingutesse

### <a name="initial-synchronization-of-products"></a>Toodete esialgne sünkroonimine

Kui topeltkirjutus on lubatud, sünkroonitakse finantside ja toimingute rakenduste tooted ja Dataverse kliendi kaasamise rakendused. Tooteid, mis on Dataverse loodud rakenduses Dynamics 365 ja muid Dynamics 365 rakendusi enne topeltkirjutuse väljastamine, ei värskendata ega vastendata finantside ja toimingute rakenduste tooteandmetega.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Ühtivad tooteandmed finantside ja toimingute ning muude Dynamics 365 rakendustega.

Kui samu tooteid hoitakse (kattumine/sobitamine) Dataverse finantsis ja toimingutes ning teistes Dynamics 365 rakendustes, Dataverse siis finantside ja toimingute toodete topeltkirjutuse lubamisel toimuvad topeltread ja samas tootes ilmuvad topeltread.
Et vältida eelmist olukorda, kui teistel Dynamics 365 rakendustel on tooted, mis kattuvad finantside ja toimingutega/ühtivad, peab administraator, mis lubab topeltkirjutust, **kasutama** veeru ettevõtet (nt "USMF) **ja msdyn_productnumber** (näide: "1234:Black:S") enne toodete sünkroonimist. See tähendab, et need kaks Dataverse veergu tootes tuleb täita vastava ettevõttega finantsis ja toimingutes, millega toode peab olema vastendatud ja koos selle tootenumbriga.

Seejärel, kui sünkroonimine on lubatud ja toimub, sünkroonitakse finantside ja toimingute Dataverse tooted vastendatud toodetega rakenduses ja teistes Dynamics 365 rakendustes. See kehtib nii eristatavate toodete kui ka tootevariantide kohta.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Tooteandmete siirdamine teistest Dynamics 365 rakendustest finantsidesse ja toimingutesse

Kui muudel Dynamics 365 rakendustel on tooted, mida ei ole finantsides ja toimingutes olemas, **saab administraator esmalt kasutada EcoResReleasedProductCreationV2Entity** nende toodete importimiseks finantsidesse ja toimingutesse. Ja teiseks vastendage finantside ja toimingute ning teiste Dynamics 365 rakenduste tooteandmed vastavalt ülaltoodud kirjeldusele.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

