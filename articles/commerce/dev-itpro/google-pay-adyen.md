---
title: Saate konfigureerida Oma tasu koos Mileeniga.
description: See artikkel kirjeldab, kuidas konfigureerida Rakenduste palka koos Chromeeniga moodulis Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115012"
---
# <a name="configure-google-pay-with-adyen"></a>Saate konfigureerida Oma tasu koos Mileeniga.

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas konfigureerida Rakenduste palka koos Chromeeniga moodulis Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce Rakendus <a0/& pakub Väljale Pay integratsiooni, kui kasutatakse Portaali makselüüsiteenust. The Pay on digitaalse maksmise maksmise meetod, mis kasutabSumma kaupmehekontot Makseteenusega Naisele. Kui see on konfigureeritud, on nupp The Pay saadaval valitava makseviisina võrgutellimuse väljaregistreerimise ajal. Kui kasutajad valivad **Tagasimakstavates brauserites või seadmetes,** suunatakse nad oma makse otse Pay teenusega lõpule viima. Seejärel tagastatakse need tellimuse lõpetamiseks võrgupoes.

Kui Ärimoodulis kasutatakse Hinnaaland Payi kiirväljaregistreerimise mooduliga, täidetakse kasutaja maksekonto teave automaatselt väljaregistreerimise vormis, et aidata kasutajal läbida väljaregistreerimise protsess kiiremini. Commerce sisaldab kiirregistreerimise käitumist lubav kiirmakse kiirmoodulit. Makse väljendamise moodulit saab kasutada tükis, mis on kaasatud väljaregistreerimise või ostukorvi lehele. Viite Dynamics 365 Payment Connector for The Pay Connector kasutatakse lisaks Dynamics 365 Makseühendusele Puhvrile Puhvrile, et lubada nii kiirmakse kui ka tavalise väljaregistreerimise suvandid, kui PayPal konfigureeritakse. Ladu Pay saab konfigureerida ka Portaali makseterminalide ja kaupluses kasutamiseks commerce'i kassaga.

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| Kalendripalk | Seda nimetatakse ka Button Pay 'button'iks', Hinnaaland Pay on Puhvri kaudu toetatav maksete pakkumine. See võimaldab kliendikogemust ja integreerimist, mida Dynamics Connector Toetab Dynamics Portaali Pay Connector. |
| Rahakott | Maksetüüp, mis ei sisalda traditsioonilisi makse omadusi nt panga ID-koodi (BIN) vahemikku ja aegumiskuupäeva, mida kasutatakse krediit- ja deebetkaardi tüüpide eristamiseks. |
| Kiirmakse moodul | Moodul Dynamics 365 Commerce, mis toetab toetatud makseviisidega kiiremat väljaregistreerimise käitumist. |

## <a name="prerequisites"></a>Eeltingimused

