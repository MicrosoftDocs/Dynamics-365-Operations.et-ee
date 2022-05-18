---
title: Tugi ja uuendamine
description: See teema kirjeldab, kuidas seadistada ja kasutada müügitellimuste toe- ja uuendamisprotsessi kaupade uuendamise arveldusgraafiku loomiseks.
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
ms.openlocfilehash: 7de74f2b12e8e7201663ba78d936131b301b1ff9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685766"
---
# <a name="support-and-renewals"></a>Tugi ja uuendamine 

See teema kirjeldab, kuidas sisestada tugiüksusi või uuendada kaupu müügitellimuste sisestamisel. Neid kaupu kasutatakse algse toelepingu tasusumma arvutamiseks ja/või uuendamise summa arvutamiseks, mida kasutatakse arveldusgraafiku loomisel kordustellimuse arvelduses. Näiteks müüb teie ettevõte serveri kliendile ning pakute esimesel aastal andmete varundamise kordustellimust ja võimalust seda kordustellimust igal aastal uuendada. Tugiüksus *on* esimese aasta kordustellimus ja *uuendamiskaup uuendatakse* igal järgneval aastal.

Saate sisestada teabe tugiteenuste lepingu, uuendamislepingu või mõlema kohta. Kui sisestate tugilepingu teabe, lisatakse müügitellimusele ainult tugiüksus. Kui sisestate uuendamislepingu teabe, kasutatakse uuendamisüksust arveldusgraafiku loomiseks.

## <a name="support-and-renewal-setup"></a>Toe ja uuendamise häälestus

Lehel Tugi **ja tasemete uuendamine** saate kaupade toetamiseks ja uuendamiseks häälestada erinevad tugitasemed. Tugi või uuendamine võib olla protsent algsest kaubasummast või võib olla standardsumma.

Korduva lepingu arveldusparameetrite lehel saate valida **vaikimisi toetasemed**.

Näiteks võib ettevõte pakkuda järgmist toe- ja uuendamistaset.

| Tugitase | Toetuse protsent | Uuendamisprotsent |
|---|---|---|
| Piiramatu | 40% | 30% |
| Kuldne | 25% | 18% |
| Hõbe | 20% | 14% |
| Pronks | 15% | 10% |

Toe loomiseks või taseme uuendamiseks järgige neid samme.

1. Valige lehel **Tugi ja tasemete uuendamine** suvand **Uus**.
2. **Väljale Tugitase** sisestage kordumatu nimi.
3. Väljale **Kirjeldus** sisestage kirjeldus.
4. **Väljal Tugiarvutusmeetod** valige tugiarvutusmeetod. Kui valite **protsendi**, sisestage tugiteenuste protsendi väljale **Tugiteenuste** protsent.
5. Valige väljal **Kalkulatsioonimeetodi** uuendamine. Kui valite **protsendi**, sisestage uuendamisprotsent väljale **Uuendamisprotsent**.
6. Valige käsk **Salvesta**.

### <a name="fields"></a>Väljad

**Tasemete Toe ja uuendamise** lehel on järgmised väljad.

| Väli | Kirjeldus |
|---|---|
| Tugitase | Tugi- või uuendamistaseme kordumatu ID (nt **Kuld või** **Hõbedas**). |
| Kirjeldus | Toe või uuendamistaseme kirjeldus. |
| Toe arvutamise meetod | Valige taseme toe arvutamise meetod: protsent **või** **standardsumma**. |
| Toetuse protsent | Kui valisite **toe** arvutamismeetodiks protsent, määrake protsent, mida kasutatakse tugiüksuse hinna arvutamiseks. Kui valisite **arvutamismeetodiks** standardsumma, määratakse summa kande loomisel. |
| Uuendamise arvutamise meetod | Valige taseme uuendamise arvutusmeetod: protsent **või** **standardsumma**. |
| Uuendamisprotsent | Kui valisite **uuendamise** arvutusmeetodiks Protsent, määrake protsent, mida kasutatakse uuendamiskauba hinna arvutamisel. Kui valisite **arvutamismeetodiks** standardsumma, määratakse summa kande loomisel. |

## <a name="support-and-renewal-process"></a>Toe ja uuendamise protsess

Tugi- ja uuendamisfunktsioonid võivad kaupadele rakendada erinevaid tugitasemeid ja uuendada kordustellimuse arvelduse uuendusteavet.

Enne toe ja uuendamise funktsioonide kasutamist tuleb lõpetada järgmised ülesanded.

1. Looge tugiteenuste **ja tasemete uuendamise** lehel vähemalt üks tugi- või uuendamistase.
2. Seostage **kaup kauba** seadistuse lehel kaupade toega ja uuendamisega. See ülesanne on nõutav ainult siis, kui soovite seadistada vaikeväärtused kaupade toe ja/või uuendamise jaoks.
3. Korduva lepingu **arveldusparameetrite lehel** määrake vaikimisi tugi ja uue arveldusgraafiku uuendamise sätted.

Kaupadele erinevate tugitasemete rakendamiseks ja uuendamisteabe värskendamiseks järgige neid samme.

