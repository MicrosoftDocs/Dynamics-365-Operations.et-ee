---
title: Hankija tagasimaksed
description: Selles teemas antakse ülevaade kõige levinumatest ülesannetest, mida on vaja teha hankija tagasimaksetega töötamisel. Hankija tagasimaksed aitavad ettevõtetel tarnijate tagasimakseprogramme paremini hallata, automatiseerides toiminguid, mis on vajalikud teenitud tagasimaksete haldamiseks, jälgimiseks ja nõudmiseks.
author: omulvad
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.openlocfilehash: e56bf86a11eb34679269eae5ca093d7cc379932b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822463"
---
# <a name="vendor-rebates"></a>Hankija tagasimaksed

[!include [banner](../includes/banner.md)]

Hankija tagasimaksed aitavad ettevõtetel tarnijate tagasimakseprogramme paremini hallata, automatiseerides toiminguid, mis on vajalikud teenitud tagasimaksete haldamiseks, jälgimiseks ja nõudmiseks.

Selles teemas antakse ülevaade kõige levinumatest ülesannetest, mida on vaja teha hankija tagasimaksetega töötamisel. Ülevaade hõlmab järgmisi ülesandeid.

- Tagasimakselepingu üksikasjade ülevaatamine.
- Tagasimaksetele kvalifitseeruvate tellimuste tuvastamine ja tagasimaksenõuete koostamine.
- Nõuete ülevaatamine ja kinnitamine.

## <a name="audience-and-purpose"></a>Sihtgrupp ja eesmärk

Selles teemas sisalduv teave on mõeldud ettevõtete äriotsuste tegijatele (ametikohad nagu ostujuht, finantsjuht ja pearaamatupidaja), kellel on järgmised ülesanded.

- Läbirääkimiste pidamine hankijate hindade, allahindluste ja tagasimakselepingute teemal.
- Tagasimaksenõuete töötlemise ja maksete sissenõudmisega tegelevate töötajate juhtimine.
- Varude tellimine võimalikult heade hindadega.

Nendel ametikohtadel töötavad inimesed otsivad võimalusi mitmesuguste eesmärkide saavutamiseks. Järgmisena on toodud mõned näited.

- Mitmesuguste hankijate kampaaniaprogrammide ja tagasimaksetingimuste paindlik arvestamine.
- Halduskoormuse ja vigade arvu vähendamine seoses kampaaniatulemuste jälgimise ja nõuete töötlemisega.
- Rahavooprognooside parandamine tulevaste debitoorsete võlgnevuste koondamisega.
- Kvantifitseeritud aluse omamine jooksvate ja tulevaste läbirääkimiste jaoks hankijatega tagasimaksete teemal.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>Hankija tagasimakselepingu üksikasjade ülevaatamine

Hankija tagasimakseleping on registreeritud kokkulepe hankijaga, mis täpsustab läbi räägitud tingimused, mille alusel ettevõte kvalifitseerub rahalisele tasule eelnevalt määratud ostueesmärkide saavutamise eest. Hankija tagasimakselepingud registreeritakse lehel **Tagasimakselepingud**.

Lehe **Hankija tagasimakselepingud** avamiseks valige **Hanked** &gt; **Hankija tagasimaksed** &gt; **Tagasimakselepingud**.

![Ostuleping](media/purchase-agreement.PNG)

Lehel **Hankija tagasimakselepingud** saate vaadata hankija lepingu läbiräägitud tingimuste üksikasju.

Lepingu päises on täpsustatud üldtingimused, mille alusel ettevõte tagasimakse saamiseks kvalifitseerub. Päise teave määrab, et hankija teeb tagasimakse, kui teatud toodet ostetakse teatud koguses. Päises määratakse ka tagasimakse mõõtühiku suvand ja arvutuse kuupäeva tüüp.

- Kui vahekaardil **Ülevaade** on suvandiga **Kaubakood** ridade väärtuseks seatud *tabel*, et kaupa täpsustada, siis on lepe selle konkreetse kauba jaoks. Kui suvandiga **Kaubakood** ridade väärtuseks on seatud *Grupp* või *Kõik*, et kaupu täpsustada, siis töödeldakse hankija tagasimakselepingut ühe kaubakoodile vastava kauba haaval, mitte kõigi kaubakoodile vastavate kaupade põhjal.

- Vahekaardil **Üldine** väljal **Tagasimakse mõõtühiku suvand** saate määrata, kas mõõtühik peaks olema tingimus, mille alusel ostutellimuse rida kvalifitseeruks tagasimaksenõudele.

    - **Teisenda** – ostutellimuse rida kvalifitseerub tagasimakse lepingu kohaselt hankija tagasimaksele. Saate tagasimakse olenemata real rakendatud mõõtühikust.
    - **Täpne vaste** – tagasimaksele kvalifitseerumiseks peab ostureal olema sama mõõtühik, mis on lepingus määratud.

