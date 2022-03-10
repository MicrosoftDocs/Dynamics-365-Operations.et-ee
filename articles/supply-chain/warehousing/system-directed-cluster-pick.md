---
title: Süsteemi suunatud kogumi komplekteerimine
description: Selles teemas antakse ülevaade süsteemi suunatud kogumi komplekteerimise kohta teenuses Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkCluster, WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3c474705e5260f4be62bc59d8d1d84a1ba597b6f96eafd8f673cc110285fc597
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772348"
---
# <a name="system-directed-cluster-picking"></a>Süsteemi suunatud kogumi komplekteerimine

[!include [banner](../includes/banner.md)]

Kogumi komplekteerimine on tükkhaaval komplekteerimise protsess, mis võimaldab teil samaaegselt komplekteerida erinevate tellimuste kaupu, kogudes need komplekteeritud kogumiteks. Peate seejärel külastama komplekteerimise asukohta ainult üks kord. Tavaliselt kasutatakse seda funktsiooni väikeste tellimuste komplekteerimisel või kogustes, mis on väiksemad kui juhtumi kogused.

Kui süsteemi suunatud kogumi komplekteerimine on seadistatud, saate süsteemi loodud kogumi põhjal komplekteerida kokku tööpäised. Süsteem kogub kokku nii palju tellimusi, kui on positsioonide arv, mis on kogumiprofiilis määratletud. Seega saate samaaegselt komplekteerida mitu tellimust ilma, et peaksite looma kogumi käsitsi.

Süsteemi suunatud kogumi komplekteerimine pakub alternatiivi käsitsi kogumi loomisele, kus kogumi loomiseks kasutatakse kogumiprofiili. Enne selle kasutamist tuleb kogumiprofiilis määratleda mitu seadistusega seotud rida.

- **Positsioonide arv** vastab tellimuste arvule, mis pannakse kogumisse. Seega vastab see koormate arvule.
- **Tükelda kogum** määrab, millal kogum tuleb tükeldada.
- **Loo kogumi ID** kontrollib seda, kas kogumi ID luuakse süsteemi poolt või sisestatakse kasutaja poolt.
- **Sortimise kontrollimistüüp** määrab, kas positsiooni kinnitamine on nõutav.

Süsteemi suunatud kogumi komplekteerimiseks kasutatakse uut mobiilse seadme menüü-üksust. Valitud suvandi **Juhtija** jaoks tuleb määrata **Kogumi profiili ID**. Lisaks saavad süsteemi suunatud töö järjestamise päringud rühmitada tellimusi ettevõttepõhiste kriteeriumide põhjal. Seega saate töökäskude määramist veelgi optimeerida, määrates süsteemi suunatud töö järjestuse päringute abil kohandatud sortimise kriteeriumid.

Kui süsteemi suunatud kogumi komplekteerimine on lubatud, antakse lao töötajatele kogum, kus komplekteerimise tellimused on eelmääratud kogumi positsioonidele. Seega saavad töötajad hakata komplekteerima kaupu mitme töökäsu jaoks, külastades komplekteerimise asukohta ainult üks kord. Süsteemi suunatud kogumi komplekteerimise komplekteerimisprotsess on sama, mis kasutaja suunatud kogumi komplekteerimise protsessil.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Süsteemi suunatud kogumi komplekteerimise lubamine

Enne selle funktsiooni kasutamist tuleb see teie süsteemis lubada. Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et kontrollida funktsiooni olekut ja vajaduse korral see lubada. Siin on funktsioon loetletud järgmiselt.

- **Moodul** – laohaldus
- **Funktsiooni nimi** – süsteemi suunatud kogumi komplekteerimine

See funktsioon eeldab ka sõltuva funktsiooni lubamist. Sõltuv funktsioon on järgmine.

- **Moodul** – laohaldus
- **Funktsiooni nimi** – organisatsiooniülene süsteemi suunatud töö järjestamine

## <a name="set-up-system-directed-cluster-picking"></a>Süsteemi suunatud kogumi komplekteerimise seadistamine

### <a name="create-cluster-profiles"></a>Kogumiprofiilide loomine

