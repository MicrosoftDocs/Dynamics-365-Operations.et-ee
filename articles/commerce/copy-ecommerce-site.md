---
title: E-kaubanduse saidi kopeerimine
description: See artikkel kirjeldab, kuidas kopeerida olemasolevat e-äri saiti saidi sees või e-äri keskkondade vahel saidikonstruktoris Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 06/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: cb53a76b2ebe5b511bf5009727f20f20755e5720
ms.sourcegitcommit: 13c7a1cc4c90417e3e88db59b7d2165b3c40a56c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2022
ms.locfileid: "8935740"
---
# <a name="copy-an-e-commerce-site"></a>E-kaubanduse saidi kopeerimine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas kopeerida olemasolevat e-äri saiti saidi sees või e-äri keskkondade vahel saidikonstruktoris Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce Toetab saitide kopeerimist või teisaldamist Iseteenindustoiminguna Commerce'i saidi koostajas. Saite saab kopeerida üksikus e-äri keskkonnas või kahe e-äri keskkonna vahel. Kasutaja, kes käivitab saidi kopeerimise toimingu, peab olema rentniku administraator nii lähte- kui siht-e-äri keskkondades.

Saidi koopia toiming kopeerib kogu lähtesaidi e-kaubanduse sisu. See sisu hõlmab lehekülgi, killusteid, malle, URL-e ja varasid. Enne uue saidi kasutamist tuleb see lähtestada esimese käituskogemuse (EXE) protsessi kaudu. Kanaleid saab vastendada ja hallata saidikonstruktoris saidi sätete **kanalites \>**.

Saidi koopiatoimingu kestus sõltub peamiselt lähtesaidi varade arvust. Väga suurte saitide puhul soovitame selle asemel kasutada keskkonna kopeerimistoimingut. (Seda toimingut tuntakse ka andmete teisaldamise toiminguna).

> [!NOTE]
> - Lähtelaokoht on saidi koopiatoimingu kestuse jaoks kirjutuskaitstud.
> - Kopeeritakse ainult avaldatud dokumentide versioonid. Kui ühtki versiooni pole avaldatud, kopeeritakse ainult viimased versioonid.
> - Sisu versiooniajalugu ei ole sihtsaidil saadaval.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Saidi kopeerimine e-ärikeskkonnas

Saidi kopeerimiseks e-äri keskkonnas järgige neid samme.

1. Logige sisse saidikonstruktorisse keskkonnas, kus soovite teha kopeerimistoimingu.
1. Avage saidiloendi vaade, valides **ülemises parempoolses nurgas** saidilüliti ja valides seejärel suvandi Halda **saite**.
1. Otsige sait, mida soovite kopeerida või muuta, ning valige see, märkides saidi nime kõrval ruudu.
1. Käsuribal valige suvand **Kopeeri sait**.
1. **Menüüs Kopeeri saidi** väljale Uue saidi **nimi** sisestage uue saidi nimi. Uus saidi nimi peab e-ärikeskkonnas olema kordumatu. Lähte **rentniku** ja **lähtekoha** väljad seatakse automaatselt praeguse rentniku ja valitud saidi teabele.
1. Valige **loo koopia**.

