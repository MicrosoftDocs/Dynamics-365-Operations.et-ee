---
title: Kaubandushüvitise haldus
description: Selles teemas kirjeldatakse kaubandushüvitise haldust rakenduses Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRBrokerClaims, MCRBrokerWriteOffReasonPrompt, MCRRoyaltyVendTable, MCRRoyaltyVendTrans, PdsCustRebateGroup, PdsRebateAgreement, TAMCopyTradePromotions, TAMDeduction, TAMDeductionCreate, TAMDeductionDenyReason, TAMDeductionParmDeny, TAMDeductionParmMassUpdate, TAMDeductionParmMatch, TAMDeductionParmSplit, TAMDeductionParmWriteOff, TAMDeductionType, TAMDeductionWriteOffReason, TAMFundManagement, TAMFundUsage, TAMListPage, TAMMarketingObjective, TAMMerchEventType, TAMOneTimePromotion, TAMPromoCompareGraph, TAMPromoStatistic, TAMPromotionAnalysisSummary, TAMPromotionParameters, TAMPromotionPeriod, TAMTemplateListPage, TAMTradePromotionAnalysis, TAMTradePromotions, TAMWhatIfPromotionAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c9e523ef88a472e8f6372f871360803649c9cded
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672846"
---
# <a name="trade-allowance-management"></a>Kaubandushüvitise haldus

[!include [banner](../includes/banner.md)]

Kaubandushüvitise haldus aitab ettevõtetel hallata müügi kampaaniaprogramme, mis pakuvad rahalisi tulemuspreemiaid klientidele, kes saavutavad mahulisi ja käitumuslikke eesmärke. Funktsiooni võimalused on loodud ettevõtetele, kes keskenduvad ulatuslikele kasumi nimel premeerimise protsessidele, alates kampaaniafondi eelarve koostamisest ja eraldamisest kuni hüvitise lepingu seadistamise, nõuete loomise ja töötlemise, maksete töötlemise ning kampaania tõhususe analüüsimiseni.


Selles artiklis antakse põhjalik ülevaade kaubandushüvitise halduse funktsioonist ja tutvustatakse teile tüüpilisi ülesannete komplekte, mis on seotud müügi kampaaniaprogrammide haldamisega. Seda funktsiooni peaksid oma vastavate eesmärkide saavutamiseks kasutama mitut tüüpi kasutajad, kellel on funktsionaalsed ja otsustamisrollid.

- Vaba valikuga fondide eraldamine valitud kontodele ja kampaaniatele kaubandushüvitise lepete seadistamine, lähtudes tagasiarveldustest ja ühekordsetest tervikväljamaksetest (kokkulepitud teenuse eest)
- Kokkulepitud kampaanialepingute käivitamine läbi pooleliolevate müükide ja tagasiarvelduse nõuete loomise
- Loodud nõuete arvutamine, kinnitamine ja töötlemine ning nende edastamine müügireskontrole (A/R) makse tasakaalustamise mahaarvamistena
- Kliendi osalise makse vastavusse viimine mahaarvamisega
- Kampaaniafondi kasutamise jälgimine ning programmi tulususe ja tõhususe hindamine

## <a name="audience-and-purpose"></a>Sihtgrupp ja eesmärk

Selles dokumendis sisalduv teave on mõeldud ettevõtete äriotsuste tegijatele (ametikohad nagu ostujuht, finantsjuht ja pearaamatupidaja), kellel on järgmised ülesanded.

- Kõrgetasemeliste eelarvete ja fondide eraldamine
- Müügikampaaniate plaanimine ja analüüsimine
- Töötajate haldamine, kes töötlevad tagasiarvelduste nõudeid, käivitavad makseid tootesündmuste põhjal ning tasakaalustavad osalisi makseid ja mahaarvamisi

Neid rolle täitvad inimesed otsivad võimalusi järgmiste eesmärkide saavutamiseks.

