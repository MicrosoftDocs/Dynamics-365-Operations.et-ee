---
title: Eelarve plaanimise integreerimine muude moodulitega
description: Eelarveplaane saab luua mitmest erinevast ressursist. Perioodilise protsessi põhielemendid on kõikide ressursside puhul samad.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c497f6ff4588ab1fd334f98ea822006006f16e4e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971224"
---
# <a name="budget-planning-integration-with-other-modules"></a>Eelarve plaanimise integreerimine muude moodulitega

[!include [banner](../includes/banner.md)]

 Eelarveplaane saab luua mitmest erinevast ressursist. Perioodilise protsessi põhielemendid on kõikide ressursside puhul samad. 



<a name="periodic-processes-for-generating-budget-plans"></a>Perioodilised protsessid eelarveplaanide loomiseks
----------------------------------------------

Eelarveplaane saab luua järgmistest ressurssidest.

-   Pearaamatu kanded
-   Põhivarad
-   Prognoositavad ametikohad
-   Projekti eelarved
-   Tarneprognoosid
-   Nõudluse prognoosid
-   Eelarve registrikirjed
-   Muud eelarveplaanid

Perioodilise protsessi põhielemendid on kõikide protsesside puhul samad. Vahekaardid võimaldavad teil määratleda andmeallika, sihtatribuudid (eelarveplaan) ja suvandid protsessi taustal pakktöötlusena käitamiseks. Selle artikli järgmistes jaotistes kirjeldatakse kaupu, mis ei pruugi iga protsessi puhul nähtavad olla.

### <a name="actions"></a>Tegevused

Iga loomisprotsessi puhul on saadaval kolm toimingut.

-   **Uue eelarveplaani loomine** loob uue plaani, millel on atribuudid, mis on valitud jaotises **Sihtkoht**. Need atribuudid ei pea olema kordumatud. Seega võib kahel plaanil olla sama nimi ja muud väärtused.
-   **Olemasoleva eelarveplaani stsenaariumi asendamine** kustutab kõik andmed valitud eelarveplaani stsenaariumi sihteelarveplaanis ja loob uued read, mis kasutavad valitud lähteandmeid.
-   **Olemasoleva eelarveplaani stsenaariumi värskendamine ja uute andmete lisamine** värskendab olemasolevaid ridu sihtplaanis, mis vastavad allika ridadele, ja lisab uute andmete jaoks ka uusi ridu. Vastavus põhineb pearaamatukontol, kuupäeval, eelarveklassil ja mitmetel muudel väljadel. Näiteks kui loote eelarveplaane prognositavatest ametikohtadest, on amtikoha kood oluline väli. Kõik read, millel on ametikoha kood, mis vastab allika ametikoha koodile, asendatakse uute ridadega allikast.

### <a name="source"></a>Allikas

Kõigi protsesside puhul võimaldab vahekaart **Allikas** andmeid filtreerida nupu **Filter** abil. Vaikimisi lisatakse iga protsessi puhul filtrile kindlad väljad. Näiteks protsessi **Eelarveplaani loomine pearaamatust** puhul on saadaval kategooriad **Pearaamatukonto** ja **Põhikonto** ning need kuvatakse loomise lehel. Kõik filtrile lisatud väljad lisatakse ka lehele koos mis tahes lisatava kriteeriumiga.

### <a name="target"></a>Siht

Suvand **Ajalooline** vahekaardil **Sihtkoht** võimaldab teil kasutada lähteandmete kuupäevi eelarveplaani jõustumiskuupäevana. Tavaliselt peab jõustumiskuupäev jääma plaani eelarvetsüklisse. Kui määrate suvandi **Ajalooline** väärtuseks **Jah**, kasutatakse allika kuupäeva (isegi aastat), nii et saate kasutada võrdluse alusena mineviku andmeid. Te ei saa muuta eelarveplaani ajaloolisi andmeid ja plaanile määratakse kinnitatud töövoo olek. Kuid saate oleku lähtestada, kui plaani muud stsenaariumid vajavad muutmist.

Lehe ülaosas olev väli **Kogusumma liitmine** määrab samuti kasutatud kuupäeva. See väli võtab summad kokku ja määrab valikuliselt rahandusaasta või rahandusperioodi esimesele päevale jõustusmikuupäeva. 

Paljud väljad vahekaardil <strong>Sihtkoht</strong> muutuvad redigeeritavaks või kirjutuskaitstuks olenevalt valitud tegevusest. Kui lähete uue eelarveplaani loomiselt üle olemasoleva plaani värskendamisele, muutub väli **Eelarveplaani nimi** kättesaamatuks ja olemasoleva plaani valimisega seotud väljad muutuvad kättesaadavaks. Vahekaartidel **Sihtkoht** ja **Allikas** on väli **Pearaamat** alati kättesaamatu, sest väärtuse määrab valitud eelarve plaanimise protsess. 