Pärast teabe kinnitamist näitab teatis, et uus saidi koopiatöö on loodud. Töö edenemist saate jälgida rentnike [tööde lehe parempoolsel **paanil**](#monitor-the-site-copy-operation). Kui kopeerimistoiming on edukalt lõpule viidud, kuvatakse uus sait saidiloendi vaates saitide loendis.

Järgmine näide näitab saidikonstruktori **menüü** Kopeeri sait väljaminek näidet.

![Kopeeri saidi väljaminev menüü saidikonstruktoris.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Saidi kopeerimine kahe e-ärikeskkonna vahel

Saidi kopeerimiseks kahe e-äri keskkonna vahel järgige neid samme.

1. Logige sisse sihtkoha e-äri keskkonna saidikonstruktorisse.
1. Käsuribal valige suvand **Kopeeri sait**.
1. **Menüüs Kopeeri saidi** väljale Uue saidi **nimi** sisestage uue saidi nimi. Uus saidi nimi peab e-ärikeskkonnas olema kordumatu.
1. Väljal Allika **rentnik** valige lähte rentniku nimi.
1. **Valige väljal Lähtesaidid** lähtesaidid.
1. Valige **loo koopia**.

> [!NOTE]
> Rentnike administraatori õigused on nõutavad nii lähte- kui sihtkoha e-äri keskkondades.

Pärast teabe kinnitamist näitab teatis, et uus saidi koopiatöö on loodud. Töö edenemist saate jälgida rentnike [tööde lehe parempoolsel **paanil**](#monitor-the-site-copy-operation). Kui kopeerimistoiming on edukalt lõpule viidud, kuvatakse uus sait saidiloendi vaates saitide loendis.

## <a name="map-channels-during-the-site-copy-operation-optional"></a>Kanalite vastendamine saidi kopeerimistoimingu ajal (valikuline)

Lähtekanaleid ja -lokte saab vastendada sihtkanalite ja -lokaadidega saidi koopiatoimingu osana. Kui kanali vastendamine toimub saidi kopeerimistoimingu osana, ei ole SAIDI lähtestamine TOOTMISPROTSESSI ABIL JA kanalite konfigureerimine saidi sätetes vajalik. 

Kõigi kanalite ja lokaadide vastendamiseks saidikonstruktoril nii nagu on" (1-1), järgige neid samme.

1. Avage saidiloendi vaade, valides **ülemises parempoolses nurgas** saidilüliti ja valides seejärel suvandi Halda **saite**.
1. Otsige sait, mida soovite kopeerida või muuta, ning valige see, märkides saidi nime kõrval ruudu.
1. Käsuribal valige suvand **Kopeeri sait**.
1. Sisestage **menüü Kopeeri sait** väljale Uue saidi **nimi**, Allika **rentnik** **ja** Lähtekoht (kui seda pole juba olemas) väärtused.
1. Valige suvand **Lisa kanali vastendused**.
1. Saidikanalite **ja lokaadide väljaminekmenüüs** valige **lähtekanal** ja seejärel valige lähtekanal.  
1. Valige **sihtkanal** ja seejärel lähtekanaliga sama kanal. 
1. Valige **lisa lokaadiks**.
1. Valige **lähte lokaadiks** ja seejärel allika lokaadiks.
1. Valige **sihtkaust** ja seejärel lähte lokaadiga sama lokaadi. 
1. URL-i **tee** jaoks sisestage kordumatu URL-tee, mida praegu sihtkeskkonnas ei kasutata.
1. Korrake samme 8-11 iga kanali vastendamiseks lokaadiga.
1. Valige **Rakendamine**.
1. Korrake samme 6–11 iga lähtekanali puhul.
1. Valige suvand **Sule**.
1. Kontrollige konfiguratsiooni täpsuse üle ja valige suvand **Kopeeri sait**.

> [!NOTE]
> Kõik lähtekanalid ja lokid tuleb vastendada ja neid saab vastendada ainult üks kord.

## <a name="monitor-the-site-copy-operation"></a>Saidi koopiatoimingu s monitorimine

Saidi koopiatoimingu edenemise jälgimiseks järgige neid samme.

1. Logige sisse sihtkoha e-äri keskkonna saidikonstruktorisse.
1. Valige vasakul paanil **rentnikutööd**.
1. Otsige ja **valige lehel** Rentniku tööd loendist saidi koopiatöö. Paan ilmub paremal ja näitab valitud töö olekut ja üksikasju.

Saate tühistada töö, mille olek on **Pooleli**. Valige loendist töö ja seejärel valige **käsuribalt** Tühista.

Saate uuesti käivitada töö, mille olek on Nurjunud **või** **Tõrgetega lõpetatud**. Valige loendist töö ja seejärel valige **käsuribalt** Uuesti proovige.

> [!NOTE]
> Video varade töötlemine võib jätkuda pärast saidi koopiatöö lõpetamist.

Järgmine näide kuvab saidikonstruktori rentnike **tööde lehe** parempoolse paani näite.

![Töö üksikasjad saidikonstruktori rentniku tööde lehe paremal paanil.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Uue saidi lähtestamine, kasutades KÄIVITAMISprotsessi EXE

Enne uue saidi kasutamist tuleb see LÄHTESTAdaTOOTMISPROTSESSI KÄIGUS.

Uue saidi lähtestamiseks, kasutades JÄRGNEVAID etappe.

1. Logige uue saidi puhul sisse saidikonstruktorisse.
1. Avage saidiloendi vaade, valides **ülemises parempoolses nurgas** saidilüliti ja valides seejärel suvandi Halda **saite**.
1. Otsige ja valige uus sait, mida soovite lähtestada.
1. **Dialoogiaknas Saidi** häälestamine väljal **Domeeni valimine** valige domeen. Valida saab kõiki lähtestamise ajal e-ärikeskkonnaga seostatud domeene.
1. Valige väljal **Valige vaikimisi kanal** seostatud võrgupoe kanal. Valitud kanal pakub sortimente ja muud teavet, mis on talletatud Commerce Headquartersis.
1. **Valige väljal Vaikekeele** valimine autori vaikekeel. Valida saab kõiki valitud võrgupoe kanali jaoks konfigureeritud keeli.
1. Väärtus koosneb **väljal** Tee põhidomeenist ja valikulisest URL-teest, mille saate sisestada. VÕITE URL-i tee tühjaks jätta, kui kanalit toimetatakse domeeni juurkaustast või kui soovite seda teavet sisestada hiljem kanali konfiguratsiooni vaates saidikonstruktoris. E-äri keskkonnas peab saiditee olema kordumatu.
1. Valige nupp **OK**. Sait lähtestatakse esitatud teabega ja olete valmis saidihalduse vaatesse.

Järgmine näide kuvab saidikonstruktori **dialoogiboksi** Häälestuse.

![Seadistage oma saidi dialoogiboks saidikonstruktoris.](media/site-copy_3.png)

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-b2c-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-b2c-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)
