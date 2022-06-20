---
title: Sisestusprofiilide ülevaade
description: See artikkel selgitab, kuidas sisestusprofiile kasutatakse kogu Microsoft Dynamics 365 rakendustes.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7ef3be13e82ff3722fc81247b5cd581b0b571b0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876120"
---
# <a name="posting-profiles-overview"></a>Sisestusprofiilide ülevaade

Finantside ja toimingute rakendustes kasutatakse termin sisestusprofiile konfiguratsioonide kirjeldamiseks, mis kontrollivad, kuidas alammooduli kontod põhikontodeks teisendatakse, *et* neid saaks kasutada pearaamatusse sisestatud kannetes. Näiteks kontrollivad need, kuidas klient arve sisestamisel müügireskontro põhikontoks teisendatakse.

Mõnedel moodulitel ja funktsioonidel on leht, mis sisaldab nimes sõna "sisestusreeglid" (nt Kliendi **sisestusreeglid või** Hankija **sisestusreeglid**). Lisaks on mõnedel moodulitel mitu valikut pearaamatu sisestamise konfigureerimiseks alammoodulist loodud kannete jaoks. Näiteks moodulis Tootmise **juhtimine** saate seadistada sisestamise tootmisgrupi, ressursi või ressursigrupi järgi.

Pange tähele, et paljude kandetüüpide puhul on sisestusreeglitele alternatiiv: sisestamisdefinitsioonid. Toetatud dokumentide puhul saate kasutada sisestusreeglite asemel sisestamisdefinitsioone, et klassifitseerida raamatupidamiskirjete põhikontosid ja finantsdimensioone. Kui plaanite kasutada pandiõiguseid või eelpandiõiguseid, on raamatupidamiskirjete kontode määratlemiseks vajalik sisestamisdefinitsioon.

Enne, kui saate konfigureerida sisestusprofiile, **sisestamisdefinitsioone** või automaatsete kannete lehte Kontod, peate konfigureerima kontoplaani juriidilise isiku lehel Pearaamat, **mida** soovite konfigureerida.

## <a name="posting-types"></a>Sisestustüübid

Finantside ja toimingute rakendustes kasutatakse sisestustüüpi deebeti või kreediti üldise kategooria määratlemiseks. See kategooria ei sõltu pearaamatu põhikontost. Pearaamatus on sisestustüüpe iga deebeti või kreediti jaoks.

Ühel kandel võib olla üks või mitu sisestustüüpi. Näiteks kandel, mis sisestatakse pearaamatu kaudu, kus konto ja vastaskonto on seadistatud pearaamatusse, **·** **on** pearaamatu töölehe sisestustüüp nii deebeti kui kreediti jaoks. Vastandina on hankija arvel mitu sisestamistüüpi. Need sisestustüübid hõlmavad ühte rida hankija saldo jaoks ja lisaridu vastaskande jaoks, nt Pearaamatu **tööleht**.

Sisestustüüpi saate vaadata lehe **Kande kanded vahekaardi** **Üldine väljal Sisestamistüüp** **.**

> [!TIP]
> Vahekaardi Ülevaade ruudustikku **sisestamise** **tüübi välja lisamiseks** või selle teisaldamiseks saate kasutada tööriistariba **Isikupärastamine**. Sel viisil saate muuta selle välja kannete vaatamise ajal juurdepääsu ja vaatamise lihtsamaks.

## <a name="detail-settings-for-a-posting-profile"></a>Sisestusreegli üksikasjalikud sätted 

Sisestusreeglite konfigureerimisel määratleb **kontokoodi** väli sätte taseme. Saadaval on järgmised valikud: **Tabel**, **Grupp** ja **Kõik**. Vastendamine lõpeb pärast esimest vastet ning tellimus on kõige konkreetsem tase kõige sobivam tase. Kuigi välja **Konto** kood nimi võib mõnel juhul mõneti erineda, jäävad välja käitumine ja funktsioon samaks. Näiteks lao sisestusreeglid sisaldavad kaubakoodi **välja** ja konto **koodi** välja. Mõlema välja väärtused **on Tabel** **·**, Grupp **ja Kõik**.

