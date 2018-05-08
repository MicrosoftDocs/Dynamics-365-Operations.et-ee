---
title: Kontsernisisene arveldamine
description: "Selles artiklis on teave ja näited projektide kontsernisisese arveldamise kohta Microsoft Dynamics 365 for Finance and Operationsis."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3d4354316d0c37c6556c0ec3d27a3c62c5afb7b0
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="intercompany-invoicing"></a>Kontsernisisene arveldamine

[!include [banner](../includes/banner.md)]

Selles artiklis on teave ja näited projektide kontsernisisese arveldamise kohta Microsoft Dynamics 365 for Finance and Operationsis.

Teie organisatsioonil võib olla mitu allüksust, tütarettevõtet ja muud juriidilist isikut, mis edastavad üksteisele projektide tarbeks tooteid ja teenuseid. Juriidilist isikut, kes teenust või toodet pakub *, nimetatakse laenu väljastavaks juriidiliseks isikuks* ja teenust või toodet vastuvõtvat juriidilist isikut *laenavaks juriidiliseks isikuks*. 

Järgmisel joonisel on kujutatud tüüpilist stsenaariumi, kus kaks juriidilist isikut SI FR (laenav juriidiline isik) ja SI USA (laenu väljastav juriidiline isik) jagavad ressursse projekti läbiviimiseks kliendile A. Selle stsenaariumi puhul on peatöövõtja SI FR, kes peab töö kliendile A üle andma. 

