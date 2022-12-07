---
title: Asünkroonsed tellimuse sünkroonimise probleemid
description: See artikkel kirjeldab asünkroonse tellimuse loomise Microsoft Dynamics 365 Commerce tõrke tava põhjuseid ja annab tõrkeotsingu samme, et aidata süsteemi kasutajatel ja partneritel mõista, mis läks valesti.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815752"
---
# <a name="asynchronous-order-synchronization-issues"></a>Asünkroonsed tellimuse sünkroonimise probleemid

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab asünkroonse tellimuse loomise Microsoft Dynamics 365 Commerce tõrke tava põhjuseid ja annab tõrkeotsingu samme, et aidata süsteemi kasutajatel ja partneritel mõista, mis läks valesti.

## <a name="symptom"></a>Sümptom

E-kaubandusest või kassast Dynamics 365 Commerce loodud asünkroonsed tellimused ei kajastu commerce headquartersis.

## <a name="troubleshooting"></a>Tõrkeotsing

Tellimuse loomine võib peakontoris nurjuda erinevatel põhjustel, sõltuvalt etapist, mille jooksul tellimuse loomise protsess nurjub. Järgmised tõrkeotsingu sammud läbivad võimalikud juurpõhjused.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Kinnitage, et asünkroonse tellimusega seotud kanne on jõudnud peakontorisse

E-commerce’i tellimuste peakontoris minge jaemüügi ja äri päringute **\> ja aruannete võrgupoe \> kannetele**. Kui teil on tellimuse kinnitusnumber, filtreerige kanded, sisestades kinnitusnumbri kanali **viite ID väljale** . Kui teil ei ole kinnitusnumbrit, filtreerige kanded kliendi kontonumbri sisestamisega.

Müügikoha tellimuste puhul avage kaupluse **kannete leht** ja filtreerige kirjed kviitungi numbri või kliendi kontonumbri järgi. Kui kannet ei leita, käitage **P-0001** kanali kannete töö, mis sünkroonib kanded kanalist peakontorisse. Kui töö **P-0001** ebaõnnestub, avage töö nurjumise tugipilet. Kui töö **P-0001** on edukas, kuid kandeid peakontoris siiski ei kuvata, avage vastava teabega tugipilet.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Kontrollige sünkroonimise olekut, kui kanne on peakontoris olemas, kuid pole müügitellimusega lingitud.

Kui kanne on peakontoris olemas, kuid müügitellimust pole loodud, **avage võrgupoe kannete**  **leht ja valige sünkroonimise oleku** kiirkaart. Kui tellimuste **sünkroonimise töö** proovis seda kannet sünkroonida, **peaks** ootel tellimuse oleku väljal olema olek **Õnnestus** või **Nurjus**. Kui olek on **Õnnestunud**, peab sellel kandel olema müügitellimuse väli. Kui olek on **Nurjunud**, saate vaadata tõrke üksikasju **väljal Tellimuse tõrke üksikasjad** sünkroonimise oleku **kiirkaardil** . Kui kumbki neist olekutest ei kuvata, pole kande töötlemiseks katset tehtud. Sellisel juhul saate sünkroonimistöö **käivitamiseks** valida lehe ülaosas valiku Sünkrooni tellimus.

Veenduge, et **tellimuste sünkroonimise** tööd plaanitakse perioodiliselt käitada, et saaks luua asünkroonseid kandeid peakontoris tellimustena.

Järgmised jaotised annavad teavet mõne tavalise tõrke ja nende pakutud paranduste kohta.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Tellimuse tõrke üksikasjade väljal kuvatakse järgmine tõrketeade: "Numbriseeria on ületatud"

Numbriseeriaid kasutatakse müügitellimuste loomiseks peakontoris. Kui kõik numbriseeria jaoks lubatud numbrid on järjestatud, loob süsteem selle tõrketeate. Müügitellimuste loomiseks kasutatava numbriseeria leiate **müügireskontro parameetritest \> Numbriseeriad \> Müügitellimus**. Tõrke lahendamiseks parandage olemasolev numbriseeria või asendage see uue numbriseeriaga.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Tellimuse tõrke üksikasjade väljal kuvatakse järgmine tõrketeade: "Krediitkaarditehingute töötlemiseks peab olema vaikemakseteenus".

Vea parandamiseks kinnitage, et vaikemakse on peakontoris määratletud. Kui vaikemakset ei ole määratletud, peate selle määratlema. Minge müügireskontro **\> makse seadistuse \>** makseteenustesse **·**  **ja** veenduge, et uute krediitkaartide suvandi Vaikeprotsessor on seadistatud valikule Jah ühe makseteenuse puhul.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Väli Tellimuse tõrke üksikasjad näitab konto struktuuri tõrketeadet

Konto struktuuri tõrketeate tekst võib varieeruda, nagu järgnevad näited näitavad. Kuid tõrgetel on ühine juurpõhjus, mis on seotud konto struktuuri konfiguratsiooniga.

- "Töölehe partiinumbri 0009656328 kande ARP-000959899 1,00 kande puhul ARP-000959899 ettevõttes usrt sisestatakse üle- või alamaksena"
- "Töölehe partiinumbri 0009656328 sisestustulemused ARP-000959899 kande ARP-000959901 struktuuri jaoks kombinatsiooni 618160 puhul ei kehti pearaamatu ettevõtte ühiskasutuses põhikontole.
- "Töölehe partiinumbri sisestustulemused 0009656328 kande ARP-000959899 kande ARP-000959901 esitatud ettevõttekontodelt usrt"
- "Sisestamise tulemused töölehe partiinumbri 0009656328 Kande ARP-000959899 sisestamine on tühistatud"
    
Tõrgete parandamiseks vaadake konto struktuurid täpsuse üle. Lisateavet vt konto struktuuride [konfigureerimine](/dynamics365/finance/general-ledger/configure-account-structures).
    
Kui viga on parandatud, valige nurjunud **kanne** ja seejärel valige sünkroonimistöö käivitamiseks lehe ülaosas suvand Sünkrooni tellimus.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Muud tõrketüübid, mis võivad nõuda kandeandmete fikseeritudmist

Teist tüüpi vigade parandamiseks, mis võivad nõuda kandeandmete kinnitamist, saate kasutada võimalusi Kannete redigeerimine ja auditeerimine. Lisateavet vt teemast Kannete redigeerimine [ja auditeerimine](../edit-order-trans.md).