- Valige vahekaardil **Üldine** väljalt **Arvutuskuupäeva tüüp** kuupäev, mida kasutatakse määramiseks, kas ost toimub tagasimakselepingu kehtivusperioodil.

    - **Loodud** – kasutage ostutellimuse loomise kuupäeva.
    - **Nõutav tarne** – kasutage nõutavat tarnekuupäeva.

Lepinguridadel saate määrata hankija tagasimakselepingu üksikasjalikumalt.

- Väljal **Ostude koondamisalus** saate määrata tagasimaksenõude arvutuse. Summa saab määrata sõltuma perioodist (nädal, kuu, aasta, kasutusiga või kohandatud periood). Väärtus **Arve** näitab, et tagasimaksenõue määratakse iga kord, kui ostutellimuse rea eest arve esitatakse.
- Väljal **Võetud:** saate määrata tagasimakse arvutuse aluse.

    - **Bruto** – tagasimakse arvutatakse kauba brutohinna põhjal.
    - **Neto** – tagasimakse arvutatakse kauba netohinna põhjal (st hind pärast muude allahindluste rakendamist).

- Väljadel **Tagasimakseprogrammi juurdekasvukonto** ja **Tagasimakseprogrammi kulukonto** on määratud kontonumbrid, mis saavad kinnitamise ja töötlemise vaheetapi jooksul kogunenud tagasimaksesummad.
- Kui valiku **Kinnitus nõutud** väärtuseks on määratud **Jah**, tuleb tagasimaksenõue kinnitada, enne kui seda saab koguda või välja maksta.
- Väli **Tagasimakserea katkestuse tüüp** näitab tagasimaksete alust.

    - **Kogus** – tagasimaksed on mahupõhised.
    - **Summa** – tagasimaksed on summapõhised.

- Kiirkaardil **Read** näete, kuidas erinevaid kogusejärkusid saab seadistada erinevate tagasimaksete andmiseks. Näiteks näitavad väljad **Väärtusest** ja **Väärtuseni**, et toote kogus vahemikus 10–19 ühikut kvalifitseerub tagasimaksele 15 dollarit ühiku kohta.

    > [!NOTE]
    > Väärtus **Alates väärtusest** on kaasav, samas kui väärtus **Kuni väärtuseni** on välistav. Näiteks on väljale **Tagasimakse reapiiri tüüp** määratud väärtus **Kogus** ja sisestate numbri **1** väljale **Alates väärtusest** ning numbri **3** väljale **Kuni väärtuseni**. Sellisel juhul rakendub tagasimakse summa, kui ostate ühe või kaks kaupa, kuid mitte siis, kui ostate kolm kaupa.

- Väljal **Töövoo kinnituse olek** näitab väärtus **Kinnitatud**, et lepingut saab rakendada lepingu tingimustele vastavatele ostutellimustele.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>Tagasimaksetele kvalifitseeruvate tellimuste tuvastamine ja tagasimaksenõuete koostamine

Kui esitatakse ostutellimusi hankijale, kellega ettevõttel on tagasimakseleping, tuvastab programm tulevased hankija kreeditmaksed. Kui ostutellimused kvalifitseeruvad tagasimaksele, koostatakse igale tellimuse reale tagasimaksenõue kohe, kui ostuarve on sisestatud. See on automaatne protsess. Hiljem saate oodatavaid tagasimakseid üle vaadata ja näha, millist mõju need tagasimaksed toote maksumusele ja kasumimarginaalile avaldavad.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Hankija tagasimakselepingu alusel ostutellimuse reale rakendatavate allahindluste üksikasjade vaatamine

1. Valige lehelt **Ostutellimus** tellimuse rida ja valige siis **Ostutellimuse rida** &gt; **Kuva** &gt; **Hinna üksikasjad**.
2. Valige lehelt **Hinna üksikasjad** kiirkaart **Tagasimaksed**.

Tagasimakse teave kuvatakse ka väljal **Hankija tagasimakse** lehe **Hinna üksikasjad** jaotises **Eeldatav marginaal**.

> [!NOTE]
> Veenduge, et lehel **Hangete parameetrid** vahekaardil **Hinnad** oleks suvandi **Hinna üksikasjade lubamine** väärtuseks määratud **Jah**. Kui suvandi väärtuseks on määratud **Ei**, ei saa tagasimakseid vaadata.

## <a name="review-and-approve-claims"></a>Nõuete ülevaatamine ja kinnitamine

Loodud tagasimaksenõuded tähistavad hankijalt oodatavaid tulevasi makseid. Enne kreeditarve väljastamist hankijale soovib lepingu omanik tavaliselt nõuded üle vaadata ja need kinnitada. Kuid pange tähele, et nõude olek määrab, kas nõue on valmis kinnitusprotsessi läbima.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>Nõuete olek ja mõju kinnitusprotsessile

Nõude olekuks määratakse selle loomisel **Arvutamisele kuuluv väärtus**, kui tagasimakse tehakse kumulatiivsel alusel, või **Arvutatud**, kui tagasimakse antakse arvepõhiselt. Kui nõude olek on **Arvutamisele kuuluv väärtus**, peab see läbima arvutusprotsessi, millega tegeleb funktsioon Kumuleeri. Kinnitusprotsessi saab lisada ainult nõuded, mille olek on **Arvutatud**.

