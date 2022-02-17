---
title: Soodustuse halduse tööruum
description: See teema kirjeldab personalihalduse tööruumi kontseptuaalseid elemente.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a83dea308e3e2eec1edebd5d619f9455e1a2268
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066571"
---
# <a name="personnel-management-workspace"></a>Soodustuse halduse tööruum


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Personalihalduse** tööruum sisaldab suurt hulka sisu. See sisaldab personali liikumist, jälgib töötajate muutusi, avatud positsioone, aadressimuutusi, aeguvaid kirjeid ja analüüsi ning pakub linke konkreetsele teabele. See teema annab teavet varahalduse tööruumi iga osa kohta.

## <a name="activity-tab"></a>Tegevuse vahekaart

Vahekaart **Tegevus** sisaldab jaotisi, mis grupeerivad töötajaid nende tööhõiveprotsessi etapi alusel:

- **Palgatavad kandidaadid**
- **Alustab varsti**
- **Viimati palgatud**
- **Lahkumine**
- **Lahkunud**

Kui töötaja on ühes nendest etappidest, on konkreetsed tegevused saadaval nupuna kaardil või menüül, mis kuvatakse, kui valite ellips (**...**) ülemises parempoolses nurgas. Järgmised alamjaotised kirjeldavad vahekaardi **Tegevus** jaotisi ja loetlevad saadaolevad tegevused.

### <a name="candidates-to-hire"></a>Palgatavad kandidaadid

Tööruumi **palkamiskandidaatide** jaotis täidetakse mitmest allikast:

- Avatud andmeprotokoll (OData) üksus
- LinkedIni integreerimine
- Käsitsi tootesse sisestatud andmed

Kui kandidaadid ilmuvad **Kandidaadid palkamiseks** jaotisesse, saate kandidaadi kaardi ellipsi abil sooritada järgmisi toiminguid:

- **Lõpeta kandidaat**
- **Ära palka**
- **Palka**

> [!NOTE]
> Kui kandidaatide loend täidetakse asukohast Microsoft Dataverse, kuvatakse samad kandidaadid kõigis juriidilistes isikutes, kuna juriidiline isik polekandidaadiga seostatud.

### <a name="starting-soon"></a>Alustab varsti

**Algab varsti** loetletakse töötajad, kellel on tulevikus alguskuupäev. Loend sorditakse alguskuupäeva järgi. Tänasele kuupäevale lähim alguskuupäev loetletakse esimesena.

Kui juhataja ei ilmu kaardile, pole töötajale ametikohta määratud.

> [!NOTE] 
> Soovitame enne kontroll-loendi rakendamist määrata töötajale ametikoha. Mõnikord määratakse pardalemineku ülesanded äsja palgatud töötaja juhile. Kui ühtegi ametikohta pole määratud, ei saa uue töötaja juhatajat määrata. Sel juhul määratakse juhatajale mõeldud põhiülesanded hoopis kontroll-loendi omanikule.

Kui töötajad ilmuvad jaotises **Alagb peatselt**, on nende jaoks saadaval järgmised tegevused:

- Ametikoha määramine
- Kontrolli töösuhet
- Põhipalga määramine
- Ergutussüsteemi määramine
- Hierarhias kuvamine
- Kontroll-loendi rakendamine\*\*

\*\* See väärtus on vaikesäte. Ilmub nupuna kaardil.

### <a name="recent-hires"></a>Viimati palgatud

Jaotises **Hiljutised palkamised** loetletakse töötajad, kelle alguskuupäev on hiljutine. Loend sorditakse alguskuupäeva järgi. Tänasele kuupäevale lähim alguskuupäev loetletakse esimesena.

Vaikimisi kuvatakse loendis töötajad, kes on palgatud viimase 7 päeva jooksul. Selle sätte muutmiseks määratlege **inimressursside parameetrite** leht, **Üldisel** vahekaardil, määratlemaks ajaplaani **Hiljutised palkamised**. Jaotises **Hiljutised palkamised** saab kuvada andmeid kindla päevade, kuude või aastate arvu kohta. Näiteks viimase 14 päeva jooksul palgatud töötajate loendi vaatamiseks seadke välja **Periood** väärtuseks **14** ja **Ühik** välja väärtuseks **Päevad**.

