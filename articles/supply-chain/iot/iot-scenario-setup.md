---
title: IoT iseõppimisvõime stsenaariumi seadistamine
description: Selles teemas selgitatakse, kuidas konfigureerida stsenaariume IoT iseõppimisvõime jaoks rakenduses Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a45ed57f1fb5e4d508c30b2f3a83dafacfb7dd870701a8f519bbc1e807ed982
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736789"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT iseõppimisvõime stsenaariumi seadistamine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida stsenaariume IoT iseõppimisvõime jaoks rakenduses Microsoft Dynamics 365 Supply Chain Management. Enne stsenaariumide seadistamist tuleb teil [seadistada teenused Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).

Selles teemas konfigureerite stsenaariumi **Seadmete seisakuaeg**, et masina tõrgete puhul luuaks rakenduses Supply Chain Management teatis. Selles teemas näidatakse ka, kuidas konfigureerida stsenaariumi **Tootekvaliteet**, et kauba atribuudi jäämisel väljapoole määratud vahemikku luuaks teatis, ja kuidas konfigureerida stsenaariumi **Tootmisviivitused**, et olukorras, kus tootmise läbilaskevõime jääb allapoole läviväärtust, luuaks teatis.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Stsenaariumi Seadmete seisakuaeg konfigureerimine Supply Chain Managementis

Stsenaarium **Seadmete seisakuaeg** vastendab märguande **PartOut** masina teatiste lävega. Masinat jälgitakse ainult juhul, kui see on selle stsenaariumi jaoks valitud ja kui selle olekuks on rakenduses Supply Chain Management seatud **Töötab**. Kui aeg, millal masinast saadi viimati märguanne **PartOut**, on suurem kui teatiste lävi, käivitatakse teatis **Masina seisak**. Kui masin töötab edasi, käivitatakse järgmise märguande **PartOut** saamisel teatis **Masin töötab**. Kui masina seisak kestab 30 minutit, käivitatakse uus teatis **Masina seisak**.

Stsenaariumil **Seadmete seisakuaeg** on järgmised sõltuvused.

+ Teatist saab käivitada ainult juhul, kui tootmistellimus töötab vastendatud masinal.
+ Märguanne, mis esindab vastendatud masina märguannet **PartOut**, tuleb saata IoT keskusesse koos kordumatu atribuudinimega.
+ Azure'i IoT keskuse teade peab sisaldama UNIX-i atribuuti **ajatempel**, mille väärtust väljendatakse millisekundites (ms).

Stsenaariumi konfigureerimiseks tehke järgmist.

