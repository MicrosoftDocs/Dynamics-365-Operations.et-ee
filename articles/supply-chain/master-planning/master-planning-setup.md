---
title: Koondplaneerimise seadistamine
description: See artikkel kirjeldab mitmesuguseid olulisi strateegiaid ja parameetreid, mida kasutatakse koondplaneerimise seadistamiseks.
author: t-benebo
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: effdefcf8326babaa89d7de4b28a86bbef7280f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888553"
---
# <a name="set-up-master-planning"></a>Koondplaneerimise seadistamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab mitmesuguseid olulisi strateegiaid ja parameetreid, mida kasutatakse koondplaneerimise seadistamiseks. See sisaldab ülevaadet koondplaneerimise kasutatavate plaanide tüüpidest ja selgitab, millist plaani strateegiat peaksite sõltuvalt ettevõtte vajadustest kasutama. Samuti kirjeldatakse põhiparameetreid, mis plaani mõjutavad, ja selgitatakse, kuidas need parameetrid soovitatud plaanitud tellimusi mõjutavad.

## <a name="types-of-master-plans"></a>Koondplaanide tüübid

Koondplaneerimises on kahesuguseid plaane: staatiline ja dünaamiline. Iga tüüp on mõeldud erinevaks kasutamiseks. Parimaks jõudluseks on soovitatav kasutada stsenaariumi jaoks sobivat plaani.

### <a name="static-plan"></a>Staatiline plaan

Staatiline plaan jääb muutumatuks hoolimata pakkumise ja nõudluse muudatustest, kuni koondplaneerimise järgmisel korral käivitamiseni.

Staatilist plaani kasutatakse soovitatud tellimuste kinnitamiseks ja tagamiseks. Seda plaani saavad kasutada ettevõtte erinevad töötajad (nt sisseostja või tooteplaanija), toetudes sellele oma otsuste langetamisel ja igapäevaste tööde tegemisel.

Staatiline plaan toetab ka taasloomist. Täiesti uus optimeeritud plaan arvutatakse iga kord, kui koondplaneerimise käitatakse, ja olemasolevad kinnitamata tellimused kustutatakse.

### <a name="dynamic-plan"></a>Dünaamiline plaan

Dünaamiline plaan algab tavaliselt staatilise plaani koopiana, kuid seda saab uuendada iga kord, kui koondandmed muutuvad. Näiteks kui andmed muutuvad, luuakse uus müügitellimus.

Dünaamilist plaani kasutatakse sihtplaneerimiseks. See võimaldab ettevõttel jälgida tellimusevõrgu muutusi ja kauba kättesaadavust, häirimata teiste inimeste tööks vajalikku staatilist plaani. Seda kasutatakse eriti lubamiseks võimaldamiseks (CTP). Dünaamiline plaan on vaikeplaan, kui netonõuded avatakse tellimuse lehtedelt (nt müügitellimuse, ostutellimuse või tootmistellimuse lehed).

Dünaamiline plaan kasutab netomuutust. Seetõttu aitab see tagada kiirema töötamise aja.

## <a name="strategies-for-using-master-plans"></a>Koondplaanide kasutamise strateegiad

Koondplaneerimise käigus saate kasutada kas ühte või kahte plaani. Kasutatav strateegia oleneb teie ettevõtte vajadustest.

### <a name="one-plan-strategy"></a>Ühe plaaniga strateegia

Ühe plaaniga strateegia puhul kasutate staatilise plaani ja dünaamilise plaani jaoks sama koondplaani. Seda strateegiat kasutatakse lattutootmise stsenaariumite puhul, kus tavaliselt te ei pea tellimuse täitmise plaani simuleerima.

Ühe plaaniga strateegiat kasutatakse tavaliselt jaemüügis ja levitamises või kus müügi tarnekuupäevad kinnitatakse teenusetaseme lepete (SLAd) või täitmisaja alusel. Plaani jaoks saab tarnekuupäeva kontrolli kasutada ilma CTP-ta.

Kui peate simulatsiooni läbi viima, saab plaani simulatsiooni nõudvate kaupade puhul uuesti käitada. Tellimuse simulatsiooni loodavad plaanitud tellimused tavaliselt kinnitatakse.

### <a name="two-plan-strategy"></a>Kahe plaaniga strateegia