- Turunduse kampaaniafondide parem kasutamine.
- Mitmesuguste kampaaniaprogrammide ja hüvitiste paindlik arvestamine.
- Halduskoormuse ja vigade arvu vähendamine seoses kampaaniatulemuste jälgimise ja nõuete töötlemisega.
- Rahavooprognooside parandamine tulevaste kohustuste koondamisega.
- Kvantifitseeritud aluse omamine jooksvate ja tulevaste läbirääkimiste jaoks klientidega kampaaniate teemal.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Kampaaniafond ja kaubandushüvitise leping

Kaubandushüvitise leping on premeerimisprogramm, kus pakutakse rahalisi tulemuspreemiaid klientidele, kes saavutavad konkreetseid mahulisi sihtmärke ja/või käitumuslikke eesmärke. Kampaaniafondid on eelarvestatud kulud. Sedasi on võimalik kampaaniaid jäädvustada.

### <a name="promotional-fund"></a>Kampaaniafond

Kaubandushüvitise lepingutele eraldatavad fondid salvestatakse lehele **Fondid**. Lehe **Fondid** avamiseks valige suvandid **Müük ja turundus** \> **Kaubandushüvitised** \> **Fondid** \> **Fondid**.

![Fondide leht.](./media/trade-allowance-management-funds-page.png "Fondide leht")

Lehel **Fondid** saate vaadata kampaaniafondide üksikasju.

Kiirkaardil **Üldine** on näha periood, millal fond kehtib, ja selle eelarvestatud summa. Selleks et fond kampaanialepingule eraldataks, peab välja **Olek** väärtus olema **Kinnitatud**.

Kiirkaart **Kliendid** kuvab kliendi hierarhia. Klientide valimiseks, kes on fondi sihtmärgid, lohistage kliendid jaotisesse **Fondi kliendid**. Sellel kiirkaardil on näha ka, kuidas fondi kogusumma jaotub.

Kiirkaart **Üksused** kuvab üksused, mis kampaaniasse on kaasatud.

### <a name="trade-allowance-agreement"></a>Kaubandushüvitise leping

Kui fondidefinitsioon on paigas, on kampaania plaanimise järgmine samm registreerida kampaanialepingud (mida nimetatakse kaubandushüvitise lepinguteks), eraldada fondid ja määratleda iga tootesündmuse jaoks tulemuslikkuse eesmärgid.

Kaubandushüvitise lepingud salvestatakse lehele **Kaubandushüvitise lepingud**. Lehe **Kaubandushüvitise lepingud** avamiseks valige suvandid **Müük ja turundus** \> **Kaubandushüvitised** \> **Kaubandushüvitise lepingud**.

![Kaubandushüvitise lepete leht.](./media/trade-allowance-management-agreements-page.png "Kaubandushüvitise lepete leht")

#### <a name="header"></a>Päis

Valige suvand **Päis**, et minna ümber päisevaatele.

Kiirkaardil **Üldine** määravad väljad **Kuni** ja **Alates** määravad perioodi, millal leping kehtib. Lepingu kinnituse olek **Seesmiselt kinnitatud** näitab, et leping ei ole veel kehtiv ja seda ei saa rakendada müügitellimuse töötlemise ajal.

Jaotis **Analüüs** kiirkaardil **Üldine** sisaldab olulisi välju, mis määravad kampaania hinnangus kasutatavad kogused ja kulud.

- Väli **Baasühikud** määrab toodete koguse, mis tuleb valitud klientidele müüa, enne kui kampaania rakendatakse.
- Väärtus **Arvutatud lähetuskogus** arvutatakse väärtuse **Tõusu protsent** põhjal, mis on kampaania eesmärgi plaanitud tõus.
- Väli **Kaubandushüvitise kulu** arvutatakse kaubandushüvitise lepingu mitmesuguste sündmuste koguste põhjal.

Kiirkaardil **Kliendid** loendis vasakul saate valida ja vaadata kliendigruppe, mis on seadistatud eelmääratletud hierarhiatena. Seejärel saate kaubandushüvitise lepingu jaoks sihtmärkideks valida kogu hierarhia või konkreetsed kontod.

