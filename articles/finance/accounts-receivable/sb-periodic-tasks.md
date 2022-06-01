---
title: Korduva lepingu arvelduse perioodilised ülesanded
description: Selles teemas kirjeldatakse korduva lepinguga arveldamise jaoks saadaolevaid perioodilisi toiminguid.
author: JodiChristiansen
ms.date: 04/29/2022
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
ms.openlocfilehash: 80f65d82881bb000f626c4225b3eac7dd1a2a44a
ms.sourcegitcommit: 1877696fa05d66b6f51996412cf19e3a6b2e18c6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786982"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Korduva lepingu arvelduse perioodilised ülesanded

Selles teemas kirjeldatakse korduva lepinguga arveldamise jaoks saadaolevaid perioodilisi toiminguid.

## <a name="generate-invoice"></a>Arve loomine

Kasutage lehte **Arve loomine**, et luua igakuised korduvad hulgiarved **teabest, mille seadistate kõigil arveldusgraafikutel** ja arvelduse **üksikasjade lehtedel**. Arve loomisel uuendatakse müügitellimuse töötlemisrea kauba kirjeldust kauba kirjeldusega ning arveldatud graafikurea arvelduse algus- ja lõppkuupäevaga.

## <a name="generate-invoice-batch-processing"></a>Arve pakett-töötluse loomine

Korduvate **arvete loomiseks** korduvate pakett-tööde protsessi kaudu kasutage lehte Arve pakktöötluse loomine. Saadaolevad parameetrid on samad, mis arve loomise lehel olevad parameetrid, kuid neid saab **salvestada** pakktöötluses, mida saab mitu korda käitada.

## <a name="price-update"></a>Hinna uuendamine

Kasutage utiliidi Hinna uuendamine mitme kauba hindade uuendamiseks ühel toimingul mitmes arveldusgraafikus. Hindu saab uuendada kas määratud protsendi või määratud summa põhjal. Ridade loendis kuvatakse ainult kaupade praegused ühikuhinnad. See ei näita hindu pärast hinna uuendamist.

Pange tähele järgmisi punkte utiliidi Hinna uuendamine kohta:

- Kui kindla aasta müügitellimus on juba loodud (st kaubad on arveldatud), ei mõjutata reaüksuste hinda.
- Utiliiti Hinna uuendamine saab kasutada reaüksuste puhul, mille olek on Aktiivne **või** **Ootel**. Ootel kaupade puhul peab ootel **olemisel** **olema** valik Kohanda graafikut määratud väärtusele Ei.
- Hinna uuendamise utiliiti ei saa kasutada reaüksuste puhul, mis on kasutusüksused, mis kasutavad laiendamist, vahe-eesmärgi arveldust või tulu tükeldamist.

### <a name="price-update-example"></a>Hinna värskendamise näide

Luuakse arveldusgraafik ja lisatakse uuendamisüksus. Ühiku hind on $750. Kauba esimene aasta tasutakse 15. detsembril 2021. Arveldusgraafik luuakse perioodiks 1. jaanuarist kuni 31. detsembrini 2022.

Uuendamise ajal loob **arve loomise** protsess müügitellimuse aastale 2022. Pärast utiliidi Price update käivitamist uuendatakse hind $750 $800.

2022. aasta müügitellimust ja arveldusgraafikut ei mõjutata ja ühiku hind jääb $750, sest 2022. aasta arveldusgraafikule on arve juba välja antud. Arveldusgraafiku rida ja rea üksikasju 2023-ks värskendatakse $800, sest 2023. aasta arveldusgraafikule pole veel arvet esitatud.

### <a name="update-prices--flat-pricing-method"></a>Hindade uuendamine – lamehinna meetod

Kui värskendate kaupade hindu, mis kasutavad kindla hinnakujunduse meetodit, saate hinna suurendamiseks määrata protsendi või summa.

Utiliidi Hinna uuendamine käivitamiseks kaupade puhul, mis kasutavad kindla hinnakujunduse meetodit, järgige neid samme.