Kahe plaaniga strateegia puhul kasutate staatilist plaani ja teistsugust dünaamilist plaani. Kahe plaaniga strateegiat kasutatakse tavaliselt tellimisel konfigureerimise ja tellimuse järgi tegemise stsenaariumites, kus peate viima läbi müügitellimuse simulatsioone ja arvutama müügitellimuste täpsed tarnekuupäevad, kuid arvutused ei tohi igapäevaseid operatsioone mõjutada. Need simulatsioonid viiakse alati läbi dünaamilises plaanis. Kahe plaaniga strateegia on kasulik näiteks autonduse ja originaalseadmete tootmise (OEM) tööstusharudes.

Kahe plaaniga strateegia jaoks saab kasutada tarnekuupäeva kontrolli CTP-d. CTP kasutamisel käivitab see automaatselt dünaamilise plaani käitamise.

### <a name="setting-up-the-plans"></a>Plaanide seadistamine

Plaane saate luua lehel **Koondplaanid** (**Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**).

Saate määrata, milliseid plaane staatilise plaani ja dünaamilise plaani jaoks kasutatakse, häälestades väljad **Praegune staatiline koondplaan** ja **Praegune dünaamiline koondplaan** lehel **Koondplaneerimise parameetrid** (**Koondplaneerimine \> Seadistus \> Koondplaneerimise parameetrid**). Ühe plaaniga strateegia kasutamiseks valige väljadel **Praegune staatiline koondplaan** ja **Praegune dünaamiline koondplaan** sama plaan.

## <a name="types-of-planning-methods"></a>Planeerimismeetodite tüübid

Koondplaneerimise käitamiseks saab kasutada kolme arvutusmeetodit: taasloomine ja netomuutus. Iga meetod loob käitamisel teistsuguse plaani.

Planeerimismeetodi saate määratleda dialoogiaknas **Koondplaneerimise käitus**. Selle dialoogiakna avamiseks valige suvandid **Koondplaneerimine \> Koondplaneerimine \> Käivita \> Koondplaneerimine** või valige käsk **Käivita** tööruumis **Koondplaneerimine**.

### <a name="regeneration"></a>Taasloomine

Taasloomise planeerimismeetod kustutab olemasolevad plaanitud tellimused, mis pole kinnitatud. See loob kõikide nõuete põhjal uued plaanitud tellimused. Taasloomine on ainuke planeerimismeetod, mis on staatilise plaani jaoks saadaval.

- Tarne muudatused võetakse arvesse. Need muudatused hõlmavad prognoosi muudatusi.
- See meetod arvestab kattekoodiga **Periood**.
- See meetod toetab toote asendamise funktsiooni (PI).

### <a name="net-change"></a>Netomuutus

Netomuutuse planeerimismeetod loob plaanitud tellimused, et katta nõuded, mis on pärast viimast koondplaneerimise käitamist loodud või muudetud. Selle meetodi käitamisel tarne muudatustega ei arvestata. Süsteem ei võta uusi tarneid arvesse ja varem loodud plaanitud tellimusi ei kustutata, kui need pole enam vajalikud. Netomuudatuse planeerimismeetod töötab taasloomise meetodist kiiremini. See on saadaval ainult dünaamilistes plaanides.

- Tegevuste kuupäevad ja tähtajad uuendatakse kõigi vajaduste puhul.
- See meetod ei arvesta kattekoodiga **Periood**.
- See meetod ei täida prognoosi, isegi kui see on plaanis valitud.
- See meetod ei toeta toote asendamise funktsiooni (PI).

### <a name="net-change-minimized"></a>Netomuutus minimiseeritud

Minimiseeritud netomuutuse planeerimismeetod loob plaanitud tellimused, et katta ainult nõuded, mis on pärast viimast koondplaneerimise ajastamise käitamist loodud või muudetud. Selle meetodi puhul uuendatakse erinevalt netomuutuse meetodile tegevuse kuupäevi ja tulevikukuupäevasid uuendatakse ainult uute või muudetud nõuete puhul. See planeerimismeetod on saadaval ainult dünaamiliste plaanide jaoks.

## <a name="types-of-scheduling-methods"></a>Kavandamismeetodite tüübid

Iga plaani jaoks peate kiirkaardil **Üldine** lehel **Koondplaanid** (**Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**) valima tootmistellimuste jaoks kasutatava kavandamismeetodi. Saate plaanida tootmist operatsiooni ja töö tasandil.

### <a name="operations-scheduling"></a>Operatsioonide planeerimine

