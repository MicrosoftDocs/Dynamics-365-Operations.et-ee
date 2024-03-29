---
title: Ärikanalite fiskaalintegratsiooni ülevaade
description: See artikkel annab ülevaate fiskaalintegratsiooni võimalustest, mis on saadaval Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1812405db3c1e58eaf7cd1df3896f786e7bf026f
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631232"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Ärikanalite fiskaalintegratsiooni ülevaade

[!include [banner](../includes/banner.md)]

See artikkel on ülevaade fiskaalintegratsiooni võimalustest, mis on saadaval Dynamics 365 Commerce. 

Fiskaalüksuse integratsioon hõlmab integratsiooni erinevate fiskaalseadmete ja -teenustega, mis võimaldavad müügi fiskaalüksuse registreerimist kooskõlas kohalike rahandusseadustega, mille eesmärk on ennetada jaemüügivaldkonna maksupettust. Tavalised stsenaariumid, mida fiskaalüksuse integratsioon hõlmab, on järgmised.

- Müügi registreerimine fiskaalseadmes, mis on ühendatud kassaga (POS), nt fiskaalprinter, ja kliendi jaoks fiskaalsissetuleku printimine.
- Retail POS-is lõpule viidud müükide ja tagastustega seotud teabe turvaline edastamine välisesse veebiteenusesse, mida käitab maksuamet.
- Aitab tagada müügikande andmete alistust digitaalallkirjade kaudu.

