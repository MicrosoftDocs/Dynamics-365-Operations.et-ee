---
title: Poola Intrastat
description: See teema sisaldab teavet Intrastat-aruandluse kohta Poola.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.openlocfilehash: fbacc204208e536291035c6f9bb2ef4fa4038f58
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566087"
---
# <a name="polish-intrastat"></a>Poola Intrastat

[!include[banner](../includes/banner.md)]

**Intrastat** lehte kasutatakse Euroopa Liidu (EL) riikide vahelise kaubavahetuse aruannete loomiseks ja esitamiseks. Poola Intrastati deklaratsioon sisaldab teavet aruandluseks ettetavate kaupade kaubanduse kohta.

Järgmised väljad on lisatud Poola Intrastati deklaratsioonile. Kõik väljad kaasatakse **saabumistel ja lähetamisel, v.a RodzajTransportu** (transpordirežiim) **jaPuhvriPochodzenia** (päritoluriik või -regioon), mida ei kaasata lähetamistel, **ja IdKontrahenta** (kliendi välismaine KM-kood), mida saabumistel ei kaasata.

| Välja nimi | Kirjeldus |
|-------------------------|-------------------------|
| Deklaracja andmed | Dokumendi loomise kuupäev. |
| Miesiac | Deklaratsiooni viitekuu. |
| Omasa | Deklaratsiooni viiteaasta |
| Number | Deklaratsiooni number viiteperioodis. |
| Wersja | Deklaratsiooni versiooninumber |
| Välja nrWlas väljad | Deklaratsiooni identifikaator Väärtus luuakse automaatselt. |
| Typ | Aruande suund.</br><li>Saabumiste puhul prinditakse "P".</li><li>Lähetuste puhul prinditakse "W".</li> |
| Rodzaj | Deklaratsiooni tüüp Väärtus näitab, kas aruanne on algse deklaratsiooni või parandusdeklaratsiooni. |
| UC | Ühiku kood, mille kohta Intrastat-deklaratsioon on adresseeritakse. Väärtus määratakse vahekaardi **Väliskaubanduse parameetrid** **·** **agendi** jaotise Käibemaksukohuslase kood väljal Maksukohuslase **kood.** |
| Nazwa | Ettevõtte nimi. |
| Miejscoscoscosc,IndikaatorNumer, KodPo slots | Juriidilise isiku täielik aadress. |
| Nip | Poola maksu ID-kood (käibemaksu [VAT] ID). |
| Piirkond | Poola statistiline ID-kood (ettevõtte number). |
| Kausta KaustaWartoscFaktur | Arve väärtuste summa. |
| Kausta KaustaWartoscStatystytoolna | Statistiliste väärtuste summa. |
| LisadeLiaasibaPozarcdži | Kaupade koguarv. |
| Selle välja ID | Kauba järjenumber. |
| Väljade OpisT sünkroonitud väljad | Kauba kaubandusnimi. |
| OmastepochodzeniaAatidek | Rahvusvaheliselt standardiorganisatsiooni (ISO) kood ksi poole riigile või regioonile. |
| Selle artikli nimi on < a0/&. | Tarnetingimuste Intrastati kood. |
| RodzajTransakcji | Kande olemust näitav kood. Poola ettevõtted kasutavad kahenumbrilist kandekoodi. |
| KodTowartool | Kaheksakohaline kaubaartiklikood vastavalt kombineeritud nomendgrupile. |
| RodzajTransportu | Intrastati transpordiviisi kood. |
| OmaoPochodzenia | Riigi või regiooni ISO-kood, kus kaubad toodeti või toodeti. |
| MasaNetto | Netomass täis kilogrammides. |
| Ilosc UsbupelniajacaJm | Kogus lisa mõõtühikutes täisarvudes. |
| (<a0/&) | Kõigi ühe kaubaga kaetud kannete arve väärtus. |
| MinustoscStatystytoolna | Statistiline väärtus. |
| Dublinpelniajacy:EttiwiskoImie, Telefon, Faks, Meil | Deklaratsiooni esitanud isiku ees- ja perekonnanimi, telefoninumber, faksinumber ja meiliaadress. |
| IDKontrahenta | Kliendi välismaine KM-kood EL liikmesriikides. |


## <a name="set-up-intrastat"></a>Intrastati seadistamine

Globaalsest hoidlast importige järgmiste elektroonilise aruandluse (ER) konfiguratsioonide uusim versioon:

   - Intrastati mudel
   - Intrastat-aruanne
   - Intrastat (PL)