Väli **Eelarveklass** võimaldab teil määrata eelarveplaani ridu kas kulu- või tulukannetena. Tavaliselt on tulukanded krediidid pearaamatukontole ja seetõttu on need talletatud negatiivsete summadena. Tavaliselt ilmuvad need kanded ka eelarveplaani negatiivsete summadena. Kuid lisades eelarveklassi plaani paigutuse väljana saate lubada tulu kuvamise positiivsete summadena.

### <a name="generation-rules"></a>Loomise reeglid

Kolm välja pakuvad täiendavaid funktsioone: **Tegur**, **Miinimum** ja **Ümardamise** **reegel**. 

Väljal **Tegur** olev väärtus korrutatakse lähtesummaga, et määrata summa eelarveplaanis. Saate eelarveplaani ridu luues korrigeerida. Näiteks saate 3-protsendilise kasvu puhul sisestada **1,03**. Tegur peab olema positiivne arv. 

Väli **Miinimum** võimaldab teil määrata eelarveplaani rea loomise lävisumma. Kui lähtesumma on sellest arvust väiksem, siis eelarveplaani rida ei looda. Väärtus **0,00** lubab kõiki summasid, kuid ei piira ridu positiivsete summadega. Ükski väärtus ei piira ridu positiivsete summadega. Negatiivsed summad kaasatakse alati ja need esindavad tavaliselt kreeditkirjeid.)

Väli **Ümardamisreegel** võimaldab teil määrata loodud eelarveplaani ridade täpsuse. Saate ümardada summasid kõige lähemale valuutale 1,00, 10,00, 100,00 jne.

## <a name="notes-for-specific-processes"></a>Märkused kindlate protsesside kohta
### <a name="generate-budget-plan-from-general-ledger"></a>Eelarveplaani loomine pearaamatust

Kui loote eelarveplaani pearaamatu andmetest, peate määrama välja **Kogusumma liitmine** väärtusele **Rahandusaasta**, kui suvand **Ajalooline** on seatud väärtusele **Ei**. Allikas olevad perioodid ja kuupäevad ei pruugi sihtkohas olevate kuupäevade perioodiga ühilduda. Kuna protsessil ei ole usaldusväärset viisi nende väärtuste vastendamiseks, peate piirama protsessi esimesele aastale. 

Sihtkohas on välja **Eelarveklass** väärtuseks seatud kas **Kulu** või **Tulu**. Seda sätet kasutatakse loodud ridadele atribuutide **Eelarve tüüp** valimiseks, kui rea põhikonto tüüp ei ole **Tulu** ega **Kulu**.

### <a name="generate-budget-plan-from-fixed-assets"></a>Eelarveplaani loomine põhivaradest

Ptotsessil **Eelarveplaani loomine põhivaradest** ei ole liitmise võimalust perioodi või päeva järgi. Samuti ei ole võimalust seadistada plaani ajaloolisena. Saate seda perioodilist protsessi kasutada selleks, et kaasata kavandatud kanded eelarve plaanimise põhivarasse.

### <a name="generate-budget-plan-from-forecast-positions"></a>Eelarveplaani loomine prognoositavatest ametikohtadest

Protsess **Eelarveplaani loomine prognoositavatest ametikohtadest** määrab eelarveplaani reale allikaks oleva prognoositava ametikoha. Saate ametikohta vaadata, lisades prognoositava ametikoha eelarveplaani paigutuse reana või kasutades päringut **Eelarveplaani read**. Kui te ei soovi eelarveplaani ridadele prognoositavat ametikohta määrata, määrake suvandi **Kaasa ametikoht eelarveplaani real** väärtuseks **Ei**.

Pearaamatukonto ja ametikoht liidavad eelarveplaani read. Saate aga ametikoha koodi välja jätta, nii et ridu liidab ainult pearaamatukonto. Määrake vahekaardil **Sihtkoht** suvandi **Kaasa ametikoht eelarveplaani real** väärtuseks **Ei**.

Väljal **Eelarveplaani täistööaja vaste stsenaarium** saate valida stsenaariumi, mis kaasab täistööajaga töötajate (FTE-d) arvu eelarveplaani. See väli on piiratud koguse tüüpi stsenaariumidega, mis on kaasatud sihteelarveplaani paigutusse. Kui valite täistööaja vaste stsenaariumi, peate valima ka täistööaja vaste põhikonto. Seda kontot kasutatakse koguse eelarveplaani ridade loomiseks. 

Allikas valitud eelarve plaanimise protsess ja eelarveplaani stsenaarium et määravad sihtstsenaariumi eelarve planeerimise protsessi ja stsenaariumi. Kuna need atribuudid on määratud prognoositavatele ametikohtadele, peavad need eelarveplaaniga ühilduma. Seega ei saa neid atribuute sihtkohas muuta.

### <a name="generate-budget-plan-from-project-forecasts"></a>Loo eelarveplaan projekti prognoosidest

Protsessil **Loo eelarveplaan projekti prognoosidest**, nagu ka protsessil **Eelarveplaani loomine prognoositavatest ametikohtadest**, on võimalus kaasata projekti kogused (tunnid, kulud ja kaubad) koguse stsenaariumis. Kahel protsessil on keelarveplaani paigutuses ka veergudele sarnased filtrid. 

