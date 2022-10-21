---
title: Varude paigutamine
description: See artikkel annab teavet strateegilise lao positsioonimise kohta, mis hõlmab punktide dekodeerimise tuvastamist tarneahelas, kus saate luua vaba kaubavaru, et tihendada täitmisajasid ja kasutada tarneahelale ära täitmisajasid.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 847108575cbf7207282db00d731363c8cfad883a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689534"
---
# <a name="inventory-positioning"></a>Varude paigutamine

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Strateegilise lao positsioon hõlmab punktide dekodeerimise tuvastamist tarneahelas, kus saate luua vaba kaubavaru. Seda lähenemist kasutatakse peamiselt täitmisaegade tihendamiseks ja tarneahelasse ära kasutada. See võimaldab teil leevendada "thewhip effect", sest nõudluse hälbeid ei läbitud kogu tarneahelas. (Vastavalt *sellele*, kuidas väikesed nõudluse kõikumised jaemüügitasemel võivad põhjustada progresseeruvalt suuremaid nõudluse kõikumisi hulgimüügi, levitaja, tootja ja toormaterjali tarnija tasemel.)

Lao asukoht on nõudlusepõhiste materjalide ressursiplaanimise (DDMRP) esimene samm.

## <a name="inventory-positioning-for-manufacturing"></a>Lao asukoha paigutus tootmises

See jaotis annab näite, mis näitab, kuidas teha lao positsioonimisotsuseid, kui te toodate tüüpilist näidistoodet. Kooslusel on mitmetasemeline kooslus, nagu näha järgmises illustratsioonis.

![Näide mitmetasemelise koosluse kohta.](media/ddmrp-bom-example.png "Näite mitmetasemeline kooslus (BOM) koosteletoote kohta")

### <a name="choose-your-decoupling-points"></a>Valige oma dekodeerimispunktid

Kui valite, kuhu oma dekodeerimise punktid panna, arvestage kriteeriumina iga koosluse iga kauba kõiki järgmiseid aspekte:

- Väline hälve
- Varude finantsvõimendus ja paindlikkus
- Kriitiline toimingukaitse
- Kliendi lubatud hälbe aeg
- Müügitellimuse nähtavuse horisond
- Turupotentsiaalne täitmisaeg

Microsofti näites võite panna oma esimese dekodeerimise punkti billette’ile *järgmistel* põhjustel:

- Raske on saada materjalide allikaid, mida kasutatakse selle abil, et teha billette’i, ja allikaks on kättesaadavus. Seetõttu on välise *hälbe* kriteerium täidetud.
- Koosluse kooslused saab tükeldada mitmeks erinevaks kujuks ja suuruseks, et luua lisandeid teistele teie toodetavatele toodetele lisaks kooslustele. Seega on varude finantsvõimenduse *ja paindlikkuse* kriteerium täidetud.

Seejärel võite panna järgmise dekodeerimispunkti kangakomplekti *, mis* on eelnevalt kärbiva kanga lõikamine. Võite selle punkti valida, sest teil on ainult üks kanga lõikamismasin. Seetõttu on kriitilise *tähtsusega toimingu kaitse* kriteerium täidetud.

Lõpuks võite panna oma viimase dekodeerimispunkti lõpetatud kaubale. Võite selle punkti valida, sest teil on müügi puhul *kliendi tolerantsi* aeg väga väike ja kuna teie müügitellimuse nähtavuse *horisond* on lühike. Seega soovite tagada, et vaba kaubavaru vastaks sissetulevatele tellimustele. Saate seada ka kõrgema hinna, säilitades nii lühikest täitmisaega, millele *turupotentsiaali täitmisaja* kriteerium viitab.

Selle analüüsi põhjal näitab järgmine näide, milline koosluse koosluse välja näeb. Kollased laosümbolid tõstavad esile dekodeerimispunktid.

![Näide kooslus koos dekodeerimise punktidega esile tõstetud.](media/ddmrp-bom-decoupling-example.png "Näide kooslus koos dekodeerimise punktidega on esile tõstetud")

### <a name="calculate-your-decoupled-lead-time"></a>Dekodeeritud täitmisaja arvutamine

See jaotis näitab, kuidas arvutada oma uusi täitmiskordi pärast seda, kui olete dekodeerimispunktid juurutanud.

Järgmises näites eelmises jaotises alustatud näidete kohta kuvatakse täitmisajad iga koosluse komponendi ülemises vasakpoolses ruudus hallis kastis. Punase liigendusega kastid näitavad kaupu, mis juhivad kumulatiivset täitmisaega (pikima täitmisaja summa koosluse igal tasandil). See täitmisaeg on 21 päeva, kui alustate nullist.

![Täitmisaegade näitekooslus.](media/ddmrp-bom-lead-times-example.png "Täitmisaegadega koosluse näide")

