---
title: "Ergutussüsteemi plaanide loomine"
description: "Ergutussüsteem moodustab töötaja ebaregulaarse tasu, nagu lisatasud või aktsiapreemiad. See teema kirjeldab komponente, mida tuleb seadistada enne kasutada muutuva töötasu ja registreeruda töötaja muutuva töötasu kava."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Ergutussüsteemi plaanide loomine

Ergutussüsteem moodustab töötaja ebaregulaarse tasu, nagu lisatasud või aktsiapreemiad. Selles artiklis kirjeldatakse komponente, mis peavad olema seadistatud, enne kui saate kasutada ergutussüsteemi ja registreerida töötaja ergustussüsteemi plaani.

Ergutussüsteemi summade arvutamine töötajatele võib põhineda mitmel teguril, näiteks töötaja tulemustel, töötaja palgatasemel ja osakonna tulemustel.

## <a name="variable-compensation-components"></a>Ergutussüsteemi osad
### <a name="create-compensation-types"></a>Tasutüüpide loomine

**Ergutussüsteemi tüübid **on kohustuslik osa. Ergutussüsteemi tüübid võimaldavad kirjeldada organisatsioonis kasutatavaid ergutussüsteeme. Samuti võimaldavad need määrata, kas tasu makstakse sularahas või mitterahalistes vahendites (nt aktsiatega).

### <a name="describe-vesting-rules"></a>Pensionireeglite kirjeldamine

Soovi korral saavad ettevõtted seadistada **pensionireegleid**. Omandi üleandmise reeglites kirjeldatakse, kuidas eraldada muutuva sõlmimise aja jooksul. Näiteks omandi reegel võib märkida, et töötaja saab oma kokku auhinna 25% aastas järgmise nelja aasta jooksul. Omandi üleandmise eeskirjad on ainult informatiivne.

## <a name="variable-compensation-plans"></a>Tulemustasu plaanid
**Ergutussüsteemi plaan** sisaldab reegleid, arvutusmeetodeid ja vaikeväärtusi registreerunud töötajate ergutussüsteemi arvutamiseks. Muutuv töötasu plaani loomisel peate seadistama muutuva töötasu tüüp. Muutuv töötasu liik määratleb, kas süsteem arvutab rahasumma või tunnistatud edukaks ühikute arv. Peate seadistama ka arvutusmeetodi.

-   **Aeg** – muutuv auhinna arvutus põhineb kindlasummaline hüvitis, et töötaja oli kindlal kuupäeval. Seda kuupäeva on määratud protsessi sündmuse uus hüvitissummade töötlemisel.
-   **Kombineeritud** – preemiasumma arvutatakse iga kordumatu põhipalga määra kohta, mis töötajal protsessisündmuse tsükli alguskuupäeva ja tsükli lõppkuupäeva vahel oli. Määrad liidetakse kokku, et määratleda lõpliku. Näiteks töötsükli ajal töötaja üle teise kohta, mis oli erinev tasu määr. Sellisel juhul korrigeeritakse tulemustasu selle aja kohta, mille vältel töötajal kumbki tasumäär oli.

Tulemustasu summa võib põhineda töötaja regulaarse põhitasu protsendil või määratud ühikute arvul.