Kogumiprofiilid juhivad, kuidas süsteem iga kogumi loob. Kui nõutavad on erinevad kogumid, tuleb iga mobiilse seadme menüü-üksuse jaoks luua erineva kogumi profiili.

1. Avage **Laohaldus \> Seadistamine \> Mobiilne seade \> Kogumiprofiilid**.
2. Valige suvand **Uus**.
3. Väljale **Kogumiprofiili ID** sisestage **Positsioon 2**.
4. Väljale **Nimi** sisestage **Positsioon 2**.
5. Sisestage kiirkaardil **Üldine** järgmine teave.

    - **Loo kogumi ID** – valige **Jah**. See valik määrab, kas kogumi ID luuakse automaatselt süsteemi poolt või kasutaja loob selle komplekteerimise alguses. 
    - **Aktiveeri asukohad** – valige **Jah**. See valik määrab, kas positsiooni nimed luuakse positsiooni nime seadistuse põhjal automaatselt. Kui see suvand on seatud valikule **Ei**, kasutatakse positsiooni litsentsiplaadi identifikaatorit.
    - **Positsioonide arv** – valige **2**. See väli määrab positsioonide maksimaalse arvu, mida kogum võib omada (st maksimaalne arv kaste, koormaid jne).
    - **Positsiooni nimi** – valige **Numbriline**, et positsioonidele antaks nimed järjestikuseid numbreid kasutades. Kui valite suvandi **Tähestikkuline**, nimetatakse positsioonid tähestikulises järjekorras.
    - **Tükelda kogum asukohas**– valige **Pane**. See väli määratleb, millal kogum katkestatakse. 
    - **Sortimise kontrollimistüüp** – valige **Positsiooni skannimine**. See väli määrab, kas positsiooni panemise etapp on kinnitatud.
        
6. Kiirkaardil **Kogumi sortimine** saate määratleda sortimise kriteeriumid, luues uue rea ja sisestades järgmise teabe.

    - **Numbriseeria** – valige **1**. See väli määrab järjestuse, mille alusel süsteem sordib. Väärtus sisestatakse automaatselt, kuid saate seda vajadusel muuta.
    - **Välja nimi** – sisestage **WMSLocationId**. See väli määrab välja, mida rida kriteeriumide sortimiseks kasutab.
    - **Sortimine** – valige **Kasvav**. See väli määrab, kas sortimine toimub kasvavas või kahanevas järjestuses.

### <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine

Süsteemi suunatud kogumi komplekteerimiseks uue mobiilse seadme menüü-üksuse loomiseks ja kogumiprofiili ID linkimiseks mobiilse seadme menüü-üksusega, toimige järgmiselt.

1. Avage **Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüükäsud**.
1. Valige suvand **Uus**.
1. Sisestage päise jaotises järgmine teave.
    - **Menüükäsu nimi** – SD kogum
    - **Pealkiri** – SD kogum
    - **Režiim** – töö
    - **Kasuta olemasolevat tööd** – Jah

1. Sisestage kiirkaardil **Üldine** järgmine teave.
    - **Juhataja** – süsteemi suunatud kogumi komplekteerimine
    - **Loo litsentsiplaat** – jah
    - **Kogumiprofiili ID** – positsioon 2

1. Seadistage kiirkaardil **Töö klassid** selle mobiilse seadme menüü-üksuse kehtiv töö klass, seadistades järgmised väljad:
    - **Tööklassi ID** – müük
    - **Töökäsu tüüp** – müügitellimused

1. Valige toimingupaanil **Mobiilse seadme menüükäsud** suvand **Süsteemi suunatud töö järjestamisjärjestused** ja järgige uue süsteemi suunatud töö järjestamisjärjestuse sätestamiseks järgmisi etappe.
    - Valige toimingupaanil **Uus**.
    - **Järjekorranumber** – 1
    - **Kirjeldus** – töö prioriteet – töö ID

1. Valige toimingupaanil **Päringu redigeerimine**
1. Valige vahekaart **Sortimine**
1. Valige uue rea lisamiseks suvand **Lisa** ja sisestage järgmine teave.
    - **Tabel** – töö
    - **Tuletatud tabel** – töö
    - **Väli** – töö prioriteet
    - **Otsingusuund** – kasvav
