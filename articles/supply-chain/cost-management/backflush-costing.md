---
title: Omahinna tagasiarvestus
description: Selles teemas tutvustatakse omahinna tagasiarvestuse mõistet, mida kasutatakse lean manufacturingi jaoks.
author: cvocph
manager: tfehr
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: kamaybac
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 945d164fc57ca91baa71a8729da67726de7a9b02
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209703"
---
# <a name="backflush-costing"></a>Omahinna tagasiarvestus

[!include [banner](../includes/banner.md)]

Selles teemas tutvustatakse omahinna tagasiarvestuse mõistet, mida kasutatakse lean manufacturingi jaoks. 

Lean manufacturingi kuluarvutus võimaldab tootmisvoos kasutada kulu akumuleerimise viisi, mida nimetatakse omahinna tagasiarvestuseks. Omahinna tagasiarvestuse meetodi puhul akumuleeruvad tarbitud otsesed materjalikulud tootmisvoo lõpetamata toodangu (WIP) kulukontole. Kasutatakse standardkuludele laomudeligruppi. Töövoost saadud tooted lahutatakse lõpetamata toodangust standardomahinnaga. Standardomahinna ja omahinna tagasiarvestuse peamine erinevus on see, et omahinna tagasiarvestuse puhul ei arvutata hälbeid kanbani või lõpetatud toote kohta. Selle asemel arvutatakse hälbeid tootmisvoo kohta perioodi jooksul. See meetod tutvustab materjalitarbimise aruandluse jaoks tõelist säästlikkuse mõistet. Sihtotstarbelisi komplekteeritud materjalikoguseid ei esitada kanban- ega tootmistellimuse jaoks. Selle asemel koondatakse töövoole täielikud partiid või materjali käsitlemisühikud. Pärast seda, kui partiid või materjali käsitlemisühikud on tühjana registreeritud, deklareeritakse need tarbituks. Kasutada võib täiustatud tarbimist, sõltuvalt [töövoo konfiguratsioonist](../production-control/lean-manufacturing-modeling-lean-organization.md). Enne täiustatud tarbimise kasutamist peavad organisatsioonid endale lubama materjali kaotamist tootmisvoo lõpetamata toodangus. Perioodiline omahinna tagasiarvestus määrab lõpetamata toodangu kehtiva väärtuse perioodi lõppu. See määramine põhineb kanbani materjali käsitlemisühikutel ja kanban-töö olekul. Kõrvalekaldeid kehtiva väärtuse ja tegeliku lõpetamata toodangu väärtuse iga kulugrupi ja kauba kohta vahel arvutatakse ja näidatakse hälvetena.

## <a name="configuring-backflush-costing"></a>Omahinna tagasiarvestuse konfigureerimine
Kuluarvestuse lubamiseks peate läbima järgmise häälestuse.

-   **Häälestage lõpetamata toodangu kontod tootmisgrupile ja tootmisvoole.** Tootmisvoo lõpetamata toodangu kontod on määratletud tootmisgrupis. Omahinna tagasiarvestuse tootmisvoog arvutab hälbeid erinevusena lõpetamata toodangu väärtuses enne ja pärast iga tootmisvoo omahinna tagasiarvestuse käivitamist. Seetõttu soovitame teil luua lõpetamata toodangu (WIP) konto iga tootmisvoo jaoks.
-   **Määrake ressursigrupile kulukategooria** Peate määrama tööraku käitusaja kategooriale kulukategooria. Kui tahate määrata hälbeid tegevuse järgi, peaksite looma kulukategooria igale töörakule. Häälestuse ja koguse kulukategooriaid ei arvestata lean manufacturingi kuluarvestuses. Lõpetamata toodangu kontosid ressursigrupi kohta eiratakse omahinna tagasiarvestuses. Alltöövõtu tegevuste puhul pole kulukategooria nõutav. Selle asemel kasutatakse kulugruppi, mis on määratud aktiivsele teenusele.
-   **Määrake kulugrupid.** Tootmisvoos kulu panuse segmentimise lubamiseks peate määrama kulugrupid kulugrupi tüübi järgi.
    -   **Otsese materjalikulu kulugrupp** \– otsene materjalikulu nõuab kulugruppi, mis tuvastab materjali kategooria kuluarvutuseks. See kulugrupp esitab koondatud ülevaate otsese materjalikulu kuludest, lõpetamata toodangust ja hälvetest.
    -   **Otsese tootmiskulu kulugrupp** \– otsese tootmiskulu kulugrupp võtab tööressursside otsese kulu panuse tootmisvoo jaoks. See kulugrupp esitab koondatud ülevaate otsese tootmiskulu kuludest, lõpetamata toodangust ja hälvetest.
    -   **Kaudse kulu grupp** \– kaudse kulu grupp on vajalik kaudse kulu panuse arvutamisel tootmisvoole. See kulugrupp esitab koondatud ülevaate kaudse kulu kuludest, lõpetamata toodangust ja hälvetest.
    -   **Otse väljasttellimise kulugrupp** \– teenuste kulugrupp esitab koondatud ülevaate määratud kulust ja lõpetamata toodangust ning määrab allhanketeenuste kulu hälbed.
    -   **Valmistoote kulugrupp** \– valmistoodetele on vaja kulugruppi, mis tuvastab kuluarvestuse jaoks tootekategooria. See kulugrupp esitab koondatud ülevaate tootekategooria kuludest, lõpetamata toodangust ja hälvetest. Toodete standardkulu arvutamisel kasutatakse kuluarvutust, mis põhineb kooslusel (BOM) ja tootmisvool ning kanban-reeglitel või protsessil.

