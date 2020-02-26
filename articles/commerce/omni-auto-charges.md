---
title: Omnikanali täpsemad automaatsed kulud
description: See teema kirjeldab võimalusi Commerce’i kanali tellimuste täiendavate tellimuskulude haldamise kohta, kasutades täpsemate automaatsete kulude funktsioone.
author: hhaines
manager: annbe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: fd02a81f35b40e5075ccfe5c9a617d7de4e8250d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022323"
---
# <a name="omni-channel-advanced-auto-charges"></a>Omnikanali täpsemad automaatsed kulud

[!include [banner](includes/banner.md)]

See teema sisaldab teavet rakenduse Dynamics 365 for Retail versioonis 10.0 saadaolevate täpsemate automaatsete kulude funktsiooni konfigureerimise ja juurutamise kohta.

Kui täpsemate automaatsete kulude funktsioonid on lubatud, saavad mis tahes toetatud Commerce’i kanalis (kassa, kõnekeskus ja veebipood) loodud tellimused kasutada [automaatsete kulude](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) konfiguratsioone, mis on määratletud ERP rakenduses nii päise- kui ka reatasemega seotud kuludele.

Varasemates väljaannetes kui rakenduse Retail versioon 10.0 pääsevad [automaatsete kulude](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) konfiguratsioonidele juurde ainult e-kaubanduse ja kõnekeskuse kanalites loodud tellimused. Versioonis 10.0 ja uuemates saavad kassas loodud tellimused kasutada automaatsete kulude konfiguratsioone. Nii saab mitmesuguseid lisakulusid süstemaatiliselt müügikannetesse lisada.

Varasemate versioonide kui 10.0 kasutamisel palutakse kassa kasutajal sisestada saatekulu kassakande Saada kõik või Saada valitud loomise ajal käsitsi. Kui tellimusse kulude kirjutamiseks kasutatakse rakenduse lisakulude võimalusi, ei pakuta süstemaatilist arvutamist – kulude väärtuste arvutamisel toetutakse kasutaja sisendile. Kulusid saab lisada ainult ühe saadetisega seotud kulukoodina ja seda ei saa kassas pärast loomist hõlpsalt redigeerida ega muuta.

Versioonis 10.0 ja uuemates on endiselt võimalik kasutada saatekulude lisamiseks käsitsi viipasid. Kui organisatsioon ei luba parameetrit **Täpsemad automaatsed kulud**, jäävad kassa viibad kulude käsitsi sisestamiseks samaks.

Täpsemate automaatsete kulude funktsioon pakub kassa kasutajatele automaatsete kulude seadistustabelite põhjal süstemaatilisi arvutusi mis tahes määratletud kulude puhul. Peale selle on kasutajatel võimalik lisada või redigeerida piiramatut summat lisakulusid ja -tasusid mis tahes kassa müügikandele päise- või reatasandil (sularaha või klienditellimuse puhul).

## <a name="enabling-advanced-auto-charges"></a>Täpsemate automaatsete kulude lubamine

Minge lehel **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid** vahekaardile **Klienditellimused**. Valige kiirkaardil **Kulud** suvandi **Täpsemate automaatsete kulude kasutamine** sätteks **Jah**.

![Täpsemate automaatsete kulude parameeter](media/advancedchargesparameter.png)

Kui täpsemad automaatsed kulud on lubatud, ei paluta kasutajatel klienditellimuse Saada kõik või Saada valitud loomisel enam saatekulu kassaterminalis käsitsi sisestada. Kassa tellimuse kulusid arvutatakse süstemaatiliselt ja need lisatakse kassa kandesse (kui leitakse vastav automaatsete kulude tabel, mis vastab loodava tellimuse kriteeriumidele). Kasutajad saavad päise- või reatasandil kulusid ka käsitsi lisada või hallata, kasutades äsjalisatud kassatoiminguid, mille saab lisada kassa ekraanipaigutustesse.

Kui täpsemad automaatsed kulud on lubatud, ei kasutata olemasolevat suvandit **Kaubanduse parameetrit** enam valikute **Saatekulude kood** ja **Saatekulude tagasimakse** puhul. Need parameetrid kohalduvad ainult siis, kui parameetri **Kasuta täpsemaid automaatseid kulusid** sätteks on valitud **Ei**.