[![Kontsernisisese arveldamise näide](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Eesmärk on muuta kulude juhtimine, tulude kajastamine, maksud ja sisehind kontsernisiseste projektikannete puhul paindlikumaks ja võimsamaks. Lisaks pakutakse järgmisi võimalusi.

-   Kliendiarvete koostamine projekti suhtes laenavas juriidilises isikus, kasutades kontsernisiseseid ajatabelid, kulusid ja hankija arveid laenu väljastavas juriidilises isikus.
-   Maksuarvutuste ja kaudsete kulude toetus.
-   Tulu näitamise edasilükkamine laenu väljastavas juriidilises isikus ja laenava juriidilise isiku poolsel tulu näitamisel.
-   Lõpetamata toodangu (WIP) tulu kogumine laenu väljastavasse juriidilisse isikusse.
-   Üleviimishindade määramine mitmesuguste hinnamudelite põhjal. Järgmisena on toodud mõned näited.
    -   **Kogus** – summa, mis sisestatakse väljale **Hinnakujundus**, on tegelik kulu koguse või ühiku kohta.
    -   **Kulude summa** – hind/kulu kande kohta pluss kulusumma, mille sisestate väljale **Hinnakujundus**.
    -   **Kulude protsent** – üleviimishind on hind/kulu kande kohta, mis on korrutatud väljale **Hinnakujundus** sisestatud tasuprotsendiga.
    -   **Müügihinna protsent** – protsent müügihinnast, mis edastatakse laenu väljastavale juriidilisele isikule.
    -   **Summa alla müügihinna** – summa, mille laenav juriidiline isik peab müügihindadest kinni enne ülekannet laenu väljastavale juriidilisele isikule.
    -   **Kasumimäär** – arv, mille sisestate väljale **Hinnakujundus**, on kasumimäär, mis on väljendatud protsendina müügihinnast.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>1. näide: kontsernisisese arveldamise parameetrite seadistamine
Selles näites on USSI laenu väljastav juriidiline isik ja tema ressursid registreerivad aega laenava juriidilise isiku FRSI suhtes, kellel on sõlmitud leping lõppkliendiga. USSI töötajate registreeritavad tunnid ja kulud saab lisada FRSI koostatavale projektiarvele. Lisaks on olemas kolmas kannete allikas, mis võib pärineda laenavast juriidilisest isikust (selles näites USSI), kui see osutab allüksustele (nt FRSI) jagatud hankijate teenuseid ja edastab need kulud siis projektidele nendes allüksustes. Kõik vastavad arvedokumendid ja maksuarvutused teeb Finance and Operations. 

Selles näites peab FRSI olema USSI juriidilises isikus klient ja USSI peab olema FRSI juriidilises isikus hankija. Seejärel saate seadistada kahe juriidilise isiku vahelise kontsernisisese seose. Järgmine protseduur näitab, kuidas seadistada parameetreid, nii et mõlemad juriidilised isikud saaksid kontsernisiseses arvelduses osaleda.

1. Seadistage FRSI kliendina USSI juriidilises isikus ja USSI hankijana FRSI juriidilises isikus. Selle ülesande jaoks vajalike toimingute puhul on kolm sisestuspunkti.

   | Etapp |                                                       Sisestuspunkt                                                        |                                                                                                                                                                                               Kirjeldus                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Klõpsake USSI all valikuid <strong>Müügireskontro</strong> &gt; <strong>Kliendid</strong> &gt; <strong>Kõik kliendid</strong>. |                                                                                                                                                                  Looge FRSI-le uus kliendikirje ja valige kliendigrupp.                                                                                                                                                                  |
   |  B   |    Klõpsake FRSI all valikuid <strong>Ostureskontro</strong> &gt; <strong>Hankijad</strong> &gt; <strong>Kõik hankijad</strong>.     |                                                                                                                                                                    Looge USSI-le uus hankija kirje ja valige hankijagrupp.                                                                                                                                                                    |
   |  C   |                                  Avage FRSI all äsja loodud hankija kirje.                                  | Klõpsake tegumiriba vahekaardil <strong>Üldine</strong> grupis <strong>Seadistus</strong> valikut <strong>Kontsernisisene</strong>. Määrake lehe <strong>Kontsernisisene</strong> vahekaardil <strong>Kaubandussuhe</strong> liuguri <strong>Aktiivne</strong> väärtuseks <strong>Jah</strong>. Valige väljalt <strong>Kliendi ettevõte</strong> kliendi kirje, mille lõite etapis A. |


2. Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Seadistus** &gt; **Projektihalduse ja raamatupidamise parameetrid** ja seejärel vahekaarti **Kontsernisisene**. See, kuidas parameetrid seadistate, sõltub sellest, kas olete laenav või laenu väljastav juriidiline isik.
   -   Kui olete laenav juriidiline isik, siis valige hankekategooria, mida tuleks kasutada automaatselt loodavate hankija arvete vastendamisel.
   -   Kui olete laenu väljastav juriidiline isik, siis valige iga laenava üksuse puhul igale kandele projekti vaikekategooria. Projektikategooriaid kasutatakse maksude konfigureerimiseks, kui kontsernisiseste kannete arveldatud kategooria on olemas ainult laenavas juriidilises isikus. Saate valida kontsernisiseste kannete puhul kulude juurdekasvu. See juurdekasv tekib kannete sisestamisel ja see tühistatakse kontsernisisese arve sisestamisel.

3. Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Seadistus** &gt; **Hinnad** &gt; **Ülekande hind**.
4. Valige valuuta, kande tüüp ja ülekande hinnamudel. Arvel kasutatav valuuta on valuuta, mis on konfigureeritud laenu väljastava juriidilise isiku all laenava juriidilise isiku kliendikirjes. Valuutat kasutatakse üleviimise hinnatabeli kirjete vastendamiseks.
5. Klõpsake valikuid **Pearaamat** &gt; **Sisestamise seadistus** &gt; **Kontsernisisene raamatupidamine** ja seadistage USSI ja FRSI seos.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2. näide: kontsernisisese ajatabeli loomine ja sisestamine
USSI, laenu väljastav juriidiline isik, peab looma ja sisestama ajatabeli FRSI (laenava juriidilise isiku) projektile. Selle ülesande jaoks vajalike toimingute puhul on kaks sisestuspunkti.

| Etapp | Sisestuspunkt                                                                       | Kirjeldus                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektihaldus ja raamatupidamine** &gt; **Ajatabelid** &gt; **Kõik ajatabelid** | Looge uus ajatabel. Tehke ajatabeli rea väljal **Juriidiline isik** valik **FRSI**. Valige väljal **Projekti ID** FRSI alt projekt. Sisestage iga nädalapäeva tundide arv. |
| B    | Leht **Ajatabel**                                                                | Pärast töövoo aktiveerimist postitage ajatabel ja märkige üles kandenumber.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3. näide: kontsernisisese hankija arve loomine ja sisestamine
USSI, laenu väljastav juriidiline isik, peab looma ja sisestama kontsernisisese hankija arve FRSI (laenava juriidilise isiku) projektile. See hankija arve kajastab sisse ostetud tööjõudu ja kulu, mis kaasnes USSI palgatud hankijate tööga. Selle ülesande jaoks vajalike toimingute puhul on kaks sisestuspunkti.

| Etapp | Sisestuspunkt                                                                                      | Kirjeldus                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Ostureskontro** &gt; **Arved** &gt; **Ava hankija arved** &gt; **Uus hankija arve** | Looge uus hankija arve ja sisestage teenused, mis FRSI projekti nimel hangiti.                                                                                                                                                                                  |
| B    | Leht **Hankija arve**                                                                      | Sisestage read, mis kajastavad FRSI nimel sisse ostetud teenuseid. Sisestage kiirkaardil **Rea üksikasjad** vahekaardil **Projekt** arve reale väljal **Projekti ettevõte** väärtus **FRSI**. Sisestage projekt ja vastav teave. Seejärel sisestage hankija arve. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4. näide: kontsernisisese arve loomine ja sisestamine
USSI, laenu väljastav juriidiline isik, peab koostama ja sisestama kontsernisisese arve. Selle ülesande jaoks vajalike toimingute puhul on kaks sisestuspunkti.

| Etapp | Sisestuspunkt                                                                                             | Kirjeldus                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektihaldus ja raamatupidamine** &gt; **Projektiarved** &gt; **Kontsernisisene kliendiarve**  | Klõpsake valikut **Uus** lehe **Kontsernisisese arve loomine** avamiseks.                                                                                  |
| B    | **Projektihaldus ja raamatupidamine** &gt; **Projektiarved** &gt; **Kontsernisisesed kliendiarved** | Sisestage lehele **Kontsernisisese arve loomine** juriidiline isik, määrake kanne, mis peaks olema lisatud, ja klõpsake siis käsku **Otsi**. |
| C    | **Projektihaldus ja raamatupidamine** &gt; **Projektiarved** &gt; **Kontsernisisesed kliendiarved** | Valige arveldatavad kanded või klõpsake nuppu **Vali kõik** kõigi loendis olevate kannete arveldamiseks ja klõpsake siis nuppu **OK**.                  |
| D    | Leht **Kontsernisisene arve**                                                                       | Kuvatakse kontsernisisene kliendiarve soovitus.                                                                                             |
| E    | Leht **Kontsernisisene arve**                                                                       | Klõpsake käsku **Sisesta**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5. näide: hankija arve sisestamine ja kliendile arve esitamine
Kui laenu väljastav juriidiline isik USSI sisestab kontsernisisese kliendiarve, luuakse laenava juriidilise isiku FRSI all vastav ootel olev hankija arve. Pärast selle hankija arve sisestamist esitab FRSI projekti kliendile ka arve USSI sisestatud tundide eest. Selle ülesande jaoks vajalike toimingute puhul on kolm sisestuspunkti.

| Etapp | Sisestuspunkt                                                                                        | Kirjeldus                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Ostureskontro** &gt; **Arved** &gt; **Ootel hankija arved**                            | Vaadake arve üle, veendumaks, et ajatabeli väärtused on lisatud, ja sisestage siis hankija arve.                  |
| B    | **Projektihaldus ja raamatupidamine** &gt; **Projekti arved** &gt; **Projekti arvesoovitused** | Looge projektile uus projektiarve ja veenduge, et sisestatud tunnikanded kuvatakse.            |
| C    | Leht **Projekti arve**                                                                       | Valige projekti arve ja klõpsake siis  **Kuva üksikasjad** kulude ja müügisumma ülevaatamiseks. Seejärel sisestage arve. |


Lisateabe saamiseks vt [Ettevõtetevahelise projekti arvete konfigureerimine](tasks/configure-intercompany-project-invoicing.md).



