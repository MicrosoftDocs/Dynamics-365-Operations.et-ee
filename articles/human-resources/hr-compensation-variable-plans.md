---
title: Ergutussüsteemi plaanide loomine
description: Selles artiklis kirjeldatakse komponente, mis peavad olema seadistatud, enne kui saate kasutada ergutussüsteemi ja registreerida töötaja ergustussüsteemi plaani.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f2f51a095a23b651dca645b14e652519f20037e2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070554"
---
# <a name="create-variable-compensation-plans"></a>Ergutussüsteemi plaanide loomine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ergutussüsteem moodustab töötaja ebaregulaarse tasu, nagu lisatasud või aktsiapreemiad. See artikkel selgitab, kuidas seadistada komponente, mida on vaja muutuja kompensatsiooniks ja töötaja registreerimine tulemustasu plaani.

Ergutussüsteemi summade arvutamine töötajatele võib põhineda mitmel teguril, näiteks töötaja tulemustel, töötaja palgatasemel ja osakonna tulemustel.

## <a name="variable-compensation-components"></a>Ergutussüsteemi osad
### <a name="create-compensation-types"></a>Tasutüüpide loomine

**Ergutussüsteemi tüübid** on kohustuslik osa. **Ergutussüsteemi tüübid** võimaldavad kirjeldada organisatsioonis kasutatavaid ergutussüsteeme. Samuti võimaldavad need määrata, kas tasu makstakse sularahas või mitterahalistes vahendites (nt aktsiatega).

### <a name="describe-vesting-rules"></a>Pensionireeglite kirjeldamine

Soovi korral saavad ettevõtted seadistada **Pensionireegleid**. **Pensionireeglid** kirjeldavad, kuidas tuleks preemiat aja jooksul eraldada. Näiteks võib pensionireegel sätestada, et töötaja saab nelja järgmise aasta jooksul igal aastal 25 protsenti kogu preemiast. Pensionireeglid on üksnes informatiivsed.

## <a name="variable-compensation-plans"></a>Tulemustasu plaanid
**Ergutussüsteemi plaan** sisaldab reegleid, arvutusmeetodeid ja vaikeväärtusi registreerunud töötajate ergutussüsteemi arvutamiseks. Ergutussüsteemi plaani loomisel peate määrama ergutussüsteemi tüübi. Ergutussüsteemi tüüp määrab, kas süsteem arvutab preemiana valuutasumma või ühikute arvu. 

Juurdepääsu **piiramine valitud rolliparameetritele** piirab juurdepääsu tasuplaanile valitud turberollidele, mis on inimressurssides sellele plaanile määratud. Näiteks kui loote hüvitusplaane, mis on juhatajatele ja ei tohiks olla nähtavad kõigile inimressurssidele omastele rollidele, saate seda parameetrit kasutada juurdepääsu piiramiseks nendele tasuplaanidele. 

Peate seadistama ka arvutusmeetodi.

-   **Ajahetk** – preemia arvutus põhineb põhipalgal, mis töötajal konkreetsel kuupäeval oli. See kuupäev määratakse protsessisündmuses uute tasusummade töötlemisel.
-   **Kombineeritud** – preemiasumma arvutatakse iga kordumatu põhipalga määra kohta, mis töötajal protsessisündmuse tsükli alguskuupäeva ja tsükli lõppkuupäeva vahel oli. Seejärel liidetakse määrad lõpliku preemia määramiseks kokku. Näiteks viidi tsükli ajal töötaja üle teisele ametikohale, millel oli teistsugune tasumäär. Sellisel juhul korrigeeritakse tulemustasu selle aja kohta, mille vältel töötajal kumbki tasumäär oli.

Tulemustasu summa võib põhineda töötaja regulaarse põhitasu protsendil või määratud ühikute arvul.

