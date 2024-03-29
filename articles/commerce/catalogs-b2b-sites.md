---
title: B2B-saitide Commerce'i kataloogide loomine
description: See artikkel kirjeldab, kuidas luua äriettevõtetele Microsoft Dynamics 365 Commerce (B2B) saitide ärikatalooge.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136822"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>B2B-saitide Commerce'i kataloogide loomine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas luua äriettevõtetele Microsoft Dynamics 365 Commerce (B2B) saitide jaoks äritootekatalooge. Vastuseid korduma kippuvatele küsimustele B2B-saitide ärikataloogide kohta [vt B2B PVQ ärikataloogidest](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> See artikkel kehtib versioonile Dynamics 365 Commerce 10.0.27 ja hilisematele väljalasetele.

Ärikataloogide abil saate tuvastada tooted, mida soovite oma B2B võrgupoodides pakkuda. Kui loote kataloogi, tuvastate e-poed, kuhu tooteid pakutakse, lisate tooteid, mida soovite kaasata ja täiustate tooteostmist, lisades toote üksikasjad. Iga B2B e-poe jaoks saate luua mitu kataloogi, nagu näha järgmises illustratsioonis.

![Äritootekataloogide eelvaade.](./media/Commerce_Catalogs.png)

Commerce'i tootekataloogide abil saate määratleda järgmise teabe:

- **Kataloogi tüüp** : konfigureerige väärtus B2B-ina **·**. Saate määrata B2B-kataloogipõhised atribuudid, nt navigeerimishierarhia, kliendi hierarhia ja kataloogi atribuudi metaandmed. 
- **Kataloogipõhine navigeerimishierarhia** – organisatsioonid saavad luua oma kataloogi jaoks eristatava kategooriastruktuuri.
- **Kataloogipõhise atribuudi metaandmed** – atribuudid sisaldavad toote üksikasju. Atribuutide määramisega navigeerimishierarhia kategooriale saate nendele atribuutidele määrata väärtused kategooriale määratud toodete tasemel. Siis saavad organisatsioonid need ülesanded lõpule viia:

    - Määratlege kataloogispetsiifilised atribuudiväärtused.
    - Kontrollige atribuutide nähtavust kataloogi tasemel.
    - Valige konkreetsele kataloogile omased täpsustused.