Kasutades Rakenduste palka koos Mileeniga äris, on vaja Merchanti kontot. Teavet selle kohta, kuidas oma Merchanti konto seadistada, [vt Enammaksmise dokumentatsiooniSt The Pay](https://docs.adyen.com/payment-methods/google-pay/) ja Merchanti integratsiooni kontroll-loendis [...](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist).

MaksemeetodLülitus Pay tuleb integreerida ka teie Lülituse kontoga. Integratsioonilingi juhiseid vt [Enamast Kui Logi pay'st](https://www.adyen.com/payment-methods/google-pay).

Samuti peate lubama peakontoris täiustatud Dynamics 365 Commerce funktsiooni. Minge tööruumide funktsioonihaldusesse, otsige täiustatud hinnaalandi **\> toe ja maksete parendusfunktsiooni, valige funktsioon ja seejärel valige luba** **.** **·** Kui funktsioon on lubatud, käivitage **1110 jaotusgraafik**, et teha muudatus kättesaadavaks kõikides kanalites.

## <a name="map-the-google-pay-payment-method"></a>Saate vastendada Maksete makseviisi Vastendamine

Summa maksmine on digitaalse maksmise meetod. Lisateavet maksete vastendamise häälestamise kohtaKriteeriumi Pay jaoks vt Makseteenuse toe [kontolt](../wallets.md).

Nii kassa- kui võrgukanalite kaardipõhise maksevahendi tüüpide vastendamiseks järgige neid samme.

1. Minge Commerce Headquartersi jaemüügi ja ärikanali **häälestuse \> maksemeetodite \> kaarditüüpidele \>**.
1. Valige **Uus**, et lisada rida soovitud Pay'i jaoks.
1. **Väljale ID** sisestageAaaa **·**.
1. Väljale Elektroonilise **makse nimi sisestage** TheMay **Pay**.
1. Väljale Tüüp **sisestage** Sisesta **Sisesta**.
1. Väljale Väljastaja **sisestage** **Sisesta.**
1. Tegevuspaanil valige Protsessori vastendamine **,** et avada protsessori **makse vastendamise** meetodite dialoogiboks.
1. Vastendamata **protsessori makseviiside** all näete vastendamata protsessori maksemeetodite loendit, millest igaüks on ühendatud sobiva ühendusega. Vastendamata Pay Pay protsessori makseviiside kaardiga maksevahendi tüüpidega vastendamiseks järgige iga kaardi maksevahendi tüübi puhul neid samme.

    1. Valige **valiku Kaardi maksevahendi** tüübid kaardi maksevahendi tüüp.
    1. **Veerus Vastendamata protsessori makseviisid** **valige nii Dynamics 365 Payment Connector Sumeni** konnektori jaoks (kassas kasutamiseks) **kui ka Dynamics 365 Payment Connector Pay** Connectori jaoks (kasutamiseks võrgukanalites).
    1. Valige **Lisa**. Valikud lisatakse veergu Vastendatud **protsessori makseviisid**.

1. Kui olete makseviiside vastendamise lõpetanud, valige käsk **Salvesta**.
1. Valige lehel **Kaarditüübid** suvand **Salvesta**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Commerce'i e-poe konfigureerimine Commerce Payi jaoks

Commerce'i e-poe konfigureerimiseks Selleks, et kasutada Maksja Pay'i, järgige neid samme.

1. Minge commerce headquartersi kaupluse ja ärikanalite **võrgupoodidesse \>\>**.
1. Valige oma saidi võrgupoe kanal, valides kanali jaemüügikanali **ID** väärtuse.
1. Kinnitage **maksekontode** kiirkaardil konnektori **all** **, et Dynamics 365 Maksekonnektor Puhvri** jaoks on loendis. Kui see ei ole loendis, järgige [lisamiseks Dynamics 365 Payment Connectori häälestamise Puhvrit](adyen-connector-setup.md).

    > [!NOTE]
    > Enamasti peab **Dynamics 365 Payment Connector for Puhvri** konnektor olema nimetatud teie kanali esimese konnektorina (esmast konnektorit nimetatakse ka esmaseks ühenduseks). Seejärel peavad sellele järgnema muud kasutatavad ühendused, **nagu Dynamics 365 Payment Connector PayPal** **jaoks ja Dynamics 365 Payment Connector For The Connectori Ja DynamicsPay** connectori jaoks.

1. **Kui Dynamics 365 makseühendus Puhvri** jaoks on lisatud, **valige Suvand Lisa** **, et lisada Dynamics 365 makseühendus Aaaa ühendusele**. Seejärel seadke konnektorile järgmised atribuudid.

    | Väli                  | Kirjeldus | Nõutav | Automaatselt seadistatud | Näidisväärtus |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Assembleri nimi          | Dynamics 365 Payment Connectori Assembleri nimiEldaPay jaoks. | Jah | Jah | *Binaarnimi* |
    | Teenusekonto ID     | Kaupmehe atribuutide seadistuse kordumatu ID. See identifikaator on tembeldatud maksekannetele ja tuvastab kaupmehe atribuudid, mida allavoolu protsessid (nt arveldamine) peavad kasutama. | Jah | Jah | *GUID* |
    | Merchanti ID     | Sisestage Teie Merchanti kontole määratud Merchanti ID. See atribuut on nõutav tootmiskeskkondades, kuid on katsekeskkonnale valikuline. Lisateabe saamiseks külastage .<https://pay.google.com/> | Jah | Nr | *Numbriline ID* |
    | Kaupmehe konto ID    | Sisestage kordumatu Diagramm kaupmehe identifikaator. See väärtus esitatakse siis, kui registreerite end Omaen-lepingu alusel sisse, nagu on kirjeldatud [jaotises Nendesse registreerumine](adyen-connector-setup.md#sign-up-with-adyen). | Jah | Nr | *Kaupmehe ID* |
    | Pilve API võti          | Sisestage Sisselöödetud pilve API võti. Selle võtme hankimiseks järgige API võtme [hankimise juhiseid](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Jah | Nr | "abcdefg" |
    | Portaali keskkond    | Portaal Portaalkeskkond, millega vastendada. Võimalikud väärtused on Katse **ja** Reaalajas **·**. Määrake selle välja väärtuseks Live **ainult** tootmisseadmete ja kannete puhul. | Jah | Jah | "Reaalajas" |
    | Toetatud valuutad   | Valuutad, mida konnektor peaks töötlema. Kaardi praegusi stsenaariumedes saab Prognoos toetada täiendavaid valuutasid dünaamilise [valuutateisenduse](https://www.adyen.com/pos-payments/dynamic-currency-conversion) kaudu pärast kande taotluse saatmist makseterminali. Toetatud valuutade loendi saamiseks pöörduge Oma Omatoe poole. | Jah | Jah | "USD; Summa (eur) |
    | Toetatud maksevahendi tüübid | Maksevahendi tüübid, mida ühendus peaks töötlema. | Jah | Jah | JadyPay |

1. Pärast konnektori atribuutide häälestamise lõpetamist käivitage **1070 -** jaotusgraafiku töö.

## <a name="configure-commerce-pos-for-google-pay"></a>Commerce POS-i konfigureerimine Pay'i jaoks

Müügikoha konfiguratsioon kasutab riistvaraprofiili EFT-teenuse **välja** sätet Dynamics 365 Payment Connectori jaoks Puhvrile. Teavet selle kohta, kuidas konfigureerida elektroonilise ülekande (EFT) teenust Dynamics 365 Payment Connectori jaoks Puhvrile Commerce headquartersis, [vt Dynamics 365 müügikoha riistvaraprofiili sektsiooni seadistamine](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Puhvri vastendamine Puhvri konnektori jaoks fikseerib kaarditüübid, midaRegistri tasu kassaterminalis kasutab.

### <a name="use-the-payment-express-module-with-google-pay"></a>Kasuta Maksete väljendamise moodulit KoosMoodiga Pay

Commerce Payment Expressi moodul töötab toetavate makseviisitega, et anda saitide klientidele võimalus väljaregistreerida kiiremini, kasutades väljaregistreerimise protsessi ajal nende makseteenuse kontoteavet. Makse väljendamise moodul viitab konfigureeritud konnektori nupule ja tagastab kasutaja valitud tellimuse üksikasjad (aadress, kontaktteave ja makseviis) väljaregistreerimise vormi eeltäitmiseks.

Kui maksete väljendamise moodulit kasutatakse koosMoodul Pay'iga, siis kui kliendid klõpsavad jaotises Payment Express nuppuTool **Pay**, avaneb Window iframe' iframe. Kasutajad saavad siis oma Kontosse sisse logida, et kasutada kande eest maksmiseks oma konto lähetusaadressi, arveaadressi, meiliaadressi jaArvestusmaksemeetodit.

Kui kasutajad lõpetavad toimingu Window The Pay's, suunatakse nad Commerce'i saidi väljaregistreerimise lehele, kus väljaregistreerimise vorm täidetakse eelnevalt oma Konto üksikasjadega. Kui kasutajad pöörduvad tagasi Väljaregistreerimise lehele AknaLtUdu palk, näete järgmisi üksikasju:

- Makse kiirvoos valitakse kliendi jaoks esimene tagastatud lähetusaadressi jaoks saadav tarnevalik.
- Kui kasutatakse Ettevõtte tasu, ei tagastata kontakti e-posti aadressi. Külalise väljaregistreerimise kasutajad peavad sisestama väljaregistreerimise lehe kontakti jaotisesse meiliaadressi. Sisse logitud kasutajate kontaktandmed täidetakse automaatselt oma Dynamicsi kliendikontolt (esmane meiliaadress, mida nad autentimiseks kasutavad).

Klientidel on võimalus tellimused üle vaadata ja väljaregistreerimise tellimuse üksikasju muuta enne **, kui nad valivad** tellimuse lõpetamiseks tellimuse paigutamise.

### <a name="configure-google-pay-in-site-builder"></a>Kasutaja makse konfigureerimine saidikonstruktoril 

Enne fragmentide või lehekülgede konfigureerimist SüsteemigaRuktori Pay peate tagama, et teie saidi sisu turbepoliitika on Commerce'i saidi koostajas seatud.

Kindlustamaks, et teie sisu turbepoliitika on saidikonstruktoris seadistatud, järgige neid samme.

1. Minge oma saidil saidi sätete **laiendustele \>**.
1. Lisage sisu turbepoliitika vahekaardil rida alam-rc, ühendus-rc **·**, `*.google.com` raam-eellased, **·** **raami-src**, **lisa-src**, **skripti-src** **ja stiili-src** direktiivid.**·** **·**
1. Kui olete lõpetanud, valige Salvesta **ja avalda**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Makse väljendamise killu konfigureerimine Saidikonstruktori Osamaksega

Makse väljendamise killu häälestamiseks koos Võrgupoes Pay Pay'iga, järgige neid samme.

1. Minge saidikonstruktoris **killustajatele**.
1. Valige suvand **Uus**.
1. Dialoogiaknas **Uus** tükk valige **konteinerimoodul**, sisestage tüki nimi (**nt Kiirväljaregistreerimine**) ja seejärel valige **OK**. 
1. Valige uue killu konteineri **vaikepesa**.
1. Seadke parempoolsel atribuutide paanil konteinerimooduli atribuudid.

    - **Pealkiri** : sisestage pealkiri, mida kuvada oma saidi kiir väljaregistreerimise jaotises (nt **Kiir väljaregistreerimine**).
    - **Konteineri** paigutus: valige **voog**.
    - **Laius**: valige **täitekonteiner**.
    - **Kuvatud** lastid: **valige** kolm, et määrata väljaregistreerimise lehe kiirväljaregistreerimise sektsiooni reale mahtuv arv (nt tekstiboks, makse kiirmakse PayPal ja Töö tasu makse väljendamiseks).
    - **CSS klassi nimi** : sisestage **msc-kiirmakse konteiner** (nõutav).

    > [!IMPORTANT]
    > - Klassi **CSS nime väärtus** peab olema seatud **msc-kiirmakse** konteinerile, et juhtida konteineri käitumist väljaregistreerimise ajal. See käitumine hõlmab peitmist, kokkulangemist ja muid tegevusi, mis kehtivad väljaregistreerimise voo jooksul kiir väljaregistreerimise sektsioonile. MSC-kiirmakse **konteineri klass** töötab vaiketoimingutega, mis vabastatakse moodulteegi väljaregistreerimise mooduliga.
    > - Klassinimele saab lisada täiendavaid **CSS laade**. Kui kohandate mooduli käitumist, ristkontrollige laadi juhtelemente, kui kasutate sama mooduliteekide kodeeritud käitumist väljaregistreerimise moodulis, et kiir väljaregistreerimise käitumist.

1. **Valige konteineri vaikepesas** kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige makse kiirmoodul **ja** seejärel valige **OK**.
1. Määrake või **korrigeerige makse** väljendamise mooduli atribuutide **paanil väärtuse iFrame** kõrgus pikslites (nt **60**).
1. Väljal Toetatud **maksevahendi** tüübid **sisestageEldapay**. Väärtus peab vastama **kanali** jaoks häälestatud toetatud maksevahendi tüüpide stringile ([vt selles artiklis eespool toodud jaotist Commerce'i võrgupoe konfigureerimine Sektsioonis Omas Pay](#configure-a-commerce-online-store-for-google-pay)).

    > [!NOTE]
    > Saate korrake samme 6 kuni 9, et lisada makse **kiirmoodulid** muudele makseviisidele. Kooskõlasge **toetatud maksevahendi** tüüpide väärtus täiendavate konfigureeritud maksetüüpidega (nt **Paypal**).

1. Valikuline: vaikekonteinerimoodulile saate lisada tekstiblokaadi mooduli, et kaasata juhised või avaldamisteave. Pärast mooduli lisamist atribuutide paanil sisestage soovitud tekst väljale **Rikastekst**. Teksti saate asetada makse väljendamismoodulite peale või alla, **valides tekstibloki pesast ellipsi (**...**)** **ja seejärel valides Nihuta üles** või **Nihuta alla**.
1. Muudatuste **salvestamiseks** klõpsake nuppu Salvesta ja valige suvand **Lõpeta redigeerimine**.
1. **Tüki avaldamiseks** valige käsk Avalda.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Makse väljendamise killu lisamine väljaregistreerimise lehele

Makse väljendamise killu lisamiseks väljaregistreerimise lehele järgige neid samme.

1. Minge saidikonstruktori **lehekülgedele** ja valige seejärel oma saidi väljaregistreerimise lehekülg.
1. Valige suvand **Redigeeri**.
1. Põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Seadke parempoolsel atribuutide paanil konteinerimooduli atribuudid.

    - **Konteineri** paigutus – valige **virnastatud**.
    - **Laius**: valige **täitekonteiner**.
    - **Kuvatud** lastid :**valige** kolm, et määrata väljaregistreerimise lehe kiirväljaregistreerimise sektsiooni reale mahtuv arv (nt tekstiboks, makse kiirmakse PayPal ja Töö tasu makse väljendamiseks).

1. **Valige konteinerimooduli** pesast kolmikpunkt (**...**) ja seejärel valige käsk Lisa **kill.**
1. Dialoogiaknas **Vali tükk** valige loodud kiirmakse killus ja seejärel valige **OK**.
1. Muudatuste **salvestamiseks** klõpsake nuppu Salvesta ja valige suvand **Lõpeta redigeerimine**.
1. Valige **lehe** avaldamiseks avaldamine.

> [!NOTE]
> Kui väljaregistreerimise leht sisaldab juba konteinerit, mille väljaregistreerimise tükk on ja te soovite, et makse väljendamise moodulit renderdatakse tavalisest väljaregistreerimise konteinerist ülalpool, saate selle asetada olemasoleva väljaregistreerimise kohale või alla, valides põhipesas ellipspunkti (**...**) **·** **ja** valides seejärel suvandi Nihuta üles või **Nihuta alla.**

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Makse väljendamise killu lisamine ostukorvi lehele

Makse väljendamise killu lisamiseks ostukorvi lehele järgige neid samme.

1. Minge saidikonstruktori **lehekülgedele** ja valige seejärel oma saidi ostukorvi lehekülg.
2. Valige suvand **Redigeeri**.
3. Liigenduse vaates laiendage puuvaates **põhipesa** ja leidke ostukorvi moodulit sisaldav **konteiner**.
4. Ostukorvi moodulis valige Makse väljendamise **pesa**, valige ellips (**...**) ja seejärel valige **lisamoodul**.**·**
5. Dialoogiaknas **Vali** moodulid valige makse kiirmoodul **ja** seejärel valige **OK**.
6. Valige Makse väljendamise **mooduli** pesa. Parempoolsel atribuutide paanil sisestage siis jaotises Toetatud **maksevahendi tüübid** **väljale EnterPay**. Väärtus peab vastama **kanali** jaoks häälestatud toetatud maksevahendi tüüpide stringile ([vt selles artiklis eespool toodud jaotist Commerce'i võrgupoe konfigureerimine SektsioonisVäljal Pay](#configure-a-commerce-online-store-for-google-pay)).
1. Muudatuste **salvestamiseks** klõpsake nuppu Salvesta ja valige suvand **Lõpeta redigeerimine**.
1. Valige **lehe** avaldamiseks avaldamine.

Kasutajad saavad makse väljendamise **moodulite** (teisisõnu, kolm saadaolevat toetatud maksevalikut) **ostukorvi Makse väljendamise pesas olla kuni kolm toetatud makse kiirmoodulit**.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Seadistage Hinnaaland Pay väljaregistreerimise makse sektsioonis suvandina

Võite Seadistada Kuni-pay väljaregistreerimise makse jaotises valikuna ainult makse- ja mitte kiirfunktsioonide jaoks. Väljaregistreerimise vormi täidab kasutaja ja Theo Pay makseleht valmis ainult Vaikimisi Pay makseks. Täidetud sisseregistreerimise üksikasjade ülekirjutamiseks ei kasutata Kasutaja kontoteavet.

> [!NOTE]
> Järgmine protseduur eeldab, et teie sait kasutab väljaregistreerimise killust, mis on konfigureeritud pealemineku teabega, saatmisaadressi, tarnevalikute, kontaktteabe, valikuliste tingimuste ja väljaregistreerimise elementide jaotisega. Vaikemooduli teegi väljaregistreerimise moodul vabastatakse väljaregistreerimise jaotise konteineriga, mille tekstiblokk, boonuspunktid, kinkekaart ja maksemoodulid. Lisateavet vt [maksemoodulist](../payment-module.md).

Selleks, et seadistada Hinnaaland Pay tavalise makse suvandina **väljaregistreerimise** lehe makseviisi jaotises, järgige neid samme.

1. Minge saidikonstruktoris **tükid** ja valige seejärel saidi väljaregistreerimise killus.
1. Valige suvand **Redigeeri**.
1. Väljaregistreerimise teabe pesal **valige kolmikpunkt (**...**) ja seejärel valige lisamoodul** **.**
1. Dialoogiaknas **Vali** moodulid valige maksemoodul **ja** seejärel valige **OK**.
1. Seadke maksemooduli **atribuutide** paanil paremal konteinerimooduli atribuudid.

    - **Pealkiri** : sisestage pealkiri, mida kuvada oma saidi kiir väljaregistreerimise jaotises (ntEkraani **Pay**).
    - **Välja kõrgus iFrame** – muutke väärtus eelistatud kujunduse kõrguseks pikslites (nt **75**). 
    - **Toetatud maksevahendi** tüübid – **sisestageEldaPay**, et see ühtiks Commerce headquartersiElda Pay Connectori konfiguratsiooniga.
    - **On esmane makse** – jätke märkeruut tühjaks. (See atribuut on tavaliselt lubatud Udueni väljaregistreerimise mooduli jaoks.)
    - **Makse laadi alistamine** – atribuuti ei toetataEldav makse konfiguratsiooni puhul.
    - **Kasuta konnektori ID-d** – see atribuut tuleb valida, kui lehel kasutatakse mitut makseühendust.

1. Asetage moodul teiste maksemoodulite peale või alla, valides maksepesast kolmikpunkti (**...**)**·** **ja seejärel valides Nihuta üles** või **Nihuta alla.**
1. Muudatuste **salvestamiseks** klõpsake nuppu Salvesta ja valige suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

### <a name="modes-of-delivery"></a>Tarneviisid

Maksete väljendamise mooduliga, mis kasutab Osamaksmistasu, eelvalitakse esimene tagasisaadmisvalik valitud lähetusaadressi suhtes KontostSeadis tasumine. Kasutajatel on võimalus lähetusaadressi soovi korral erinevale suvandile kohandada.

Järjestus, milles tarneviisid kuvatakse makse väljendamise moodulis on **konfigureeritud kanali tarneviiside lehel** Rakenduse Commerce headquartersis. Minge Commerce Headquartersi kaupluse ja **ärikanalite \>\> võrgupoodidesse** ja valige **kaupluse jaemüügikanali ID** väärtus. Tegevuspaani vahekaardil Seadistus **valige tarneviisid** **.** Loetletud tarneviisid kuvatakse sama tellimusena makse kiirmoodulis. Jaemüügikanali **või toote tarneviiside** lisamiseks või eemaldamiseks valige tegevuspaanil suvand Tarneviiside haldamine. Tarneviiside kohta lisateabe saamiseks vt tarneviiside [seadistamist](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Väljaregistreerimise moodul kasutab ka tarnesuvandite moodulit, kui tarneviisid renderdatakse väljaregistreerimise ajal. Lisateavet vt tarnesuvandite [moodulist](../delivery-options-module.md).

Tarneviisid kuvatakse, kui need on lisatud võrgupoes **tarneviiside** loendisse.

## <a name="additional-resources"></a>Lisaressursid

[Maksete KKK](payments-retail.md)

[Maksmismoodul](../add-checkout-module.md)

[Maksemoodul](../payment-module.md)