Kiirkaardil **Üksused** ja lehe **Fondid** kiirkaardil **Üksused** lisatakse tooteid lepingule, et seostada selle müüke hüvitisega, milles kokku lepiti.

Kiirkaardil **Fondid** saate vaadata kampaaniafonde, mis on seostatud selle lepinguga. Saate ka vaadata lepingu sündmuse kulude eraldamist. 100-protsendine sündmuse kulude eraldamine tähendab, et seda kampaaniat rahastatakse ainult ühest fondist. Kampaanialeping võib saada rahastust ka mitmest fondist ja kasutada võrdset või eristavat protsendi eraldamist.

#### <a name="lines"></a>Read

Järgmiseks valige suvand **Read**, et minna ümber reavaatele.

Vahekaardil **Tootesündmused** kuvatakse lepinguga kaetud sündmuste tüübid. Tüüpe on kolm: tagasiarveldus, tervikväljamakse ja väljaspool arvet.

Kui valite tootmissündmuse ja seejärel vahekaardi **Summad**, leitakse sündmuse üksikasjad.

![Kaubandushüvitise lepingu read.](./media/trade-allowance-management-agreements-lines.png "Kaubandushüvitise lepingu read")

Jaotises **Kaubandushüvitise read** saate määrata koguse või summa vahemikud, mille klient peab definitsioonide kohta saavutama, et preemiaid saada.

Tüübi **Tagasiarveldus** tootmissündmuse korral määrab vahekaardi **Summad** ülemine osa reeglid, mida järgides tagasiarveldust rakendatakse, luuakse ja makstakse. Näiteks võivad reeglid määrata tagasiarvelduse nõudele järgmised tingimused.

- See põhineb müügitellimuse loomiskuupäeval (suvandi **Arvutuskuupäeva tüüp** väärtus on **Loodud**).
- See arvutatakse müügitellimuse rea summa põhjal enne allahindlusi, mitte netosumma põhjal, mis sisaldab allahindlusi (suvandi **Võetud:** väärtus on **Bruto**).
- See põhineb müüdud toodete mahul, mitte summa (suvandi **Tagasimakse reapiiri tüüp** väärtus on **Kogus**).
- See arvutatakse kuuajalise perioodi kohta (suvandi **Müügi kumuleerimisalus** väärtus on **Kuu**). 
- See tasakaalustatakse mahaarvamisena, mitte A/P-d kasutades (suvandi **Makse tüüp** väärtus on **Kliendi mahaarvamised**).

Tüübi **Tervikväljamakse** tootmissündmuse korral kuvab vahekaart **Summad** koguse, mis makstakse kliendile mahaarvamisena, kui klient saavutab konkreetse tulemuse. Kinnituse olek **Avatud** näitab, et tervikväljamakset pole veel makstud.

Lepingu rakendamiseks müügitellimustele, mis vastavad lepingu tingimustele, peab lepingu olek olema **Kinnitatud**. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Müükide tegemine plaanitud tootmisündmuse all ja tagasiarvelduse nõuete loomine

Kui loote müügitellimuse, millel on read, mis täidavad lepingu tingimusi, saate vaadata seotud teavet lehel **Müügitellimus**, valides suvandid **Müügitellimuse rida** \> **Kuva** \> **Hinna üksikasjad**.

Lehel **Hinna üksikasjad** kiirkaardil **Tagasimaksed** näeb müügiametnik tagasiarveldust kehtivast kaubandushüvitise lepingust (tagasimakseprogrammi ID on näha) ja reale rakendatavat kogusummat. Summa kuvatakse ka väljal **Tagasimakse summa** jaotises **Eeldatav marginaal** lehel **Hinna üksikasjad**.

Müügiarve sisestamisel luuakse iga arverea kohta vastav tagasiarvelduse nõue.