1. Valige teise rea lisamiseks suvand **Lisa** ja sisestage järgmine teave.
    - **Tabel** – töö
    - **Tuletatud tabel** – töö
    - **Väli** – töö ID
    - **Otsingusuund** – kasvav

1. Süsteem sordib nüüd töö ID-d kogumis, kõigepealt töö prioriteedi ja seejärel töö ID järgi.

### <a name="set-up-a-mobile-device-menu"></a>Mobiilse seadme menüü seadistamine

1. Avage **Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü**.
1. Lisage mobiilse seadme menüüle äsja loodud menüükäsk **SD kogum**.
1. Valige menüü **Väljaminev**.
1. Valige toimingupaanil **Redigeeri**.
1. Kerige, kuni leiate suvandi **SD kogum**.
1. Valige suvand **SD kogum**, loendile **Menüüstruktuur** viitav nool lubatakse.
1. Valige nupp **nool**, et liigutada menüükäsk **SD kogum** menüüstruktuuri **Väljaminev**.
1. Valige loendist **Menüüstruktuur** suvand **SD kogum** ja seejärel klõpsake menüükäsu mobiilse seadme menüüs sobivasse asendisse liigutamiseks noolel **ÜLES** või **ALLA**.

## <a name="scenario"></a>Stsenaarium

### <a name="create-picking-work"></a>Komplekteerimistöö loomine

Enne süsteemi suunatud kogumi komplekteerimise seadistamist peate looma sobiliku väljamineva töö. Varasemalt loodud kogumiprofiil määrab kaks kogumi positsiooni. Seetõttu peate looma vähemalt kaks töö ID-d. Sellise stsenaariumi puhul loote kaks müügitellimust, reserveerite varud, väljastate müügitellimused lattu ning töötlete voogu seejärel käsitsi.

1. Avage **Müük ja turundus > Müügitellimused > Kõik müügitellimused**.
1. Toimingupaanil esimese müügitellimuse loomiseks vajutage **Uus**.
    - Avaneb menüü **Müügitellimuse loomine**, sisestage järgmine teave.
        - Sisestage kiirkaardil **Klient** väärtus **Kliendikonto** - **US-004**.
        - Sisestage kiirkaardil **Üldine** väärtus **Ladu** - **62**.
        - Tehke menüü sulgemiseks valik **OK** ja looge müügitellimus.
    - Kui uut rida ei lisata automaatselt, siis valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida** ja sisestage järgmine teave.
        - **Kauba kood** – A0001
        - **Kogus** – 1
        - Teise rea lisamiseks valige **Lisa rida**.
        - **Kauba kood** – A0002
        - **Kogus** – 3
    - Reserveerige varud mõlema äsja loodud rea jaoks.
        - Valige **Rida 1**.
        - Valige toimingupaanil **Müügitellimuse read** suvand **Varud** ja seejärel valige loendist **Reserveerimine**.
        - Valige vormil **Reserveerimine** varude reserveerimiseks suvand **Reserveeri saatepartii**.
        - Kui reserveerimine on lõpule viidud, siis sulgege vorm **Reserveerimine**.
        - Korrake varude reserveerimise samme ka suvandi **Rida 2** puhul.
1. Toimingupaanil teise müügitellimuse loomiseks vajutage **Uus**
    - Avaneb menüü **Müügitellimuse loomine**, sisestage järgmine teave.
        - Sisestage kiirkaardil **Klient** väärtus **Kliendikonto** - **US-005**.
        - Sisestage kiirkaardil **Üldine** väärtus **Ladu** - **62**.
        - Tehke menüü sulgemiseks valik **OK** ja looge müügitellimus
    - Kui uut rida ei lisata automaatselt, siis valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida** ja sisestage järgmine teave.
        - **Kauba kood** – A0001
        - **Kogus** – 4
        - Teise rea lisamiseks valige **Lisa rida**.
        - **Kauba kood** – A0002
        - **Kogus** – 2
    - Reserveerige varud mõlema äsja loodud rea jaoks.
        - Valige **Rida 1**.
        - Valige toimingupaanil **Müügitellimuse read** suvand **Varud** ja seejärel valige loendist **Reserveerimine**.
        - Valige vormil **Reserveerimine** varude reserveerimiseks suvand **Reserveeri saatepartii**.
        - Kui reserveerimine on lõpule viidud, siis sulgege vorm **Reserveerimine**.
        - Korrake varude reserveerimise samme ka suvandi **Rida 2** puhul.
    - Sulgege müügitellimus ja minge tagasi lehele, kus on loend **Kõik müügitellimused**.