Kuid kui rakendate eelnevalt valitud dekodeerimise punkte, on dekodeeritud kaubad alati laos. Seetõttu on täitmisaeg 0 (null). Kohe on selle järgi uus täitmisaeg vaid viis päeva: lõime ostmiseks kaks päeva ja selle loomiseks kolm päeva. Seda täitmisaega nimetatakse dekodeeritud *täitmisajaks*.

![Dekodeeritud täitmisaja näide.](media/ddmrp-bom-decoupled-lead-time-example.png "Dekodeeritud täitmisaja näide")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Strateegilise lao positsioonimine jaemüügimudelis

Kuna jaemüüjate laos on ainult lõpetatud tooted, pole koosluste probleem. Jaemüüjad saavad siiski kasutada DDMRP-d strateegiliste varude paigutamise ja puhvertasemete seadmisega, mis põhinevad ladustamisasukohtadel jaotusvõrgus.

Järgmine näide näitab näidet ettevõtte kohta, kus on jaotuskeskus Seattle’is ja kauplustes Seattle, Atlantas ja Angeleses.

![Punktide dekodeerimisel põhinedes asukohale jaemüügimudelis.](media/ddmrp-retail-decoupl-points-example.png "Punktide dekodeerimisse loomine jaemüügimudeli asukoha alusel")

Võite otsustada, *et* raamtoote jaotuskeskusesse teisaldamise ja kaupluste vahelise ülekande aeg rikub teie kliendi tolerantsiaega, sest teie kliendid eeldavad, et raam on külastades laos. Sel juhul seadistate igas kolmes kaupluses raamkauba dekodeerimispunkti. Igal kauplusel on erinevad puhvertasemed, mis põhinevad selle täitmisaegadel, nõudlusmustritel jne.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Juuruta varude paigutamine Dynamics 365 Supply Chain Management

See jaotis kirjeldab, kuidas juurutada Microsofti lao positsioonimisstrateegiat Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Saate häälestada kauba laovarude gruppe, mis loovad dekodeerimispunktid.

Kaubad muutuvad dekodeerimispunktideks, kui nad kuuluvad laovarude gruppi, mis on konfigureeritud **dekodeerimispunkti** *laovarude koodi väärtusega*. Seega on DDMRP seadistamise esimene samm otsustada, milliseid laovarude gruppe peate oma DDMRP strateegias rakendama, ja seejärel looge need järgmiste sammude abil.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarud \> Laovarude grupid**.
1. Tegevuspaanil valige laovarude **grupi** loomiseks uus.
1. Sisestage teave, mis tuvastab laovarude grupi ja seejärel valige kasutatav kalender.
1. Vahekaardil Üldine **määrake** välja Laovarude kood **väärtuseks** Dekodeerimise *punkt*. Selle sättega koheldakse kõiki sellesse laovarude gruppi kuuluvaid kaupu DDMRP-i dekodeerimispunktidena. Samuti lubab see selle grupi jaoks kõik DDMRP-sätted, nagu kirjeldatud selles protseduuris.
1. **·** **Seadke DDMRP parameetrite jaotise vahekaardil** Muu järgmised väljad:

    - **Täitmisaja** tegur: määrake tegur (kümnendväärtusena vahemikus 0–1), et kontrollida mõju, mis peaks täitmisajal olema selles laovarude grupis kaupade minimaalse ja maksimaalse laovarude taseme arvutamisel. Üldiselt, mida kauem on kauba täitmisaeg, seda madalam peaks olema kauba täitmisaja tegur. Väiksem täitmisaja tegur toodab madalamaid minimaalseid ja maksimaalseid laotasemeid ning seetõttu väiksemaid ja sagedasemaid tellimusi. DDMRP metodoloogia soovitab väärtust vahemikus 0,20 kuni 0,40 kaupadele, mille täitmisajad on pikad, vahemikus 0,41 kuni 0,60 kaupade puhul, ning 0,61 kuni 1,00 kaupade puhul, mille täitmisajad on lühikesed. Lisateavet vt puhverprofiilist [ja tasemetest](ddmrp-buffer-profile-and-levels.md).
    - **Hälbetegur** : määrake tegur (kümnendväärtusena vahemikus 0–1), et kontrollida erineva nõudluse mõju, kui selle laovarude grupi kaupade puhul arvutatakse minimaalne laovaru tase. Üldiselt, seda muutujana peaks kauba nõudlus olema, seda kõrgem peaks olema selle hälbetegur. Suurem hälbetegur loob kõrgema minimaalse laovarude taseme. DDMRP metodoloogia soovitab väärtust 0,00 ja 0,40 väikese hälbega kaupade puhul vahemikus 0,41 kuni 0,60 keskmise hälbega kaupade puhul ning 0,61 kuni 1,00 suure hälbega kaupade puhul. Lisateavet vt puhverprofiilist [ja tasemetest](ddmrp-buffer-profile-and-levels.md).
    - **Miinimum-, maksimum- ja uuesti tellimispunkti periood** – määrake, kui sageli arvutatakse puhverväärtused (*kord päevas või* kord *nädalas*).