1. Utiliidilehel **Hinnavärskendus** valige lamehinna **meetod**.
2. **Valige väljal Tõusu** meetod kaupade hinna värskendamiseks kasutatav kasvumeetod.
3. Sõltuvalt valitud kasvumeetodist määrake protsent väljal **Protsent** või summa väljal **Summa**.
4. Kiirkaarti **kaasavad** kirjetes kasutage andmefiltrite **lisamiseks** nuppu Filtreeri.
5. **Kirjete** vahemiku vaatamiseks valige kuva eelvaade.
6. Kui te ei soovi mõnda rida töödelda, märkige need ja valige käsk **Eemalda**.
7. Valige nupp **OK**.

### <a name="update-prices--standard-pricing-method"></a>Uuenda hinnad – standardne hinnakujundusmeetod

Kui kauba hinda on kauba kirjes muudetud, saab seda uuendada kõigi arveldusgraafiku ridade puhul, kui kaup kasutab standardset hinnakujundusmeetodit.

1. Utiliidilehel **Hinna** uuendamine valige **standardne** hinnakujundusmeetod.
2. Kiirkaarti **kaasavad** kirjetes kasutage andmefiltrite **lisamiseks** nuppu Filtreeri.
3. **Kirjete** vahemiku vaatamiseks valige kuva eelvaade.
4. Kui te ei soovi mõnda rida töödelda, märkige need ja valige käsk **Eemalda**.
5. Valige nupp **OK**.

## <a name="mass-hold-processing"></a>Hulgi kinnipidamise töötlemine

Kasutage hulgi ootel **olemise** lehte, et rakendada ootel olemise suvandeid korraga mitmele arveldusgraafikule.

Ainult ühe arveldusgraafiku või ühe arveldusgraafiku rea ootele panemiseks avage leht **Kõik arveldusgraafikud** ja valige ootele **soovitud koht**. Ootel olese eemaldamiseks kasutage lehte Eemalda **ootel hoida**.

### <a name="put-billing-schedules-on-hold"></a>Pane arveldusgraafikud ootele

Mitme arveldusgraafiku ootele panemiseks järgige neid samme.

1. Seadistage **lehel Mass** ootel suvand **Töötle nii, et** see rakendaks **ootel olemist**.
2. **Väljal Põhjuse** kood valige põhjuse kood.
3. Seadistage valik **Kohanda graafikut**:

    - **Jah** – kui seate suvandi väärtuseks **Jah**, määrake väljal Ootel **olemise kuupäev ootel olemise** kuupäev. Kõik arveldusgraafiku read pärast ootel olemiskuupäeva on eemaldatud.
    - **Ei** – arveldusgraafiku ridu ei ole muudetud. Muudetakse ainult olekut. See uuendatakse ootel **.**

4. Kiirkaarti **kaasavad** kirjetes kasutage andmefiltrite **lisamiseks** nuppu Filtreeri.
5. **Kirjete** vahemiku vaatamiseks valige kuva eelvaade.
6. Kui te ei soovi mõnda rida töödelda, märkige need ja valige käsk **Eemalda**.
7. Valige nupp **OK**.

Kui naasete arveldusgraafikute loendisse, peaksite nägema, et arveldusgraafikute olek on muudetud **ootel olekuks**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Ootel olemise eemaldamine mitmest arveldusgraafikust

1. Seadke lehel **Mass ootel** suvand Töötle **väärtuseks** Eemalda **ooteltus**.
2. Sisestage **põhjusekood** väljale Põhjuse kood.
3. Valige väljal **Eemalda** kuupäev ootel olemise eemaldamise kuupäev.
4. Seadistage **vastavalt vajadusele taassaamiskuupäeva** **ja** viitvõla kuupäeva väljad. Viitvõlakuupäev lisatakse kõigile viitvõlga omavatele ridadele.
5. Kiirkaarti **kaasavad** kirjetes kasutage andmefiltrite **lisamiseks** nuppu Filtreeri.
6. **Kirjete** vahemiku vaatamiseks valige kuva eelvaade.
7. Kui te ei soovi mõnda rida töödelda, märkige need ja valige käsk **Eemalda**.
8. Valige nupp **OK**.