1. **Looge müügitellimus leheküljel** Kõik müügitellimused.
2. **Lisage kaup müügitellimuse** ridade kiirkaardile.
3. Valige vahekaardil **Arve suvand** Tugi ning **värskendage tuge \> ja värskendage seda**.
4. Toe **ja uuendamise protsessi lehel** värskendatakse päisejaost sätted lehelt Korduva lepingu **arveldusparameetrid**. Need väärtused rakenduvad kõigile toe- ja uuendamisüksustele. (Nt kui arveldussagedus on seatud väärtusele **Igal aastal** on kõigil uuendamiskaubaga loodud müügiridadel aastane sagedus.) Müügitellimuse seostamiseks olemasoleva arveldusgraafikuga valige väärtus väljal **Arveldusgraafiku** number.
5. Toe või uuendamise alguskuupäeva muutmiseks seadke alistamise **alguskuupäeva suvandiks** **Jah**.
6. Tugiüksuse lisamiseks või redigeerimiseks märkige ruut **Tugi** ja sisestage seejärel tugiüksus **väljale Tugiüksus**. Kaup lisatakse müügitellimusele.
7. Uuendamisüksuse lisamiseks või redigeerimiseks märkige ruut **Uuenda** ja sisestage seejärel uuendatav kaup väljale Uuendatav **kaup**. Müügitellimuse arveldamisel luuakse kaubaga seotud arveldusgraafik.
8. Valige nupp **OK**.
9. Valige vahekaardil **Loomine** suvand **Arve**. Kui müügitellimus on sisestatud, luuakse arveldusgraafik. Sõnumi üksikasjades kuvatakse teatis, mis sisaldab arveldusgraafiku teavet.
10. Valige kõikide **/aktiivsete arveldusgraafikute** loendilehel arveldusgraafiku number **, et üle vaadata arveldusgraafikute üksikasju arveldusgraafikute** lehel.
11. Valige arveldusgraafiku **ridade** kiirkaardil **Tugi ja uuendamine**, et vaadata üle loodud ridade üksikasjad.

> [!NOTE]
> Kui tuleb muuta arveldusgraafiku rea uuendamise alguskuupäeva, **·** **saate redigeerida arveldusgraafikute lehel oleva rea alguskuupäeva** väärtust. Kui avate **rea arvelduse** üksikasjade lehe, uuendatakse **arvelduse** alguskuupäeva väli uue kuupäevaga. Arvelduse **lõppkuupäeva** väärtus arvutatakse ümber arveldussageduse põhjal. Uuendamise alguskuupäeva saab värskendada ainult siis, kui uuendamise arveldusgraafiku esimest arvet pole loodud ja sisestatud. Pärast esimese arve loomist ja sisestamist ei saa alguskuupäeva redigeerida.

Tugi- ja uuendamisprotsess on saadaval ainult müügitellimuse jaoks. Kui lisate müügitellimusele toe ja uuendate kaupu, saate luua uue arveldusgraafiku või lisada uuendamiskauba olemasolevasse arveldusgraafikusse.

## <a name="support-and-renewal-audit"></a>Toe ja uuendamise audit

Auditi lehel **Toe ja** uuendamisel saate üle vaadata arveldusgraafiku ridade üksikasjad, mis on loodud müügitellimusel kauba uuendamisest. See suvand on saadaval, kui arveldusgraafiku rea kaup on uuendamisüksus.

Arveldusgraafiku rea toe ja uuenduse teabe redigeerimiseks järgige neid samme.

1. Valige lehel **Kõik arveldusgraafikud** arveldusgraafiku number.
2. Valige jaotises **Arveldusgraafiku read** rida ning seejärel valige tugi ja **uuendamine**.
3. Vaadake üle kogu toe- või uuendamisüksuse teave.
4. Tehke vajalikud muudatused tugitasemel või uuendamise protsendil või summal ja seejärel sisestage väärtus **väljale Muutmise** põhjus.
5. Valige **protsess**.

### <a name="fields"></a>Väljad

Auditi **lehe Tugi ja uuendamine** sisaldab järgmisi välju.

| Väli | Kirjeldus |
|-------|-------------|
| Kaubakood | Arveldusgraafiku rea kaubakood. |
| Toote nimi | Toote nimetus |
| Toetusplaani tase | Vaadake või muutke uuendamisüksuse tugitaset. |
| Uuendamisprotsent | Sisestage uuendamisprotsent, mida kasutatakse ühiku hinna arvutamisel uuendamiskauba jaoks arveldusgraafikus. |
| Uuendamise summa | Sisestage uuendatav summa, mida kasutatakse, kui ühiku hind arvutatakse uuendatava kauba jaoks arveldusgraafikus. |
| Muutmise põhjus | Sisestage toe muutmise ja uuendamise teabe muutmise põhjus. Uuendamise protsendi, uuendatava summa või tugiplaani **taseme** **väärtuse muutmisel** **peate sisestama põhjuse**. |
| Algne müügikaup | Algne müügikauba kood müügitellimusest. |
| Algne netosumma | Kauba algne netosumma. |
| Algne toe tase | Kauba algne tugitase. |
| Algne uuendamise protsent | Kauba algne uuendamisprotsent. |
| Algne uuendamise summa | Kauba uuendamise algne summa. |
| **Tabel** | |
| Algne toe tase | Eelmine tugitase |
| Algne uuendamise protsent | Eelmine uuendamisprotsent |
| Algne uuendamise summa | Eelmine uuendamise summa |
| Muutja | Muudatuse teinud kasutaja kasutajanimi. |
| Muutmise kuupäev ja kellaaeg | Kuupäev, mil muudatus toimus |
| Põhjus | Muutmise põhjus. |