### <a name="costing-sheet"></a>Kuluarvutustabel

Kuluarvutustabel on ettevõtte kulustruktuuri mudeliks ja tugineb kulugruppidel, et kulusid klassifitseerida. Kuluarvutustabelil on mitu vormi. See näitab kuluteavet vastavalt selles loodud struktuurile. Kuluarvutustabelis saate ka määratleda valemit, mida kasutatakse kaudse kulu arvutamiseks. Arvutusvalemi aluseks võivad olla kogused, kaal, maht või väärtus.

-   **Määrake kuluversioon.** Kuluversioonis määrab ettevõte, kuidas kulu tuleb hallata. Kuluversioon võib sisaldada standardsete kulukirjete kogumit või planeeritud kulukirjete kogumit, sõltuvalt kuluversioonile määratud kulutüübist. Kuluversioon, mida kasutatakse lean manufacturingi kuluarvutuseks, peab põhinema standardomahinnal.
-   **Määrake väljastatud toodetele laomudeligrupp.** Kõik tooted, mis on tootmisvooga seotud, tuleb määrata laomudeligruppi, mis kasutab laomudeligruppi **Standardomahind**. Standardomahinda säilitatakse iga tegevuskoha ja aktiveerimiskuupäeva kohta. Tooteetalonide puhul saab laomudeligruppi valida, kui hinda säilitatakse iga variandi või tooteetaloni kohta.
-   **Allhanketeenuseid määratletakse kui inventeerimata teenuseid.** Allhanketegevustel pole laomudeligruppi. Allhanketegevuse kulude õigesti arvutamiseks peate veenduma, et teenuse tegevus kuuluks laomudeligruppi, kus varude poliitika on seatud olekusse **Ladustatav toode = vale**.

Toodangu puhul vajab kuluarvutus, mis põhineb tootmisvool, et standardomahind säilitataks teenuste jaoks, mis on seotud allhanketeenustega. Kulugruppi, mis on teenustele määratud, kasutatakse allhanketegevuse kuluhälvete määramiseks.

## <a name="cost-calculation-for-lean-manufacturing"></a>Kulu kalkulatsioon lean manufacturingi jaoks
Tootmisvoo pakutud toodete puhul peab koosluse arvutamine põhinema protsessiversioonil või tootmisvool. Koosluse kalkulatsioon arvutab toote kulu ja jaotumist ressurssidele ning materjalile, mis on toote valmistamiseks vajalikud. Selleks, et lahutada WIP-kontost tootmisvoo jaoks, kasutatakse toote jaotust kauba ja kulugrupi alusel.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Arvutamine, mis põhineb tootmisvool

Lean manufacturing rakendusele Dynamics 365 Supply Chain Management on protsessidest sõltumatu. Kuluarvutus toodete jaoks, mida pakutakse tootmisvoost, võib põhineda tootmisvool enesel. Enne arvutuse tegemist tuleb luua kanban-reegel, mis pakub toodet tootmisvoost. Kui toodet saab arvutamiskuupäeval pakkuda mitmest tootmisvoost samas tegevuskohas, saate koosluse kalkulatsiooni jaoks valida tootmisvoo. Lehel **Vaikimisi tootmisvoog** saate konfigureerida vaikimisi tootmisvoo iga kauba jaoks. Kui ühes töövoos, mis on kalkulatsiooni kuupäeval aktiivne, on sama kauba jaoks olemas mitu kanban-reeglit, siis valib kalkulatsioon esimese kanban-reegli, mis on kalkulatsiooni jaoks aktiivne.

### <a name="calculation-that-is-based-on-the-route"></a>Protsessil põhinev kalkulatsioon