> [!NOTE]
> Ootel olemise eemaldamiseks peate lehel **Korduva lepingu arveldusparameetrid** **häälestama ootel kasutajagrupi eemaldamise** väärtuse.

Näiteks arveldusreal on alguskuupäev 1. veebruar 2022 ja lõppkuupäev 28. veebruar 2022. Arveldussumma on $200. Ootel **olemise** kuupäeva väli on seatud 10. veebruarile 2022. Seetõttu korrigeeritakse veebruari perioodi nii, et see välistaks mis tahes kuupäeva pärast 10. veebruari. Uus periood on alates 1. veebruarist kuni 9. veebruarini ja summat $64.29 (läbi igapäevase katseaja). Kõik arveldusgraafiku read 10. veebruaril või hiljem eemaldatakse.

Kui ootel **protsessi** Eemaldamine on lõpetatud **ja** välja Eemalda kuupäev väärtuseks on seatud 10. veebruar 2022, siis on kaks arveldusperioodi. Esimene arveldusperiood on 1. veebruar – 9. veebruar ja summa $64.29. Teine arveldusperiood on 10. veebruar – 28. veebruar ja summa $135.71.

## <a name="mass-termination-processing"></a>Hulgi lõpetamise töötlemine

Kasutage massilise **lõpetamise lehte**, et lõpetada arveldusgraafiku read, mis on hetkel kuvatud, määrates lõpetamise kuupäeva.

Kui kasutate tulu ja kulu viitvõlgu, on arveldusgraafikud, **·** **kus** lõpetamise kuupäeva väli on seatud kohandama graafikut lehel Kõik arveldusgraafikud on **tagasimakseks** kõlblik.

Arveldusgraafikuid, mis kasutavad mitme elemendi eraldamise (MEA) funktsiooni, ei ilmu massilise **lõpetamise lehel**. Saate siiski lõpetada individuaalse arveldusgraafiku, kasutades arveldusgraafikus lõpetamise funktsioone.

> [!NOTE]
> Arveldusgraafiku read, mis on praegu kaasatud arve **loomise partiisse**, pole selle protsessi jaoks saadaval.