1. Leidke kaks äsja loodud müügitellimust (võimalik, et peate selleks lehte värskendama). Valige tabelis jaotise kontrollmärget kasutades mõlemad müügitellimused.
    - Valige toimingupaanil **Kõik müügitellimused** vahekaart **Ladu**.
    - Valige grupis **Toimingud** suvand **Lattu väljastamine**, et väljastada mõlemad müügitellimused lattu.
1. Kui lattu väljastamise protsess on lõpule viidud, siis kuvatakse teabeteade.
    - Iga müügitellimuse kohta luuakse saadetised.
    - Luuakse voog ja mõlemad saadetised määratakse voogu. Märkige üles **Voo ID**.
1. Avage **Laohaldus > Väljaminevad vood > Saadetise vood > Kõik vood**.
    - Leidke ja valige loendis **Kõik vood** **Voo ID**, mille eelmises etapis lõite.
    - valige toimingupaanil vahekaart **Voog**.
    - Valige grupis **Voog** suvand **Töötlemine**, et töödelda ja luua vastav **Töö**.
    - Kui töötlemine on lõpule viidud, siis kuvatakse informatiivsed teated, mis näitavad, et töö on loodud ja voog on sisestatud.
1. **Valikuline**: avage loodud töö vaatamiseks **Laohaldus > Töö > Töö üksikasjad**. Luuakse kaks erinevat töö ID-d. Igal töö ID-l on kaks komplekteerimisrida.

### <a name="run-the-mobile-device-flow"></a>Mobiilse seadme voo käitamine

1. Logige mobiilsesse seadmesse lao **62** kasutaja jaoks sisse.
1. Valige **Peamenüüs** suvand **Väljaminev**.
1. Komplekteerimise käivitamiseks valige menüüs **Väljaminev** suvand **SD kogum**.
    - Luuakse kogum ja lisatakse kaks varem loodud töö ID-d. Kui lõite rohkem kui kaks töö ID-d, lisatakse kogumile ainult kaks esimest. Pange tähele, et töö ID-d lisatakse kogumile kasvavas järjestuses, nagu määrasite päringu häälestuses.

    > [!NOTE]
    > Uus kogum luuakse automaatselt ainult siis, kui eelnevalt on loodud piisavalt täiendavaid töö ID-sid. Vastasel juhul kuvatakse järgmine teade: „Kogumi jaoks ei leidu piisavalt tööd”.

    - Pärast menüü valimist ilmub esimene komplekteerimiskuva. Süsteem koondab kõik ühtivad komplekteerimisread kahest töö ID-st ja suunab teid külastama komplekteerimise asukohta üks kord, nii et saate täita mõlemad tellimused ühe komplekteerimisega. See protsess teostatakse samamoodi nagu kasutaja suunatud kogumi komplekteerimise protsess.

1. Kinnitage esimese komplekteerimise asukoht ja kaup, valides **OK**.
    - Komplekteeritav kogus on kogumis müügitellimuste juures kujutatud kaupade kogusumma.
1. Sisestage positsiooni nimi (numbrites või tähemärkides), et kinnitada, et positsiooni jaoks komplekteeritud kaupade kogus paigutati õigesse asukohta.
1. Korrake seda protsessi seni, kuni kõik kaubakogused on komplekteeritud ja õigesse kohta pandud.
1. Mobiilse seadme viimane etapp on suvand **Pane**, millega pannakse kogum lõplikku asukohta. Valige **OK**
    - Kui see panemise toiming kinnitatakse, kogum suletakse ja tükeldatakse vastavalt väärtusele, mille määrasite kogumiprofiilis väljale **Tükelda kogum asukohas**. Töö ID-d on samuti suletud.
1. Mobiilsel seadmel kuvatakse teade „Kogum lõpetatud”.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]