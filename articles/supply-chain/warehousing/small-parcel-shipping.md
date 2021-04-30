---
title: Väikepaki saatmine
description: Sellest teemast leiate teavet väikepaki saatmise (SPS) funktsiooni kohta. See funktsioon võimaldab rakendusel Microsoft Dynamics 365 Supply Chain Management esitada üksikasju pakitud konteineri kohta vedajale ja seejärel saada sellelt vedajalt tagasi saadetise silt, tarnemäär ja jälgimisnumber.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910205"
---
# <a name="small-parcel-shipping"></a>Väikepaki saatmine

[!include [banner](../../includes/banner.md)]

Väikepaki saatmise (SPS) funktsioon võimaldab rakendusel Microsoft Dynamics 365 Supply Chain Management suhelda otse vedajatega, pakkudes raamistikku vedaja API-de kaudu suhtlemiseks. See funktsioon on kasulik, kui saadate individuaalseid müügitellimusi kommertsvedajate kaudu, mitte kasutades konteineriga saatmist või vähem kui koormatäis (LTL) saatmist.

SPS-i funktsioon suhtleb teie saadetise vedajaga spetsiaalse *määramootori* kaudu. Teie organisatsioon peab selle määramootori välja töötama koos teie vedaja või vedaja keskuse teenusega. Määramootor võimaldab rakendusel Supply Chain Management esitada üksikasju pakitud konteineri kohta teie vedajale ja seejärel saada sellelt vedajalt tagasi saadetise silt, tarnemäär ja jälgimisnumber.

Tagastatav tarnemäär lisatakse seotud müügitellimusele lisakuluna. Tagastatud saadetise sildi saab seejärel automaatselt printida, kasutades Zebra programmeerimiskeelega (ZPL) printerit ja kinnitada saadetisele. Vedaja skannib selle saadetise silti, kui võtab pakid teie laos peale.

## <a name="prepare-your-system-to-support-sps"></a>Süsteemi ettevalmistamine SPS-i toetamiseks

Enne SPS-i funktsiooni kasutamist peate SPS-i funktsiooni funktsioonihalduses sisse lülitama, lisama oma määramootori ning häälestama selle toetamiseks moodulid **Transpordihaldus** ja **Laohaldus**.

### <a name="turn-on-the-sps-feature"></a>Funktsiooni SPS sisselülitamine

Enne selle funktsiooni SPS kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *Transpordihaldus*
- **Funktsiooni nimi:** *Väikepaki saatmine*

### <a name="deploy-and-set-up-rate-engines"></a>Määramootorite juurutamine ja häälestamine

Supply Chain Management ei sisalda ühtegi määramootorit. Teil tuleb hankida või luua mis tahes nõutav määramootor ja seejärel lisada see oma süsteemile. Samas pakub Microsoft määramootori demoversiooni, mida saate kasutada testimiseks.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Määramootori demoversiooni allalaadimine ja juurutamine

Määramootori demoversiooni hankimiseks tehke järgmist.

1. Laadige GitHubis alla [määramootori demoversiooni dünaamilise lingiga teek (DLL)](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).
1. Salvestage DLL oma Supply Chain Managementi serveris kaustas **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Funktsionaalsete määramootorite loomine ja juurutamine

Lisateavet selle kohta, kuidas funktsiooni määramootoreid luua ja juurutada nii, et neid saaks kasutada tootmis- või katsekeskkonnas, vaadake järgmistest teemadest.

