---
title: "Põhipalgaplaanide loomine"
description: "Põhipalk on töötaja regulaarne brutopalk või tasu. Selles artiklis kirjeldatakse komponente, mis peavad olema seadistatud, enne kui saate luua põhipalga plaani ja töötajaid registreerida."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: bbf08a9620dbc8ad928fe40a3ae5e9b2a2fcb373
ms.lasthandoff: 03/31/2017


---

# <a name="create-fixed-compensation-plans"></a>Põhipalgaplaanide loomine

Põhipalk on töötaja regulaarne brutopalk või tasu. See teema kirjeldab komponente, mida tuleb seadistada enne kindlaksmääratud hüvitiste plaan luua ja registreeruda töötajad.

Põhipalga summad saab töötajatele arvutada tegurite põhjal nagu jõudlus, regioon ja eelarve suurenemine. Microsoft Dynamics 365 toiminguteks toetab samm, klassi ja bänd hüvitise liigid.

## <a name="fixed-compensation-components"></a>Põhipalga osad
### <a name="compensation-levels"></a>Palgatasemed

Kasutage **hüvitise** tuleb hüvitiste erinevaid töid, tagamiseks töötajatele, kes hoida nende tööde eest korraliku. Kohta ning **hüvitise** lehe, saate seadistada hüvitise taset, mis on iga samm, klassi ja bänd kava. Kasutage nuppe **Üles** ja **Alla** tasemete õigesse järjekorda paigutamiseks nende tüübi alusel. Töö palgatasemete seadistamisega aitate tagada, et kõigile töötajatele, kes sellel ametikohal töötavad, makstakse ühe taseme järgi.

### <a name="reference-points"></a>Viitepunktid

**Viitepunktid** on ruudustiku veerud, mis määratlevad iga taseme palgavahemikud. Palgatase on ruudustiku rida. Tüüpilise tegevuskava, mille klassi tüüp on vähemalt, on keskmine ja maksimaalne. Loote tugikeskused ning **viide punkti seadistuse** lehel.

### <a name="compensation-grids"></a>Tasuruudustikud

Pärast tasemete ja viitepunktide seadistamist saab neid kombineerida, moodustades **tasuruudustiku**. Lehel **Tasuruudustikud** saate määratleda ruudustiku teabe. Näiteks saate määrata, mille jaoks ruudustik on mõeldud, millist tüüpi plaaniga seda kasutatakse ja millised viitepunktid või veerud on ruudustikus vajalikud. Kui olete selle teabe sisestamise lõpetanud, klõpsake nuppu **Tasustruktuur** ruudustikku tasemete ja summade lisamiseks. 

**Näpunäide.** Kasutage tasustruktuuri puhul funktsiooni **Hulgimuutmine** algsummade määramiseks ja siis suurendage protsentide või summade kaupa tasemete või viitepunktide lõikes.

### <a name="pay-frequencies"></a>Tasusagedused

Jaotist **Tasusagedused** kasutatakse määratlemiseks, kuidas töötaja töötasu määratakse (nt 10 dollarit tunnis vs 50 000 dollarit aastas) ja kuidas tunni-, nädala-, kuu- (12 kuu) ja aastamäärasid teisendatakse. Näiteks ettevõte, mis kasutab tunnipalgal olevate töötajate jaoks 38-tunnist töönädalat, määrab maksmise sageduse, mille tunnimäär on 1, nädalamäär on 38, kuumäär on 164,6666666667 ja aastamäär on 1976. Neid teisendusi kasutatakse mitmesuguste töötaja põhipalga kirjes kuvatavate tasumäärade arvutamiseks.

## <a name="fixed-compensation-plans"></a>Põhipalgaplaanid
Põhipalga plaani koostamisel saab kombineerida kõik seadistatud komponendid. Põhipalga plaani loomiseks avage leht **Põhipalga plaanid**. Siin saate anda plaanile nime ja lisada kirjelduse, valida plaani tüübi (etapp, klass või astmik), valida maksmise sageduse, mida töötaja palgamäära puhul kasutate (tunni- või aastatasu jne) ja määrata suvandeid, mis juhivad tasu töötlemise viisi. 

Säte **Vahemikust väljajäämise tolerants** võimaldab määrata, kui rangelt soovite veenduda, et tasusummad on miinimum- ja maksimumsummade vahel. Tolerantsitase **Jäik** nõuab, et tasu oleks antud tasemele määratletud vahemikus. Tolerantsitase **Paindlik** annab märku, kui tasusumma on vahemikust väljas, kuid lubab jätkata. Kui määrate tolerantsiks **Pole**, saate sisestada töötajale igasuguse tasusumma, ilma et saaksite hoiatusi või veateateid. 

Selle **rendi eeskiri** seadmine võimaldab teil määrata, kas kõik töötajad peavad saama sama kasvu, olenemata kuupäevast, mil nad olid palgatud (**rendi eeskiri** = **ükski**), või kas töötaja peaks saama protsendi alusel, kui kaua nad töötasid ajal vastavalt (**rendi eeskiri** = **%**). 