-   Tehke valik **Alusprotsent** vaikeprotsendi sisestamiseks ja määrake, kas alus peaks olema töötaja põhipalgamäär või töötaja palgataseme kontrollpunkt. Hüvitise tase asub töötaja töö. Viide punktiga struktuurist hüvitise saab määrata punkti kohta kindlaksmääratud hüvitiste plaan. Süsteem kasutab töötaja tööst hüvitise tase ja sellele ristviite kontrollpunkt, mis on loetletud töötaja kindlaksmääratud hüvitiste plaan leida kontrolli punkti summa töötaja hüvitise tase. Kontrolli punkti summa kasutatakse seejärel asemel töötaja fikseeritud tasu alusena sõlmimise.
-   Valige** Ühikute arv**, et sisestada ühikute vaikearv, iga ühiku väärtus ja ühiku väärtuse valuuta, kui tasuplaan on mitterahaline tasu (nt 200 aktsiat väärtusega 40 dollarit) või lihtsalt ühikute arv, kui tasuplaan on rahalise tulemustasu kohta. Töötaja saab raha sõlmimiseks määratud arvu rahaühikutes, mida kasutatakse oma kindlaksmääratud hüvitiste plaan (nt 500 ühikut 1 USD). Üks-ühele seose kontrolli saab näidata, kas on otsene üks-ühele kaardistamine osakute arvust ja osaku väärtuse vahel. Muutuv töötasu plaani kassapõhise plaani loomisel ühikute abil suvand on automaatselt lukustatud **Jah**, ja ühiku väärtus on **1,0000**.

Selle **rendi eeskiri** seadmine võimaldab teil määrata, kas kõik töötajad peavad saama sama kasvu, sõltumata kuupäevast, tööle võeti (**rendi eeskiri** = **ükski**), või kas töötaja peaks saama protsendina auhind, mis põhineb nende töötajatele tsükli ajal (**rendi eeskiri** = **%**). 

**Finantsvõimenduse** võimaldab teil kohandada töötaja auhinna, põhinevad osakonna töötaja. Tulemuslikkus saab määrata iga osakonna ning **osakondade** lehekülg alla **seotud vormide**&gt;**hüvitist**&gt;**täitmise**. Auhind, mis töötajad selles osakonnas saada sõltub väärtus selle **protsenti eesmärgi saavutada** välja, mida näitab osakonna tulemuslikkuse:

-   Kui osakonna tulemus on 100 protsenti, faktooritakse selle osakonna töötajate preemiat väljal ** Väljamakse 100% juures** määratud protsendi võrra.
-   Kui osakonna tulemus on üle 100 protsendi, lisab süsteem väljal **1% kohta üle eesmärgi** määratud protsendi väljal **Väljamakse 100% juures** määratud protsendile, kuni jõutakse väljal **Kõrgeim lubatud väljamakse** määratud väärtuseni.
-   Kui osakonna jõudlus on alla 100 protsendi, lahutab süsteem väljal **1% kohta alla eesmärgi** määratud protsendi väljal **Väljamakse 100% juures** määratud protsendist, kuni jõutakse väljal **Madalaim lubatud väljamakse** määratud väärtuseni.

Saate seadistada läveprotsentidele **tolerantsi tasemeid**, et juhul, kui finantsvõimendus viib protsendi läveprotsendist väljapoole, kuvatakse hoiatusteade. 

Vaikimisi otsib süsteem osakond, mis on määratud töötaja. Mitu talituste võib sõltuvad siiski mõned töötajad auhinna. Sel juhul erinevate osakondade ja auhinna, mis ei eraldada järgi kohaldatakse osakaal saab määrata töötaja muutuva töötasu registreerimine. Lisateabe saamiseks vt "Muutuv töötasu kuulumist" lõik, et järgnevalt. 

Finantsvõimendust kasutatakse ainult juhul, kui tasuprotsessi käivitamisel on valitud **Tulemuspalk**. 

Selle **tasanditel alistab** vahekaardil saate alistada auhinna vaikimisi protsendi või ühikute, põhineb hüvitise töötaja. Kui **luba alistab Levelite** on seatud **Jah** töötajatele, kes õpib muutuva hüvitiste plaan, süsteem võtab töötaja tööst tasandile ja seejärel otsib see taset alistab tabelis protsendi või ühikute sellele tasemele. Kui ei leidu tase tase alistab tabelis, vaikimisi protsendi või ühikute arvu ning **üldise** vahekaart on mõeldud. Protsent ja üksuste arvu saate ka alistada töötaja liitumise kohta muutuva töötasu kava.

## <a name="variable-compensation-enrollment"></a>Tulemustasu jaoks registreerimine
### <a name="determine-who-is-eligible-for-the-plan"></a>Määratlege, kellele plaan kohaldub