- [Uue transpordihalduse mootori loomine](../transportation/create-new-transportation-management-engine.md)
- [Transpordihalduse mootorite häälestamine](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Lisateavet SPS-i määramootori loomise kohta vt järgmiselt ajaveebipostitusest [Väikepaki saatmine: kuidas kasutada väikepaki saatmise funktsiooni rakenduses Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Määramootori häälestamine Supply Chain Managementis

Pärast SPS-i määramootori loomist ja juurutamist järgige selle häälestamiseks järgmisi juhiseid.

1. Avage **Transpordihaldus \> Seadistus \> Mootorid \> Määramootor**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Määrake uuel real järgmised väljad.

    - **Hindamise mootor** – sisestage määramootori kordumatu nimi. Kui kasutate määramootori demoversiooni, sisestage *Määramootori demoversioon*.
    - **Nimi** – sisestage määramootori lühikirjeldus. Kui kasutate määramootori demoversiooni, sisestage *Määramootori demoversioon*.
    - **Hindamise metaandmete ID** – valige alus, mida tuleks kasutada määra arvutamiseks. Näiteks võib teie hinnamäära arvutada vahemaa põhjal. Kui kasutate määramootori demoversiooni, võite selle välja tühjaks jätta.
    - **Mootori komplekt** – sisestage juurutatud DLL-i paketi failinimi. Kui kasutate määramootori demoversiooni, sisestage *TMSSmallParcelShippingEngine.dll*.
    - **Mootori klass** – sisestage klassi nimi, mis loodi teie määramootori jaoks. Kui kasutate määramootori demoversiooni, sisestage *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.

## <a name="example-scenario"></a>Näidisstsenaarium

See näidise stsenaarium näitab, kuidas SPS-i seadistada ja kasutada pärast seda, kui olete oma süsteemi selles teemas kirjeldatud viisil ette valmistanud. See stsenaarium kasutab eelnevalt mainitud määramootori demoversiooni.

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle stsenaariumi kasutamiseks siin määratud demokirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

### <a name="set-up-the-scenario"></a>Stsenaariumi seadistamine

Selle näite stsenaariumi korral peab teil olema demo vedaja, vedaja grupp, pakkimispoliitika ja pakkimisprofiil. Järgmistes alamjaotistes seletatakse, kuidas valmistada ette stsenaariumi jaoks vajalikke kirjeid. Tootmisstsenaariumis sarnaneb seadistusprotsess tavaliselt siin kirjeldatud protsessile. Samas määrate te erinevad väärtused.

#### <a name="set-up-carriers"></a>Vedajate häälestamine

Vedaja häälestamiseks tehke järgmist.

1. Avage jaotis **Transpordihaldus \> Seadistus \> Vedajad \> Kättetoimetajad**.
1. Vedaja lisamiseks valige toimingupaanilt suvand **Uus**.
1. Määrake päises järgmised väärtused.

    - **Saadetise vedaja:** *demo vedaja*
    - **Nimi:** *demo vedaja*
    - **Viis:** *maismaa*

1. Määrake kiirkaardil **Ülevaade** järgmised väärtused.

    - **Aktiveeri saadetise vedaja:** *jah*
    - **Aktiveeri vedaja hinnang:** *jah*

1. Valige kiirkaardil **Teenused** suvand **Uus**, et lisada teenus ruudustikku.
1. Määrake uue teenuse jaoks järgmised väärtused.

    - **Vedaja teenus:** *demo vedamisteenus*
    - **Nimi:** *demo vedamisteenus*
    - **Transpordiviis:** *maapind*

    Sisestage nõutud väärtused kõigi muude väljade jaoks. (Kui salvestate uue saadetise vedaja kirje, luuakse uus tarneviis ja väli **Tarneviis** määratakse automaatselt.)

1. Hinnanguprofiili lisamiseks valige ruudustikus kiirkaardil **Hindamise profiilid** suvand **Uus**.
1. Määrake uue profiili jaoks järgmised väärtused.

    - **Hindamise profiil:** *demo vedamisteenus*
    - **Nimi:** *demo vedamisteenus*
    - **Määramootor:** *määramootori demoversioon*

    Sisestage nõutud väärtused kõigi muude väljade jaoks.

1. Valige toimingupaanil nupp **Salvesta**.

Lisateavet vedajate seadistamise kohta vt teemast [Vedajate häälestus](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Vedaja teenusekontode häälestamine

Vedaja teenusekonto häälestamiseks tehke järgmist.

1. Avage **Transpordihaldus \> Seadistus \> Hinnang \> Vedaja teenusekonto**.
1. Valige toimingupaanil suvand **Uus**, et lisada vedaja teenusekonto.
1. Määrake uue konto jaoks järgmised väärtused.

    - **Saadetise vedaja:** *demo vedaja*
    - **Vedaja teenus:** *demo vedamisteenus*
    - **Vedaja kliendikonto number:** vedaja kliendikonto number, mida kasutatakse saadetise vedaja seose kinnitamiseks ja autentimiseks. Selle väärtuse annab teie vedaja. Kui kasutate demoteenust, saate sisestada vaikeväärtuse.
    - **Tegevuskoht:** *6*
    - **Ladu:** *62*

    > [!NOTE]
    > Sageli on väärtus **Vedaja kliendikonto number** ainus väärtus, mis on vajalik ühenduse autentimiseks. Samas kui teie vedaja nõuab siiski täiendavaid autentimisparameetreid, peaks teie organisatsioon seda lehekülge kohandada vastavalt vajadusele lisaväljade lisamiseks.

#### <a name="set-up-a-container-packing-policy"></a>Konteineri pakkimise poliitika häälestamine

Konteineri pakkimispoliitika häälestamiseks tehke järgmist.

1. Kui te pole veel ZPL-printeri definitsiooni häälestanud, kasutage selleks dokumendi marsruudivaliku agendi rakendust. Lisateavet vt [Dokumentide printimise ülevaade](../../fin-ops-core/dev-itpro/analytics/print-documents.md).
1. Avage jaotis **Laohaldus \> Seadistus \> Konteinerid \> Konteineri pakkimise poliitikad**.
1. Valige toimingupaanil suvand **Uus**, et lisada konteineri pakkimise poliitika.
1. Määrake uue poliitika päises järgmised väärtused.

    - **Konteineri pakkimise poliitika:** *pakkimise demopoliitika*
    - **Kirjeldus:** poliitika kirjeldus.

1. Määrake kiirkaardil **Ülevaade** järgmised väärtused.

    - **Ladu:** *62*
    - **Lõpliku saadetise vaikeasukoht:** *Baydoor*
    - **Massiühik:** *KG*
    - **Konteineri sulgemise poliitika:** *Automaatne väljastamine*
    - **Konteineri väljastamise poliitika:** *tee kättesaadavaks saadetise lõppsihtkohas*

1. Kiirkaardil **Konteineri manifest** määrake järgmised väärtused.

    - **Automaatne manifest konteineri sulgemisel:** *jah*
    - **Konteineri manifesti nõuded:** *transpordihaldus*
    - **Prindi konteineri sisu:** *ei*

1. Kiirkaardil **Konteineri sildi printimine** määrake järgmised väärtused.

    - **Prindi konteineri saadetise silt:** *alati*
    - **Printeri nimi:** ZPL-printeri nimi, mis prindib saadetise sildid

#### <a name="set-up-a-packing-profile"></a>Pakkimisprofiili häälestamine

Pakkimisprofiili häälestamiseks tehke järgmist.

1. Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Pakkimisprofiilid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku pakkimisprofiil.
1. Määrake uue profiili jaoks järgmised väärtused.

    - **Pakkimisprofiili ID:** *demo pakkimisprofiil*
    - **Kirjeldus:** profiili kirjeldus.
    - **Konteineri pakkimise poliitika:** *pakkimise demopoliitika*
    - **Konteineri ID-režiim:** *Automaatne*
    - **Konteineri tüüp:** *SmallBox*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>SPS-i vedaja kasutamiseks kliendi häälestamine

Järgige neid samme kliendi häälestamiseks, nii et see saaks kasutada teie loodud vedajat.

1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Otsige ja valige ruudustikust klient *US-027.*
1. Valige toimingupaani vahekaardil **Üldine** grupis **Häälesta** suvand **Vedaja kliendikontod**.
1. Valige tegevuspaanil lehel **Vedaja kliendi kontod** suvand **Uus**, et lisada konto ruudustikku.
1. Määrake uue konto jaoks järgmised väärtused.

    - **Saadetise vedaja:** *demo vedaja*
    - **Vedaja kliendikonto number:** *12345*(väärtus ei ole selle stsenaariumi puhul oluline, kuid sellele viidatakse järgmises jaotises.)

### <a name="go-through-the-example-scenario"></a>Läbige näidisstsenaarium

Pärast kõigi näidisandmete seadistamist eelmises jaotises kirjeldatud viisil olete valmis läbima näidisstsenaariumi.

#### <a name="create-a-sales-order-and-process-the-work"></a>Müügitellimuse loomine ja töö töötlemine

Müügitellimuse loomiseks tehke järgmist.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse loomiseks valige **Uus**.
1. Määrake dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvandiks *US-027*.
1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. Seadke kiirkaardil **Müügitellimuse päis** väli **Vedaja kliendikonto number** väärtus, mille sellele kliendile varem valisite (*12345*).
1. Lisage jaotises **Müügitellimuse read** müügirida ja seadke selle jaoks järgmised väärtused.

    - **Kauba kood:** *A0002*
    - **Kogus:** *1*
    - **Tegevuskoht:** *6*
    - **Ladu:** *62*

1. Lülituge vaatele **Päis**.
1. Määrake kiirkaardil **Kohaletoimetamine** järgmised väärtused.

    - **Saadetise vedaja:** *demo vedaja*
    - **Vedaja teenus:** *demo vedamisteenus*

1. Minge tagasi vaatesse **Read**. Kui teil palutakse uuendada müügiridade tarneviisi, valige **Jah**.
1. Valige jaotises **Müügitellimuse read** varem seadistatud tellimuse rida ja seejärel valige **Varud \> Reserveerimine**.
1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Töö on loodud kaupade teisaldamiseks komplekteerimise asukohast pakkejaama.

1. Jaotises **Müügitellimuse read** valige **Ladu \> Saadetise üksikasjad**.
1. Märkige ües saadetise ID lehel **Saadetise üksikasjad**. Vajate seda, kui pakite saadetist pakkimisjaamas.
1. Müügitellimuse juurde naasmiseks sulgege leht **Saadetise üksikasjad**.
1. Märkige müügitellimuse number üles ja avage **Laohaldus \> Töö \> Kogu töö**.
1. Kasutage müügitellimuse numbrit tellimuse jaoks loodud töö otsimiseks ja valimiseks.
1. Toiminguriba vahekaardil **Töö** valige suvand **Lõpeta töö**.
1. Valige lehel **Lõpeta töö** väljal **Kasutaja ID** kasutaja ID. Seejärel valige toimingupaanil suvand **Kinnita töö**.
1. Kui töö läbib valideerimise, valige toiminguriba vahekaardil suvand **Lõpeta töö**.

    Töö on märgitud lõpetatuks, et simuleerida kaupade liikumist pakkejaama.

#### <a name="pack-the-shipment"></a>Saadetise pakkimine

Saadetise pakkimiseks tehke järgmist.

1. Avage **Laohaldus \> Seadistamine \> Töötaja** ja veenduge, et teie kasutajakonto on seostatud laohalduse töötaja kontoga.
1. Avage jaotis **Laohaldus \> Komplekteerimine ja konteinerisse paigutamine \> Pakkimine**.
1. Dialoogiboksis **Pakkimisjaama valimine** määrake järgmised väärtused.

    - **Tegevuskoht:** *6*
    - **Ladu:** *62*
    - **Asukoht:** *Pakkimine*
    - **Pakkimisprofiili ID:** *demo pakkimisprofiil*

1. Valige nupp **OK**.
1. Kuvatakse leht **Pakkimine**. Tootmisstsenaariumis skannib töötaja litsentsiplaadi või saadetise ID. Kuid selle stsenaariumi puhul avage leht **Kõik saadetised** ja otsige saadetise numbrit, mille äsja lõite. Seejärel sisestage see väärtus väljale **Numbrimärk või saadetis** lehel **Pakkimine**. Teise võimalusena sisestage saadetise ID, mille olete varem üles märkinud.
1. Valige toimingupaanil nupp **Uus konteiner**.
1. Kuvatavas dialoogiboksis kuvatakse uue konteineri üksikasjad. Jätke vaikeväärtused ja seejärel valige **OK**.
1. Kauba pakkimiseks valige lehel **Pakkimine** kiirkaardil **Kauba pakkimine** väljal **Identifikaator** väärtus *A0002*. Kaup lisatakse konteinerisse.
1. Valige toimingupaanil suvand **Konteinerid saatmiseks**.

    Ilmuval lehel **Konteinerid saatmiseks** on rida konteineri jaoks. mille lõite. Sellel real on väli **Konteineri manifesti ID** praegu tühi, sest te pole veel saadetise silti ega jälgimisnumbrit vedajalt kätte saanud.

1. Valige toimingupaanil nupp **Sule konteiner**.
1. Dialoogiboksis **Konteineri sulgemine** määrake välja **Brutokaal** väärtuseks *1 kg* ja seejärel valige **OK**.

    Saadetise silt tuleb nüüd printida varem valitud ZPL-printeriga. See peals sarnanema järgmise näitega.

    ![Saadetise sildi näide](media/sps-label-example.png "Saadetise sildi näide")

1. Pange tähele, et **Konteineri manifesti ID** ja **Veose koguväärtus** on vedajalt saadud.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]