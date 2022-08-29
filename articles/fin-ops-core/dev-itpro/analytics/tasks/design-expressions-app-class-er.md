---
title: Elektroonilise aruandluse avaldiste kujundamine, millega kutsuda rakendusklasside meetodeid
description: See artikkel kirjeldab, kuidas taaskasutada olemasolevat rakendusloogikat elektroonilise aruandluse konfiguratsioonide puhul, kutsudes nõutavad rakendusklasside meetodid.
author: kfend
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21c24cee15e9a0fd11838b5b8fd816e4aaed9a93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267838"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Elektroonilise aruandluse avaldiste kujundamine, millega kutsuda rakendusklasside meetodeid

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, [kuidas taaskasutada olemasolevat rakendusloogikat elektroonilise aruandluse (ER)](../general-electronic-reporting.md) konfiguratsioonides, kutsudes nõutavad rakendusklasside meetodid ER-avaldistes. Kutsumisklasside argumentide väärtusi saab käitusajal dünaamiliselt määratleda. Näiteks võivad väärtused põhineda sõelumisdokumendi teabel, et tagada selle õigsust.

Näiteks selles artiklis kujundate protsessi, mis sõelub sissetulevad pangaväljavõtted rakenduse andmete uuendamiseks. Te saate sissetulevad pangaväljavõtted tekstifailina (.txt) failidena, mis sisaldavad rahvusvahelisi pangakonto numbri (IBAN) koode. Pangaväljavõttete importimise osana peate kinnitama IBAN-koodi õigsust, kasutades juba saadaolevat loogikat.

## <a name="prerequisites"></a>Eeltingimused

Selle artikli protseduurid on mõeldud kasutajatele, kellele on määratud süsteemiadministraator **või elektroonilise** **aruandluse arendaja** roll.

Protseduure saab läbi viia mis tahes andmekogumi abil.

Nende lõpuleviimiseks peate alla laadima ja salvestama järgmise faili: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

