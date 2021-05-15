---
title: Kassas (POS) olevad klienditellimused
description: Selles teemas kirjeldatakse kassas (POS) olevaid klienditellimusi. Klienditellimused on teise nimega eritellimused. Teema hõlmab arutelu seotud parameetrite ja kandevoogude kohta.
author: josaw1
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e495ac4f3cc55503cc8b15d4d4640d3468ab7cd2
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936726"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Kassas (POS) olevad klienditellimused

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse kassas (POS) olevate klienditellimuste loomist ja haldamist. Klienditellimusi saab kasutada sellise müügi jäädvustamiseks, mille korral ostjad soovivad tooted hiljem või muust asukohast kätte saada või et kaup tarnitakse neile sobivale aadressile. 

Mitmekanalilises kaubandusmaailmas pakuvad paljud jaemüüjad mitmesuguste toote- ja täitmisnõuete täitmiseks klienditellimuste ehk eritellimuste võimalust. Tüüpilised stsenaariumid on näiteks järgmised.

- Klient soovib tooted kohale toimetada kindlal kuupäeval kindlale aadressile.
- Klient soovib tooted kätte saada teisest poest või asukohast kui see, kust ta tooted ostis.
- Kaupluse asukohas olev klient soovib tooteid tellida juba täna ja need hiljem samast kaupluse asukohast kätte saada.

Jaemüüjad saavad kasutada klienditellimusi ka kaotatud müügi minimeerimiseks, mida laoseisak võib põhjustada, kuna kauba saab tarnida või kätte saada teisel ajal või teises kohas.

## <a name="set-up-customer-orders"></a>Klienditellimuste seadistamine
Enne kui proovite kassas kasutada klienditellimuse funktsioone, veenduge, et olete lõpule viinud kõik vajalikud konfiguratsioonid Commerce'i peakorteris.

### <a name="configure-modes-of-delivery"></a>Tarnerežiimide konfigureerimine