> [!NOTE]
> Lehel **Inimressursside parameetrid** jaotatakse sätted ettevõttepõhiselt. Seetõttu võib ajaraam, mille jooksul hiljuti palgatud on, ettevõtteti erineda. Näiteks ettevõttes USMF võite tahta vaadata kõiki viimasest seitsmest päevast pärit uusi palkamisi. Kuid USSI ettevõttes võiksite vaadata kõiki viimase 14 päeva uusi töötajaid. Sellisel juhul avage **igas ettevõttes inimressursside parameetrite** leht ja seadke parameetrid vastavalt vajadusele.

Kui juhataja ei ilmu kaardile, pole töötajale ametikohta määratud.

Kui töötajad ilmuvad jaotises **Viimased palkamised**, on nende jaoks saadaval järgmised tegevused:

- Ametikoha määramine
- Kontrolli töösuhet
- Põhipalk
- Ergutussüsteemi määramine
- Hierarhias kuvamine
- Kontroll-loendi rakendamine\*\*

\*\* See väärtus on vaikesäte. Ilmub nupuna kaardil.

### <a name="exiting"></a>Lahkumine

**Lahkumas** jaotises loetletakse töötajad, kellel on tulevikus lahkumiskuupäev. Loend sorditakse lahkumiskuupäeva järgi. Tänasele kuupäevale lähim lahkumiskuupäev loetletakse esimesena. 

Vaikimisi kuvatakse loendis töötajad, kelle lahkumiskuupäev on järgmise seitsme päeva jooksul. Selle sätte muutmiseks määratlege **inimressursside parameetrite** leht, **Üldisel** vahekaardil, määratlemaks ajaplaani **Vaata lahkunud töötajaid**. Jaotises **Lahkunud** saab kuvada andmeid kindlate päevade, kuude või aastate arvu kohta. Näiteks viimase 14 päeva jooksul lahkunud töötajate loendi vaatamiseks seadke välja **Periood** väärtuseks **14** ja **Ühik** välja väärtuseks **Päevad**.

Kui töötajad ilmuvad jaotises **Lahkunud**, on nende jaoks saadaval järgmised tegevused:

- Kontroll-loendi rakendamine\*\*
- Kontrolli töösuhet
- Hierarhias kuvamine

\*\* See väärtus on vaikesäte. Ilmub nupuna kaardil.

### <a name="exited"></a>Lahkunud

Jaotises **Lahkunud** loetletakse töötajad, kelle lahkumiskuupäev on hiljutine. Loend sorditakse lahkumiskuupäeva järgi. Tänasele kuupäevale lähim lahkumiskuupäev loetletakse esimesena.

Vaikimisi kuvatakse loendis töötajad, kelle lahkumiskuupäev on viimase seitsme päeva jooksul. Selle sätte muutmiseks määratlege **inimressursside parameetrite** leht, **Üldisel** vahekaardil, määratlemaks ajaplaani **Vaata lahkunud töötajaid**. Jaotises **Lahkunud** saab kuvada andmeid kindlate päevade, kuude või aastate arvu kohta. Näiteks viimase 14 päeva jooksul lahkanud töötajate loendi vaatamiseks seadke välja **Periood** väärtuseks **14** ja **Ühik** välja väärtuseks **Päevad**.

Kui töötajad ilmuvad jaotises **Lahkunud**, on nende jaoks saadaval järgmised tegevused:

- Kontroll-loendi rakendamine\*\*
- Kontrolli töösuhet
- Hierarhias kuvamine

\*\* See väärtus on vaikesäte. Ilmub nupuna kaardil.

## <a name="employee-changes-tab"></a>Töötaja muudatuste vahekaart

Vahekaart **Töötaja muudatused** annab kõigi töötaja personalitoimingute loendi. See valik pole vaikimisi saadaval. Funktsiooni lubamiseks seadke **inimressursside jagatud parameetrite** lehel **Personalitoimingud** vahekaardil suvandi **Luba töötaja tegevused** väärtusele **Jah**.

## <a name="position-changes-tab"></a>Vahekaart Positsiooni muudatused

Vahekaart **Töötaja muudatused** annab kõigi töötaja ametikoha toimingute loendi. See valik pole vaikimisi saadaval. Funktsiooni lubamiseks seadke **inimressursside jagatud parameetrite** lehel **Personalitoimingud** vahekaardil suvandi **Luba töötaja tegevused** väärtusele **Jah**.

