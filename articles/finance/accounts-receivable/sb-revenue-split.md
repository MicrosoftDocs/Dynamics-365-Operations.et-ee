---
title: Tulu tükeldamise mallid kordustellimuse arvelduses
description: See artikkel selgitab, kuidas seadistada tulu tükeldatud malle kaupadele, mida müüakse kogumina.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904755"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Tulu tükeldamise mallid kordustellimuse arvelduses

Tulu tükeldamiseks **mallilehe** abil saate seadistada tulu tükeldamiseks malle. Tulu tükeldamine koosneb tütarüksustega emakaubast. Seda tüüpi kaupa müüakse klientidele tihti üksiku kauba või kogumina.

Näiteks saab arvutiüksuse luua järgmiselt:

- **Emaüksus: kordustellimuse** hõbedast
- **Rea (tütar)kaubad:**

    - Tugi
    - Hooldus
    - Litsents

Emakauba loomisel pidage silmas järgmisi piiranguid.

- Kaupa saab määrata emakaubana ainult üks kord.
- Emakauba saab valida samas mallis tütarkaubana.
- Kehtiv mall nõuab vähemalt ühte tütarüksust.
- Kaupa saab määrata rohkem kui ühe kogumi kauba tütarkaubana.
- Iga ema-tütarsuhe peab olema kordumatu.

## <a name="create-a-parent-item-that-has-child-items"></a>Looge emaüksus, kus on tütarüksused.

Järgige neid samme tütarüksustega emakauba loomiseks.

1. Tulu tükeldatud **malli lehel** valige **Uus**.
1. **Valige emaüksus** väljal Emaüksus. Välja **Variandi number** uuendatakse automaatselt. Väärtust saate vajaduse korral muuta.
1. **Valige väljal Eraldamismeetod** eraldamismeetod.
1. Valige loendis **Komponentüksused** suvand **Lisa tütarüksuste** lisamiseks.
1. Kui valisite **väljal** Eraldamismeetod **väärtuse** Protsent, määrake väljal **Protsent** protsent protsent.

    - Kui valisite **eraldamise meetodi** väljal Võrdse **summa**, uuendatakse **protsentuaalselt** automaatselt nii, et igal kaubal oleks võrdne protsent.
    - Kui valisite **eraldusmeetodi** väljal Muutuja summa, **·** **·** **Null** emasumma või Nullsumma, **·** **jääb välja Protsent väärtus 0** (null) ja seda ei saa muuta.

1. Valige käsk **Salvesta**.

## <a name="fields"></a>Väljad

Tulude **tükeldatud malli** lehekülg sisaldab järgmisi välju.

| Väli | Kirjeldus |
|-------|-------------|
| Ülemkaup | Saate valida kaubakoodi. Sellest kaubast saab teie lootav kogumikauba emakaup. |
| Toote nimi | Toote nimetus |
| Eraldamismeetod | <p>Valige eraldamismeetod:</p><ul><li>**Võrdne summa** – eraldamisprotsendid arvutatakse automaatselt ja jagatakse võrdselt kõigi mallis olevate kaupade vahel.</li><li>**Protsent** – saate määrata eraldamiseks protsendisumma. Kõigi protsentide summa peab olema 100.</li><li>**Muutuv** summa : lisatavatel tütarüksustel on netosumma 0 (null). Tütarüksuste hind tuleb määrata kande tasemel.</li><li>**Nullsumma** – emakaup säilitab oma ühiku hinna ja netosumma. Kõigi tütarüksuste netosumma on 0 (null).</li><li>**Emaüksuse nullsumma** – emakauba netosumma on 0 (null). Kõiki tütarüksusi käsitletakse standardüksustena. Kinnitamist ei kontrollita selle üle, kas tütarkauba summade summa võrdub emakauba summaga.</li></ul> |
| **Komponendi kaubad** | |
| Komponendi kaup | Saate valida kaubakoodi. See kaup on tütarüksus. |
| Variandi number | Valige kauba variandi number. |
| Toote nimi | Toote nimetus |
| Protsent | <p>Vahe-eesmärgi eraldamisprotsent:</p><ul><li>Kui välja **Eraldamismeetod** väärtuseks on seatud **Protsent**, saate määrata protsendi.</li><li>Kui eraldamismeetodi **välja** väärtuseks on seatud **Võrdne summa**, arvutatakse protsent automaatselt nii, et igal malli kaubal on võrdne protsent.</li><li>Kui eraldamismeetodi **välja** väärtuseks on **seatud Muutuv** summa, **Emasumma** null või Nullsumma **,** on protsent 0 (null) ja seda ei saa redigeerida.</li></ul><p>Selle välja väärtus võib olla mis tahes positiivne arv vahemikus 0 (null) kuni 100. Kõigi protsentide summa peab olema 100.</p> |
| Koguprotsent | <p>Väärtuste summa veerus **Protsent**.</p><ul><li>Kui välja **Eraldamismeetod** väärtuseks on **seatud Võrdne** **summa** või Protsent, peab kõigi protsentide summa võrduma 100-ga.</li><li>Kui eraldamismeetodi **välja** väärtuseks on seatud **Muutuv** summa, **·** **Emaüksuse nullsumma või Nullsumma**, on koguprotsent 0 (null).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Müügitellimuse tulu tükeldamine