Enne selle funktsiooni lubamist veenduge, et teie töötajad oleksid läbinud koolituse ja testid, kuna see muudab äriprotsessi voogu saate- või muude kulude arvutamise ja kassa müügitellimuste lisamise meetodis. Veenduge, et mõistaksite protsessivoo mõju kassast kannete loomisele. Kõnekeskuse ja e-kaubanduse tellimuste puhul on täpsemate automaatsete kulude lubamise mõju minimaalne. Kõnekeskuse ja e-kaubanduse rakendustel on endiselt sama käitumine, mis neil oli varem seoses automaatsete kulude tabelitega tellimuse lisatasude arvutamisel. Kõnekeskuse kanali kasutajatel on endiselt võimalik redigeerida päise- või reatasemel käsitsi mis tahes süsteemi arvutatud automaatseid kulusid või lisada päise- või reatasemel käsitsi mis tahes lisakulusid.

## <a name="additional-pos-operations"></a>Kassa lisatoimingud

Selleks et täpsemate automaatsete kulude funktsioon teie kassarakenduse keskkonnas nõuetekohaselt töötaks, on lisatud uued kassatoimingud. Need toimingud tuleb lisada oma [Kassa ekraanipaigutustesse](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) ja juurutada kassaseadmetes täpsemate automaatsete kulude juurutamisel. Kui neid toiminguid ei lisata, ei ole kasutajatel võimalik kassakannetes lisakulusid hallata ega kuluväärtusi, mida automaatsete kulude konfiguratsioonide põhjal süstemaatiliselt arvutatakse, reguleerida ega muuta. Minimaalselt on soovitatav juurutada kassa ekraanipaigutusse toiming **Kulude haldamine**.

Uued toimingud on järgmised.

- **142 – kulude haldamine** – see toiming võimaldab kassa kasutajatel vaadata ja redigeerida kassakande lisakulusid, mis lisati kas käsitsi või süstemaatiliselt automaatsete kulude arvutuste kaudu.
- **141 – päisekulude lisamine** – see toiming võimaldab kasutajal lisada käsitsi päisetasemel lisakulu mis tahes kassa müügikandele (ja valida kasutatava kulude koodi).
- **140 – reakulude lisamine** – see toiming võimaldab kasutajal lisada käsitsi reatasemel lisakulu mis tahes kassa müügikande reale (ja valida kasutatava kulude koodi).
- **143 – kulude ümberarvutamine** – see toiming võimaldab teha müügikande kulude täieliku ümberarvutamise. Mis tahes varasemad kasutaja ülekirjutatud automaatsed kulud arvutatakse ümber praeguse ostukorvi konfiguratsiooni põhjal.

Nagu kõigi kassatoimingute puhul saab teha turbekonfiguratsioonid, mille alusel nõutakse toimingu käivitamiseks halduri kinnitust.

On oluline tähele panna, et ülal loetletud kassatoimingud saab kassa paigutusse lisada isegi siis, kui parameeter **Kasuta täpsemaid automaatseid kulusid** on keelatud. Selles stsenaariumis saavad organisatsioonid veel kasutada lisatud eeliseid nagu käsitsi lisatud kulude vaatamine ja nende redigeerimine toiminguga **Kulude haldamine**. Kasutajad saavad kassakannete jaoks kasutada toiminguid **Lisa päisetasud** ja **Lisa reatasud**, isegi kui parameeter **Kasuta täpsemaid automaatseid kulusid** on keelatud. Toimingul **Kulude ümberarvutus** on vähem funktsioonaalsust, kui seda kasutatakse, kui parameeter **Kasuta täpsemaid automaatseid kulusid** on keelatud. Selle stsenaariumi puhul ei arvutata midagi ümber ja mis tahes kandele käsitsi lisatud kulud lähtestatakse lihtsalt väärtusele $0,00.

## <a name="use-case-examples"></a>Kasutusjuhtumite näited

Selles jaotises on kirjeldatud kasutusjuhtude näidiseid, mis aitavad teil mõista automaatsete kulude ja lisakulude konfigureerimist ning kasutamist kanali tellimuste kontekstis. Need näited illustreerivad rakenduse käitumist, kui parameeter **Kasuta täpsemaid automaatseid kulusid** on lubatud.

### <a name="auto-charges-header-charges-example"></a>Automaatsete kulude päisekulude näide

#### <a name="use-case-scenario"></a>Kasutusjuhu stsenaarium

