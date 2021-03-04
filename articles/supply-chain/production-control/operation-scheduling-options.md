---
title: Operatsioonide plaanimise valikud
description: Selles teemas kirjeldatakse operatsioonide plaanimise võimalusi. Operatsioonide plaanimine võimaldab anda tootmisprotsessi kohta üldise hinnangu aja jooksul.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3865bfc3b66c018f836e21bbddf658de0351e57
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426102"
---
# <a name="operations-scheduling-options"></a>Operatsioonide plaanimise valikud

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse operatsioonide plaanimise võimalusi. Operatsioonide plaanimine võimaldab anda tootmisprotsessi kohta üldise hinnangu aja jooksul.

Operatsioonide plaanimine arvutab tootmistellimuse jaoks järgmise teabe.

-   Tootmistellimusele ja igale operatsioonile määratud algus- ja lõppkuupäevad.
-   Operatsioonidele määratud ressursid.

Tootmisgraafikute arvutamisviise määravad mitmed sätted. Saate need sätted määratleda lehel **Operatsioonide plaanimine**. Järgmine teave kirjeldab plaanimisvalikuid.

## <a name="operations-scheduling"></a>Operatsioonide planeerimine
### <a name="scheduling-direction"></a>Planeerimise suund

Planeerimisprotsessis on planeerimissuund põhiline. Tootmise saab plaanida mis tahes kuupäevast edasi või tagasi, olenevalt ajastamise ja plaanimise nõuetest.

-   **Edasisuunas plaanimine**– saate plaanida tootmise alustamise võimalikult vara. Tootmist võib alustada täna, homme või mis tahes kindlal kuupäeval tulevikus. Tootmise algus planeeritakse võimalikult varasele kuupäevale ja planeeritakse sealt edasi võimalikult varase lõppkuupäevaga.
-   **Tagasisuunas plaanimine** – saate plaanida tootmise alustamise võimalikult hilja. Graafik põhineb kuupäeval, milleks tootmine peab olema lõpule viidud, ja arvutatakse tagasi hiliseima võimaliku kuupäevani, millal tootmist tuleks alustada, et see ei ületaks lõpptähtaega.

Valikud on järgmised:

-   **Tänasest edasi** – plaanimine praegusest kuupäevast edasi. (Praegune kuupäev on süsteemikuupäev.)
-   **Plaanitud algusest edasi** – plaanimine varasemast alguskuupäevast edasi. Kui varasem plaanimine puudub, on plaanimise suund praegusest kuupäevast edasi.
-   **Plaanimiskuupäevast edasi** – plaanimine väljal **Plaanimiskuupäev** määratud kuupäevast edasi. Kui te plaanimiskuupäeva ei määra, on plaanimise suund praegusest kuupäevast edasi.
-   **Tarnekuupäevast tagasi** – plaanimine tootmistellimuse jaoks määratud tarnekuupäevast tagasi. Kui valite selle suvandi, kuid tarnekuupäeva pole määratud, seatakse tarnekuupäevaks praegune kuupäev.
-   **Plaanitud lõpust tagasi** – plaanimine varem arvutatud lõppkuupäevast tagasi. Kui varasem plaanimine puudub, on lõppkuupäevaks praegune kuupäev.
-   **Plaanimiskuupäevast tagasi** – plaanimine väljal **Plaanimiskuupäev** määratud kuupäevast tagasi. Kui te plaanimiskuupäeva ei määra, kasutatakse praegust kuupäeva. Plaanimiskuupäevast tagasi plaanimine arvutatakse tootmistellimuse jaoks viimasel vajaduse arvutamise korral. Kui tootmistellimuse jaoks ei ole kuupäeva määratud, kasutatakse süsteemi praegust kuupäeva.
-   **Tähtajakuupäevast tagasi** – plaanimine viimasel vajaduse arvutamisel tootmistellimuse jaoks arvutatud tähtajakuupäevast tagasi. Kui tootmistellimuse jaoks ei ole tähtajakuupäeva määratud, kasutatakse süsteemi praegust kuupäeva.
-   **Viimase plaanimisena** – operatsioonide ja tööde plaanimise puhul salvestatakse valitud plaanimissuund ja -kuupäev. Seetõttu saate selle suvandi valida edasiseks plaanimiseks. Kui tootmistellimuse varasem plaanimine puudub, plaanitakse süsteemi praegusest kuupäevast tagasi.
-   **Homsest edasi** – plaanimine edasi praegusest kuupäevast, millele on lisatud üks päev.
-   **Eelmisest tööst edasi** – see suvand on asjakohane ainult tööde plaanimisel. Kui valite selle plaanimissuuna operatsioonide plaanimisel, plaanitakse tootmistellimus edasi praegusest kuupäevast. Tööde plaanimisel kehtestatakse plaanimine ühe töö jaoks ja kõik muud tootmise tööd plaanitakse selle töö põhjal.
-   **Eelmisest tööst tagasi** – see suvand on asjakohane ainult tööde plaanimisel. Kui valite selle plaanimissuuna operatsioonide plaanimisel, plaanitakse plaanitud tellimused praegusest kuupäevast tagasi. Tööde plaanimisel kehtestatakse plaanimine ühe töö jaoks ja kõik muud tootmise tööd plaanitakse selle töö põhjal.