Kaubaga müügitellimuse loomiseks, mis on seadistatud tulu tükeldamiseks, järgige neid samme.

1. **Looge müügitellimus** lehel Müügitellimus.
2. Valige iga tulu tükeldamiseks seadistatud kauba real märkeruut Tulu **tükeldamine**. Sellest kaubast saab emaüksus. Kui mall on juba seadistatud, ilmuvad tütarüksused automaatselt loendisse.
3. Veel tütarüksuste lisamiseks valige suvand **Lisa tulu tükeldatud tütarüksus** ja valige lisamiseks tütarüksus.
4. Salvestage tellimus.

## <a name="revenue-split-with-billing-schedules"></a>Tulu tükeldamine arveldusgraafikutega

Arveldusgraafiku loomiseks, mis on kaubaga, mis on seadistatud tulu tükeldamiseks, järgige neid samme.

1. Leheküljel Kõik **/aktiivsed arveldusgraafikud** looge arveldusgraafik.
2. Valige iga tulu tükeldamiseks seadistatud kauba real märkeruut Tulu **tükeldamine**. Sellest kaubast saab emaüksus. Kui mall on juba seadistatud, ilmuvad tütarüksused automaatselt loendisse.
3. Veel tütarüksuste lisamiseks valige suvand **Lisa tulu tükeldatud tütarüksus** ja valige lisamiseks tütarüksus.
4. Jätkake arveldusgraafikuga töötamise sammudega.

> [!NOTE]
> Kui tulude **automaatse tükeldamise suvand** on seatud korduva **lepingu** arveldusparameetrite **lehel** väärtusele Jah, ilmnevad järgmised tegevused:
>
> - Kui rea kaup on seadistatud tulu tükeldamise mallis emakaubaks, valitakse **automaatselt tulu tükeldamise** märkeruut.
> - Tütarüksused sisestatakse automaatselt müügitellimusele või arveldusgraafiku reale.
>
> Kui valiku **Loo tulu automaatselt tükeldamine** väärtuseks on seatud **Ei**, siis käitumine on nagu varem kirjeldatud.

## <a name="additional-revenue-split-information"></a>Täiendav tulu tükeldamise teave

Kui lisate kauba, mis on tulu tükeldamise osa, pange tähele järgmist teavet: 

- Emasummat ei saa edasi lükata.
- Tütarüksuste alguskuupäev, lõppkuupäev, kogus, üksus, sait ja laoväärtused põhinevad emakaubal. Neid väärtusi ei saa tütarüksuste puhul muuta. Kõik muudatused tuleb teha emaüksusele. 
- Hinnakujundusmeetod on Lame **ja** seda ei saa muuta.
- Alamüksusi saab lisada või eemaldada.
- Ema- ja tütarüksused peavad kasutama sama kaubagruppi. 
- Alamüksustel võib olla üks järgmistest seadistustest:

    - Arveldussageduse **ja** **arveldusintervallide** väljad on seadistatud samale väärtusele kui emaüksusel. 
    - Arveldussageduse **väli** on seatud väärtusele **Üks kord**. Sel juhul seatakse **arveldusintervallide** välja väärtuseks automaatselt **1**. 

- Tütarüksuste netosumma võrdub emasummaga. Kui eraldamismeetod on **Nullsummad**, on tütarkauba summad ja emasumma mõlemad 0 (null). 

    > [!NOTE]
    > Kui eraldamismeetod on **emasumma** null, ei võrdu tütarüksuste (mitte null) summa emasummaga, mis on 0 (null). Seda eraldusviisi kasutatakse sisemistes eesmärkides, et töötajad saaksid näha tütarüksusi. Kliendid saavad siiski näha ainult emakaupa.

