---
title: Korduva lepingu arveldamine parameetrites
description: See artikkel selgitab, kuidas seadistada korduva lepinguga arveldamises loodud arveldusgraafikute vaikeväärtusi. See selgitab ka seda, kuidas luua arveldusgraafiku gruppe.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: cb60253f3cbb8c991ef2e106abdb1c685bf22171
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903330"
---
# <a name="recurring-contract-billing-parameters"></a>Korduva lepingu arveldamine parameetrites

Kasutage korduva **lepingu arveldusparameetrite lehte**, et seadistada korduvas lepingu arvelduses loodud arveldusgraafikute vaikeväärtused. Kõik teie valitud arveldusgraafikud kasutavad algselt neid vaikeväärtusi. Kuid te saate iga arveldusgraafiku väärtusi vastavalt vajadusele muuta.

## <a name="general-tab"></a>Vahekaart Üldine

1. **Korduva lepingu arveldusparameetrite** lehel vahekaardil **Üldine** väljal **Arveldusgraafiku grupp** valige arveldusgraafiku grupp. Teavet arveldusgraafiku gruppide häälestamise kohta vt selles artiklis [hiljem](#set-up-billing-schedule-groups) arveldusgraafiku gruppide jaotisest.
2. Väljal Lõpetamise **tüüp** valige, kuidas lõplik arve arvutatakse siis, kui arveldusgraafik on lõpetatud:

    - **Korrigeerige** graafikut: katkestage arveldusgraafik lõpetamise kuupäeval, **muutke** graafiku olek olekuks Viimane arveldus ja kohandage seotud viitvõla graafikut, muutes summa, mida ei ole enam vaja tuvastada. Kui arvelduse alguskuupäev on pärast lõpetamise kuupäeva, eemaldatakse arveldusperioodi jääk.
    - **Allesjäänud arve** – lisage lepingu lõpetamise perioodile kõik arveldusgraafiku ülejäänud summad, **muutke** graafiku olek olekuks Viimane arveldus ja värskendage viitvõla graafikut. Kui arvelduse alguskuupäev on pärast lõpetamise kuupäeva, lisatakse arveldusperioodile kõigi järelejäänud arveldusperioodide kogusumma ja järelejäänud arveldusperioodid eemaldatakse.
    - **Korrigeerimine** puudub – lõpetage arveldusgraafik lõpetamise kuupäeval. Arveldusgraafikusse ei ole korrigeerimisi tehtud.

3. Valige väljal **Kordumatu graafiku** tüüp suvand **Pole**, et määratleda klientide piiramine ühe arveldusgraafikuga. Valige **kliendi või** lõppkasutaja **kohta, et** määratleda klientide kordumatu graafiku piiramine.
4. Seadke suvandi **Kuu joondamine** väärtusele **Jah**, et joondada arveldusgraafiku üksikasjaread kuu lõpuga, kui arveldusgraafik on loodud või värskendatud. Järkjärguliste kuupäevade **kasutamiseks** määrake selle väärtuseks Ei.
5. Määrake suvand **Jaota osalised perioodid** suvandile **Jah**, et eraldada arveldussummad perioodi päevade arvu põhjal. Seadistage see **väärtusele** Ei, et saada võrdne summa igas arveldusperioodis, sõltumata päevade arvust.
6. Kui seate suvandi **Jaota** osalised perioodid väärtusele **Jah**, määrake väärtuseks Mõõduväli Igapäevane **,** **et** jaotada summad perioodi päevade arvu põhjal. Määrake see väärtusele **Kord** kuus, et summa oleks igal kuul võrdne.
7. Määrake, kas vastloodud arveldusgraafikud on vaikimisi ootel.

    > [!NOTE]
    > Arveldusgraafiku ootel olemise eemaldamiseks peab kasutaja olema kasutajagrupi osa. Valige **suvand Eemalda ootel kasutajagrupi alistamine**, et seadistada kasutajagrupp, kus suvand Luba **eemaldamise ootel** olla on lubatud.

8. Valige arve **kandetüübi** väljal arve kande vaiketüüp uute arveldusgraafikute jaoks.
9. Seadistage viitvõla **joondamine arveldussuvandi** alla **Jah**, et joondada vastav viitvõla graafik nii, et see kasutaks arveldusgraafikuga samasid kuupäevi. Erinevate kuupäevade **soovitud** kuupäevade miseks määrake selle väärtuseks Ei.
10. Kui kasutate tulude tükeldamise funktsiooni, seadistage **suvand Loo tulu tükeldamine** automaatselt **valikule Jah**, kui kaubad lisatakse arveldusgraafikusse. Kui **kaup on** seadistatud tulu tükeldamise kaubaks, valitakse automaatselt arveldusgraafiku real märkeruut Tulu tükeldamine. Kui soovite märkeruudu **Tulu** tükeldamine käsitsi valida, märkige **valik** Ei.
11. Seadke müügitellimuse loomise väljad:

    - Arveid saab konsolideerida perioodi, kliendi või kauba kaupa. Määrata saab väärtuste **Jah** **ja** Ei mis tahes kombinatsiooni. Arveid saab jagada ka kaubagrupi kaupa.
    - Arvete jaoks on saadaval järgmised sisestusvalikud:

        - **Loo müügitellimus** – looge ainult müügitellimus.
        - **Kuva arve sisestamine** – arveldage müügitellimus ja avage leht, kus saate arve käsitsi sisestada.
        - **Tasu tekstiarve loomine** – valige see suvand, kui kasutate vabas vormis arveid.
        - **Sisestage arve** automaatselt – arveldage müügitellimus ja sisestage see automaatselt.

    - Häälestage valikuLe **Kauba kirjeldus arvelduskuupäevade** lisamine suvandile **Jah**, et lisada kirjeldus, mis sisaldab arvelduse alguskuupäeva ja lõppkuupäeva.
    - Määrake suvandi Nulltarbimine **valiku välistamine** väärtusele **Jah,** et välistada arveldusgraafiku read, kus tarbimine puudub. Määrake nende ridade **kaasamiseks** müügitellimusele väärtuseks Ei.
    - Kui te **ei soovi printida müügitellimusel** **tulu** tükeldatud tütarüksusi, määrake suvandi Ära prindi tütarüksused väärtusele Jah. Arvel kuvatakse ainult emaüksus. Kui (peidetud) tütarüksuste netosumma pole null, kuvatakse emarea netosumma tütarridade kokkuvõte. Valikuks määrake **Ei,** et printida müügiarvel kõik emakauba all olevad tütarüksused.

12. Seadke toe ja uuendamise väljad:

    - Häälestage suvand **Automaatsed toe ja uuendamise** lubamine valikule **Jah**, et kasutada müügitellimuses automaatselt toe ja uuendamise funktsiooni.
    - Valige väljal **Tugi ja uuendamise tase** vaikimisi tugi ja uuendamise tase.
    - Väljal Tugi **ja uuendatav kogus** määrake tugi ja uuendatav kogus.
    - Väljal Vaikimisi **toe ja uuendamise alguskuupäev** määrake kuupäev, mida kasutada vaikimisi alguskuupäevana toe ja uuendamise puhul:

        - **Kande kuupäev** – kasutage kandekuupäeva alguskuupäevana.
        - **Jooksva kuu algus** – kasutage alguskuupäevana praeguse kuu esimest.
        - **Järgmise kuu algus** – kasutage alguskuupäevana järgmise kuu esimest. Kui kandekuupäev on esimene, kasutatakse käesoleva kuu esimest.
        - **Reegel 15** – kasutage alguskuupäevaks praeguse kuu esimest, kui kande kuupäev on kuu esimesest kuni viieteistkümnendani. Kui kande kuupäev on kuueteistkümnes või hilisem, kasutage alguskuupäevana järgmise kuu esimest.

    - Häälestage valik **Kaasa allahindlus arvutusse** valikule **Jah,** et kaasata allahindluse summa toe- või uuendamissummasse. Allahindluse summa välistamiseks **määrake** selle väärtuseks Ei.
    - Väljadel **·** **Toe** sagedus ja Uuendamissagedus valige sagedus, mida kasutada, kui arveldusgraafikusse lisatakse tugi- ja uuendamisüksused: **Igapäevane**,**Kuu**, **Kvartal**, **Semiannually** või **Iga-aastane.**
    - Häälestage suvand **Kaubagrupi järgi joondamine** suvandile **Jah**, et joondada uute kaupade algus- ja lõppkuupäevad kaubagrupil põhinevalt olemasolevate kaupadega.
    - Häälestage **suvand** **Vii** järgmise tasumata perioodi alla suvand Jah, et määrata uuendamiskauba joonduskuupäev järgmise, pärast uuendamist tasumata perioodi kuupäeva alusel.
    - Seadistage **suvand Kopeeri seerianumber** valikule **Jah,** et kopeerida kauba seerianumber algse müügitellimuse realt vastavale arveldusgraafiku reale.

13. Kui kasutate arveldusgraafiku eskalatsiooni, valige meetod, mida kasutatakse tarbimishinna indeksi arvutamiseks.
14. Kui soovite **arveldusgraafiku ridade** hinnamuutuste **kirjet**, määrake suvandi Jälgi hinnamuutust väärtuseks Jah. Kui arveldusgraafiku rida muudetakse käsitsi standardsest lamehinnaks ja uus hind on sisestatud, jälitatakse auditi teavet arveldusgraafiku real. Kui te ei soovi **muudatusi** jälitada, määrake valikuks Ei.
15. Määrake, kas arve loomise lehel filtreeritakse vaikimisi algus- või lõppkuupäeva **järgi kirjed**.
16. Kui kasutate segmentimata **tulu funktsiooni**, määrake kasutatavad valikud:

    - Kui soovite **, et üldtööleht** loodaks **ja** sisestaks samaaegselt, määrake suvandi Üldise töölehe automaatne sisestamine väärtuseks Jah. Kui soovite pearaamatu **luua** ja seejärel käsitsi sisestada, määrake selle väärtuseks Ei.
    - **Väljal Töölehe vaikenimi** saate valida üldise töölehe loomisel kasutatava vaiketöölehe nime.
    - **Väljal Lühiajalised vabad meetod** valige lühiajaliselt vaba meetod, kui kasutate meetodit. Valiku Pole **puhul** ei kasutata lühiajalist funktsiooni tuluga, mis ei ole seotud ühegi tuluga. Valige **Jooksvad perioodid**, et kasutada alati 12 kuud või **Fikseeritud aasta** ülejäänud finantsaasta kasutamiseks.

17. Määrake valikud, mida kasutatakse siis, kui arveldusgraafik ja selle read on lõpetatud:

    - **Väljasta** krediit – looge kreeditarve, kui arveldusgraafik või arveldusgraafiku rida on lõpetatud.
    - **Kreediti** korrigeerimine: looge arveldusgraafiku kreediti korrigeerimine, kui rida lõpetatakse. Kreediti korrigeerimine ilmub arveldusgraafiku tulevases arveldusperioodis. Kreediti korrigeerimine värskendab arve summat järgmiseks arveldusperioodiks, kuni krediit on arveldusgraafikule rakendatud.
    - **Kreedit puudub** – ärge looge kreediti korrigeerimist ega kreeditarvet, kui arveldusgraafik või arveldusgraafiku rida on lõpetatud. See valik on saadaval ainult siis, kui **suvandit** Korrigeerimata kasutatakse arveldusgraafiku lõpetamiseks.

## <a name="sequence-number-tab"></a>Vahekaart Seerianumber

Kasutage korduva **lepingu** arveldusparameetrite **lehel järjekorranumbri vahekaarti** arveldusgraafiku numbrite vaikeväärtuse miseks. Vaikeväärtused seadistatakse numbriseeriate **lehel** (**Organisatsiooni haldamise numbriseeriad \>\> Numbriseeriad**).

## <a name="set-up-billing-schedule-groups"></a>Arveldusgraafiku gruppide seadistamine

Kasutage arveldusgraafiku **grupi lehte**, et luua arveldusgraafiku grupp korduva lepinguga arveldamiseks. Kui luuakse uus arveldusgraafik ja sellele rakendatakse **arveldusgraafiku** gruppi, sisestatakse arveldusgraafiku grupi lehel määratud väärtused arveldusgraafiku vaikeväärtuseks. Saate muuta kõiki vaikeväärtusi konkreetse arveldusgraafiku jaoks, mille loote. Saate seadistada mitu arveldusgraafiku gruppi ja seejärel määrata ühe neist vaikimisi arveldusgraafiku grupiks lehel **Korduva lepingu arveldusparameetrid**.

Korduva lepingu arveldamise arvelduse arveldusgraafiku grupi loomiseks järgige neid samme.

1. Arveldusgraafiku **grupi lehel valige** uus **, et** luua arveldusgraafiku grupp.
2. Sisestage **väljale Arveldusgraafiku** grupp kordumatu ID.
3. Väljale **Kirjeldus** sisestage kirjeldus.
4. Määrake väljal **Arveldussagedus**, kui sageli arveldatakse kliendile arveldusgraafikut: **üks kord**, Igapäevane, **·** **Igakuine**, **Kord** kvartalis, **Poolaasta** või **Kord aastas.**
5. Sisestage **arveldusintervalli** väljale arveldusintervall. Näiteks seadistage arveldussageduse **välja igakuiseks** **ja arveldusintervalli** **välja väärtuseks** **2**, et arveldada igal teisel kuul.
6. **Väljal Hinnakujundusmeetod** valige arveldusgraafiku kaupadele hinnakujunduse vaikemeetod:

    - **Standardne** – arvutage ühiku hind sisestatud kogusumma põhjal ja kasutage tooteteabe halduses **lehte Väljastatud** tooted standardset hinnakujundust.
    - **Lame** – rakendage arveldusgraafiku reale sisestatud kindla hinna.
    - **Kiht** – arvutage ühiku hind, kasutades fikseeritud kogust erinevates hinnakujunduse sulgudes. Enne järgmise hinnakujunduse sulgudesse teisaldamist tuleb täita kõik järgud.
    - **Lame** kiht – arvutage ühiku hind, kasutades fikseeritud kogust ja laiendatud hinnasummasid erinevate hinnakujunduse sulgude puhul. Arveldusperioodi jooksul küsitav hind kasutab laiendatud hinda, mis vastab järgule, kus arvelduskogus on olemas.

7. **Väljal Kauba tüüp** valige arveldusgrupile kauba tüüp:

    - **Standard** – valige see väärtus, kui kogus on staatiline.
    - **Kasutus** : valige see väärtus mõõte- või tarbimistüüpi kaupade puhul. Kui valite selle väärtuse, seadistage **suvandi Kasutus** **lugemine** väärtuseks Lugemine, et sisestada arvesti või seadme arveldusperioodi väärtus (lugemine). Tarbitud väärtus arvutatakse eelmise arveldusperioodi ja praeguse sisestamisel põhinevalt.
    - **Vahe-eesmärk** – valige see väärtus, et kasutada vahe-eesmärgi arveldusfunktsiooni. Kui valite selle väärtuse, valige **vahe-eesmärgi malli** väljal vahe-eesmärgi mall, kui kasutate seda.
    - **Tarbimine**: valige see väärtus arveldusperioodi jaoks tarbitava väärtuse sisestamiseks.

8. Määrake valik **Arve eraldi** valikule **Jah**, et luua samale kliendile konsolideeritud arvete ja eraldi arvete kombinatsioon. Näiteks kliendil on viis arveldusgraafikut. Kolm neist konsolideeritakse ühele arvele, kuid igaüks ülejäänud kahest nõuab eraldi arvet. Määrake valikuks Ei **,** et kliendile luua ainult üks konsolideeritud arve.
9. Häälestage suvand **Värskenda automaatselt** valikule **Jah,** et uue arveldusperioodi korduv arveldusgraafikut arve loomisel automaatselt uuendada. Määrake arveldusgraafiku **käsitsi** uuendamiseks väärtusele Ei. Määrake uuendamisvälja **kohta lisamiseks** ridade arv iga uuendamise puhul.
10. Seadke suvandi **Eskaleerimine** väärtusele **Jah** *, et rakendada eskalatsioone* (hinnatõusu) selle arveldusgraafiku grupiga seostatud arveldusgraafikutele.