Jaemüüja soovib lisada kulud automaatselt veosele, kui mis tahes Commerce’i kanalis luuakse kanded, mis nõuavad toodete saatmist kliendile. Jaemüüja pakub kaht tarneviisi: maismaa ja õhu kaudu. Kui klient valib maismaatranspordi ja tellimuse väärtus on väiksem kui 100 eurot, soovib jaemüüja kliendilt veokulu 10,00 eurot. Kui tellimuse väärtus on üle 100 euro ja klient valib maismaatranspordi, ei küsita talt täiendavat veokulu. Kui klient valib kõigi tellimuste puhul õhutranspordi olenemata nende koguväärtusest õhutranspordi, tuleb tal tasuda veokulu 20,00 eurot.

#### <a name="setup-and-configuration"></a>Seadistamine ja konfigureerimine

Selle stsenaariumi puhul tuleb konfigureerida kaks automaatsete kulude tabelit.

Minge jaotisse **Müügireskontro \> Kulude seadistus \> Automaatsed kulud**.

Konfigureerige kaks erinevat päisetasemel automaatset kulu. Konfigureerige üks maismaatranspordi ja teine õhutranspordi jaoks. Selle stsenaariumi puhul konfigureerige need kasutamiseks kõigi klientide puhul.

Maismaatranspordi kulude puhul määratlege lehe **Automaatsed kulud** ridade jaotises kulu, mis rakendatakse tellimustele väärtusevahemikus 0,01 kuni 100 eurot, väärtuseks 10,00 eurot. Looge veel üks kulurida näitamaks, et tellimustele üle 100,01 eurot kulu ei kohaldu.

![Automaatsete kulude näide](media/headerchargesexample.png)

Õhutranspordi kulude puhul määratlege lehe Automaatsed kulud ridade jaotises kõigile tellimustele (väärtusevahemikus 0,01 kuni 9 999 999 eurot kulu 20,00 eurot).

Saatke muudatused Commerce’i skaala üksusesse / kanali andmebaasi nii, et kassa saaks neid kasutada, käivitades töö **1040 jaotusgraafik**.

#### <a name="sales-processing-for-this-scenario"></a>Müügiprotsess selle stsenaariumi puhul

Kui eespool kirjeldatud konfiguratsioonietapid on lõpule viidud ja muudatused kanali andmebaasi rakendatud, kasutavad kõik kassas, kõnekeskuses või e-kaubanduse kanalites loodud klienditellimused või müügikanded, millel on päisetasemel määratud tarne maismaa või õhu kaudu, neid kulusid ja rakendavad need automaatselt müügile.

Sel ajal kohalduvad kulud kõigile neid tarneviise kasutavas juriidilises isikus loodud müügikannetele, kuna puudub funktsionaalsus määrata, et automaatsete kulude konfiguratsioon kohaldub ainult kindlale müügikanalile.

Kassa ja e-kaubanduse stsenaariumide puhul kohalduvad päisetasemel kulud ainult juhul, kui kõik kande müügiread on seatud kasutama täpselt sama tarneviisi, kuna nende tellimuste puhul puudub selgelt määratletud päis. Kui kassas või ee-kaubanduses loodud kannetel on täitmise segaviis, võetakse arvesse ja kohaldatakse ainult reatasemel automaatseid kulusid.

Kõnekeskuse stsenaariumide puhul saab kasutaja hallata tarneviisi seadistust tellimuse päises, mistõttu kohalduvad neile tellimustele päisetasemel kulud, isegi kui mõni müügirida on konfigureeritud kasutama muud tarneviisi. Kõnekeskuse tellimuste päisetasemel kulud põhinevad alati müügitellimuse päisetasemel määratletud tarneviisil.

### <a name="auto-charges-line-charges-example"></a>Automaatsete kulude reakulude näide

#### <a name="use-case-scenario"></a>Kasutusjuhu stsenaarium 

Jaemüüja soovib lisada kliendile seadistustasude puhul lisakulu, kui klient ostab kindla arvutimudeli. Selle arvuti puhul on vajalikud täiendavad kohustuslikud seadistustoiminguid, mille jaemüüja teeb kliendi eest. Jaemüüja on kliente teavitanud, et sellele seadistusele kohaldub lisatasu. Jaemüüja eelistab finantsaruandluse otstarbel hallata selle tasuga seotud kulusid toote müügihinnast eraldi. Selle konkreetse arvutimudeli ostmisel mis tahes kanalist peab klient maksma seadistustasu 19,99 eurot.

#### <a name="setup-and-configuration"></a>Seadistamine ja konfigureerimine

Selle stsenaariumi puhul tuleb konfigureerida üks reatasemel automaatsete kulude tabel.

Minge jaotisse **Müügireskontro \> Kulude seadistus \> Automaatsed kulud**.

