---
title: Koondplaneerimise installiviisard
description: Selles teemas kirjeldatakse mitmesuguseid olulisi strateegiaid ja parameetreid, mida kasutatakse koondplaneerimise seadistamiseks.
author: t-benebo
manager: tfehr
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 2f2ec94b8d3bce9ca9fb565fe06b268f5c7458fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005023"
---
# <a name="master-planning-setup-wizard"></a>Koondplaneerimise installiviisard

[!include [banner](../includes/banner.md)]

Selles teemas antakse **Koondplaneerimise installiviisardi** juhiseid. Selles selgitatakse, kuidas parameetrisoovitusi arvutatakse ja esitatakse ka näiteid selle kohta, kuidas erinevad ettevõtted seadistavad koondplaneerimist vastavalt oma ärivajadustele.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

Video [Koondplaneerimise häälestusviisard rakenduses Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) (näha eespool) on lisatud [Finance and Operationsui esitusloendisse](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), mis on saadaval YouTube’is.


## <a name="specific-requirements-of-your-company"></a>Teie ettevõtte erinõuded

Viisardi esimesel leheküljel küsitakse teie ettevõtte erinõuete kohta. Teie vastused nendele küsimustele ei pea olema täpsed, kuid te peaksite esitama juriidilise isiku jaoks ette nähtud üksuste ja plaanitud tellimuste ligikaudset arvu. Teie vastuseid kasutatakse juriidilisele isikule ja mitte ainult valitud koondplaanile rakendatavaid parameetreid. Järgmistes jaotistes kirjeldatakse arvutatavaid parameetreid ja kasutatavaid valemeid.

### <a name="number-of-threads"></a>Lõimede arv

- **Kui toodate mistahes kaupu:** Lõimede arv = plaanitud tellimuste arv ÷ 1000
- **Kui te ei tooda mistahes kaupu:** Lõimede arv = Kaupade arv ÷ 1000

Kui arvutatud lõimede arv ületab 75 protsenti saadaolevatest lõimede arvust, on iga kliendi jaoks saadaolevate lõimede arvu piirmääraks 75%. (Saadaolevate lõimede arv määratakse iga kliendi puhul.)