Kui olete valmis töötajaid ergutussüsteemi plaanides registreerima, on esimene samm otsustada, kellele plaanis määratletud tasu kohaldub. Te ei saa määrata plaani ühelegi töötajale, kui te ei määra kohaldumist. Kohaldumise seadistamiseks avage leht **Sobivuse reeglid**, et luua oma plaanile uus sobivusreegel, ja määratlege siis kriteeriumid, millele töötaja peab vastama, et tasuplaan talle kohalduks. Saate piirata sobivust osakonna, ametiühingu, palgapiirkonna (asukoha), töö, tööfunktsiooni, töö tüübi ja/või palgatasemega. Töötajaid saab registreerida tasuplaani ainult juhul, kui nad vastavad **kõikidele** sobivusreeglis seadistatud kriteeriumidele. 

**Märkus.** Sobivuse reegleid kasutatakse nii põhipalga kui ka ergutussüsteemi plaanide kohaldamisel. Sobivusreeglid arvestavad järgmiste töö, ametikoha ja töötaja kirjete väljade väärtust määratlemisel, kas töötajale kohaldub tasuplaan.

-   Lehel **Töö**:
    -   Väli **Töö**
    -   Väljad **Funktsioon** ja **Töö tüüp** vahekaardil **Töö klassifikatsioon**
    -   Väli **Tase** vahekaardil **Tasu**
-   Lehel **Ametikohad**: väljad **Osakond** ja **Hüvituspiirkond**.
-   Kohta ning **töötajate** leht: ametiühingutele teavet, mis on seotud töötaja all **isikuandmeid**&gt;**ametiühingud** kohta on *** töötaja *** vahekaarti

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Ergutussüsteemi plaanis registreerimise lubamine

Määrake lehel **Ergutussüsteemi plaanid** valiku **Luba registreerimine** olekuks **Jah**, et lubada sobivatel töötajatel plaanis registreeruda.

### <a name="enroll-the-employee"></a>Töötaja registreerimine

Nüüd saate töötajaid ergutussüsteemi plaanis registreerida. Töötaja registreerimiseks minge lehele **Töötajad** ja valige töötaja. Kohta ning tegevus paanil klõpsake **hüvitist**&gt;**muutuva kava registreerimine**. 

**Märkus.** Valiku **Registreerumine** olekuks peab olema ergutussüsteemi plaanis märgitud **Jah**. Selle **on kavas** väljal kuvatakse vaid töötaja on puhul seatud nende kavade abikõlblikkuse eeskirjad vastavalt plaane. Kui abikõlblikkuse eeskiri ei ole plaani, ei ole töötajate õigus saada selle plaani. 

Veenduge, et selle **kuupäev** väärtuseks on seatud õigesti. Kui muutuva töötasu plaan kasutab selle **kombineeritud** arvutamise meetod registreerimise kuupäevale võib pidada töötaja auhinna arvutamise. 

Kasutage selle **alistab** vahekaarti alistada eriväärtuste töötaja. Näiteks kui **rendi eeskiri** on seatud **%** plaani, ja erinevate rendi kuupäev tuleb kasutada töötaja rendi protsendi arvutamine, seate rendi kuupäev ning **palgata reegli kuupäeva** välja. Saate alistada ka kas on **sõlmida protsenti** väärtus või on **ühikute** väärtus konkreetse töötaja, sõltuvalt plaani. Need väärtused on tegureid ikka rendi eeskiri, tulemustele ja kava muid sätteid. 

**Organisatsiooni alistab** kasutatakse ühe või mitme talituste töötaja lepingu sõlmimise aluseks. Protsent, mis on eraldatud talituste vahel peaks summa olema 100 protsenti. Töötaja isiklike töötulemuste peetakse. Neid sätteid kasutatakse ainult siis, kui **maksa töös** on valitud hüvitise protsessi käitamisel.

<a name="see-also"></a>Vt ka
--------

[Hüvitusplaanid](compensation-plans.md)


