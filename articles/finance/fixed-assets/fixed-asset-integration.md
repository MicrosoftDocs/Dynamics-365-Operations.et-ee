---
title: Põhivarade integreerimine
description: Põhivarasid saab integreerida moodulitega Pearaamat, Varude haldus, Müügi- ja Ostureskontro. Samuti on teil võimalik seadistada moodulit Põhivarad, et see oleks integreeritud ostutellimustega.
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fb1348a3a3c47e5fd7df46d9ce4af3725d8896b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177333"
---
# <a name="fixed-assets-integration"></a>Põhivarade integreerimine

[!include [banner](../includes/banner.md)]

Põhivarasid saab integreerida moodulitega Pearaamat, Varude haldus, Müügi- ja Ostureskontro. Samuti on teil võimalik seadistada moodulit Põhivarad, et see oleks integreeritud ostutellimustega.

<a name="general-ledger"></a>Pearaamat
--------------

Pearaamatus summeeritakse kõikide põhivarade väärtus tavaliselt mitmes finantsaruandluseks vajalikus põhikontos. Lehel **Põhivarad** saate siiski luua paljusid põhivarakirjeid. Need kirjed võivad hõlmata sellist teavet nagu soetusmaksumus, kulum ja väärtus. Igal põhivarakande sisestamisel värskendatakse vastavad põhikontod. Põhivarade põhikontod kajastavad alati põhivarade värskendatud väärtust.

Lehel **Põhivara sisestusreeglid** saate määratleda põhikontod, kuhu sisestatakse põhivara raamatu kanded. Samuti saate määratleda, mis tüüpi põhivarakandeid sisestatakse igale põhikontole. Sõltuvalt pearaamatus põhivaradele soovitavast üksikasjatasemest saate luua mitmeid põhivarade põhikontode kombinatsioone. Põhikontode aluseks võivad olla kandetüübid, raamatud ja muud põhikontod.

## <a name="inventory-management"></a>Varud
Põhivarade laotöölehel saate sisestada juriidilise isiku enda jaoks toodetud või loodud põhivarade soetuse. Seejärel saate laokaubad kas soetusena või soetuse osana põhivaradesse edastada. 

Saate varasid soetada ka ostutellimusi kasutades. Kui ostutellimused sisaldavad laokaupu, mis on määratud põhivarana, määrab märkeruudu **Luba vara soetamine ostmiselt** säte lehel **Põhivarade parameetrid**, kas soetus sisestatakse põhivara puhul arve sisestamisel. Üks osturida loob ühe põhivara, olenemata kogusest. Põhivarade soetamise mõju varudele sõltub juriidilise isiku seadistusest. 

Kui laokaubast saab põhivara soetus (laotöölehe, ostutellimuse või soetussoovituse kaudu), luuakse põhivara raamatu soetuskanne. Raamatu soetuses sisalduva tuletatud raamatu puhul luuakse ka tuletatud raamatu soetuskanne. 

Mooduli Varude haldus lehel **Sisestamine** seadistatud sisestusreeglid juhivad varude vähenemist soetuse sisestamisel. Te ei vähenda siiski varusid iga kord, kui sisestate põhivaradega seotud arveid. Mõnel juhul võib põhivara osta sisemiseks kasutamiseks. Näiteks on arvuti, mis ostetakse müügiosakonnale. ostutellimustega töötades saate kasutada kaupu, mis on seadistatud nii edasimüügiks kui ka sisemiseks kasutamiseks. 

Kui kasutate konkreetseid sissetuleku- ja väljaminekukontosid põhivarade kaubagruppide puhul, saate nii sisemiste ostude kui ka edasimüügi varude puhul kasutada sama laokaupa. 

Sisemiseks kasutamiseks mõeldud põhivarad seadistatakse nii, et nende konto tüüp on **Põhivara sissetulek**. Seda konto tüüpi kasutatakse põhivara sissetuleku jälgimiseks. Hankija arve sisestamisel kasutage põhivara sissetulekukontot, kui mõni järgmistest tingimustest on täidetud.

-   Arverida sisaldab olemasolevat asutusesiseseks kasutamiseks mõeldud põhivara.
-   Ruut **Uus põhivara?** on sisestatud toote sissetuleku rea puhul märgitud.
-   Ruut **Loo uus põhivara** on hankija arve rea puhul märgitud.

See konto on tavaliselt kulukonto. Saate seadistada kontotüübi **Põhivara sissetulek** kas kaubagrupile või üksikkaubale, kasutades vahekaarti **Ostutellimus** lehel **Kaubagrupp** või **Sisestamine**.

Sarnasel moel saab sisemiseks kasutamiseks mõeldud põhivarasid seadistada nii, et nende konto tüüp on **Põhivara väljastus**. Seda konto tüüpi kasutatakse jälgimaks põhivara väljaminekut saajale. Vara soetamisel ostutellimuse kaudu tasakaalustab põhivara väljamineku konto põhivara deebetkontot. Vara soetamist saab sisestada, kui sisestate hankija arve või kui sisestate vara soetamise töölehel Põhivarad, kasutades võimaluse korral soetussoovitust. Saate seadistada kontotüübi **Põhivara väljastus** kas kaubagrupile või üksikkaubale, kasutades vahekaarti **Varud** lehel **Kaubagrupp** või **Kauba sisestamine**. 