Protsessil põhinev kalkulatsioon on sama sobiv, kui tootmisvool põhinev kalkulatsioon. Siiski ei kasuta protsessil põhinev kalkulatsioon kuluarvutuse ega lean manufacturingi funktsioone. Protsess peaks kasutama ressursigruppide puhul ressursitingimusi. Süstemaatiliste hälvete vältimiseks peaks see kasutama ka samu töörakke või vähemalt samu kulukategooriaid. Jällegi, peaksite vältima kulukategooriaid häälestuse ja koguse jaoks. Need ei aita arvutada kulu detailsema jaotusega kui lean manufacturingi omahinna tagasiarvestus. Otsustamisel, millist suvandit (tootmisvoog või protsess) peaksite kasutama kulude arvutamiseks, arvestage kulude jaotamise tulemusi. Parem suvand on versioon, mis on lähemal tegelikkusele ja toodab üldiselt vähem hälbeid. Lean manufacturingi keskkonnas, kus toodet pakub üksainus tootmisvoog ja üks kanban-reegel, on tootmisvool põhinev kalkulatsioon tõenäoliselt täpsem. Toote puhul, mida saab pakkuda lean manufacturing ja tootmistellimus samas tegevuskohas või millel võib samas voos olla mitu tootmisvoogu või mitu kanban-reeglit, võib kalkulatsioon olla täpsem, kui see põhineb protsessiversioonil, mis on valmistatud just kuluarvutuse ja mitte tootmise jaoks. Tootmisvoo kalkulatsiooni tuleb kasutada toodete arvutamisel, mis hõlmavad allhanget. Tootmistellimusega allhanke ja lean manufacturingi allhanke kulumudelid kaht erinevat meetodit. Lean manufacturingiga tutvustatakse uut kulugrupi tüüpi **Otse väljasttellimine**, et arvutada allhanketeenuseid.

## <a name="material-consumption"></a>Materjali tarbimine
Kui materjali tarbitakse laost lõpetamata toodangusse, siis lisatakse materjali kulu lõpetamata toodangule selle kulugrupi standardomahinnaga. See toiming toimub järgmistel tingimustel.

-   Kanban-väljaminekud on sisestatud kanban-komplekteerimisridadele, mis värskendavad varu.
-   Lõpetatud on ülekandetööd, mis värskendavad varu komplekteerimisel aga mitte sissetulekul (materjali ülekanne laost lõpetamata toodangusse).

## <a name="receiving-products-from-the-production-flow"></a>Toodete saamine tootmisvoost
Tooteid saadakse tootmisvoost järgmistel tingimustel.

-   Lõpetatud on protsessitööd, mille säte **Värskenda varusid sissetulekul** on seatud olekusse **Jah**.
-   Lõpetatud on ülekandetööd, mis värskendavad varusid sissetulekul, kuid mille säte **Värskenda varusid komplekteerimisel** on seatud olekusse **Ei** (ülekandmine lõpetamata toodangust varudesse). See suvand võimaldab saada kõiki tooteid tootmisvoost kooslusest ja protsessi konfiguratsioonist sõltumatult. Protsess järgib lihtsalt füüsilisi vooge. See suvand sobib eriti kõrvalsaaduste, kaastoodete või tootmisvoo praagi jaoks ja tootmisvoo lõpetamata toodangu kulusaldo vastavaks parandamiseks.

Töövoost saadud tooted lahutatakse lõpetamata toodangust.

## <a name="products-in-wip"></a>Tooted lõpetamata toodangus
Lean manufacturingi lõpetamata toodangu mudel võimaldab kasutada kanbani materjali käsitlemisühiku olekut, et hallata lõpetamata toodangu osaks olevaid materjale, pooltooteid ja lõpetatud tooteid.

-   **Määratud** \– kanban võib kasutada tarbitud materjali, mis on arvestatud lõpetamata toodangus.
-   **Vastu võetud** \– kui kanban viitab viimasele tegevusele, kus säte **Värskenda varusid sissetulekul** on seatud olekusse **Ei**, esindab see toote või pooltoote kogu materjali käsitlemisühikut, mis pole varudesse registreeritud.

Pange tähele, et lõpetamata toodangu materjal ei ole nähtav laovarude ülevaadetes. Siiski on see nähtav kanban-koguse ülevaadetes.

## <a name="consuming-products-in-wip"></a>Lõpetamata toodangu toodete tarbimine
Lõpetamata toodangu tooteid tarbitakse siis, kui vastavad kanbani materjali käsitlemisühikud on tühjendatud. Kanbani tühjendamise signaal ei tooda aktiivset kuluarvutuse kannet, kuid jõustub järgmisel omahinna tagasiarvestuse käivitamisel. Tüjendatud kanbani materjali käsitlemisühikuid ei arvestata enam laos saadavatena ja arvutatakse seega perioodi jooksul tarbituna.

### <a name="automatic-empty-registration"></a>Automaatne tühjendamise registreerimine

Plaanitud või sündmuse kanbaneid saab kanban-reeglis määrata automaatselt tühjendamist registreerima.