Vahekaardil **Allikas** määravad kolm suvandit jaotises **Kaasa väljavõte**, millised eelarveplaani read luuakse. Need suvandid on samad suvanditega, mis on saadaval, kui loote eelarve registrikanded otse projekti prognoosidest. Määrake suvandi **Tulu ja kulu** väärtuseks **Jah**, et luua read kulude ja tulude jaoks. Määrake suvandi **WIP** väärtuseks **Jah**, et luua lõpetamata toodangu kirjeid. Määrake suvandi **Palga eraldamine** väärtuseks **Jah**, et luua read palga tasakaalustuskontodele tunnikannete kohta. 

Välja **Eelarveklass** ei ole, sest eelarveklassi (**Kulu** või **Tulu**) määrab allikas. 

Saate kasutada projekti eelarveid allikana, valides eelarvemudeli, mis sisaldab projekti eelarvesummasid. Pidage meeles, et projekti eelarved loovad projekti prognoosi kirjeid, kui need kinnitatakse.

Eelarveplaani ridadele ainult kulude või tulude valimiseks kasutage filtrit, et valida suvand <strong>Eelarve värskendused: summa tüüp = kulu</strong>. Ainult ühte tüüpi prognoosi valimiseks kasutage filtrit, et valida suvand <strong>Eelarve värskendused: kande tüüp = *xxx</strong>*. 

Eelarveplaani stsenaariumi loomiseks saab kasutada ainult ühte eelarvemudelit. Kui käitate protsessi ühe eelarvemudeli jaoks ja teete siis värskenduse ning püüate määrata muu mudeli, alistatakse esimene mudel, kui kehtivad sama projekt ja pearaamatukonto. Eelarveplaani stsenaariumi loomiseks mitmest eelarvemudelist looge erinevatesse eelarveplaani stsenaariumidesse ja kasutage eraldamisvõimalusi, et lisada need koos teise stsenaariumisse. 

Protsess **Loo eelarveplaan projekti prognoosidest** määrab eelarveplaani reale ka lähteprojekti.

### <a name="generate-budget-plan-from-supply-forecast"></a>Eelarveplaani loomine tarneprognoosist

Lähtefiltri suvandid protsessis **Eelarveplaani loomine tarneprognoosist** mudeldati pärast suvandeid funktsioonis **Kanna ostueelarve pearaamatusse** protsessi ja funktsiooni vaheliste sarnasuste tõttu.

### <a name="generate-budget-plan-from-demand-forecast"></a>Eelarveplaani loomine nõudluse prognoosist

Protsessi **Eelarveplaani loomine nõudluse prognoosist** jaoks saate määrata suvandi **Müügitellimus** väärtuseks **Jah**, et luua eelarveplaani kasumiread, määrata suvandi **Tarbimine** väärtuseks **Jah**, et luua kuluread, või määrata mõlema suvandi väärtuseks **Jah**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Eelarveplaani loomine eelarve registrikirjetest

Protsessi **Eelarveplaani loomine eelarve registrikirjetest** puhul peab allikas määrama ühe alammudeli, ühe eelarvekoodi ja ühe kande numbri. Teisisõnu saate luua eelarveplaani ridu korraga ainult ühele eelarveregistri kandele. Saate kasutada täiendavaid kandeid samas eelarveplaanis, käitades protsessi ühe korra iga allika kirje puhul.

### <a name="generate-budget-plan-from-budget-plan"></a>Eelarveplaani loomine eelarveplaani põhjal

Protsessi **Eelarveplaani loomine eelarveplaani põhjal** puhul võimaldavad täiendavad suvandid vahekaardil **Sihtkoht** määrata uusi finantsdimensioone. Kui valitud on finantsdimensioon, kasutatakse seda väärtust kõikide eelarveplaani ridade puhul. Seega saate kasutada ühte eelarveplaani muude eelarveplaanide alusena, kuid saate määrata uutele eelarveplaanidele ka näiteks erineva osakonna või kulukeskuse.

## <a name="looking-back-from-the-budget-plan"></a>Eelarveplaanist varasema otsimine
### <a name="budget-plans-by-dimension-set-inquiry"></a>Eelarveplaanide päring dimensioonikogumi järgi

Päring **Eelarveplaanid dimensioonikogumi järgi** hõlmab mitut suvandit, mis võimaldavad teil päringu käivitada aitamaks tuvastada eelarveplaani andmete allikat. 

Valige rida ja klõpsake nuppu **Eelarveplaani read**, et käivitada päring **Eelarveplaani read**. Tulemused filtreeritakse valitud rea dimensiooni väärtuste kohta. Seejärel saate rakendada täiendavaid parameetreid. 

Nende päringute käivitamiseks kasutage nuppe **Tarneprognoos** ja **Nõudluse prognoos**. Mõlemal juhul otsib päring prognoosi ridu, mis võisid luua eelarveplaani ridu. 

Täiendavad saadaolevad aruanded hõlmavad aruannet **Prognoositavad ametikohad eelarveplaani järgi**. See aruanne on eriti kasulik, kui soovite määrata, kas amtikoht on eelarveplaanidesse õigesti eraldatud.