### <a name="scheduling-date"></a>Planeerimiskuupäev

Seda kuupäeva kasutatakse plaanimissuundadel **Plaanimiskuupäevast edasi** ja **Plaanimiskuupäevast tagasi**. Planeerimine toimub sellest kuupäevast tagasi või edasi. Lisateavet vaadake eelmisest jaotisest „Plaanimissuund”.

### <a name="recalculate-bom-levels"></a>Arvuta kooslusetasemed uuesti

Kui valite suvandi **Arvuta kooslusetasemed**, arvutatakse valitud koosluse (BOM) tasemed ümber, et tagada õige plaanimisjärjestus.

## <a name="limitations"></a>Kitsendused
### <a name="finite-capacity"></a>Piiratud võimsus

Plaanimine sõltub tootmise lõpuleviimiseks vajalike ressursside saadavusest. Kui võimsust pole piisavalt, võidakse tootmistellimused edasi lükata või isegi peatada. Kui operatsioonide plaanimisele rakendatakse piiratud võimsus, võetakse arvesse ressurssidele tehtud olemasolevaid võimsuse reserveerimisi ja see võimsus kuvatakse kui mittesaadaval. Tootmistellimus plaanitakse nõutavate ressursside võimsuse saadavusel. Operatsioonide plaanimine kasutab operatsioonide määratud seeriat, et määrata tootmisprotsessi operatsioonide järjestus. Operatsioonide plaanimine reserveerib võimsuse ressursigruppides tootmisprotsessis määratletud operatsiooniaegade põhjal. Ressursigruppide võimsus on ressursigruppide kõigi ressursside saadaolevate võimsuste summa.

### <a name="finite-material"></a>Limiteeritud materjal

Plaanimine sõltub ka tootmiseks vajalike materjalide saadavusest. Komponentide ebapiisav saadavus võib samuti põhjustada tootmise hilinemist. Plaanimine võib põhineda ka materjalide kasutusel. Määrake lihtsalt materjalid, mis peavad tootmises saadaval olema, mitte materjalid, mis pole kriitilise tähtsusega. Seda tüüpi plaanimist nimetatakse limiteeritud materjaliga plaanimiseks. Kui määrate limiteeritud materjalid, plaanitakse tootmine materjalide saadavuse põhjal. **Märkus.** Kui optimeerite nii võimsuse kui ka materjalide alusel, arvestatakse tootmine nii, et see vastaks mõlemale piirangule. Võimsuse ja materjalide saadavust võetakse arvesse ning tootmistellimuse operatsioone ei saa plaanida alustama, enne kui võimsus ja materjalid on samal ajal ja nõutud kogustes saadaval. Märkige see ruut, kui materjale tuleks plaanimisel käsitleda limiteerituna. kui materjalid on piiratud, võetakse arvesse sellel ajal olemasolevaid materjali laovarusid. See tähendab, et planeerimisel arvestatakse kaupade arvutatud tähtajakuupäevi. Planeerimisel reserveeritakse toormaterjalid ja jaotatakse praegune tootmine. Kui plaanimine toimub mitu korda, käivitab koosnevusarvutuse ja teeb reserveeringuid ainult esimene plaanimine. Kui muudate tootmise kooslust või protsessi, käivitab koosnevusarvutuse järgmine plaanimine. Koosnevusarvutusel eeldatakse, et materjale vajatakse samal päeval. Kuna tootmine pole plaanitud koondplaani koosnevusarvutuse ajaks, kasutatakse kaupade saadavuse hindamiseks praegust kuupäeva. Seejärel kontrollib jaotamine, kas kaubad on vabad. Kui kaubad on saadaval, saab tootmisvajaduse täita. Kui kaubad pole praeguseks kuupäevaks saadaval, luuakse plaanitud tellimus ja valitakse plaanitud tellimuse vastaskonto. Kui plaanitud tellimusele on seatud automaatne kinnitamine, kinnitatakse plaanitud tellimus ostu või tootmise puhul automaatselt. Tootmise olekuks saab automaatselt dialoogiboksi **Laovarude grupid** väljal **Taotletud tootmisolek** määratud olek. Kui see ruut on tühi, käsitletakse materjale alati saadaval olevana. Seetõttu ei arvestata plaanimisel materjalide saadavust taotlemise ajal.

