---
title: Kassas (POS) olevad klienditellimused
description: Selles teemas kirjeldatakse kassas (POS) olevaid klienditellimusi. Klienditellimused on teise nimega eritellimused. Teema hõlmab arutelu seotud parameetrite ja kandevoogude kohta.
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9e5770de82638e6cef6d4c1dffd1dc85549fb11f
ms.sourcegitcommit: 30e4dc0a45f7de5f0a7178b1e88f7c3d61a7395e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763697"
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

Klienditellimuste kasutamiseks peate konfigureerima tarnerežiimid, mida kauplusekanal saab kasutada. Peate määratlema vähemalt ühe tarnerežiimi, mida saab kasutada tellimuse ridade kliendile kauplusest lähetamisel. Samuti peate määratlema vähemalt ühe järeletulemise tarnerežiimi, mida saab kasutada, kui tellimuse read võetakse vastu kauplusest. Tarnerežiimid on määratletud Commerce'i peakorteri lehel **Tarnerežiimid**. Lisateavet Commerce'i kanali tarnerežiimi seadistamise kohta vaadake teemast [Tarnerežiimide määratlemine](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Tarnerežiimide leht](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Täitmisgruppide häälestamine

Mõned kauplused või lao asukohad ei pruugi olla suutelised täitma klienditellimusi. Täitmisgruppide konfigureerimisega saab organisatsioon määrata, millised kauplused ja laod kuvatakse valikutena kasutajatele, kes loovad klienditellimusi kassas. Täitmisgrupid konfigureeritakse lehel **Täitmisgrupid**. Organisatsioonid saavad luua nii palju täitmisgruppe kui vaja. Pärast täitmisgrupi määratlemist lingitakse see kauplusega lehe **Kauplused** tegevuspaani vahekaardil **Häälestamine** oleva nupu abil.

Commerce'i versioonis 10.0.12 ja uuemates versioonides saavad ettevõtted määratleda, kas täitmisgruppides määratletud lao- või lao/kaupluse kombinatsioone saab kasutada lähetamiseks, järeletulemiseks või mõlema jaoks. Seetõttu on kauplusel täiendav paindlikkus juhtida lao- ja kauplusesuvandeid, mis kuvatakse kasutajatele, kes loovad järeletulemisega tellimuse, võrreldes lähetatava tellimusega. Nende konfiguratsioonisuvandite kasutamiseks peate funktsiooni **Võimalus määrata asukohti nii, et olek Lähetamine või Järeletulemine on täitmisgrupis lubatud** sisse lülitama. Kui täitmisgrupiga lingitud ladu pole kauplus, saab seda konfigureerida ainult lähetuse asukohana. Seda ei saa kasutada, kui järeletulemisega tellimused on konfigureeritud kassas.

![Täitmisgruppide leht](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanalisätete konfigureerimine

Kui töötate klienditellimustega kassas, peate arvestama kauplusekanali teatud sätetega. Need sätted leiate Commerce'i peakontori lehelt **Kauplused**.

- **Ladu** – see väli kuvab ladu, mida kasutatakse kauplusest saatmiseks konfigureeritud tellimuste täitmiseks.
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
- **Kasuta täpsemaid automaatseid kulusid** – saate seada selle suvandi väärtuseks **Jah**, et kasutada süsteemi arvutatud automaatseid tasusid klienditellimuste kassas loomisel. Neid automaatseid tasusid saab kasutada lähetamise tasude või muude tellimuse- või kaubapõhiste tasude arvutamiseks. Lisateabe saamiseks täpsemate automaatsete tasude seadistamise ja kasutamise kohta leiate teemast [Omnikanali täpsemad automaatsed tasud](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Klienditellimuste vahekaart lehel Kaubanduse parameetrid](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Kandekuva paigutuste värskendamine kassas

Veenduge, et kassa [ekraani paigutus](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) oleks konfigureeritud toetama klienditellimuste loomist ja haldamist ning et kõik nõutavad kassatoimingud oleksid konfigureeritud. Siin on mõned kassatoimingud, mida on soovitatav klienditellimuse loomise ja haldamise õigeks toetamiseks teha.
- **Läheta kõik tooted** – selle suvandi abil saate määrata, et kande ostukorvi kõik read saadetakse sihtkohta.
- **Läheta valitud tooted** – selle suvandi abil saate määrata, et kande ostukorvi valitud read saadetakse sihtkohta.
- **Tule kõigile toodetele järele** – selle suvandi abil saate määrata, et kande ostukorvi kõigile ridadele tullakse järele valitud kaupluse asukohta.
- **Tule valitud toodetele järele** – selle suvandi abil saate määrata, et kande ostukorvi valitud ridadele tullakse järele valitud kaupluse asukohta.
- **Kõik tooted on järeletulemisega** – selle suvandi abil saate määrata, et kande ostukorvi kõigile ridadele tuleb klient järele. Kui seda toimingut kasutatakse kassas, teisendatakse klienditellimus sularaha- ja vedamiskandeks.
- **Valitud tooted on järeletulemisega** – selle suvandi abil saate määrata, et kande ostukorvi valitud ridadele tuleb klient järele ostu sooritamisel. See suvand on kasulik ainult [hübriid-tellimuse](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders) korral.
- **Tellimuse tagasikutsumine** – seda suvandit kasutatakse klienditellimuste otsimiseks ja toomiseks, et kassa kasutajad saaksid neid vastavalt vajadusele redigeerida või tühistada või teostada täitmisega seotud toiminguid.
- **Muutke kassas tarneviisi** – seda suvandit saab kasutada juba saadetiseks konfigureeritud ridade tarnerežiimi kiireks muutmiseks ilma, et kasutajad peaksid läbima uuesti voo „Läheta kõik tooted” või „Läheta valitud tooted”.
- **Deposiidi alistamine** – selle suvandi abil saab muuta deposiidi summat, mille klient maksab valitud klienditellimuse eest.

![Kassa kandekuva suvandid](media/customer-order-screen-layout.png)

## <a name="working-with-customer-orders-in-pos"></a>Klienditellimustega töötamine kassas

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
5. Saate valida järeletulemise kuupäeva.
6. Tasuge kõigi tasumisele kuuluvate arvutatud summade eest maksefunktsioonide abil või kasutage tasumisele kuuluvate summade muutmiseks suvandit **Deposiidi alistamine** ja seejärel rakendage makse.
7. Kui tellimuse kogusummat ei makstud, valige, kas klient teeb makse hiljem (järeletulemisel) või kas krediitkaardile luuakse praegu luba ning seda kasutatakse järeletulemise ajal.

### <a name="edit-an-existing-customer-order"></a>Olemasoleva klienditellimuse redigeerimine

Võrgu- või kauplusekanalis loodud jaemüügitellimusi saab vastavalt vajadusele kassa kaudu tagasi kutsuda ja redigeerida.

> [!IMPORTANT]
> Kõnekeskuse kanalis loodud tellimusi ei saa kassas redigeerida, kui kõnekeskuse kanali jaoks on sisse lülitatud säte [Tellimuse lõpetamise lubamine](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion). Korrektseks maksete töötlemise tagamiseks tuleb kõnekeskuse kanalist pärinevaid tellimusi, mis kasutavad funktsiooni Tellimuse lõpetamise lubamine, redigeerida kõnekeskuse rakenduse kaudu Commerce'i peakontoris.

Commerce'i versiooni 10.0.13 ja varasemate versioonide korral saavad kasutajad redigeerida toetatud klienditellimusi kassa kaudu ainult siis, kui tellimused on täielikult avatud. Kui tellimuse ridu on juba täitmiseks töödeldud (komplekteerimine, pakkimine jne), lukustatakse tellimus, et seda ei saaks kassas redigeerida.

> [!NOTE]
> Commerce'i versiooni 10.0.14 funktsioon, mis on saadaval [avaliku eelversioonina](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms), võimaldab kassa kasutajatel redigeerida klienditellimusi kassa kaudu, isegi kui osa tellimusest on juba täidetud. Täielikult arveldatud tellimusi ei saa siiski kassa kaudu redigeerida. Selle eelversiooni funktsiooni testimiseks ja täiendava tagasiside esitamiseks lülitage asukohas **Funktsioonihaldus** sisse funktsioon **(Eelversioon) Osaliselt täidetud tellimuste redigeerimine kassas**. Kõnekeskuse kanalist pärinevaid ja funktsiooni Tellimuse lõpetamise lubamine kasutavaid klienditellimusi ei saa redigeerida isegi pärast selle funktsiooni lubamist.

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

Pärast tellimuse loomist saab klient kaubad kätte kaupluse asukohast või need lähetatakse sõltuvalt tellimuse konfiguratsioonist. Selle protsessi kohta lisateabe saamiseks vt [kaupluse tellimuse täitmise](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview)dokumentatsiooni.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Klienditellimuste asünkroonne kannetevoog

Klienditellimus saab luua kassa kaudu kas sünkroonses režiimis või asünkroonses režiimis. Kui märkate jõudlusprobleeme või hilinemisi kassas klienditellimuste loomisel, kaaluge asünkroonse tellimuse loomise sisselülitamist.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Klienditellimuste asünkroonses režiimis loomise lubamine

1. Valige Commerce'i peakorteris lehel **Funktsiooniprofiilid** funktsiooniprofiil, mis vastab kauplusele, mida soovite konfigureerida.
2. Määrake kiirkaardil **Üldine** valiku **Klienditellimuse loomine asünkroonses režiimis** sätteks **Jah**.

Kui suvandi **Klienditellimuse loomine asünkroonses režiimis** sätteks on valitud **Jah**, luuakse klienditellimused alati asünkroonses režiimis, isegi kui Retail Transaction Service (RTS) on saadaval. Kui määrate valiku sätteks **Ei**, luuakse klienditellimused alati sünkroonses režiimis, kasutades RTS-i. Kui klienditellimused luuakse asünkroonses režiimis, tuuakse ja luuakse need jaemüügikannetena Commerce'i peakorteris Commerce Pulli (P) töödest. Jaemüügikannete vastavad müügitellimused luuakse, kui käsk **Sünkrooni tellimused** käivitatakse käsitsi või pakktöötluse kaudu.

## <a name="additional-resources"></a>Lisaressursid

[Hübriidkliendi tellimused](hybrid-customer-orders.md)