**Kui** väli Põhikonto on sisestusreegli jaoks tühi ja te pole **konfigureerinud** põhikontot automaatse kande lehe jaoks või mooduliomase või funktsioonipõhise lehekülje jaoks, saate tõrketeate, kui sisestate sisestustüüpi kasutav kanne. Tavaliselt on teateks "Sisestamise tüüpi \[kontot\] ei leitud."

### <a name="table-value"></a>Tabeli väärtus

Väärtus **Tabel** viitab sisestusreegliga seotud koondkirjele. Iga tabelikirje on omane ühele väärtusele. Määratlege see väärtus väljal, mis kuvatakse pärast välja **Konto** kood. Tavaliselt on selle välja nimi Konto või **Konto** **/Grupi number**. Täpne nimi erineb olenevalt lehest, kus see kuvatakse.

Näiteks kui töötate kliendi sisestusreeglitega, **esindab väärtus Tabel** konkreetset klienti. Kui valite väljal Konto kood väärtuse **Tabel, peate väljal Konto/grupi number** valima kliendikoodi **.** **·**

Väärtus **Tabel** esindab kõige konkreetset kirjetüüpi. Süsteem kasutab seda väärtust alati, isegi kui olete konfigureerinud mõne muu kirje, kus **on valitud väärtus Grupp** **või** Kõik. See väärtus alistab ka mis tahes väärtused, mille lõite automaatsete kannete **lehel Kontode vaikeväärtustena**.

Me ei soovita kasutada **tabeli** väärtust sisestusreeglite haldamiseks esmaseks mehhanism, sest andme kvaliteediprobleeme võib esineda siis, kui iga koondandmete kirje kohta säilitatakse eraldi sisestusprofiil. Samuti on raske säilitada ja viia vastavusse eraldi sisestusreeglid iga koondandmete kirje jaoks. Selle asemel tuleks seda väärtust kasutada sisestusreeglite erandite haldamiseks.

### <a name="group-value"></a>Grupi väärtus

Grupi **väärtus** viitab grupeerimiskirjele, mida toetab sisestusreeglitega seotud koondkirje. Iga grupikirje on omane ühele väärtusele. Määratlege see väärtus väljal, mis kuvatakse pärast välja **Konto** kood. Tavaliselt on selle välja nimi Konto või **Konto** **/Grupi number**. Täpne nimi erineb olenevalt lehest, kus see kuvatakse.

Grupi **väärtus** nõuab kõigepealt grupi konfigureerimist ja selle linkimist konto ühe või mitme kirjega. Grupi **väärtus** on väiksem kui tabeli väärtus **,** kuid konkreetsem kui **väärtus** Kõik. Kui tabeli jaoks pole kirjet konfigureeritud, püüab süsteem leida kirjegrupile, kuhu kirje kuulub.

Näiteks **kui** **töötate kliendi sisestusreeglitega ja valite väljal Konto** kood valiku Grupp, **peate valima kliendigrupi väljal Konto/grupi** number. Kliendigrupid tuleb eelnevalt määratleda kliendigrupi **leheküljel** ning kliendi loomisel tuleb kliendigrupid määrata.

Kui peate jälgima antud sisestamistüübi puhul mitut põhikontot, soovitame kasutada väärtust **Grupp**. Näiteks on teil kolm Müügireskontro kaubanduse põhikontot: üks püsiklientidele, üks töötajate jaoks ja teine kontsernisisese müügi jaoks. Sel juhul on soovitatav klientide segmentimiseks luua kolm kliendigruppi. Seejärel vastendage iga kliendigrupp õige põhikontoga kliendi sisestusreeglites. Järgmises tabelis on toodud selle näite kolm kliendigruppi.

| Kliendigrupp | Nimi | Kirjeldus |
|----------------|------|-------------|
| EXT | Väliskliendi | Seda gruppi kasutatakse kõigi standardsete välise poole suunatud klientide puhul. |
| Tühjenda (EMP) | Töövõtjad | Seda gruppi kasutatakse kõigi töötajate puhul, kes ostavad teie organisatsioonist. |
| INT | Kontsernisisene müük | Seda gruppi kasutatakse kõigi kontsernisiseste kliendikontode puhul, mida kasutatakse koos integratsiooni müügi- ja ostutellimustega. |

