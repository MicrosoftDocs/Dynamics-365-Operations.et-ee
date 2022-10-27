---
title: Automatiseeri pearaamatu tasakaalustused
description: See artikkel annab teavet pearaamatu tasakaalustuste automatiseerimise protsessi kohta.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9707759"
---
# <a name="automate-ledger-settlements"></a>Automatiseeri pearaamatu tasakaalustused

[!include [banner](../includes/banner.md)]

Finantside Microsoft Dynamics automatiseerimise protsessi funktsioon 365 10.0.31 **on funktsioonihalduse** **tööruumis**  saadaval. Saate lubada automaatse pearaamatu **tasakaalustuste protsessi funktsiooni** ainult siis, kui pearaamatu **tasakaalustuse ja aasta lõpu sulgemise funktsiooni** vaheline teadmine on lubatud.

Pearaamatu tasakaalustamine on deebet- ja kreeditkannete vastavusseviimise protsess pearaamatus. Organisatsioonid, mis teevad pearaamatu tasakaalustamistoiminguid korduvas graafikus, saavad nüüd protsessi automatiseerida. Automaatse pearaamatu tasakaalustusprotsessi ajal saab deebet- ja kreeditkande automaatselt vastendada ainult siis, kui nende summad arvestusvaluutas on võrdsed.Näiteks saab kogusumma deebetsummat $1.00 automaatselt vastendada kogusumma kreeditsummaga $1.00. Ent deebetiväärtust, mis on $1.00, ei saa automaatselt vastendada kahe krediidiga, millest igaüks on $0.50. Pearaamatukande summade osalist vastendamist ei toetata.

Pearaamatu tasakaalustuse automatiseerimine määratleb järgmised üksikasjad:

- Kui pearaamatu tasakaalustused on käitatud
- Milliseid kriteeriumeid kasutatakse deebetide ja kreeditide vastendamiseks, mida saab automaatselt tasakaalustada
- Millist tellimust pearaamatu tasakaalustuse teavet töödeldakse?

## <a name="define-the-occurrence-of-ledger-settlements"></a>Pearaamatu tasakaalustuste esinemiskordade määratlemine

Pearaamatu tasakaalustuse automatiseerimine kasutab protsessi automatiseerimise raamistikku. Erinevad äriprotsessid kasutavad seda raamistikku valitud protsessi kordumise määratlemiseks. Pearaamatu tasakaalustuste puhul minge Süsteemihalduse  **seadistusprotsessi \> automatiseerimise \> või** Pearaamatu pearaamatu **seadistusprotsessi \> automatiseerimised \>**.

Kõigepealt valige suvand **Loo uus protsessi automatiseerimine** ja valige pearaamatu **tasakaalustused**. Seejärel juhendab viisard teid automatiseerimisprotsessi seadistamisel.

## <a name="general-page"></a>Üldine lehekülg

 **Sisestage** viisardi üldisele lehele selle pearaamatu tasakaalustuse esinemiskorra nimi, mida loote. Näiteks kui teie vastendatud deebetid ja kreeditid on esmaspäeval pearaamatuga tasakaalustatud, sisestage kirjeldav nimi, nagu **LedgerSettle\_ Esmaspäev**. Sisestatav nimi kuvatakse pearaamatu tasakaalustuste **lehe** automatiseerimisreegli **veerus** .

Ülejäänud sätted on üldsätted ja määratlevad selle pearaamatu tasakaalustuste versiooni esinemismustri. Näiteks, kui esinemine on esmaspäev, saate selle määrata nii, et see käivitub kord nädalas, ja te saate valida nädalapäevaks selle käitamisel esmaspäeva. Samuti saate sisestada varase graafikuaja, nt 02:00, et protsessi automatiseerimine viidaks lõpule enne järgmise tööpäeva algust. Soovitame planeerida protsessi automatiseerimise nii, et seda tehtaks väljaspool teie tavalist tööaega. Sel viisil saate vähendada raamatupidamispersonali mõju tööpäeva jooksul.

Lisateavet teiste väljade kohta lehel **Üldine** , vt protsessi automatiseerimise dokumentatsioonist.

## <a name="ledger-settlements-match-criteria-page"></a>Pearaamatu tasakaalustuste vastendamise kriteeriumileht

