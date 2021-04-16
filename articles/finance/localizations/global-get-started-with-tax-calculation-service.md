---
title: Alustage maksuarvutuse lisandmooduliga
description: Selles teemas selgitatakse, kuidas seadistada maksuarvestuse lisandmoodulit.
author: wangchen
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 835ae33fba31d4bccb218969aa9aa61eaa7a3061
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832589"
---
# <a name="get-started-with-the-tax-calculation-add-in-preview"></a>Alustage maksuarvutuse lisandmooduliga (Eelvaade)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

See teema annab teavet selle kohta, kuidas alustada maksuarvestuse lisandmooduliga. Esiteks antakse teile juhised konfigureerimise kohta lahendustes Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) ja Dynamics 365 Finance ja Dynamics 365 Supply Chain Management. Seejärel vaatab see üle tavalise protseduuri kasutades maksuarvestuse lisandmoodulit Finants ja Supply Chain Management -i kannetes.

Seadistus koosneb neljast peamisest astmest:

1. LCS-s installi maksuarvestuse lisandmoodul.
2. RCS-is seadistage maksuarvestuse funktsioon. Need häälestusandmed pole spetsiifilised iga juriidilise üksuse jaoks. Seda saab jagada finants- ja Supply Chain Management -i kõigi juriidiliste üksuste vahel.
3. Finantside ja Supply Chain Management -is seadistage juriidilise üksuse maksu arvutamise lisandmooduli parameetrid.
4. Finantside ja Supply Chain Management -is looge kandeid, nt müügitellimusi, ning kasutage maksude määramiseks ja arvutamiseks maksuarvutuse lisandmoodulit.

## <a name="prerequisites"></a>Eeltingimused

Enne selles teemas kirjeldatud protseduuride lõpetamist peavad täidetud olema järgmised eeltingimused:

- Teil on juurdepääs oma LCS-i kontole ja olete juurutanud LCS-projekti, mille järgu 2 (või kõrgemas) keskkonnas töötab Dynamics 365 versioon 10.0.18 või uuem versioon.
- Juurdepääs oma RCS-i kontole.
- Olete Microsoftiga ühendust võtnud, et lubada lennud juurutatud finantside või Supply Chain Management keskkonnas.

## <a name="set-up-the-tax-calculation-add-in-in-lcs"></a>Seadistage maksuarvestuse lisandmoodul LCS-is

