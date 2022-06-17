---
title: Finantstöölehtede vaikefinantsdimensioonid
description: Selles artiklis kirjeldatakse reegleid, mis määratlevad finantsdimensiooni väärtuste seadistamise finantstöölehtede kaudu sisestatud kannetele. See sisaldab ka fikseeritud dimensioonide kasutamisel kasutatavate stsenaariumide üksikasju.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d0fcf836e22207baae562801fb082d735df0f96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907918"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Finantstöölehtede vaikefinantsdimensioonid

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse reegleid, mis määratlevad finantsdimensiooni väärtuste seadistamise finantstöölehtede kaudu (kuid mitte varude töölehtede või projektitöölehtede kaudu) sisestatud kannetele. See sisaldab ka fikseeritud dimensioonide kasutamisel kasutatavate stsenaariumide üksikasju.

## <a name="symptom"></a>Sümptom

Finantsdimensiooni väärtused pole finantstöölehe kontol või vastaskontol määratud oodatult. Järgmised stsenaariumid on kaks näidet:

Kanne sisestatakse üldtöölehele. Konto on hankija konto ja vastaskonto on pangakonto. Hankija finantsdimensioonid sisestatakse kontole vaikimisi, kuid panga finantsdimensioone ei sisestata vaikimisi vastaskontole. Selle asemel sisestatakse konto dimensiooniväärtused vaikimisi vastaskontole.

Kliendile on määratud finantsdimensiooni vaikeväärtused ja tulu põhikontol on osakonna finantsdimensiooni jaoks määratud fikseeritud dimensiooniväärtus. Kanne sisestatakse üldtöölehele.  Konto on klient ja Vastaskonto on pearaamatukonto, täpsemalt fikseeritud dimensiooniväärtusega tulukonto. Tulu põhikonto vastaskontole pole määratud fikseeritud dimensiooni. Selle asemel määratakse sellele kliendilt saadud konto osakonna dimensiooniväärtus.  Pärast kande sisestamist kasutatakse fikseeritud dimensiooniväärtust sisestatud raamatupidamiskandes, kuid kandes kuvatakse tulukontol siiski kliendi osakonna väärtus. 

Milliseid reegleid järgitakse töölehe kannetel seatud finantsdimensiooni väärtuste puhul?

## <a name="resolution"></a>Lahendus

Finantsdimensiooni väärtuste sisestamisel vaikimisi finantstöölehtede kande ridadele (nt üldtöölehele või hankija arve töölehele) järgitakse järgmisi reegleid. 

1. **Töölehe päis**

   - Töölehe päise dimensioonid sisestatakse vaikimisi töölehe nime dimensioonidest.

2. **Tööleherea konto**

   - Tööleherea konto dimensioonid sisestatakse vaikimisi töölehe päise dimensioonidest.
   - Kui mõni finantsdimensioon on tühi, sisestatakse nende väärtused vaikimisi kliendi, hankija, panga, põhivara, projekti või pearaamatu dimensioonidelt.

     - Kui konto tüübiks on **Pearaamat**, koheldakse pearaamatukonto fikseeritud dimensiooni kande sisestamisel vaikedimensioonina.
     - Kui konto tüübiks on **Klient**, **Hankija**, **Pank**, **Põhivarad** või **Projekt**, ei saa põhikontot veel määratleda. Seetõttu ei sisestata kontole kunagi vaikimisi fikseeritud dimensiooni.

3. **Tööleherea vastaskonto**

 - Esmalt sisestatakse tööleherea Vastaskonto dimensioonid vaikimisi tööleherea Konto dimensioonidest.

 - Kui mõni finantsdimensioon on tühi, tuleb järgmine vaikekirje kliendi, hankija, panga, põhivara, projekti või pearaamatu vaikedimensioonidelt.
   1. Kui vastaskonto tüübiks on **Pearaamat**, koheldakse pearaamatukonto fikseeritud dimensiooni kande sisestamisel vaikedimensioonina. Kui dimensiooniväärtus on kontolt juba vaikimisi sisestatud, ei alista põhikonto vaike- või fikseeritud dimensiooniväärtus olemasolevat väärtust.
   2. Kui vastaskonto tüüp on **Klient**, **Hankija**, **Pank**, **Põhivarad** või **Projekt**, ei ole põhikonto veel teada, seega ei saa fikseeritud dimensioon kunagi vastaskonto vaikeväärtust.

4. **Sisestamine**

    1. Sisestamise ajal hinnatakse (nii konto kui ka vastaskonto) raamatupidamiskirje iga rea põhikontot määramaks, kas fikseeritud dimensiooni väärtus on olemas. Kui fikseeritud dimensioon on määratletud, asendatakse selle fikseeritud dimensiooni väärtusega mis tahes olemasolevad või tühjad väärtused.

        Fikseeritud dimensiooniväärtust **ei** kuvata tööleheridadel pärast sisestamist. Selle asemel kuvatakse see raamatupidamiskirjel, kui vaatate kannet pärast selle sisestamist.

    2. Sisestamisel ei sisestata vaikimisi ühtegi muud dimensiooniväärtust, sealhulgas pearaamatu lisakontod, mis võidakse lisada sisestamisel, nt sendiümarduskontod ja kontsernisisesed algus- ning lõpptähtajaga kontod. Pearaamatu lisakontode dimensiooni vaikekirjed võetakse kontolt või vastaskontodelt.

