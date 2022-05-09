---
title: Looge B2B-saitide jaoks ärikataloogid
description: See teema kirjeldab, kuidas luua äriettevõtetele Microsoft Dynamics 365 Commerce (B2B) saitide ärikatalooge.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 868f6bbeefeb1698bb136d52c09cebf293c95731
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/29/2022
ms.locfileid: "8657186"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Looge B2B-saitide jaoks ärikataloogid

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema kirjeldab, kuidas luua äriettevõtetele Microsoft Dynamics 365 Commerce (B2B) saitide jaoks äritootekatalooge. Vastuseid korduma kippuvatele küsimustele B2B-saitide ärikataloogide kohta [vt B2B PVQ ärikataloogidest](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> See teema kehtib versiooni Dynamics 365 Commerce 10.0.26 ja hilisemate väljalasete kohta.

Ärikataloogide abil saate tuvastada tooted, mida soovite oma B2B võrgupoodides pakkuda. Kui loote kataloogi, tuvastate e-poed, kuhu tooteid pakutakse, lisate tooteid, mida soovite kaasata ja täiustate tooteostmist, lisades toote üksikasjad. Iga B2B e-poe jaoks saate luua mitu kataloogi.

Commerce'i tootekataloogide abil saate määratleda järgmise teabe:

- **Kataloogipõhine navigeerimishierarhia** – organisatsioonid saavad luua oma kataloogi jaoks eristatava kategooriastruktuuri.
- **Kataloogipõhise atribuudi metaandmed** – atribuudid sisaldavad toote üksikasju. Atribuutide määramisega navigeerimishierarhia kategooriale saate nendele atribuutidele määrata väärtused kategooriale määratud toodete tasemel. Siis saavad organisatsioonid need ülesanded lõpule viia:

    - Määratlege kataloogispetsiifilised atribuudiväärtused.
    - Kontrollige atribuutide nähtavust kataloogi tasemel.
    - Valige konkreetsele kataloogile omased täpsustused.

- **Kanalid** – organisatsioonid saavad kataloogiga seostada rohkem kui ühe B2B võrgukanali. Kataloogide lõpptoe on praegu saadaval ainult B2B e-poodide jaoks.
- **Kliendi hierarhiad** – antud B2B-kanali puhul saavad organisatsioonid teha konkreetse kataloogi kättesaadavaks valitud B2B partneritele, seostades kliendi hierarhiad selle kataloogiga.
- **Hinnagrupid** – saate konfigureerida hinnad ja kampaaniahinnad, mis on omased antud kataloogile. See võimalus on põhipõhjus kataloogi määratlemiseks B2B-kanali jaoks. Kataloogide hinnagrupid võimaldavad organisatsioonidel teha tooted kättesaadavaks oma kavandatud B2B-organisatsioonidele ja rakendada oma eelistatud hinnakujundust ja allahindlusi. B2B-kliendid, kes tellivad konfigureeritud kataloogist saavad kasu spetsiaalsetest hindadest ja kampaaniatest pärast seda, kui nad on sisse loginud Commerce B2B saidile. Kataloogispetsiifiliste hindade konfigureerimiseks valige **vahekaardil** **Kataloogid suvand Hinnagrupid**, et linkida kataloogiga üks või mitu hinnagruppi. Kõik kaubanduslepped, hinnakorrektsiooni töölehed ja täpsemad allahindlused, mis on lingitud sama hinnagrupiga, rakendatakse siis, kui kliendid tellivad sellest kataloogist. (Täpsemad allahindlused hõlmavad läve, kogust ning segamise ja sobitamise allahindlusi.) Lisateavet hinnagruppide kohta vt [hinnagruppidest](price-management.md#price-groups).

> [!NOTE]
> See funktsioon on saadaval alates versiooni Dynamics 365 Commerce 10.0.26 väljalaskest. Kataloogispetsiifiliste konfiguratsioonide, nt navigeerimishierarhia ja kliendihierarhia konfigureerimiseks avage Commerce Headquartersis funktsioonihalduse tööruum (**Süsteemihalduse** **tööruumide funktsioonihaldus \>), \> lubage mitme kataloogi kasutamine jaemüügikanalite funktsioonis** **ja käivitage seejärel 1110 CDX-töö**.**·**

## <a name="catalog-process-flow"></a>Kataloogi protsessivoog

Kataloogi loomise ja töötlemise protsessil on neli üldist sammu. Iga etappi kirjeldatakse järgmises jaotises üksikasjalikult.

1. **[Konfiguratsioon](#configure-the-catalog)**

    - Navigeerimishierarhia seostamine
    - Määrake aja kehtivad ja aegumiskuupäevad, kui need on rakendatavad.
    - Lisage ja kategoriseerige tooted.
    - Seostage hinnagrupid.
    - Seostage kliendi hierarhia, mis on omane teie B2B-organisatsioonidele. 
    - Saate vaikedimensiooni atribuudigrupi siduda täpsustajatele, nt suurus, stiil ja värv.
    - Atribuudi metaandmete kogum.

1. **[Kinnitamine](#validate-the-catalog)** – selles etapis käivitage kinnitusreeglid, mis jõustavad kindla käitumise. Järgmisena on toodud mõned näited.

    - Veenduge, et kategoriseerimata tooteid ei ole.
    - Veenduge, et kataloogiga on seotud kõik iga kanali jaoks valikuga kaubad.

1. **[Heakskiit](#approve-the-catalog)**
1. **[Avaldamine](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Kataloogi häälestamine

Kasutage kataloogi häälestamiseks selle jaotise teavet.

### <a name="configure-the-catalog"></a>Kataloogi konfigureerimine

Minge Rakenduse Commerce headquarters kataloogi konfigureerimiseks **\>\> jaemüügi- ja ärikataloogidele ja sortimentide** hulka kõik kataloogid.

Uue kataloogi loomisel peate selle esmalt seostama ühe või mitme kanaliga. Kataloogi loomisel saab kasutada ainult valitud kanali [sortimentiga](/dynamics365/unified-operations/retail/assortments) lingitud kaupu. Kataloogi seostamiseks ühe või mitme kanaliga valige **kataloogi** **häälestuse lehe ärikanalite** kiirkaardil **suvand** Lisa.

#### <a name="associate-the-navigation-hierarchy"></a>Navigeerimishierarhia seostamine

Toodete lisamiseks kataloogi peate valima navigeerimishierarhia. Navigeerimishierarhia toetab kataloogi kategooriastruktuuri. Peate valima kataloogi **häälestuslehe** **ärikanalite kiirkaardil valitud kanalitega seotud navigeerimishierarhia**. Vaikimisi navigeerimishierarhia seostamiseks kõigi oma kanalitega minge jaemüügi ja ärikanali **häälestuse \> kanali kategooriatesse \> ja toote atribuutidesse**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Määrake kehtivusaja ja aegumiskuupäevad.

Kataloogi ajaliste ja aegumiskuupäevade määramiseks valige kataloogihierarhia ülemine sõlm, et naasta kataloogi põhipäise vaatesse. Seejärel konfigureerige kiirkaardil **Üldine** vastavalt vajadusele kehtivuse ja aegumiskuupäevad.

#### <a name="add-and-categorize-products"></a>Toodete lisamine ja kategoriseerimine

Toodete konfigureerimiseks kataloogi lisamiseks minge Commerce Headquartersis jaemüügi **- \> ja ärikataloogidele ja sortimentide \> kõik kataloogid**. Seejärel valige vahekaardil **Kataloogid** suvand **Lisa tooted**.

Teise võimalusena valige sõlm navigeerimishierarhias. Seejärel saate tooteid lisada otse kataloogi kategooriasse.

#### <a name="associate-price-groups"></a>Hinnagruppide seostamine

Kataloogispetsiifiliste hindade konfigureerimiseks peate kataloogiga seostama ühe või mitu hinnagruppi. Hinnagruppide seostamiseks kataloogiga minge Rakenduse Commerce headquarters valikusse **Jaemüügi- ja ärikataloogid \> ning sortimendid \> Kõik kataloogid**. Seejärel valige vahekaardi **Kataloogid** jaotises Hinnakujundus **suvand** Hinnagrupid **·**. Kõik kaubanduslepped, hinna korrigeerimise töölehed ja täpsemad allahindlused (lävi, kogus ning segamise ja sobitamise allahindlused), mis on lingitud sama hinnagrupiga, rakendatakse siis, kui kliendid tellivad kataloogist.

Lisateavet hinnagruppide kohta vt [hinnagruppidest](price-management.md#price-groups).

> [!NOTE]
> Uut hinnagruppi ei saa lehest **Kõik kataloogid luua**. Selle asemel peate selle looma leheküljelt **Kõik hinnagrupid**. Seejärel peate seostama selle kataloogiga lehel **Kõik kataloogid**.

#### <a name="associate-a-customer-hierarchy"></a>Kliendi hierarhia seostamine

Kliendi hierarhiate seostamiseks minge Rakenduse Commerce headquarters kaudu jaemüügi **- ja ärikataloogidele \> ja sortimentide \> hulka Kõik kataloogid**. Seejärel valige kliendi **hierarhias** kataloogide **vahekaardil** Kataloogid suvand Määra **hierarhiad,** et linkida kataloogiga üks või mitu kliendihierarhiat.

> [!NOTE]
> Uut kliendihierarhiat ei saa leheküljelt Kõik **kataloogid luua**. Selle asemel peate selle looma leheküljel Kliendi **hierarhiad**. Seejärel peate seostama selle kataloogiga lehel **Kõik kataloogid**.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Dimensiooniatribuudi vaikegrupi seostamine täpsustajatele, nt suurus, stiil ja värv

Dimensiooniatribuudi vaikegrupi seostamiseks täpsustajatele (nt suurus, stiil ja värv) minge Commerce Headquartersis **\>\> jaemüügi ja ärikataloogide ja sortimentide kõigi kataloogide hulka.** Seejärel valige vahekaardi Kataloogid **jaotises** Atribuudid suvand **Atribuudigrupid** **.**

#### <a name="set-attribute-metadata"></a>Atribuudi metaandmete häälestamine

Atribuudi metaandmete konfigureerimiseks minge Commerce Headquartersi jaemüügi **ja ärikataloogide \> ja sortimentide \> kõigi kataloogide hulka**. Seejärel valige vahekaardi **Kataloogid** jaotises Atribuudid **suvand Sea** atribuudi **metaandmed**. Et valida atribuudid, **mis peaksid olema vaadatavad ja määratletavad, valige kategooria seostatud kataloogipõhises navigeerimishierarhias** ja seejärel valige jaotises Kataloogitoote atribuudid atribuut. Seejärel valige **suvand Näita atribuuti kanalil**. Vaikimisi on otsitavad ka kõik vaadatavad atribuudid. Valige suvand Saab täpsustada, **et atribuudid valikuliselt täpsustada**.

### <a name="validate-the-catalog"></a>Kataloogi valideerimine

Enne kui uus kataloog on kasutamiseks saadaval, tuleb see kinnitada ja avaldada.

Kataloogi kontrollimiseks tehke järgmist.

1. Kinnitamise käivitamiseks valige vahekaardi **Kataloogid** jaotises **Kontrolli** **kataloogi**.**·** See samm on nõutav. See kinnitab, et nõutav seadistus on täpne.
1. Valige **valideerimise** üksikasjade vaatamiseks tulemused. Vigade ilmnemisel peate andmed parandama ja kinnitamise uuesti käivitama, kuni see läbib.

### <a name="approve-the-catalog"></a>Kataloogi kinnitamine

Pärast kataloogi kinnitamist tuleb see kinnitada.

Kataloogi kinnitamise töövoo käivitamiseks järgige neid samme.

1. Valige lehe Kõik kataloogid **toimingupaanil** suvand Töövoo **esitamine \>**.
1. Minge rakenduse **Retail ja Commerce \> Headquarters häälestama \> Commerce'i töövood**, et konfigureerida sammud ja töövoo volitatud kasutajad. Töövoog määratleb sammud, mis on vajalikud kataloogi toomiseks kinnitatud **olekusse**.

### <a name="publish-the-catalog"></a>Kataloogi avaldamine

Kui kataloog on kinnitatud **olekus**, saate selle avaldada, valides **menüüs** **Kataloogid käsu** Avalda. Kui kataloog on avaldatud **olekus**, saab seda kasutada kõnekeskuse tellimuse sisestamiseks ja kataloogi saatmiseks. Kataloogi saate avaldada käsitsi või pakktöötluse abil. Kataloogi jaoks määratletud kehtivuse kuupäev määratleb, millal tooted on võrgupoes saadaval. Teie määratud aegumiskuupäev määrab, millal tooted võrgupoest eemaldatakse.

> [!NOTE]
> Saate avaldada kataloogi, mis sisaldab hoiatustega tooteid. Need tooted ei ilmu siiski võrgupoes.

## <a name="additional-resources"></a>Lisaressursid

[Ärikataloogide laiendatav mõju B2B-kohandustele](catalogs-b2b-sites-dev.md)

[B2B KKK ärikataloogid](catalogs-b2b-sites-FAQ.md)
