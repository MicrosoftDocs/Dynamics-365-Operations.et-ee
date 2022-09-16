---
title: Ennetavad kvaliteedivärskendused
description: See artikkel annab teavet kvaliteediuuenduste ennetava tarne kohta.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 985800aad3711a1b28613f0f82585b4d592cdf58
ms.sourcegitcommit: de989037d83393bea013cd58c061159765305b4f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473601"
---
# <a name="proactive-quality-updates"></a>Ennetavad kvaliteedivärskendused

[!include[banner](../includes/banner.md)]

Viimase mitme aasta jooksul on Microsoft teinud pidevat edenemist selle osas, mida me nimetame üheks [versiooniks](../../dev-itpro/lifecycle-services/oneversion-overview.md). Ühe versiooni eelne on lihtne: mida lähemal on võimalik saada kõigi klientideni sama tarkvaraversiooni puhul, seda kõrgem on kvaliteet, mida suudame tarnida. Probleemid leiab ja lahendatakse üks kord ning need lahendused võetakse rohkematest klientidest kiiremini.

Selle eelduse kinnitavad tulemused: väiksem juhtumite arv kõigis meie toodetes. Kui kliendid ei ole samas versioonis, oleme järjepidev, et neid mõjutavad probleemid, mille jaoks lahendus on juba saadaval. Oleme juba teinud suurt edu Dynamics 365 Finance’i, Dynamics 365 Dynamics 365 Project Operations Dynamics 365 Commerce tarneahelaga ja tänu viimastele tehnilistele ettemaksetele on nüüd võimalik teha järgmine samm. Järgmine teave annab välja selle, mida me kavatseme teha, mida oleme juba etapi kehtestab ning kuidas ja millal me uusi võimalusi katkestuseta tutvustame.

## <a name="focus-on-quality-updates"></a>Fookus kvaliteediuuendustele

Pakume praegu 7 [teenuseuuendust](public-preview-releases.md) aastas. Näiteks versioon 10.0.29 on teenuse värskendus. Kuni viimaseni uuendati aasta kohta kaheksat uuendust. Kuid me kukutasime ühe värskenduse vastuseks kliendi tagasisidele, mis soovis vältida muudatusi kalendriaasta lõpus.

Teenuse uuenduste sagedust ei muuda me. Selle asemel keskendub meie järgmine samm edasi ühe versiooni reisil *kvaliteediuuendustele*. Kvaliteediuuendused on kiirparanduste kumulatiivsed järgud. Need ei sisalda uusi funktsioone. Mis tahes aja jooksul on kogu meie klientide ühendus erinevusi kolme või nelja kõige viimase teenuse uuenduse vahel. Iga teenusevärskenduse puhul saab siiski kasutada grupi sees tosinat erinevat kvaliteedivärskenduse versiooni, sõltuvalt juurutatud inimeste kuupäevadest. Järgmise sammuna levitame ennetavalt kvaliteediuuendusi. Me juba kasutame seda mudelit meie - Dataverse põhiste rakenduste jaoks ning oleme pidanud nägema eeldatavaid kvaliteedi parandamise ja vähenenud tugijuhtumite tulemusi.

Defektide vähenemine võib muidugi vähendada või täielikult eemaldada kvaliteediuuenduste vajaduse. Meil on lennus mitu algatused kvaliteediuuendust nõudva defekti vähendamiseks. Isegi siis, kui kvaliteedi uuendamisel vähendatakse töökoormust, parandab järjepidevus kliendibaasi kaudu tugitavust, tagab klientide parendusi kiiremini ja vähendab klientide sagedust lahenduste juba olemas olemise probleemi korral.

## <a name="making-proactive-distribution-possible"></a>Ennetava jaotuse võimalikuks tegemine

Mitmed ettemaksed on juba juurutatud, mis võimaldavad kvaliteediuuenduste ennetavat tarnimist:

