---
title: Tootmisprotsessi ülevaade
description: See teema annab ülevaate tootmisprotsessidest. Selles kirjeldatakse mitmesuguseid tootmistellimuste, partiitellimuste ja kanbanide etappe, alates tellimuse loomisest kuni rahandusperioodi sulgemiseni.
author: johanhoffmann
ms.date: 09/13/2019
ms.topic: overview
ms.search.form: JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, OpResLifecycleManagementWorkspace, ProdParmCostEstimation, ProdParmRelease, ProdSchedule, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19832"
- intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c9eac4d3f984b6fe511d7cc5ebab67e6c24c722
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983209"
---
# <a name="production-process-overview"></a>Tootmisprotsessi ülevaade

[!include [banner](../includes/banner.md)]

See teema annab ülevaate tootmisprotsessidest. Selles kirjeldatakse mitmesuguseid tootmistellimuste, partiitellimuste ja kanbanide etappe, alates tellimuse loomisest kuni rahandusperioodi sulgemiseni.

Toodete tootmine, protsess, mida nimetatakse ka tootmise töötsükliks, järgib kindlaid etappe, mis on nõutavad kauba tootmiseks. Töötsükkel algab tootmistellimuse, partiitellimuse või kanbani loomisega. See lõpeb lõpetatud kaubaga, mis on valmis kas kliendi või tootmise teise faasi jaoks. Igal töötsükli sammul vajatakse protsessi lõpule viimiseks erinevat laadi teavet. Iga etapi lõpulejõudmisel kuvatakse tootmistellimuses, partii tellimuses või kanbanis tootmise oleku muudatus. Erinevat tüüpi tooted nõuavad erinevaid tootmisprotsesse.

Moodul **Tootmise juhtimine** on seotud teiste moodulitega, nagu **Tooteteabe haldus**, **Varude haldus**, **Pearaamat**, **Laohaldus**, **Projekti raamatupidamine** ja **Organisatsiooni administreerimine**. Selline integreeritus toetab teabevoogu, mida on vaja valmis kauba tootmiseks.

Tavaliselt mõjutavad tootmisprotsessi kindla tootmisprotsessi jaoks valitud kuluarvestuse ja varude hindamise meetodid. Supply Chain Management toetab nii tegeliku kulu (esimesena sisse, esimesena välja \[FIFO\], viimasena sisse, esimesena välja \[LIFO\], liikuv keskmine ja perioodiline kaalutud keskmine) kui ka standardkulu meetodit. Lean manufacturingit rakendatakse omahinna tagasiarvestuse põhimõtte alusel.

Kulumõõtmismeetodite valik määratleb ka tootmisprotsessi materjalide ja ressursside tarbimise aruandluse nõuded. Tavaliselt nõuavad tegeliku kulu meetodid täpset aruandlust töö tasemel, samas kui perioodilise kuluarvestuse meetodid võimaldavad esitada materjalide ja ressursside tarbimise kohta üldisema aruande.

## <a name="mixed-mode-manufacturing"></a>Tootmise segarežiim

Erinevad toodete ja tootmise topoloogiad nõuavad erinevate tellimustüüpide rakendamist. Supply Chain Managementi saab rakendada erinevaid tellimusetüüpe segarežiimis. Teisisõnu võib kogu tootmisprotsessi käigus kuni valmistooteni esineda kõiki tellimusetüüpe.

- **Tootmistellimus** – see on klassikaline tellimus kindla toote või tootevariandi antud koguse tootmiseks kindlal kuupäeval. Tootmistellimused põhinevate kooslustel ja protsessidel.
- **Partii tellimus** – seda tüüpi tellimust kasutatakse protsessi harude ja diskreetsete protsesside puhul, kus tootmise teisendus põhineb valemil või kus kaastooted ja kõrvalsaadused võivad olla lõpptooted kas põhitootele lisaks või selle asemel. Partii tellimused kasutavad **valemi** tüüpi kooslusi ja protsesse.
- **Kanban** – kanbane kasutatakse märguandmiseks korduvatest lean manufacturingi protsessidest, mis põhinevad tootmisvoogudel, kanban-reeglitel ja kooslustel.
- **Projekt** – tootmisprojekti ühendab tooted ja teenused antud graafiku ja eelarvega. Projekti tootmisosa saab edastada mis tahes muud tüüpi tellimuste kaudu.

## <a name="manufacturing-principles"></a>Tootmispõhimõtted

Kindlale tootele ja seotud turule kõige paremini sobiva tootmispõhimõtte valimiseks peate arvestama tootmise ja logistika nõudeid ning ka kliendi ootusi tarne täitmisaegade kohta.