Operatsioonide plaanimine võimaldab anda tootmisprotsessi kohta üldise hinnangu aja jooksul. Operatsioonide plaanimine ei tükelda tootmisprotsessi operatsioone töödeks. Lisateavet operatsioonide plaanimise kohta vt teemast [Operatsioonide plaanimine](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Tööde plaanimine

Tööde planimine on üksikasjalikum planeerimismeetod, kus iga operatsioon on jagatud selle üksikuteks ülesanneteks või töödeks. Tööde plaanimine hõlmab mahutavuse teavet. Seda kasutatakse tavaliselt üksikute tööde plaanimiseks tööde juhtimise moodulis kohe või lühikese ajavahemiku jooksul. Lisateavet tööde plaanimise kohta vt teemast [Tööde plaanimine](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Ajapiirid päevades

Iga plaani puhul saate valida, kui kaugele tulevikku peab koondplaneerimine erinevad nõuded ja muud asjaolud arvutama. Periood on tuntud kui *ajapiir*. Koondplaneerimise parima jõudluse tagamiseks on soovitatav ärinõuete täitmiseks kohandada erinevaid ajapiire. Iga plaani jaoks leiate ajapiirid kiirkaardil **Ajapiirid päevades** lehel **Koondplaanid** (**Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**).

> [!NOTE]
> Ajapiirid näitavad, kui kaugele tulevikku on koonplaneerimine erinevad nõuded ja muud asjaolud arvutanud. Sellel lehel valitud ajapiirid tühistavad laovarude grupis määratletud ajapiirid. See tähendab, et ajapiiri suvandi väärtuseks jah seadmine ja päevade määratlemine alistab laovarude grupis määratletud ajapiiri. Kui see on määratud valikule Ei, on ajapiir määratletud laovarude grupis. Lõpuks kui te ei soovi suvandit kasutada (näiteks te ei soovi tegevuse sõnumeid kasutada), seadke see valikule **Jah** ning seejärel määrake ajapiir **0** (null) päevale.

### <a name="coverage"></a>Laovarud

Laovarude ajapiir tähistab planeerimisperioodi või kui kaugele tuleks nõudlus kaasata. Teisisõnu näitab see teie plaaniperioodi.

Seades suvandi **Laovarud** valikule **Jah**, saate tühistada laovarude ajapiiri, mis oli koondplaneerimise ajal üksuse jaoks määratletud. Sellisel juhul sisestage päevade arv, mille jooksul peaks koondplaanimise arvestus vajadused katma. Laovarude ajapiir arvutatakse praegusest kuupäevast edasi. Alati töödeldakse praegusest kuupäevast varasemad vajadused.

> [!NOTE]
> Koondplaneerimise parima jõudluse tagamiseks on soovitatav kohandada plaaniperioodi laovarude ajapiiri.

### <a name="freeze"></a>Külmuta

Külmutuse ajapiir tähistab perioodi, mil uue koondplaneerimise käitamisel olemasolevaid plaanitud tellimusi ei muudeta. Plaanitud tellimused külmutatakse ja uusi plaanitud tellimusi ei soovitata.

Seades suvandi **Külmuta** valikule **Jah**, saate tühistada külmutamise ajapiiri, mis oli koondplaneerimise ajal üksuse jaoks määratletud. Sellisel juhul sisestage päevade arv, mille jooksul planeerimistegevus peaks olema külmutatud. Pidage meeles, et selle perioodi jooksul uusi plaanitud tellimusi ei looda ja olemasolevaid ei saa muuta.

### <a name="firming"></a>Kinnitamine

Kinnitamise ajapiir näitab ajavahemikku, mil plaanitud tellimused teisendatakse automaatselt tootmis- ja ostutellimusteks. Seda protsessi nimetatakse ka *plaanitud tellimuste automaatseks kinnitamiseks*.

Seades suvandi **Kinnitamine** valikule **Jah**, saate tühistada kinnitamise ajapiiri, mis oli koondplaneerimise ajal üksuse jaoks määratletud. Sellisel juhul sisestage päevade arv, mille jooksul plaanitud ostu- ja tootmistellimused peaksid olema automaatselt kinnitatud. Kinnitamise ajapiir arvutatakse koondplaanimise kuupäevast edasi. Plaanitud ostutellimuse automaatne kinnitamine saab aset leida ainult siis, kui üksus on hankijaga seostatud.

### <a name="forecast-plan"></a>Eelarveplaan

Eelarveplaani ajapiir näitab, kui kaugele tulevikku loob koondplaneerimine plaanitud tellimusi prognoositud nõudlusega kaupadele.

Seades suvandi **Eelarveplaan** valikule **Jah**, saate tühistada eelarveplaani ajapiiri, mis oli koondplaneerimise ajal üksuse jaoks määratletud. Sellisel juhul sisestage päevade arv, mille jooksul peab eelarveplaani müügieelarve olema koondplaneerimisse kaasatud.

### <a name="capacity"></a>Mahutavus

Mahutavuse ajapiir näitab, kui kaugele tulevikku süsteem tellimuste kavandamisel ressursside maksimaalset mahutavust arvesse võtab. Teisisõnu kavandab plaan tootmistellimused, kasutades üksuste tootmisprotsessi, ja see arvestab tootmisprotsessi ressurssidea ja iga ressursi maksimaalset mahutavust.

Seades suvandi **Mahutavus** valikule **Jah**, saate tühistada mahutavuse ajapiiri, mis oli koondplaneerimise ajal üksuse jaoks määratletud. Sellisel juhul sisestage päevade arv, mille jooksul peaks plaanitud tootmistellimuste mahutavus olema plaanitud. Koondplaneerimine kasutab kauba aktiivset tootmisprotsessi ja planeerib vajaduse kuupäevast tagasi. Kui plaanitud tootmistellimuse vajaduse kuupäev langeb väljapoole võimsuse ajapiiri, määratakse täitmisaeg kauba tarnekuupäeva järgi. Mahutavuse ajapiir arvutatakse praegusest kuupäevast edasi.

### <a name="action-message"></a>Tegevussoovitus

Tegevussoovitused soovitavad muudatusi, mida saab olemasolevasse tarneahelasse teha, et aidata tarneplaani optimeerida. Näiteks võivad nad soovitada tellimusi ettepoole või tahapoole liigutada või tellimuste koguseid suurendada või vähendada.

Seades suvandi **Tegevussoovitus** valikule **Jah**, saate tühistada tegevussoovituse ajapiiri, mis oli koondplaneerimise ajal üksuse jaoks määratletud. Sellisel juhul sisestage päevade arv, mille jooksul koondplaneerimine peaks vajaduste kohta tegevussoovitusi looma. Tegevussoovituse ajapiir arvutatakse praegusest kuupäevast edasi.

Lisateavet tegevussoovituste kohta vt teemast [Tegevussoovitused](/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Tegevussoovituste arvutamine põhjustab koondplaneerimise töötamise aja pikenemise. Kui tegevussoovitusi ei analüüsita ja rakendata korrapäraselt (iga päev, nädal jne), kaaluge arvutuse väljalülitamist koondplaneerimise töötamise ajaks. Arvutuse väljalülitamiseks seadke lehel **Koondplaanid** suvandi **Tegevussoovitus** ajapiir väärtusele **0** (null) selle koondplaani jaoks, mida käitate. Veenduge ka, et suvand **Tegevussoovitus** oleks välja lülitatud kõikide laovarude gruppide jaoks.

### <a name="calculated-delays"></a>Arvutatud hilinemised

Saate määrata, kui kaugele tulevased võimalikud viivitused plaanitud tellimustes tuvastatakse ja esitatakse. Sellisel viisil saate kavandada võimalikke (hilinenud) tarnekuupäevi.

Kui plaanitud tellimust ei saa nõudekuupäevaks täita, planeeritakse see kande varaseima täitmise kuupäevaks, mis põhineb täitmisaegadel ning materjali ja võimsuse saadavusel.

### <a name="approved-requisitions-time-fence"></a>Kinnitatud taotluste ajapiir

Taotluse nõudluse plaanitud tellimuste loomiseks saate seadistada koondplaneerimise. Määrake suvand **Kaasa taotlused** valikule **Jah** kiirkaardil **Üldine** lehel **Koondplaanid**. Seejärel kui kinnitatud taotluse eesmärk on täiendamine, loob koondplaneerimine selle täitmiseks automaatselt vastava plaanitud tellimuse. Täiendamise meetod määratakse kindlaks tarnepoliitikaga, mis on seadistatud teie organisatsiooni kaupadele. Pärast täiendamise taotluse loomist ja kinnitamist pole kasutaja täiendavad tegevused vajalikud.

Määrates suvandi **Kinnitatud taotluste ajapiir** valikule **Jah** kiirkaardil **Ajapiirid päevades**, saate kinnitatud taotluste ajapiiri tühistada, mis on üksuse jaoks koondplaneerimise ajal määratud. Sellisel juhul sisestage päevade arv minevikus, mis peaksid olema koondplaneerimise kinnitatud taotlustesse kaasatud, mille eesmärk on täiendamine. Näiteks saate määrata, et ainult viimase 10 päeva jooksul loodud kinnitatud taotlustest pärit täitmata ja möödunud nõudlust arvestatakse ja kaasatakse plaanimisse.

### <a name="sequencing"></a>Järjestus

Järjestus võimaldab plaanitud tellimuste korraldamist, mis põhineb valmistoodetega seotud järjestuse atribuutidel. Seda kasutatakse sageli pakendamise tootmistellimuste ettevalmistamiseks. Näiteks saab seda kasutada kastide kindlas järjestuses pakkimiseks, mis põhineb värvil ja suurusel.

Määrates valiku **Järjestus** suvandile **Jah**, saate määrata, kui kaugele tulevikku peaksid operatsioonid ja tööd olema järjestatud. Pidage meeles, et mida pikem on ajapiir, seda kauem koondplaneerimine kestab.

### <a name="calculated-delays"></a>Arvutatud hilinemised

Viivituse suvandid aitavad tagada, et tellimustel on teostatavad plaanitud kuupäevad. Kiirkaardil **Arvutatud hilinemised** lehel **Koondplaanid** on saadaval järgmised operatsioonid.

- **EVeenduge, et kavandatud tellimused poleks loodud enne koondplaneerimise käivitamise kuupäeva** – Määrake see suvand valikule **Jah**, et aidata tagada, et tellimusi saab kavandada minevikku jäävatele kuupäevadele.
- **Arvutatud hilinemise lisamine vajaduse kuupäevale** (**Plaanitud ostutellimused** all) – Määrake see suvand valikule **Jah**, et lisada nõuetele arvutatud hilinemine.
- **Arvutatud hilinemise lisamine vajaduse kuupäevale** (**Plaanitud tootmistellimused** all) – Määrake see suvand valikule **Jah**, et lisada nõuetele arvutatud hilinemine.
- **Arvutatud hilinemise lisamine vajaduse kuupäevale** (**Plaanitud ülekanne** all) – Määrake see suvand valikule **Jah**, et lisada nõuetele arvutatud hilinemine.
- **Arvutatud hilinemise lisamine vajaduse kuupäevale** (**Plaanitud kanban** all) – Määrake see suvand valikule **Jah**, et lisada nõuetele arvutatud hilinemine.

Kui määrate nõuetele hilinemiste lisamiseks suvandi **Arvutatud hilinemise lisamine vajaduse kuupäevale** valikule **Jah**, võtab süsteem arvesse ressursside võimsuse ja loob teostatavad plaanitud tellimused. Plaanitud tellimuse kuupäevade ümberarvutamine suurendab koondplaneerimise kestust. Seega kui te ei pea hilinemisi kasutama, määrake suvand valikule **Ei**.

## <a name="positive-and-negative-days"></a>Positiivsed ja negatiivsed päevad

Positiivsed ja negatiivsed päevad mõjutavad, kuidas koondplaneerimine plaanitud tellimusi ja tegevusi soovitab. Positiivsed ja negatiivsed päevad määratakse üksuse kauba laovarude grupile. Saate määrata erinevad laovarude grupid ja määrata nende parameetrid lehel **Laovarude grupid** (**Koondplaneerimine \> Seadistus \> Laovarud \> Laovarude grupid**).

### <a name="positive-days"></a>Positiivsed päevad

Positiivsed päevad näitavad, kui kaugele tulevikku koondplaneerimine praguseid varusid või sissetulekuid tulevaste nõudluste täitmiseks arvesse võtab. Näiteks kui positiivsed päevad on seatud väärtusele **100**, saab praegust laovaru kasutada nõudluse täitmiseks järgmise 100 päeva jooksul. Kui on olemas tellimus praegusest kuupäevast 150 päeva pärast, loob koondplaneerimine selle nõudluse rahuldamiseks plaanitud tellimuse, kuigi kaubavarude laoseis võib tellimuse täita. Lühikese täitmisega kiiresti liikuva kauba puhul ei pruugi te soovida kasutada kaugel tulevikus olevat varude laoseisu. Selle kiiresti liikuva juhtumi puhul läheb praegune vaba kaubavaru kiiresti ära ja tulevikus saaks esitada tulevase nõudluse õigeaegseks täitmiseks rohkem tellimusi, mis ei oleks kauba lühikese täitmisaja tõttu võimalik.

Positiivsed päevad mõjutavad ka tegevussoovitusi. Näiteks võib süsteem soovitada, et suurendaksite plaanitud ostutellimust, et see sisaldaks nõudlust, mis on tuleviku positiivsete päevade arvu piires. Kui positiivsed päevad on seatud väärtusele **100** ja kui kaubale on nõudlus praegusest kuupäevast 30 päeva jooksul, loob süsteem nõudluse rahuldamiseks plaanitud tellimuse. Kui samale kaubale on nõudlus praegusest kuupäevast 90 päeva jooksul, soovitab süsteem, et suurendaksite tellimuse kogust praegusest kuupäevast 30 päeva jooksul, et tellimus kataks nõudluse ka 90 päeva pärast. Samas kui kaubale on nõudlus praegusest kuupäevast 150 päeva jooksul, süsteem juba plaanitud tellimuse kogust suurendada ei soovita. Selle asemel luuakse uus plaanitud tellimus.

Tavaliselt määratakse positiivsed päevad arvule, mis on kaupade kõige pikema täitmisaja ja laovarude ajapiiri vahel. Soovitame määrata regulaarselt hangitavad või toodetavad kaubad laovarude grupile, kus positiivsete päevade arv on võrdne kauba täitmisajaga.

### <a name="negative-days"></a>Negatiivsed päevad

Negatiivsed päevad näitavad, kui suure hilinemisega kauba sissetulekud on lubatud. Need tähistavad päevade arvu, mida olete valmis ootama, enne kui tellite negatiivse kaubavaru või ebapiisava kaubavaru korral uue täienduse. Negatiivsed päevad vastavad küsimusele, kas peaksime looma kauba uue ostutellimuse või peaksime kasutama olemasolevat ostu, kuigi teame, et kaup jääb hiljaks?

Näiteks on teil müügitellimus kaubale 15 päeva pärast alates tänasest kuupäevast. Samuti on teil samale kaubale ostutellimus. See ostutellimus võetakse vastu 20 päeva pärast alates tänasest kuupäevast. Kas soovite, et süsteem looks selle müügitellimuse jaoks ostutellimuse või soovite kasutada olemasolevat tellimust, kuigi te ei saa müügitellimust õigeaegselt täita? Kui negatiivsed päevad on seatud vähemale kui **5**, mis näitab, et kaup võib hilineda maksimaalselt viis päeva, loob süsteem müügitellimuse rahuldamiseks uue plaanitud ostutellimuse. Kui negatiivsed päevad on määratud väärtusele suurem kui **5**, kasutab süsteem kauba jaoks olemasolevat tellimust.

Negatiivsed päevad mõjutavad ka koondplaneerimise jõudlust. Kui negatiivsed päevad on seatud kõrgele numbrile, luuakse palju tegevussoovitusi.

Soovitame seada negatiivsed päevad arvule, mis on väiksem kui kauba täitmisaeg.

### <a name="dynamic-negative-days"></a>Dünaamilised negatiivsed päevad

Dünaamilised negatiivsed päevad võtavad arvesse kauba täitmisaja ja teie määratud negatiivsed päevad. Süsteem loob uue plaanitud ostutellimuse, mis põhineb negatiivsete päevade ajapiiril, mis arvutatakse järgmist valemit kasutades.

Täitmisaeg + negatiivsed päevad + tänane kuupäev – vajaduse kuupäev

Süsteem kasutab ainult selle ajapiiri piires olevaid plaanitud hanketellimusi ja loob uue plaanitud tellimuse sellest väljaspool. Dünaamilise negatiivsete päevade eeliseks on see, et need hõlmavad individuaalse toote täitmisaega, et taaskasutada olemasolevaid tellimusi ja vältida uute plaanitud tellimuste loomist, mis lõpevad täitmisaja põhjustatud hilinemise tõttu hilisema päevaga. 

Lisateavet vt teemast [Negatiivsed päevad ja dünaamilised negatiivsed päevad](/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]