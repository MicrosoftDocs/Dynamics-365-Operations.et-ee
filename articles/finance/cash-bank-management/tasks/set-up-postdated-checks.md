---
title: Hilisema kuupäevaga tšekkide seadistamine
description: Selles teemas selgitatakse, kuidas määrata, kas sisestada hilisema kuupäevaga dateeritud tšekkidele töölehe sisestused ja milliseid sisestamise töölehti kliiringukirjete ja hankija maksete puhul kasutada.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc1798836d9b905d991adb4c87d55ddce41d260bdbfdad6bf0c4b4feb846ee57
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743069"
---
# <a name="set-up-postdated-checks"></a>Hilisema kuupäevaga tšekkide seadistamine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas määrata, kas sisestada hilisema kuupäevaga dateeritud tšekkidele töölehe sisestused ja milliseid sisestamise töölehti kliiringukirjete ja hankija maksete puhul kasutada. Samuti saate määrata kliiringukontod väljastatud tšekkidele, vastuvõetud tšekkidele ja kinnipeetavatele maksudele. Hilisema kuupäevaga dateeritud tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemiseks ja vastuvõtmiseks. Saate määrata, kas tšekk peab kajastuma raamatupidamises enne selle lõpptähtaega.



Selle protseduuri roll on Kassiir. See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="set-up-postdated-checks"></a>Hilisema kuupäevaga tšekkide seadistamine
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.
2. Klõpsake vahekaarti Hilisema kuupäevaga dateeritud tšekid.
3. Märkige või tühjendage ruut Luba hilisema kuupäevaga dateeritud tšekid.
4. Märkige või tühjendage ruut Sisesta töölehe kirjed hilisema kuupäevaga dateeritud tšekkide jaoks.
5. Määrake väljal Kliiringukonto väljastatud tšekkide jaoks soovitud väärtused.
6. Määrake väljal Kliiringukonto vastuvõetud tšekkide jaoks soovitud väärtused.
7. Sisestage väärtus väljale Pearaamat kliiringukirjete jaoks.
8. Sisestage väärtus väljale Kanna hilisema kuupäevaga dateeritud tšekid üle selle hankija maksetöölehele.
9. Määrake väljal Kinnipeetava maksu kliiringukonto soovitud väärtused.
10. Klõpsake nuppu Salvesta.
11. Sulgege leht.
12. Avage Ostureskontro > Makse seadistus > Makseviisid.
13. Klõpsake valikut Uus.
14. Sisestage väärtus väljale Makseviis.
15. Märkige ruut Hilisema kuupäevaga dateeritud tšekkide kliiringsisestus näitamaks, et tšeki summa sisestatakse kliiringukontole.
16. Valige väljalt Konto tüüp suvand Pank.
    * Maksemeetodi vastaskonto on pank.  
17. Määrake väljal Maksekonto soovitud väärtused.
    * Valige pangakonto, mida kasutatakse arvesumma mahaarvamiseks.  
18. Klõpsake nuppu Salvesta.
19. Sulgege leht.
> [!NOTE]
> Et saada pärast kuupäevaga dateeritud tšekki pangakontole sisestada, kui seansi kuupäev on tähtajakuupäevast suurem või sellega võrdne, peate lubama funktsiooni **Tähtaja kuupäeva kinnitamise maksetöölehe sisestamisel kuupäevaga dateeritud tšekkide** pangakontole. See funktsioon võimaldab teil sisestada maksetöölehti hankijatele või klientidele, kellel on dateeritud tšekid, kui seansi kuupäev on tähtaja kuupäevast suurem või sellega võrdne.
> 
> Kui seadistate **maksemeetodi** (**Ostureskontro > Makse seadistus > Makseviisid)**, ärge täitke **Ühiskontot**. Sel juhul sisestatakse vastaskonto pangakontole, mis on seadistatud **Makseviis**.
>  
> Kui funktsioon on lubatud ja seansi kuupäev on tähtajast väiksem, kuvatakse maksetöölehe sisestamisel järgmine tõrketeade: "Tähtaja kuupäev peab olema seansi kuupäevast väiksem või sellega võrdne, kui vastaskonto tüüp on Pank". Kui see funktsioon pole lubatud, saate sisestada maksetöölehe dateeritud tšekiga, kui seansi kuupäev on tähtaja kuupäevast väiksem.
> See funktsioon on saadaval rakenduses versioonis 10.0.21 ja uuemas.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
