---
title: Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks
description: See artikkel kirjeldab, kuidas konfigureerida kliendikonto makseviisi moodulis Microsoft Dynamics 365 Commerce. See kirjeldab ka seda, kuidas krediidilimiidid mõjutavad ettemaksete hõivamist ettevõtete vahel (B2B) e-kaubanduse saitidel.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: b8424920c3a177e01b71fc1c288b7acdd97ef191
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272013"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas konfigureerida kliendikonto makseviisi moodulis Microsoft Dynamics 365 Commerce. See kirjeldab ka seda, kuidas krediidilimiidid mõjutavad ettemaksete hõivamist ettevõtete vahel (B2B) e-kaubanduse saitidel.

Jaemüüjad võivad võtta e-kaubanduse kanalis müüdavate toodete ja teenuste eest tasu erinevat tüüpi maksemeetoditega. Kõik jaemüüja aktsepteeritavad maksetüübid tuleb konfigureerida süsteemi seadistamisel rakenduses Dynamics 365 Commerce. Kliendikonto (või "ettemaks") makseviisi peab toetama B2B e-commerce’i saitidel. 

## <a name="prerequisites"></a>Eeltingimused

1. Lisage kliendikonto makseviis Commerce'i peakontoris.
2. Siduge kliendikonto makseviis e-kaubanduse kanaliga.
3. Veenduge, et **atribuudi Luba kontol** on **kliendile rakenduse Retail ja Commerce \> Customers \> kõigi klientide \> makse vaikesätted commerce headquartersis** lubatud.

    > [!NOTE]
    > Kui kõigil klientidel peaks **olema** **lubatud lubatud kasutada ettemakse makseviisi,** saate B2B-saidiga seotud kanali vaikekliendi jaoks seada atribuudi Luba kontol väärtuseks Jah. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Kliendikonto makseviisi lubamine Commerce'i saidiehitajas 

Kliendikonto makseviisi lubamiseks Commerce'i saidiehitajas toimige järgmiselt.

1. Avage **Saidi sätted \> Laiendused**.
1. Seadke atribuut **Luba kliendikonto maksed** väärtusele **B2B-klientidele lubatud**. 
1. Valige suvand **Salvesta ja avalda**.