Lõppkokkuvõttes määratakse sisestamiseks kasutatavad põhikontod pearaamatu integratsioonivalikutega, mis on määratud kauba mudeligrupi jaoks. Lisaks erinevad kasutatavad põhikontod sõltuvalt sellest, kas ostutellimuse reale on määratud vara. Kontod tuletatakse iga kaubagrupi sisestusreeglist. 
**Märkus.** Kui toote sissetulekute sisestamisel on olemas varude reserveering, ei saa te määrata põhivara ega luua realt põhivara. 

Põhivarakannete sisestamisel kasutatavate kontode valik sõltub kahest tegurist: kas varad on juriidilise isiku enda ostetud või toodetud, ning vara kandetüübist. 

Kandetüüp seob laokande Põhivaras sisestusreegliga. Kuna põhivaras olevad sisestusreeglid määratlevad värskendatavad kontod, on põhivara kandetüübi valimine kaudselt ka selle põhikonto valimine, kuhu kanne sisestatakse. Nii toodetud kui ka ostetud põhivarade puhul kasutatakse tavaliselt kandetüüpi **Soetus** või **Soetuse korrigeerimine**.

## <a name="accounts-receivable"></a>Müügireskontro
Põhivarade integreerimisel müügireskontroga kasutatakse sisestusreegleid, mis on põhivarades seadistatud. Sisestusreeglid aktiveeritakse, kui enne kliendiarve sisestamist on kliendiarve jaoks valitud põhivara, raamat ja põhivara kandetüüp. Kuna põhivarad ei kuulu moodulisse Varude haldus, peate põhivara müügil kasutama lehte **Vabas vormis arve**. 

Kui raamat hõlmab tuletatud kulumiraamatut, luuakse kliendiarve sisestamisel tuletatud raamatu kanne.

## <a name="accounts-payable"></a>Ostureskontro
Põhivarade soetamine toimub tavaliselt välistelt hankijatelt. Saate lehel **Põhivarade parameetrid** määrata, kas vara soetamine sisestatakse alati, kui sisestate hankija arveid, või kas vara soetamist saab sisestada ainult Põhivaradest. Kui lubate varasoetuse sisestamise moodulist Ostureskontro, värskendatakse põhivarakontod iga kord, kui sisestatakse hankija arve põhivara soetamise eest. 

Kui süsteem on seadistatud sisestama vara soetamist, kui arve on sisestatud, sisestatakse kanne vastavalt sisestusreeglitele, mis on seadistatud erinevate põhivara kandetüüpide põhivarades. Sisestamist juhitakse põhivara, raamatu ja põhivara kandetüübiga, mis valitakse lehel **Ostutellimus** enne hankija arve sisestamist. 

Kui raamat hõlmab tuletatud raamatut, luuakse hankija arve sisestamisel tuletatud raamatu kanne.

Iga tellimuserea integratsioon aktiveeritakse lehe **Ostutellimus** kiirkaardi **Rea üksikasjad** vahekaardil **Põhivarad**. Saate põhivara ostutellimuse hankijale saata. Põhivarasid ja põhikontosid värskendatakse ainult siis, kui sisestate hankija arve pärast põhivara saabumist. Kuna ostutellimused võivad sisaldada ainult laokaupu, sõltub põhivarade soetamise mõju varudele juriidilise isiku seadistusest.

## <a name="project-management-and-accounting"></a>Projektihaldus ja raamatupidamine
Saate seostada projekti varaga, mis on projektist mõjutatud. Samuti saate seostada iga faasi, ülesannet või alamprojekti erineva varaga. Üht vara saab seostada iga projektikirjega. Saate luua seose, kui sisestate põhivara koodi lehel **Projektid** väljale **Põhivara kood**. Projekti tüüp peab olema **Sisemine projekt** või **Kuluprojekt**. 

Saate vaadata projektidega seostatud varade üksikasju ka lehel **Projektid**. Põhivarakirje kuvamiseks klõpsake kiirkaardil **Seadistus** vara linki, et avada leht **Põhivarad**. Seejärel klõpsake valikuid **Projektid** &gt; **Kõik projektid**, et kuvada põhivaraga seostatud projektid. 

Tavaliselt seostate põhivarad projektidega, kui projektid on seotud tööga, hooldusega või põhivara remondiga. Kui projekt on lõpule viidud, ei looda automaatselt vara üleshindluse korrigeerimist. Seega peate üleshindluse korrigeerimise käsitsi looma, kui see on nõutav. 

Seose kustutamiseks projekti ja vara vahel tühjendage lehel **Projektid** väli **Põhivara kood**. 

Saate määrata ka põhivara, mida loote või toodate osana hinnanguprojektist. Hinnanguprojekti lõpus saate automaatselt sisestada varasoetamise kande.

Lisateavet leiate jaotisest [Varade soetamine hankega](acquire-assets-procurement.md)