Selles artiklis loote nõutavad ER konfiguratsioonid näidisettevõttele Litware, Inc. Seetõttu peate enne selle artikli protseduuride sooritamist neid samme järgima.

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Lokalisatsiooni **konfiguratsioonide lehel** kontrollige, et **konfiguratsioonipakkuja Litware, Inc.** näidisettevõttele on saadaval ja märgitud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, täitke esmalt [sammud jaotises Loo konfiguratsioonipakkujad ja märkige need aktiivseks](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Uue elektroonilise aruandluse mudeli konfiguratsiooni importimine

1. Lokaliseerimiskonfiguratsioonide lehel jaotises Konfiguratsioonipakkujad **valige** Microsofti konfiguratsioonipakkuja jaoks **paan**.**·**
2. Valige **Hoidlad**.
3. Valige lehel **Lokaliseerimise** hoidlad suvand Näita **filtreid**.
4. Globaalse hoidlakirje valimiseks lisage nimefiltri **väli**.
5. Väljale Nimi **sisestage** globaalne **·**. Seejärel valige sisaldab filtri **operaatorit**.
6. Valige **Rakendamine**.
7. Valige **[avatud](../er-download-configurations-global-repo.md#open-configurations-repository)**, et vaadata läbi valitud hoidla ER-konfiguratsioonide loend.
8. Konfiguratsioonihoidla **lehel konfiguratsioonipuus valige maksemudel** **.**
9. Kui nupp **Import** on saadaval, valige **see** kiirkaardil Versioonid ja seejärel valige **Jah**.

    Kui nupp **Impordi** pole saadaval, olete juba importinud maksemudeli ER-i **konfiguratsiooni valitud** versiooni.

10. **Sulgege konfiguratsioonihoidla leht** ja seejärel sulgege leht **Lokaliseerimishoidlad**.

## <a name="add-a-new-er-format-configuration"></a>Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine

Lisage uus ER-i vorming, et sõeluda TXT-vormingus sissetulevaid pangaväljavõtteid.

1. Valige lokaliseerimise **konfiguratsioonide lehel** aruandluskonfiguratsioonide **paani**.
2. **Valige vasakul paanil** oleva konfiguratsioonipuu lehel Konfiguratsioonid **maksemudel**.
3. Valige **Konfiguratsiooni loomine**. 
4. Dialoogiakna ripploendis järgige allolevaid etappe.

    1. Sisestage väljale **Uus suvand** **Andmemudelil PaymentModel põhinev vorming**.
    2. Sisestage **väljale** Nimi pangaväljavõtte **impordivorming (näidis**).
    3. Valige väljal **Toetab andmete importimist** suvand **Jah**.
    4. **Konfiguratsiooni loomise lõpetamiseks** valige käsk Loo konfiguratsioon.

## <a name="design-the-er-format-configuration--format"></a>ER-vormingu konfiguratsiooni kujundamine – vorming

Saate kujundada ER-vormingu, mis tähistab välise faili eeldatavat struktuuri TXT-vormingus.

1. Pangaväljavõtte **impordivormingu (näidis) lisatud** vormingu konfiguratsiooni jaoks valige suvand **Kujundaja**.
2. Valige vormingukujundaja **leheküljel** vasakul paanil oleva vormingustruktuuri puus suvand Lisa **juur**.
3. Ilmuvad dialoogiaknas tehke järgmist.

    1. Valige puus tekstiseeria **,\\ et** lisada seeriavormingu **komponent**.
    2. Sisestage **väljale** Nimi **juur**.
    3. Väljal Erimärgid **valige** uus **rida – Windows (CRPIKKU).** Selle sätte alusel peetakse iga rida sõelumisfailis eraldi kirjeks.
    4. Valige nupp **OK**.

4. Valige **Lisa**.
5. Ilmuvad dialoogiaknas tehke järgmist.

    1. Valige puus tekstiseeria **\\**.
    2. Väljale Nimi **sisestage** **Read**.
    3. Valige väljal **Mitmekordsus** suvand **One many**. Selle sätte alusel eeldatakse, et sõelumisfailis on vähemalt üks rida.
    4. Valige nupp **OK**.

6. Valige puus juurread **\\ ja** seejärel lisa **seeria**.
7. Ilmuvad dialoogiaknas tehke järgmist.

    1. Sisestage **väljale** Nimi **väljad**.
    2. **Väljal Mitmekülgsus** valige täpselt **üks**.
    3. Valige nupp **OK**.

8. Valige puus juurridade **\\ väljad\\** ja seejärel käsk **Lisa**.
9. Ilmuvad dialoogiaknas tehke järgmist.

    1. Valige puus tekstistring **\\**.
    2. Sisestage **väljale Nimi** IBAN **·**.
    3. Valige nupp **OK**.

10. Valige käsk **Salvesta**.

Konfiguratsioon on nüüd seadistatud nii, et iga rida sõelumisfailis sisaldab ainult IBAN-koodi.

![Pangaväljavõtte impordivormingu (näidis) konfiguratsioon vormingukujundaja lehel.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>ER-vormingu konfiguratsiooni kujundamine – andmemudelile vastendamine

Saate kujundada ER-vormingu vastenduse, mis kasutab andmemudeli täitmiseks sõelumisfaili teavet.

1. Valige tegevuspaanil **Vormingu** kujundaja leht suvand Kaardista **vorming mudeli jaoks**.
2. Valige tegevuspaanil **mudeli ja** andmeallika vastendamise lehel väärtus **Uus**.
3. **Väljal Definitsioon** valige **BankToCustomerDebitCreditNotificationInitiation**.
4. Sisestage **väljale** Nimi väärtus Vastendamine **andmemudeliga**.
5. Valige käsk **Salvesta**.
6. Valige **Kujundaja**.
7. Valige mudeli **vastendamise** kujundaja lehel andmeallika **tüüpide puus** väärtus **Dynamics 365 for Operations\\ Klass**.
8. Valige jaotises **Andmeallikad** suvand Lisa **juur**, et lisada andmeallikas, mis kutsub olemasolevat rakendusloogikat IBAN-koodide valideerimiseks.
9. Ilmuvad dialoogiaknas tehke järgmist.

    1. Väljale Nimi **sisestage** Tšekikoodid **\_**.
    2. Sisestage **või** valige väljal Klass **ISO7064**.
    3. Valige nupp **OK**.

10. Andmeallikate **tüüpide puus** järgige neid samme.

    1. Laiendage **vormingu** andmeallikat.
    2. Laienda **vorming\\ Juur: Seeria(Juur)**.
    3. Laiendage vormingut **Juur: seeria(juur)\\ read: seeria 1.\\ (read)\*.**
    4. Laiendage vormingut **Juur: seeria(juur)\\ read: seeria 1.\\ (read)\* väljad: seeria 1..1 (väljad).\\)**

11. Andmemudeli **puus** järgige neid samme.

    1. Laiendage **andmemudeli** välja Maksed.
    2. Laiendage **maksete\\ kreeditkonto(CreditorAccount)**.
    3. Laiendage **maksete\\ kreeditkonto(CreditorAccount)\\ ID**.
    4. Laiendage **maksete kreeditkonto(CreditorAccount)Identification\\\\ IBAN\\**.

12. Järgige neid samme konfigureeritud vormingu komponentide sidumiseks andmemudeli väljadega.

    1. Valige **vorming\\ Juur: seeria(juur)\\ read: seeria 1.\* (read)**.
    2. Valige **maksed**.
    3. Valige **Seo**. Selle sätte alusel loetakse iga sõelumisfaili rida üksikuks makseks.
    4. Valige **vormingu juur\\: seeria(juur)\\ read: seeria 1..\* (read)\\ väljad: seeria 1..1 (väljad)\\ IBAN: string(IBAN)**.
    5. Valige **Maksete kreeditkonto\\(CreditorAccount)IBAN-i\\\\ ID**.
    6. Valige **Seo**. Selle sätte alusel **täidetakse andmemudeli IBAN-väli** väärtusega sõelumisfailist.

    ![Vormingu komponentide sidumine andmemudeli väljadega mudeli vastendamise kujundaja lehel.](../media/design-expressions-app-class-er-02.png)

13. Vahekaardil Kontrollimised **järgige neid samme, et lisada kinnitusreegel, mis näitab tõrketeadet mis tahes real sõelumisfailis**, [mis](../general-electronic-reporting-formula-designer.md#Validation) sisaldab kehtetut IBAN-koodi:

    1. Valige **väärtus** Uus ja seejärel redigeeri **tingimust**.
    2. Laiendage **valemikoosturi** lehel **andmeallika** puus kontrollkoodide andmeallikat, mis esindab ISO7064 **rakendusklassi,\_** **et** vaadata selle klassi saadaolevaid meetodeid.
    3. Valige **kontrollkoodid\_\\ verifyMOD1271\_ 36**.
    4. Valige **Andmeallika lisamine**.
    5. Sisestage **valemi** väljale järgmine [avaldis](../general-electronic-reporting-formula-designer.md#Binding): **Check\_ codes.verifyMOD1271\_ 36(vorming. Root.Rows.Fields.IBAN)**.
    6. Valige **Salvesta** ja sulgege seejärel leht.
    7. Valige **suvand Redigeeri teadet**.
    8. Sisestage **valemikoosturi** lehe **valemiväljal** **CONCATENATE("Leiti kehtetu IBAN-kood:&nbsp;", vorming. Root.Rows.Fields.IBAN)**.
    9. Valige **Salvesta** ja sulgege seejärel leht.

    Nende sätete alusel annab kinnitamistingimus iga kehtetu IBAN-koodi *[puhul väärtuse FALSE](../er-formula-supported-data-types-primitive.md#boolean)*, **kutsudes olemasoleva VERIFYMOD1271\_ 36** **meetodi ISO7064** rakenduseklassile. Pange tähele, et IBAN-koodi väärtus määratletakse käitusajal dünaamiliselt helistamismeetodi argumendina, mis põhineb sõelumisteksti faili sisul.

    ![Kinnitusreegel mudeli vastendamise kujundaja lehel](../media/design-expressions-app-class-er-03.png)

14. Valige käsk **Salvesta**.
15. Sulgege mudeli **vastendamise koostaja** lehekülg ja seejärel sulgege mudel andmeallika **vastendamise lehega**.

## <a name="run-the-format-mapping"></a>Vormingu vastendamise käitamine

Testimiseks käivitage vormingu vastendamine, kasutades varem allalaaditud faili SampleIncomingMessage.txt. Loodud väljund hõlmab andmeid, mis imporditakse valitud tekstifailist ja teisaldatakse kohandatud andmemudelisse reaali importimisel.

1. Valige lehel **Mudeli ja andmeallika vastendamine** suvand **Käivita**.
2. Elektroonilise aruande **parameetrite lehel valige** sirvimine, **·** **sirvige allalaaditud faili SampleIncomingMessage.txt** ja valige see.
3. Valige nupp **OK**.
4. Pange tähele, et **mudeli vastendamine andmeallikaga** näitab tõrketeadet kehtetu IBAN-koodi kohta.

    ![Vormingu vastendamise käitamine mudeli ja andmeallika vastendamise lehel](../media/design-expressions-app-class-er-04.png)

5. Vaadake väljund üle XML-vormingus, mis tähistab valitud failist imporditud ja andmemudelisse porditud andmeid. Pange tähele, et tõrgeteta töödeldud on ainult kolm rida imporditud tekstifailist. IBAN-kood võrgus 4 ei kehti ja jäeti vahele.

    ![XML-väljund.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