Lisateavet leiate teemast [ER konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Km-i ID ja ettevõtte numbri seadistamine teie ettevõttele

### <a name="create-registration-types-for-company-codes"></a>Ettevõttekoodide registreerimistüüpide loomine

Peate ettevõtte koodide jaoks looma kaks registreerimistüüpi: üks KM-i ID-le (NIP-kood) ja teine ettevõttekoodile (Regon-kood).

1. Minge organisatsiooni **administratsiooniglobal** > **aadressiraamatusseRegistration** > **typesRegistration** > **.**
2. Tegevuspaanil valige **UUS**, et luua KM-i ID jaoks registreerimistüüp.
3. **Sisestage uue registreerimise** tüübi nimi **dialoogiboksi Registreerimise** tüübi üksikasjad väljale Nimi. Näiteks sisestage **NIP**.
4. Väljal **Riik/regioon** valige **POL**.
5. Valige **Loo**.
6. Tegevuspaanil valige **uus**, et luua ettevõttenumbrile registreerimistüüp.
7. **Sisestage uue registreerimise** tüübi nimi **dialoogiboksi Registreerimise** tüübi üksikasjad väljale Nimi. Näiteks sisestage **Tagasigon**.
8. Väljal **Riik/regioon** valige **POL**.
9. Valige **Loo**.

### <a name="match-the-registration-types-with-registration-categories"></a>Vastenda registreerimistüübid registreerimiskategooriatega

1. Minge organisatsiooni **administratsiooniGlobal** > **aadressiraamatusseRegistration** > **typesRegistration** > **·**.
2. Tegevuspaanil valige **Uus**, et luua link iga loodud registreerimistüübi ja registreerimiskategooria vahel.

    - Käibemaksu ID (NIP-kood) registreerimistüübi jaoks valige käibemaksu **ID registreerimiskategooria**.
    - Ettevõtte numbri (Regoni kood) registreerimistüübi jaoks valige **ettevõtte ID (COID) registreerimiskategooria**.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Km-i ID ja ettevõtte numbri seadistamine teie ettevõttele

1. Avage **Organisatsiooni haldus** > **Organisatsioonid** > **Juriidilised isikud**.
2. Ruudustikus valige oma ettevõte.
3. Tegevuspaanil valige registreerimiste **ID-d**.
4. Valige kiirkaardil **Registreerimise ID** suvand **Lisa**.
5. Väljal Registreerimise **tüüp** valige üks varem loodud registreerimistüüpidest.
6. Sisestage oma ettevõtte KM-i ID (NIP-kood) või ettevõtte number (Regoni kood), sõltuvalt eelmises sammus valitud registreerimistüübist.
7. Korrake varem loodud muu registreerimise tüübi puhul samme 4 kuni 6.

## <a name="set-up-a-company-address"></a>Ettevõtte aadressi seadistamine

1. Avage **Organisatsiooni haldus** > **Organisatsioonid** > **Juriidilised isikud**.
2. Ruudustikus valige oma ettevõte.
3. Valige vahekaardil **Aadressid** suvand **Redigeeri**.
4. **Valige dialoogiboksi Aadressi** redigeerimine väljal **Sihtnumber** oma ettevõtte sihtnumber.
5. Sisestage **väljale** Tänav oma aadress.
6. **Väljal Linn** valige oma linn.

## <a name="set-up-foreign-trade-parameters"></a>Väliskaubanduse parameetrite häälestamine

1. Minge kaubandusparameetritele **TaxSetupForeign** > **·** > **·**.
2. **Valige Intrastati** (**PL) väljal Elektroonilise** **·** **aruandluse kiirkaardil Intrastati (PL) failivormingu vastendamine.**
3. Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.
4. Valige kiirkaardi **Kaubaartikli hierarhia** väljal **Kategooriahierarhia** väärtus **Intrastat**.
5. Väljal **Kande kood** valige varaülekannete kandekood. Seda koodi kasutatakse tehingute jaoks, mis põhjustavad vara tegeliku või kavandatud üleandmise hüvitise eest (finantsiline ja muu). Seda kasutatakse ka paranduste puhul. Poola ettevõtted kasutavad kahenumbrilist kandekoodi.
6. Väljal **Kreeditmärge** valige kandekood kaupade tagastamiseks.
7. Vahekaardil **Riigi/regiooni atribuudid** väljal **Riik/regioon**, loetlege kõik riigid või regioonid, millega teie organisatsioonil on ärisuhted. Iga EL-i osa oleva **riigi** **jaoks valige EL riigi/piirkonna tüübi** väljal, nii et riik kuvatakse teie Intrastat-aruandes. Poola puhul valige riigi **/** regiooni **tüübi väljal Kodumaine**.
8. Sisestage **·** **agendi vahekaardi Kiirkaardi Agent** **·** **jaotises Käibemaksukohuslase kood väljale Maksukohuslase kood** 420000 **, et näidata ühiku koodi,** mille jaoks Intrastat-deklaratsioon on adresseeritakse.
9. **Vahekaardile Kontakt** sisestage deklaratsiooni esitava isiku nimi, telefoninumber, faksinumber ja meiliaadress.
10. Määrake XML-failinumbri **viite numbriseeria väljal Numbriseeria kood mittejärjekorraline numbriseeria, mille lubatud maksimumpikkus** **·** **on üheksa tähemärki.** Seda välja kasutatakse Intrastat-aruande deklaratsiooni **identifikaatori välja** väärtuse automaatseks loomiseks.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Saate häälestada intrastati deklaratsiooni tooteparameetreid.

1. Avage **Tooteteabe haldus** > **Tooted** > **Väljastatud tooted**.
2. Valige ruudustikus toode.
3. Kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige sobiv kauba kood. Kauba nimi prinditakse **Intrastat-aruande kaubakirjelduse** väljale.
4. **Valige jaotise** Päritolu väljal **Riik/regioon** toote päritoluriik või -regioon.
5. Kiirkaardi **Varude haldamine** jaotise **Kaaluühikud** väljale sisestage toote kaal kilogrammides.

## <a name="set-up-compression-of-intrastat"></a>Seadista Intrastati tihendamine

-   Minge **Maks** > **Seadistamine** > **Väliskaubandus** > **Intrastati kompressioon** ja valige väljad, mida tuleb Intrastati teabe summeerimisel võrrelda. Poola Intrastati jaoks valige järgmised väljad:

    - Artikkel
    - Kandekood
    - Päritoluriik/-regioon
    - Transport
    - Tarnetingimused
    - Saatja riik/regioon
    - Riik/regioon
    - Parandus
    - Maksuvabastuse number
    - Suund
    - Arve

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Transpordimeetodi ja tarnetingimuste seadistamine

1.  Transpordikoodide seadistamine.

    1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Transpordimeetodid**.
    2. Valige toimingupaanil nupp **Uus**.
    3. Sisestage **kordumatu** kood väljale Transport. Poola ettevõtted kasutavad ühekohalist transpordikoodi.

2.  Saate seadistada tarneviisi Intrastat-koodid.

    1. Minge tarnelepingu **juurde Hanke ja hankeseSetupDistributionTerms** > **·** > **·** > **·**.
    2. Valige ruudustikus tarnetingimuste komplekt.
    3. **Intrastati** koodiväljal General **FastTab** sisestage kordumatu kood.

## <a name="intrastat-transfer"></a>Intrastati ülekanne

**Intrastati** lehel saate valida tegevuspaanil valiku **Ülekanne**, et edastada automaatselt oma müügitellimuste, vabas vormis arvete, ostutellimuste, hankija arvete, hankija toote sissetulekute, projektiarvete ja üleviimistellimuste teabe automaatne ülekandmine. Edastatakse ainult dokumendid, mille siht- või saadetise riik või regioon on EL riik.

Kandeid saate sisestada ka käsitsi, valides **tegevuspaanil** valiku Uus.

### <a name="generate-an-intrastat-report"></a>Looge Intrastati aruanne

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Toimingupaanil valige suvandid **Väljund** &gt; **Aruanne**.
3. Määrake dialoogiboksis **Intrastati aruanne** järgmised väljad.

    | Field | Kirjeldus |
    |-------------------------|-------------------------|
    | Kehtivuse alguskuupäev | Valige aruande alguskuupäev. |
    | Loo fail | Intrastat-aruande jaoks **xml-faili** loomiseks valige väärtuseks Jah. |
    | Failinimi | Sisestage .xml-faili nimi. |
    | Aruande loomine | .xlsx faili genereerimiseks Intrastati aruande jaoks määrake suvandi väärtuseks **Jah**. |
    | Aruandefaili nimi | Sisestage .xlsx faili nimi. |
    | Direction | Valige ühendusesiseste saabumiste aruande jaoks **Saabumised**.</br>Valige ühendusesiseste lähetuste aruande jaoks **Lähetused**. |
    | Deklaratsiooni identifikaator | Dokumendi ID luuakse automaatselt ja seda saab uuendada. |
    | Deklaratsiooni tüüp | Valige **algse** deklaratsiooni deklaratsioon.</br>Valige **deklaratsiooni parandus – parandusdeklaratsiooni** asendamine, mis on mõeldud olemasoleva eelnevalt esitatud algse või parandusdeklaratsiooni täielikuks asendamiseks. |
    | Dokumendi loomise linn | Sisestage väärtus, mis tuleks printida Intrastat-deklaratsiooni **väljale Miejscoscosc**. |
    | Dokumendi loomise kuupäev | Saate sisestada intrastati deklaratsiooni väljale **Deklaracja Data** prinditava väärtuse. |
    | Dokumendi nr | Saate sisestada intrastati deklaratsiooni väljale **Number prinditav** väärtuse. |
    | Dokumendiversioon | Saate sisestada intrastati deklaratsiooni väljale **Wersja** prinditav väärtuse. |

4. Valige **OK** ja vaadake loodud aruanded üle.

## <a name="example"></a>Näide

See näide näitab, kuidas Sisestada Intrastati saabumised ja lähetamised, kasutades **DEMF-i juriidilist** isikut.

### <a name="preliminary-setup"></a>Esialgne seadistamine

Importige elektroonilise aruandluse (ER) konfiguratsioonide uusim versioon:

   - Intrastati mudel
   - Intrastat-aruanne
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Ettevõtte aadressi seadistamine

1. Avage **Organisatsioonihaldus** > **Globaalne aadressiraamat** > **Aadress** > **Aadressi seadistus**.
2. **Vahekaardil Linn** valige **Uus**.
3. Väljal **Riik/regioon** valige **POL**.
4. Väljale Linn **sisestage** **Varssavi**.
5. Valige vahekaardil **Sihtnumber** suvand **Uus**.
6. Väljal **Riik/regioon** valige **POL**.
7. **Väljal Linn** valige **Varssavi**.
8. Sisestage **väljale Sihtnumber** **00-844**.
9. Minge **organisatsiooni haldus** > **organisatsioon** > **juriidilised isikud** ja valige **DEMF** juriidiline isik.
10. Kiirkaardil **Aadressid** valige **Redigeeri**.
11. Väljal **Riik/regioon** valige **POL**.
12. Väljal Sihtnumber **valige** **31-111**.
13. Väljale Tänav **sisestage** **Statystynavna 22/1**.
14. **Väljal Linn** valige **Varssavi**.
15. Valige nupp **OK**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>KM-i ID ja ettevõttekoodi seadistamine teie ettevõtte jaoks

### <a name="create-registration-types-for-company-codes"></a>Ettevõttekoodide registreerimistüüpide loomine

1. Minge organisatsiooni **administratsiooniglobal** > **aadressiraamatusseRegistration** > **typesRegistration** > **.**
2. Tegevuspaanil valige **uus**, et luua km-i ID-le (NIP-kood).
3. Dialoogiaknas **Sisestage registreerimise** tüübi üksikasjad väljale **Nimi sisestage** **NIP**.
4. Väljal **Riik/regioon** valige **POL**.
5. Valige **Loo**.
6. Tegevuspaanil valige **uus**, et luua ettevõtte numbrile registreerimistüüp (regoni kood).
7. Sisestage **dialoogiboksi Registreerimise tüübi** üksikasjad väljale **Nimi** väärtus **Tagasikast**.
8. Väljal **Riik/regioon** valige **POL**.
9. Valige **Loo**.

### <a name="match-the-registration-types-with-registration-categories"></a>Vastenda registreerimistüübid registreerimiskategooriatega

1. Minge organisatsiooni **administratsiooniGlobal** > **aadressiraamatusseRegistration** > **typesRegistration** > **·**.
2. Tegevuspaanil valige **Uus**, et luua link iga loodud registreerimistüübi ja registreerimiskategooria vahel.

    - NIP-registreerimise **tüübi** puhul valige käibemaksu **ID registreerimise** kategooria.
    - Valige Registreerimise **tüübiKs Regon** ettevõtte **ID (COID).**

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Km-i ID ja ettevõtte numbri seadistamine teie ettevõttele

1. Avage **Organisatsiooni haldus** > **Organisatsioonid** > **Juriidilised isikud**.
2. Valige ruudustikus **DEMF**.
3. Tegevuspaanil valige registreerimiste **ID-d**.
4. Valige kiirkaardil **Registreerimise ID** suvand **Lisa**.
5. Väljal Registreerimise **tüüp** valige **NIP**.
6. Väljale Registreerimisnumber **sisestage** 1234567890 **·**.
7. Valige **Lisa**.
8. Väljal Registreerimise **tüüp** valige Käsk **Muuda.**
9. Väljale Registreerimisnumber **sisestage** 12345678901234 **·**.

### <a name="set-up-a-number-sequence-code"></a>Numbriseeria koodi häälestamine

1. Avage **Organisatsiooni haldus** > **Numbriseeriad** > **Numbriseeriad**.
2. Valige tegevuspaani vahekaardil **Numbriseeria** jaotises Uus **väärtus** **Numbriseeria**.
3. Sisestage **Koodi** kiirkaardi väljale **Numbriseeria kood** **XMLfile\_**.
4. **Valige ulatuse parameetrite** kiirkaardi väljal **Ulatus** suvand **Ettevõte**.
5. Väljal Ettevõte **valige** **DEMF**.
6. Kiirkaardi segmendid väljale Pikkus tähe- ja numbrimärkidest **märkides** sisestage **4**.**·** **·**
7. Seadke jaotise **Häälestus jaotise** Üldine kiirkaardi **pidev suvandiks** **Ei** **.**
8. Sisestage **jaotise** Suurim väljale Numbri **eraldamine** **9999**.

### <a name="set-up-foreign-trade-parameters"></a>Väliskaubanduse parameetrite häälestamine

1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Väliskaubanduse parameetrid**.
2. Valige vahekaardil **Intrastat** kiirkaardil **Üldine** väljal **Kande** **kood** väärtus **11**.
3. Elektroonilise aruandluse **kiirkaardi** väljal Failivormingu vastendamine **valige** **Intrastat (PL).**
4. Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.
5. Veenduge, **et kaubakoodi** hierarhia kiirkaardil on kategooriahierarhia **väljal** seatud **Intrastat.**
6. Klõpsake vahekaardil **Riigi/regiooni atribuudid** valimiseks **Uus**.
7. Väljal **Riik/regioon** valige **POL**. Seejärel valige väljal **Riigi/regiooni tüüp** suvand **Kodumaine**.
8. Väljal **Riik/regioon** valige **DEU**. Seejärel valige väljal **Riigi/regiooni tüüp** EL **·**.
9. Sisestage agendi **kiirkaardi** **·** **vahekaardi Agent jaotises Käibemaksukohuslase kood väljale Maksukohuslase kood** **420000.** **·**
10. Vahekaardi Kontakt **väljal Nimi sisestage** **ManishKlahvira** **.**
11. Väljale Telefon **sisestage** **425-555-5068**.
12. Väljale Faksinumber **sisestage** 425-555-5049 **·**.
13. Sisestage **väljale** Meil manishc@contoso.com **·**.
14. **Valige XML-failinumbri** viite numbriseeria **koodi väljal** **numbriseeriate vahekaardil XML-fail** **\_**.

### <a name="set-up-product-information"></a>Seadistage tooteteave

1. Minge tooteteabe **haldusseProductsReleased** > **·** > **·** **tooted.**
2. Valige ruudustikus **D0001**.
3. Valige kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige **100 200 30**.
4. Kiirkaardi **Varude haldamine**  jaotise **Kaaluühikud** väljale **Netokaal** sisestage **2**.
5. Valige toimingupaanil nupp **Salvesta**.
6. Valige ruudustikus **D0003**.
7. Valige kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige **100 200 30**.
8. **Päritolu** jaotises **Riik/regioon** väljal valige **DEU**.
9. Kiirkaardi **Varude haldamine**  jaotise **Kaaluühikud** väljale **Netokaal** sisestage **5**.
10. Valige toimingupaanil nupp **Salvesta**.

### <a name="change-the-site-address"></a>Muutke saidi aadressi

1. Avage jaotis **Warehouse management** > **Seadistus** > **Ladu** > **Saidid**.
2. Valige ruudustikus **1**.
3. Kiirkaardil **Aadressid** valige **Redigeeri**.
4. Dialoogiakna **Aadressi redigeerimine** väljal **Riik/regioon** valige **POL**.
5. Valige nupp **OK**.

### <a name="set-up-a-transport-method"></a>Transpordimeetodi seadistamine

1. Saate luua transpordimeetodi.

    1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Transpordimeetodid**.
    2. Valige toimingupaanil nupp **Uus**.
    3. Väljale Transport **sisestage** **3**.
    4. Sisestage **väljale** Kirjeldus Väärtus **transport**.

2. Määrake tarneviisile uus transpordiviis. Sel viisil saate seadistada vaikeväärtused, mida kasutatakse transpordiviisi puhul, kui valitakse vastav tarneviis.

    1. Minge jaotisse **Ostmine ja hankimine** > **Seadistamine** > **Tarneviis** > **Saatmise mudel**.
    2. Valige ruudustikus **10**.
    3. Kiirkaardi **Väliskaubandus** väljal **Transport** valige **3**.

3. Valige kliendile tarnimise vaikerežiim.

    1. Avage **Müügireskontro** > **Kliendid** > **Kõik kliendid**.
    2. Valige ruudustikus DE-016 **·**.
    3. Valige arve **ja tarne** kiirkaardi väljal **Tarneviis** väärtus **10**.

4. Saate valida hankija jaoks vaikimisi tarneviisi.

    1. Minge hankijatele **OstureskontroVendorsAll** > **·** > **·**.
    2. Valige ruudustikus DE-001 **·**.
    3. Valige arve **ja tarne** kiirkaardi väljal **Tarneviis** väärtus **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Tarnetingimuste koodide seadistamine

1. Saate tarnetingimuste jaoks seadistada Intrastat-koodi.

    1. Minge tarnelepingu **juurde Hanke ja hankeseSetupDistributionTerms** > **·** > **·** > **·**.
    2. Valige ruudustikus **CIF**.
    3. Intrastati **koodi** väljal General FastTab **sisestage** **CIF**.

2. Saate valida kliendi puhul vaikimisi soovitud tarnetingimused.

    1. Avage **Müügireskontro** > **Kliendid** > **Kõik kliendid**.
    2. Valige ruudustikus DE-016 **·**.
    3. Valige ARVE **ja tarne** kiirkaardil tarnetingimuste **väljal** **CIF**.

3. Saate valida hankija puhul vaikimisi soovitud tarnetingimused.

    1. Minge hankijatele **OstureskontroVendorsAll** > **·** > **·**.
    2. Valige ruudustikus DE-001 **·**.
    3. Valige ARVE **ja tarne** kiirkaardil tarnetingimuste **väljal** **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>EL-i kliendi maksukohustuslase koodi kontrollimine

1. Avage **Müügireskontro** > **Kliendid** > **Kõik kliendid**.
2. Valige ruudustikus DE-016 **·**.
3. Käibemaksu jaotise **arve ja tarne** kiirkaardil **veenduge**, **et maksukohuslase koodi välja väärtuseks** **on seatud DE9012**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Looge müügitellimus EL-i kliendiga

1. Avage **Müügireskontro** > **Tellimused** > **Kõik müügitellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Loo müügi tellimus** jaotises **Klient** väljas **Kliendi** jaotises **Kliendi konto** väljal väärtus **De-016**.
4. Valige **Üldine** kiirkaardi jaotise **Ladustamisdimensioonid** väljal **Saidi väärtus** väärtus **1**.
5. Valige väljal **Ladu** väärtus **11**.
6. Kontrollige **vahekaardil** Aadress, **·** **et väli Aadress on seatud väärtusele Te veebiaadressiks 12,Cher, 24103, DEU**, sest klient on Saksamaalt.
7. Valige nupp **OK**.
8. Kontrollige **päise** vahekaardil tarne **kiirkaardil**, **·** **et tarnetingimuste välja väärtuseks on seatud CIF** ja **·** **tarneviisi välja väärtuseks on seatud 10.**
9. Valige **Read** vahekaardil **Müügi tellimuse ridade** väljal **Kaubakoodi** väärtuseks **D0001**. Sisestage väljale **Kogus** väärtus **8**.
10. **Väliskaubanduse** vahekaardi rea üksikasjade kiirkaardil veenduge, **·** **et kande koodi välja väärtuseks on seatud 11**, **·** **kauba väli on seatud 100 200 30** **ja päritoluriik/** **-regioon on** **seatud VALIKUle POL.**
11. Valige toimingupaanil nupp **Salvesta**.
12. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
13. Valige dialoogiboksi **Arve sisestamine** kiirkaardi **Parameetrid** jaotises **Parameeter** väljal **Kogus** suvand **Kõik**.
14. **Valige kiirkaardi Setup** FastTab **väljal Müügikuupäev** **10/18/2021** (18. oktoober 2021).
15. Klõpsake sissetuleku sisestamiseks nuppu **OK**.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Kandke kanne üle Intrastati töölehele ja vaadake tulemus üle

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Valige tegevuste paanil käsk **Insener**.
3. Seadke dialoogiboksi **Intrastat (ülekanne)** jaotises **Parameetrid** valiku **Kliendiarve** väärtuseks **Jah**.
4. Valige **Filter**.
5. Valige intrastati **filtri** dialoogiboksi vahekaardil **Vahemik esimene** rida ja veenduge, **et välja väärtuseks** on seatud **Kuupäev**.
6. Valige **Kriteeriumid** väljal praegune kuupäev.
7. Valige dialoogiboksi **Intrastat filter** sulgemiseks **OK**.
8. Valige **OK**, et sulgeda **Intrastati (ülekanne)** dialoogiboks ja vaadake tulemus üle. Rida tähistab varem loodud müügitellimust.

    ![Rida tähistab Intrastati lehe müügitellimust](media/intrastat_pl_1.png)

9. Valige kande rida ja seejärel valige vahekaart **Üldine**, et vaadata rohkem üksikasju.

    ![Müügitellimuse üksikasjad intrastati lehe vahekaardil Üldine](media/intrastat_pl_2.png)

10. Toimingupaanil valige suvandid **Väljund** > **Aruanne**.
11. **Valige dialoogiboksi Intrastat-aruanne** **·** **·** **kiirkaardi Parameetrid jaotises Kuupäev väljal Alates kuupäevast** praeguse kuu esimene päev.
12. Seadke jaotises **Ekspordi** **suvandid**, suvandi **Loo fail** väärtuseks **Jah**. Siis sisestage faili nõutav nimi väljale **Faili nimi**.
13. Määrake suvand **Loo aruanne** valikule **Jah**. Siis sisestage nõutav nimi väljale **Aruande faili nimi**.
14. Valige **Saadetised** väljalt **Suund**.
15. Kontrollige **failivormingu vastendamise** jaotises, et deklaratsiooni **tüübi väli** on seatud väärtusele **Deklaratsioon**.
16. Sisestage **väljale Dokumendi loomis** linn **Väärtus.**
17. Valige dokumendi **loomise kuupäeva väljal** **10/19/2021 (19** . oktoober 2021).
18. Väljale Dokumendi **nr** sisestage **11**.
19. Väljale Dokumendi **versioon** sisestage **22**.
20. Valige **OK** ja vaadake aruanne üle LOODUD XML-vormingus. Järgmine tabel näitab näidisaruande väärtusi.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Välja nimi</strong></p>
    </td>
    <td>
    <p><strong>Välja kirjeldus</strong></p>
    </td>
    <td>
    <p><strong>Väärtus</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Teave dokumendi kohta</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja andmed</p>
    </td>
    <td>
    <p>Dokumendi loomise kuupäev.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscosesc</p>
    </td>
    <td>
    <p>Linn, kus dokument loodi.</p>
    </td>
    <td>
    <p>Kraków</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LisadeLiaasibaPozarcdži</p>
    </td>
    <td>
    <p>Kaupade koguarv.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Kausta KaustaWartoscStatystytoolna</p>
    </td>
    <td>
    <p>Kogu statistiline väärtus.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Kausta KaustaWartoscFaktur</p>
    </td>
    <td>
    <p>Arve koguväärtus.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Ühiku kood.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Deklaratsiooni tüüp</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Dokumendi versioon.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Number</p>
    </td>
    <td>
    <p>Dokumendi number.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Viitekuu.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Omasa</p>
    </td>
    <td width="330">
    <p>Viiteaasta.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>Aruande suund.</p>
    </td>
    <td>
    <p>K</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Välja nrWlas väljad</p>
    </td>
    <td width="330">
    <p>Deklaratsiooni identifikaator</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Ettevõtte teave</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscosesc</p>
    </td>
    <td width="330">
    <p>Ettevõtte asukohalinn.</p>
    </td>
    <td>
    <p>Varssavi</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Piirkond</p>
    </td>
    <td width="330">
    <p>Ettevõtte regoni kood.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Ettevõtte NIP-kood.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPo slots</p>
    </td>
    <td>
    <p>Ettevõtte sihtnumber.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IicaNumer</p>
    </td>
    <td>
    <p>Ettevõtte asukoha tänav.</p>
    </td>
    <td>
    <p>Statystyaaaa 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Ettevõtte nimi.</p>
    </td>
    <td>
    <p>Contoso meelelahutussüsteem Saksamaa</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Teave hea kohta</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MinustoscStatystytoolna</p>
    </td>
    <td>
    <p>Statistiline väärtus.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>(<a0/&)</p>
    </td>
    <td>
    <p>Arve väärtus.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Netomass.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IDKontrahenta</p>
    </td>
    <td>
    <p>Kliendi KM-kood.</p>
    </td>
    <td>
    <p>De9012 (uuendatud)</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowartool</p>
    </td>
    <td>
    <p>Artiklikood</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Kande kood.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Selle artikli nimi on < a0/&.</p>
    </td>
    <td>
    <p>Tarneviisi tingimused.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OmastepochodzeniaAatidek</p>
    </td>
    <td>
    <p>Lähetus-/sihtriigi või -regiooni kood.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Väljade OpisT sünkroonitud väljad</p>
    </td>
    <td>
    <p>Kaupade kirjeldus.</p>
    </td>
    <td>
    <p>Riistvara</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Selle välja ID</p>
    </td>
    <td>
    <p>Kaubakood.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Kontaktandmed</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Meil</p>
    </td>
    <td>
    <p>Edastaja meiliaadress.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks (faks)</p>
    </td>
    <td>
    <p>Edastaja faksinumber.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Edastaja telefoninumber.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>VäljaminevskoImie</p>
    </td>
    <td>
    <p>Edastaja nimi.</p>
    </td>
    <td>
    <p>Tiksa väljak</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Vaadake loodud fail Exceli vormingus üle.

    ![Lähetuste Intrastat-aruanne](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Avage **Ostureskontro** > **Ostutellimused** > **Kõik ostutellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Hankija konto** suvand **DE-001**.
4. Valige väljal **Sait** väärtus **1**.
5. **Väljal Ladu** valige **11**.
6. Valige nupp **OK**.
7. Kontrollige **päise** vahekaardil tarne **kiirkaardil**, **·** **et tarneviisi välja väärtuseks on seatud 10** ja **tarnetingimuste** välja väärtuseks on **seatud CIF.**
8. Valige **Read** vahekaardil **Müügi tellimuse ridade** väljal **Kaubakoodi** väärtuseks **D0003**. Sisestage väljale **Kogus** väärtus **6**.
9. **Kaubarea üksikasjade** kiirkaardi vahekaardil Väliskaubandus veenduge, **·** **et kande koodiks on seatud 11**,**·** **transpordivälja väärtuseks on seatud 3**, **kauba väli** **on** **seatud 100 200 30** **ja päritoluriik/-regioon** **on seatud väärtusele DEU.**
10. Valige toimingupaanil vahekaardi **Ostmine** grupis **Tegevused** suvand **Kinnita**.
11. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
12. Valige tegevuspaanil **vaikekogus** ja **seejärel valige ridade vaikekogus** väljal Tellitud **kogus**. Seejärel valige **OK**.
13. Sisestage **hankija arve** päise kiirkaardi jaotise **Arve ID** väljale **Number** väärtus **00010**.
14. **Valige väljal Arve** kuupäev jaotises **Arve kuupäevad** praegune kuupäev. Seda kuupäeva kasutatakse Intrastati ülekandmiseks.
15. Valige dokumendi **vastuvõtukuupäeva väljal** **10/18/2021** (18. oktoober 2021).
16. Valige arve postitamiseks toimingupaanilt **Postita**.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Intrastati deklaratsiooni loomine saabumiste jaoks

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Valige tegevuste paanil käsk **Insener**.
3. Dialoogiboksis **Intrastat (ülekanne)** seadke **hankija arve** valikuks **Jah**.
4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut.

    ![Rida, mis tähistab ostutellimust Intrastati lehel](media/intrastat_pl_4.png)

5. Vaadake üle teave vahekaardil **Üldine** ostutellimuse puhul.

    ![Ostutellimuse üksikasjad intrastati lehe vahekaardil Üldine](media/intrastat_pl_5.png)

6. Toimingupaanil valige suvandid **Väljund** > **Aruanne**.
7. **Valige dialoogiboksi Intrastat-aruanne** **·** **·** **kiirkaardi Parameetrid jaotises Kuupäev väljal Alates kuupäevast** praeguse kuu esimene päev.
8. Seadke jaotises **Ekspordi** **suvandid**, suvandi **Loo fail** väärtuseks **Jah**. Siis sisestage faili nõutav nimi väljale **Faili nimi**.
9. Määrake suvand **Loo aruanne** valikule **Jah**. Siis sisestage nõutav nimi väljale **Aruande faili nimi**.
10. Valige **Suund** väljalt **Saabumised**.
11. Kontrollige **failivormingu vastendamise** jaotises, et deklaratsiooni **tüübi väli** on seatud väärtusele **Deklaratsioon**.
12. Sisestage **väljale Dokumendi loomis** linn **Väärtus.**
13. Valige dokumendi **loomise kuupäeva väljal** **10/19/2021 (19** . oktoober 2021).
14. Väljale Dokumendi **nr** sisestage **11**.
15. Väljale Dokumendi **versioon** sisestage **22**.
16. Valige **OK** ja vaadake aruanne üle LOODUD XML-vormingus. Järgmine tabel näitab näidisaruande väärtusi.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Välja nimi</strong></p>
    </td>
    <td>
    <p><strong>Välja kirjeldus</strong></p>
    </td>
    <td>
    <p><strong>Väärtus</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Teave dokumendi kohta</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja andmed</p>
    </td>
    <td>
    <p>Dokumendi loomise kuupäev.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscosesc</p>
    </td>
    <td>
    <p>Linn, kus dokument loodi.</p>
    </td>
    <td>
    <p>Kraków</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LisadeLiaasibaPozarcdži</p>
    </td>
    <td>
    <p>Kaupade koguarv.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Kausta KaustaWartoscStatystytoolna</p>
    </td>
    <td>
    <p>Kogu statistiline väärtus.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Kausta KaustaWartoscFaktur</p>
    </td>
    <td>
    <p>Arve koguväärtus.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Ühiku kood.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Deklaratsiooni tüüp</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Dokumendi versioon.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Number</p>
    </td>
    <td>
    <p>Dokumendi number.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Viitekuu.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Omasa</p>
    </td>
    <td width="332">
    <p>Viiteaasta.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>Aruande suund.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Välja nrWlas väljad</p>
    </td>
    <td width="332">
    <p>Deklaratsiooni identifikaator</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Ettevõtte teave</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscosesc</p>
    </td>
    <td width="332">
    <p>Ettevõtte asukohalinn.</p>
    </td>
    <td>
    <p>Varssavi</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Piirkond</p>
    </td>
    <td width="332">
    <p>Ettevõtte regoni kood.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Ettevõtte NIP-kood.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPo slots</p>
    </td>
    <td>
    <p>Ettevõtte sihtnumber.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IicaNumer</p>
    </td>
    <td>
    <p>Ettevõtte asukoha tänav.</p>
    </td>
    <td>
    <p>Statystyaaaa 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Ettevõtte nimi.</p>
    </td>
    <td>
    <p>Contoso meelelahutussüsteem Saksamaa</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Teave hea kohta</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MinustoscStatystytoolna</p>
    </td>
    <td>
    <p>Statistiline väärtus.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>(<a0/&)</p>
    </td>
    <td>
    <p>Arve väärtus.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Netomass.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OmaoPochodzenia</p>
    </td>
    <td>
    <p>Päritoluriiki või -regiooni kood.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Transpordikoodi transpordiviis.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowartool</p>
    </td>
    <td>
    <p>Artiklikood</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Kande kood.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Selle artikli nimi on < a0/&.</p>
    </td>
    <td>
    <p>Tarneviisi tingimused.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OmastepochodzeniaAatidek</p>
    </td>
    <td>
    <p>Lähetus-/sihtriigi või -regiooni kood.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Väljade OpisT sünkroonitud väljad</p>
    </td>
    <td>
    <p>Kaupade kirjeldus.</p>
    </td>
    <td>
    <p>Riistvara</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Selle välja ID</p>
    </td>
    <td>
    <p>Kaubakood.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Kontaktandmed</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Meil</p>
    </td>
    <td>
    <p>Edastaja meiliaadress.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks (faks)</p>
    </td>
    <td>
    <p>Edastaja faksinumber.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Edastaja telefoninumber.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>VäljaminevskoImie</p>
    </td>
    <td>
    <p>Edastaja nimi.</p>
    </td>
    <td>
    <p>Tiksa väljak</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Vaadake loodud fail Exceli vormingus üle.

    ![Intrastati aruanne saabumiste kohta](media/intrastat_pl_6.png)