Fiskaalüksuse integratsiooni funktsioon on raamistik, mis pakub ühtset lahendust integratsiooni edasiarenduseks ja kohandamiseks Retail POS-i ning fiskaalseadmete ja -teenuste vahel. Funktsioon hõlmab ka fiskaalüksuse integratsiooni näidiseid, mis toetavad põhistsenaariume kindlate riikide või regioonide kohta ja töötavad kindlate fiskaalseadmete või -teenustega. Fiskaalüksuse integratsiooni näidis koosneb mitmest kaubanduskomponendi laiendusest ja sisaldub tarkvara arenduskomplektis (SDK). Lisateavet fiskaalüksuse integratsiooni näidiste kohta vt teemast [Fiskaalüksuse integreerimise näidised Commerce SDK-s](#fiscal-integration-samples-in-the-commerce-sdk). Teavet Cpmmerce SDK installimise ja kasutamise kohta vt teemast [Jaekaubanduse tarkvara arenduskomplekti (SDK) arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Selleks et toetada muid stsenaariume, mida fiskaalüksuse integratsiooni näidis ei toeta, integreerida Retail POS muude fiskaalseadmete või -teenustega või täita muude riikide või regioonide nõudeid, peate kas laiendama olemasolevat fiskaalüksuse integratsiooni näidist või looma uue näidise, kasutades näitena olemasolevat näidist.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Fiskaalregistreerimise protsess ja fiskaalintegratsiooni näidised fiskaalseadmete ja teenuste puhul

Fiskaalüksuse registreerimisprotsess Retail POS-is võib hõlmata üht või mitut etappi. Iga etapp hõlmab kindlate kannete või -sündmuste fiskaalüksuse registreerimist ühes fiskaalseadmes või -teenuses. Järgmised lahenduse komponendid osalevad fiskaalseadmes või -teenuses fiskaalregistreerimises:

- **Fiskaaldokumendi** pakkuja: see komponent järjestab kande/sündmuse andmed vormingus, mida kasutatakse ka fiskaalseadme või -teenusega suhtlemiseks, sõelub vastused fiskaalseadmest või teenusest ja salvestab vastused kanali andmebaasis. Laiendus määratleb ka kindlad kanded ja sündmused, mis tuleb registreerida.
- **Fiskaalühendus**: see komponent käivitab side fiskaalseadme või teenusega, saadab finantsseadmele või -teenusele päringud või otsekäsud, võttes aluseks finantsdokumendist ekstraktitud kande/sündmuse andmed ja võtab vastu fiskaalseadmelt või -teenusest saadud vastused.

Fiskaalintegratsiooni näidis võib sisaldada commerce runtime’i (CRT), riistvarajaama ja kassa laiendeid fiskaaldokumendi pakkujale ja fiskaalühendusele. Samuti sisaldab see järgmisi komponendi konfiguratsioone.

- **Fiskaaldokumendi pakkuja konfiguratsiooni** – see konfiguratsioon määratleb fiskaaldokumentide väljundmeetodi vormingu. See sisaldab ka maksude ja makseviiside andmevastendust, et retail POS-i andmed ühilduks fiskaalseadmes või teenuses eelmääratletud väärtustega.
- **Fiskaalkonnektori** konfiguratsioon – see konfiguratsioon määrab füüsilise side konkreetse fiskaalseadme või teenusega.

Fiskaalüksuse registreerimise protsess kindla kassaregistri puhul määratletakse vastavate sätetega kassa funktsiooniprofiilis. Lisateavet fiskaalregistreerimise protsessi konfigureerimise, fiskaaldokumendi pakkuja ja fiskaalkonnektori konfiguratsioonide konfigureerimise ja konfiguratsiooniparameetrite muutmise kohta vt [fiskaalregistreerimise protsessi seadistamine](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Kui vajate mitterahaliste toimingute seadmeid, nt tootekataloogi otsingut, kliendi otsingut või kande mustandi loomist, saate need valida finantsprotsessi piirangutega registritena. Lisateavet vt häälestage fiskaalregistreerimispiirangutega [registrid](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions).

Järgmine tüüpiline fiskaalregistreerimise voog algab kassa sündmusega (nt müügikande lõpetamine) ja juurutab eelmääratletud astmete järjestuse, mis hõlmab muid Ärikomponente (CRT nt riistvarajaam).

1. Kassa taotleb fiskaaldokumenti fiskaalintegratsiooni raamistikust (FIF).
1. FIF määrab, kas praegune sündmus nõuab fiskaalregistreerimist.
1. Fiskaalregistreerimise protsessi sätete põhjal tuvastab FIF fiskaalühenduse ja vastava fiskaaldokumendi pakkuja fiskaaldokumendi registreerimiseks.
1. FIF käitab finantsdokumendi pakkujat, mis loob fiskaaldokumendi (nt XML-dokumendi), mis tähistab kannet või sündmust.
1. FIF tagastab loodud fiskaaldokumendi kassasse.
1. Kassa taotleb FIF-i finantsdokumendi esitamist fiskaalseadmele või -teenusele.
1. FIF käitab fiskaalühendust, mis töötleb finantsdokumenti ja esitab selle fiskaalseadmele või -teenusele.
1. FIF tagastab fiskaalvastuse (st fiskaalseadme või teenuse vastuse) kassasse.
1. Müügikohas analüüsitakse fiskaalvastust fiskaalregistreerimise edu kindlaksmääramiseks. Vastavalt vajadusele taotleb kassa, et FIF käsitleb mis tahes ilmnenud tõrkeid. 
1. Kassa taotleb FIF-protsessi ja salvestab fiskaalvastuse.
1. Finantsdokumendi pakkuja töötleb fiskaalvastust. Osana sellest töötlemisest sõelub fiskaaldokumendi pakkuja vastuse ja ekstraktib sellelt laiendatud andmed.
1. FIF salvestab vastuse ja laiendatud andmed kanali andmebaasi.
1. Nagu nõutud, prindib kassa kviitungi tavalise kviitungiprinteri kaudu, mis on ühendatud riistvarajaamaga. Kviitung võib sisaldada fiskaalvastuse nõutud andmeid.
 
Järgmised näited näitavad fiskaalregistreerimise käivitamisvoogusid tüüpiliste finantsseadmete või -teenuste puhul.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Fiskaalregistreerimine toimub riistvarajaamaga ühendatud seadme kaudu.

Seda konfiguratsiooni kasutatakse siis, kui füüsiline fiskaalseade, nt fiskaalprinter, on ühendatud riistvarajaamaga. See on rakendatav ka siis, kui side fiskaalseadme või teenusega toimub riistvarajaamas installitud tarkvara kaudu. Sellisel juhul asub fiskaaldokumendi pakkuja riistvarajaamas CRT ja fiskaalühenduse asukoht riistvarajaamas.

![Fiskaalregistreerimine riistvarajaamaga ühendatud seadme kaudu.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Fiskaalregistreerimine toimub välise teenuse kaudu.

Seda konfiguratsiooni kasutatakse siis, kui fiskaalregistreerimist tehakse välise teenuse kaudu, nt maksuhalduri käitatav veebiteenus. Sel juhul asuvad nii fiskaaldokumendi pakkuja kui ka fiskaalühendused .CRT

![Fiskaalregistreerimine välise teenuse kaudu.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Fiskaalregistreerimine toimub sisemiselt ettevõttes CRT

Seda konfiguratsiooni kasutatakse siis, kui fiskaalregistreerimiseks pole vaja välist fiskaalseadet ega teenust. Seda kasutatakse näiteks siis, kui fiskaalregistreerimine toimub müügikannete digitaalsel allkirjastamisel. Sel juhul asuvad nii fiskaaldokumendi pakkuja kui ka fiskaalühendused .CRT

![Fiskaalregistreerimine toimub sisemiselt ettevõttes CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Fiskaalregistreerimine toimub kohaliku võrgu seadme või teenuse kaudu.

Seda konfiguratsiooni kasutatakse siis, kui füüsiline fiskaalseade või fiskaalteenus on kaupluse kohalikus võrgus olemas ja pakub HTTPS-i rakenduse programmeerimisliidest (API). Sellisel juhul asub fiskaaldokumendi pakkuja kassas CRT ja fiskaalühendus kassas.

![Fiskaalregistreerimine toimub kohalikus võrgus seadme või teenuse kaudu.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Tõrketöötlus

Fiskaalüksuse integratsiooni raamistik pakub fiskaalüksuse registreerimise ajal ilmnevate tõrgete lahendamiseks järgmisi võimalusi.

- **Kordage –** operaator saab seda suvandit kasutada, kui tõrke saab kiiresti lahendada ja fiskaalregistreerimist saab uuesti käivitada. Näiteks võib seda valikut kasutada siis, kui fiskaalseade pole ühendatud, fiskaalprinteris pole paberit või fiskaalprinteris on paberiummistus.
- **Tühista** – see valik võimaldab operaatoril praeguse kande või sündmuse fiskaalregistreerimise nurjumisel edasi viitda. Pärast registreerimise edasilükkamist saab operaator kassaga edasi töötada ja lõpetada mis tahes toimingu, mille jaoks fiskaalregistreerimine ei ole vajalik. Kui kassas toimub sündmus, mis nõuab fiskaalüksuse registreerimist (nt uue kande avamine), kuvatakse automaatselt tõrketöötluse dialoogiboks, mis teavitab operaatorit, et eelmist kannet ei registreeritud õigesti, ja pakub tõrketöötluse valikud.
- **Jäta** vahele – operaator saab seda suvandit kasutada, kui praeguse kande või sündmuse fiskaalregistreerimist ei ole võimalik lõpetada, **nt** kui fiskaalprinter on tellimusest väljas ja fiskaalregistreerimise saab kindlatel tingimustel vahele jätta. Näiteks saab seda valikut kasutada, kui müügikannet, mille puhul fiskaalüksuse registreerimine nurjus, saab registreerida spetsiaalsel pabertöölehel. Pärast fiskaalregistreerimise vahelejätmist saab kassas regulaarseid toiminguid jätkata. 
- **Märgi registreeritud** - operaator saab seda suvandit kasutada, kui praegune kanne või sündmus on tegelikult fiskaalseadmes registreeritud, näiteks fiskaalsissetulek on prinditud, kuid fiskaalvastuse salvestamisel kanali andmebaasi ilmnes tõrge. Pärast praeguse kande või sündmuse märkimist registreerimiseks saab kassas regulaarseid toiminguid jätkata.
- **Lükka** edasi – operaator saab seda valikut kasutada, kui kannet pole **registreeritud**, kuna registreerimisseade või teenus ei ole saadaval ja kehtib üks järgmistest:
    - On olemas varu fiskaalregistreerimise suvand ja on võimalik jätkata praeguse kande fiskaalregistreerimisprotsessi. Näiteks võib kohalik fiskaalseade [olla](./latam-bra-cf-e-sat.md#scenario-4-make-a-cash-and-carry-sale-of-goods-by-using-sat-as-contingency-mode) võrgu fiskaalregistreerimise teenuse varundussuvand, kui teenus pole saadaval.
    - Fiskaalregistreerimise saab lõpetada hiljem, mitte fiskaalintegratsiooni raamistiku abil. Näiteks saab edasilükatud kandeid hiljem partiisse eraldi funktsiooni abil finantsiliselt [registreerida](./latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode).
    
    Pärast praeguse kande või sündmuse edasilükkamist saab kassas regulaarseid toiminguid jätkata.

> [!WARNING]
> Suvandeid **Jäta** vahele, **Märgi registreeritud** ja **Edasilükkumise** suvandeid tuleks käsitleda hädaolukorra valikutena ja kasutada ainult erandlikel juhtudel. Arutlege nende tõrgete käsitlemise võimaluste üle oma seadusliku või maksuametiga ja rakendage head käsitlust enne nende lubamist. Suvandid tuleb enne kasutamist fiskaalregistreerimise protsessis aktiveerida. Selleks, et operaatorid ei kasutaks neid regulaarselt, peavad operaatoritele olema antud vastavad load.

Fiskaalkanne luuakse [siis](#storing-fiscal-response-in-fiscal-transaction), kui on valitud suvand Jäta, **·** **Märgi** registreeritud või Lükka edasi, kuid fiskaalkanne ei sisalda fiskaalvastust.**·** See võimaldab teil hõivata fiskaalregistreerimise tõrke sündmuse. Need valikud võimaldavad ka teabekoodidele fikseerida tõrke kohta konkreetset teavet, nt tõrke põhjuseid, või finantsregistreerimise vahelejätmise või kande registreerimise märkimise põhjendust. Lisateavet tõrketöötluse parameetrite seadistamise kohta vt teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Valikuline fiskaalüksuse registreerimine

Fiskaalüksuse registreerimine võib olla kohustuslik mõne toimingu jaoks, aga valikuline teiste jaoks. Näiteks võib kohustuslik olla regulaarsete müükide ja tagastuste fiskaalüksuse registreerimine, aga kliendi deposiitidega seotud toimingute fiskaalüksuse registreerimine võib olla valikuline. Sellisel juhul peaks müügi fiskaalüksuse registreerimise tegemata jätmine keelama edaspidised müügid, kuid kliendi deposiidi fiskaalüksuse registreerimise tegemata jätmine ei tohiks edaspidiseid müüke keelata. Kohustuslike ja valikuliste toimingute eristamiseks soovitame nendega tegeleda läbi eri dokumendipakkujate ning seadistada nende pakkujate jaoks fiskaalüksuse registreerimise protsessis eraldi etapid. Parameeter **Jätka tõrke korral** peab olema lubatud mis tahes etapi jaoks, mis on seotud valikulise fiskaalüksuse registreerimisega. Lisateavet tõrketöötluse parameetrite seadistamise kohta vt teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Käivitage fiskaalregistreerimine käsitsi uuesti

Kui kande või sündmuse fiskaalregistreerimine on pärast nurjumist edasi lükatud (nt kui **tehtemärk** valis tõrke käsitlemise dialoogiboksis tühista), saate finantsregistreerimise käsitsi uuesti käivitada, käivitades vastava toimingu. Lisateavet vt edasilükatud fiskaalregistreerimise [käsitsi käivitamise lubamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).

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
> Seisundi kontroll käivitatakse ainult siis, **kui praegune toiming nõuab fiskaalregistreerimist ja kui fiskaalregistreerimise protsessi praeguse etapi puhul on** tõrke jätkamise parameeter keelatud. Lisateavet leiate teemast [Tõrketöötluse sätete määramine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Fiskaalvastuse talletamine fiskaalkandesse

Kui kande või sündmuse fiskaalüksuse registreerimine õnnestus, luuakse kanali andmebaasi fiskaalkanne ja lingitakse algse kande või sündmusega. Samamoodi, kui **nurjunud** fiskaalregistreerimise **·** **puhul on valitud suvand Jäta,** Märgi kui registreeritud või Edasi lükatud, talletatakse see teave fiskaalkandesse. Fiskaalkandel on fiskaalseadme või -teenuse fiskaalvastutus. Kui fiskaalüksuse registreerimisprotsess koosneb mitmest etapist, luuakse fiskaalkanne protsessi iga etapi kohta, mille tulemuseks on õnnestunud või nurjunud registreerimine.

Fiskaalkanded edastatakse koos kannete ja *P-tööga* peakorterisse. Lehe **Kaupluse kanded** kiirkaardil **Fiskaalkanded** saate vaadata kannetega lingitud fiskaalkandeid.

Fiskaalkanne talletab järgmised üksikasjad.

- Fiskaalüksuse registreerimisprotsessi üksikasjad (protsess, konnektorigrupp, konnektor jne). Samuti talletab see fiskaalseadme seerianumbri väljale **Registrinumber**, kui see teave sisaldub fiskaalvastuses.
- Fiskaalregistreerimise olek: **edukaks registreerimiseks lõpetatud. Jäeti vahele,** **·** **kui operaator valis nurjunud registreerimise jaoks suvandi Jäta vahele. Märgitud registreerituks,** **·** **kui operaator valis suvandi Märgi registreerituks, või lükatakse edasi,** **·** **kui operaator valis suvandi Edasilükkumine.**
- Teabekoodi kanded, mis on seotud valitud fiskaalkandega. Teabekoodi kannete vaatamiseks valige finantskannete kiirkaardil fiskaalkanne, **mille olek on** **Vahele jäetud,** **Märgitud kui registreeritud või** **Edasi lükatud, ja** seejärel valige teabekoodi kanded **.**

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