> [!NOTE]
> Lehe **Hinna üksikasjad** nägemiseks valige lehel **Müügireskontro parameetrid** vahekaardil **Hinnad** märkeruut **Hinna üksikasjade lubamine**. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Nõuete töötlemine ja nende edastamine mahaarvamistena A/R-i

Tagasiarvelduste haldamise protsessi järgmised sammud on üle vaadata, arvutada ja kinnitada nõuded ning seejärel teisendada need mahaarvamisteks.

Tagasiarvelduse töölaual vaatab kampaanialepingu omanik aeg-ajalt üle loodud nõuded ja töötleb neid. Seal teisendab ka A/R-i administraator kinnitatud nõuded mahaarvamisteks või regulaarseteks makseteks, olenevalt nõude makseviisist.

Lehel **Tagasiarvelduse töölaud** saate üle vaadata nõuderidu. Kui nõuete olek on **Tuleb ümber arvutada**, tuleb need kumulatiivset efekti arvestades ümber arvutada.

### <a name="recalculate-claims"></a>Nõuete ümberarvutamine

Nõuete ümberarvutamiseks valige tegumiribal suvand **Kumuleeri**. Seejärel valige klient dialoogiboksist **Tagasimaksete kumuleerimine**.

Ümberarvutamise tulemusena loob programm summadele uued nõuded, et korrigeerida originaalnõudeid kvalifitseeruvale summale üksuse kohta. Kliendi, üksuse, valuuta, mõõtühiku, varude dimensioonide, finantsdimensioonide ja käibemaksugrupi iga eraldi kombinatsiooni kohta luuakse üks korrigeerimise nõue. Nendel korrigeerimise nõuetel on sama viide müügitellimusele ja arve numbrile kui nõuetel, mida korrigeeritakse (ehk nõuetel, mis loodi algselt müügidokumendist). Erinevalt algsest nõudest ei sisalda korrigeerimise nõue väärtusi väljadel, mis kirjeldavad algseid müügitellimuse rea summasid ja koguseid.

Pärast ümberarvutamist määratakse nõuete olekuks **Arvutatud**. Nõuete kinnitamiseks valige tegumiribal suvand **Kinnita**.

### <a name="process-claims-and-pass-them-to-ar"></a>Nõuete töötlemine ja nende edastamine A/R-i

Nõuded on nüüd A/R-i töötlemiseks valmis. Nende töötlemiseks valige tegumiribal suvand **Töötle**. 

Nõuete töötlemisel muutub olek väärtusele **Märgi**, mis näitab, et töölehe sisestamine (sisestatud tööleht on tagasimakse juurdekasvu tööleht, nagu on määratud A/R-i parameetrites) on põhjustanud järgmised sündmused. 

- Nõuded on üle kantud mahaarvamistena ajutisele kliendisaldole.
- Tagasimaksete juurdekasvukonto on krediteeritud, et kajastada kliendi tulevasi kohustusi.
- Tagasimakse kulukonto on debiteeritud, et tuvastada müügiga kaasnevat kulu.

Protsessi lõpetamiseks peab A/R-i ametnik nüüd tegelema kogunevate mahaarvamistega, kandes need üle kliendi saldole kreeditarvena (kohustus). 

Ülesande alustamiseks valige lehe **Klient** tegumiribalt suvandid **Kogu** \> **Kannete tasakaalustamine**. Seejärel valige lehelt **Kannete tasakaalustamine** suvandid **Funktsioonid** \> **Tagasiarveldusprogramm**. Sellel tagasimakse lehel on näha kõik tagasiarvelduse nõuded, mida eelnevalt töödeldi.

Kui soovite luua kreeditarve, valige kõikide ridade kohta märkeruut **Märgi** ja seejärel valige suvandid **Funktsioonid** \> **Loo kreeditarve**.

Kreeditarve loomisel sisestatakse tööleht. (Sisestatud tööleht on müügireskontro tarbimise tööleht, nagu on määratud A/R-i parameetrites.) Selle tulemusel on reaalkohustuse (kreedit) summa viidud kliendi saldole. Rahaliselt viitab see olukord, et tekkinud on järgmised sündmused.