-   Tehke valik **Alusprotsent** vaikeprotsendi sisestamiseks ja määrake, kas alus peaks olema töötaja põhipalgamäär või töötaja palgataseme kontrollpunkt. Töötaja ametile määratakse palgatase. Üks palgastruktuuri viitepunkt võib olla määratud põhipalgaplaani kontrollpunktiks. Töötaja hüvitise taseme kontrolltaseme suuruse leidmiseks kasutatakse töötaja tööhüvitise taset ja sellele viidatakse kontrollpunktiga, mis on kirjas töötaja fikseeritud hüvituskavas. Kontrollpunkti summat kasutatakse siis töötaja fikseeritud palgamäära asemel tulemustasu alusena.
-   Valige **Ühikute arv**, et sisestada ühikute vaikearv, iga ühiku väärtus ja ühiku väärtuse valuuta, kui tasuplaan on mitterahaline tasu (nt 200 aktsiat väärtusega 40 dollarit) või lihtsalt ühikute arv, kui tasuplaan on rahalise tulemustasu kohta. Rahalise preemia puhul saab töötaja nimetatud valuutaühikute arvu, mida kasutatakse tema põhipalgaplaani puhul (nt 500 ühikut väärtusega 1 dollar). Üks-ühele seose juhtimise abil saab näidata, kas ühikute arvu ja ühiku väärtuse vahel on otsene üks-ühele vastendus. Kui koostate ergutussüsteemi plaani rahapõhisele plaanile, kasutades ühikute arvu, lukustatakse see valik automaatselt väärtusele **Jah** ja ühiku väärtus on **1,0000**.

Säte **Palkamise reegel** määrab, kas kõik töötajad peaksid saama ühesugust palgatõusu, olenemata nende palkamise kuupäevast (**Palkamise reegel** = **Pole**) või peaksid töötajad saama preemiaprotsenti selle põhjal, kui kaua nad tsükli vältel palgatud olid (**Palkamise reegel** = **Protsent**). 

**Mõjujõud** kohandab töötaja preemiat töötaja osakonna tulemuste põhjal. Igale osakonnale saab määrata tulemuste näitajad lehel **Osakonnad** jaotises **Seotud vormid** &gt; **Tasu** &gt; **Tulemused**. Osakonna töötajatele makstav preemia sõltub välja **Saavutatava eesmärgi protsent** väärtusest, mis näitab osakonna tulemust.

-   Kui osakonna tulemus on 100 protsenti, faktooritakse selle osakonna töötajate preemiat väljal **Väljamakse 100% juures** määratud protsendi võrra.
-   Kui osakonna tulemus on üle 100 protsendi, lisab süsteem väljal **1% kohta üle eesmärgi** määratud protsendi väljal **Väljamakse 100% juures** määratud protsendile, kuni jõutakse väljal **Kõrgeim lubatud väljamakse** määratud väärtuseni.
-   Kui osakonna jõudlus on alla 100 protsendi, lahutab süsteem väljal **1% kohta alla eesmärgi** määratud protsendi väljal **Väljamakse 100% juures** määratud protsendist, kuni jõutakse väljal **Madalaim lubatud väljamakse** määratud väärtuseni.

Saate seadistada läveprotsentidele **Tolerantsi tasemeid**, et juhul, kui finantsvõimendus viib protsendi läveprotsendist väljapoole, kuvatakse hoiatusteade. 

Vaikimisi kasutatakse töötajate auhindade jagamiseks töötaja ametikohale määratud osakonda. Mõne töötaja preemia võib siiski sõltuda mitme osakonna tulemustest. Sellisel juhul saab töötaja ergutussüsteemi registreerimisele määrata mitmesugused osakonnad ja preemiaprotsendi, mis iga osakonna tulemustele eraldatakse. Lisateavet leiate järgmisest teemast „Ergutussüsteemis registreerimine”. 

Finantsvõimendust kasutatakse ainult juhul, kui tasuprotsessi käivitamisel on valitud **Tulemuspalk**. 

Vahekaardil **Tasemete alistamised** saate alistada preemia vaikeprotsendi või ühikute arvu töötaja palgataseme põhjal. Kui valiku **Luba tasemete alistamised** väärtuseks on ergutussüsteemi plaanides registreeritud töötajate puhul määratud **Jah**, võrreldakse töötaja töökoha taset tasemete alistamise tabeliga, et määrata selle taseme protsent või ühikute arv. Kui taset tasemete alistamise tabelist ei leita, kasutatakse vaikeprotsenti või ühikute arvu vahekaardilt **Üldine**. Protsenti ja ühikute arvu saab alistada ka töötaja registreerimisel ergutussüsteemi plaanis.