1. Logige sisse rakendusse Supply Chain Management.
2. Lubage IoT iseõppimisvõime funktsiooni lipp. Lisateavet vt [Funktsioonihalduse ülevaatest](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigureerige mõõdikud. Vaadake lisateavet teemast [Kuidas konfigureerida mõõdikuid](iot-metrics-setup.md#configure-metrics).
4. Avage **Tootmise juhtimine \> Seadistus \> IoT iseõppimisvõime \> Stsenaariumihaldus**.
6. Valige paanil **Seadmete seisakuaeg** suvand **Konfigureeri**, et avada viisard.

   Viisardi esimene leht on **Seadmete anduri skeemi määratlus**. Sellel lehel on teie eesmärk seadistada rakenduses Supply Chain Management skeem nii, et see ühtiks IoT keskuse teadete vorminguga JavaScript Object Notation (JSON). Saate määratleda mitu teateskeemi. Vaadake lisateavet teemast [IoT keskuse teadete skeemivormingud](iot-schema-format.md). Selles näites sisaldab teate last järgmises vormingus teadete partiid.

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Lisage tabelisse rida ja seadke järgmised väärtused.

    1. Seadke välja **Skeemi nimi** väärtuseks **ID**.
    2. Seadke välja **Skeemi tee** väärtuseks **/payload\[\*\]/id**.
    3. Seadke välja **Kirjeldus** väärtuseks **Teate ID**.

8. Lisage tabelisse veel üks rida ja seadke järgmised väärtused.

    1. Seadke välja **Skeemi nimi** väärtuseks **Ajatempel**.
    2. Seadke välja **Skeemi tee** väärtuseks **/last\[\*\]/ajatempel**.
    3. Seadke välja **Kirjeldus** väärtuseks **Teate ajatempel**.

9. Lisage tabelisse veel üks rida ja seadke järgmised väärtused.

    1. Seadke välja **Skeemi nimi** väärtuseks **Väärtus**.
    2. Seadke välja **Skeemi tee** väärtuseks **/last\[\*\]/väärtus**.
    3. Seadke välja **Kirjeldus** väärtuseks **Teate väärtus**.

    > [!NOTE]
    > Te ei pea kõiki teate atribuute määratlema. Määratlege ainult vajalikud atribuudid. Eelmiste sammude käigus ei loonud te rida **juurajatempli** jaoks. Üksuse **Juurajatempel** tee oleks **/ajatempel**.

10. Valige **Edasi**, et avada leht **Seadmete anduri skeemikaart**.
11. Määrake **Seadmete ressursi ID** real välja **Skeemi nimi** väärtuseks **ID**.
12. Määrake rea **UTC-aeg** välja **Skeemi nimi** väärtuseks **Ajatempel**.
13. Määrake real **Osaliselt toodetud märguanne** välja **Skeemi nimi** väärtuseks **Väärtus**.
14. Valige **Edasi**, et minna lehele **Seadmete ressursi ID konfiguratsioon**.
15. Järgige neid juhiseid, et vastendada IoT keskuse teatiste väärtused rakenduse Supply Chain Management ressurssidega.

    1. Lisage tabelile **Märguande andmete väärtused** uus rida. Sisestage väljale **Väärtus** tekst **IoTInt.Machine1225.PartOut**. See väärtus on pärit IoT keskuse teate JSON-i atribuudist **id**.
    2. Valige käsk **Salvesta**.
    3. Valige tabelis **Ärikirje vastendamine** suvand **Uus**. Välja **Ärikirje tüüp** vaikeväärtus täidetakse automaatselt ja seda ei pea muutma.
    4. Valige väljal **Ärikirje** rakenduse Supply Chain Management masina ressurss, kust selle märguande väärtus saadetakse.
    5. Valige käsk **Salvesta**.
    6. Korrake neid samme, et lisada üksusele **Machine1226** uus ärikirje vastendus. Ühe kirjega saate rakenduses Supply Chain Management vastendada mitu märguande andmete väärtust.

16. Kasutage veergu **Valitud**, et valida masinad, mida soovite töödelda. Kõiki märguande väärtusi ei pea määratlema ja kõiki masinaid ei pea valima.
17. Valige **Edasi**, et avada **Osaliselt toodetud märguande konfigureerimine**.
18. Lisage rida tabelisse **Märguande andmete väärtused** ja seadke välja **Väärtus** väärtuseks **Tõene**. See väärtus on pärit IoT keskuse teate JSON-i atribuudist **väärtus**. Saate lisada nii palju väärtusi, kui oma stsenaariumi jaoks vajate.
19. Valige käsk **Salvesta**.
20. Valige **Edasi**, et avada leht **Seadmete seisakuaja lävi**. Loetletud masinad on varem märguande väärtustega vastendatud masinad. Sellel lehel määratlete läve masina seisaku tuvastamiseks. Näiteks kui seate läve väärtuseks **10**, loob rakendus Supply Chain Management teatise, kui masinalt ei tule 10 minuti jooksul märguannet **PartOut**.
21. Lehele **Stsenaariumi lubamine** minemiseks valige **Edasi**. Seadistage suvand stsenaariumi lubamiseks.
22. Valige **Lõpeta**.

Stsenaariumi seadistus on lõpetatud. IoT iseõppimisvõime alustab automaatselt IoT keskuse teatiste töötlemist.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Stsenaariumi Toote kvaliteet konfigureerimine Supply Chain Managementis

Stsenaarium **Toote kvaliteet** loob teatise, kui kauba atribuut jääb määratletud vahemikust väljapoole. Näiteks saadab sensor iga kauba kaalu IoT keskusesse. Kui kaup on liiga raske või liiga kerge, luuakse rakenduses Supply Chain Management teatis.

Stsenaariumil **Tootekvaliteet** on järgmised sõltuvused.

+ Teatis käivitatakse ainult siis, kui tootmistellimus töötab vastendatud masinal ja toodab vastendatud partiiatribuuti omavat toodet.
+ Partiiatribuuti esindav märguanne tuleb saata IoT keskusesse koos kordumatu atribuudinimega.
+ IoT keskuse teade peab sisaldama UNIX-i atribuuti **ajatempel**, mille väärtust väljendatakse millisekundites.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Stsenaariumi Tootmise viivitused konfigureerimine Supply Chain Managementis

Stsenaarium **Tootmise viivitused** loob teatise, kui tootmise läbilaskevõime langeb alla läve väärtuse. Selle stsenaariumi puhul saadetakse IoT keskusesse märguanne **PartOut** iga toodetava kauba kohta. Rakenduses Supply Chain Management arvutatakse tellimuse viivitus selle põhjal, kui pikalt on tootmistellimuse käitamine plaanitud, mitu kaupa tuleks toota, kui kaua tööd on käitatud ja mitu märguannet **PartOut** vastu võetakse. Viivituse teatis luuakse siis, kui töö märguannete **PartOut** arv jääb läviväärtusest allapoole.

Stsenaariumil **Tootmise viivitused** on järgmised sõltuvused.

+ Teatist saab käivitada ainult juhul, kui tootmistellimus töötab vastendatud masinal.
+ Märguanne, mis esindab vastendatud masina märguannet **PartOut**, tuleb saata Azure'i IoT keskusesse koos kordumatu atribuudinimega.
+ IoT keskuse teade peab sisaldama UNIX-i atribuuti **ajatempel**, mille väärtust väljendatakse millisekundites.

## <a name="disable-a-scenario"></a>Stsenaariumi keelamine

Stsenaariumi keelamiseks järgige neid toiminguid.

1. Avage rakenduses Supply Chain Management suvand **Tootmise juhtimine \> Seadistus \> IoT iseõppimisvõime \> Stsenaariumihaldus**.
2. Stsenaariumi paanil valige **Konfigureeri**.
3. Valige **Edasi**, et minna viimasele viisardilehele.
4. Seadistage suvand stsenaariumi keelamiseks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]