---
title: Tellimuse lubamine
description: See artikkel käsitleb tellimuse lubamist. Tellimuse lubamine aitab teil usaldusväärselt tarnekuupäevi klientidele lubada ja annab teile paindlikkuse, et saaksite neid kuupäevi täita.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228262"
---
# <a name="order-promising"></a>Tellimuse lubamine

[!include [banner](../includes/banner.md)]

See artikkel käsitleb tellimuse lubamist. Tellimuse lubamine aitab teil usaldusväärselt tarnekuupäevi klientidele lubada ja annab teile paindlikkuse, et saaksite neid kuupäevi täita.

Tellimuse lubamine arvutab varaseimad lähetamise ja vastuvõtmise kuupäevad ning põhineb tarnekuupäeva kontrollimeetodil ja transpordipäevadel. Saate valida järgmiste tarnekuupäevade kontrollimeetodite hulgast:

- **Müügi täitmisaeg** – müügi täitmisaeg on müügitellimuse koostamise ja kaupade lähetamise vaheline aeg. Tarnekuupäeva arvutamine põhineb vaikepäevade arvul ja ei arvesta lao kättesaadavust, teadaolevat nõudlust või plaanitud tarnet.
- **ATP (saadaval lubamiseks)** – ATP on kaubakogus, mis on saadaval ja mida saab kliendile konkreetsel kuupäeval lubada. ATP arvutamine sisaldab kehtestamata laosaldot, täitmisaegu, plaanitud sissetulekuid ja väljaminekuid.
- **ATP + väljamineku** brutokasum – lähetuskuupäev võrdub ATP kuupäeva ja kauba väljaminekumarginaaliga. Väljamineku ohutusvaru on aeg, mis on vajalik kaupade saatmiseks ettevalmistamiseks.
- **CTP (lubamiseks võimeline)**– saadavus arvutatakse koosnevusarvutuse abil. Kui kasutate planeerimise optimeerimist, *pole CTP* tarnekuupäeva kontrollmeetod lubatud ja kui see on valitud, põhjustab see arvutuse käitamisel vea. CTP-i seadistamis- ja kasutamise kohta leiate lisateavet müügitellimuse [tarnekuupäevade arvutamisest CTP abil](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).
- **CTP plaanimise optimeerimise** jaoks – kasutage CTP arvutust, mille pakub planeerimise optimeerimine. See valik ei oma mingit mõju, kui kasutate integreeritud koondplaneerimise mootorit. CTP-i seadistamis- ja kasutamise kohta leiate lisateavet müügitellimuse [tarnekuupäevade arvutamisest CTP abil](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

> [!NOTE]
> Müügitellimuse värskendamisel uuendatakse tellimuse lubamise teavet ainult juhul, kui kehtivat tellimuse lubamise kuupäeva ei saa täita, nagu on näidatud järgmistes näidetes.
>
> - **Näide 1**: praegune tellimuse lubamise kuupäev on 20. juuli, kuid suurenenud koguse tõttu ei saa te tarnida enne 25. juulit. Kuna praegust kuupäeva ei saa enam täita, käivitatakse tellimuse lubamine.
> - **Näide 2**: praeguse tellimuse lubaduse kuupäev on 20. juuli, kuid vähenenud koguse tõttu on nüüd võimalik tarnida 15. juulil. Kuna aga praegust kuupäeva saab veel täita, siis tellimuse lubaduse ei käivitata ja 20. juuli jääb tellimuse lubaduse kuupäevaks.

## <a name="atp-calculations"></a>ATP arvutused

ATP kogus arvutatakse meetodiga "kumulatiivne ATP tulevikku vaatamise abil". Selle ATP arvutamise meetodi peamiseks eeliseks on see, et selle abil saab käsitleda juhtumeid, kus väljaminekute summa sissetulekute hulgas on suurem kui viimane sisstulek (näiteks kui nõude täitmiseks tuleb kasutada varasema sissetuleku kogust). Arvutusmeetod "kumulatiivne ATP tulevikku vaatamise abil" hõlmab kõiki väljaminekuid seni, kuni kumulatiivne saadav kogus ületab väljastamiseks kumulatiivse koguse. Seetõttu hindab see ATP arvutusmeetod, kas mõne varasema perioodi kogust saab hilisemas perioodis kasutada.

ATP kogus on esimese perioodi kehtestamata laosaldo. Tavaliselt arvutatakse see iga perioodi kohta, milles sissetulekut plaanitakse. Programm arvutab ATP perioodi päevades ja arvutab praeguse kuupäeva esimeseks ATP koguse kuupäevaks. Esimeses perioodis sisaldab ATP vaba kaubavaru, millest on lahutatud tähtajalised või tähtaja ületanud klienditellimused.

ATP arvutamiseks kasutatakse järgmist valemit.

ATP = eelmise perioodi ATP + praeguse perioodi sissetulekud – praeguse perioodi väljaminekud – netoväljamineku kogus iga tulevase perioodi jaoks kuni periood, millal kõikide tulevaste perioodide sissetulekute summa (kuni tulevaste perioodideni ja need kaasa arvatud) on suurem kui väljaminekute summa (kuni tulevaste perioodideni ja need kaasa arvatud).

Pange tähele, et ATP arvutamine ei sisalda teavet aegumiskuupäeva ega ATP ajapiirist välja jääva aja kohta, mida süsteem eeldab, kui lubada saab mis tahes kogust.

Kui rohkem väljaminekuid ja sissetulekuid ei ole, on järgmiste kuupäevade ATP kogus sama, mis viimane kalkuleeritud ATP.

Kui kõiki kaubale kasutatud dimensioonide ei ole ATP kontrolliks esitatud, võidakse need siiski määrata väljaminekutele ja sissetulekutele. Sel juhul peavad ATP arvutamisel olema väljaminekud ja sissetulekud olemasoleva dimensiooniga liidetud, et vähendada ATP arvutuses kasutatavaid väljaminekute ja sissetulekute ridasid.

Kuvatav ATP kogus on alati suurem kui 0 (null) või sellega võrdne. Kui arvutus tagastab negatiivse ATP koguse (nt kui eelnevalt lubatud kogus ületab saadaoleva koguse), määratakse koguseks automaatselt 0.

### <a name="example"></a>Näide

Väli **ATP tagasiulatuv nõudluse ajapiir** juhib, kui kaugele hilinenud nõudluse tellimuste või lao väljaminekute otsimisel ajas tagasi minnakse. Väli **ATP tagasiulatuv tarne ajapiir** juhib, kui kaugele hilinenud tarnetellimuste või lao sissetulekute otsimisel ajas tagasi minnakse. Näiteks kui tellimusi, mis on hilinenud ainult seitse päeva, peaks ATP arvutamisel arvestama, tuleb mõlemale väljale määrata väärtus **7**.

Väljad **ATP hilinenud nõudluse viivituse aeg** ja **ATP hilinenud tarne viivituse aeg** juhivad, millal hilinenud nõudlust või tarnet ATP arvutamisel arvestatakse. Näiteks kui hilinenud tarnet ja nõudlust tuleks arvestada ATP arvutamisel ülehomme, tuleb mõlemale väljale määrata väärtus **2**. Väärtus **2** tähendab, et kauba kogust hilinenud ostutellimusel, mida ATP arvutamisel arvestada tuleks, nähakse saadaval olevana kaks päeva pärast praegust kuupäeva.

Järgmises näites sisestatakse **7** väljadele **ATP tagasiulatuv nõudluse ajapiir** ja **ATP tagasiulatuv tarne ajapiir** ja **1** sisestatakse väljadele **ATP hilinenud nõudluse viivituse aeg** ja **ATP hilinenud tarne viivituse aeg**.

Ostutellimust 200 tooteühikule, mis oleks pidanud jõudma kohale kolm päeva tagasi, pole veel vastu võetud. Seetõttu pole müügitellimuse rida sama toote 75 ühikule, mis oleks tulnud eile teele panna, veel teele pandud.

Klient helistab ja soovib tellida 150 ühikut sama toodet. Kui kontrollite toote saadavust, siis leiate, et teine ostutellimus 100 tooteühikule tarnitakse 10 päeva hiljem.

Loote tootele müügitellimuse rea ja sisestate koguseks **150**.

Kuna tarnekuupäeva kontrollmeetod on ATP, arvutatakse ATP andmed, et leida varaseim võimalik lähetuskuupäev. Sätete põhjal arvestatakse hilinenud ostutellimust ja müügitellimust ning saadud ATP kogus praeguse kuupäeva kohta on 0. Homme, kui hilinenud ostutellimus peaks kohale jõudma, arvutatakse ATP koguseks rohkem kui 0 (praegusel juhul arvutatakse selleks 125). 10 päeva pärast, kui oodatakse täiendava 100 ühikuga ostutellimuse saabumist, saab aga ATP koguseks rohkem kui 150.

Seetõttu määratakse tarnekuupäevaks ATP arvutuse alusel 10 päeva alates tänasest. Seetõttu saate kliendile öelda, et soovitud koguse saab tarnida 10 päeva pärast.

## <a name="ctp-calculations"></a>CTP arvutused

CTP-funktsioon võimaldab teil anda klientidele realistlikke kuupäevi, millal te saate lubada kindlaid kaupu. Iga müügirea kohta saate sisestada kuupäeva, mis arvestab olemasolevat vaba kaubavaru, tootmisvõimsust ja transpordiaja.

CTP laiendab ATP funktsioone, võttes arvesse võimsuse teavet. Kuigi ATP võtab arvesse ainult materjali saadavuse ja eeldab piiramatuid võimsuse ressursse, võtab CTP arvesse nii materjalide kui võimsuse kättesaadavust. Seega on sellel realistlikum pilt sellest, kas nõudlust saab antud aja jooksul rahuldada.

CTP töötab veidi teistmoodi, sõltuvalt kasutatavast koondplaneerimise mootorist (planeerimise optimeerimine või integreeritud mootor). Plaanimise optimeerimise CTP toetab praegu ainult alamkogumit CTP stsenaariumitest, mida integreeritud mootor toetab.

Üksikasjalikku teavet ctp kasutamise kohta iga mootori puhul [vt müügitellimuse tarnekuupäevade arvutamine CTP abil](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