### <a name="finite-property"></a>Piiratud omadus

Märkige see ruut, kui tööde plaanimine peaks hõlmama atribuudinõudeid.

### <a name="keep-production-unit"></a>Säilita tootmisüksus

Valige, kas plaanimismootor peaks plaanima ainult ressursse, mis on tootmisüksuses juba määratud.

### <a name="keep-warehouse-from-resource"></a>Säilita ressursist pärinev ladu

Valige, kas plaanimismootor peaks plaanima ainult ressursse, mis on seostatud ressursis määratud sisendlaoga.

## <a name="references"></a>Viited
### <a name="schedule-references"></a>Ajakava viited

Kui viited sõltuvad tootmistellimustest, nimetatakse neid ka alamtootmisteks. Alamtootmised saab plaanida tootmistellimuse plaanimise osana. Märkige see ruut, kui alamtootmiste plaanimine peaks põhinema põhitootmise plaanimisel. Põhitootmisega seoses plaanitakse kõrgemalseisvad tootmised edasisuunas ja alustootmised tagasisuunas. Tootmistellimuste viiteid saab vaadata lehe **Tootmistellimused** väljal **Viitetase**.

### <a name="synchronize-references"></a>Sünkrooni viited

Saate sünkroonida viited tootmistellimusega. Kui see suvand on valitud, nihutatakse alamtootmiste kuupäevi ja joondatakse, kui tootmistellimuse graafikus tehakse muudatusi. Kui tootmistellimusel on üks või mitu alamtootmist, saate soovi korral plaanida alamtootmised koos põhitootmisega. Sellisel juhul ei saa põhitootmist käivitada enne, kui seotud alamtootmised on lõpule viidud. Seetõttu märkige see ruut, kui alamtootmiste plaanimine peaks põhinema valitud tootmise algus- ja lõppajal. Saate märkida selle ruudu vaid juhul, kui märgitud on ka ruut **Graafiku viited**.

## <a name="cancellation"></a>Tühistamine
### <a name="cancel-queue-time"></a>Tühista ooteaeg

Märkige see ruut, kui soovite plaanimisest ooteaja välja jätta.

### <a name="cancel-setup"></a>Tühista seadistus

Märkige see ruut, kui soovite plaanimisest seadistusaja välja jätta.

### <a name="cancel-process"></a>Tühista töötlemine

Märkige see ruut, kui soovite plaanimisest käitusaja välja jätta.

### <a name="cancel-overlap"></a>Tühista kattumine

Märkige see ruut, kui soovite plaanimisest kattumisaja välja jätta.

### <a name="cancel-transport"></a>Tühista transport

Märkige see ruut, kui soovite plaanimisest transiitaja välja jätta.

## <a name="set-default"></a>Sea vaikeväärtused
Saate praegused väärtused salvestada vaikeväärtustena. Selleks on kaks võimalust.

-   Määra minu vaikesätteks
-   Määra kõigile vaikesätteks


<a name="additional-resources"></a>Lisaressursid
--------

[Operatsioonide plaanimine](operations-scheduling.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]