Klienditellimuste kasutamiseks peate konfigureerima tarnerežiimid, mida kauplusekanal saab kasutada. Peate määratlema vähemalt ühe tarnerežiimi, mida saab kasutada tellimuse ridade kliendile kauplusest lähetamisel. Samuti peate määratlema vähemalt ühe järeletulemise tarnerežiimi, mida saab kasutada, kui tellimuse read võetakse vastu kauplusest. Tarnerežiimid on määratletud Commerce'i peakorteri lehel **Tarnerežiimid**. Lisateavet Commerce'i kanali tarnerežiimi seadistamise kohta vaadake teemast [Tarnerežiimide määratlemine](./configure-call-center-delivery.md#define-delivery-modes).

![Tarnerežiimide leht](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Täitmisgruppide häälestamine

Mõned kauplused või lao asukohad ei pruugi olla suutelised täitma klienditellimusi. Täitmisgruppide konfigureerimisega saab organisatsioon määrata, millised kauplused ja laod kuvatakse valikutena kasutajatele, kes loovad klienditellimusi kassas. Täitmisgrupid konfigureeritakse lehel **Täitmisgrupid**. Organisatsioonid saavad luua nii palju täitmisgruppe kui vaja. Pärast täitmisgrupi määratlemist linkige see kauplusega, valides lehe **Kauplused** tegevuspaani vahekaardil **Seadistus** suvandi **Täitmisgrupi määramine**.

Commerce'i versioonis 10.0.12 ja uuemates versioonides saavad ettevõtted määratleda, kas täitmisgruppides määratletud lao- või lao/kaupluse kombinatsioone saab kasutada lähetamiseks, järeletulemiseks või mõlema jaoks. See võimaldab ettevõttel paindlikumalt määrata, milliseid ladusid saab valida, kui luuakse klienditellimus lähetatavatele kaupadele, või millised kauplusi saab valida, kui luuakse klienditellimus järeletulemisega kaupadele. Nende konfiguratsioonisuvandite kasutamiseks lülitage funktsioon **Võimalus määrata asukohti nii, et olek Lähetamine või Järeletulemine on täitmisgrupis lubatud** sisse. Kui täitmisgrupiga lingitud ladu pole kauplus, saab seda konfigureerida ainult lähetuse asukohana. Seda ei saa kasutada, kui järeletulemisega tellimused on konfigureeritud kassas.

![Täitmisgruppide leht](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanalisätete konfigureerimine

Kui töötate klienditellimustega kassas, peate arvestama kauplusekanali teatud sätetega. Need sätted leiate Commerce'i peakontori lehelt **Kauplused**.

- **Ladu** – see väli näitab ladu, mida kasutatakse selle kauplusega seotud sularaha ja kaupade ning kliendiga komplekteeritud tellimuste laovarude arvestamisel. Soovitame seetõttu kasutada kordumatuid ladusid iga kaupluse kanali jaoks, et vältida kaupluste vahel vastuolulisi äriloogika probleeme.
- **Lähetamise ladu** – see väli näitab ladu, mida kasutatakse selle valitud kauplusesse lähetatud ja seotud kliendi komplekteeritud tellimuste laovarude arvestamisel. Kui funktsioon **Oskus määrata asukohti kui "Lähetamine" või "Vastuvõtt" on täitmisgrupis** on teie keskkonnas lubatud, saavad müügikoha kasutajad valida kindla lao, millelt kassas lähetada, selle asemel et valida kauplus, millest lähetada. Seega, kui see funktsioon on lubatud, ei kasutata enam saatmisladu, kuna kasutaja valib konkreetse lao tellimuse lähetamiseks tellimuse loomisel.
- **Täitmisgrupi määramine** – valige see nupp (tegevuspaani vahekaardil **Häälestamine**), et linkida täitmisgrupid, millele viidatakse, et kuvada järeletulemise asukohtade või lähetuse päritolu sätted, kui klienditellimused luuakse kassas.
- **Kasuta sihtkohapõhist maksu** – see suvand näitab, kas lähetusaadressi kasutatakse kliendi aadressile lähetatavate tellimuse ridadele rakendatava maksugrupi määratlemiseks.
- **Kasuta kliendipõhist maksu** – see suvand näitab, kas kliendi tarneaadressi jaoks määratletud maksugruppi kasutatakse kliendi nende tellimuste maksustamiseks, mis on loodud kassas kliendile koju saatmiseks.

![Kauplusekanali häälestamine lehel Kauplused](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Klienditellimuse parameetrite seadistamine

Enne kui proovite luua klienditellimusi kassas, peate konfigureerima vastavad parameetrid Commerce'i peakorteris. Need parameetrid leiate lehe **Kaubanduse parameetrid** vahekaardilt **Klienditellimused**.

- **Vaiketellimuse tüüp** – saate määrata tellimuse tüübi, mis määratakse vaikimisi kassas loodud klienditellimustele. Need klienditellimused võivad olla kas müügitellimused või pakkumise tellimused. Sõltumata tellimuse vaiketüübist saavad kasutajad luua kassas nii müügitellimusi kui ka klienditellimusi.
- **Deposiidi vaikeprotsent** – saate määrata tellimuse kogusumma protsendi, mille klient peab enne tellimuse kinnitamist deposiidina tasuma. Kaupluse töötajad võivad sõltuvalt oma õigustest alistada summa kassa suvandi **Deposit alistamine** abil, kui see suvand on konfigureeritud kandekuva paigutuse jaoks.
- **Järeletulemise tarnerežiim** – saate määrata tarnerežiimi, mida tuleks rakendada müügitellimuse ridadele, mis on konfigureeritud kassas järeletulemiseks.
- **Järeletulemise tarnerežiim** – Saate määrata tarnerežiimi, mida tuleks rakendada müügitellimuse ridadele, mida käsitletakse väljaminekuorderi ridadena kombineeritud ostukorvi loomisel, mille korral mõned read lähetatakse ja ülejäänud ridadele tuleb klient kohe järele.
- **Tühistamistasu protsent** – saate määrata klienditellimuse tühistamisel rakendatava tasu summa.
- **Tühistamistasu kood** – saate määrata Müügireskontro tasu koodi, mida tuleks kasutada tühistamistasu rakendamisel tühistatud klienditellimustele kassa kaudu. Tasu kood määratleb tühistamistasu finantssisestuse loogika.
- **Saatekulude kood** – kui suvandi **Kasuta täpsemaid automaatseid kulusid** väärtuseks on seatud **Jah**, siis see parameetrisäte ei toimi. Kui selle suvandi väärtuseks on seatud **Ei**, palutakse kasutajatel sisestada lähetuse tasu käsitsi, kui nad loovad klienditellimusi kassa kaudu. Selle parameetri abil saate vastendada Müügireskontro tasu koodi, mis rakendatakse tellimustele, kui kasutajad sisestavad lähetamise tasu. Tasu kood määratleb lähetamise tasu finantssisestuse loogika.
- **Kasuta täpsemaid automaatseid kulusid** – saate seada selle suvandi väärtuseks **Jah**, et kasutada süsteemi arvutatud automaatseid tasusid klienditellimuste kassas loomisel. Neid automaatseid tasusid saab kasutada lähetamise tasude või muude tellimuse- või kaubapõhiste tasude arvutamiseks. Lisateabe saamiseks täpsemate automaatsete tasude seadistamise ja kasutamise kohta leiate teemast [Omnikanali täpsemad automaatsed tasud](./omni-auto-charges.md).

![Klienditellimuste vahekaart lehel Kaubanduse parameetrid](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Kandekuva paigutuste värskendamine kassas

Veenduge, et kassa [ekraani paigutus](./pos-screen-layouts.md) oleks konfigureeritud toetama klienditellimuste loomist ja haldamist ning et kõik nõutavad kassatoimingud oleksid konfigureeritud. Siin on mõned kassatoimingud, mida on soovitatav klienditellimuse loomise ja haldamise õigeks toetamiseks teha.
- **Läheta kõik tooted** – selle suvandi abil saate määrata, et kande ostukorvi kõik read saadetakse sihtkohta.
- **Läheta valitud tooted** – selle suvandi abil saate määrata, et kande ostukorvi valitud read saadetakse sihtkohta.
- **Tule kõigile toodetele järele** – selle suvandi abil saate määrata, et kande ostukorvi kõigile ridadele tullakse järele valitud kaupluse asukohta.
- **Tule valitud toodetele järele** – selle suvandi abil saate määrata, et kande ostukorvi valitud ridadele tullakse järele valitud kaupluse asukohta.
- **Kõik tooted on järeletulemisega** – selle suvandi abil saate määrata, et kande ostukorvi kõigile ridadele tuleb klient järele. Kui seda toimingut kasutatakse kassas, teisendatakse klienditellimus sularaha- ja vedamiskandeks.
- **Valitud tooted on järeletulemisega** – selle suvandi abil saate määrata, et kande ostukorvi valitud ridadele tuleb klient järele ostu sooritamisel. See suvand on kasulik ainult [hübriid-tellimuse](./hybrid-customer-orders.md) korral.
- **Tellimuse tagasikutsumine** – seda suvandit kasutatakse klienditellimuste otsimiseks ja toomiseks, et kassa kasutajad saaksid neid vastavalt vajadusele redigeerida või tühistada või teostada täitmisega seotud toiminguid.
- **Muutke kassas tarneviisi** – seda suvandit saab kasutada juba saadetiseks konfigureeritud ridade tarnerežiimi kiireks muutmiseks ilma, et kasutajad peaksid läbima uuesti voo „Läheta kõik tooted” või „Läheta valitud tooted”.
- **Deposiidi alistamine** – selle suvandi abil saab muuta deposiidi summat, mille klient maksab valitud klienditellimuse eest.

![Kassa kandekuva suvandid](media/customer-order-screen-layout.png)

## <a name="work-with-customer-orders-in-pos"></a>Kassas klienditellimustega töötamine

> [!NOTE]
> Tulu tuvastamise funktsiooni ei toetata praegu Commerce'i kanalites (e-kaubandus, kassa, kõnekeskus). Tulu tuvastamisega konfigureeritud kaupu ei tohiks lisada Commerce'i kanalites loodud tellimustele. 

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Klienditellimuse loomine kliendile saadetavate toodete kohta

1. Kassa kandekuval saate lisada kliendi kandele.
2. Lisage tooted ostukorvi.
3. Valige **Läheta valitud** või **Läheta kõik**, et lähetada tooted kliendikontol esitatud aadressile.
4. Valige see suvand klienditellimuse loomiseks.
5. Kinnitage „lähetamise” asukoht või muutke seda, kinnitage tarneaadress või muutke seda ja valige saatmisviis.
6. Sisestage kliendi soovitud tellimuse lähetuskuupäev.
7. Tasuge kõigi tasumisele kuuluvate arvutatud summade eest maksefunktsioonide abil või kasutage tasumisele kuuluvate summade muutmiseks suvandit **Deposiidi alistamine** ja seejärel rakendage makse.
8. Kui tellimuse kogusummat ei makstud, sisestage krediitkaart, millelt võetakse tellimuse eest tasumisele kuuluv saldo pärast selle arveldamist.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Klienditellimuse loomine kliendi järeletulemisega toodete kohta

1. Kassa kandekuval saate lisada kliendi kandele.
2. Lisage tooted ostukorvi.
3. Tellimuse järeletulemise konfigureerimise alustamiseks valige **Tule valitutele järele** või **Tule kõigile järele**.
4. Valige kaupluse asukoht, kuhu klient tuleb valitud toodetele järgi.
5. Valige kaubale järeletulemise kuupäev.
6. Tasuge kõigi tasumisele kuuluvate arvutatud summade eest maksefunktsioonide abil või kasutage tasumisele kuuluvate summade muutmiseks suvandit **Deposiidi alistamine** ja seejärel rakendage makse.
7. Kui tellimuse kogusummat ei makstud, valige, kas klient teeb makse hiljem (järeletulemisel) või kas krediitkaardile luuakse praegu luba ning seda kasutatakse järeletulemise ajal.

### <a name="edit-an-existing-customer-order"></a>Olemasoleva klienditellimuse redigeerimine

Võrgu- või kauplusekanalis loodud jaemüügitellimusi saab vastavalt vajadusele kassa kaudu tagasi kutsuda ja redigeerida.

> [!IMPORTANT]
> Kõiki jaemüügitellimusi ei saa kassa rakenduse kaudu redigeerida. Kõnekeskuse kanalis loodud tellimusi ei saa kassas redigeerida, kui kõnekeskuse kanali jaoks on sisse lülitatud säte [Tellimuse lõpetamise lubamine](./set-up-order-processing-options.md#enable-order-completion). Korrektseks maksete töötlemise tagamiseks tuleb kõnekeskuse kanalist pärinevaid tellimusi, mis kasutavad funktsiooni Tellimuse lõpetamise lubamine, redigeerida kõnekeskuse rakenduse kaudu Commerce'i peakontoris.

Versioonis 10.0.17 ja uuemates versioonides saavad kasutajad kassa rakenduse kaudu sobilikke tellimusi redigeerida, isegi kui tellimus on osaliselt täidetud. Täielikult arveldatud tellimusi ei saa siiski kassa kaudu redigeerida. Selle võimaluse lubamiseks lülitage tööruumis **Funktsioonihaldus** sisse funktsioon **Osaliselt täidetud tellimuste redigeerimine kassas**. Kui see funktsioon ei ole lubatud või kui kasutate versiooni 10.0.16 või varasemat versiooni, saavad kasutajad kassas klienditellimusi redigeerida ainult siis, kui tellimus on täielikult avatud. Peale selle, kui see funktsioon on lubatud, saate piirata, millised kauplused saavad osaliselt täidetud tellimusi redigeerida. Suvandit selle võimaluse keelamiseks konkreetsete kaupluste puhul saab konfigureerida kiirkaardi **Üldine** jaotise **Funktsiooniprofiil** kaudu.


1. Valige **Tellimuse tagasikutsumine**.
2. Selleks et leida tellimust kasutage filtrite sisestamiseks **Otsingut** ja seejärel valige **Rakenda**.
3. Valige tulemuste loendis tellimus ja seejärel valige **Redigeeri**. Kui nupp **Redigeeri** pole saadaval, on tellimusel olek, mille korral ei saa seda redigeerida.
4. Tehke kõik vajalikud klienditellimuse muudatused kande ostukorvis. Mõned muudatused võivad olla redigeerimise ajal keelatud.
5. Viige redigeerimisprotsess lõpule, valides maksmissuvandi.
6. Redigeerimisprotsessist väljumiseks muudatusi salvestamata saate kasutada suvandit **Tühista kanne**.



### <a name="cancel-a-customer-order"></a>Klienditellimuse tühistamine

1. Valige **Tellimuse tagasikutsumine**.
2. Selleks et leida tellimust kasutage filtrite sisestamiseks **Otsingut** ja seejärel valige **Rakenda**.
3. Valige tulemuste loendis tellimus ja seejärel valige **Tühista**. Kui nupp **Tühista** pole saadaval, on tellimusel olek, mille korral ei saa seda enam tühistada.
4. Kui tühistamistasud on konfigureeritud, kinnitage need. Tühistamistasusid saate korrigeerida enne nende kinnitamist vastavalt vajadusele. 
5. Viige tühistamisprotsess lõpule ostukorvi kaudu, valides maksesuvandi. Kui makstud deposiidid ületavad tühistamistasu, võivad tagasimaksed kuuluda tasumisele.
6. Tühistamisprotsessist väljumiseks muudatusi salvestamata saate kasutada suvandit **Tühista kanne**.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Lähetamise või järeletulemisega klienditellimuse töötlemise lõpuleviimine kassa kaudu

Pärast tellimuse loomist saab klient kaubad kätte kaupluse asukohast või need lähetatakse sõltuvalt tellimuse konfiguratsioonist. Selle protsessi kohta lisateabe saamiseks vt [kaupluse tellimuse täitmise](./order-fulfillment-overview.md)dokumentatsiooni.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Klienditellimuste asünkroonne kannetevoog

Klienditellimus saab luua kassa kaudu kas sünkroonses režiimis või asünkroonses režiimis. Kui märkate jõudlusprobleeme või hilinemisi kassas klienditellimuste loomisel, kaaluge asünkroonse tellimuse loomise sisselülitamist.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Klienditellimuste asünkroonses režiimis loomise lubamine

1. Valige Commerce'i peakorteris lehel **Funktsiooniprofiilid** funktsiooniprofiil, mis vastab kauplusele, mida soovite konfigureerida.
2. Määrake kiirkaardil **Üldine** valiku **Klienditellimuse loomine asünkroonses režiimis** sätteks **Jah**.

Kui suvandi **Klienditellimuse loomine asünkroonses režiimis** sätteks on valitud **Jah**, luuakse klienditellimused alati asünkroonses režiimis, isegi kui Retail Transaction Service (RTS) on saadaval. Kui määrate valiku sätteks **Ei**, luuakse klienditellimused alati sünkroonses režiimis, kasutades RTS-i. Kui klienditellimused luuakse asünkroonses režiimis, tuuakse ja luuakse need jaemüügikannetena Commerce'i peakorteris Commerce Pulli (P) töödest. Jaemüügikannete vastavad müügitellimused luuakse, kui käsk **Sünkrooni tellimused** käivitatakse käsitsi või pakktöötluse kaudu.

## <a name="additional-resources"></a>Lisaressursid

[Hübriidkliendi tellimused](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]