Viisardi järgmine lehekülg on pearaamatu tasakaalustuste **vastendamise kriteeriumileht** . Seda kasutatakse protsessi automatiseerimise esinemiskorda kaasatud põhikontode määratlemiseks ja vastavate deebetide ja kreeditide määramiseks kasutatavate kriteeriumide määratlemiseks.

### <a name="account-selection"></a>Konto valik

Kuvatakse põhikontod, mille olete eelnevalt juriidilise isiku jaoks pearaamatu tasakaalustuskontodena määratlenud. (Põhikontod määratakse pearaamatu tasakaalustuskontodeks **Pearaamatu pearaamatu \> seadistus Pearaamatu \> parameetrid Pearaamatu \> tasakaalustused**.)

### <a name="main-account-and-posting-layer"></a>Põhikonto ja sisestamiskiht

Põhikonto  **ja sisestamiskihi** **väärtused** on nõutavad vastendamiskriteeriumid. Pearaamatu **deebet-** **ja kreeditkande** põhikonto ja sisestamiskihi väärtused peavad automaatse pearaamatu tasakaalustusprotsessi ajal olema võrdsed.

### <a name="posting-type"></a>Sisestamistüüp

Valige suvand **Sisestamistüüp**, kui pearaamatu deebet- ja kreeditkannetel peab automaatse pearaamatu tasakaalustusprotsessi ajal olema sama sisestamistüüp.

### <a name="financial-dimensions"></a>Finantsdimensioonid

Valige suvand **Finantsdimensioonid**, kui pearaamatu deebet- ja kreeditkannetel peavad automaatse pearaamatu tasakaalustusprotsessi ajal olema samad finantsdimensioonid. Kui see suvand on valitud, tuleb valida kriteerium finantsdimensiooni väärtustele loendis Saadaolevad **finantsdimensioonid**. Saadaolevad **finantsdimensioonide** loend ei sisalda põhikonto dimensiooni, kuna see on automaatselt vajalik vastendamiskriteeriumi osana.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Saate kuvada pearaamatu tasakaalustuste automatiseerimise tulemusi.

Pärast pearaamatu tasakaalustuse automatiseerimise seeria loomist kuvatakse iga pearaamatu tasakaalustuse esinemiskordi protsessi automatiseerimise nädalases vaates. Samuti kuvatakse iga sündmuse olek. Kasutatakse järgmisi olekuid.

- **Plaanitud**  – automatiseerimine on planeeritud, kuid see on veel käivitamata.
- **Käivitamine** – automatiseerimine on hetkel käimas.
- **Tõrge**  – automatiseerimine on käivitunud, kuid ilmnes tõrge. Saate tõrkeid vaadata, klõpsates nuppu **Kuva** tulemused.
- **Lõpule viidud**  – automatiseerimine on edukalt käitatud. Tasakaalustuse tulemusi saate vaadata pearaamatu tasakaalustuste **lehel**.

Vastavate tulemuste vaatamiseks minge pearaamatu perioodiliste **ülesannete \> pearaamatu \> tasakaalustustele**. Automatiseerimisreegli **väli** pearaamatu **tasakaalustuste** lehel näitab automaatse pearaamatu tasakaalustuse planeeritud ülesande nime, mida kasutati kande tasakaalustamiseks. Ebaõnnestunud tasakaalustuskatsed ei värskenda automatiseerimisreegli **väärtust**. Kui pöörate käsitsi ümber kande, mille automatiseerimisprotsess tasakaalustas edukalt, **siis automatiseerimisreegli** väärtus eemaldatakse.

Vastendatud **kirjete** tasakaalustatud kuupäeva väli näitab automatiseeritud protsessi sooritamise kuupäeva.

## <a name="editing-a-ledger-settlement-automation"></a>Pearaamatu tasakaalustuse automatiseerimise redigeerimine

Protsessi automatiseerimise raamistik võimaldab teil redigeerida seeriaid ja esinemiskordi, mis luuakse pearaamatu tasakaalustuse jaoks. Seeriat saab redigeerida kas protsessi automatiseerimise **leheküljelt** või protsessi automatiseerimise nädala kuvalt. Näiteks kui haldur otsustab esmaspäeva asemel teostada pearaamatu tasakaalustamise, võib ta leida iganädalases vaates esinemisjuhtumi **ja valida vaate/redigeerimise – seeria**.

