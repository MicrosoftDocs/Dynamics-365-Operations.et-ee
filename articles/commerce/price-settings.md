---
title: Hinnakujunduse sätted
description: See artikkel kirjeldab peakontoris hinnakujunduse ja allahindluse halduse erinevaid Microsoft Dynamics 365 Commerce sätteid.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 4bc8cb16e7960d26adbb9590b4ad83cf46b02838
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410471"
---
# <a name="pricing-settings"></a>Hinnakujunduse sätted

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

See artikkel kirjeldab peakontoris hinnakujunduse ja allahindluse halduse erinevaid Microsoft Dynamics 365 Commerce sätteid. Need sätted võimaldavad organisatsioonidel määrata hinnakujunduse käitumise ärilahenduses, mis vastab konkreetsetele ärivajadustele.

## <a name="company-level-pricing-settings"></a>Ettevõttetasemel hinnakujunduse sätted

Enamik hinnakujunduse sätteid on ettevõtte tasemel ja neid saab **leida Commerce’i parameetritest Hinnad \> ja allahindlused** rakenduse Commerce headquarters kaudu.

### <a name="best-price-and-compound-concurrency-control-model"></a>Parima hinna ja liitmise kokkulangevuse juhtelemendi mudel

Parim **hinna ja liit konkurentsuskontrolli** mudeli säte määrab, kuidas hinnakujundusmootor töötleb mitmeid allahindlusi parimas hinna- **·** **või** liitkordusrežiimis. 

Kui parameetri väärtuseks on **seatud Parim hind ja liitmine prioriteedi piires,** ei liita kunagi prioriteetide alusel kõiki liitallahindlusi, **mille** hinnakujunduse prioriteet on sama. Liittulemus võistleb **siis** kõigi parimate hinnaallahindlustega, mis on sama hinnakujunduse prioriteediga, rakendatakse parimat hinda ja kõiki allahindlusi, mille hinnakujunduse prioriteet on madalam.

Kui parameetri väärtuseks on määratud Ainult **parim hind ainult prioriteedi piires,** **liittakse** kõik liitallahindlused alati parimate **hinnaallahindlustega.** Hinnakujunduse prioriteedi piires võidetakse vaid üks allahindlus. Kui see üksik allahindlus on parim **hind** **või liitallahindlus**, **·** **siis** liittakse see kõigi täiendavate parima hinna või liitallahindlustega, mille hinnakujunduse prioriteet on madalam.

### <a name="discount-compound-behavior"></a>Allahindluse liitmiskäitumine

Allahindluse **liitkäitumise** säte määrab, kuidas hinnakujundusmootor arvutab mitu liitallahindlust.

Kui parameetri väärtuseks on **seatud** Liit, rakendatakse ühte allahindlust teise peale amulatiivsel viisil. Kui see on seatud väärtusele **Liitmine** alghinnaga, koheldakse kõiki allahindlusi üksteisest sõltumatult ja rakendatakse samale alghinnale.

Näiteks soovite liita 10-protsendiseid ja 20-protsendiseid allahindlusi tootele, mille alghind on $100. Kui seate allahindluse **liitkäitumise** parameetriks **Liit**, määratakse lõpphind $72 (100 90 &times; % 80% &times; $ 80%). Kui seate selle väärtuseks **Liitmine** alghinnaga, määratakse lõpphind $70 (100 $ – $10 – $20).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Luba välistav lävi ja muude perioodiliste allahindluste vaheline konkurents

Kui välistav **lävi** **ja muude perioodiliste allahindluste parameetri vaheline konkurents on seatud väärtusele Jah**, teeb hinnakujundusmootor välistavad läve allahindlused välistavate läveväliste allahindlustega. Hinnakujunduse prioriteet kehtib endiselt. Parim hinna ja **liitläve** allahindluste **käitumine** jääb selliseks nagu on. See tähendab, et nad ei konkureeri mitteläve allahindlustega.

### <a name="manual-line-discount-and-system-discount"></a>Käsitsi rea allahindlus ja süsteemiallahindlus