> [!NOTE]
> Kui hankija tagasimakselepingu suvandi **Kinnitus nõutud** väärtuseks on määratud **Ei**, on kõigi loodavate nõuete olek **Kinnitatud**. Kinnitamine on kumulatiivsel alusel antavate nõuete puhul kohustuslik.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Nõuete kinnitamine ning sisestuste ja arve üksikasjade vaatamine

Kui nõuded on kinnitatud, saab neid töödelda ostureskontro. Krediiditeatis (hankijaarve) koostatakse tagasimaksenõude summale automaatselt. Siis saab krediidi hankija saldole lisada ja ostureskontro töörühm saab selle tavapärasesse tasakaalustusprotsessi lisada.

1. Valige tagasimaksenõude avamiseks **Hanked** &gt; **Hankija tagasimaksed** &gt; **Tagasimaksenõuded**.
2. Sulgege tagasimaksenõue.
3. Märkige nõue ja valige siis tegumiribalt **Kinnita**.
4. Valige taotluse lehel väljalt **Hankija** hankija, kellelt teil on õigus tagasimakset saada, ja valige siis **OK**.

    Nõude summa kohta sisestatakse tagasimakse juurdekasvu tööleht. See sisestus debiteerib kogunenud tasumisele kuuluvate hankija tagasimaksete kontolt oodatava hankija kreeditsumma ja krediteerib saadud kogunenud hankija tagasimaksete vahekontot oodatud tuluga.

    ![Teade](media/message.png)

5. Valige tagasimaksete loendist rida ja valige siis tegumiribalt **Tagasimaksekanded**, et vaadata selle tagasimakse kogunenud sisestuse töölehe partiinumbrit ja liikuda selle juurde.

    Nõuete teisaldamiseks tavapärasesse ostureskontro protsessi peab ostureskontro ametnik nüüd tagasimaksenõude täitma, käivitades funktsiooni Töötlus.

6. Valige tegumiribalt **Töötlus** ja valige siis **Filtreeri**. Valige välja **Hankija konto** väljal **Kriteerium** hankija, kelle tagasimaksenõudeid töödelda, valige teised asjakohased filtrid ja valige siis **OK**.

    Teateribad ja asjaolu, et olek on muudetud olekuks **Lõpule viidud** näitavad, et toimunud on järgmine.

    - Tagasimakse juurdekasvu töölehe sisestamine on tühistanud eelmised vahesummad kogunenud tulu- ja kulukontodel.
    - Hankija arve (kreeditarve) tagasimakse summale on loodud.

        > [!NOTE]
        > Suvandi **Käsitsi arve sisestamine** lehe **Hankeparameetrid** vahekaardil **Tagasimakseprogramm** määratleb, kas hankija arve sisestatakse nõude töötlemisel käsitsi või automaatselt.

    - Kui hankija arve on (automaatselt või käsitsi) sisestatud, on hankija tasumisele kuuluvate summade kontot debiteeritud ja saadud allahindluste ja hüvitiste kontot krediteeritud.

        > [!NOTE] 
        > Saadud allahindluste ja hüvitiste konto number määratakse hankekategooriale, mida selle allahindluse puhul ostuarve real kasutatakse. Hankekategooria omakorda määratakse lehe **Hankeparameetrid** vahekaardil **Tagasimakseprogramm**.

7. Valige tagasimaksete loendist rida ja valige siis tegumiribalt **Tagasimaksekanded**, et vaadata selle tagasimakse kogunenud sisestuse töölehe partiinumbrit ning samuti hankija arve numbrit ja liikuda nende juurde.
8. Valige hankija arve kande rida ja valige siis tegumiribalt **Hankija arve**. Kui hankija arve on sisestatud, näete arve töölehte. Vastasel korral näete hankija arvet ootel hankija arvena, mis nõuab käsitsi sisestamist.

    Arve rida määrab hankija arve üksikasjad hankekategooria **Komisjonitasud ja tagasimaksed** puhul.

9. Valige lehelt **Kõik hankijad** hankija, kellelt tagasimakse saate, ja valige siis tegumiribalt **Kanded**. Leidke arve rida. Tagasimakse summa on nüüd lisatud hankija saldole.

## <a name="summary"></a>Kokkuvõte

Hankija tagasimaksete käsitsemise protsess hõlmab mitmeid sageli tüütuid käsitsi jälgimise ülesandeid. Nende ülesannete automatiseerimisel saab hankija tagasimakse haldamise funktsioon aidata teil järgmiste protsesside vahel liikuda.

- Täpsete tagasimaksenõuete loomine
- Eeldatava tulu ja vahekasumi koondamine pearaamatus
- Hankija saldo ja kasumiaruande värskendamine tasumisele kuuluva hüvitisega


[!INCLUDE[footer-include](../../includes/footer-banner.md)]