Valige rippmenüüst **Tase** suvand **Rida** ja looge uus automaatsete kulude kirje kõigile klientidele ning kindlale tootele või tooterühmale, mille puhul kohaldub seadistustasu.

![Automaatsete kulude näide](media/linechargesexample.png)

Saatke tasud Commerce’i skaala üksusesse / kanali andmebaasi nii, et kassa saaks neid kasutada, käivitades töö **1040 jaotusgraafik**.

#### <a name="sales-processing-for-this-scenario"></a>Müügiprotsess selle stsenaariumi puhul

Kui eespool kirjeldatud konfiguratsioonietapid on lõpule viidud ja muudatused kanali andmebaasi rakendatud, käivitavad kõik kassas, kõnekeskuses või e-kaubanduse kanalites loodud klienditellimused või müügikanded, mille tellimuses sisaldub see kaup, reatasemel kulu süstemaatilise lisamise kogutellimusele.

Sel ajal kohalduvad kulud igale müügireale, mis vastab reatasemel automaatsete kulude konfiguratsioonile juriidilises üksuses, kuna puudub funktsionaalsus konfigureerida reatasemel automaatsete kulude kohaldamine ainult kindlale müügikanalile.

### <a name="manual-header-charges-example"></a>Käsitsi päisekulude näide

#### <a name="use-case-scenario-description"></a>Kasutusjuhu stsenaariumi kirjeldus

Jaemüüja teeb tüüpprotsessile erandi, pakkudes klientidele, kes tellivad poest tooteid, nende kojutoimetamise võimalust. Jaemüüja ja klient on kokku leppinud, et klient maksab selle teenuse eest lisatasu 25 eurot. Tellimuse vastuvõtja peab selle lisatasu kandesse lisama. Kuna tasu on koondtasu ega ole seotud tellimuse ühegi üksiktootega, kasutatakse päisetasu.

#### <a name="setup-and-configuration"></a>Seadistamine ja konfigureerimine

Veenduge, et selles stsenaariumis kasutatavad kulukoodid oleksid õigesti konfigureeritud, minnes jaotisse **Müügireskontro \> Kulude seadistus \> Kulud** ja määratledes stsenaariumi puhul asjakohase kulukoodi.

![Kulude näide](media/chargesexample.png)

Kui kulu tuleb käsitleda saatmisega seotud kuluna saatmisega seotud allahindluste või soodustuste otstarbel, valige kulukoodis suvandi **Saatekulu** sätteks **Jah**. Kui selle kulu puhul on lubatud ka süstemaatiline tagasimaksmine kassarakenduses tagastuskande töötlemisel, valige suvandi **Tagastatav** sätteks **Jah**. Lipp **Tagastatav** kohaldub ainult siis, kui parameetri **Kasuta täpsemaid automaatseid kulusid** sätteks on valitud **Jah**.

Saatke tasud Commerce’i skaala üksusesse / kanali andmebaasi nii, et kassa saaks neid kasutada, käivitades töö **1040 jaotusgraafik**.

Toiming **Päisekulu lisamine** tuleb konfigureerida [kassa ekraanipaigutuses](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) nii, et kasutaja saaks selle toimingu (141) kassas nupuga käivitada. Ekraanipaigutuse muudatused tuleb levitada ka kanalisse, kasutades jaotusgraafiku funktsiooni.

#### <a name="sales-processing-of-manual-header-charges"></a>Müügi käsitsi päisekulu töötlemine

Stsenaariumi käivitamiseks kassarakenduses loob kassa kasutaja müügikande tavapärasel viisil, lisades müügile tooted ja mis tahes muud konfiguratsioonid. Enne makse kogumist peab kasutaja käivitama toiming **Päisekulu lisamine**, mis palub kasutajal valida kulukoodi ja sisestada kulu väärtuse. Kui kasutaja on protsessi lõpule viinud, lisatakse kulu müügitellimusele päisetasemel kuluna.

Selle protsessi saab rakendada kõnekeskuses olemasoleva funktsiooniga **Kulud**, mille leiate tööriistariba vahekaardilt **Müük**. Lehel **Kulude haldamine** saab kasutaja lisada tellimuse päisesse uusi kuluridu.

### <a name="manual-line-charges-example"></a>Käsitsi reakulude näide

#### <a name="use-case-scenario"></a>Kasutusjuhu stsenaarium