Käsitsi **rea allahindlus ja süsteemi allahindluse** säte määratleb, kuidas hinnakujundusmootor rakendab käsitsi rea allahindluse ja süsteemi allahindluse samale reale. Käsitsi rea allahindluse saab liita süsteemi allahindlusega või asendada süsteemi allahindluse. Kui käsitsi rea allahindlus ja süsteemi allahindlus on kombineeritud, siis arvestab arvutusloogika allahindluse **liitkäitumise** sätet. Kogu tellimusele rakenduv käsitsi salvestatud lõppallahindlus ei ole selle sättega seotud.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Hoia kaubad allahindluse hindade ümardamise jaoks samal müügireal

Mõnikord ei saa koguse allahindluse summat võrdselt jaotada kvalifitseeruva kogusega (nt kui allahindluse summa $10 kolme ostuühiku puhul maha). Sellisel juhul **määrab allahindluse hinna ümardamise** sätte säte Kaupade sama müügirea jaoks, kuidas hinnakujundusmootor rakendub ja allahindlussumma jaotab. Kui parameetri väärtuseks on seatud **Jah**, rakendatakse allahindluse summa tervikuna ja seda ei tükeldata. Kui see on seatud väärtusele **Ei**, jagatakse allahindluse summa kvalifitseeruva koguse vahel ja ümardatakse. Näiteks on kolme $10 allahindluse summa jagatud ühe ühiku allahindluseks $3.33 maha, $3.33 teise ühiku puhul maha ja $3.34 kolmanda ühiku allahindluseks.

### <a name="apply-discounts-to-key-in-price-products"></a>Rakenda allahindlused hinnatoodete võtmele

Allahindluste **rakendamist hinnatoodete sisestamiseks** määratleb, kas allahindlusi saab rakendada koos kassas sisestatud sisestatavate sisestatavate hindadega. Toote **konfiguratsiooni** hinnasätte võti määrab, kas ja kuidas toode toetab sissevõtme hinda.

### <a name="apply-discounts-to-price-overrides"></a>Rakenda hinnaalistustele allahindlused

Hinnale **allahindluste rakendamiste säte** määrab, kas allahindlusi saab rakendada koos hinna arittadega.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Allahindluste levitamine odavate allahindluste jaoks

Segamise ja sobitamise allahindluste puhul, mis kasutavad kalkulatsioonitüüpi "odavaimad" määrab allahindluste jaotamise säte odavate allahindluste puhul, **kas** hinnakujundusmootor jaotab allahindluse ridadele.

Kui parameetri väärtuseks on seatud **Ei**, rakendatakse allahindlust ainult kõige odavamatele ridadele. Näiteks "osta 2 hangi 1 tasuta" segamise ja sobitamise allahindluse puhul on kõige odavam kaup tasuta ja ülejäänud kaks kaupa jäävad täishinnale. Sel juhul saab klient, kes tagastab mõlemad täishinnaga kaubad, kolmanda kauba ikkagi tasuta. See stsenaarium võib põhjustada jaemüüjale kahjumit.

Kui parameetri väärtuseks on seatud **Jah**, jaotab hinnakujundusmootor allahindluse kõigile rakendatavatele ridadele. See säte võib aidata vähendada tagastuste kahjumit.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Mitmerealiste hindade ja allahindluste käsitsi arvutamine

Mitmerealiste **hindade ja allahindluste käsitsi arvutamise säte kontrollib, kas hinnakujundusmootor kasutab müügikoha rakenduses ja kõnekeskuse kanalis** hilinenud hinna ja allahindluse arvutamist. Kui parameetri väärtuseks **on** määratud Jah, ei arvuta hinnakujundusmootor iga kord, kui müügitellimus kassa rakenduses või kõnekeskuse kanalis luuakse või redigeeritakse, kohe multiallahindlusi (nt koguse allahindlused, läve allahindlused ning segamise ja sobitamise allahindlused).

> [!NOTE]
> Äriversioonis 10.0.30 **ja varasemas** juhib mitmerealiste hindade ja allahindluste käsitsi arvutamine ainult kõnekeskuse kanalit. Eraldi arvutage **mitu kauba allahindlust, mis on funktsiooniprofiilis** seadistatud, juhib hinnakalkulatsiooni käitumist kassa rakenduses. Rakenduse Commerce versiooni 10.0.31 kaks sätet konsolideeritakse ühte ettevõttetaseme sättesse.

### <a name="retention-period-in-days"></a>Säilitusperioodi kestus päevades