Lisateavet iga välja ja protsessi kohta vt arveldusgraafikute [lõpetamisest](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Hulgiarhiivimise protsess

Mitme arveldusgraafiku **arhiveerimiseks** kasutage hulgiarhiivi lehte. Arhiivida saab ainult lõpetatud arveldusgraafikuid.

Pärast arveldusgraafiku arhiivimist toimuvad järgmised sündmused:

- Olek muudetakse arhiveeritud **olekuks**.
- Arveldusgraafikud on jäädavalt lukus.
- Arveldusgraafiku read pole enam päringulehtedel saadaval.

> [!NOTE]
> Arveldusgraafiku arhiveerimine on jäädav tegevus ja seda ei saa tühistada.

Arveldusgraafikute arhiivimiseks järgige neid samme.

1. **Määrake hulgiarhiivi** lehel arvelduse **lõppkuupäeva** väljal arvelduse lõppkuupäev. Kõikide lõpetatud arveldusgraafikute vaatamiseks jätke see väli tühjaks.
2. **Kasutage kiirkaarti kaasamiseks** kirjetes nuppu **Filtreeri**, et piirata kuvatud kirjeid.
3. Valige **vaate eelvaade**.
4. Kui te ei soovi mõnda kirjet arhiivida, märkige need ja valige käsk **Eemalda**.
5. Valige **OK**, et arhiveerida leheküljel olevad kirjed.

## <a name="mass-stubbing-process"></a>Hulgi eemaldamise protsess

Kasutage hulgikupsusti **lehte**, et märkida kõik valitud arveldusgraafiku read arveldatud (kui) või arveldamata (ümberpööratud) ridadena. Eelmüümine või ümberpööramine toimub enamasti teises süsteemis varem arveldatud imporditud arveldusgraafiku ridadel. Kangekaeldatud arveldusgraafiku read kuvatakse kui pik ning kliendi jaoks arvet ei loota.

### <a name="stub-records"></a>Jää jääga kirjed

1. Märkige hulgikupsusti **lehel** väljal **Protsessi valikud** ruutKup **·**.
2. Seadke äralõigamiskuupäeva **väljal** äralõigamiskuupäev, et määrata read, millele soovite protsessi rakendada. Kuvatakse ainult kirjed, mille arvelduse alguskuupäev on määratud äralõigamiskuupäeval või enne seda.
3. Märkige **ruudu Kuva** eelvaade, et kuvada read, mida soovite eelmüüda.
4. Rea eemaldamiseks protsessist märkige see ja valige käsk **Eemalda**.
5. Ridade **tüükamiseks** valige suvand Protsess.

### <a name="reverse-stub-records"></a>Tühista jäära kirjed

1. Hulgikupsusti **lehel** väljal Protsessi **suvandid** valige tühistakup **.**
2. Seadke äralõigamiskuupäeva **väljal** äralõigamiskuupäev, et määrata read, millele soovite protsessi rakendada. Kuvatakse ainult kirjed, mille arvelduse alguskuupäev on määratud äralõigamiskuupäeval või enne seda.
3. Märkige **ruut Kuva eelvaade**, et kuvada read, mida soovite ümber pöörata.
4. Rea eemaldamiseks protsessist märkige see ja valige käsk **Eemalda**.
5. Ridade **ümberpööramiseks** valige protsess.

## <a name="update-completion-date-process"></a>Lõpetamiskuupäeva uuendamisprotsess

Kasutage lehte **Värskenda lõpetamise kuupäeva**, et värskendada konkreetsete vahe-eesmärkide kaupade lõpetamiskuupäeva mitme arveldusgraafiku või kasutaja puhul. Samuti saate uuendada kaupade valmimisprotsenti vahe-eesmärgi mallidel, mis kasutavad viisi **Lõpetatud** protsent.

1. Minge lõppkuupäeva **uuendamise lehel** vahe-eesmärgi töötlemisele **ja** valige suvand Uuenda **lõpetamisprotsent**.
2. **Väljale Protsentuaalse** summa sisestage lõpetatud koguprotsent.
3. Saate valida vahe-eesmärgi malliga seotud kaubakoodi.
4. Valige kiirkaardile **kaasamiseks** kirjetes **filter** **,** et filtrikriteeriumiks valida konkreetne lõppkasutaja konto **,** **arveldusgraafiku** number või kaubakoodide väärtus.
5. Valige **OK** muudatuse töötlemiseks. Kui töötlemine on lõpetatud, lisatakse vahe-eesmärgi eraldamisele uus rida. See rida näitab vahe-eesmärgi malli jaoks lõpetatud protsenti.

## <a name="unbilled-revenue-mass-processing"></a>Arveldamata tulu hulgitöötlemine

Kasutage arveldamata **tulu** hulgitöötlemise lehte, et luua arveldamata tulu töölehe kirje või tühjendage töölehe kirje ühe või mitme valitud arveldusgraafiku või arvelduse üksikasjarea jaoks.

- **Loo töölehe kirje** : looge arveldamata tulu töölehe kirjed mitme arveldusgraafiku rea jaoks. Kasutage kiirkaardi **kaasamiseks** **kirjetes** nuppu Filtreeri, et valida loendis ilmuvate kirjete vahemik. Loendis kuvatakse ainult arveldamisgraafiku read, mille kohta pole arveldamata tulu töölehe kirjeid loodud. Luuakse algsed töölehe sisestused. Viitvõla kaupade jaoks luuakse ka viitvõlagraafikud.
- **Jäägi töölehe** kirje – märkige arveldusgraafiku read, mille kohta on arveldamata töölehe kirjed juba loodud. Seda valikut kasutatakse juhul, kui stamata töölehe kirje on juba teises süsteemis sisestatud. See märgib segmentimata tulu töölehe kui jäägiga ja ei sisesta kannet pearaamatusse.
- **Tühistab pearaamtöölehe** kirje – tühistage töödeldud pearaamtöölehe kirjed. Kui pudutöölehe kirje töötlemisel **tehti** viga, **tühjendab see suvand arveldusgraafiku rea märkeruudu Stubbed**.
- **Kinnistatud arvelduse** üksikasjade rida – kasutage seda protsessi, kui arveldamata tulu on välissüsteemis töödeldud ja mõned arvelduse üksikasjaread on juba arveldatud. See protsess tagab, et õige summa ilmub tasumata tulu kontodele.
- **Tühista arvete üksikasjade rida** – tühistage mis tahes **stub arvelduse üksikasjarea** toimingud.

Töölehe **nime välja** kasutatakse töölehe loomise **sisestuse sisestamiseks** pearaamatusse.

> [!NOTE]
> Pearaamprotsess ei sisesta summasid pearaamatusse. Töölehe **nime väli** ei ole saadaval kõigi jäägi- ja tühistamisprotsesside puhul.

### <a name="unbilled-revenue-stub-example"></a>Segmentimata tulu kange näide

Arveldusgraafik seadistatakse ühe aasta kohta alates oktoober 2021 kuni september 2022. Bilistamata tulu on juba välissüsteemis töödeldud. Üheksa kuu jooksul arveldusgraafikust on arve juba välja antud. Iga arveldusperioodi summa on $250. Aasta alguses sisestatakse tasumata tulule sisestatud kogusumma $3,000. Pärast üheksa kuud on $2,250 arve juba arveldatud ja $750 tasumata tulu jääb alles.

Arveldusgraafiku häälestamiseks, kus ainult kolm kuud arveldamata tulu jääb alles, järgige neid samme.

1. **Looge** arvelduse üksikasjade lehel arveldusgraafik perioodiks 2021. oktoober 2021 kuni septembrini 2022, kaubakood S0001 ja $250 kogusumma kuus.
2. Valige **arveldusgraafiku jaoks** töölehe sisestuse loomine. Kogutulu $3,000 sisestatakse tasumata tulule.
3. Valigekuku **arvelduse üksikasjade** rida ja määrake kande kuupäev 2022. aasta juuni (üheksa kuud). Arveldusgraafiku ridu ei kuvata eelvaates. Mõjutatud read põhinevad kande kuupäeval.
4. Valige nupp **OK**.

Arveldatud esimesed üheksa kuud on pikletud.

[![Arvelduse üksikasjade ridade vaatamiseks.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

Kulu $3,000 tühistatud tulult ja tulud $750 sisestamata tulus. Tasumata tulu **sisestuste** **vaatamiseks valige rea üksikasjade lehe vahekaardil Uuendamine** suvand Tasumata tulu töölehe sisestuse audit.

[![Segmentimata tulu töölehe sisestuse audit](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Arveldamata tulu töölehe kirje saab luua mis tahes uuendamisaja jaoks, eeldusel, et arveldatud on kõik eelnevate terminite arvelduse üksikasjaread. Näiteks on arveldusgraafiku real igakuine arveldussagedus 12 kuu jooksul, jaanuarist kuni detsembrini 2021. Real on kolm terminit: esialgne tähtaeg, teine termin (jaanuar kuni detsember 2022) ja kolmas tähtaeg (jaanuar kuni detsember 2023). Kui arve on loodud kõigile arvelduse üksikasjaridadele alates 2021. aasta 12 esimesest kuust, saab arveldamata tulu töölehe sisestuse luua ka teiseks perioodiks.
>
> Viitvõlgade kaupade puhul, mis kasutavad arveldamata tulu funktsiooni, töödeldakse arveldusrida ja allahindluse ridu. Nende kaupade jaoks luuakse arveldamata tulu töölehe kirje ning arveldusrea ja allahindluse rea viitvõla graafik.
>
> Mitte edasilükkamiste ja viitvõlgnevate kaupade jaoks loodud töölehe sisestused sisestavad kreediti erinevatele tulukontodele.