Klient soovis, et kaks viiest müügitellimusel olevast kaubast pakitaks kingitusena. Jaemüüja pakub seda lisateenust tasu eest 2,00 eurot kauba kohta. Tellimuse vastuvõtja peab need tasud lisama konkreetsetele kaupadele, mis tuleb kingitusena pakkida.

#### <a name="setup-and-configuration"></a>Seadistamine ja konfigureerimine

Veenduge, et selles stsenaariumis kasutatavad kulukoodid oleksid õigesti konfigureeritud, minnes jaotisse **Müügireskontro \> Kulude seadistus \> Kulud** ja määratledes stsenaariumi puhul asjakohase kulukoodi.

Kui kulu tuleb käsitleda saatmisega seotud kuluna saatmisega seotud allahindluste või soodustuste otstarbel, valige kulukoodis suvandi **Saatekulu** sätteks **Jah**. Kui kulu puhul on lubatud ka süstemaatiline tagasimaksmine kassarakenduses tagastuskande töötlemisel, valige suvandi **Tagastatav** sätteks **Jah**. Lipp **Tagastatav** kohaldub ainult siis, kui parameetri **Kasuta täpsemaid automaatseid kulusid** sätteks on valitud **Jah**.

Saatke tasud Commerce’i skaala üksusesse / kanali andmebaasi nii, et kassa saaks neid kasutada, käivitades töö **1040 jaotusgraafik**.

Toiming **Reakulu lisamine** tuleb konfigureerida [kassa ekraanipaigutuses](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) nii, et kasutaja saaks selle toimingu (toiming 140) kassas nupuga käivitada. Ekraanipaigutuse muudatused tuleb levitada ka kanalisse, kasutades jaotusgraafiku funktsiooni.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Müügi käsitsi reakulu töötlemine

Stsenaariumi käivitamiseks kassarakenduses loob kassa kasutaja müügikande tavapärasel viisil, lisades müügile tooted ja mis tahes muud konfiguratsioonid. Enne makse kogumist peab kasutaja valima kassa kaubaloendi kuval konkreetse rea, millele kulu kohaldub, ja käivitama toimingu **Reakulu lisamine**. Kasutajal palutakse valida kulukood ja sisestada kulu väärtus. Kui kasutaja on protsessi lõpule viinud, seotakse kulu reaga ja lisatakse tellimuse kogusummale reatasemel kuluna. Kasutaja saab protsessi korrata, et lisada vajaduse korral täiendavaid reakulusid kande teistele kaubaridadele.

Sama protsessi saab rakendada kõnekeskuses, kasutades kulude haldamise funktsiooni, mille leiate lehe **Müügitellimus** jaotises **Müügitellimuse read** rippmenüüst **Finantsid**. See avab lehe **Kulude haldamine**, kus kasutaja saab lisada kandele uue reakohase kulu.

## <a name="additional-features"></a>Lisafunktsioonid

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Kulude redigeerimine kassa müügikandes

Toiming **Kulude haldamine** (142) tuleb lisada [kassa ekraanipaigutusse](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) nii, et kasutaja saaks vaadata ja redigeerida või tühistada mis tahes süsteemi arvutatud või käsitsi loodud päise- või reatasemel kulusid. Kui toimingut ei lisata, ei saa kasutajad kulu väärtust kassakandes reguleerida ega vaadata kulude üksikasju, nagu kuluga seotud kulukoodi tüüp.

Kassa lehel **Kulude haldamine** saab kasutaja vaadata nii päise- kui ka reatasemel kulude üksikasju. Kasutaja saab sellel lehel saadaoleva funktsiooniga **Redigeerimine** muuta kindlale kulureale määratud summat. Kui kulurida kirjutatakse käsitsi üle, ei arvutata seda süstemaatiliselt ümber, enne kui kasutaja käivitab toimingu **Kulude ümberarvutus**.

Kui **Kulu tühistamise põhjusekood** on suvandi **Kaubanduse parameetrid** seadistuslehel konfigureeritud, palutakse kasutajal sisestada kassarakenduses kulude muutmisel põhjusekood.

Kui ülekirjutatud kulude kohta on põhjusekoodid sisestatud, on nende tühistuste ülevaatamiseks ja auditeerimiseks saadaval ka uus aruanne. Aruande leiate jaotisest **Jaemüük ja kaubandus \> Päringud ja aruanded \> Kulu tühistamisajalugu**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Kulude tagastamine kassa tagastuskandes

