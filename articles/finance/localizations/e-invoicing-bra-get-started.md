---
title: Alustage elektroonilise arveldusega Brasiilias
description: See artikkel annab teavet, mis aitab teil alustada elektroonilise arveldusega Brasiilia jaoks finantside ja tarneahela halduses.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8c540daca852a8197841957c1d6d3e5c7892ce4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279930"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Alustage elektroonilise arveldusega Brasiilias 

[!include [banner](../includes/banner.md)]

See artikkel annab teavet, mis aitab teil Alustada Brasiilia elektroonilise arveldusega. Artikkel juhendab teid läbi konfiguratsioonietappide, mis sõltuvad regulatiivsetest konfiguratsiooniteenustest (RCS) ja täiendab artikli kirjeldatud samme, [alustage elektroonilise arveldamise abil](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Brasiilia NF-e (BR) elektroonilise arveldamise funktsiooni riigispetsiifiline konfiguratsioon

Mõned parameetrid **Brasiilia NF-e (BR) Elektroonilise arvelduse funktsioonist** avaldatakse vaikeväärtustega. Vaadake üle ja vajadusel uuendage väärtusi, et need sobiksid paremini teie äritegevuse vajadustega, enne kui juurutate elektroonilise arveldamise funktsiooni teenuse keskkonda.

See jaotis täiendab artikli **elektroonilise arvelduse funktsiooni** jaotise riigiomast konfiguratsiooni. [Alustage elektroonilise arveldusega](e-invoicing-get-started.md).

1. RCS-i jaotises **Funktsioonid** tööruumis **Globaliseerimisfunktsioonid** valige paan **Elektrooniline arveldus** .
2. Lehel **Elektroonilise arveldamise Funktsioonid** veenduge, et **Brasiilia NF-e (BR)** on valitud loodud elektroonilise arveldamise funktsioon.
3. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
4. Vahekaardil **Häälestus** ruudustikus valige **Edasta** ja siis valige **Redigeeri.**
5. Valige **Tegevused** vahekaardil **Tegevused** väljagrupis **(Eelvaade) Allkirjasta XML-dokument** tegevus.
6. Väljagrupis **Parameetrid** valige **Serdi nimi** ja **Väärtus** väljal sisestage parameetriga seostatud serdi nimi.
7. Valige **Tegevused** vahekaardil **Tegevused** väljagrupis **(Eelvaade) Kutsu Brasiilia SEAFAZ teenus** tegevus.
8. Väljagrupis **Parameetrid** valige **URL-aadressi** parameeter.
9. Vajadusel vaadake välja **Väärtus** läbi ja uuendage oma osariigi jaoks SEFAZ-dokumentatsioonis avaldatud veebiteenuste URL-i ja valige seejärel suvand **Salvesta.**
10. Vahekaardil **Kohaldatavusreeglid** väljagrupis **kohaldatavusreegli seadistamine** vaadake läbi ja uuendage **Osariigi** välja kriteeriume nii, nagu on vaja sama osariigi puhul, millele veebiteenuste URL-is viidatakse.
11. Valige **Salvesta** ja sulgege leht.
12. Elektroonilise arveldamise funktsiooni juurutamiseks Teenusse keskkonda vt [Alustage elektroonilise arvelduse lisandmooduliga](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Brasiilia NF-e (BR) elektroonilise arveldamise funktsiooni riigispetsiifiline konfiguratsioon

Viige need sammud lõpule enne rakenduse häälestuse juurutamist ühendatud finants- või Supply Chain Management rakendusse.

See jaotis täiendab artikli **jaotise Rakenduse häälestuse riigispetsiifilist** konfiguratsiooni Alustage [elektroonilise arveldusega](e-invoicing-get-started.md).

1. RCS-i jaotises **Funktsioonid** tööruumis **Globaliseerimisfunktsioonid** valige paan **Elektrooniline arveldus** .
2. Lehel **Elektroonilise arveldamise Funktsioonid** veenduge, et **Brasiilia NF-e (BR)** on valitud loodud elektroonilise arveldamise funktsioon.
3. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
4. Vahekaardil **Seadistused** valige **rakenduse häälestus** ja **Ühendatud rakendus** väljal, valige rakendus, kuhu soovite juurutada.
5. Väljal **Tabeli nimi** kontrollige, kas valitud on suvand **Finantsdokumendi päis**.
6. Valige **Vastuse tüübid** ja seejärel **Uus**.
7. Väljale **Vastuse tüüp** sisestage "Vastus" fikseeritud väärtusena ja **Kirjeldus** väljale sisestage "Kirjeldus".
8. Valige väljal **Edastuse olek** suvand **Ootel**.
9. Väljal **Mudeli kaardistamine** valige **Mudeli vastendamine vastusesõnumist** koos **(Eelvaade) Vastuse sõnumi impordivorming** ja siis valige **Salvesta**.
10. Valige **Uus** ja **Vastuse tüüp** väljal sisestage "Vastus" fikseeritud väärtusena ja **Kirjeldus** väljale sisestage "Kirjeldus".
11. Valige väljal **Edastuse olek** suvand **Ootel**.
12. Väljal **Mudeli kaardistamine** valige **Mudeli vastendamine vastusesõnumist** koos **(Eelvaade) NF-e vastuse andmed impordivorming (BR)** ja siis valige **Salvesta**.
13. Rakenduse häälestuse juurutamiseks finants- või tarneahelaga seotud rakendusse vt [Alustamine elektroonilise arveldamisega](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Brasiilia NF-e (BR) elektroonilise arveldamise funktsiooni riigispetsiifiline konfiguratsioon

Mõned parameetrid **Brasiilia NFS-e ABRASF Curitiba (BR) Elektroonilise arvelduse funktsioonist** avaldatakse vaikeväärtustega. Vaadake üle ja vajadusel uuendage väärtusi, et need sobiksid paremini teie äritegevuse vajadustega, enne kui juurutate elektroonilise arveldamise funktsiooni teenuse keskkonda.

See jaotis täiendab artikli **elektroonilise arvelduse funktsiooni** jaotise riigiomast konfiguratsiooni. [Alustage elektroonilise arveldusega](e-invoicing-get-started.md).

1. RCS-i jaotises **Funktsioonid** tööruumis **Globaliseerimisfunktsioonid** valige paan **Elektrooniline arveldus** .
2. Lehel **Elektroonilise arveldamise funktsioonid** veenduge, et **Brasiilia NFS-e ABRASF Curitiba (BR)** on valitud loodud elektroonilise arveldamise funktsioon.
3. Vahekaardil **Versioonid** kontrollige, et **Mustand** versioon on valitud ja vahekaardil **Häälestus** valige suvand **Edasta**.
4. Valige **Redigeeri** ja vahekaardil **Tegevused** väljagrupist **Tegevused**, valige **(Eelvaade) Allkirjasta xml dokuemnt**.
5. Väljagrupis **Parameetrid** valige **Serdi nimi**.
6. Sisestage **Väärtus** väljale oma võtmehoidla parameetriga seostatud serdi nimi.
7. Valige **Tegevused** väljagrupis teine esinemiskord **(Eelvaade) Allkirjastaxml-dokument**.
8. Väljagrupis **Parameetrid** valige **Serdi nimi**.
9. Sisestage **Väärtus** väljale oma võtmehoidla parameetriga seostatud serdi nimi.
10. Valige **Tegevused** vahekaardil **Tegevused** väljagrupis **(Eelvaade) Kutsu Brasiilia SEAFAZ teenus** tegevus.
11. Väljagrupis **Parameetrid** valige **URL-aadressi** parameeter.
12. Väljal **Väärtus** vaadake vajadusel läbi ja uuendage maksuameti avaldatud veebiteenuste URL-i ja valige seejärel suvand **Salvesta.**
13. Vahekaardil **Häälestus** ruudustikus valige **Päring** ja siis valige **Redigeeri.**
14. Valige **Tegevused** vahekaardil **Tegevused** väljagrupis **(Eelvaade) Kutsu Brasiilia SEAFAZ teenus** tegevus.
15. Väljagrupis **Parameetrid** valige **URL-aadressi** parameeter.
16. Väljal **Väärtus** vaadake vajadusel läbi ja uuendage maksuameti avaldatud veebiteenuste URL.
17. Valige **Salvesta** ja sulgege seejärel leht.
18. Elektroonilise arveldamise funktsiooni juurutamiseks Teenusse keskkonda vt [Alustage elektroonilise arvelduse lisandmooduliga](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Brasiilia NFS-e ABRASF Curitibia (BR) elektroonilise arveldamise funktsiooni riigispetsiifiline konfiguratsioon

Viige need sammud lõpule enne rakenduse häälestuse juurutamist ühendatud finants- või Supply Chain Management rakendusse.

See jaotis täiendab artikli **rakenduse häälestuse jaotise** riigiomast konfiguratsiooni Ja [alustage elektroonilise arveldamisega](e-invoicing-get-started.md).

1. RCS-i jaotises **Funktsioonid** tööruumis **Globaliseerimisfunktsioonid** valige paan **Elektrooniline arveldus** .
2. Lehel **Elektroonilise arveldamise Funktsioonid** veenduge, et **Brasiilia NFS-e ABRASF (BR)** on valitud loodud elektroonilise arveldamise funktsioon.
3. Vahekaardil **Versioonid** kontrollige, et **Mustand** versioon on valitud ja vahekaardil **Häälestused** valige suvand **Rakenduse häälestus**.
4. Väljal **Ühendatud rakendus** valige rakendus, mida soovite juurutada.
5. Väljal **Tabeli nimi** kontrollige, kas valitud on suvand Finantsdokumendi päis.
6. Valige **Vastuse tüübid** ja seejärel **Uus**.
7. Väljale **Vastuse tüüp** sisestage "Vastus" fikseeritud väärtusena" ja **Kirjeldus** väljale sisestage "Kirjeldus".
8. Valige väljal **Edastuse olek** suvand **Ootel**.
9. Väljal **Mudeli kaardistamine** valige **Mudeli vastendamine vastusesõnumist** koos **(Eelvaade) NFS-e ABRASF vastuse andmed impordivorming (BR)** ja siis valige **Salvesta**.
10. Valige **Uus** ja **Vastuse tüüp** väljal sisestage "Vastus" fikseeritud väärtusena ja **Kirjeldus** väljale sisestage "Kirjeldus".
11. Valige väljal **Edastuse olek** suvand **Ootel**.
12. Väljal **Mudeli kaardistamine** valige **Mudeli andmete import** koos **(Eelvaade) NFS-e ABRASF vastuse andmete impordivorming (BR)** ja siis valige **Salvesta**.
13. Valige **Uus** ja **Vastuse tüüp** väljal sisestage "Vastus fikseeritud väärtusena ja **Kirjeldus** väljale sisestage "Kirjeldus".
14. Valige väljal **Edastuse olek** suvand **Ootel**.
15. Väljal **Mudeli kaardistamine** valige **Mudeli vastendamine vastusesõnumist** koos **(Eelvaade) NFS-e ABRASF vastuse andmed impordivorming (BR).**
16. Valige **Salvesta** ja sulgege leht.
17. Rakenduse häälestuse juurutamiseks finants- või tarneahelaga seotud rakendusse vt [Alustamine elektroonilise arveldamisega](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Privaatsusavaldus
Funktsioonide **NF-e Federal - Brasiilia elektroonilise arve (BR)** ja **NFS-e - Brasiilia teenuse (linn) elektroonilise arve** lubamine võib nõuda piiratud andmete saatmist, sealhulgas organisatsiooni maksu registreerimise ID-d. See info edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata maksuametile elektroonilisi arveid eelmääratletud vormingus, mis on vajalik integratsiooniks valitsuse veebiteenusega. Administraatorina saate lubada või lülitada välja **NF-e Federal - Brasiilia elektroonilise arve(BR)** ja **NFS-e - Brasiilia teenuse (city) elektroonilise arve** funktsioonid. Selleks läbige järgmised sammud: 

1. Avage **Organisatsiooni halduses** > **Seadistus** > **Elektroonilise dokumendi parameetrid**. 
2. Valige **Funktsioonid** vahekaardil rida, mis sisaldab **NF-e Föderaalset - Brasiilia elektroonilist arvet (BR)** või **NFS-e - Brasiilia teenuse (linn) elektroonilise arve** funktsiooni ja valige funktsioon.. Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli teenusehalduse kasutamise alustamine](e-invoicing-get-started-service-administration.md)
- [Elektroonilise arveldusega alustamine](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
