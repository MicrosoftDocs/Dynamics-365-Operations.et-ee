---
title: Kaubanduskanalite fiskaalüksuse integratsiooni ülevaade
description: Selles teemas antakse ülevaade rakenduses Dynamics 365 Commerce saadaolevatest fiskaalüksuse integratsioonivõimalustest.
author: josaw
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 155056eb3a2acd0d66e0ace8d5558929678cb8e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798777"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>Kaubanduskanalite fiskaalüksuse integratsiooni ülevaade

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Sissejuhatus

Selles teemas antakse ülevaade rakenduses Dynamics 365 Commerce saadaolevatest fiskaalüksuse integratsioonivõimalustest. Fiskaalüksuse integratsioon hõlmab integratsiooni erinevate fiskaalseadmete ja -teenustega, mis võimaldavad müügi fiskaalüksuse registreerimist kooskõlas kohalike rahandusseadustega, mille eesmärk on ennetada jaemüügivaldkonna maksupettust. Tavalised stsenaariumid, mida fiskaalüksuse integratsioon hõlmab, on järgmised.

- Müügi registreerimine fiskaalseadmes, mis on ühendatud kassaga (POS), nt fiskaalprinter, ja kliendi jaoks fiskaalsissetuleku printimine.
- Retail POS-is lõpule viidud müükide ja tagastustega seotud teabe turvaline edastamine välisesse veebiteenusesse, mida käitab maksuamet.
- Müügi kandeandmete muutmatuse tagamine digitaalallkirjade abil.

