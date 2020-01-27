---
title: Riistvara suuruse muutmise nõuded kohapealsetes keskkondades
description: Riistvara suuruse muutmise nõuded kohapealsetes keskkondades
author: sericks007
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 8fa644f35a086af99cde74fd6a2062f9b59a6ff7
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870260"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>Riistvara suuruse muutmise nõuded kohapealsetes keskkondades

[!include [banner](../includes/banner.md)]

Enne kui alustate kohapealses keskkonnas riistvara ja taristu suuruse muutmise protsessi, tutvuge [pilvjuurutuste süsteeminõuete](system-requirements.md) ning [seadistus- ja juurutusjuhistega](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md), et aluseks olev taristu endale hästi selgeks teha.

> [!NOTE]
> Optimaalse jõudluse saavutamiseks pöörake tähelepanu süsteemi seadistamise parimatele tavadele.

Kui olete dokumentatsiooni läbi vaadanud, võite alustada oma tehingute ja samaaegsete kasutajate mahu hindamise ning keskkonna suuruse muutmise protsessi tuuma keskmise läbilaskevõime põhjal.

## <a name="factors-that-affect-sizing"></a>Suuruse muutmist mõjutavad tegurid

Suuruse muutmist mõjutavad kõik järgmisel joonisel näidatud tegurid. Mida põhjalikum on kogutud teave, seda täpsemalt saate suuruse muutmise kindlaks määrata. Riistvaraline suuruse muutmine ilma toetavate andmeteta on tõenäoliselt ebatäpne. Vajalike andmete absoluutne miinimumnõue on maksimaalne kanderea koormus tunni kohta.

