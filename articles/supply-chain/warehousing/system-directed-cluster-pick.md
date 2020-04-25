---
title: Süsteemi suunatud kogumi komplekteerimine
description: Selles teemas antakse ülevaade süsteemi suunatud kogumi komplekteerimise kohta teenuses Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 390e0a3379a6482e99a13f4f7835b5264e3747ac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217237"
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

Süsteemi suunatud kogumi komplekteerimiseks kasutatakse uut mobiilse seadme menüü-üksust. Suvandi **Juhtija** jaoks tuleb määrata kogumi profiili ID. Lisaks saab süsteemi suunatud päringu tellimus rühmitada tellimusi ettevõttepõhiste kriteeriumite põhjal. Seega saate töökäskude määramist veelgi optimeerida, määrates süsteemi suunatud päringu tellimusele kohandatud sortimise kriteeriumid.

Kui süsteemi suunatud kogumi komplekteerimine on valmis, antakse lao töötajatele kogum, kus komplekteerimise tellimused on eelmääratud kogumi positsioonidele. Seega saavad töötajad hakata komplekteerima kaupu mitme töökäsu jaoks, külastades komplekteerimise asukohta ainult üks kord. Süsteemi suunatud kogumi komplekteerimise komplekteerimisprotsess on sama, mis kasutaja suunatud kogumi komplekteerimise protsessil.

## <a name="set-up-system-directed-cluster-picking"></a>Süsteemi suunatud kogumi komplekteerimise seadistamine

### <a name="create-cluster-profiles"></a>Kogumiprofiilide loomine

Kogumiprofiilid juhivad, kuidas süsteem iga kogumi loob. Kui nõutavad on erinevad kogumid, tuleb iga mobiilse seadme menüü-üksuse jaoks luua erineva kogumi profiili.

1. Avage **Laohaldus \> Seadistamine \> Mobiilne seade \> Kogumiprofiilid**.
2. Valige suvand **Uus**.
3. Väljale **Kogumiprofiili ID** sisestage **Positsioon 2**.
4. Väljale **Nimi** sisestage **Positsioon 2**.
5. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Loo kogumi ID:** määrake see suvand valikule **Jah**. See valik määrab, kas kogumi ID luuakse automaatselt süsteemi poolt või kasutaja loob selle komplekteerimise alguses.
    - **Aktiveeri positsioonid:** määrake see suvand valikule **Jah**. See valik määrab, kas positsiooni nimed luuakse positsiooni nime seadistuse põhjal automaatselt. Kui see suvand on seatud valikule **Ei**, kasutatakse positsiooni litsentsiplaadi identifikaatorit.
    - **Positsioonide arv:** sisestage **2**. See väli määrab positsioonide maksimaalse arvu, mida kogum võib omada (st maksimaalne arv kaste, koormaid jne).
    - **Positsiooni nimi:** valige **Numbriline**, et positsioonidele antaks nimed järjestikkuseid numbreid kasutades. Kui valite suvandi **Tähestikkuline**, nimetatakse positsioonid tähestikulises järjekorras.
    - **Tükelda kogum asukohas:** valige suvand **Pane**. See väli määratleb, millal kogum katkestatakse.
    - **Sortimise kontrollimistüüp:** valige suvand **Positsiooni skannimine**. See väli määrab, kas positsiooni panemise etapp on kinnitatud.

6. Kiirkaardil **Kogumi sortimine** saate määratleda sortimise kriteeriumid, luues uue rea ja seadistades järgmised väljad:

    - **Järjekorranumber:** see väli määrab süsteemi sortimise järjestuse. Väärtus sisestatakse automaatselt, kuid saate seda vajadusel muuta.
    - **Välja nimi:** valige **WMSLocationId**. See väli määrab välja, mida rida kriteeriumide sortimiseks kasutab.
    - **Sortimine:** valige suvand **Kasvav**. See väli määrab, kas sortimine toimub kasvavas või kahanevas järjestuses.

### <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine

Süsteemi suunatud kogumi komplekteerimiseks uue mobiilse seadme menüü-üksuse loomiseks ja kogumiprofiili ID linkimiseks mobiilse seadme menüü-üksusega, toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
2. Valige suvand **Uus**.
3. Väljale **Menüü-üksuse nimi** sisestage **SD kogum**.
4. Väljale **Pealkiri** sisestage **SD kogum**.
5. Valige väljal **Režiim** suvand **Töö**.
6. Valige suvandi **Kasuta olemasolevat tööd** sätteks **Jah**.
7. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Suunaja:** valige suvand **Süsteemi suunatud**.
    - **Loo litsentsiplaat:** määrake see suvand valikule **Jah**.
    - **Kogumiprofiili ID:** valige **Positsioon 2**.