**Vahemiku kasutuse maatriks** on abiks, kui soovite vähendada aega, mis on töötajate puhul vajalik selleks, et nad jõuaksid oma vahemiku keskpunkti, või pikendada aega, mis on vajalik selleks, et nad jõuaksid vahemiku maksimaalsesse viitepunkti. Näiteks soovite anda töötajatele, kes on oma vahemiku alumise 25 protsendi sees, 110 protsenti nende sihtpreemiast, kuid töötajatele, kes on oma vahemiku ülemise 25 protsendi sees, ainult 80 protsenti nende sihtpreemiast, et nad ei jõuaks nii kiiresti maksimumini. 

Pärast põhipalgaplaani põhialuste määratlemist saate seadistada plaani tasustruktuuri. Klõpsake **loodud hüvitist**. Avaneb dialoog liugurit, mis pakub kolme võimalust:

-   Saate luua uue tasuruudustiku, valides viitepunkti seadistuse ja andes ruudustikule nime.
-   Saate luua uue tasuruudustiku, tehes koopia olemasolevast ruudustikust, mida saate lähtepunktina kasutada.
-   Saate kasutada olemasolevat tasuruudustikku, mis on juba määratletud. Kõiki sama ruudustikku kasutavaid tasuplaane värskendatakse ruudustiku muutmisel.

Kui olete valiku teinud, avaneb leht **Tasustruktuur** ja saate teha uues või olemasolevas tasuruudustikus muudatusi.

## <a name="fixed-compensation-enrollment"></a>Põhipalga registreerimine
### <a name="determine-who-is-eligible-for-the-plan"></a>Määratlege, kellele plaan kohaldub

Esimene samm töötajate registreerimisel põhipalgaplaani on määratleda, kellele plaanis määratletud tasu kohaldub. Enne kohaldamise määratlemist ei saa plaani ühelegi töötajale määrata. Abikõlblikkuse seadistamiseks avada selle **abikõlblikkuse eeskirjad** lehel. Siin, luua uus abikõlblikkuse eeskiri hüvitiste plaan ja määratleda kriteeriumid, mida töötaja peab vastama kava. Saate piirata sobivust osakonna, ametiühingu, palgapiirkonna (asukoha), töö, tööfunktsiooni, töö tüübi või palgatasemega. Töötajaid saab registreerida tasuplaani ainult juhul, kui nad vastavad kõikidele sobivusreeglis seadistatud tingimustele. 

**Märkus.** Sobivuse reegleid kasutatakse nii põhipalga kui ka ergutussüsteemi plaanide kohaldamisel. 

Sobivusreegel arvestab kirjete Töö, Ametikoht ja Töötaja konkreetsete väljade väärtust määratlemisel, kas töötajale kohaldub tasuplaan.

-   Lehel **Töö** arvestab sobivuse reegel järgmisi välju.
    -   Väli **Töö**
    -   Vahekaardil **Töö klassifikatsioon** väljad **Funktsioon** ja **Töö tüüp**
    -   Vahekaardil **Tasu** väli **Tase**
-   Lehel **Ametikohad** arvestab sobivusreegel välju **Osakond** ja **Hüvituspiirkond**.

Abikõlblikkuse reeglina leiab ka ametiühingud, mis on seotud töötaja (kohta ning **töötajate** lehekülg, edasi on **töötaja** vahekaardil, klõpsake **isikuandmeid**&gt;**ametiühingud**).

### <a name="define-fixed-compensation-actions"></a>Põhipalga tegevuste määratlemine

Valikut **Põhipalga tegevused** kasutatakse siis, kui seadistate või rakendate töötaja põhipalga muudatusi. Põhipalga tegevused võimaldavad anda kirjeldavaid nimesid tegevuste tüüpidele, mida hüvitise ja eeliste haldur saab teha. Erinevate tegevusetüüpide taga on eriline loogika, et neid saaks kasutada konkreetsetel aegadel. 

Näiteks kui töötajale on seadistatud põhipalk, saab kasutada ainult toiminguid, mille tüüp on **Palka/Palka uuesti**. Sellisel juhul võib olla vaja luua kolm erinevat toimingut tüübiga **Palka/Palka uuesti** ja anda neile nimed **Palkamine**, **Uuesti palkamine** ja **Üleviimine**. Siis on kirjeldavam selgitus ainult põhjusel, miks töötaja põhipalk anti või muudeti.

### <a name="enroll-the-employee"></a>Töötaja registreerimine

Nüüd saate määrata põhipalga plaani juurde töötaja. Avage leht **Töötajad** ja valige tasuplaani registreerimiseks töötaja. Kohta ning tegevus paanil klõpsake **hüvitist**&gt;**fikseeritud kava**. Nüüd saate luua uue kindlaksmääratud töötasu tegevuse töötaja. 

**Märkus.** Tasuplaani väljal on kuvatud ainult need plaanid, mis töötajale iga plaani puhul seadistatud sobivusreeglite põhjal kohalduvad. Kui plaanile pole ühtegi sobivusreeglit seadistatud, ei kohaldu see plaan ühelegi töötajale. 

Süsteem kontrollib, kas klassi või astmiku tüüpi tasuplaani puhul on määratud tasusumma töötaja ametikohale kehtival tasutasemel minimaalse ja maksimaalse viitepunkti vahel. Kui tasusumma on lubatud vahemikust väljas, kuvatakse hoiatus või veateade, olenevalt põhipalga plaanile määratud tolerantsi tasemest.

<a name="see-also"></a>Vt ka
--------

[Hüvitusplaanid](compensation-plans.md)