Fiskaalüksuse integratsiooni funktsioon on raamistik, mis pakub ühtset lahendust integratsiooni edasiarenduseks ja kohandamiseks Retail POS-i ning fiskaalseadmete ja -teenuste vahel. Funktsioon hõlmab ka fiskaalüksuse integratsiooni näidiseid, mis toetavad põhistsenaariume kindlate riikide või regioonide kohta ja töötavad kindlate fiskaalseadmete või -teenustega. Fiskaalüksuse integratsiooni näidis koosneb mitmest kaubanduskomponendi laiendusest ja sisaldub tarkvara arenduskomplektis (SDK). Lisateavet fiskaalüksuse integratsiooni näidiste kohta vt teemast [Fiskaalüksuse integreerimise näidised Retail SDK-s](#fiscal-integration-samples-in-the-retail-sdk). Teavet Retail SDK installimise ja kasutamise kohta vt teemast [Retaili tarkvara arenduskomplekti (SDK) arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Selleks et toetada muid stsenaariume, mida fiskaalüksuse integratsiooni näidis ei toeta, integreerida Retail POS muude fiskaalseadmete või -teenustega või täita muude riikide või regioonide nõudeid, peate kas laiendama olemasolevat fiskaalüksuse integratsiooni näidist või looma uue näidise, kasutades näitena olemasolevat näidist.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Fiskaalüksuse registreerimisprotsess ja fiskaalüksuse integratsiooni näidised fiskaalseadmete puhul

Fiskaalüksuse registreerimisprotsess Retail POS-is võib hõlmata üht või mitut etappi. Iga etapp hõlmab kindlate kannete või -sündmuste fiskaalüksuse registreerimist ühes fiskaalseadmes või -teenuses. Riistvarajaamaga ühendatud fiskaalseadmes toimuvas fiskaalüksuse registreerimises osalevad järgmised lahenduse komponendid.

- **Commerce Runtime’i (CRT) laiendus** – see komponent serialiseerib kannete/-sündmuste andmed vormingus, mida kasutatakse ka fiskaalseadmega suhtlemiseks, sõelub vastused fiskaalseadmest ja talletab need kanali andmebaasi. Laiendus määratleb ka kindlad kanded ja sündmused, mis tuleb registreerida. Seda komponenti nimetatakse sageli *fiskaaldokumendi pakkujaks*.
- **Riistavarajaama laiendus** – see komponent lähtestab suhtluse fiskaalseadmega, saadab fiskaalseadmele taotlused ja otsekäsud fiskaaldokumendist eraldatud kande/-sündmuse andmete põhjal ning võtab vastused fiskaalseadmest vastu. Seda komponenti nimetatakse sageli *fiskaalkonnektoriks*.

Fiskaalüksuse integratsiooni näidis fiskaalseadme puhul sisaldab CRT ja riistvarajaama laiendusi vastavalt fiskaaldokumendi pakkuja ja fiskaalkonnektori kohta. Samuti sisaldab see järgmisi komponendi konfiguratsioone.

- **Fiskaaldokumendi pakkuja konfiguratsiooni** – see konfiguratsioon määratleb fiskaaldokumentide väljundmeetodi vormingu. See sisaldab ka andmetüüpide vastendust maksude ja makseviiside kohta, et panna Retail POS-ist pärit andmed ühilduma fiskaalseadme püsivaras eelmääratletud väärtustega.
- **Fiskaalkonnektori konfiguratsioon** – see konfiguratsioon määratleb füüsilise suhtluse konkreetse fiskaalseadmega.

Fiskaalüksuse registreerimise protsess kindla kassaregistri puhul määratletakse vastavate sätetega kassa funktsiooniprofiilis. Lisateavet fiskaalüksuse registreerimisprotsessi, fiskaaldokumendi pakkuja ja fiskaalkonnektori konfiguratsioonide üleslaadimise ning nende parameetrite muutmise kohta vt teemast [Fiskaalüksuse registreerimisprotsessi seadistamine](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Järgmises näites on toodud tüüpiline fiskaalüksuse registreerimise käivitamise voog fiskaalseadme puhul. Voog algab sündmusega kassas (nt müügikande lõpetamine) ja rakendab järgmised etapid.

1. Kassa taotleb CRT-st fiskaaldokumenti.
2. CRT teeb kindlaks, kas praeguse sündmuse tuleb fiskaalüksus registreerida.
3. Fiskaalüksuse registreerimisprotsessi põhjal tuvastab CRT fiskaalkonnektori ja vastava fiskaaldokumendi pakkuja, mida fiskaalüksuse registreerimiseks kasutada.
4. CRT käitab fiskaaldokumendi pakkujat, mis loob kannet või sündmust kujutava fiskaaldokumendi (nt XML-dokumendi).
5. Kassa saadab CRT ettevalmistatud dokumendi riistvarajaama.
6. Riistvarajaam käitab fiskaalkonnektorit, mis töötleb fiskaaldokumenti ja edastab selle fiskaalseadmesse või -teenusesse.
7. Kassa analüüsib fiskaalseadmest või -teenusest saadud vastust, et teha kindlaks, kas fiskaalüksuse registreerimine õnnestus.
8. CRT salvestab vastuse kanali andmebaasi.

![Lahenduse skeem](media/emea-fiscal-integration-solution.png "Lahenduse skeem")

## <a name="error-handling"></a>Tõrketöötlus

Fiskaalüksuse integratsiooni raamistik pakub fiskaalüksuse registreerimise ajal ilmnevate tõrgete lahendamiseks järgmisi võimalusi.

- **Proovi uuesti** – operaatorid saavad seda valikut kasutada, kui tõrke saab kiiresti lahendada, ja fiskaalüksuse registreerimise võib uuesti käivitada. Näiteks võib seda valikut kasutada siis, kui fiskaalseade pole ühendatud, fiskaalprinteris pole paberit või fiskaalprinteris on paberiummistus.
- **Tühista** – see valik võimaldab operaatoril praeguse kande või sündmuse fiskaalüksuse registreerimise edasi lükata, kui see nurjub. Kui registreerimine on edasi lükatud, saab operaator tööd kassas jätkata ja teha mis tahes toiminguid, mille jaoks pole fiskaalüksuse registreerimine vajalik. Kui kassas toimub sündmus, mis nõuab fiskaalüksuse registreerimist (nt uue kande avamine), kuvatakse automaatselt tõrketöötluse dialoogiboks, mis teavitab operaatorit, et eelmist kannet ei registreeritud õigesti, ja pakub tõrketöötluse valikud.
- **Jäta vahele** – operaatorid saavad seda valikut kasutada, kui fiskaalüksuse registreerimise saab teatud tingimustes vahele jätta ja kassas tavatoiminguid jätkata. Näiteks saab seda valikut kasutada, kui müügikannet, mille puhul fiskaalüksuse registreerimine nurjus, saab registreerida spetsiaalsel pabertöölehel.
- **Märgi registreerituks** – operaatorid saavad seda valikut kasutada, kui kanne on tegelikult fiskaalseadmes registreeritud (nt on prinditud fiskaalsissetulek), kuid fiskaalvastuse salvestamisel kanali andmebaasi tekkis tõrge.

> [!NOTE]
> Valikud **Jäta vahele** ja **Märgi registreerituks** tuleb aktiveerida fiskaalüksuse registreerimisprotsessis, enne kui neid saab kasutada. Peale selle tuleb anda operaatoritele asjakohased õigused.

Valikud **Jäta vahele** ja **Märgi registreerituks** võimaldavad teabekoodidel talletada tõrke kohta teatud teavet, nagu tõrke põhjus või fiskaalüksuse registreerimise vahelejätmise või kande registreerituks märkimise põhjendus. Lisateavet tõrketöötluse parameetrite seadistamise kohta vt teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valikuline fiskaalüksuse registreerimine

Fiskaalüksuse registreerimine võib olla kohustuslik mõne toimingu jaoks, aga valikuline teiste jaoks. Näiteks võib kohustuslik olla regulaarsete müükide ja tagastuste fiskaalüksuse registreerimine, aga kliendi deposiitidega seotud toimingute fiskaalüksuse registreerimine võib olla valikuline. Sellisel juhul peaks müügi fiskaalüksuse registreerimise tegemata jätmine keelama edaspidised müügid, kuid kliendi deposiidi fiskaalüksuse registreerimise tegemata jätmine ei tohiks edaspidiseid müüke keelata. Kohustuslike ja valikuliste toimingute eristamiseks soovitame nendega tegeleda läbi eri dokumendipakkujate ning seadistada nende pakkujate jaoks fiskaalüksuse registreerimise protsessis eraldi etapid. Parameeter **Jätka tõrke korral** peab olema lubatud mis tahes etapi jaoks, mis on seotud valikulise fiskaalüksuse registreerimisega. Lisateavet tõrketöötluse parameetrite seadistamise kohta vt teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-running-fiscal-registration"></a>Fiskaalüksuse registreerimise käsitsi käivitamine

Kui kande või sündmuse fiskaalüksuse registreerimine on pärast tõrget edasi lükatud (nt kui operaator valis tõrketöötluse dialoogiboksis suvandi **Tühista**), saate fiskaalüksuse registreerimist käsitsi uuesti alustada, käivitades vastava toimingu. Lisateavet leiate teemast [Edasi lükatud fiskaalüksuse registreerimise käsitsi käivitamise lubamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="fiscal-registration-health-check"></a>Fiskaalüksuse registreerimise seisundikontroll

Fiskaalüksuse registreerimise seisundikontrolli protseduur kontrollib fiskaalse seadme või teenuse saadavust konkreetsete sündmuste tekkimisel. Kui fiskaalüksuse registreerimist ei saa lõpule viia, teavitatakse sellest operaatorit ette.

Kassa käivitab seisundikontrolli järgmiste sündmuste tekkimisel.

- Avatakse uus kanne.
- Peatatud kanne kutsutakse tagasi.
- Müügi- või tagastuskanne viiakse lõpule.

Kui seisundikontroll nurjub, kuvab kassa seisundikontrolli dialoogiboksi. Selles dialoogiboksis on järgmised nupud.

- **OK** – selle nupuga saab operaator eirata seisundikontrolli tõrget ja jätkata toimingu töötlemist. Operaatorid saavad seda nuppu valida ainult siis, kui luba **Luba seisundikontrolli tõrge vahele jätta** on nende jaoks lubatud.
- **Tühista** – kui operaator valib selle nupu, tühistab kassa viimase toimingu (nt ei lisata kaupa uude kandesse).

> [!NOTE]
> Seisundikontroll käivitatakse ainult siis, kui praegune toiming nõuab fiskaalüksuse registreerimist ja parameeter **Jätka tõrke korral** on fiskaalüksuse registreerimise protsessi selles etapis keelatud. Lisateavet leiate teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Fiskaalvastuse talletamine fiskaalkandesse

Kui kande või sündmuse fiskaalüksuse registreerimine õnnestus, luuakse kanali andmebaasi fiskaalkanne ja lingitakse algse kande või sündmusega. Samamoodi, kui nurjunud fiskaalüksuse registreerimisel valitakse suvand **Jäta vahele** või **Märgi registreerituks**, talletatakse see teave fiskaalkandesse. Fiskaalkandel on fiskaalseadme või -teenuse fiskaalvastutus. Kui fiskaalüksuse registreerimisprotsess koosneb mitmest etapist, luuakse fiskaalkanne protsessi iga etapi kohta, mille tulemuseks on õnnestunud või nurjunud registreerimine.

Fiskaalkanded edastatakse koos kannete ja *P-tööga* peakorterisse. Lehe **Kaupluse kanded** kiirkaardil **Fiskaalkanded** saate vaadata kannetega lingitud fiskaalkandeid.

Fiskaalkanne talletab järgmised üksikasjad.

- Fiskaalüksuse registreerimisprotsessi üksikasjad (protsess, konnektorigrupp, konnektor jne). Samuti talletab see fiskaalseadme seerianumbri väljale **Registrinumber**, kui see teave sisaldub fiskaalvastuses.
- Fiskaalüksuse registreerimise olek: **Lõpule viidud** eduka registreerimise puhul, **Vahele jäetud**, kui operaator valis nurjunud registreerimise puhul suvandi **Jäta vahele**, või **Registreerituks märgitud**, kui operaator valis suvandi **Märgi registreerituks**.
- Teabekoodi kanded, mis on seotud valitud fiskaalkandega. Teabekoodi kannete kuvamiseks valige kiirkaardil **Fiskaalkanded** fiskaalkanne olekuga **Vahele jäetud** või **Registreerituks märgitud** ja seejärel valige suvand **Teabekoodi kanded**.

## <a name="fiscal-texts-for-discounts"></a>Fiskaaltekstid allahindluste jaoks

Teatud riikides või regioonides kehtivad erinõuded lisatekstide kohta, mis tuleb eri tüüpi allahindluste kohaldamisel fiskaalsissetulekutele printida. Fiskaalüksuse integratsiooni funktsioon võimaldab seadistada allahindluse jaoks teksti, mis prinditakse fiskaalsissetulekul allahindlusrea järele. Käsitsi allahindluste puhul saate määrata fiskaalteksti teabekoodile, mis on määratud kassa funktsiooniprofiilis teabekoodina **Toote allahindlus**. Lisateavet allahindluste jaoks fiskaaltekstide seadistamise kohta vt teemast [Fiskaaltekstide seadistamine allahindluste jaoks](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Fiskaalüksuse x- ja z-aruannete printimine

Fiskaalüksuse integratsiooni funktsioon toetab integreeritud fiskaalseadme või -teenuse kohaste päeva lõpetamise väljavõtete loomist.

- Kassa ekraanipaigutusse tuleb lisada uued nupud, mis käivitavad vastavad toimingud. Lisateavet vt teemast [Kassa fiskaalüksuste x-/z-aruannete seadistamine](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Fiskaalüksuse integratsiooni näidises peavad need toimingud vastama fiskaalseadme vastavatele toimingutele.

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Fiskaalüksuse integratsiooni näidised Retail SDK-s

Retail SDK-s on praegu saadaval järgmised fiskaalüksuse integratsiooni näidised.

- [Fiskaalprinteri integratsiooni näide Itaalia jaoks](emea-ita-fpi-sample.md)
- [Fiskaalprinteri integratsiooni näide Poola jaoks](emea-pol-fpi-sample.md)
- [Fiskaalüksuse registreerimisteenuse integratsiooni näide Austria jaoks](emea-aut-fi-sample.md)
- [Fiskaalüksuse registreerimisteenuse integratsiooni näide Tšehhi Vabariigi jaoks](emea-cze-fi-sample.md)
- [Juhtseadme integratsiooni näidis Rootsi jaoks](./emea-swe-fi-sample.md)
- [Fiskaalüksuse registreerimisteenuse integratsiooni näide Saksamaa jaoks](./emea-deu-fi-sample.md)

Retail SDK-s on saadaval ka järgmised fiskaalüksuse integratsiooni funktsioonid, mis aga praegu ei kasuta fiskaalüksuse integratsiooni raamistikku. Nende funktsioonide migreerimine fiskaalüksuse integratsiooni raamistikku on kavandatud tulevastesse värskendustesse.


- [Digitaalallkiri Prantsusmaa jaoks](emea-fra-cash-registers.md)
- [Digitaalallkiri Norra jaoks](emea-nor-cash-registers.md)

Järgmine pärandi fiskaalüksuse integreerimise funktsioon, mis on saadaval Retail SDK-s, ei kasuta fiskaalüksuse integreerimise raamistikku ja on hilisemates värskendustes aegunud.

- [Juhtseadme integratsiooni näidis Rootsi jaoks (pärand)](./retail-sdk-control-unit-sample.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]