8. Seadistage kiirkaardil **Töö klassid** selle mobiilse seadme menüü-üksuse kehtiv töö klass, seadistades järgmised väljad:

    - **Töö klassi ID:** veenduge, et sisestatud oleks **Müük**.
    - **Tööklassi tüüp:** veenduge, et sisestatud oleks **Müügitellimused**.

9. Uue süsteemi suunatud töö järjestuse päringu määramiseks tehke järgmist.

    1. Valige suvand **Uus**.
    2. Sisestage väljale **Järjekorranumber** väärtus **1**.
    3. Väljal **Kirjeldus** valige **Töö prioriteet – Töö ID**.

10. Valige menüüs käsk **Redigeeri päringut**.
11. Vahekaardil **Sortimine** seadke järgmised väljad:

    - **Tabel:** valige suvand **Töö**.
    - **Tuletatud tabel:** valige suvand **Töö**.
    - **Väli:** valige **Töö prioriteet**.
    - **Otsingusuund:** valige **Kasvav**.
    - **Tabel:** valige suvand **Töö**.
    - **Tuletatud tabel:** valige suvand **Töö**.
    - **Väli:** valige **Töö ID**.
    - **Otsingusuund:** valige **Kasvav**.

Süsteem sordib nüüd töö ID-d kogumis, kõigepealt töö prioriteedi ja seejärel töö ID järgi.

### <a name="set-up-a-mobile-device-menu"></a>Mobiilse seadme menüü seadistamine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
2. Lisage menüü-üksus, mille just lõite, soovitud menüüsse.

## <a name="example"></a>Näide

### <a name="create-picking-work"></a>Komplekteerimistöö loomine

Enne süsteemi suunatud kogumi komplekteerimise seadistamist peate looma mõne sobiliku väljamineva töö. Varasemalt loodud kogumiprofiil määrab kaks kogumi positsiooni. Seetõttu peate looma vähemalt kaks töö ID-d.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
2. Müügitellimuse loomiseks valige **Uus**.
3. Valige väljalt **Kliendi konto** mis tahes klient.
4. Kiirkaardi **Üldine** väljal **Ladu** valige ladu **62**.
5. Valige nupp **OK**.
6. Kiirkaardil **Müügitellimuse read** valige suvand **Lisa rida**.
7. Valige väljal **Kaubakood** väärtus **A0001**.
8. Sisestage väljale **Kogus** väärtus **1**.
9. Teise rea lisamiseks valige**Lisa rida**.
10. Valige väljal **Kaubakood** väärtus **A0002**.
11. Sisestage väljale **Kogus** väärtus **3**.
12. Korrake etappe 2–6.
13. Valige väljal **Kaubakood** väärtus **A0001**.
14. Sisestage väljale **Kogus** väärtus **4**.
15. Teise rea lisamiseks valige**Lisa rida**.
16. Valige väljal **Kaubakood** väärtus **A0002**.
17. Sisestage väljale **Kogus** väärtus **2**.

Reserveerige varud ja vabastage need lattu. Luuakse kaks erinevat töö ID-d. Igal töö ID-l on kaks komplekteerimisrida.

### <a name="run-the-mobile-device-flow"></a>Mobiilse seadme voo käitamine

1. Valige mobiilses seadmes menüü, mis sisaldab uut mobiilse seadme menüü-üksust.
2. Valige menüü-üksus **SD kogum** ja käivitage komplekteerimine. Luuakse kogum ja kaks varem loodud töö ID-d on sellele lisatud. Kui lõite rohkem kui kaks töö ID-d, lisatakse kogumile ainult kaks esimest. Pange tähele, et töö ID-d lisatakse kogumile kasvavas järjestuses, nagu määrasite päringu häälestuses.

    > [!NOTE]
    > Uus kogum luuakse automaatselt ainult siis, kui eelnevalt on loodud piisavalt täiendavaid töö ID-sid. Vastasel juhul kuvatakse järgmine teade: „Kogumi jaoks ei leidu piisavalt tööd”.

    Pärast menüü valimist ilmub esimene komplekteerimiskuva. Süsteem koondab kõik ühtivad komplekteerimisread kahest töö ID-st ja suunab teid külastama komplekteerimise asukohta üks kord, nii et saate täita mõlemad tellimused ühe komplekteerimisega. See protsess teostatakse samamoodi nagu kasutaja suunatud kogumi komplekteerimise protsess.

3. Kinnitage esimene komplekteerimine. Peate seejärel sisestama positsiooni nime kinnitamaks, et kaubad pandi õigesse kohta.
4. Korrake seda protsessi seni, kuni kõik esemed on komplekteeritud ja õigesse kohta pandud.
5. Mobiilse seadme viimane etapp on panna kogum lõplikku asukohta. Kui see panemise toiming kinnitatakse, kogum suletakse ja tükeldatakse vastavalt väärtusele, mille kogumiprofiilis väljale **Tükelda kogum asukohas** määrasite. Töö ID-d on samuti suletud.
6. Mobiilsel seadmel kuvatakse teade „Kogum lõpetatud”.
