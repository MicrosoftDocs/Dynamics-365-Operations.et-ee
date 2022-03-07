---
title: Pitseeritud pakkumine pakkumiskutsete puhul
description: See teema kirjeldab, kuidas seadistada pitseeritud pakkumine, et hoida müüja pakkumise vastused saladusse seni, kuni ostupersonal neid pitseerib.
author: Henrikan
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 96549b6053ba75f2d5b9a85bcd5b7feb006f0f1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578076"
---
# <a name="sealed-bidding-for-rfqs"></a>Pitseeritud pakkumine pakkumiskutsete puhul

[!include [banner](../includes/banner.md)]

Pitseeritud pakkumine hoiab müüja pakkumise vastused saladusse seni, kuni ostupersonal neid pitseerib. Kõik pakkumiskutsega seotud pakkumised (RFQ) saab pakkumise lõppemisel esmalt sulgeda. Enne pakkumise avanemist pääsevad sellele juurde ainult kasutajad, kellel on sihtotstarbeline kasutajaroll ja kes esindab müüjat.

> [!IMPORTANT]
> Vormide muutmine ja laiendamine või uute vormide ja äriloogika loomine võib rikkuda Microsofti suletud pakkumiste kaitset. Te kannate riski kasutades muudatusi, laiendusi, uusi vorme või äriloogikat või ei saa selliste muudatuste, laienduste, uute vormide või äriloogika tõttu kasutada suletud pakkumisfunktsiooni.  Microsoft ei vastuta kahjude eest, mis tulenevad vormide muudatustest või laiendustest, teie loodud uutest vormidest või äriloogikast või mis tahes kolmanda osapoole eest. Microsoft ei paku tehnilist ega muud tuge teie või kolmanda osapoole poolt tehtud muudatustele, laiendustele, uutele vormidele ega äriloogikale. Te olete ainuisikuliselt vastutav kõigi kinniste pakkumistega seotud kehtivate seaduste või eeskirjade järgimise eest.

## <a name="how-bids-are-kept-secure"></a>Kuidas hoitakse pakkumisi turvalisena

Pitseeritud pakkumine kasutab asümmeetrilist krüptimist, et krüptida pakkumise krüptimisvõtit (KEK) ja sümmeetrilist krüptimist tegeliku pakkumise krüptimiseks. Süsteem integreerub võtmega Microsoft Azure Key Vault, et luua ja hallata krüptimisvõtmeid, mida kasutatakse pitseeritud pakkumiste krüptimiseks. Igal pakkumisel on oma krüptimisvõti. See krüptimine hoitakse seifis võtmehoidlas, mis kuulub organisatsioonile, kes käitab rakendust Dynamics 365 Supply Chain Management. Süsteem pääseb võtmehoidlasse nõudmisel juurde alati, kui on vaja krüptimist ja dekrüpteerimist.

## <a name="setup-and-configuration"></a>Seadistamine ja konfigureerimine

See jaotis kirjeldab eeltingimusi, mis peavad olema enne, kui saate saata välja pakkumiskutsed, mis nõuavad pitseeritud pakkumist.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>1. etapp: kasutaja juurdepääsu seadistamine pitseeritud pakkumisele

Kui kasutate pitseeritud pakkumist, saavad ainult müüja kontaktisikuks määratud kasutajad selle müüja pakkumisi vaadata, redigeerida ja esitada kuni pakkumise perioodi lõpuni. Nendel kasutajatel peab olema **Müüja (väline)** roll ja nad tuleb seadistada müüja konto kontaktisikuks. Kontaktisikul peab olema ka müüja koostöö luba, nagu on kirjeldatud jaotises [Müüja koostöö häälestamine ja hooldamine](set-up-maintain-vendor-collaboration.md).

Kuna kasutajatel, kellel on vastavad õigused ja kes on seadistatud hankija kontaktidena, on hankija pitseeritud pakkumistele juurdepääs, on oluline jälgida nende kasutajate õigusi. Kasutajaid ja turberolle seadistav süsteemiadministraator vastutab pitseeritud pakkumistele juurdepääsu piiramise eest nendele kasutajatele, kellel on nende vaatamiseks tõepoolest lubatud.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>2. etapp: pitseeritud pakkumise funktsiooni lubamine