1. Logige sisse [LCS](https://lcs.dynamics.com)
2. Viige integratsiooni seadistus Microsoft Power Platform -i jaoks lõpule. Lisateavet vt teemast [Lisandmooduli ülevaade](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Valige üks teie juurutatud mittetootmiskeskkonnast ja seejärel valige **Installi uus lisandmoodul**.
4. Valige **Maksuarvestuse (eelvaade)**.
5. Lugege tingimusi ja nõustuge nendega ning valige seejärel **Installi**.

## <a name="set-up-the-tax-calculation-add-in-in-rcs"></a>Seadistage maksuarvestuse lisandmoodul RCS-is

Selle jaotise sammud ei ole seotud kindla juriidilise üksusega. Seda protseduuri tuleb teha ainult üks kord ning seda saab täita mis tahes RCS-i juriidilises üksuses.

1. Logige teenusesse [RCS](https://marketing.configure.global.dynamics.com/) sisse.
2. Finantsis **Elektroonilise atuandluse** tööruumis, lisage uus konfiguratsiooni pakkuja. Kasutage oma ettevõtte nime pakkuja nimena. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Valige äsja loodud konfiguratsioonipakkuja ja valige **Määra aktiivseks**.
4. Valige **Microsoft** konfiguratsiooni pakkuja ja seejärel valige **Hoidlad**.
5. Väljalt **Tüüp** valige **Globaalne**.
6. Valige **Avamine**.
7. Minge **Maksu andmemudelisse**, laiendage failipuud ja valige seejärel **Maksukonfiguratsioon – Euroopa**.
8. Valige uusim versioon ja seejärel käsk **Impordi**.
9. Minge tagasi **Globaliseerimisfunktsiooni (Eelvaade)** tööruumi, valige **Funktsioonid**, valige **maksuarvutuse** paan ja seejärel valige **Lisa**.
10. Saate valida ühe järgmistest funktsioonitüüpidest:

    - **Uus funktsioon** – Looge funktsiooniseadistuse, kus sisu on tühi.
    - **Põhineb olemasoleval funktsioonil** – Looge funktsioon olemasolevast funktsioonist ja kopeerige sisu olemasolevast funktsiooni seadistusest.

11. Sisestage funktsiooni nimi ja kirjeldus ja seejärel valige **Loo funktsioon**.

    Pärast funktsiooni loomist luuakse automaatselt selle mustandversioon.

12. Valige funktsiooni mustandversioon ja seejärel käsk **Redigeeri**. **Maksuarvestuse seadistuse** leht on täidetud.
13. Valige **Konfiguratsiooniversioon**. Peaksite nägema konfiguratsiooni versiooni, mille importisid sammus 8.

    Microsoft pakub vaikemaksukonfiguratsiooni maksu arvutamise lisandmooduli jaoks. See konfiguratsioon katab enamiku maksuarvutuse käitumiste nõuded. Seda uuendatakse turu tagasiside põhjal. Kui peate konfiguratsiooni konkreetsetele nõuetele vastamiseks laiendama, vaadake [Kuidas ehitada maksuteenuse laiendust](https://go.microsoft.com/fwlink/?linkid=2138483) saamaks lisateavet selle kohta, kuidas luua ja valida omamaksukonfiguratsiooni.

    Pärast **Konfiguratsiooniversiooni** valimist kuvatakse veel mitu vahekaarti:

    - **Maksukoodid** – See vahekaart on maksu arvutamise teenuse puhul kohustuslik. Seda kasutatakse maksukoodide koondandmete säilitamiseks. Kõik sellel vahekaardil loodud maksukoodid sünkroonitakse finantsidega automaatselt, kui lubate juriidilise üksuse maksufunktsiooni seadistuse praeguse versiooni.
    - **Maksukoodide kohaldatavus** – See vahekaart on maksu arvutamise lisandmooduli puhul kohustuslik. Seda kasutatakse maatriksi määratlemiseks, mis määratleb maksukoodi, maksugrupi ja kauba maksugrupi. Määratletud maksukoodi kasutatakse maksusumma arvutamiseks. Väljade **Maksukood**, **Maksugrupp** ja **Kauba maksugrupp** väärtused tagastatakse Finantsidesse.
    - **Kliendi maksuregistreerimise numbri kohaldatavus** – See vahekaart on maksu arvutamise lisandmooduli puhul valikuline. Kui teil on mitu maksuregistreerimise numbrit ühe kliendi kohta, saab maksuarvestuse lisandmoodul õige maksuregistreerimise numbri määrata automaatselt. Selle vahekaardi maatriksis määrate reeglid, mida lisandmoodul määramise määramiseks kasutab. Vastasel juhul jätkavad finants- ja Supply Chain Management käibemaksu registreerimisnumbri vaikenumbri kasutamist müügikannete maksustatavate dokumentide puhul.
    - **Hankija maksuregistreerimise numbri kohaldatavus** – See vahekaart on maksu arvutamise lisandmooduli puhul valikuline. Kui teil on mitu maksuregistreerimise numbrit ühe hankija kohta, saab maksuarvestuse lisandmoodul õige maksuregistreerimise numbri määrata automaatselt. Selle vahekaardi maatriksis määrate reeglid, mida lisandmoodul määramise määramiseks kasutab. Vastasel juhul jätkavad finants ja Supply Chain Management maksu registreerimisnumbri vaikenumbri kasutamist müügikannete maksustatavate dokumentide puhul.
    - **Loendikoodide kohaldatavus** – See vahekaart on maksu arvutamise lisandmooduli puhul valikuline. See aitab automaatselt määrata **Loendi kood** välja väärtust paindlikumate ja konfigureeritavate reeglite abil. Selle vahekaardi maatriksis määrate reeglid, mida lisandmoodul määramise määramiseks kasutab. Vastasel juhul jätkavad finants- ja Supply Chain Management maksu vaikekoodi kasutamist maksustatavate dokumentide puhul.

14. Vahekaardil **Maksukoodid** valige **Lisa** ning sisestage maksukood ja kirjeldus.
15. Valige **maksukomponent**. Maksukomponent on maksuarvutusmeetodite grupp, mis määratleti valitud maksukonfiguratsiooni eelmises versioonis. Saadaval on järgmised maksu komponendid:

    - netosumma järgi
    - brutosumma järgi
    - Koguse järgi
    - Marginaali järgi
    - Maks maksult

16. Valige käsk **Salvesta**. Valitud maksukomponendi põhjal on saadaval veel välju.
17. Kasutage järgmisi valikuid maksukoodi olemuse tuvastamiseks:

    - Vabastatud
    - Kasutusmaks
    - On pöördtasu
    - Välista baassumma arvutamisel

    Kasutusmaksu stsenaariumi korral seadistage positiivne maksumäär ja märkige see kui **Kasutusmaks**.

    Pöördtasu stsenaariumi korral seadistage kaks maksukoodi, millest ühel on positiivne maksumäär ja teine, millel on negatiivne maksumäär, kuid sama määra väärtus. Märkige negatiivne maksukood kui **Pöördtasu**. Lisateavet finantsis pöördtasu lahenduse kohta vt [Pöördtasu mehhanism VAT/GST skeem](emea-reverse-charge.md).
    
    Mõne maksutüübi puhul, mis tuleks hinna maksu baassumma arvutusest inklusiivsete kannete korral välistada nagu mõne riigi tollimaksud, valige märkeruut **Välista baasmaksusumma arvutus** .

    Halda maksumäärasid ja maksusumma limiite selle maksukoodi jaoks.

18. Korrake samme 14–17 kõigi vajalike maksukoodide lisamiseks.
19. Vahekaardil **Maksukoodide kohaldatavus** valige veerud, mis on nõutavad õige maksukoodi määramiseks, ja seejärel valige **Lisa**.
20. Sisestage või valige väärtused iga veeru jaoks. Väljade **Maksukood**, **Maksugrupp** ja **Kauba maksugrupp** väärtused on selle maatriksi väljund.
21. Korrake samme 19 kuni 20, et seadistada kliendi maksu registreerimisnumbrite, hankija maksu registreerimisnumbrite ja loendikoodide kohaldatavus.
22. Valige **Salvesta** ja sulgege seejärel leht.
23. Valige **Muuda olekut** \> **Lõpule viidud**. Pärast oleku muutmist olekuks **Lõpetatud** ei saa seda versiooni enam redigeerida.
24. Valige **Muuda olekut** \> **Avalda**. See maksufunktsiooni häälestuse versioon tõugatakse globaalsesse hoidlasse ja on nähtav igale finantsi juriidilisele üksusele.

## <a name="dynamics-365-setup"></a>Dynamics 365 häälestus

Pärast seadistuse lõpule viimist RCS-s, nagu kirjeldatud eelmises jaotises, on teil maksufunktsiooni avaldatud versioon. Järgige neid samme finantside maksuarvestuse lisandmooduli häälestamiseks.

Selle jaotise seadistas juriidiline üksus. Peate selle konfigureerima iga juriidilise üksuse jaoks, kelle jaoks soovite finantsis maksuarvestuse lisandmooduli lubada.

1. Finantsis minge **Maksu** \> **Seadistamise** \> **Maksukonfiguratsiooni** \> **Maksuarvutuse lisandmooduli häälestusse (eelvaade)** .
2. Vahekaardil **Üldine** määrake järgmised väljad.

    - **Luba maksuarvutuse lisandmoodul** – Märkige see ruut, et lubada juriidilisele üksusele maksuarvutuse lisandmoodul. Kui maksuarvutuse lisandmoodul ei ole praegusele juriidilisele üksusele lubatud, kasutab juriidiline isik maksu määramiseks ja arvutamiseks olemasolevat maksumootorit.
    - **Funktsiooni häälestus** – Valige juriidiliseüksuse avaldatud maksu funktsiooni häälestus ja versioon. Lisateavet avaldatud maksufunktsiooni seadistamis- ja lõpuleviimise kohta vt selle teema eelmisest jaotisest.
    - **Äriprotsess** – Valige äriprotsessid, et lubada maksuarvutuse lisandmoodulit.
    - **Luba maksukoodi korrigeerimine** -- Seadistage see valik valikule **Jah** , et lubadaemaksukoodi korrigeerimine käibemaksu leheküljel.

3. Määratlege vahekaardil **Arvutus** juriidilise isiku eeldatav ümardamisreegel.
4. Määratlege vahekaardil **Tõrkekäsitlus** juriidilise isiku eeldatav tõrke käsitlemise meetod. Maksuarvestuse lisandmoodulist on iga tulemusekoodi jaoks saadaval kolm võimalust:

    - Ei
    - Hoiatus
    - Viga

5. Salvestage maksuarvestuse lisandmooduli seadistus.
6. Korrake samme 1–5 iga järgmise juriidilise isiku jaoks.

## <a name="transaction-processing"></a>Kannete töötlemine

Kui olete kõik seadistusprotseduurid lõpule viinud, saate finantside maksu määramiseks ja arvutamiseks kasutada maksuarvutuse lisandmoodulit. Kannete töötlemise sammud jäävad samaks. Finantsversioonis 10.0.18 toetatakse järgmisi kandeid:

- Müügiprotsess

    - Müügipakkumine
    - Müügitellimus
    - Kinnitus
    - Komplekteerimisleht
    - Saateleht
    - Müügiarve
    - Kreeditarve
    - Tagastustellimus
    - Päise tasu
    - Reatasu

- Ostuprotsess

    - Ostutellimus
    - Kinnitus
    - Saabunud kaupade loend
    - Toote sissetulek
    - Ostuarve
    - Päise tasu
    - Reatasu
    - Kreeditarve
    - Tagastustellimus
    - Ostutaotlus
    - Ostutaotluse rea tasu
    - Pakkumiskutse
    - Pakkumiskutse päise tasunõue
    - Pakkumiste rea tasunõue

- Inventuuriprotsess

    - Kandetellimus-- lähetus
    - Kandetellimus-- kättesaamine