-   **Kui materjali käsitlemisühikud on vastu võetud** \– vaikimisi deklareeritakse plaanitud kanbanite puhul materjal tarbituks siis, kui kanbani viimane töö lõpetatakse. Fikseeritud kogusega kanbanite puhul soovitatakse seda suvandit vaid ühe kohaga kanbanite jaoks, kuna see tagastab kaardi nõudluse allikasse iga kord, kui kanban võetakse viimases sihtkohas vastu.
-   **Kui lähtetingimus on registreeritud** \– see suvand on saadaval ainult sündmuse kanbanite jaoks ja on nendele vaikesuvand. Lõpetamata toodangu puhul on see suvand kasulik lõpetamata toodangu puhtana hoidmisel, kuna lõpetamata toodangu kanbanite komponendid tühjendatakse automaatselt ja on seega lõpetamata toodangust tarbitud siis, kui peamine kanban on ette valmistatud.

Kokkuvõtteks: kanbani materjali käsitlemisühikuid saab määrata (= lõpetamata), vastu võtta (= täielik) või tühjendada. Osalist tühjendamist pole. Seega on tarbimise täpseks registreerimiseks oluline, et piirate kanbani tootekoguseid nii, et need on väiksemad kui tarbimine perioodi kohta. Tooted, mis liigutatakse tööde juhtimisse suurte partiidena, mis täidavad päevade või nädalate jagu nõudlust, ei tohiks tarbida lõpetamata toodangusse. Selle asemel peaks neid tooteid hoidma varudes.

## <a name="backflush-costing"></a>Omahinna tagasiarvestus
Peaksite käivitama omahinna tagasiarvestuse, et perioodiliselt hinnata lõpetamata toodangut ja luua perioodi lõpu olek, mis arvutab materjali, tööjõu ja kaudsete kulude hälbeid. Arvutatud hälbed sisestatakse hälvete kontodele. Omahinna tagasiarvestuse protsessis kasutatakse kõiki juriidilise isiku töövooge samas partiikäivituses. Kui omahinna tagasiarvestus käivitatakse pakett-tööna, võib töötlemine olla tootmisvooga mitmelõimeline. Tagasiarvestuse periood määratakse lõppkuupäevaga. Kuupäevale ei saa sisestada uusi kandeid, kui omahinna tagasiarvestuse kalkulatsioon on käivitatud. Te ei tohiks kunagi käivitada praegusele kuupäevale omahinna tagasiarvestust enne, kui päev läbi on. Omahinna tagasiarvestus läbib järgmised sammud.

1.  Määrab tootmisvoos kasutamata kogused perioodi lõpu kuupäeva seisuga. Pärast omahinna tagasiarvestuse käivitamist saate vaadata kasutamata koguseid kuluarvutuse käivitamise kuupäeval dialoogiboksis **Kasutamata kogused**.
2.  Arvutab perioodi jooksul tootmisvoo neto realiseeritud kasutuse.
3.  Tühjendab lõpetamata toodangu realiseeritud ressursi tarbimisest ja toodetest.
4.  Arvutab perioodi jooksul standardomahinna tootmishälbed. **Perioodi jooksul tarbitud komponentide puhul läbib tagasiarvestus järgmised sammud.**
    -   Värskendab finantsiliselt materjali neto realiseeritud koguseid, mida tootmisvoog perioodi jooksul tarbis. Süsteem töötleb üksikuid laokandeid elavjärjekorra (FIFO) alusel, et töövoo jaoks füüsiliselt värskendatud kandeid finantsiliselt värskendada, kuni perioodi jaoks saavutatakse neto realiseeritud kogused.
    -   Kanded on finantsiliselt tükeldatud, et vastendada täpsed tarbitud kogused.
    -   Lõpetamata toodangu tootmisvoo kasutamata kogused jäävad füüsiliselt värskendatud olekusse.

    **Perioodi jooksul lõpetatud tootmiskoguste puhul läbib tagasiarvestus järgmised sammud.**
    -   Värskendab finantsiliselt lõpetatud koguste varude kandeid perioodi jaoks.

    **Teisenduskulu jaoks läbib tagasiarvestus järgmised sammud.**
    -   Värskendab finantsiliselt perioodi jooksul salvestatud rakendatud teisenduskulu kandeid (protsessikandeid).
    -   Värskendab finantsiliselt kõiki otseseid tootmiskulusid. Akumuleerib kõik kanbani protsessitööd, mis perioodi jooksul lõpetatakse.
    -   Arvutab kõik perioodi jooksul tarbitud materjalide kaudsed kulud ja lahutab selle lõpetatud toodangust. Ülejäänud kaudsed kulud sisestatakse hälbena.

5.  Arvutab standardomahinna tootmishälbed. Hälve arvutatakse iga kulugrupi kohta.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]