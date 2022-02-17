---
title: Kaubanduskanalite fiskaalüksuse integratsiooni ülevaade
description: Selles teemas antakse ülevaade rakenduses Dynamics 365 Commerce saadaolevatest fiskaalüksuse integratsioonivõimalustest.
author: EvgenyPopovMBS
ms.date: 01/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 82913eaca1d56a5b0609480d8825717278eca132
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077188"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>Kaubanduskanalite fiskaalüksuse integratsiooni ülevaade

[!include [banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Selles teemas antakse ülevaade rakenduses Dynamics 365 Commerce saadaolevatest fiskaalüksuse integratsioonivõimalustest. 

Fiskaalüksuse integratsioon hõlmab integratsiooni erinevate fiskaalseadmete ja -teenustega, mis võimaldavad müügi fiskaalüksuse registreerimist kooskõlas kohalike rahandusseadustega, mille eesmärk on ennetada jaemüügivaldkonna maksupettust. Tavalised stsenaariumid, mida fiskaalüksuse integratsioon hõlmab, on järgmised.

- Müügi registreerimine fiskaalseadmes, mis on ühendatud kassaga (POS), nt fiskaalprinter, ja kliendi jaoks fiskaalsissetuleku printimine.
- Retail POS-is lõpule viidud müükide ja tagastustega seotud teabe turvaline edastamine välisesse veebiteenusesse, mida käitab maksuamet.
- Müügi kandeandmete muutmatuse tagamine digitaalallkirjade abil.

Fiskaalüksuse integratsiooni funktsioon on raamistik, mis pakub ühtset lahendust integratsiooni edasiarenduseks ja kohandamiseks Retail POS-i ning fiskaalseadmete ja -teenuste vahel. Funktsioon hõlmab ka fiskaalüksuse integratsiooni näidiseid, mis toetavad põhistsenaariume kindlate riikide või regioonide kohta ja töötavad kindlate fiskaalseadmete või -teenustega. Fiskaalüksuse integratsiooni näidis koosneb mitmest kaubanduskomponendi laiendusest ja sisaldub tarkvara arenduskomplektis (SDK). Lisateavet fiskaalüksuse integratsiooni näidiste kohta vt teemast [Fiskaalüksuse integreerimise näidised Commerce SDK-s](#fiscal-integration-samples-in-the-commerce-sdk). Teavet Cpmmerce SDK installimise ja kasutamise kohta vt teemast [Jaekaubanduse tarkvara arenduskomplekti (SDK) arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Selleks et toetada muid stsenaariume, mida fiskaalüksuse integratsiooni näidis ei toeta, integreerida Retail POS muude fiskaalseadmete või -teenustega või täita muude riikide või regioonide nõudeid, peate kas laiendama olemasolevat fiskaalüksuse integratsiooni näidist või looma uue näidise, kasutades näitena olemasolevat näidist.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Fiskaalse registreerimise protsess ja fiskaalseintegratsiooni näidised fiskaalseadmete ja -teenuste jaoks

Fiskaalüksuse registreerimisprotsess Retail POS-is võib hõlmata üht või mitut etappi. Iga etapp hõlmab kindlate kannete või -sündmuste fiskaalüksuse registreerimist ühes fiskaalseadmes või -teenuses. Finantsseadmes või -teenuses osalevad finantsregistreerimisel järgmised lahendusekomponendid.

- **Rahandusdokumendi pakkuja** – see komponent serialiseerib kande/sündmuse andmed vormingus, mida kasutatakse ka fiskaalseadme või -teenusega suhtlemiseks, sõelub fiskaalseadme või -teenuse vastused ja salvestab vastused kanali andmebaasi. Laiendus määratleb ka kindlad kanded ja sündmused, mis tuleb registreerida.
- **Fiskaalkonnektor** – see komponent lähtestab suhtluse rahandusseadme või -teenusega, saadab rahandusseadmele või -teenusele finantsseadmele või -teenusele päringuid või otseseid käske, tuginedes rahandusdokumendist ekstraktitud tehingu/sündmuse andmetele, ning saab vastuseid rahandusseadmest või -teenusest.

Fiskaalseintegratsiooni näidis võib sisaldada Commerce'i käitusaega (CRT), riistvarajaama ja kassalaiendeid rahandusdokumendi pakkujale ja fiskaalse konnektori jaoks. Samuti sisaldab see järgmisi komponendi konfiguratsioone.

- **Fiskaaldokumendi pakkuja konfiguratsiooni** – see konfiguratsioon määratleb fiskaaldokumentide väljundmeetodi vormingu. See sisaldab ka maksude ja makseviiside andmete vastendust, et muuta Retail POS-i andmed ühilduvaks fiskaalseadmes või hooldus püsivaras eelnevalt määratletud väärtustega.
- **Fiskaalkonnektori konfiguratsioon** – see konfiguratsioon määratleb füüsilise suhtluse konkreetse fiskaalseadme või teenusega.

Fiskaalüksuse registreerimise protsess kindla kassaregistri puhul määratletakse vastavate sätetega kassa funktsiooniprofiilis. Lisateavet finantsregistratuuri konfigureerimise, rahandusdokumendi pakkuja ja fiskaalse konnektori konfiguratsioonide üleslaadimise ning konfiguratsiooniparameetrite muutmise kohta leiate teemast [Fiskaalregistreerimise protsessi häälestamine](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Järgmine tüüpiline fiskaalne registreerimisvoog algab kassas oleva sündmusega (nt müügitehingu lõpuleviimine) ja rakendab eelnevalt määratletud sammude jada, mis hõlmab teisi Commerce'i komponente (nt CRT ja riistvarajaama).

1. Kassas taotletakse fiskaalse integratsiooni raamistikust fiskaaldokumenti.
1. FIF määrab, kas praegune sündmus nõuab eelarve registreerimist.
1. Finantsregistreerimise protsessi sätete põhjal tuvastab FIF fiskaalse konnektori ja vastava rahandusdokumendi pakkuja, mida kasutada fiskaalregistreerimiseks.
1. FIF käitab finantsdokumendi pakkujat, kes loob kannet või sündmust tähistava finantsdokumendi (nt XML-dokumendi).
1. FIF tagastab loodud rahandusdokumendi kassasse.
1. Kassas nõutakse, et FIF esitaks finantsdokumendi rahandusseadmele või -teenusele.
1. FIF käivitab fiskaaldokumendi töötleva fiskaalse konnektori ja esitab selle rahandusseadmele või teenusele.
1. FIF tagastab kassale fiskaalse vastuse (st fiskaalseadme või teenuse vastuse).
1. Kassa analüüsib fiskaalset vastust, et teha kindlaks, kas eelarve registreerimine õnnestus. Vastavalt vajadusele nõuab müügikohal, et FIF tegeleks ilmnenud vigadega. 
1. Müügikohal nõutakse, et FIF töötleks ja salvestaks fiskaalse vastuse.
1. Finantsdokumendi pakkuja töötleb fiskaalvastust. Selle töötlemise osana analüüsib fiskaaldokumentide pakkuja vastust ja ekstraktib sellest laiendatud andmed.
1. FIF salvestab vastuse ja laiendatud andmed kanali andmebaasi.
1. Vastavalt vajadusele prindib kassa kviitungi tavalise kviitungiprinteri kaudu, mis on ühendatud riistvarajaamaga. Kviitung võib sisaldada finantsvastuse nõutavaid andmeid.
 
Järgmistes näidetes on toodud tüüpiliste fiskaalseadmete või -teenuste finantsregistreerimise vood.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Maksuregistreerimine toimub riistvarajaamaga ühendatud seadme kaudu

Seda konfiguratsiooni kasutatakse siis, kui riistvarajaamaga on ühendatud füüsiline fiskaalseade (nt fiskaalprinter). See kehtib ka siis, kui suhtlemine fiskaalseadme või teenusega toimub riistvarajaama installitud tarkvara kaudu. Sellisel juhul asub finantsdokumendi pakkuja ja CRT fiskaalkonnektor riistvarajaamas.

![Finantsregistreerimine toimub riistvarajaamaga ühendatud seadme kaudu.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Maksuregistreerimine toimub välise teenuse kaudu

Seda konfiguratsiooni kasutatakse siis, kui finantsregistreerimine toimub välise teenuse kaudu, näiteks maksuhalduri hallatava veebiteenuse kaudu. Sellisel juhul asuvad nii fiskaaldokumendi pakkuja kui ka fiskaalkonnektor .CRT

![Finantsregistreerimine toimub välise teenuse kaudu.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Maksu registreerimine toimub sisemiselt CRT

Seda konfiguratsiooni kasutatakse siis, kui finantsregistreerimiseks pole vaja välist fiskaalseadet ega teenust. Näiteks kasutatakse seda siis, kui finantsregistreerimine toimub müügikannete digitaalse allkirjastamise kaudu. Sellisel juhul asuvad nii fiskaaldokumendi pakkuja kui ka fiskaalkonnektor .CRT

![Eelarve registreerimine toimub sisemiselt .CRT](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Maksuregistreerimine toimub kohaliku võrgu seadme või teenuse kaudu

Seda konfiguratsiooni kasutatakse siis, kui füüsiline fiskaalseade või fiskaalteenus on kaupluse kohalikus võrgus ja pakub HTTPS-rakenduse programmeerimisliidest (API). Sellisel juhul asub fiskaaldokumendi pakkuja ja CRT fiskaalkonnektor asub kassas.

![Maksuregistreerimine toimub kohalikus võrgus seadme või teenuse kaudu.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Tõrketöötlus

Fiskaalüksuse integratsiooni raamistik pakub fiskaalüksuse registreerimise ajal ilmnevate tõrgete lahendamiseks järgmisi võimalusi.

- **Proovi uuesti** – operaatorid saavad seda valikut kasutada, kui tõrke saab kiiresti lahendada, ja fiskaalüksuse registreerimise võib uuesti käivitada. Näiteks võib seda valikut kasutada siis, kui fiskaalseade pole ühendatud, fiskaalprinteris pole paberit või fiskaalprinteris on paberiummistus.
- **Tühista** – see valik võimaldab operaatoril praeguse kande või sündmuse fiskaalüksuse registreerimise edasi lükata, kui see nurjub. Kui registreerimine on edasi lükatud, saab operaator tööd kassas jätkata ja teha mis tahes toiminguid, mille jaoks pole fiskaalüksuse registreerimine vajalik. Kui kassas toimub sündmus, mis nõuab fiskaalüksuse registreerimist (nt uue kande avamine), kuvatakse automaatselt tõrketöötluse dialoogiboks, mis teavitab operaatorit, et eelmist kannet ei registreeritud õigesti, ja pakub tõrketöötluse valikud.
- **Jäta vahele** – operaatorid saavad seda valikut kasutada, kui fiskaalüksuse registreerimise saab teatud tingimustes vahele jätta ja kassas tavatoiminguid jätkata. Näiteks saab seda valikut kasutada, kui müügikannet, mille puhul fiskaalüksuse registreerimine nurjus, saab registreerida spetsiaalsel pabertöölehel.
- **Märgi registreerituks** – operaatorid saavad seda valikut kasutada, kui kanne on tegelikult fiskaalseadmes registreeritud (nt on prinditud fiskaalsissetulek), kuid fiskaalvastuse salvestamisel kanali andmebaasi tekkis tõrge.
- **Edasilükkamine** – operaatorid saavad seda suvandit kasutada, kui kannet ei registreeritud, kuna registreerimisteenus polnud saadaval. 

> [!NOTE]
> Enne **kasutamist tuleb suvandid Vahelejätmine** **, Registreerimine registreerituks** märkida ja **Edasi lükata**. Peale selle tuleb anda operaatoritele asjakohased õigused.

Suvandid Vahelejätmine **,** Registreerimine **ja** Edasi lükkamine **võimaldavad teabekoodidel jäädvustada tõrke kohta teatud konkreetset teavet (nt tõrke põhjust) või finantsregistreerimise vahelejätmise või kande registreeritud märkimise põhjendust**. Lisateavet tõrketöötluse parameetrite seadistamise kohta vt teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valikuline fiskaalüksuse registreerimine

Fiskaalüksuse registreerimine võib olla kohustuslik mõne toimingu jaoks, aga valikuline teiste jaoks. Näiteks võib kohustuslik olla regulaarsete müükide ja tagastuste fiskaalüksuse registreerimine, aga kliendi deposiitidega seotud toimingute fiskaalüksuse registreerimine võib olla valikuline. Sellisel juhul peaks müügi fiskaalüksuse registreerimise tegemata jätmine keelama edaspidised müügid, kuid kliendi deposiidi fiskaalüksuse registreerimise tegemata jätmine ei tohiks edaspidiseid müüke keelata. Kohustuslike ja valikuliste toimingute eristamiseks soovitame nendega tegeleda läbi eri dokumendipakkujate ning seadistada nende pakkujate jaoks fiskaalüksuse registreerimise protsessis eraldi etapid. Parameeter **Jätka tõrke korral** peab olema lubatud mis tahes etapi jaoks, mis on seotud valikulise fiskaalüksuse registreerimisega. Lisateavet tõrketöötluse parameetrite seadistamise kohta vt teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Finantsregistratuuri käsitsi uuesti käivitamine

Kui kande või sündmuse fiskaalüksuse registreerimine on pärast tõrget edasi lükatud (nt kui operaator valis tõrketöötluse dialoogiboksis suvandi **Tühista**), saate fiskaalüksuse registreerimist käsitsi uuesti alustada, käivitades vastava toimingu. Lisateavet leiate teemast [Edasi lükatud fiskaalüksuse registreerimise käsitsi käivitamise lubamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Suvand Edasilükkamine

Suvand **Edasilükkamine** võimaldab teil jätkata finantsregistreerimise protsessi, kui praegune etapp nurjub. Seda saab kasutada, kui on olemas fiskaalse registreerimise varundamise võimalus.

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
> Tervisekontroll käivitatakse ainult siis, kui praegune toiming nõuab fiskaalset registreerimist ja kui **eelarve registreerimise protsessi praeguse etapi jaoks on keelatud parameeter Jätka tõrkega**. Lisateavet leiate teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Fiskaalvastuse talletamine fiskaalkandesse

Kui kande või sündmuse fiskaalüksuse registreerimine õnnestus, luuakse kanali andmebaasi fiskaalkanne ja lingitakse algse kande või sündmusega. Samamoodi, kui nurjunud fiskaalüksuse registreerimisel valitakse suvand **Jäta vahele** või **Märgi registreerituks**, talletatakse see teave fiskaalkandesse. Fiskaalkandel on fiskaalseadme või -teenuse fiskaalvastutus. Kui fiskaalüksuse registreerimisprotsess koosneb mitmest etapist, luuakse fiskaalkanne protsessi iga etapi kohta, mille tulemuseks on õnnestunud või nurjunud registreerimine.

Fiskaalkanded edastatakse koos kannete ja *P-tööga* peakorterisse. Lehe **Kaupluse kanded** kiirkaardil **Fiskaalkanded** saate vaadata kannetega lingitud fiskaalkandeid.

Fiskaalkanne talletab järgmised üksikasjad.

- Fiskaalüksuse registreerimisprotsessi üksikasjad (protsess, konnektorigrupp, konnektor jne). Samuti talletab see fiskaalseadme seerianumbri väljale **Registrinumber**, kui see teave sisaldub fiskaalvastuses.
- Finantsregistreerimise olek: Lõpetatud edukaks **registreerimiseks, Vahele jäetud,** kui operaator valis **nurjunud registreerimiseks suvandi Jäta** vahele, **Märgitud registreeritud**, kui operaator valis **märgi registreeritud** suvandiks, või **Edasi lükatud**, kui operaator valis **valiku Edasilükkamine**.**·**
- Teabekoodi kanded, mis on seotud valitud fiskaalkandega. Teabekoodikannete vaatamiseks valige kiirkaardil **Finantskanded** rahanduskanne, mille olek **on Vahele jäetud**, **Märgitud registreeritud** või **Edasi lükatud, ja seejärel valige** Teabekoodi **kanded**.

**Laiendatud andmeid** valides saate vaadata ka rahanduskande atribuute. Kuvatav atribuutide loend on fiskaalkande loonud fiskaalregistreerimise funktsioonile omane. Näiteks saate vaadata digitaalallkirja, seerianumbrit, serdi sõrmejälge, hash algoritmi ID-d ja teisi finantskande atribuute Prantsusmaa digitaalse allkirjastamise funktsiooni jaoks.

## <a name="fiscal-texts-for-discounts"></a>Fiskaaltekstid allahindluste jaoks

Teatud riikides või regioonides kehtivad erinõuded lisatekstide kohta, mis tuleb eri tüüpi allahindluste kohaldamisel fiskaalsissetulekutele printida. Fiskaalüksuse integratsiooni funktsioon võimaldab seadistada allahindluse jaoks teksti, mis prinditakse fiskaalsissetulekul allahindlusrea järele. Käsitsi allahindluste puhul saate määrata fiskaalteksti teabekoodile, mis on määratud kassa funktsiooniprofiilis teabekoodina **Toote allahindlus**. Lisateavet allahindluste jaoks fiskaaltekstide seadistamise kohta vt teemast [Fiskaaltekstide seadistamine allahindluste jaoks](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Fiskaalüksuse x- ja z-aruannete printimine

Fiskaalüksuse integratsiooni funktsioon toetab integreeritud fiskaalseadme või -teenuse kohaste päeva lõpetamise väljavõtete loomist.

- Kassa ekraanipaigutusse tuleb lisada uued nupud, mis käivitavad vastavad toimingud. Lisateavet vt teemast [Kassa fiskaalüksuste x-/z-aruannete seadistamine](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Fiskaalüksuse integratsiooni näidises peavad need toimingud vastama fiskaalseadme vastavatele toimingutele.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Fiskaalüksuse integratsiooni näidised Commerce SDK-s

Commerce SDK-s on praegu saadaval järgmised fiskaalüksuse integratsiooni näidised:

- [Fiskaalprinteri integratsiooni näide Itaalia jaoks](./emea-ita-fpi-sample.md)
- [Fiskaalprinteri integratsiooni näide Poola jaoks](./emea-pol-fpi-sample.md)
- [Fiskaalüksuse registreerimisteenuse integratsiooni näide Austria jaoks](./emea-aut-fi-sample.md)
- [Fiskaalüksuse registreerimisteenuse integratsiooni näide Tšehhi Vabariigi jaoks](./emea-cze-fi-sample.md)
- [Juhtseadme integratsiooni näidis Rootsi jaoks](./emea-swe-fi-sample.md)
- [Fiskaalüksuse registreerimisteenuse integratsiooni näide Saksamaa jaoks](./emea-deu-fi-sample.md)
- [Fiskaalprinteri integratsiooni näide Venemaa jaoks](./rus-fpi-sample.md)

Järgmisi fiskaalintegratsiooni funktsioone rakendatakse ka fiskaalintegratsiooni raamistiku abil, kuid see on saadaval kastist väljas ja seda ei kaasata Commerce SDK-sse:

- [Fiskaalregistreerimine Brasiilia puhul](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Digitaalallkiri Prantsusmaa jaoks](./emea-fra-cash-registers.md)

Commerce SDK-s on saadaval ka järgmised fiskaalüksuse integratsiooni funktsioonid, mis aga praegu ei kasuta fiskaalüksuse integratsiooni raamistikku. Nende funktsioonide migreerimine fiskaalüksuse integratsiooni raamistikku on kavandatud tulevastesse värskendustesse.

- [Digitaalallkiri Norra jaoks](./emea-nor-cash-registers.md)

Järgmine pärandi fiskaalüksuse integreerimise funktsioon, mis on saadaval Commerce SDK-s, ei kasuta fiskaalüksuse integreerimise raamistikku ja on hilisemates värskendustes aegunud:

- [Juhtseadme integratsiooni näidis Rootsi jaoks (pärand)](./retail-sdk-control-unit-sample.md)
- [Digitaalallkiri Prantsusmaa jaoks (pärand)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
