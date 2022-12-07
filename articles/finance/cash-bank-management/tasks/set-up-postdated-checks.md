---
title: Hilisema kuupäevaga tšekkide häälestus
description: See artikkel selgitab, kuidas määrata, kas sisestada töölehe sisestused pärast kuupäevaga tšekkide jaoks ja millist töölehte kasutada kliiringukirjete ja hankijamaksete jaoks.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5ef9aa6b67eb630713dd1f15b2ae49c358edae9
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804178"
---
# <a name="set-up-postdated-checks"></a>Hilisema kuupäevaga tšekkide häälestus

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas määrata, kas sisestada töölehe sisestused pärast kuupäevaga tšekkide jaoks ja millist töölehte kasutada kliiringukirjete ja hankijamaksete jaoks. Samuti saate määrata kliiringukontod väljastatud tšekkidele, vastuvõetud tšekkidele ja kinnipeetavatele maksudele. Hilisema kuupäevaga dateeritud tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemiseks ja vastuvõtmiseks. Saate määrata, kas tšekk peab kajastuma raamatupidamises enne selle lõpptähtaega.



Selle protseduuri roll on Kassiir. See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="set-up-postdated-checks"></a>Hilisema kuupäevaga tšekkide seadistamine
1. Avage sularaha **- ja > halduse > parameetrid**.
2. Klõpsake vahekaardile **Järelndekseeritud tšekid** .
3. Märkige või tühjendage ruut **Luba pärast seda aegunud** tšekid.
4. Märkige või tühjendage **ruut Sisesta töölehe kirjed aegunud tšekkide** jaoks.
5. Määrake väljal **Kliiringukonto väljastatud** tšekkide jaoks soovitud väärtused.
6. Määrake väljal **Kliiringukonto vastuvõetud tšekkide** jaoks soovitud väärtused.
7. Väljale Peatööleht **kliiringukirjete** jaoks tippige väärtus.
8. Sisestage **väärtus väljale Kandud üle sellele hankija maksetöölehele** .
9. Määrake väljal **Kinnipeetava maksu kliiringukonto** soovitud väärtused.
10. Klõpsake nuppu **Salvesta**.
11. Sulgege leht.
12. Minge > **ostureskontro > seadistuse makseviiside kohta**.
13. Klõpsake valikut **Uus**.
14. Väljale **Makseviis** sisestage väärtus.
15. Valige järeldindeeritud **tšekkide tühjendamise sisestamise** suvand, et näidata tšeki summa sisestamist kliiringukontole.
16.  **Väljal Konto tüüp** valige **pank**.
    * Maksemeetodi vastaskonto on pank.  
17.  **Määrake väljal Maksekonto** soovitud väärtused.
    * Valige pangakonto, mida kasutatakse arvesumma mahaarvamiseks.  
18. Klõpsake nuppu **Salvesta**.
19. Sulgege leht.
> [!NOTE]
> Et saada pärast kuupäevaga dateeritud tšekki pangakontole sisestada, kui seansi kuupäev on tähtajakuupäevast suurem või sellega võrdne, peate lubama funktsiooni **Tähtaja kuupäeva kinnitamise maksetöölehe sisestamisel kuupäevaga dateeritud tšekkide** pangakontole. See funktsioon võimaldab teil sisestada maksetöölehti hankijatele või klientidele, kellel on dateeritud tšekid, kui seansi kuupäev on tähtaja kuupäevast suurem või sellega võrdne.
> 
> Kui seadistate **makseviisi**  (Ostureskontro **> Makse seadistus >** makseviisid), **ärge täitke bridging-kontot**. Sel juhul sisestatakse vastaskonto pangakontole, mis on seadistatud **Makseviis**.
>  
> Kui funktsioon on lubatud ja seansi kuupäev on tähtajast väiksem, kuvatakse maksetöölehe sisestamisel järgmine tõrketeade, et tähtaja kuupäev peab olema seansi kuupäevast väiksem või sellega võrdne, **kui vastaskonto tüüp on Pank**. Kui see funktsioon pole lubatud, saate sisestada maksetöölehe dateeritud tšekiga, kui seansi kuupäev on tähtaja kuupäevast väiksem.
> See funktsioon on saadaval rakenduses versioonis 10.0.21 ja uuemas.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