- **Nullväärtusega downtime-uuendamine** – sagedaste keskkondade tõukamiseks on oluline vähendada mõju keskkonna saadavusele, et säilitada Dynamics 365 teenustaseme lepingud (SLAs). Algselt juurutati nullväärtusega ajaline uuendamine, et aidata parandada kuu operatsioonisüsteemi paikamist klastri ülemineku abil värskendatud pildi aktiveerimiseks minimaalse katkestusega. Uuenduste rakendamise mehhanism on täiustatud nii, et see oleks veel vähem katkestav ning kataks nii operatsioonisüsteemi paikamise kui ka kvaliteediuuenduse juurutamise.

    Interaktiivsete kasutajate puhul võib aktiivne seanss katkeda ja uuesti käivitatakse uuesti uuendatud keskkond. Prioriteedipõhise partiiplaneerimise [juurutamisel](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), mis on nüüd saadaval liitumise alusel, taastab pakkplaneerimine ja töötlemine ning jätkab tööd kohe pärast uuendamist. Prioriteetne pakkplaneerimine toimub klientide jaoks enne, kui nad hakkavad osalema oma tootmiskeskkondades kvaliteediuuenduste ennetavas jaotuses.

- **tumetunnid** – tume tunnid on määratud igale Azure’i piirkonnale ja lähedalasuvad null ajaperioodi värskendused tekivad tumetunnise perioodi jooksul.

## <a name="the-proactive-update-process"></a>Ennetav uuendusprotsess

Ennetava kvaliteedivärskenduste juurutamine järgib seifijuurutusprotsessi (SDP). SDP spetsiifilised reeglid muutuvad, kuid kvaliteediuuendused juurutatakse algselt kaustakeskkonda. Protsess algab keskkondadega, mis nõustuvad varajase juurutamisega. Kui edukalt juurutatud bokside protsent suureneb, algab juurutamine tootmiskeskkondades. Taas kord algab protsess keskkondadega, mis valivad varajase juurutamise. Kuulamissüsteem jälgib süsteemi telemeetriat ja livesite’i juhtumeid ning peatab konkreetse versiooni väljapööramise, kui tuvastati regresssioon. Kliendid saavad siiski enne enne enne juurutamist kvaliteedivärskendusi tõmbada, kui nad seda soovivad.

Praegused väljalaskehalduse andmed näitavad, et kvaliteediuuendustele tutvustatakse vähem kui 3 protsenti regressioone. Suurenenud fookuse eemaldamisel regressiooni ja täiustatud SDP-ni on regressioone potentsiaalne mõju potentsiaalselt väiksem kui kvaliteedikasumid, mis on klientide jaoks paranduste kiiremaks juurutamise teel saavutatav.

## <a name="process-changes"></a>Protsessi muudatused

Protsessimuudatuste kogum rakendatakse enne enne kvaliteedivärskenduse juurutamist.

- **Skeem**: tööriistamine tagab, et kvaliteedivärskenduse järgud sisaldavad ainult skeemi muudatusi, mida saab rakendada, kui teenus on võrgus. See lähenemine aitab säilitada võimalust rakendada uuendust nullväärtusega downtime’iga.
- **Aktiivsete muudatuste** muutumine on juba täiendav protsessisamm, et kinnitada muudatused kvaliteedivärskendusse kaasamise jaoks. Regressioone võimalike vähendamiseks suurendatakse lisasammide edasist haldust. Kvaliteediuuenduste puhul pole katkestatud muudatused lubatud ja suurenenud muudatus aitab tagada, et vastame sellele sihile.
- **Nähtavus** – me saadame teatised meili ja elutsükli teenuste (LCS) kaudu eesseisva ennetava kvaliteediuuenduse jaoks. Lisaks on tugimeeskonnad ja juhtumi vihjed nähtavusega seal, kus kvaliteediuuendused on ennetavalt juurutatud.
- **Versiooni varuversioon** – lennuteed kasutatakse kõikide muutuste grupeerimiseks proaktiivses kvaliteedivärskenduses. Kui tagasipöördumine on vajalik pärast ennetavat juurutamist, saab seda teha lennusüsteemi kaudu.
- **Windowsi sünkroonimise määramine** – vähem kui 20%-l klientidest on täna mitu ruutu ja ühe boksi juurutamiseks on versiooni vastendamise tootmisse juurutatud, et aidata teil tõrkeotsingut. Kui klient kasutab märkeruutu uuema versiooni testimiseks kui nende tootmises, saab see märkeruut kvaliteediuuendused uuemale versioonile.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Mis on kvaliteediuuenduste jaoks pöördumine?

Ennetava kvaliteediuuenduste jaotus sisendkausta keskkondades peaks eeldatavasti algama septembri lõpus või septembril 2022 Azure’i avaliku pilve klientidele. Proovikeskkonnad hakkavad saama ka sel ajal ennetavat uuendamist. Septembris saadetakse kliendile teatis, mis teavitab neid eeldatavast keskkonnagraafikust. Ennetava värskendatud jaotusprotsessi erandid on lubatud ainult FDA-ga reguleeritud klientide puhul. Töötame endiselt selles, kuidas hallatakse reguleeritud keskkondi ja ande- ja valitsuse pilve kliente.

