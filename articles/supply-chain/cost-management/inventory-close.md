---
title: Lao sulgemine
description: Väljaminekukannete sissetulekukannetega tasakaalustamise protsessi osana saate valida, et pearaamatu värskendamine kajastaks tehtud korrigeerimisi.
author: AndersGirke
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d25db42351529fafbc68313c992f873918cd5e8638d9dc9417cb04f1ba5698f3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711925"
---
# <a name="inventory-close"></a>Lao sulgemine

[!include [banner](../includes/banner.md)]

Väljaminekukannete sissetulekukannetega tasakaalustamise protsessi osana saate valida, et pearaamatu värskendamine kajastaks tehtud korrigeerimisi.

Süsteemi lao sulgemise protsess tasakaalustab väljaminekukanded sissetulekukannetega varude hinnamääramise meetodi alusel, mis on valitud kauba mudeligrupis. Tasakaalustusprotsessi osana saate määrata, et pearaamatut peaks uuendama nii, et see kajastaks tehtud korrigeerimisi. Kuid lao sulgemise või ümberarvutamise toimumiseni sisestatakse väljaminekukanded arvutatud keskmise jooksva omahinnaga. 

Pärast lao sulgemist ei ole enam võimalik sisestada määratud lao sulgemise kuupäevast varasemasse perioodi, kui te ei võta tagasi lõpetatud lao sulgemise protsessi. Näiteks kui lao sulgemine toimub perioodi kohta, mis lõpeb 31. jaanuaril, ei saa sisestada kandeid, mille kuupäev on varasem kui 31. jaanuar. 

Laos olevad kaubad määratakse ühte kahest varude tüübist: kaup või teenus. Lao sulgemine sooritab samad funktsioonid mõlema tüübi puhul. Kuid teenuseüksuste puhul tasakaalustab lao sulgemine siiski väljastused sissetulekutega. 

Lao sulgemisprotsessi käitamise sagedus on ettevõtete lõikes erinev. Kuid kande maht peaks aitama määrata, kui sageli otsustate lao sulgemist kasutada. Üldiselt käitab enamik ettevõtteid lao sulgemist kuu lõpu sulgemise vastavusse viimise protseduuride osana.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Varude ümberarvutamine ja pearaamat
Kui kuu või mõne muu laoperioodi jooksul on vaja korrigeerida ladu ja pearaamatut, saate lao sulgemise asemel käitada lao ümberarvutust. Lao ümberarvutamine korrigeerib, kuid ei tasakaalusta lao kanded. 

Varude ümberarvutamise ajal korrigeeritakse vaba kaubavaru, korrigeeritakse laokandeid ning käitatakse varude ümberarvutusi ja lao sulgemisi. Need ülesanded mõjutavad mis tahes pearaamatukontosid, mis on seotud algsete laokannetega. 

**Näide** 

Kui loote ostutellimuse müügitellimusest, värskendatakse algse müügitellimuse jaoks kasutatavaid pearaamatukontosid. Isegi kui sellele kaubale määratud kaubagrupi pearaamatukontod on müügitellimuse sisestamisest saadik muutunud ja lao ümberarvutus on loonud korrigeerimissumma, sisestatakse korrigeerimissumma ikkagi algsesse pearaamatukontosse. Korrigeeritud summat ei sisestata kaubale määratud uutesse pearaamatukontodesse. 

Pärast värskenduse lõpuleviimist saate üle vaadata pearaamatukande, mis on sisestatud mõne sellise ülesande tagajärjel.

1.  Valige lehe **Sulgemine ja korrigeerimine** vahekaardil **Ülevaade** ülevaadatav värskendus.
2.  Klõpsake nuppu **Üksikasjad** ja valige seejärel suvand **Kanne**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Lao sulgemisprotsessi mõjud pearaamatule
Mitmed tööülesanded, mida saate teha lehel **Sulgemine ja korrigeerimine**, toovad kaasa pearaamatu värskenduse. Näiteks värskendatakse pearaamatut, kui teete vaba kaubavaru korrigeerimisi, laokannete korrigeerimisi, käitate laokannete ümberarvutamist ja lao sulgemist. 