Seeria muutmisel palutakse teil määrata, kas muudatus tuleks teha kõigi olemasolevate või ainult uute esinemiskordade puhul. Ajaloolisi esinemisi, mille olek on **juba** Lõpetatud või mille olek on Tõrge **** , ei muudeta.

Samuti saate lisada uue sündmuse või muuta olemasolevat sündmust. Näiteks planeeritakse järgmise pearaamatu tasakaalustuse esinemine kolmapäevaks, 1. jaanuariks, kuid selleks kuupäevaks on püha. Te saate juhtumit muuta kas protsessi automatiseerimise **leheküljelt** või protsessi automatiseerimise nädala kuvalt. Avatakse leht, mis näitab graafiku üksikasju ja vastendamise kriteeriume. Siin saate redigeerida plaanitud kellaaega ja kuupäeva. Vajadusel saate vastekriteeriume ka redigeerida. 

Samuti saate sündmuse või seeria keelata. Juhtumi keelamiseks ja selle töötlemise peatamiseks valige see protsessi automatiseerimise nädalavaates ja valige käsk **Keela**. Seeria saate keelata lehel Protsessi **automatiseerimine** .

## <a name="security-for-ledger-settlement-automation"></a>Pearaamatu tasakaalustuse automatiseerimise turvalisus

Pearaamatu **tasakaalustuste** **automatiseerimise** seeria sätete kohustuse haldamine on lisatud raamatupidamise haldaja ja raamatupidamise ülevaataja rollidele ning pearaamatu tasakaalustuste automatiseerimise seeriasätete kuvamine on lisatud pearaamatu tasakaalustamise automatiseerimise rollidele raamatupidaja, raamatupidamise haldaja ja raamatupidamise ülevaataja rollidele. Need kohustused on vaikimisi turvasätted, kuid neid saab muuta vastavalt teie organisatsiooni vajadustele.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Pearaamatu parameetrid pearaamatu tasakaalustuse automatiseerimiseks

Tasakaalustuse **tüüpiline** saldo väli näitab järjekorda, kus automaatset pearaamatu tasakaalustust töödeldakse. Tasakaalustamise tavalise saldo väärtuse **seadistamiseks** või vaatamiseks minge **\>\> pearaamatu häälestuse pearaamatu parameetritesse** ja valige vahekaart Pearaamatu **tasakaalustused**.

Kui **deebet** on valitud, algab automatiseeritud pearaamatu tasakaalustusprotsess deebeti poolelt ja otsib vastavaid kreediteid. Kui **kreedit** on valitud, algab automaatne pearaamatu tasakaalustusprotsess kreediti poolelt ja otsib vastavaid deebeteid. See valik peaks peegeldama põhikonto tüüpilist saldot.

## <a name="processing-a-ledger-settlement-automation"></a>Pearaamatu tasakaalustuse automatiseerimise töötlemine

Automatiseerimise käivitamisel valib süsteem pearaamatukanded põhikontodele, mis on määratletud protsessi automatiseerimise seeriale. See tellib kanded kuupäeva järgi, kasutades kuupäevavahemikku rahandusaasta algusest kuni protsessi automatiseerimise käituse kuupäevani. See vastab määratud vastendamiskriteeriumi põhjal. Deebeti ja kreediti arvestusvaluuta summade absoluutväärtused peavad tasakaalustamiseks ühtima.

Kui põhikontot töötleb pearaamatu tasakaalustuste automatiseerimise esinemine, ei saa te seda **pearaamatu tasakaalustuste lehel kuvada**. Peate ootama, kuni automatiseerimisprotsess on lõpetatud. Soovitame konfliktide vältimiseks planeerida protsessi automatiseerimise töötamaks väljaspool tööaega.

Automatiseerimisprotsess kaasab kõik kriteeriumitele vastavad kanded, v.a kanded, mis on käsitsi märgitud tasakaalustamiseks pearaamatu **tasakaalustuste** lehel.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Automatiseerimisprotsessi tasakaalustatud kannete tagasipööramine

Saate tühistada automaatse pearaamatu tasakaalustusprotsessi tehtud tasakaalustuse. Automatiseerimisprotsessiga tasakaalustatud kande tühistamisel automatiseerimisreegli **väärtus** eemaldatakse.