Dimensiooniväärtuste vaikimisi sisestamise eesmärgil ei saa töölehe vaikeprotsess määrata, kas tühi dimensiooniväärtus on tahtlikult tühjaks jäetud või kas vaikesisestust ei tehtud. Kui dimensiooniväärtus on tahtlikult tühjaks jäetud, võib varem kirjeldatud vaikejärjestust kasutades vaikimisi väärtuse sisestada. Kui vajate tühja väärtusega dimensiooni, peate võib olla looma dimensiooni, mille väärtus on **0** (null) või **Tühi**, et seda saaks kasutada tühja dimensiooni asemel.

Järgmistest stsenaariumidest leiate näiteid finantsdimensiooni vaikejärjestuse kohta.

### <a name="scenario-1"></a>1. stsenaarium

Avage **Pearaamat \> Töölehe seadistamine \> Töölehenimed** ja valige töölehenimi **GenJrn**. Seejärel määratlege kiirkaardil **Finantsdimensioonid** vaikefinantsdimensioonide jaoks järgmised väärtused:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Töölehenimede leht](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Avage **Pearaamat \> Töölehe kirjed \> Üldtööleht** ja looge uus üldtööleht, mis kasutab töölehenime **GenJrn**. Dimensioonid sisestatakse vaikimisi töölehenimest (tabel LedgerJournalName) töölehepäisesse (tabel LedgerJournalTable), nagu näidatud vahekaardil **Finantsdimensioonid**.

[![Vahekaart Finantsdimensioonid üldtöölehtede lehel](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Avage tööleht **Read**. Valige väljal **Konto tüüp** üksus **Pearaamat** ja seejärel sisestage väljale **Konto** väärtus **170150**. Seejärel valige **tabeldusklahv** väljalt teisaldamiseks. Dimensioonid sisestatakse vaikimisi töölehepäisest. Seetõttu kuvatakse **Konto** väärtusena **170150-001-024**.

[![Üldtöölehe tööleheread töölehe kande lehel](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Seadke **Konto** väärtuseks **170150-001-023**. Sisestage deebetsumma või kreeditsumma. Valige väljal **Vastaskonto tüüp** üksus **Pearaamat** ja seejärel sisestage väljale **Vastaskonto** väärtus **600150**. Dimensiooniväärtused sisestatakse vaikimisi kontolt. Seetõttu kuvatakse **Vastaskonto** väärtusena **600150-001-023**.

### <a name="scenario-2"></a>2. stsenaarium

Kasutage samu finantsdimensioone, mille määratlesite töölehenimele 1. stsenaariumis. Järgmisena valige **Müügireskontro \> Kliendid \> Kõik kliendid** ja määratlege kliendi US-001 jaoks finantsdimensiooni vaikeväärtused. Valige klient, et avada kliendi üksikasjad. Säilitage vahekaardil **Finantsdimensioonid** dimensiooni **BUSINESSUNIT** vaikeväärtus (**001**). Lisage dimensioon **COSTCENTER** ja sisestage väärtuseks **007**.

Looge uus üldtööleht, mis kasutab töölehenime **GenJrn**. Muutke vahekaardil **Finantsdimensioonid** üksuse **BUSINESSUNIT** vaikeväärtuseks **001** asemel **002**.

Avage tööleht **Read**. Valige väljal **Konto tüüp** üksus **Klient** ja seejärel sisestage väljale **Konto** väärtus **US-001**. Mitte-pearaamatukonto tüüpi finantsdimensioonide vaatamiseks valige **Finantsdimensioonid \> Konto**. Sisestatakse järgmised finantsdimensiooni väärtuste vaikekirjed:

- **BUSINESSUNIT:** 002 – vaikekirje võetakse töölehe päisest. Kliendilt US-001 ei sisestata vaikimisi väärtust **001**, kuna vaikeväärtus on juba sisestatud.
- **COSTCENTER:** 007 – vaikekirje võetakse kliendi US-001 seadistusest.
- **DEPARTMENT:** 024 – vaikekirje võetakse töölehe päisest.

Tagasi real, valige väljal **Vastaskonto tüüp** üksus **Pearaamat** ja seejärel sisestage väljale **Vastaskonto** väärtus **600150**. Reale sisestatakse järgmised finantsdimensiooni väärtuste vaikekirjed:

- **BUSINESSUNIT:** 002 – vaikekirje võetakse konto finantsdimensioonidest. (See sisestati algselt vaikimisi töölehepäisest.)
- **DEPARTMENT:** 024 – vaikekirje võetakse konto finantsdimensioonidest. (See sisestati algselt vaikimisi töölehepäisest.)
- **COSTCENTER:** 007 – vaikekirje võetakse konto finantsdimensioonidest. (See sisestati algselt vaikimisi kliendist.)

### <a name="scenario-3"></a>3. stsenaarium

Lisage samale töölehele, mida kasutasite 2. stsenaariumis, uus rida. Valige väljal **Konto tüüp** üksus **Pearaamat** ja seejärel sisestage väljale **Konto** väärtus **170150**. Tühjendage dimensiooni vaikeväärtused, et alles jääks ainult põhikonto 170150. Valige väljal **Vastaskonto tüüp** üksus **Klient** ja seejärel sisestage väljale **Vastaskonto** väärtus **US-001**. Sisestatakse järgmised finantsdimensiooni väärtuste vaikekirjed:

- **BUSINESSUNIT:** 002 – vaikekirje võetakse töölehe päisest, sest konto dimensiooni väärtus on tühi. Kliendilt US-001 ei sisestata vaikimisi väärtust **001**, kuna vaikeväärtus võeti juba töölehe päisest. Kui üksuse **BUSINESSUNIT** väärtus jäeti tahtlikult tühjaks, peate ka vastaskontolt finantsdimensiooni eemaldama.
- **COSTCENTER:** 007 – vaikekirje võetakse kliendilt US-001, sest konto dimensiooniväärtus ja töölehe päise dimensiooniväärtus on tühjad. Kui üksuse **COSTCENTER** väärtus jäeti tahtlikult tühjaks, peate ka vastaskontolt finantsdimensiooni eemaldama.
- **DEPARTMENT:** 024 – vaikekirje võetakse töölehe päisest, sest konto dimensiooni väärtus on tühi. Kui üksuse **DEPARTMENT** väärtus jäeti tahtlikult tühjaks, peate ka vastaskontolt finantsdimensiooni eemaldama.

### <a name="scenario-4"></a>4. stsenaarium

Kasutage samu finantsdimensiooni vaikeväärtusi, mille määratlesite töölehe nime ja kliendi jaoks 1. ja 2. stsenaariumis. Järgmisena määratlege põhikonto 170150 dimensiooni **BUSINESSUNIT** fikseeritud väärtus. Avage jaotis **Pearaamat \> Kontoplaan \> Kontod \> Põhikontod**. Valige väljal **Põhikonto** väärtus **170150** ja seejärel valige vahekaardil **Juriidilise isik** käsk **Lisa**. Valige juriidiliseks isikuks **USMF** ja seejärel valige käsk **Lisa**. Valige see kirje ja seejärel valige **Vaikedimensioonid**. Muutke dimensiooni **BUSINESSUNIT** väärtuseks **Fikseeritud väärtus** ja sisestage väärtus **003**.

Looge uus üldtööleht, mis kasutab töölehenime **GenJrn**. Eemaldage vahekaardil **Finantsdimensioonid** kõik dimensiooni vaikeväärtused.

Avage tööleht **Read**. Valige väljal **Konto tüüp** üksus **Pearaamat** ja seejärel sisestage väljale **Konto** väärtus **170150**. Seejärel valige **tabeldusklahv** väljalt teisaldamiseks. Dimensiooniväärtused sisestatakse vaikimisi konto 170150 põhikonto seadistusest. Seetõttu kuvatakse **Konto** väärtusena **170150-003-**.

Seadke **Konto** väärtuseks **170150-004-**. **Töölehe funktsioon ei takista fikseeritud dimensiooniväärtuse muutmist.** Sisestage deebetsumma või kreeditsumma. Valige väljal **Vastaskonto tüüp** üksus **Pearaamat** ja seejärel sisestage väljale **Vastaskonto** väärtus **170250**. Finantsdimensiooni väärtus 004 sisestatakse vaikimisi kontolt. Seejärel sisestage dokument. Valige töölehel **Kanne**. Pange tähele, et üksuse **BUSINESSUNIT** väärtus pöördus sisestamise ajal tagasi fikseeritud dimensiooniväärtusele **003**.

Töölehe kandele naasmisel **ei** kajasta dimensioon **BUSINESSUNIT** fikseeritud dimensiooniväärtust. Sellel on alati väärtus, mis kuvati ekraanil enne sisestamist. Sisestusprotsess ei muuda midagi, mis sisestatakse kandesse. Sisestamisel muudetakse ainult raamatupidamiskirjet.

## <a name="developer-notes"></a>Arendaja märkmed

Kui olete arendaja ja soovite vaadata viivitusprotsessi koodi, vaadake üle järgmised meetodid:

- **LedgerJournalEngine.accountModified()** – see meetod on peamine sisestuspunkt esmase konto dimensiooni viivitusprotsessi jaoks, mis on kõigile töölehtedele standardne (ja mille mõned töölehetüübid alistavad).
- **LedgerJournalEngine.offsetAccountModified()** – see meetod on vastaskonto dimensiooni viivitusprotsessi peamine sisestuspunkt.