> [!NOTE]
> Uued saidi sätted jõustuvad alles pärast faili app.settings.json värskendamist. Lisateabe saamiseks vt [SDK ja mooduliteegi värskendused](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Kliendikonto makseviisi lubamine B2B e-kaubanduse saidi kassa lehel

Kliendikonto makseviisi lubamiseks B2B e-kaubanduse saidi kassa lehel toimige järgmiselt.

1. Leidke ja redigeeride Commerce'i saidiehitajas kassa lehte või fragmenti, mis sisaldab kassamoodulit B2B e-kaubanduse saidi jaoks.
1. Valige lahtrist **Kassa jaotise konteiner** käsk **Lisa moodul** ja seejärel lisage moodul **Kliendikonto makse**.
1. Paigutage moodul **Kliendikonto makse** valides kolmikpunkti (**...**) ja seejärel valides vastavalt vajadusele kas **Nihuta üles** või **Nihuta alla**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Kinnitage, et kliendikonto makseviis on lubatud ja avaldatud.

Kinnitamiseks, et kliendikonto makseviis on lubatud ja avaldatud, toimige järgmiselt.

1. Logige e-kaubanduse saidile sisse.
1. Lisage toode ostukorvi.
1. Minge kassa lehele. Peaksite nägema uut makseviisi **Kliendikonto**.

## <a name="work-with-credit-limits"></a>Krediidilimiidiga töö

Kui kliendi konto maksete võimalused on B2B-saidil lubatud, soovivad organisatsioonid tavaliselt tellimuse hõivamise protsessi käigus näidata teavet krediidilimiitide ja krediidilimiidi saldode kohta. Kliendi krediidilimiit on **määratud** **Commerce** Headquartersi kliendikirje krediidi ja sissenõuete kiirkaardi krediidilimiidi atribuudiga. B2B stsenaariumi puhul tuleb siiski sageli esitada tellimus, mille alusel kliendi kohad arveldatakse selle organisatsiooni kontole, kuhu klient kuulub. Seetõttu peate arve konto atribuudi **kliendikirje** **arve** ja tarne kiirkaardil seadistama organisatsiooni kliendikonto ID-le. Seejärel, kui klient sisestab tellimuse B2B saidile, arveldatakse tellimus organisatsioonile. B2B-sait kasutab ka organisatsiooni krediidilimiiti kliendikirjes määratletud krediidilimiidi asemel.

B2B-veebisaidil kuvatava krediidilimiidi arvutamine ja saldo sõltuvad **Commerce Headquartersi krediidilimiidi tüübi** atribuudi sättest. Selle atribuudi asukoht on erinev sõltuvalt sellest, kas funktsioonihalduse **tööruumis** on krediidihalduse **funktsioon lubatud**.

- Kui krediidihalduse **funktsioon** on lubatud, **·** **\>\> asub atribuut krediidilimiidi kiirkaardil krediidi ja sissenõuete seadistamise krediidi ja sissenõuete parameetrite krediidis.\>** 
- Kui krediidihalduse **funktsioon** on keelatud, **·** **asub atribuut krediidireitingu all Müügireskontro seadistuse \>\> müügireskontro parameetrid Krediidireiting \>**.

Väärtused, mida krediidilimiidi **tüübi** **atribuut toetab, on Pole**, Saldo **,** Saldo **+ saateleht või toote sissetulek** ja Saldo **+ Kõik**. Lisateavet nende väärtuste kohta vt krediidilimiidi [tüübi väärtustest](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Soovitame teil seada krediidilimiidi **tüübi** atribuudiks **Saldo +** saateleht või tootekviitung, nii et avatud müügitellimused ei panustaks saldo arvutamisse. Sel juhul, kui teie kliendid teevad tulevasi tellimusi, ei pea nad sidjagama, et need tellimused mõjutaksid nende praegust saldot.

Teine atribuut, mis mõjutab **järeltellimusi**, on kohustuslik krediidilimiidi atribuut, mis asub **kliendikirje** krediidi ja kollektsioonide kiirkaardil. Kui määrate **selle** atribuudi kindlatele klientidele väärtuseks Jah, saate sundida süsteemi kontrollima nende krediidilimiiti, isegi kui krediidilimiidi tüübi atribuudi väärtuseks on määratud Pole **,** **et** määrata, et krediidilimiiti ei kontrollita iga kliendi puhul.

Seda ettemaksemeetodit kasutav klient ei saa praegu maksta tellimuse järelejäänud kreeditsaldost rohkem. Näiteks kui kliendi järelejäänud kreeditsaldo on $1,000 kuid tellimuse väärtus $1,200, saab klient arveid $1,000 ainult ettemaksmeetodil. Sel juhul peab klient saldo maksmiseks kasutama mõnda muud makseviisi. Tulevikus võimaldab ärikonfiguratsioon kasutajatel tellimuste paigutamisel kulutada peale oma krediidilimiidi.

Krediidi **- ja sissenõuete moodulil** on uued krediidihalduse võimalused. Nende võimaluste sisse lülitamiseks lubage funktsioonihalduse **tööruumis** krediidihalduse **funktsioon**. Üks uutest võimalustest võimaldab müügitellimusi blokeerimisreeglite järgi ootele panna. Seejärel saab krediidihaldur persona tellimused vabastada või tagasi lükata pärast edasist analüüsi. Siiski ei kehti müügitellimuste ootele panemise võimalus Commerce Ordersi puhul, **kuna** müügitellimustel on sageli ettemakse ja krediidihalduse funktsioon ei toeta täielikult ettemaksestsenaariume. 

Vaatamata sellele, kas **krediidihalduse** funktsioon on lubatud ja kui kliendi saldo läheb tellimuse täitmise ajal krediidilimiidist üle, ei jää müügitellimused ootele. Selle asemel loob Commerce kas hoiatusteate või tõrketeate, **·** **sõltuvalt teate väärtusest krediidilimiidi välja ületamisel krediidilimiitide** kiirkaardil.

Atribuut **Välista krediidihaldusest**, mis takistab Äri müügitellimuste ootele jäämist, asub müügitellimuse päises (**Jaemüügi ja \> ärikliendid \> Kõik müügitellimused**). Kui äri müügitellimuste **puhul on** selle atribuudi väärtuseks seatud Jah (vaikeväärtus), jäetakse tellimused krediidihalduse ootel oleku töövoost välja. Kuigi atribuudi nimi on Välista **krediidihaldusest**, kasutatakse tellimuse täitmise ajal siiski määratletud krediidilimiiti. Tellimused ei jää ootele.

Võimalus panna Commerce’i müügitellimused blokeerimisreeglite alusel ootele on plaanitud tulevasteks Commerce’i väljalaseteks. Kuni seda toetatakse, kui peate rakenduse Commerce müügitellimused läbima uued krediidihalduse vood, saate kohandada järgmisi XML-faile oma lahenduses Visual Studio. Muutke failides loogikat nii, et **CredManExcludeSalesOrderi** lipu väärtuseks oleks seatud **Ei**. Nii määratakse äri müügitellimuste **puhul atribuut** Välista **krediidihaldusest** väärtuseks Ei vaikimisi.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

**Kui lipu CredManExcludeSalesOrder** **väärtuseks on seatud Ei** ja B2B klient saab kauplustest osta müügikoha rakendust kasutades, võib sularaha ja kannete sisestamine nurjuda. Näiteks on sularahamakse tüübil blokeerimisreegel ja B2B klient ostis sularaha abil kauplusest kaupu. Sellisel juhul ei arveldata tulemuseks saadud müügitellimust edukalt, kuna see jääb ootele. Seetõttu sisestamine nurjub. Seetõttu soovitame pärast selle kohandamise juurutamist teha lõpp-lõpu testimist.

## <a name="additional-resources"></a>Lisaressursid

[B2B e-kaubandussaidi häälestamine](set-up-b2b-site.md)

[B2B äripartnerite haldamine kliendihierarhiaid kasutades](partners-customer-hierarchies.md)

[Äripartnerkasutajate haldamine B2B e-kaubandussaitidel](manage-b2b-users.md)

[Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks](quantity-limits.md)

[SDK ja mooduliteegi värskendused](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