1. **Seadke vahekaardi** Muu jaotises Keskmine igapäevane **kasutus** järgmised väljad:

    - **Keskmine igapäevane kasutus põhineb** – valige, millistel ajaperioodidel peaks keskmise päevase kasutuse (ADU) arvutamine põhinema. Valige üks järgmistest väärtustest.

        - *Möödunud* – saate vaadata ainult möödunud perioodil (päevades **) määratud päevade arvu möödunud kasutust**. ADU arvutatakse arvutamisperioodi kauba kogu nõudlusena (laoühikutes) jagatuna arvestusperioodi päevade arvuga.
        - *Edasi* – vaadake ainult väljal Edasi (päevades) **määratud päevade arvu prognoositud tuleviku kasutust (kaasa arvatud eelarved**). ADU arvutatakse arvutamisperioodi kauba kogu nõudlusena (laoühikutes) jagatuna arvestusperioodi päevade arvuga. 
        - *Kombineeritud* – vaadake nii möödunud kui ka tulevast kasutust. Möödunud perioodi **(päevade) välja**, välja Edasi **(päevad) ja** ühendamisvalikute sätted kehtivad kõik. 

            *Kombineeritud ADU* = (\[*varasemad* × *viimase ADU*\] + \[*edasisuunas* kaalumise × *adu*\]) ÷ (*kaalutud* + *edasisuunas kaalumine*)

    - **Möödunud periood (päevades)** – sisestage möödunud päevade arv (kuni tänaseni), mida süsteem peaks selles laovarude grupis kaupade ADU arvutamiseks arvesse võtma. See säte kehtib ainult siis, kui väljal **põhinev keskmine igapäevane kasutus on** seatud väärtusele *Past* või *Blended*.
    - **Edasisuunas periood (päevades)** – sisestage tuleviku päevade arv (alates tänasest ja kuni määratud päevani), mida süsteem peaks arvestama selles laovarude grupis kaupade ADU arvutamiseks. See säte kehtib ainult siis, kui väljal **põhinev keskmine igapäevane kasutus on** seatud väärtusele *Edasi* või *Kombineeritud*.
    - **Möödunud perioodi suhteline kaal kombineeritud keskmise päevase kasutuse jaoks** – sisestage kaal (protsendina), mida rakendada möödunud perioodile, kui arvutatakse kombineeritud ADU. See säte kehtib ainult siis, kui väljal **põhinev keskmine igapäevane kasutus on** seatud sättele *Kombineeritud*.
    - **Kombineeritud keskmise päevase kasutuse edasisuunas** perioodi suhteline kaal – sisestage kaal (protsendina), mida rakendada edasisuunas perioodile, kui arvutatakse kombineeritud ADU. See säte kehtib ainult siis, kui väljal **põhinev keskmine igapäevane kasutus on** seatud sättele *Kombineeritud*.

1. Kõigi muude vahekaartide ja väljade jaoks sisestage üksikasjalikud sätted, mida kasutatakse selle laovarude grupiga lingitud kaupade nõuete arvutamiseks.

### <a name="set-an-item-as-a-decoupling-point"></a>Kauba määramine dekodeerimispunktiks

Et seadistada kaup dekodeerimispunktiks, järgige neid samme.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Otsige ja valige vabastatud kaup, mida soovite seadistada DDMRP jaoks.
1. Valige tegevuspaani vahekaardil **Plaan kauba laovarud** **.**
1. Kauba laovarude **lehel võib** juba olla loetletud mitu kauba laovarude kirjet, millest igaüks kehtib laoala ja tootedimensioonide erineva kombinatsiooni kohta. Saate valida olemasoleva kauba laovarude kirje, mis rakendub dimensioonidele, kus soovite luua dekodeerimispunkti. Võite ka valida tegevuspaanil **uue** kauba laovarude kirje loomiseks uue.
1. Seadistage kauba laovarude kirje nagu tavaliselt. Peate määrama vähemalt saidi ja lao, kus dekodeerimispunkt rakendub.
1. Kui vajalik kirje on veel valitud, valige vahekaart **Üldine**.
1. Märkige ruut **Kasuta kindlaid** sätteid.
1. Seadistage **väli Laovarude** grupp laovarude grupile, mis on seadistatud looma dekodeerimispunkte (nagu kirjeldatud eelmises jaotises).
1. Kaup on nüüd konfigureeritud dekodeerimispunktina. Tavaliselt, kui kasutate DDMRP-i, konfigureerite ka siin sätted, mis mõjutavad puhvrisuurusi ja järeltellimuse kogust. Selle konfiguratsiooni saate hiljem lõpule viia. Lisateavet sätete kohta vt dekodeerimispunkti [kauba puhvrite seadistamine](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Selleks, et planeerida kaupu, mis ei ole dekodeerimiseta punktid, järgige samu samme, mida järgite, kui kasutatakse standardsete materjalinõuete planeerimist (MRP).