Enne, kui alustate selle funktsiooni seadistamist või kasutamist, peate veenduma, et see oleks teie süsteemis saadaval. Administraatorid saavad kasutada **[Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *hanked*
- **Funktsiooni nimi:** *pakkumiskutse pitseeritud pakkumine*

### <a name="step-3-set-up-azure-key-vault"></a>3. etapp: Azure'i võtmehoidla häälestus

Supply Chain Management kasutab krüptimisvõtmeid, et kaitsta kõiki pitseeritud pakkumisi ja hoida neid seni, kuni see on sobiv aeg. See kasutab võtmehoidla võimalusi vajalike võtmete loomiseks ja haldamiseks. Seetõttu peate süsteemi lubamiseks häälestama ühenduse rakenduse Supply Chain Management ja võtmehoidla vahel.

> [!IMPORTANT]
> Turvahoidlad, mida kasutate pitseeritud pakkumiseks, peavad vastama järgmistele nõuetele:
>
> - Kui kasutate arenduseks ja testimiseks kausta, siis peab teil olema üks sihtotstarbelise võtme vault boksi jaoks ja eraldi kaust tootmiseks.
> - Iga võtmehoidla tuleb luua Azure'i kordustellimuses, mis kuulub teie organisatsioonile (ei ole tellimus, kus käitate rakendust Supply Chain Management).
> - Iga võtmehoidlat tuleb kasutada ainult pitseeritud pakkumise jaoks. Te ei tohi kasutada oma pitseeritud-pakkumise võtmehoidlaid mis tahes muudel eesmärkidel.

Iga pakkumine pärib oma salavõtme. Seda võtit kasutatakse iga kord, kui kasutaja vaatab, uuendab või eemaldab pakkumise.

Võtmehoidla loob võtme, mida kasutatakse saladuse toomiseks, kui müüja valib müüja koostöö liideses **Pakkumine**. Võti aegub siis pärast fikseeritud aega, mille hankehaldur **hanke- ja hankeparameetrite** lehel rakenduses Supply Chain Management seadistab. Pärast võtme aegumist ei saa keegi pakkumist vaadata, redigeerida ega tühistada. Seetõttu on oluline konfigureerida võtme aegumine, nii et pakkumise protsessiks on piisavalt aega.

Järgmise kolme etapiga seadistate ühenduse võtmehoidlaga. Kõigepealt seadistate pakkumise pitseeritud pakkumisega kasutamiseks võtmehoidla. Järgmiseks konfigureerite rakendust Supply Chain Management suhtlema võtmehoidlaga. Lõpuks seadistate te võtmele aegumisaja.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>4. etapp: seadistage pakkumise pitseeritud pakkumisega kasutamiseks võtmehoidla

Oma võtmehoidla häälestuseks läbige need etapid. Sammude järjekord on oluline.

1. Kui te pole veel seadistanud Azure'i kordustellimust, mis on eraldi kordustellimusest, kus käitate rakenduse Supply Chain Management, seadistage see.
1. Seadistage turvavõti eraldi Azure'i ladustamiseks. Lisateavet leiate jaotisest [Azure'i võtmehoidla salvestusruumi haldamine](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Seadistage Supply Chain Management rakendus töötama oma võtmehoidla kliendina. Lisateavet leiate jaotisest [Azure'i võtmehoidla kliendi häälestamine](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>5. etapp: võtmehoidla parameetrite konfigureerimine rakenduses Supply Chain Management

Rakenduse Supply Chain Management konfigureerimiseks, et pidada ühendust turvahoidlaga pitseeritud pakkumise ajal, järgige neid samme.

1. Logige rakendusse Supply Chain Management sisse ja minge **Süsteemihaldus \> Häälestus \> Võtmehoidla parameetrid**.
1. Valige kirje loomiseks **Uus** ja seadke selle jaoks järgmised väljad:

    - **Nimi** - sisesta nimi.
    - **Kirjeldus** - sisesta kirjeldus.
    - **Võtmehoidla URL** – sisesta oma võtmehoidla vaike-URL.
    - **Võtmehoidla klient** – sisestage autentimiseks võtmehoidlaga seotud Active Directory rakenduse interaktiivne kliendi-ID.
    - **Võtmehoidla salavõti** – sisestage tunnistuse salaviide.
    - **Lubatud pitseeritud pakkumine** – määrake selle suvandi väärtuseks *Jah*.

![Võtmehoidla parameetrite leht](media/sealed-bidding-key-vault-param.png "Võtmehoidla parameetrite leht")

> [!NOTE]
> Saate lubada korraga pitseeritud pakkumise jaoks ainult ühe võtmehoidla konfiguratsiooni. Enne olemasoleva võtmehidla konfiguratsiooni keelamist peate veenduma, et kõik seda kasutavad pitseeritud pakkumised on pitseeritud. Kontrollige kõiki *Pitseeritud* tüüpi pakkumiskutse RFQ-juhtumit ja veenduge, et kõik selle vastused on pitseeritud.

### <a name="step-6-set-the-key-expiration-time"></a>6. etapp: määrake võtme aegumisaeg

Iga uue pakkumise jaoks loodud võtmele rakendatav aegumisaeg tuleb seadistada järgmiselt.

1. Minge **Hangete parameetrid \> Seadistus \> Hangete parameetrid**.
1. Sisestage pakkumiskutse perioodi viimane päevade arv vahekaardi **Pakkumiskutse** **vastas** väljale. Pakkumiskutse loomisel lisatakse siia sisestatud päevade arv süsteemi kuupäevale pakkumiskutse vaikimisi aegumiskuupäeva määratlemiseks.
1. Sisestage **krüptimisvõtme aegumispäeva vastaskonto** väljale päevade arv, millal iga krüptimisvõti pärast selle väljastamist kehtima peaks. Pärast krüptimisvõtme aegumist ei saa keegi seda kasutatavat pitseeritud pakkumist vaadata, redigeerida ega tühistada.

> [!TIP]
> **Krüptimisvõtme aegumispäeva vastas** välja väärtus ei tohi olla väiksem kui välja **Päevade tasakaalutuse** väärtus.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>7. etapp: määrake pakkumise vaiketüüp

Igal pakkumiskutse juhtumil on pakkumise tüüp. Pakkumise tüüp määratleb, kas pakkumiskutse juhtum pakub avatud või pitseeritud pakkumise.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Pakkumiskutse juhtumid, millel pakkumiskutse tüüpi pole

Uutele pakkumiskutse juhtumitele määratud vaikimisi pakkumise tüübi määramiseks, millele pole loomisel määratud pakkumiskutse tüüpi, järgige neid samme.

1. Minge **Hangete parameetrid \> Seadistus \> Hangete parameetrid**.
1. Seadke vahekaardil **Pakkumiskutse** väli **Pakkumise tüüp** väärtusele *Pitseeritud*.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Pakkumiskutse juhtumid, millel pakkumiskutse tüüp on

Uutele pakkumiskutse juhtumitele määratud vaikimisi pakkumise tüübi määramiseks, millele on loomisel määratud pakkumiskutse tüüp, järgige neid samme.

1. Valige **Hanked \> Seadistus \> Pakkumiskutse \> Kutse tüüp**.
1. Looge uus pakkumistüüp või valige olemasolev pakkumistüüp, kus soovite kasutada *pitseeritud* pakkumise tüüpi.
1. Määrake välja **Pakkumise tüüp** väärtuseks *Pitseeritud*.
1. Korrake neid samme iga täiendava pakkumistüübi puhul, kus soovite rakendada pitseeritud pakkumist.

> [!TIP]
> Pakkumiskutse tüüp ei pea uue pakkumiskutse loomisel olema määratud. Kui määratud on pakkumiskutse tüüp, saab pakkumiskutse vaiketüüp saab selle tuua. Vastasel juhul saab kasutada hankeparameetrites määratletud pakkumise vaiketüüpi.

## <a name="the-sealed-bidding-process"></a>Suletud pakkumisprotsess

Pitseeritud pakkumine järgib peaaegu sama protsessi, mida kirjeldatakse [Pakkumiskutsete (RFQ) ülevaates](request-quotations.md). Peamine erinevus on see, et pakkumise andmed ja nende manused krüptitakse seni, kuni pakkumise avamine on läbitud.

> [!IMPORTANT]
> [Küsimustikud](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) pole krüpteeritud ja neid ei tohiks kasutada tundliku teabe kogumiseks

Siin on protsessi ülevaade.

1. Pakkumiskutse loomine ja saatmine ühele või mitmele hankijale.
1. Müüjad vastavad, esitades oma pitseeritud pakkumise.
1. Te eemaldate pakkumised pärast pakkumise sisestamise aegumisaega.
1. Pakkumised muutuvad nähtavaks ning te saate neid hinnata ja võrrelda.
1. Kui pakkumine on aktsepteeritud, saate luua ostutellimuse, luua ostulepingu või värskendada ostutaotlust.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Pakkumiskutse juhtumi loomine, mis kasutab pitseeritud pakkumist

Pitseeritud pakkumise pakkumiskutse juhtumi loomine on peaaegu sama, mis pitseerimata pakkumise protsess. Teavet mõlemat tüüpi pakkumiskutse juhtumite loomise kohta vt [Pakkumiskutse loomine](tasks/create-request-quotation.md). Selles jaotises tõstetakse esile mõned olulised kaalutlused pakkumiskutse loomisel pitseeritud pakkumise jaoks.

Pitseeritud pakkumise pakkumiskutse **pakkumise tüüp** peab olema *Pitseeritud*. Pakkumiskutse juhtumile väärtuse määramiseks on kolm võimalust:

- Saate väärtuse seadistada pakkumiskutse juhtumile pärast selle loomist otse.
- Saate määratleda pakkumise pitseeritud pakkumise vaiketüübina kõigi hanke- ja hankeparameetrite pakkumiskutsete juhtumite puhul. (Vt Määrake selles teemas varasemalt toodud [Pakkumise vaiketüübi määramine](#set-default-bid-type).)
- Uue pakkumiskutse juhtumi loomisel valige pakkumistüüp, mis on seadistatud pitseeritud pakkumiseks. (Vt jaotist [Pakkumise vaiketüübi määramine](#set-default-bid-type).)

Pitseeritud pakkumise puhul määrab pakkumiskutse juhtumi **aegumiskuupäev ja -kellaaeg**, millal edastatud pakkumistelt saab pitseri eemaldada. Iga rea **aegumiskuupäev ja -kellaaeg** ühtivad päise väärtusega.

Te ei saa muuta pakkumise tüüpi pärast pakkumiskutse juhtumi saatmist.

### <a name="vendors-respond-to-an-rfq"></a>Müüjad vastavad pakkumiskutsele

Pitseeritud pakkumisele reageerivad hankijad kasutavad samu protseduure, mida nad kasutavad avatud pakkumistele vastamiseks, nagu on välja toodud [Pakkumiskutsetega töötamine müüja pakkumise tööruumis](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Üksikasjalikke juhiseid selle kohta, kuidas töötada nii avatud pakkumiste kui ka pitseeritud pakkumistega, vt [Pakkumiskutsete ja preemialepingute sisestamine ja võrdlemine](tasks/enter-compare-rfq-bids-award-contracts.md). Ainus erinevus pitseeritud pakkumiste töötlemise ja avatud pakkumiste töötlemise vahel on see, et pakkumise perioodi lõpuni ei saa hankespetsialistid avada müüja pitseeritud pakkumist. Ainult müüja kontaktisik saab avada selle müüja pitseeritud pakkumise.

> [!IMPORTANT]
> Pitseeritud pakkumise puhul saavad hankijad manuseid üles laadida ainult PDF-vormingus. Muid vorminguid ei aktsepteerita.

Kui registreeritud müüjast kasutaja on pitseeritud pakkumise pakkumiskutses valiku **Pakkumine** valimas, saavad nad sisestada pakkumise andmed ja andmed säilitatakse turvaliselt. Müüjad saavad oma töö salvestada nii, nagu nad pakkumise ette valmistavad, naasta selle juurde nii tihti, kui vaja ja seejärel esitada selle, kui see on valmis. Müüjad saavad ka vaadata oma pakkumist pärast selle esitamist. Kui müüjad peavad pakkumise pärast selle esitamist muutma, saavad nad selle tagasi kutsuda, värskendada ja selle pakkumise mis tahes ajal uuesti esitada, kuni pakkumise periood lõpeb.

Pitseeritud pakkumise ajal kehtivad järgmised tingimused:

- Pitseeritud pakkumise ajal loob süsteem *Pakkumiskutse* töölehe.
- Kui müüja esitab pakkumise, luuakse pitseeritud hinnaga pakkumiskutse töölehed ilma ridadeta.
- Kui juhtum on avamata, luuakse pakkumiskutse töölehed, mis omavad hinda ja summat. Sellele töölehele pääsete juurde valides lehel **Kõik pakkumiskutsed** **Pakkumisekutse töölehed**.
- Süsteem säilitab kõigi toimingute logi, mida kasutajad pitseeritud pakkumisega teevad. Need tegevused hõlmavad pakkumise vaatamist, redigeerimist ja salvestamist. See logi on nähtav nii müüjale kui ka hankespetsialistidele, kellel on juurdepääs pakkumisele.
- Pakkumise edenemise käigus saavad hankespetsialistid vaadata selle olekut. Olek on kas *Müüja värskendab* või *Müüja edastatud*.
- Pitseeritud pakkumise ridade olek jääb *saadetuks*, kuni pakkumise pitser suletakse.
- Kui müüja otsustab pakkumisest keelduda, on pakkumise oleku *Müüja poolt tagasi lükatud* väärtuseks **Vasta progressile**. See olek on hankepersonali jaoks nähtav.
- Küsimustike vastuseid **ei** talletata andmebaasis krüptitud vormil. Seetõttu pole need pitseeritud. Need pole pakkumiskutse kasutajaliideses nähtavad enne, kui juhtum on avamata.

### <a name="all-sealed-bid-activities-are-logged"></a>Kõik pitseeritud pakkumise tegevused on logitud

Üksikasjalik logikirje salvestab pakkumise kõik kasutaja tegevused. Tegevuslogi võimaldab organisatsioonidel määrata, kes uuendas pakkumise oma eluea jooksul ja millised uuendused olid. Samuti võimaldab see organisatsioonidel kinnitada, et pitseeritud pakkumisele pääsesid juurde ainult volitatud inimesed. Tegevuste logi on saadaval igal pakkumise **tegevuse** lehel.

### <a name="review-rfq-activity"></a>Pakkumiskutse tegevuse ülevaatamine

Iga suhtlus pakkumisega logitakse ja seda saab vaadata lehel **Tegevus**. Järgmisel joonisel on toodud näide.

![Tegevuse lehe näide](media/sealed-bidding-rfq-activity.png "Tegevuse lehe näide")

Müüjad pääsevad juurde **tegevuse** leheküljele, valides **tegevuse** **Päring pitseeritud pakkumisele** lehel. Hankepersonal pääseb sellele juurde, valides **Pakkumiskutse** lehel **Tegevus**. Tegevuslogi tagab pakkumisele pääsenud müüjate ja hankepersonali täieliku ülevaate. Seega võib see näidata mis tahes volitamata juurdepääsu.

### <a name="unseal-sealed-bids"></a>Pitserimata pakkumised

Kui pitseeritud pakkumise pakkumiskutse juhtumi jaoks konfigureeritud **aegumiskuupäev ja -kellaaeg** on möödas, muutub nupp **Eemalda pitset** kättesaadavaks. Valige Käsk **Eemalda pitser**, et eemaldada valitud pakkumiskutse juhtumi kõik pakkumised. Kõik pakkumise andmed ja manused muutuvad nähtavaks, et juhtumi vastuseid saaks hallata. Lisaks luuakse töölehed, mis sisaldavad edastatud pakkumise andmeid.

Pitsri eemaldamise sündmus logitakse ja seda saab vaadata lehel **Tegevus**.

### <a name="process-accepted-bids"></a>Aktsepteeritud pakkumiste protsess

Varem pitseeritud pakkumiste võrdlemise ja kinnitamise protsess on sama, mis avatud pakkumiste protsess. Teavet selle kohta, kuidas skoorida, võrrelda, tagasi lükata ja aktsepteerida avamata pakkumisi, vaadake [Pakkumiskutsete pakkumiste ja preemialepingute sisestamine ja võrdlemine](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>Pakkumiskutse tegevuslogi ei saa kunagi kustutada

Keegi, isegi mitte administraatorid ja Microsoft Support, saab pakkumiskutse tegevuslogi redigeerida või kustutada. See piirang aitab kindlustada pitseeritud pakkumise protsessi õiglust. See aitab ka tagada täpse kontrolljälje säilitamist.