- **Valmistamine lattu** – see on klassikaline tootmispõhimõte, kus tooted toodetakse lao jaoks, võttes aluseks prognoosi või lao minimaalse täitmise (viimane arvutatakse tavaliselt prognoosi või tarbimisajaloo põhjal).
- **Valmistamine tellimiseks** – standardtooted valmistatakse või lõpetatakse tellimiseks. Kuigi põhimõtte „Valmistamine lattu” alusel võib teha eeltootmist, käivitatakse väärtusahela kulukad etapid või variante loovad etapid müügitellimus või üleviimistellimus.
- **Konfigureerimine tellimiseks** – samamoodi kui põhimõtte „Valmistamine lattu” puhul, tehakse väärtusahela lõplikud operatsioonid tellimise jaoks. Tegelik toodetud tootevariant pole eelnevalt määratletud, kuid luuakse tellimuse sisestamise ajal müügitoote konfiguratsioonimudeli põhjal. Põhimõte „Konfigureerimine tellimiseks” nõuab antud tootmisliini jaoks teatud tasemel protsessi ühtlustamist.
- **Projekteeri tellimiseks**: tellimiseks projekteerimise protsessid määratleb tavaliselt projekt ja need algavad harilikult projekteerimisfaasiga. Projekteerimisfaasis tuleb tellimuse täitmiseks nõutavad tegelikud tooted kujundada ja kirjeldada. Seejärel saab toodete tootmiseks luua tootmistellimused, partiitellimused või kanbanid.

## <a name="overview-of-the-production-life-cycle"></a>Tootmise töötsükli ülevaade

Tootmistsükli järgmised etapid võivad esineda kõigi tellimusetüüpide või segarežiimis tootmise korral. Siiski ei esitata neist kõiki sõnaselge tellimuse olekuna.

1. **Loodud** – saate luua tootmistellimus, partiitellimuse või kanbani käsitsi või konfigureerida süsteemi neid looma erinevate nõudlusmärguannete põhjal. Koondplaneerimine loob tootmistellimused, partiitellimused või kanbanid, kinnitades planeeritud tellimused. Ülejäänud nõudlusmärguanded on müügitellimused või kinnistatud tarnemärguanded muudest tootmistellimustest või kanbanidest. Fikseeritud kogusega kanbanide puhul luuakse nõudlusmärguanded, kui kanbanid registreeritakse tühjana.
1. **Eeldatav** – saate arvutada eeldatava materjali- ja ressursitarbimise. Hinnang loob varude kanded toormaterjalide kohta, mille olek on **Tellimusel**. Kui tootmistellimused või partiitellimused on hinnatud, luuakse põhitoodete, kaastoodete ja kõrvalsaaduste kohta sissetulekud. Kui kooslus sisaldab ridu, mille tüüp on **Kinnistatud tarne**, luuakse materjalide või alltöövõtu operatsiooniteenuste jaoks ostutellimused ja seotakse tootmistellimuse või partiitellimusega. Kaubad või tellimused reserveeritakse tootmistellimuse reserveerimisstrateegia järgi ja valmistoodete hind arvutatakse parameetrisätete põhjal.
1. **Planeeritud** – saate tootmist planeerida operatsioonide, üksikute tööde või mõlema põhjal.

    - **Operatsioonide planeerimine** – see planeerimismeetod võimaldab üldist pikaajalist planeerimist. Selle meetodiga saate määrata tootmistellimuste käivitamise ja lõpetamise kuupäevad. Kui tootmistellimused on kinnitatud protsessi operatsioonidele, saate need määrata kulukeskuste gruppidesse.
    - **Töö planeerimine** – see planeerimismeetod võimaldab detailset planeerimist. Iga operatsioon jagatakse üksikuteks töödeks, millel on kindlad kuupäevad, kellaajad ja määratud operatsiooniressursid. Kui piiratud võimsus on ära kasutatud, määratakse tööd operatsiooniressurssidele saadavuse alusel. Plaani saate vaadata ja muuta Gantti diagrammis.
    - **Kanban-graafik** – kanban-tööd planeeritakse kanban-graafiku tahvlil või kanban-reeglite automaatse planeerimise konfiguratsiooni alusel automaatselt.