## <a name="variable-compensation-enrollment"></a>Tulemustasu jaoks registreerimine
### <a name="determine-who-is-eligible-for-the-plan"></a>Määratlege, kellele plaan kohaldub

Kui olete valmis töötajaid ergutussüsteemi plaanides registreerima, on esimene samm otsustada, kellele plaanis määratletud tasu kohaldub. Te ei saa määrata plaani ühelegi töötajale, kui te ei määra kohaldumist. Kohaldumise seadistamiseks avage leht **Sobivuse reeglid**, et luua oma plaanile uus sobivusreegel, ja määratlege siis kriteeriumid, millele töötaja peab vastama, et tasuplaan talle kohalduks. Saate piirata sobivust osakonna, ametiühingu, palgapiirkonna (asukoha), töö, tööfunktsiooni, töö tüübi ja/või palgatasemega. Töötajaid saab registreerida tasuplaani ainult juhul, kui nad vastavad **kõikidele** sobivusreeglis seadistatud kriteeriumidele. 

**Märkus.** Sobivuse reegleid kasutatakse nii põhipalga kui ka ergutussüsteemi plaanide kohaldamisel. Sobivusreeglid arvestavad järgmiste töö, ametikoha ja töötaja kirjete väljade väärtust määratlemisel, kas töötajale kohaldub tasuplaan.

- Lehel **Töö**:
  -   Väli **Töö**
  -   Väljad **Funktsioon** ja **Töö tüüp** vahekaardil **Töö klassifikatsioon**
  -   Väli **Tase** vahekaardil **Tasu**
- Lehel **Ametikohad**: väljad **Osakond** ja **Hüvituspiirkond**.
- Lehel <strong>Töötajad</strong>: töötajaga seotud ametiühingute teave jaotises <strong>Isikuandmed</strong> &gt; <strong>Ametiühingud</strong> vahekaardil *<strong><em>Töötaja</em></strong>*

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Ergutussüsteemi plaanis registreerimise lubamine

Määrake lehel **Ergutussüsteemi plaanid** valiku **Luba registreerimine** olekuks **Jah**, et lubada sobivatel töötajatel plaanis registreeruda.

### <a name="enroll-the-employee"></a>Töötaja registreerimine

Nüüd saate töötajaid ergutussüsteemi plaanis registreerida. Töötaja registreerimiseks minge lehele **Töötajad** ja valige töötaja. Seejärel klõpsake toimingupaanil valikuid **Tasu** &gt; **Ergutussüsteemi plaanis registreerimine**. 

**Märkus.** Valiku **Registreerumine** olekuks peab olema ergutussüsteemi plaanis märgitud **Jah**. Väljal **Plaan** on kuvatud ainult need plaanid, mis töötajale iga plaani puhul seadistatud sobivusreeglite põhjal kohalduvad. Kui plaanile pole ühtki sobivusreeglit seadistatud, ei kohaldu see plaan ühelegi töötajale. 

Veenduge, et väli **Jõustumiskuupäev** oleks õigesti määratud. Kui ergutussüsteemi plaanis kasutatakse arvutusmeetodit **Kombineeritud**, võidakse töötaja preemia arvutamisel arvestada registreerumise jõustumiskuupäeva. 

Saate kasutada vahekaarti **Alistamised** töötaja puhul konkreetsete väärtuste alistamiseks. Näiteks kui valiku **Palkamise reegel** väärtuseks on plaanil määratud **Protsent** ja töötaja palkamise protsendi arvutamisel tuleb kasutada teist palkamise kuupäeva, saate määrata palkamise kuupäeva väljal **Palkamise reegli kuupäev**. Saate alistada konkreetse töötaja puhul ka väärtuse **Preemia protsent** või **Ühikute arv**, olenevalt plaani sätetest. Need väärtused faktooritakse siiski palkamise reegli, tulemustegurite ja muude plaani sätetega. 

Valikut **Organisatoorsed erandid** kasutatakse töötaja preemia arvestamiseks vähemalt ühe osakonna tulemuste põhjal. Osakondade lõikes eraldatav protsent peaks olema kokku 100. Töötaja isiklikku tulemust arvestatakse samuti. Neid sätteid kasutatakse ainult juhul, kui tasuprotsessi käivitamisel on tehtud valik **Tulemuspalk**.





[!INCLUDE[footer-include](../includes/footer-banner.md)]