Kui parameetri **Kasuta täpsemaid automaatseid kulusid** sätteks on valitud **Jah**, ei kohaldu suvandile **Saatekulu tagastamine** enam olemasolev Kaubanduse parameeter. Selleks et näidata, millised kulud tuleb süstemaatiliselt kliendile tagastada, kui kasutatakse täpsemaid automaatseid kulusid, veenduge, et seotud kulukood oleks suvandi **Kulukood** seadistuslehel konfigureeritud kui **Tagastatav**. Veenduge, et sätted oleksid jaotusgraafiku protsessi kaudu sünkroonitud teie Commerce’i kanali andmebaasiga.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Kulude tagastamine tagastustellimuse kandes

Kulusid ei tagastata süstemaatiliselt Commerce’is loodud **tagastustellimustele**. Kasutajad peavad valima **tagastustellimuse** loomisel suvandi **Kopeeri kulud**. Kui suvand **Kopeeri kulud** pole valitud, ei tagastata kulusid algsest müügikandest automaatselt. Kui suvand **Kopeeri kulud** on valitud, kopeeritakse kõik kulud tagastustellimusele ja kasutaja saab mis tahes kulusid, mida ta ei soovi tagastada, käsitsi redigeerida või eemaldada. Kõnekeskuse tagastustellimuse protsess ei tuvasta praegu lippu **Tagastatav** suvandi **Kulukood** seadistuses.

### <a name="configuring-pos-receipts-to-show-charges"></a>Kassakviitungite konfigureerimine kuvama kulusid

Sissetuleku reale ja jalusesse on lisatud järgmised kviitungielemendid, et toetada täpsemate automaatsete kulude funktsiooni.

- **Rea saatekulu** – seda reatasemel elementi saab kasutada müügireale kohaldatud kindlate kulukoodide kokkuvõtteks. Siin kuvatakse ainult kulukoodid, mis on tähistatud lehel **Kulukood** kui **Saatekulu**.
- **Rea muud kulud** – seda reatasemel elementi saab kasutada müügireale kohaldatud mis tahes saatmisega mitteseotud kulukoodide kokkuvõtteks. Need on kulukoodid, mille puhul pole lipp **Saatmine** lehel **Kulukood** lubatud.
- **Tellimuse saatekulude üksikasjad** – see jalusetasemel element kuvab tellimusele kohaldatud kulukoodide kirjeldused, mis on tähistatud suvandi **Kulukood** seadistuslehel lipuga **Saatekulu**.
- **Tellimuse saatekulu** – see jalusetasemel element kuvab saatmisega seotud kulude väärtuse eurodes.
- **Tellimuse muude kulude üksikasjad** – see jalusetasemel element kuvab tellimusele kohaldatud kulukoodide kirjelduse, mis ei ole tähistatud saatmisega seotud kulu lipuga.
- **Tellimuse muud kulud** – see jalusetasemel element kuvab muude saatmisega mitteseotud kulude väärtuse eurodes.

Organisatsioonil on soovitatav lisada sissetuleku jalusesse ka vabas vormis teksti väljad, et määratleda alad, mille kohta soovitakse kulude kokkuvõtet.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Kulude arvutamise keelamine, enne kui kassatellimus on lõpule viidud

Mõni organisatsioon võib soovida, et kasutaja oleks kassakandele kõigi müügiridade lisamise lõpetanud, enne kui kulud arvutatakse. Kulude arvutamise keelamiseks, kui kaupu lisatakse kassakandele, lülitage poe kasutatavas suvandis **Funktsiooniprofiil** sisse parameeter **Kulude käsitsi arvutamine**. Selle parameetri lubamisel peab kassa kasutaja kasutama toimingut **Arvuta kogusummad**, kui ta on toodete lisamise kassakandesse lõpule viinud. Seejärel käivitab toiming **Kogusummade arvutamine** vajadust mööda tellimuse päise või ridade puhul mis tahes automaatsete kulude arvutamise.

### <a name="charges-override-reports"></a>Tasude tühistamisaruanded

Kui kasutajad tühistavad arvutatud kulud käsitsi või lisavad kulu kandele käsitsi, on need andmed auditeerimiseks saadaval aruandes **Kulu tühistamisajalugu**. Aruannetele pääseb juurde jaotises **Jaemüük ja kaubandus \> Päringud ja aruanded \> Kulu tühistamisajalugu**. On oluline tähele panna, et aruandele vajalikud andmed imporditakse kanali andmebaasist HQ-sse „P” jaotuse tööde plaanimise kaudu. Seetõttu ei pruugi kassas just tehtud tühistamiste teave aruandes saadaval olla enne, kui see töö on kaupluse kandeandmed HQ-sse üles laadinud.