- Kui müügitellimuse mitme elemendi kokkuleppe (MEA) **tüüp on Üksik**, luuakse ema- ja tütarüksuste lisatakse vastav mitme elemendi tulueraldise kande rida. 
- Kui tulu tükeldamise eraldamismeetod on **Võrdne** summa ja emasummat muudetakse, arvutatakse summad ümber kõigi alamridade puhul. 
- Tulu tükeldamisel, kus eraldamismeetod on **Muutuv** summa, ilmneb järgmine käitumine:

    - Emaüksuse netosumma kuvatakse veerus **Emasumma**. Seda väärtust saab redigeerida. Ühiku hind, netosumma ja allahindlus on 0 (null) ning seda ei saa redigeerida.
    - Tütarüksuste ühikuhind on 0 (null). Ühiku hinda või netosummat saate redigeerida. Ühe väärtuse muutmisel uuendatakse teine väärtus automaatselt.

- Tulu tükeldamisel, kus eraldamismeetod on **Protsent**, ilmneb järgmine käitumine:

    - Emaüksuse netosumma kuvatakse veerus **Emasumma**. Seda väärtust saab redigeerida. Ühiku hind, netosumma ja allahindlus on 0 (null) ning seda ei saa redigeerida. 
    - Tütarüksuste netosumma arvutatakse emaüksuse *protsendisummana*&times;*·*.

- Tulu tükeldamisel, kus eraldamismeetod on **võrdne summa**, ilmneb järgmine käitumine:

    - Emaüksuse netosumma kuvatakse veerus **Emasumma**. Seda väärtust saab redigeerida. Ühiku hind, netosumma ja allahindlus on 0 (null) ning seda ei saa redigeerida. 
    - Tütarüksuste netosumma arvutamiseks jagatakse emasumma kõigi tütarüksuste vahel võrdselt. 
    - Kui tütarüksused eemaldatakse või lisatakse, arvutatakse netosumma ja ühikuhinnad ümber nii, et kõigil tütarridadel oleks võrdsed summad. 
    - Kui emasummat ei saa võrdselt jagada, võib viimase alamkauba netosumma ja ühikuhind olla mõne võrra suurem või väiksem kui teiste tütarüksuste netosumma ja ühiku hind. 

- Tulu tükeldamisel, kus eraldamismeetodiks on **nullsumma**, ilmneb järgmine käitumine:

    - Ühiku hinda, netosummat ja allahindlust saab redigeerida. Emasumma on 0 (null) ja seda ei saa redigeerida. 
    - Tütarüksuste kogus, ühik, lao koht ja laoväärtused põhinevad emakaubal. Neid väärtusi ei saa tütarüksuste puhul muuta. Kõik muudatused tuleb teha emaüksusele. 
    - Tütarüksuste ühikuhind ja netohind on 0 (null) ning seda ei saa redigeerida. 

- Tulu tükeldamisel, kus eraldamismeetodiks on **emasumma** null, toimub järgmine käitumine:

    - Emakauba ühiku hind, emasumma ja netosumma on 0 (null).
    - Arveldusgraafikus ilmuvad tütarread nagu käsitsi lisatud ja kõik väärtused uuendatakse valitud arveldusgraafiku grupi põhjal. Neid väärtusi saab redigeerida. Tütarüksuste puhul **pääsete** **·** **juurde** laienduse ja allahindluse ning täpsemate hinnakujunduse valikute juurde, **kasutades** arvelduse üksikasjade vaate väljadel Sisestatud kogus, **Ühiku** hind, **·** **Allahindlus ja Netosumma.** 
    - Müügitellimusel on tütarridade allahindlus- ja allahindlusprotsent 0 (null). 
    - Ema- ja tütarüksuste arveldussagedust saab muuta ja igal real võib olla erinev sagedus. Emakaupa uuendatakse automaatselt nii, et see kasutaks oma tütarridade seast lühimat sagedust. Näiteks on tulu tükeldamiseks kaks tütarüksust, **·** **millest üks kasutab kuu arveldussagedust ja teine, mis kasutab iga-aastase arveldussageduse**. Sel juhul värskendatakse emakauba arveldussageduse kord **kuus**.