Kinnipidamise **perioodi päevade** säte näitab, kui palju päevi pärast aegumiskuupäeva (kui aegumiskuupäev on määratud) või keelatud kuupäeva (kui aegumiskuupäeva ei määrata), tuleb allahindlust süsteemselt kustutada. Kui parameetri väärtuseks on seatud **0** (null), siis automaatset kustutamist ei toimu.

> [!NOTE]
> Äriversioonis 10.0.30 ja varasemas on selle sätte nimi päevade arv, **pärast mida tuleb aegunud allahindlused kustutada**.

### <a name="coupon-bar-code"></a>Kupongi vöötkood

Kupongi **vöötkoodi** säte määrab, millist konkreetset vöötkoodi kasutatakse kupongi vöötkoodide loomiseks. Kasutajad saavad valida ühe eelmääratletud vöötkoodidest, mis on konfigureeritud vöötkoodi **seadistamise** lehel. Lisateavet vöötkoodide ja vöötkoodi maskide kohta vt Vöötkoodide [häälestus](set-up-bar-codes.md)[ja Vöötkoodi maskide häälestus](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Kupongikoodi tuleb tagastuskannetele käsitsi rakendada

Kupongi **koodi tuleb käsitsi rakendada tagastuskannete sättele**, mis kehtib ainult tagastamiskannetele, mille jaoks pole müügi sissetulekut antud. Määrake parameetri väärtuseks **Ei**, kui kandele tuleks automaatselt rakendada kupongikoode. Seadke see väärtusele **Jah**, kui kupongikoodid tuleb kandesse käsitsi lisada.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Kasutage organisatsiooni jaoks loodud müügilepinguid

Ettevõtete vahel (B2B) tellimuste puhul, **·** **kui** organisatsiooni parameetri jaoks häälestatud müügilepingute kasutamine on seatud väärtusele Jah, kasutab hinnakujundusmootor müügilepinguid, mis on määratud organisatsioonile kasutaja kliendi hierarhias lepingupõhise hinna määratlemiseks. Kui parameetri väärtuseks **on määratud Ei** või kui kliendi hierarhiat pole määratletud, otsib hinnamootor müügilepinguid, mis on kasutajale määratud lepingupõhise hinna määramiseks. Lisateavet B2B e-commerce’i kliendi hierarhiate kohta vt [B2B-äripartnerite haldamine kliendi hierarhiate abil](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Kanalitaseme hinnakujunduse sätted

Järgmised sätted võimaldavad organisatsioonidel kontrollida hinnakujunduse käitumist kindlates müügikanalites.

### <a name="enable-order-price-control"></a>Tellimuse hinnakontrolli lubamine

Parameeter **Luba tellimuse hinnakontroll** asub kõnekeskuse **konfiguratsioonilehe** üldisel **kiirkaardil**. Säte määrab, kas hinnakujundusmootor jõustab kõnekeskuse kanalis hinna alistamise piirangu. See toimib koos sättega Luba **hinna korrigeerimine** tootetasemel.

Kui tellimuse hinna juhtimine on välja lülitatud, saab iga kõnekeskuse kasutaja teha hinnamuudatusi kõnekeskuse kanali müügiridadele, sõltumata sellest, kas vastavad tooted võimaldavad hinna korrigeerimist.

Kui tellimuse hinna juhtimine on sisse lülitatud, lubavad ainult tooted, mille puhul on parameetri Luba hinna korrigeerimist seatud väärtusele Jah, **·** **võimaldavad** kõnekeskuse kanali müügitellimuste hinnaastleid ja vastavatel müügiridadel tuleb esitada põhjuse kood. Kõnekeskuse kasutaja saab **müügihinda** **muuta ainult kuni kulu hinnalimuse protsendi väärtuseni, mis on määratud jaemüügi \>\> ja ärikanali häälestuse kõnekeskuse \> häälestuse alistamise õigustes.** Kui hinnaesimene alistamine ületab selle protsendi, peab kasutaja esitama taotluse, mis seejärel töödeldakse eelmääratletud Äritöövoogude kaudu ülevaatamiseks ja kinnitamiseks. Lisateavet Äritöövoogude kohta vt töövoo [süsteemi ülevaatest](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Tootetaseme hinnakujunduse sätted

Järgmised sätted jõustavad hinnakujunduse reeglid tootetasemel ja on leitud organisatsiooni toote **konfiguratsioonilehelt**.

### <a name="allow-price-adjust"></a>Hinna korrigeerimise lubamine

Kui parameetri **Luba hinna korrigeerimine** väärtuseks on **seatud** Jah, saab hinna alistamise rakendada tootele kõnekeskuse kanali müügitellimuste kaudu.

### <a name="key-in-price"></a>Hinna sisestamine

Hinnasätte **võti** määratleb, kas võtme hind on kohustuslik, kui toode lisatakse müügikandele kassas. Samuti määrab see vastavad hinnaväärtuse piirangud.

### <a name="zero-price-valid"></a>Nullhind on lubatud

Nullhinna **kehtiv säte** määrab, kas toote eelmääratletud, süsteemi arvutatud või käsitsi korrigeeritud müügihinnad võivad olla 0 (null). Kui nullhind on **lubatud**, määrake parameetri väärtuseks Jah. Seda sätet saab määrata ka Commerce’i tootehierarhia kategooriatasemel.

### <a name="prevent-all-discounts"></a>Kõigi allahindluste ennetamine

Määrates parameetri **Allahindluste keelamine** väärtuseks **Jah**, väldite kõigi allahindluste tüüpide rakendamist (sh käsitsi allahindlused) tootele. Seda sätet saab määrata ka Commerce’i tootehierarhia kategooriatasemel.

> [!NOTE]
> See säte ei piira hinna alistamise toimingut, kuna see toiming seadistab hinna ja seda ei koheldakse allahindlusena.

### <a name="prevent-manual-discounts"></a>Käsitsi määratud allahindluste ennetamine

Määrates parameetri **Enneta käsitsi allahindlusi** väärtusele **Jah**, väldite tootele käsitsi rea- või kande allahindluste rakendamist. Kõiki muid allahindlusi saab siiski rakendada. Seda sätet saab määrata ka Commerce’i tootehierarhia kategooriatasemel.

> [!NOTE]
> See säte ei piira hinna alistamise toimingut, kuna see toiming seadistab hinna ja seda ei koheldakse allahindlusena.

### <a name="prevent-retail-discounts"></a>Takista jaemüügi allahindlust

Kui parameeter **Enneta jaemüügi allahindlusi** on seatud väärtusele **Jah**,**lihtne**, kogus, **·** **lävi**, **·** **segamise** ja sobitamise ja saatmise allahindlused ei saa tootele rakendada. Kõiki muid allahindlusi (k.a käsitsi allahindlused) saab siiski rakendada.

### <a name="prevent-tender-based-discounts"></a>Takista maksevahendipõhiseid allahindluseid

Kui ennetava **maksevahendil põhinevate** allahindluste **parameetri** väärtuseks on seatud **Jah,** ei saa tootele rakendada maksevahendipõhist allahindlust. Kõiki muid allahindlusi (k.a käsitsi allahindlused) saab siiski rakendada.

Jaemüüjad valivad sageli kaubapõhistest allahindlustest (nt lihtsad allahindlused ja koguse allahindlused) teatud tooted (nt uued või nõudmisel kaubad) välja. Kuid nad võivad siiski soovida rakendada maksevahendipõhiseid allahindlusi, kui klient maksab eelistatud maksevahendi abil. Selle tulemuse saavutamiseks **saab** **·** **jaemüüjad seada allahindlused enneta kõik allahindlused ja enneta maksevahendil põhinevaid allahindlusparameetreid väärtusele Ei** ning **·** **·** **ennetada jaemüügi allahindlusi ja enneta käsitsi allahindluste parameetreid väärtusele Jah.**

## <a name="deprecated-or-removed-settings"></a>Taunitud või eemaldatud sätted

Järgmised hinnakujunduse sätted on eemaldatud või plaanitud eemaldamiseks Dynamics 365 Commerce.

| Sätted | Amortiseerimise või eemaldamise põhjus | Amortiseerimise või eemaldamise olek |
|---------|-----------------------------------|-------------------------------|
| Kattuvate allahindluste käsitlemine | Oleme commerce’i parameetrites andnud selle sätte, et kontrollida, kuidas hinnakujundusmootor otsib ja määrab rakendatava parima allahindluse kombinatsiooni. Parim **allahindluse valik** jõudleb hinnakujunduse arvutamisel kõigi võimalike allahindluskombinatsioonide kaudu. Parim **jõudluse suvand** on optimeeritud valik, mis kasutab heuristilise algoritmi ja marginaali väärtuse reitingumeetodit, et määrata õigeaegne tähtsusjärjestus, hinnata ja määrata parim kombinatsioon. Koodi **aluse tasakaalustatud** arvutusvalik töötab sama mis parim **jõudlus**. Seetõttu on see põhiliselt topeltvalik. Jõudluse parandamiseks on hinnakujundusmootor uuendatud, nii et see kasutab standardse valikuna ainult **parimat** jõudlust. Seetõttu ei ole see säte enam rakendatav. | Taunitud 10.0.21 väljalaskes ja eemaldatakse oktoober 2022. |
| Hinnakorrektsioonide võimaldamine toote hinna suurendamiseks | Oleme andnud selle sätte, et kontrollida, kas hinna korrigeerimise funktsioon võib tootehindu tõsta. Kui see parameeter on välja lülitatud, saavad organisatsioonid kasutada hinna korrigeerimise funktsiooni ainult toote ühiku hinna sätetega, et see oleks madalam kui baashind ja kaubanduslelepingu müügihind. Soovitame seda sätet mittedada, kuna hinnakorrektsioonfunktsioon on uuendatud nii, et see toetaks väljast kaht korrektsiooni (kasvu või kahanemist). | Taunitud 10.0.30 väljalaskes ja eemaldatakse oktoober 2023. |
| Luba kaupluse hinna aruanne | Oleme andnud selle sätte, et kontrollida, kas **hinnaaruande** funktsioon on kaupluse konfiguratsioonilehel kasutamiseks saadaval. Me eiuni seda sätet, kuna kaupluse konfiguratsiooni lehte on uuendatud nii, et see esitab alati **hinnaaruande** standardse funktsioonina. | Taunitud 10.0.31 väljalaskes ja eemaldatakse oktoober 2023. |
| Kasuta hindade arvutamiseks tänast kuupäeva | Hinnakujundusmootor Dynamics 365 Supply Chain Management toetab hinnakujunduse arvutust, mis põhineb koos tänase kuupäevaga nõutud lähetuskuupäeval või nõutud vastuvõtukuupäeval. Commerce’i hinnakujunduse mootor toetab ainult tänasel kuupäeval põhinevat hinnakujunduse arvutust. Klientidele, kes kasutavad nii tarneahela haldamise kui ka äri võimalusi, **oleme andnud selle sätte ja soovitame, et kliendid seadistaks selle alati väärtusele Jah**, nii et kaks hinnakujundusmootorit saavad koos töötada. Oleme selle sätte tauninud, kuna see ei muuda põhiselt arvutuse käitumist ja on seetõttu üleliigne. | Taunitud 10.0.31 väljalaskes ja eemaldatakse oktoober 2023. |
| Suurim hind | Oleme andnud selle sätte funktsiooniprofiilis, et kontrollida, kas kassa kaudu saab kindlates kauplustes müüa ainult tooteid, mille müügihind on alla määratud maksimaalse hinna. Me eiuninud seda sätet madala funktsioonikasutuse tõttu. | Taunitud 10.0.31 väljalaskes ja eemaldatakse oktoober 2023. |
| Rakenda ühiku hinnale allahindlused | See säte oli mõeldud kontrollima, kas hinnad ja allahindlused ümardatakse hinnakujunduse arvutamisel ühiku hinnatasemel või müügirea tasemel. See on mittetaunitav, kuna seda ei tarbita kusagil praeguse koodi aluses. | Taunitud 10.0.31 väljalaskes ja eemaldatakse oktoober 2023. |
| Mitme kauba allahindluse käsitsi arvutamine | Oleme andnud selle sätte, et kontrollida, kas hinnakujundusmootor kasutab hilinenud hinnakalkulatsiooni kaupluse kanalis. Kui parameetri väärtuseks on **määratud Jah**, ei arvuta hinnakujundusmootor iga kord, kui kassa rakenduses luuakse või redigeeritakse multiallahindlusi (nt koguse allahindlused, läve allahindlused ning segamise ja sobitamise allahindlused). Oleme otsustanud konsolideerida selle sätte äriparameetrites sarnase sättega, et teha kontroll kanali abil. | Taunitud 10.0.31 väljalaskes ja eemaldatakse oktoober 2023. |

Eemaldatud või taunitud funktsioonide täieliku loendi leiate teemast Dynamics 365 Commerce [Eemaldatud või taunitud funktsioonid Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