[![Riistvara suuruse muutmine kohapealsetes keskkondades](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Vaadates vasakult paremale, on esimene ja kõige olulisem suuruse muutmise täpseks prognoosimiseks vajalik tegur kannete profiil ehk kannete iseloomustus. Tähtis on leida alati maksimaalne kannete maht tunnis. Kui tipp-perioode on mitu, tuleb need perioodid täpselt määratleda.

Kui mõistate koormust, mis teie taristut mõjutab, peate põhjalikumalt aru saama ka järgmistest teguritest.

- **Kanded** – tavaliselt on kandemahtudel päeva/nädala jooksul teatud tipud. See sõltub enamasti kandetüübist. Aja- ja kulukannetel on harilikult maksimumid kord nädalas, samas müügitellimuse kanded tulevad sageli päeva jooksul integratsiooni või edastuste kaudu hulgi.
- **Samaaegsete kasutajate arv** – samaaegsete kasutajate arv on teine olulisim suuruse muutmise tegur. Samaaegsete kasutajate arvu põhjal ei saa suuruse muutmist usaldusväärselt prognoosida, seega kui need on ainsad saadaolevad andmed, võtke hindamise aluseks ligikaudne arv ja seejärel tulge selle juurde tagasi, kui teil on rohkem andmeid. Samaaegsete kasutajate täpne määratlus tähendab järgmist.

    - Nimega kasutajad ei ole samaaegsed kasutajad.
    - Samaaegsetel kasutajatel on alati alamkogum nimega kasutajaid. 
    - Maksimaalne töökoormus määratleb suuruse muutmiseks vajaliku maksimaalse samaaegsuse.

    Samaaegsete kasutajate kriteeriumid tähendavad, et kasutaja vastab kõigile järgmistele kriteeriumidele.

    - On sisse loginud.
    - töötab loendamise ajal kannete/päringutega.
    - Ei ole jõudeolekus.

- **Andmete koosseis** – see tähendab enamasti seda, kuidas teie süsteem seadistatakse ja konfigureeritakse. Näiteks kui palju on teil juriidilisi isikuid, kui palju üksusi, kui palju koosluse tasemeid ja kui keeruline on teie turbeseadistus. Kõik need tegurid võivad jõudlust veidi mõjutada, seega saab need taristu loomisel nutikate valikute abil kõrvale nihutada.
- **Laiendused** – kohandused võivad olla lihtsad või keerulised. Kohanduste arvul ning keerukusel ja kasutusel on taristu vajalikule suurusele muutuv mõju. Keeruliste kohanduste puhul on soovitatav teha jõudluse hindamisi tagamaks, et neid ei testitaks üksnes tõhususe suhtes, vaid ka selleks, et mõista taristu vajadusi. See on isegi veel kriitilisem, kui laiendused pole jõudluse ja skaleeritavuse jaoks parimate tavade järgi kodeeritud.
- **Aruandlus ja analüüs** – need tegurid sisaldavad tavaliselt töötavaid väga sagedasi päringuid erinevatest andmebaasidest süsteemides. Sageduse mõistmine ja vähendamine kuluaruannete käitamisel aitab teil mõista nende mõju.
- **Kolmanda osapoole lahendused** – neil lahendustel, nagu ISV-d, on sama mõju ja soovitused kui laienduste puhul.

## <a name="sizing-your-environment"></a>Keskkonna suuruse muutmine

Suuruse muutmise nõuete mõistmiseks peate teadma kannete maksimaalset mahtu, mida peate töötlema. Enamik abistavaid süsteeme, nagu halduse aruandja või SSRS, on vähem missioonikriitilised. Seetõttu keskendub see dokument peamiselt AOS-ile ja SQL Serverile.

> [!NOTE]
> Üldiselt selgitatakse välja arvutusjärgud ja seda tuleks teha meetodil N + 1, mis tähendab, et kui hindate kolme AOS-i, lisage neljas AOS. Andmebaasijärk tuleks seadistada hästi kättesaadava seadistuse meetodil „alati sees”.

## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Suuruse muutmine

- 3000 kuni 15 000 kanderida tunnis iga andmebaasiserveri tuuma kohta.
- AOS-i ja SQL-i tuumade suhe primaarse SQL Serveri puhul on tüüpiliselt 3 : 1. Lisatuumad on vajalikud olenevalt valitud suure kättesaadavuse konfiguratsioonist.

    - Andmebaasile raskete toimingute töötlemine võib selle vähendada suhtele 2 : 1.

- Erinevust mõjutavad järgmised tegurid.

    - Kasutatavad parameetrisätted.
    - Laienduste tasemed.
    - Lisafunktsioonide, nagu andmebaasilogid ja hoiatused, kasutamine. Äärmuslik andmebaasilogimine vähendab läbilaskevõimet tunnis tuuma kohta veelgi vähem kui 3000 reale.
    - Andmete koosseisu keerukus – lihtsa kontoplaani mõju läbilaskevõimele on teistsugune kui näiteks põhjaliku ja detailse kontoplaani puhul.
    - Kannete iseloomustus.
    - 2 GB kuni 16 GB mälu iga tuuma kohta.
    - Abistavad andmebaasid andmebaasiserveris, nagu halduse aruandja ja SSRS-i andmebaasid.
    - Ajutine andmebaas = 15% andmebaasimahust, võrdse failide ja füüsiliste protsessorite arvuga.
    - SAN-i suurus ja läbilaskevõime põhinevad samaaegsete kannete kogumahul/-kasutusel.

### <a name="high-availability"></a>Suur kättesaadavus

Soovitame kogumi või peegelduse seadistamisel kasutada alati SQL Serverit. SQL-i teisel sõlmel peab olema sama arv tuumi mis primaarsel sõlmel.

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory Federation Services (AD FS)

AD FS-i suuruse muutmiseks vaadake [AD FS-i serveri jõudluse dokumentatsiooni](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Teie juurutuses eksemplaride arvu kavandamiseks on saadaval [suuruse muutmise tabel](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx).

## <a name="aos-online-and-batch"></a>AOS (veebipõhine ja pakktöötlus)

### <a name="sizing"></a>Suuruse muutmine

- Suuruse muutmine kannete mahu/kasutuse järgi

    - 2000–6000 rida tuuma kohta
    - 16 GB eksemplari kohta
    - Standardne kast – 4–24 tuuma
    - 10–15 ettevõtte kasutajat tuuma kohta
    - 15–25 tegevuste kasutajat tuuma kohta
    - 25–50 töörühma liiget tuuma kohta

- Partii

    - 1–4 pakktöötluslõime tuuma kohta
    - Pakktöötlusakna iseloomustusel põhinev suurus

- Pange tähele, et AOS-il. andmehaldusel ja pakktöötlusel on Service Fabricus sama roll. Peate valima suuruse nende kolme töökoormuse kohta kokku ega tohi neid eraldada nagu rakenduses Microsoft Dynamics AX 2012.
- Siin kehtivad samad varieeruvustegurid mis SQL Serveri puhul.

### <a name="high-availability"></a>Suur kättesaadavus

- Veenduge, et teil oleks saadaval vähemalt 1–2 AOS-i rohkem kui prognoosite.
- Veenduge, et teil oleks saadaval vähemalt 3–4 virtuaalset hosti.

## <a name="management-reporter"></a>Halduse aruandja

Enamasti peaks soovitatud miinimumnõuded, kasutades kaht sõlme, hästi toimima, kui neid ulatuslikult ei kasutata. Ainult juhtudel, kui kasutuskoormus on suur, vajate rohkem kui kaht sõlme. Skaleerige vajadust mööda.

## <a name="sql-server-reporting-services"></a>SQL Serveri aruandlusteenused

Üldiselt kättesaadava versiooni puhul saab juurutada ainult ühe SSRS-i sõlme. Jälgige oma SSRS-i sõlme testimise ajal ja suurendage SSRS-i jaoks saadaolevate tuumade arvu vajadust mööda. Veenduge, et teil oleks virtuaalhostis saadaval eelkonfigureeritud teisene sõlm, mis ei ole SSRS-i virtuaalarvuti. See on oluline, kui SSRS-i või virtuaalhosti majutava virtuaalarvutiga tekib mõni probleem. Sellisel juhul tuleb see arvutada.

## <a name="environment-orchestrator"></a>Keskkonna korraldaja

Korraldusteenus on teenus, mis haldab teie juurutust ja seotud sidet LCS-iga. See teenus juurutatakse primaarse Service Fabricu teenusena ja nõuab vähemalt kolme virtuaalarvutit. Teenus asub samas kohas mis Service Fabricu korraldusteenused. Selle suurus tuleks määrata kogumi tippkoormuse järgi. Lisateabe saamiseks vaadake teemat [Teenuse Service Fabric eraldiseisva kogumi juurutamise plaanimine ja ettevalmistamine](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="virtualization-and-oversubscription"></a>Virtualiseerimine ja ületellimine

Missioonikriitilisi teenuseid, nagu AOS, tuleks majutada virtuaalhostides, millel on spetsiaalsed ressursid – tuumad, mälu ja ketas.