1. **Väljastatud** – saate väljastada tootmistellimuse või partiitellimuse, kui graafiku lõpeb ja materjal on komplekteerimiseks või ettevalmistamiseks saadaval. Materjali kättesaadavuse kontroll võimaldab tööde järelevaatajal hinnata materjali saadavust tootmistellimuste või partiitellimuste jaoks. Samuti saate printida tootmistellimuse dokumente, nagu komplekteerimislehed, protsessikaart ja protsessitöö. Kui tootmistellimus on vabastatud, muutub tellimuse olek ning näitab see näitab, et tootmine võib alata. Laohalduse kasutamisel väljastatakse tootmistellimuse või partiitellimuse väljastamisel tootmise koosluseread laohaldusse. Seejärel luuakse lao seadistuse järgi laovood ja laotöö.
1. **Ettevalmistatud**/**komplekteeritud** – kui kõik materjalid ja ressursid on koondatud tootmise asukohta, värskendatakse tootmise koosluseridade või kanban-ridade olek sättele **Komplekteeritud**. Kinnistatud tarnetellimused ja seotud laotöö viiakse lõpule tavaliselt selles etapis. Tootmise edenemise aruandluseks nõutavad kanban-kaardid või töökaardid tuleb määrata ja printida.
1. **Alustatud** – kui tootmistellimus, partiitellimus või kanban on käivitatud, saate esitada materjali- ja ressursitarbimise tellimuse kohta. Süsteemi saab konfigureerida sisestama automaatselt materjali- ja ressursitarbimise, mis eraldatakse tellimusele selle käivitamisel. Seda eraldamist nimetatakse eeljagamiseks, ettejagamiseks või automaatseks tarbimiseks. Saate materjale käsitsi tootmistellimustele või partiitellimustele eraldada, luues täiendavad komplekteerimislehe töölehed. Samuti saate tööjõu- ja muud protsessikulud tellimusele käsitsi eraldada. Kui kasutate operatsioonide planeerimist, saate kulude eraldamiseks luua protsessikaardi töölehe. Kui kasutate töö planeerimist, saate kulude eraldamiseks luua töökaardi töölehe. Tootmistellimused või partiitellimused saab käivitada partiidena nõutavas lõplikus koguses. Tootmistellimuse, partiitellimuse või kanbani raames saab loodud tööd käivitada ja neist aru anda eraldi töölehtede, tootmise käivitusterminali (MES-terminal) või kanban-tahvlite kaudu.
1. Tööde edenemisest/**lõpetamisest** teatamine – kasutage töö või ressursiga tootmise edenemisest teatamiseks MES-etrminali, tootmistöölehti, kanban-tahvleid või mobiilse skannimise võimalusi. Materjali- ja ressursitarbimine sisestatakse ning seotud kanbanide, tootmistellimuste ja partiitellimuste olek võidakse värskendada sättele **Vastu võetud** või **Lõpetatuna teatatud**. Olenevalt lao konfiguratsioonist võidakse luua lao paigutamistöö.
1. **Lõpetatuna kinnitatud** (toote sissetulek) – kui tootmistellimus või partiitellimus on lõpetatuna kinnitatud, värskendatakse lõpetatud valmiskaupade kogust varudes. See kogus sisaldab asjakohaste kaastoodete ja kõrvalsaaduste kogust. Kui kasutate poolelioleva töö (WIP) raamatupidamist, luuakse pearaamatu tööleht, et vähendada WIP-kontosid ja suurendada valmiskaupade varusid. Tootmistellimuse kulu arvutamisel sisestatakse tootmise tegelik kulu. Kui tootmisega seotud materjali- ja töökulud ei ole juba töölehe või eeljagamisega eraldatud, saab neid nüüd automaatselt tagantjärele eraldada. Tagantjärele eraldamine hõlmab laokandeprotsesside järel-mahaarvamist. Kui tootmistellimus on lõpule viidud, märkige ruut **Lõpeta töö**, et määrata ülejäänu olekuks **Lõpetatud**. Vastasel juhul jätke väli tühjaks, et võimaldada toodetavate lisakoguste kohta aruandeid luua.
1. **Kvaliteedi hindamine** – toote sissetulek võib käivitada kvaliteettellimuste loomise olenevalt testprotsesside konfiguratsioonist ja kindlate toodete kohta loodud kvaliteedireeglitest. Kuna kvaliteettellimus saab värskendada testitud toodete varude olekut või partii atribuute, on kvaliteedi hindamine paljudes valdkondades kohustuslik protsess.
1. **Pane kõrvale** ja **Läheta tellimiseks** – pärast toote sissetulekut ja kvaliteedi hindamist suunab paigutamistöö vastuvõetud tooted järgmisse tarbimiskohta, valmiskaupade lattu või saatmistsooni, kui kehtivad tellimiseks lähetamise nõuded.
1. **Lõpetatud** – enne tootmise lõpetamist arvutatakse toodetud koguse tegelikud kulud. Kõik hinnangulised materjali- töö ja üldkulud tühistatakse ja asendatakse tegeliku kuluga. Kui märgite kuluarvutuse käivitamisel ruudu **Lõpeta töö**, muutub tootmistellimuse olek sättele **Lõpetatud**. See olek takistab lisakulude sisestamist lõpule viidud tootmistellimusele.
1. **Perioodi sulgemine** – mõni kuluarvestuse põhimõte, näiteks perioodiline keskmine, omahinna tagasiarvestus, FIFO või LIFO, nõuavad varude või rahandusperioodi sulgemiseks perioodilisi tegevusi. Tavaliselt püüab süsteem esitada enne perioodide sulgemist aruande kogu materjali- ja ressursitarbimise ning ka varude ja praagi korrigeerimiste kohta. Seda aruandlust tehakse tavaliselt varude liikumise töölehtede või korrigeerimistöölehtede abil. Eesmärk on hinnata tootmisüksuste majanduslikku toimivust perioodi kohta. Mõnel juhul, kui kasutatakse pikaajalisi, üle finantsiliste aruandeperioodide ulatuvaid tootmistellimusi, kasutatakse tootmise edenemisest ja perioodi lõpu seisuga ressursitarbimisest teatamiseks tootmistöölehti.

## <a name="additional-resources"></a>Lisaressursid

- [Tootmise tagasiside](production-feedback.md)
- [Toote konfiguratsioonimudelite ülevaade](../pim/product-configuration-models.md)
- [Lean manufacturingi ülevaade](lean-manufacturing-overview.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