- **Kanalid** – organisatsioonid saavad kataloogiga seostada rohkem kui ühe B2B võrgukanali. Kataloogide lõpptoe on praegu saadaval ainult B2B e-poodide jaoks.
- **Kliendi hierarhiad** – antud B2B-kanali puhul saavad organisatsioonid teha konkreetse kataloogi kättesaadavaks valitud B2B partneritele, seostades kliendi hierarhiad selle kataloogiga.
- **Hinnagrupid** – saate konfigureerida hinnad ja kampaaniahinnad, mis on omased antud kataloogile. See võimalus on põhipõhjus kataloogi määratlemiseks B2B-kanali jaoks. Kataloogide hinnagrupid võimaldavad organisatsioonidel teha tooted kättesaadavaks oma kavandatud B2B-organisatsioonidele ja rakendada oma eelistatud hinnakujundust ja allahindlusi. B2B-kliendid, kes tellivad konfigureeritud kataloogist saavad kasu spetsiaalsetest hindadest ja kampaaniatest pärast seda, kui nad on sisse loginud Commerce B2B saidile. Kataloogispetsiifiliste hindade konfigureerimiseks valige **vahekaardil** **Kataloogid suvand Hinnagrupid**, et linkida kataloogiga üks või mitu hinnagruppi. Kõik kaubanduslepped, hinnakorrektsiooni töölehed ja täpsemad allahindlused, mis on lingitud sama hinnagrupiga, rakendatakse siis, kui kliendid tellivad sellest kataloogist. (Täpsemad allahindlused hõlmavad läve, kogust ning segamise ja sobitamise allahindlusi.) Lisateavet hinnagruppide kohta vt [hinnagruppidest](price-management.md#price-groups).

> [!NOTE]
> See funktsioon on saadaval alates versiooni Dynamics 365 Commerce 10.0.27 väljalaskest. Kataloogispetsiifiliste konfiguratsioonide konfigureerimiseks, nagu näiteks navigeerimishierarhia ja kliendihierarhia rakenduse Commerce headquarters puhul, **minge** funktsioonihalduse tööruumi (**Süsteemihalduse \>\> tööruumide funktsioonihaldus**), **lubage mitme kataloogi kasutamine jaemüügikanalite funktsioonis** **ja käivitage seejärel 1110 CDX-töö**. Kui lubate selle funktsiooni, märgitakse kõik olemasolevad kataloogid, **mida kasutatakse müügikoha kauplustele või kõnekeskusele, kataloogi tüübiks = B2C** **kataloogide** lehel. Kassakauplustele ja kõnekeskusele **kehtivad ainult olemasolevad ja uued kataloogid, mis on märgitud kui kataloogi tüüp = B2C**. 

## <a name="b2b-catalog-process-flow"></a>B2B-kataloogi protsessivoog

Kataloogi loomise ja töötlemise protsessil on neli üldist sammu. Iga etappi kirjeldatakse järgmises jaotises üksikasjalikult.

> [!NOTE]
> Enne, kui jätkate, veenduge, et kataloog on märgitud **kui kataloogi tüüp = B2B**.

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

Uue kataloogi loomisel peate selle esmalt seostama ühe või mitme kanaliga. Kataloogi loomisel saab kasutada ainult valitud kanali [sortimentiga](/dynamics365/unified-operations/retail/assortments) lingitud kaupu. Kataloogi seostamiseks ühe või mitme kanaliga valige **kataloogi** **häälestuse lehe ärikanalite** kiirkaardil **suvand** Lisa. Veenduge, et kataloogi tüüp oleks **B2B**.

#### <a name="associate-the-navigation-hierarchy"></a>Navigeerimishierarhia seostamine

Toodete lisamiseks kataloogi peate valima navigeerimishierarhia. Navigeerimishierarhia toetab kataloogi kategooriastruktuuri. Peate valima kataloogi **häälestuslehe** **ärikanalite kiirkaardil valitud kanalitega seotud navigeerimishierarhia**. Vaikimisi navigeerimishierarhia seostamiseks kõigi oma kanalitega minge jaemüügi ja ärikanali **häälestuse \> kanali kategooriatesse \> ja toote atribuutidesse**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Määrake kehtivusaja ja aegumiskuupäevad.

Kataloogi ajaliste ja aegumiskuupäevade määramiseks valige kataloogihierarhia ülemine sõlm, et naasta kataloogi põhipäise vaatesse. Seejärel konfigureerige kiirkaardil **Üldine** vastavalt vajadusele kehtivuse ja aegumiskuupäevad.

#### <a name="add-and-categorize-products"></a>Toodete lisamine ja kategoriseerimine

Toodete konfigureerimiseks kataloogi lisamiseks minge Commerce Headquartersis jaemüügi **- \> ja ärikataloogidele ja sortimentide \> kõik kataloogid**. Seejärel valige vahekaardil **Kataloogid** suvand **Lisa tooted**.

Teise võimalusena valige sõlm navigeerimishierarhias. Seejärel saate tooteid lisada otse kataloogi kategooriasse.

#### <a name="associate-price-groups"></a>Hinnagruppide seostamine

Toodete konfigureerimiseks kataloogi lisamiseks minge Commerce Headquartersis jaemüügi **- \> ja ärikataloogidele ja sortimentide \> kõik kataloogid**. Seejärel valige vahekaardil **Kataloogid** suvand **Lisa tooted**. 

Tooted, mis lisati **kataloogi** navigeerimishierarhia juursõlmes, valides tegevuspaanil valiku Lisa tooteid, pärivad oma kategooriad, kui allika navigeerimishierarhia on seotud ka kataloogiga. Allika navigeerimishierarhias tehtud muudatused kajastuvad kohe kataloogides. Kanalite uuendamiseks peate kataloogid uuesti avaldama.

Teise võimalusena saate valida sõlm navigeerimishierarhias ja lisada tooteid otse kataloogi valitud kategooriasse. 

Toodete lisamisel on saadaval suvand **Kaasa automaatselt kõik variandid, kui valitud on ainult** tooteetelm. Kõigi variantide kaasamise vältimiseks valige tooteemudelile vähemalt üks variant. 

> [!NOTE]
> Kui valite kõigi variantide automaatse kaasamise suurte tootee põhiandmete valikusse, võib teil esineda pikemaid töötlemiskordi. Suurte valikute puhul soovitame **toimingu** pakett-režiimis käivitamiseks valida kataloogide lehekülje tegevuspaanil kõik variandid. Kui kaasati kataloogi ainult tootee master ja variante ei kaasatud, ei pruugi variandi valija toote üksikasjade lehele navigeerides saadaval olla. 

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

> [!NOTE]
> Kui **kataloogi tüüp = B2B**, nurjub kinnitamine, kui lisate kataloogile müügikoha kauplused või kõnekeskuse. B2B-kataloogidega peavad olema seotud ainult B2B võrgukanalid. Kinnitamine nurjub ka juhul, kui B2B-kataloogiga pole seotud ühtegi kliendihierarhiat. 

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

[B2B-kohanduste Commerce'i kataloogide laiendatavus](catalogs-b2b-sites-dev.md)

[B2B-saitide Commerce'i kataloogide KKK](catalogs-b2b-sites-FAQ.md)

[Kataloogi valija moodul](catalog-picker.md)