- Kliendi müügireskontro on krediteeritud.
- Tagasimaksete juurdekasvukonto on debiteeritud.

Tüübi **Tervikväljamakse** tootesündmuse kinnitamiseks valige sündmus lehelt **Kaubandushüvitise lepingud** ja seejärel valige vahekaardilt **Summa** suvand **Kinnita**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Maksmisele kuuluva mahaarvamise ja kliendi osalise makse tasakaalustamine mahaarvamise töölauda kasutades

Sageli otsustavad kliendi tagasiarvelduste ootuses valitud arveid osaliselt maksta. Selleks et tulevikus ära hoida makse vastavusse viimisega seotud probleeme, registreerib A/R-i ametnik need osalised maksed mahaarvamistena, kui ta registreerib kliendi tegelikud maksed. Seejärel saab neid kliendi mahaarvamisi mahaarvamise töölaual hõlpsasti tasakaalustada ettevõtte makstavate nõuete summadega.

Kliendi osalise makse registreerimiseks maksete töölehel valige suvandid **Müügireskontro** \> **Maksed** \> **Maksete tööleht** ja looge uus maksete tööleht. Seejärel valige tegumiribal suvand **Mahaarvamised**. Lehel **Mahaarvamine** saate luua ja jälgida summat, mis on osaliselt makstud.

Kogumishaldur vastutab nüüd avatud kreeditarve kande ja osalise makse kande tasakaalustamise eest teineteisega mahaarvamise töölaual.

Mahaarvamiste haldamiseks valige suvandid **Müük ja turundus** \> **Kaubandushüvitised** \> **Mahaarvamised** \> **Mahaarvamise töölaud**. Lehe ülaosas on read, mis kujutavad kliendi osalisi makseid. Lehe alaosas on kliendi avatud kreeditkanded. 

Mahaarvamise tasakaalustamiseks avatud kande suhtes märkige ära mahaarvamise rida ja seejärel märkige rida vahekaardil Avatud kanded. Klõpsake tegumiribal suvandeid Haldamine > Vastenda.

Algsete nõuete olek on nüüd määratud väärtusele **Lõpule viidud**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Kampaania ja fondi tarbimise tõhususe analüüs

Programmi põhinäitajate ja fondi kasutuse ülevaate saamiseks võite kasutada mitmesuguseid aruandeid ning analüütilisi vaateid, mis on saadaval kaubandushüvitise halduses.

Lehel **Kaubandushüvitise tegevus** vahekaardil **Ülevaade** on näha kaubandushüvitise lepingu peamised üksikasjad. Teistel vahekaartidel on toodud konkreetsemad üksikasjad seotud dokumentide, maksete ja muude programmiga seotud sündmuste kohta.

Vahekaardil **Kokkuvõte** on näha kampaania raames müüdud toodete lõplik kogus, arveldatud müügisumma ning makstud tagasiarveldused ja tervikväljamaksed.

Vahekaardil **Tagasiarvelduse krediit** sisaldab üksikasju kliendile krediteeritud üksikute tagasiarvelduste kohta.

Kampaania mitmesugustest jõudlusmeetmetest analüütilisema ülevaate saamiseks võite kasutada vaadet Analüüs. Analüüsi vaatesse minemiseks klõpsake suvandeid **Müük ja turundus** \> **Kaubandushüvitised** \> **Kaubandushüvitise lepingud**. Klõpsake toimingupaanil valikut **Analüüs**.  

Kampaania mitmesugustest jõudlusmeetmetest analüütilisema ülevaate saamiseks võite kasutada vaadet Analüüs. Analüüsi vaatesse minemiseks klõpsake suvandeid **Müük ja turundus** \> **Kaubandushüvitised** \> **Kaubandushüvitise lepingud**. Klõpsake toimingupaanil valikut **Analüüs**. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]