Järgmise kuue kuu jooksul suurendame järk-järgult märkeruutukeskkondade protsenti, mis saavad ennetavad uuendused, kuni kõik määratud keskkonnad on kaasatud ja edenemine tootmiskeskkondade uuendamisel. Kogu perioodi jooksul jälgime, kindlustamaks, et juurutusprotsess on tõrgeteta ja et me saada kätte meie mitteladustavate lastide sihtmärgi.

Kuna kliendid saavad regulaarselt väiksemaid töökoormusi, eeldame, et praegused täitjad muutuvad lihtsamaks. Korrigeerime juurutamise uuendamise sagedust vastavalt võimele protsessi käivitada katkestuseta. See protsess töötab juba tõhusalt meie platvormi ja Dataverse rakenduste jaoks ning pakub teenuse kvaliteedi eeldatavat parendust. Soovitame teha sama sammu edasi finants- ja operatsioonide rakenduste puhul.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Millal käivitatakse kvaliteediuuendused tootmiskeskkondades?
Praegu on kvaliteediuuendused suunatud ainult boksidele. Tootmiskeskkondade uuendused algavad pärast 2022. aasta novembrit.

## <a name="what-is-the-schedule-for-sandbox-quality-updates"></a>Mis on selle kausta kvaliteediuuenduste graafik?
Lisateavet iga piirkonna tumetundide kohta vt "Mis [on proaktiivsete kvaliteediuuenduste graafik?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-is-the-schedule-for-proactive-quality-updates)

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Kuidas käsitsetakse tume tunde klientide puhul, mil on üks finantside ja toimingute rakenduste eksemplar, kuid mis on aktiivsed mitmes ajavööndis? 
Väljaspool tumedaid tunde, kus finantside ja toimingute rakenduste eksemplar on olemas, ei ole spetsiaalseid ajakavasid, [kuna plaanime minimaalselt katkestava ja nZDT-ga kvaliteediuuendusi välja võtta](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Kuidas tagab Microsoft nende uuenduste kvaliteedi?
Microsoft püüab hoida vabastusvõimaluste tõhusust, et tagada väikeste lastide tarnimine, et hoida kinnitamiskulu madal. Iga kvaliteedivärskenduse parandus läbib erakordse ja turvalise juurutusprotsessi, mis aitab parandada kvaliteeti ja usaldusväärsust, vähendades nii klientide mõju. Juurutamine toimub esmalt koostekausta keskkondades etappidena, millele järgneb tootmine. Etapiviisiline juurutamine võimaldab korrektset jälgimist, et määratleda, kas edasine juurutamine on turvaline. Peatame väljamineku, kui tuvastatakse probleemid iga juurutatud klientide grupiga, ja tagame, et igal sammul on piisavalt aega probleemide lahendamiseks. Iga eesse tulevase kvaliteediuuenduse jaoks kasutame ajakava nähtavust avaliku dokumentatsiooni ja e-kirjade uuenduse kaudu, et kliendid saaksid seda planeerida.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Kas kliendid saavad kvaliteedi uuendamist edasi lükata, ümber planeerida või peatada?
Ei. Kvaliteediuuenduste peamine eesmärk on tagada, et turvalisus, privaatsus, usaldusväärsust, kättesaadavust ja jõudlust täiustatakse pidevalt meie klientide puhul. Värskendamise, turvalisuse, kättesaadavuse ja usaldusväärsuse edasilükkamine või selle edasilükkamine on riskiks.

## <a name="how-can-one-know-the-set-of-changes-that-went-into-a-quality-update-payload"></a>Kuidas saab teada muudatuste komplekti, mis läks kvaliteedivärskenduse töökoormusse?
Kvaliteedivärskenduse lehel **liikumine** võimaldab LCS-i **keskkonna üksikasjade lehel vaadata kõiki kvaliteedivärskenduse teabebaasi artikleid**. 

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Mis on protsess, kui pärast kvaliteedi uuendamist leitakse kriitiline probleem?
Kriitiline väljaminek või regressioon on üks või mitu sündmust, mis tavaliselt põhjustavad mitmele kliendile alandatud kogemuse ühe või mitme meie teenusega. Need probleemid võivad põhjustada plaanimata töötunde, sealhulgas kättesaamatust, jõudluse käiku ja sekkumise teenusehaldust. Kui selliste regressioonide tõttu on kliendil lai mõju, peatame kvaliteedivärskenduse väljastamise, kuni saame ühendust pidada ja probleemi lahendada. Tavaliselt on järgmisel kvaliteedivärskendustel vajalik parandus, et jätkata väljapööramist.

Kui mõjutatakse ühte kliendi keskkonda, pöörduge pileti avamiseks Microsofti toe poole. Põhjenduse põhjal peatame kvaliteedivärskenduse väljapööramise selles projektis kõigisse muudesse keskkondades, kuni probleem lahendatakse.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Kas kliendid saavad LCS-i kiirparanduse värskendusi siiski käsitsi rakendada?
Jah. Et tagada pidev paarsus selle abil, kuidas kiirparandused töötavad, saab kiirparanduse värskendusi siiski rakendada LCS-i kliendi keskkondadele. Siiski on oluline märkida, et osana kvaliteedivärskendusest juurutatud kiirparandused läbivad standardse SDP enne värskenduse juurutamist. See vähendab kõrgemast kvaliteedist põhjustatud regressioonide riski. Soovitame teil valida kvaliteedivärskendus kiirparandused käsitsi kohaldada suuremale usaldusväärsusele.

## <a name="can-customers-self-install-a-quality-update-build-by-themselves-ahead-of-the-schedule"></a>Kas kliendid saavad kvaliteetvärskenduse ise installida graafikust ette?
Jah. Saate installida kvaliteedivärskenduse ennetavalt. Microsoft jätab värskenduse vahele, kui keskkonna praegune järguversioon on kõnealuse kvaliteedivärskendusega võrdne või sellest kõrgem.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Kui keskkonnas on eesseisev planeeritud igakuine teenuse värskendus nädala jooksul, kas see saab siiski kvaliteediuuendusi?
- Kvaliteediuuendusi ei rakendata, kui eelseisva teenuse värskendus plaanitakse nädala jooksul alates kvaliteediuuenduse plaanist.
- Kui tolle keskkonnal on sama või kõrgem versiooni versioon kui eelseisval kvaliteedivärskendustel, jäetakse see vahele.
- Kui tootmiskeskkonnal on sama või kõrgem versiooni versioon kui eelseisval kvaliteedivärskendustel, jäetakse see vahele.
- Kui eboksil on kvaliteedi uuendamise või tootmise käsitsi uuendamise tõttu sama või kõrgem koosteversioon, saab tootmine ikkagi igakuiste teenusvärskenduste planeeritud versiooni. Kui te ei soovi, et plaanitud tootmiskeskkond uuendaks teenuse värskendusversiooni, saate teenuse värskenduse LCS-i kaudu peatada. 
- Soovitame kasutada uusimat kvaliteedivärskenduse koostet, et katsetada eesseinud teenusevärskenduse muutusi parema stabiilsuse ja tulemuste saavutamiseks.

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kas keskkonna saab tagasi tuua oma eelnevasse olekusse, kui kvaliteedivärskenduse rakendamist on küsimusi?
Pärast kvaliteedi värskenduse rakendamist ei ole mingites olukordades tagasipööramist. Probleemide lahendamiseks on saadaval ainult paiga edasised suvandid.

## <a name="what-about-fda-regulation-and-gpx"></a>Kuidas on FDA-määrusega jaGPX-iga?
FDA kinnitamist ja korrastamist vajav klientide plaan on endiselt läbirnitud. Ootab varsti rohkem uuendusi selles ruumis. Kõik need kliendid on praegu kvaliteediuuendustest vabastatud.

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Millised teenusevärskenduste versioonid on nende kvaliteediuuenduste puhul toetatud?
Kliente, kes on madalamates versioonides kui N-2 ei saa kvaliteedivärskendusi. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Finantside ja toimingute rakenduste juurutused jaemüügikomponentidega nõuavad tavaliselt lisaks MPOS-i uuesti juurutamiseks täiendavat tööd. Kuidas need kvaliteediuuendused Mõjutavad RetailSDK-d? 
Kuna kiirparanduste enda olemus ei muuda kvaliteedivärskenduste töökoormust, ei eelda me praegu jaemüügi komponentidega seotud lisamõju.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che-"></a>Kas see mõjub pilve majutatud keskkondadele (CHE)? ? 
Ei.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Kas on olemas integratsiooniprobleeme Microsoft Dataverse? 
Ei.