Nende tööülesannete tõttu värskendatud pearaamatukontod on sellised, mis on seotud algsete laokannetega. Kui näiteks müügitellimus tasakaalustatakse ostutellimusega, siis korrigeeritakse algse müügitellimuse jaoks kasutatud pearaamatukontosid. See toimub ka juhul, kui sellele kaubale määratud kaubagrupi pearaamatukontod on pärast müügitellimuse sisestamist muutunud. Kui varude sulgemine on loonud tasakaalustussumma, sisestatakse tasakaalustussumma ikkagi algsetele pearaamatukontodele, mitte kaubale määratud uutele pearaamatukontodele. Pearaamatut võidakse värskendada ka varude sulgemise tagasivõtmisel. 

> [!NOTE] 
> - Varud tuleb sulgeda kuu lõpus toimuva protsessi käigus kõikide laomudelite korral, v.a libisev keskmine.  Teid hoiatatakse, kui proovite finantsperioodi sulgeda, sooritamata esmalt lao sulgemist perioodi lõpukuupäeval.
> - Enne sulgemisprotseduuri käitamist saate vaadata loendit kaupadest, mida ei saa värskenduse käigus tasakaalustada.
> - Soovitame andmetöötlusressursside ühtlasemaks jaotamiseks käitada lao sulgemist väljaspool tipptunni kellaaegu.

## <a name="the-inventory-close-log"></a> Lao sulgemise logi
Pärast lao sulgemise protsessi lõpetamist võidakse sõnumikeskusesse saabunud sõnumis teatada, et ühiku omahind võib olla vale, kuna kannet ei saanud täielikult tasakaalustada. 

Enne selle teate kuvamist teatab süsteem kauba numbri ja mõjutatud kande. See teade teavitab teid, et lao sulgemise tõttu ei värskendatud selleks kandeks kasutatud omahinda. See tead ilmub, kui väljastuse tüüpi kannet ei saa tasakaalustada. 

Lao sulgemise protsessi ajal kontrollib süsteem iga finantsdimensiooni puhul, kas väljaminekuid on kuni määratud sulgemiskuupäevani leiduvatest sissetulekutest rohkem. Selline mittevastavus võib ilmneda finantsiliselt lõplikult sisestamata ostutellimuselt tehtud laokande tõttu, kui hankijalt pole arve veel saabunud või kui mõni kõrgemal tasemel tootmisse suunatud koosluse komponent on finantsiliselt sisestamata. (Alltootmise omahinda ei arvutata.) Sellisel juhul ei korrigeeri järgnev sulgemine kõigi väljaminekute omahinda, kuna selleks pole piisavalt sissetuleku teavet. 

Iga sulgemisprotseduuri käitamise puhul näitab süsteem, kas hoiatusi sisaldav logi talletatakse ja kas seda saab vaadata. 

Kui saate sõnumis palju hoiatusi, soovitame teha järgmist.

-   Uuendage sissetulekud finantsiliselt.
-   Nihutage sulgemiskuupäeva varasemaks.
-   Hinnake äritegevuse protseduurid ümber.

Mõnes olukorras ei pruugi teil olla võimalik hoiatuste suhtes midagi ette võtta. Näiteks ei saa sulgemiskuupäeva muuta märkimise kasutamisel, kui märgitud ostutellimuse finantskuupäev on pärast sulgemiskuupäeva.

## <a name="reversing-a-completed-inventory-close"></a>Lõpetatud lao sulgemise tühistamine
Vahel võib olla vaja lõpule viidud varude sulgemine ümber pöörata, et taastada tasakaalustuste korrigeerimiseelne olek. Kui pöörate lõpule viidud varude sulgemise ümber, avatakse varud uuesti, et lubada sellesse sisestamist varude sulgemise perioodil. Seotud muudatusi saab teha ka pearaamatus. Pärast korrigeerimist võite taas sulgeda varude perioodi, millega töötate. 

> [!NOTE] 
> Uuesti saab avada ainult viimasena suletud varude perioodi. Varasema lao sulgemise tühistamiseks tuleb tühistada ühekaupa kõik järgnevad lao sulgemised, alustades kõige viimasest sulgemisest.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]