Lisateabe saamiseks lugege teemat [Lõimede arv](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Kogumi suurus

Kogumi suuruseks määratakse **1**. See väärtus on sageli parim väärtus, kuna see aitab parandada koondplaneerimise jõudlust.

Lisateabe saamiseks lugege teemat [Ülesannete arv abilise ülesannete kogumis](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Kinnituskogumi suurus

- **Kui toodate mistahes kaupu:** Kinnituskogumi suuruseks määratakse suurem neist kahest väärtusest: **10** ja kogumi arvutamine
- **Kui te ei tooda kaupu:** Kinnituskogumi suuruseks määratakse suurem neist kahest väärtusest: **50** ja kogumi arvutamine

Kogumi arvutamine = (plaanitud tellimuste arv × (kinnitusaja piir ÷ laovarude ajapiir) ÷ lõimede arv) ÷ 10

### <a name="cache-size"></a>Vahemälu maht

Vahemälu mahuks määratakse **Maksimaalne**. See väärtus on sageli parim väärtus, kuna see aitab parandada koondplaneerimise jõudlust.

Lisateabe saamiseks lugege teemat [Tööde kogumisse kuuluvatele töödele aja eraldamine](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Tootmise seadistamine

Kaupade tootmisel kuvatakse viisardi hiljem leht **Tootmise seadistamine**.

## <a name="scope-of-the-current-plan"></a>Praeguse plaani ulatus

Viisardi lehel **Praeguse plaani ulatus** vastate küsimustele, mis on seotud sellega, kui kaugele tulevikus erinevaid nõudeid arvestatakse ja arvutatakse koondplaneerimisel. Iga küsimus küsib, kas soovite kasutada funktsiooni ja kuidas soovite seda konfigureerida.

Näiteks eelarveplaani funktsiooni puhul küsib viisard: „Kas soovite kasutada koondplaneerimisel eelarveplaani, et prognoositud nõudluse rahuldamiseks soovitataks plaanitud tellimusi?"

Valikud on järgmised:

- **Ei** – koondplaneerimine ei soovita plaanitud tellimusi eelarve täitmiseks. Lehe **Koondplaanide** (**Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**) vahekaardil **Ajapiir** seadistab viisard valiku **Eelarveplaan (ajapiir)** suvandiks **Jah** ja päevade arvuks **0** (null). See seadistus alistab laovarude grupis määratud ajapiiri. Kuna päevade arvuks on seatud **0** (null), siis seda funktsiooni ei kasutata.
- **Jah, nagu on määratletud selles koondplaanis** – väli muutub kättesaadavaks, kus saate sisestada päevade arvu, mille jooksul koondplaneerimine soovitab plaanitud tellimusi prognoositava nõudluse täitmiseks. Viisard seadistab valiku **Eelarveplaan (ajapiir)** suvandiks **Jah** ja määrab päevade arvuks selle päevade arvu, mis on sisestatud lehe **Koondplaanid** vahekaardi  **Ajapiirid** väljale **Eelarveplaan**. See seadistus alistab laovarude gruppidele määratud väärtused.
- **Jah, nagu on määratletud laovarude puhul** – viisard määrab valiku  **Eelarveplaan (ajapiir)** suvandiks **Ei.** Laovarude grupis määratud ajapiire kasutatakse selleks, et määrata, kui pikaks ajaks te prognoosi planeerite.

Selle lehe ülejäänud küsimused ja nende vastused järgivad sama skeemi.

- **Ei** – suvandi **Eelarveplaan (ajapiir)** väärtuseks seatakse **Jah** ja päevade arvuks seatakse **0** (null).
- **Jah, nagu on määratletud selles koondplaanis** – suvandi **Eelarveplaan (ajapiir)** väärtuseks seatakse **Jah**. Sisestatud päevade arvu kasutatakse ja need alistavad laovarude gruppidele määratud väärtused.
- **Jah, nagu on määratletud laovarude grupi puhul** – suvandi **Eelarveplaan (ajapiir)** väärtuseks seatakse **Ei.**

Lisateabe saamiseks lugege teemat [Tööde plaanimine](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Planeerimissuvandid

Leht **Planeerimissuvandid** kuvatakse ainult siis, kui vastate **Jah** küsimusele "Kas te toodate mistahes plaanitud kaupu?" viisardi esimesel lehel.

Teie vastus esimesele küsimusele sellel lehel („Kas teil on vaja planeerida operatsioone üksikutele töödele?") määratleb lehe **Koondplaanid** vahekaardil **Üldine** planeerimismeetodi.

- **Jah** – kasutatakse tööde planeerimist.
- **Ei** – kasutatakse operatsioonide planeerimist.

Lisateabe saamiseks vt [Operatsioonide plaanimine](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) ja [Tööde plaanimine](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Nõudluse ja pakkumise värskendused

Lehe **Nõudluse ja pakkumise värskendused** küsimused on seotud kinnitamise, tegevusteadete ja viivitustega.

Koondplaneerimise seadistust värskendatakse vastavalt teie vastustele sama skeemi järgi, mida on kirjeldatud eelmises jaotises.

- **Ei**  – lehel **Koondplaanid** seatakse suvandi **Ajapiir** väärtuseks **Jah** ja päevade arvuks seatakse **0** (null).
- **Jah, nagu on määratletud selles koondplaanis** – suvandi **Ajapiir** väärtuseks seatakse **Jah.** Sisestatud päevade arvu kasutatakse ja need alistavad laovarude gruppidele määratud väärtused.
- **Jah, nagu on määratletud laovarude grupis** – suvandi **Ajapiir** väärtuseks seatakse **Ei.**

Arvutatud viivituste korral uuendatakse küsimustele antud vastuste põhjal vastavad parameetrid lehe **Koondplaanid** vahekaardil **Arvutatud viivitused**.

## <a name="summary-of-your-changes"></a>Teie muudatuste kokkuvõte

Viisardi viimasel lehel kuvatakse teie vastuste põhjal soovitatavad muudatused. Seal kuvatakse nii seadistuses (**Praegune seadistus**) olev väärtus kui ka viisardi soovitatud (**Uus konfiguratsioon**) väärtus.

Samuti saate muuta parameetreid uues konfiguratsioonis. Parameetrid eraldatakse parameetritesse, mis rakenduvad teie juriidilisele isikule ja parameetritele, mis rakenduvad ainult teie valitud koondplaanile. Kõigi seadistusparameetrite vaatamiseks, mida saab viisardi abil muuta, valige lehe allosas **Kuva kõik parameetrid**. Seejärel saate parameetreid muuta.

Lõpuks, kui valite **Valmis**, rakendatakse uus konfiguratsioon. Kui valite **Loobu**, ei rakendata ühtegi muudatust.

## <a name="examples"></a>Näited

Selles jaotises kirjeldatakse kahe väljamõeldud ettevõtte seadistust, et näidata, kuidas seadistus võib iga ettevõtte vajadustest lähtuvalt muutuda.

### <a name="example-1-contoso-manufacturer"></a>Näide 1: Contoso Manufacturer

Contoso Manufacturer on kõlareid tootev ettevõte. See ostab erinevatelt tarnijatelt erinevaid tooraineid ja osi, mida kasutatakse lõplike kõlarite jaoks. Siin on mõned ettevõtte+ tarnete ja tootmise omadused.

- Ettevõtte toodetavatel lõpptoodetel on koosluse struktuur.
- Kõik lõplikud kaubad ja komponendid planeeritakse koondplaneerimisel. Käsitsi planeerimist ei tehta.
- Operatsioonide protsess määratletakse iga lõpliku toote tootmiseks.
- Tootmistehas toodab lõpp-kaupu. Seal on määratletud arv freesimis- ja puurimisseadmeid, mida kasutatakse komponentide töötlemiseks. Need seadmed peavad töötlema erinevaid osi.
- Tarnijaid on palju. Kaupade keskmine täitmisaeg on üks nädal. Sama tarnija kaupade grupil on seitsmenädalane täitmisaeg.

Viisardis sisestatakse Contoso tootja jaoks järgmised väärtused.

- **Laovarud**

    - **Küsimus:** „Kas soovite määrata oma plaaniperioodi päevade arvu?"
    - **Vastus:** „Jah, nagu on määratletud laovarude gruppides."

    Kuna kaupade täitmisaeg on väga erinev, ei pea Contoso tulevikus kõiki sama perioodi kaupu planeerima. Luuakse kaupade laovarude grupid. Sarnase täitmisajaga kaubad määratakse samasse laovarude gruppi. Iga laovarude grupi plaaniperiood (st laovarude ajapiir) on umbes täitmisaeg pluss ühe nädala marginaal. Koondplaneerimine tagab seejärel, et kaubad plaanitakse eelnevalt, lähtudes nende täitmisajast.

    Seetõttu luuakse selle näite jaoks kaks laovarude gruppi. Ühel laovarude grupil on laovarude ajapiiriks kaks nädalat ja teise grupil on see kaheksa nädalat.

    Kui vastuseks on valitud **Jah, nagu on määratletud koondplaanis**, peab sisestatud päevad arv ületama kõigi kaupade pikima täitmisaja. Kuid kuna paljusid kaupu ei pea nii pikalt ette plaanima, siis paljud plaanitud tellimused arvutatakse, kuid neid ei kasutata kunagi. Seetõttu pikeneb koondplaneerimise käitusaeg.

- **Plaanimine**

    - **Küsimus:** „Kas teil on vaja plaanida üksikuteks töödeks jagatud operatsioone?"
    - **Vastus:** „Jah.”

    Contoso tootmine peab tööde juhtimise käigus plaanima üksikuid töid. Seetõttu kasutatakse tööde plaanimist.

- **Võimsus**

    - **Küsimus:** „Kas soovite plaanida ressursivõimsuse abil?"
    - **Vastus:** „Jah, nagu on määratletud selles koondplaanis.” Sisestatakse **10 päeva**.

    Freesimis- ja puurimisseadmete arv on piiratud. Tootmisplaneerimine peab seda piirangut arvestama ja korraldama töökohad õigeaegselt vastavalt ressursivõimsusele. Teisisõnu, plaanitud tööd kavandatakse ümber ressursside piirangute alusel. Planeerimisel kasutatakse lisaks määratletud perioodile ka täitmisaega. (Plaanitud tootmistellimused võivad kattuda.) Kuna kaupade tootmise täitmisaeg on seitse päeva, kaalutakse koondplaneerimise ressursside võimsust 10 päeva jooksul.

- **Järjestus**

    - **Küsimus:** „Kas soovite järjestada plaanitud tellimusi toote jadaväärtusi kasutades?"
    - **Vastus:** „Jah, nagu on määratletud laovarude gruppides."

    Iga lõpliku kauba tootmiseks on määratletud protsess. Seetõttu plaanib koondplaneerimine tellimused õigeaegselt vastavalt määratletud protsessidele.

- **Koosnemine**

    - **Küsimus:** „Kas soovite planeerida tellimused kõigi koosluse elementide jaoks (emaettevõtte ja kõigi tütarettevõtete kaupade plaan)?"
    - **Vastus:** „Jah, nagu on määratletud laovarude gruppides."

    Kõik tootmises kasutatavad kaubad tuleb planeerida. Kuna kaupadel on väga erinevad täitmisajad, on koondplaneerimisel laovarude gruppide kasutamisel paremad tulemused. Jällegi saab sisestada ühe nädala marginaali ja koosnemist saab teha samal ajal laovarude plaanimisega.

### <a name="example-2-contoso-retailer"></a>Näide 2: Contoso Retailer

Contoso Retailer on moetööstuse turustusettevõte. See kasutab koondplaneerimist, et arvutada, millal tuleks ostutellimused esitada, tuginedes oma prognoositavale müügile. Siin on mõned selle omadused.

- Contoso Retailer kasutab müügi prognoosimiseks nõudluse prognoosi. Ostutellimused planeeritakse vastavalt prognoosidele.
- Kauplused kasutavad täiendamise jaoks ostutaotlusi.
- Täitmisaeg põhilaost igasse poodi on kõigi kaupade puhul ligikaudu kaks nädalat.

Viisardis sisestatakse Contoso Retaileri jaoks järgmised väärtused.

- **Nõudluse prognoos**

    - **Küsimus:** "Kas soovite kasutada koondplaneerimisel eelarveplaani, et prognoositud nõudluse rahuldamiseks soovitataks plaanitud tellimusi?"
    - **Vastus:** „Jah, nagu on määratletud selles koondplaanis.”

    Contoso on oma müügi prognoosimiseks lisanud nõudluse prognoosi. Seetõttu peab koondplaneerimine prognoosi täitmiseks soovitama plaanitud tellimusi.

- **Kinnitamine**

    - **Küsimus:** „Kas soovite, et koondplaneerimine kinnitaks plaanitud tellimused tellimusdokumentideks, näiteks tootmis-või ostutellimusteks?"
    - **Vastus:** „Jah, nagu on määratletud selles koondplaanis.” Sisestatakse **1 päev**.

    Kuna Contoso Retailer loob ostutellimused otse plaanitud ostutellimustest, on kasulik, kui plaanitud ostutellimused kinnitatakse automaatselt. Kuna ettevõte kasutab iga päev koondplaneerimist, kinnitab ühe päeva kinnitamise ajapiir automaatselt kõik järgmiseks päevaks nõutavad tellimused.

- **Kinnitatud taotlused**

    - **Küsimus:** „Kas soovite kaasata jaekaupluste täiendamiseks kinnitatud taotlusi?"
    - **Vastus:** „Jah, nagu on määratletud selles koondplaanis.” Sisestatakse **1 päev**.

    Contoso kasutab oma kauplustes kinnitatud ostutaotlusi, et luua nende poodide täiendamiseks plaanitud ostutellimused. Kuna koondplaneerimist kasutatakse iga päev, kaasatakse planeerimisse viimase päeva ostutaotlused.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]