## <a name="open-positions-tab"></a>Avatud positsioonide vahekaart

Vahekaardil **Avatud ametikohad** loetletakse kõik avatud ametikohad. Loendis ilmuvate ametikohtade aktiveerimiskuupäev peab olema täna või varasem ja neil ei tohi olla praegust töötajamäärangut.

> [!NOTE]
> Loend arvestab töötaja määramise tänasest. Kõiki ametikohti, mil on tulevikku ajastatud töötajamäärang, ilmuvad jätkuvalt loendis. Kuid pärast töötajamäärangu kehtivuse kuupäeva on saavutatud, eemaldatakse positsioon loendist.

## <a name="expiring-records-tab"></a>Aeguva kirje vahekaart

**Aeguvate kirjete** vahekaardil loetletakse kõik aegunud või aeguvad töötajate üksused, kus kasutaja on sisse loginud. Loendis kuvatakse järgmised üksused:

- **Serdid**
- **Tuvastamine**
- **Katseajad**
- **Skriiningud**
- **Katsed**

Määramaks, kas loend näitab aegunud või aegunud kirjeid, määratlege **inimressursside parameetrite** lehel vahekaardil **Üldine** aegunud kirjete ajaraamiks kas **Aeguvad kirjed** või **Aegunud kirjed**. Vahekaardil **Aeguvad kirjed** saab andmeid näidata kindla päevade arvu kohta. Näiteks järgmise 14 päeva jooksul aegumispäevade loendi vaatamiseks seadke **päevade arvu** välja väärtuseks **14**.

> [!NOTE] 
> Kui seate ajaraamiks **aegunud kirjete** või **aegumiskirjete** lehel **0** **inimressursside parameetrite** lehel, ei näita loend ühtegi kirjet neist.

## <a name="employees-tile"></a>Töötajate paanid

Paanil **Töötajad** kuvatakse kõigi selles ettevõttes töötavate töötajate arv, kellele kasutaja on hetkel sisse logitud. Kui valite **Töötajad** paani, kuvatakse uuel lehel töötajate üksikasjad.

## <a name="contractors-tile"></a>Peatöövõtjate paanid

Paanil **peatöövõtjad** kuvatakse kõigi peatöövõtjate arv, kes on ettevõttes palgal, kelle kasutaja on hetkel sisse logitud. Kui valite **Peatöövõtjad** paani, kuvatakse uuel lehel peatöövõtjate üksikasjad.

## <a name="open-positions-tile"></a>Avatud positsioonide vahekaart

**Avatud ametikohtade** paanis loendatakse kõik avatud ametikohad. Kui valite **Avatud ametikohad** paani, kuvatakse uuel lehel avatud ametikohtade üksikasjad. Loendis ilmuvate ametikohtade aktiveerimiskuupäev peab olema täna või varasem ja neil ei tohi olla praegust töötajamäärangut.

> [!NOTE]
> Paan arvestab töötaja määramise tänasest. Kõiki ametikohti, mil on tulevikku ajastatud töötajamäärang, ilmuvad jätkuvalt loendis. Kuid pärast töötajamäärangu kehtivuse kuupäeva on saavutatud, eemaldatakse positsioon loendist.

## <a name="approvals-tile"></a>Kinnituste paanid

**Kinnitused** paanil loendatakse kõik töövoo üksused, mis on praeguse kasutaja kinnituse ootel. Kui valite paani **Kinnitused**, kuvatakse uuel lehel töövooüksuste üksikasjad, mis nõuavad teie kinnitust.

## <a name="address-changes-tile"></a>Aadressi muudatuste paan

**Aadressimuudatuste** paanis on loendatud kõik aadressimuudatused, mis on ilmnenud päevade arvu jooksul, mis on määratud **inimressursside parameetrite** lehel. Kui valite paani **Aadressimuudatused**, kuvatakse uuel leheküljel iga aadressimuudatuse üksikasjad. Soovi korral saate valida ülemises parempoolses nurgas suvandi **Kaasa tulevased aadressimuudatused**, et kuvada tulevase kuupäevaga aadressimuudatused.

Lisateavet selle kohta, kuidas vaadata ja hallata aadressimuudatusi, vaadake [Vaadake ja hallake aadressimuudatusi](hr-personnel-view-address-changes.md).