Seejärel seadistate sisestusreeglites kolm rida. Igal real saate valida grupi **väärtuse** ja seotud põhikonto.

### <a name="all-value"></a>Kogu väärtus

Kogu **väärtus** näitab, et sätted kehtivad kõigile kirjetele. Kui valite **väljal** **Kontokood** väärtuse Kõik, **pole väli Konto/grupi number** saadaval ja te ei saa valida konkreetset kirjet, millega konfiguratsioon rakendada.

Väärtus **Kõik** on kõige vähem spetsiifiline. Seda kasutatakse ainult juhul, kui süsteem ei leia tabeli või **grupi** väärtuse **vastet**. Peaksite valima väärtuse Kõik **,** kui teil on ainult üks põhikonto kindla sisestustüübi jaoks.

Näiteks kliendi sisestusreeglitega töötamisel kehtivad teie poolt määratud põhikontod kõigile teistele klientidele ja kliendigruppidele, kellel ei ole kirjet konkreetse tabeli (klient) või grupi (kliendigrupp) jaoks.

### <a name="category"></a>Kategooria

Lao sisestusprofiilidel on täiendav väärtus, mis on omane müügikategooriale või hankekategooriale. See väärtus sarnaneb väärtusega **Tabel**, sest see rakendub ainult kindlale müügi- või hankekategooriale.

### <a name="default-value"></a>Vaikeväärtus

Kui te ei loo sisestustüübi kirjet sisestusreeglis, **·** **kus** kontokoodi väli on seatud väärtusele Kõik **ja süsteem ei leia sobivat sisestusreegli kirjet Grupi või Tabeli väärtusele, ennisb süsteem vaikeväärtuse, mille saab** **määrata kontode automaatseks kandeleheks.** **·** Lisateavet vt automaatsete kannete [kontodelt](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Kliiringukontod

Kliiringukontot *kasutatakse* sageli raamatupidamises. Microsoft Dynamics Mõned 365-rakenduste sisestustüübid on kliiringukontod. Teiste sõnadega, konto saldo kustutatakse või tühistatakse teise kande sisestamisel. Näiteks kui sisestate ostutellimuse toote sissetuleku, sisestatakse toodete hinnanguliste kulude summa, pluss maks ja ostutellimuse ridade tasud ostu viitvõla sisestamistüübile kohustusena. Hiljem, kui arveldate ostutellimuse, tühistatakse saldo ostu viitvõla sisestamistüübist ja teisaldatakse ostureskontro kaubanduskontole.

## <a name="additional-resources"></a>Lisaressursid

Paljud moodulid rakenduses Dynamics 365 Finance ja neil on sisestusprofiil või lisakonfiguratsioonid, Dynamics 365 Supply Chain Management Dynamics 365 Commerce Dynamics 365 Project Operations mis kontrollivad pearaamatusse sisestamist. Kasutage järgmisi teemasid, et saada lisateavet sisestusreeglite ja sisestusseadistuse kohta igas moodulis:

- [Automaatsete kannete kontod](accounts-for-auto-transactions.md)
- [Ostureskontro – sisestamine](accts-payble-posting.md)
- [Kontodele saab sisestada](accts-recvble-posting.md)
- [Vara rentimise sisestamine](../asset-leasing/set-up-lease-posting-accts.md)
- Varahalduse sisestamine (varsti tulev)
- Sularaha- ja pangahaldus (varsti tulev)
- Valuuta ümberhindamise sisestuskontod (varsti tulev)
- Kuluhalduse sisestamine (varsti tulev)
- [Põhivara sisestusreeglid](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Kontserni raamatupidamise sisestamine (varsti tulev)
- Lao sisestusreeglid (varsti tulev)
- [Väljaminev kulu sisestamine](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Sisestamisdefinitsioonide ülevaade](posting-definitions.md)
- Tootmise juhtimise sisestamine (tuleb varsti)
- Projektihalduse ja raamatupidamise sisestamine (varsti tulev)
- Teenusehalduse sisestamine (varsti tulev)
- Maksu sisestamine (varsti tulev)
- Kellaaja ja kohalviibimise sisestamine (varsti tulev)
- Transpordihalduse sisestamine (tuleb varsti)
- Tagasimaksehalduse sisestusreeglid (varsti tulev)
