---
title: Omnikanali maksete ülevaade
description: Selles teemas antakse ülevaade omnikanali maksetest rakenduses Dynamics 365 Commerce.
author: rubendel
manager: AnnBe
ms.date: 11/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 2251e523f7dfa3a06f0c45a4e156dbe097587f9a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022322"
---
# <a name="omni-channel-payments-overview"></a>Omnikanali maksete ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade omnikanali maksetest rakenduses Dynamics 365 Commerce. See sisaldab põhjalikku loendit toetatud stsenaariumitega, teavet funktsioonide, seadistamise ja tõrkeotsingu kohta ning tavaliste probleemide kirjeldusi.

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| Luba | Andmestring, mille maksetöötleja esitab viitena. Load võivad tähistada maksekaardi numbreid, makse autoriseerimisi ja eelmise makse jäädvustusi. Load on olulised, kuna need aitavad hoida tundlikke andmeid süsteemi kassast (POS) eemal. Neid nimetatakse mõnikord *viideteks*. |
| Kaardiluba | Luba, mille maksetöötleja esitab kassasüsteemi salvestamiseks. Kaardiluba saab kasutada ainult kaupmees, kellele see antakse. Kaardilubasid nimetatakse mõnikord *kaardiviideteks*. |
| Autoriseerimise luba | Kordumatu ID, mille makseprotsess esitab osana vastusest, mille see saadab kassasüsteemi pärast seda, kui kassasüsteem esitab autoriseerimise taotluse. Autoriseerimise luba saab kasutada hiljem, kui töötlejal palutakse teha niisuguseid toiminguid nagu autoriseerimise ennistamine või tühistamine. Kuid kõige sagedamini kasutatakse seda vahendite jäädvustamiseks, kui tellimus täidetakse või kanne lõpule viiakse. Autoriseerimise lubasid nimetatakse mõnikord *autoriseerimise viideteks*. |
| Hõivamise luba | Viide, mille maksetöötleja esitab kassasüsteemi, kui makse lõpule viiakse või hõivatakse. Hõivamise luba saab seejärel kasutada maksehõive viitamiseks järgmistes toimingutes, näiteks tagasimakse taotlustes. | 
| Kaarti pole | Tingimus, mis viitab maksekannetele, kus füüsilist kaarti pole. Näiteks võivad need kanded esineda e-kaubanduse või kõnekeskuse stsenaariumides. Nende kannete jaoks sisestatakse maksega seotud teave käsitsi e-kaubanduse veebisaidil, kõnekeskuse voos või kassa- või makseterminalis. |
| Kaart on olemas | Tingimus, mis viitab maksekannetele, kus füüsiline kaart on olemas ja seda kasutatakse makseterminalis, mis on ühendatud Microsoft Dynamics 365 kassasüsteemiga. |

## <a name="overview"></a>Ülevaade

Üldiselt kirjeldab tingimus *omnikanali maksed* võimet luua tellimus ühes kanalis ja täita see teises kanalis. Omnikanali makse toe põhiomadus on säilitada makse üksikasju koos ülejäänud makse üksikasjadega ja seejärel kasutada neid makse üksikasju, kui tellimus teises kanalis tagasi kutsutakse või seda seal töödeldakse. Klassikaline näide on veebist tellimise ja kauplusest kättesaamise stsenaarium. Selles stsenaariumis lisatakse makse üksikasjad, kui tellimus veebis luuakse. Seejärel kutsutakse need tagasi kassasse, et kliendi maksekaardilt kättesaamisel tasu võtta. 

Kõiki selles teemas kirjeldatud stsenaariume saab juurutada, kasutades Commerce’is olevat standardset maksete tarkvaraarenduse komplekti (SDK). [Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) annab valmis juurutuse iga siin kirjeldatud stsenaariumi kohta. 

### <a name="prerequisites"></a>Eeltingimused

Iga stsenaariumi jaoks, mida selles teemas kirjeldatakse, on vaja maksekonnektorit, mis toetab omnikanali makseid. Valmis Adyeni konnektorit saab samuti kasutada, kuna see toetab stsenaariume, mis on tehtud saadavaks maksete SDK kaudu. Lisateavet maksekonnektorite juurutamise ja Retaili SDK kohta üldiselt vaadake teemast [Avaleht Retail IT-professionaalidele ja arendajatele](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Toetatud versioonid

Selles teemas kirjeldatud omnikanali maksevõimalused väljastati osana rakenduse Microsoft Dynamics 365 for Retail versioonist 8.1.3. 

#### <a name="card-present-and-card-not-present-connectors"></a>Konnektorid Kaart on olemas ja Kaarti pole

Maksete SDK tugineb kahel rakenduse programmeerimisliidese (API) komplektil maksete jaoks. Esimene API-de komplekt kannab nime **iPaymentProcessor**. Seda kasutatakse maksekonnektorite Kaarti pole juurutamiseks, mida saab kasutada kõikides kõnekeskustes ja rakenduse Microsoft Dynamics e-kaubanduse platvormiga. Lisateavet liidese **iPaymentProcessor** kohta vaadake tehnilisest ülevaatest [Maksekonnektori ja -seadme juurutamine](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf) maksete kohta. 

Teine API-de komplekt kannab nime **iNamedRequestHandler**. See toetab makse integratsioonide Kaart on olemas juurutamist, mis kasutavad makseterminali. Lisateavet liidese **iNamedRequestHandler** kohta vaadake teemast [Makse integreerimise loomine makseterminali jaoks](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Seadistamine ja konfigureerimine

Vajalikud on järgmised komponendid ja seadistustoimingud.

- **eCommerce’i integratsioon:** stsenaariumide toetamiseks, kus tellimus pärineb veebipoe fassaadist, on vajalik integratsioon Commerce’iga. Lisateavet Retaili e-kaubanduse SDK kohta vaadake teemast [E-kaubanduse platvormi tarkavaraarenduse komplekt (SDK)](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). Demokeskkonnas toetab viite fassaad omnikanali makse stsenaariume. 
- **Veebimaksete konfiguratsioon:** veebikanali seadistus peab hõlmama maksekonnektorit, mis on uuendatud toetama omnikanali makseid. Võib ka kasutada valmis maksekonnektorit. Lisateavet Adyeni maksekonnektori konfigureerimise kohta veebipoodide jaoks vaadake teemast [Adyeni maksekonnektor](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce). Peale selles kirjeldatud e-kaubanduse seadistustoimingute peab parameeter **Luba makseteabe salvestamine e-kaubanduses** olema Adyeni konnektori sätetes olema seatud väärtusele **Tõene**. 
- **Omnikanali maksete konfiguratsioon:** tehke kontoris valikud **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. Seejärel seadistage vahekaardil **Omnikanali maksed** suvand **Kasuta omnikanali makseid** valikule **Jah**.
- **Makseteenused:** kõnekeskus kasutab vaikimisi maksekonnektorit lehel **Makseteenused** maksete töötlemiseks. Niisuguste stsenaariumide nagu Kõnekeskusesse tellimine ja kättesaamine kauplusest toetamiseks peab see vaikimisi maksekonnektor olema Adyeni maksekonnektor või maksekonnektor, mis vastab omnikanali maksete juurutamise nõuetele.
- **EFT-teenus:** maksed läbi makseterminali tuleb seadistada riistvaraprofiili kiirkaardil **EFT-teenus**. Adyeni konnektor toetab omnikanali maksete stsenaariume valmis kujul. Kasutada saab ka muid maksekonnektoreid, mis toetavad liidest **iNamedRequestHandler**, kui need toetavad omnikanali makseid.
- **Maksekonnektori saadavus:** kui tellimus tagasi kutsutakse, sisaldavad tellimusega koos tagasi kutsutud makse maksevahendi read maksekonnektori nime, mida kasutati selle tellimusega seotud autoriseerimiste loomiseks. Kui tellimus täidetakse, üritab maksete SDK kasutada sama konnektorit, mida kasutati algse autoriseerimise loomiseks. Seetõttu peab hõivamiseks olema saadaval maksekonnektor, millel on samad kaupmehe atribuudid. 
- **Kaarditüübid:** selleks et omnikanali stsenaariumid õigesti toimiks, peab igal kanalil olema sama seadistus maksevahendite tüüpide jaoks, mida saab omnikanali jaoks kasutada. See seadistus hõlmab maksemeetodi ID-sid ja kaarditüübi ID-sid. Näiteks kui maksevahendi tüübi **Kaardid** ID on veebipoe seadistuses **2**, peab sellel olema sama ID kaupluse seadistuses. Sama nõue kehtib kaarditüübi ID-dele. Kui kaardi number **12** seadistatakse veebipoes väärtusele **VISA**, tuleb sama ID seadistada kauplusele. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Omnikanali maksete toetamise üldpõhimõtted

Maksekonnektorid ja makseprotsessid kasutavad lubasid ehk viiteid kaardimaksetega seotud interaktsioonidele viitamiseks. Näiteks kui vajalik on makse autoriseerimine, esitatakse sellele autoriseerimisele viide. Seetõttu saab autoriseerimist hiljem viidata, kui maksevahendid täitmise ajal hõivatakse. See autoriseerimine on unikaalne kaupmehele, maksekonnektorile ja töötlejale. 

Kui veebis loodud tellimusele minnakse kauplusesse järele, tuleb selle tellimuse samad makse üksikasjad tagasi kutsuda ja neid kasutada. Kui algsed üksikasjad esitatakse osana nõudest hõivata makse algse autoriseerimise suhtes, suudab maksetöötleja taotlusega tegeleda ja makse hõivata. 

Veebitellimuse õigesti viitamiseks peab saadaval olema ka maksekonnektor Kaarti pole, mis toetab sama töötlejat. Nii saab kassasüsteemil olla üks töötleja olemasoleva kaardiga maksete jaoks, aga sellel võib olla ka juurdepääs teistele maksekonnektoritele, nii et see saab täita tellimusi, mis luuakse muudes kanalites, kasutades teistsugust maksetöötlejat. 

## <a name="supported-scenarios"></a>Toetatud stsenaariumid

Toetatakse järgmisi omnikanali makse stsenaariume.

- Ostmine veebist, kättesaamine kauplusest
- Ostmine kõnekeskusest, kättesaamine kauplusest
- Ostmine kauplusest A, kättesaamine kauplusest B
- Ostmine kauplusest A, tarnimine kliendile

Toetatakse ka nende stsenaariumide variatsioone. Näiteks veebitellimus võib sisaldada nii ridu, mis tarnitakse kliendile, kui ka ridu, mis saadakse kätte kauplusest. Tellimuse täitmise suvandeid toetatakse omnikanali maksete kaudu. 

Järgmistes jaotises kirjeldatakse iga stsenaariumi toiminguid ja näidatakse, kuidas käivitada stsenaariumit demoandmeid kasutades. 

### <a name="buy-online-pick-up-in-store"></a>Ostmine veebist, kättesaamine kauplusest

Enne alustamist veenduge, et järgmised tingimused oleks täidetud.

- Olemas on viite fassaad, kus on konfigureeritud Adyeni konnektor.
- Suvand **Omnikanali maksed** lehel **Commerce’i ühiskasutuses parameetrid** on seatud väärtusele **Tõene**.
- Adyeni maksekonnektor on konfigureeritud Houstoni kassaregistrile.

Stsenaariumi käivitamiseks järgige neid toiminguid.

1. Looge viite fassaadis kaupluses järeletulemisega tellimus. Valige kindlasti kauplus **Houston**. 
2. Läbige väljaregistreerimise toimingud ja makske, kasutades krediitkaardi kontrollnumbrit. Krediitkaardi kontrollnumbreid saate otsida lehelt [Adyeni kaardi kontrollnumbri leht](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. Kasutage Cammerce’is pakett-tööd **Tellimuste sünkroonimine** ja jaotusgraafikut **P-001**, et luua tellimused kontoris.
4. Valige kassas tervituslehel toiming **Kättesaadavad tellimused**, et näha poes kättesaadavaid tellimusi. 
5. Valige viite fassaadis loodud tellimusest üks või mitu rida ja valige suvand **Kättesaamine**.

    Tellimus võetakse kontorist. 

6. Kui tellimuse rea üksikasjad võetakse kontorist ja tuvastatakse kaardimakse, mida saab kasutada omnikanali jaoks, teavitatakse teid, et saadaval on maksemeetod.
7. Valige suvand **Saadaoleva makseviisi kasutamine**, et kanne lõpetada, kasutades viite fassaadi sisestatud kaardi üksikasju.

    Tellimuse read laaditakse kande lehele ja deebetsaldo on 0 (null). 

8. Valige vahekaart **Maksed**, et näha võrgutellimusest võetud maksevahendi rida. 
9. Valige maksemeetod kande lõpetamiseks. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Ostmine kõnekeskusest, kättesaamine kauplusest

1. Sisestage Commerce’is lehel **Klienditeenindus** otsinguribale tekst **Karen Berg** ja seejärel valige suvand **Otsi**. 
3. Valige otsingutulemustest **Karen Berg**.
4. Kui Karen on laaditud lehele **Klienditeenindus**, valige suvand **Uued müügitellimused**.
5. Valige uue müügitellimuse lehel **Päis**, et vaadata tellimuse päist. 
6. Lehel **Tellimuse päis** määrake sait valikule **Keskne** ja ladu valikule **Houston**.
7. Vahekaardil **Tarne** määrake väli **Tarneviis** kliendi kättesaamise korral valikule **60**.
8. Valige **Read** ja seejärel lisage tellimusele üks või mitu rida. 
9. Valige käsk **Lõpeta**, et sisestada tellimus lõpetamise voogu.
10. Kerige alla maksete jaotisesse, valige käsk **Lisa** ja seejärel valige rida, kus maksemeetodi tüüp on seatud valikule **Kaardid**. 
11. Valige plussmärk (**+**) kaardimakse lisamiseks. 
12. Sisestage krediitkaardi kontrollnumbri üksikasjad, mille leidsite lehelt [Adyeni kaardi kontrollnumbrite leht](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description), ja valige **OK**.

    > [!NOTE]
    > Kui sisestatud kaardinumbri kaardi tootemark erineb tootemargist, mis valiti makse käivitamisel, läheb makse siiski läbi. Kuid see sisestatakse kontodele, mis on vastendatud kaardi tootemargiga, mille valisite sammus 10.

12. Valige uuesti **OK** dialoogiboksi **Tellimuse lõpetamise maksed** sulgemiseks.
13. Lehel **Müügitellimuse kokkuvõte** valige suvand **Esita**.
14. Valige kassas tervituslehel toiming **Kättesaadavad tellimused**, et näha poes kättesaadavaid tellimusi. 
15. Valige viite fassaadis loodud tellimusest üks või mitu rida ja valige suvand **Kättesaamine**.

    Tellimus võetakse kontorist. 

16. Kui tellimuse rea üksikasjad võetakse kontorist ja tuvastatakse kaardimakse, mida saab kasutada omnikanali jaoks, teavitatakse teid, et saadaval on maksemeetod.
17. Valige suvand **Saadaoleva makseviisi kasutamine**, et kanne lõpetada, kasutades viite fassaadi sisestatud kaardi üksikasju.

    Tellimuse read laaditakse kande lehele ja deebetsaldo on 0 (null).

18. Valige vahekaart **Maksed**, et näha võrgutellimusest võetud maksevahendi rida. 
19. Valige maksemeetod kande lõpetamiseks. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Ostmine kauplusest A, kättesaamine kauplusest B

1. Käivitage kassa Houstoni kaupluse jaoks.
2. Lisage lehel **Kanne** Karen Berg kandele, kasutades numbriklahvistikku numbri **2001** sisestamiseks.
3. Lisage kandele üks või mitu rida.
4. Valige **Tellimused** tellimuse suvandite nägemiseks.
5. Valige suvand **Võta kõik peale** ja seejärel valige suvand **Klienditellimus**, kui palutakse.
6. Sisestage otsinguribale **Seattle** ja seejärel valige kättesaamise kaupluseks **Seattle**. 
7. Valige **OK** praeguse kuupäeva määramiseks kättesaamise kuupäevaks.
9. Makse alustamiseks valige suvand **Tasumine kaardiga**.
10. Määrake kaardimakse maksevahendiks deposiidiks olevale summale. 
11. Lõpetage deposiidi makse makseterminalis. 
12. Kui deposiit on makstud, valige suvand kasutada sama kaarti täitmiseks ja oodake, kuni tellimus lõpetatakse. 
13. Käivitage kassa Seattle’i kaupluse jaoks.
14. Valige kassas tervituslehel toiming **Kättesaadavad tellimused**, et näha poes kättesaadavaid tellimusi. 
15. Valige viite fassaadis loodud tellimusest üks või mitu rida ja valige suvand **Kättesaamine**.

    Tellimus võetakse kontorist. 

16. Kui tellimuse rea üksikasjad võetakse kontorist ja tuvastatakse kaardimakse, mida saab kasutada omnikanali jaoks, teavitatakse teid, et saadaval on maksemeetod.
17. Valige suvand **Saadaoleva makseviisi kasutamine**, et kanne lõpetada, kasutades viite fassaadi sisestatud kaardi üksikasju.

    Tellimuse read laaditakse kande lehele ja deebetsaldo on 0 (null).

18. Valige vahekaart **Maksed**, et näha võrgutellimusest võetud maksevahendi rida. 
19. Valige maksemeetod kande lõpetamiseks. 

### <a name="buy-in-store-a-ship-to-customer"></a>Ostmine kauplusest A, tarnimine kliendile

1. Käivitage kassa Houstoni kaupluse jaoks.
2. Lisage lehel **Kanne** Karen Berg kandele, kasutades numbriklahvistikku numbri **2001** sisestamiseks.
3. Lisage kandele üks või mitu rida.
4. Valige **Tellimused** tellimuse suvandite nägemiseks.
5. Valige suvand **Võta kõik peale** ja seejärel valige suvand **Klienditellimus**, kui palutakse.
6. Sisestage otsinguribale **Seattle** ja seejärel valige kättesaamise kaupluseks **Seattle**. 
7. Valige **OK** praeguse kuupäeva määramiseks kättesaamise kuupäevaks.
8. Makse alustamiseks valige suvand **Tasumine kaardiga**.
9. Määrake kaardimakse maksevahendiks deposiidiks olevale summale. 
10. Lõpetage deposiidi makse makseterminalis. 
11. Kui deposiit on makstud, valige suvand kasutada sama kaarti täitmiseks ja oodake, kuni tellimus lõpetatakse.

Kui tellimus on kontoris komplekteeritud, pakitud ja selle kohta on arve koostatud, kasutatakse kassas olevaid makse üksikasju maksevahendite hõivamiseks kliendile tarnitavate kaupade jaoks. 

## <a name="scenario-details"></a>Stsenaariumi üksikasjad

Peale kirjeldatud põhistsenaariumide on maksete SDK-s tehtud mitu täiustust omnikanali maksete toetamiseks. 

### <a name="pos"></a>Müügikoht

#### <a name="single-swipedip-for-customer-orders"></a>Üks kaarditõmme/kaardisisestus klienditellimustele

Enne omnikanali maksete funktsiooni juurutamist, loodi deposiite sisaldavad klienditellimused kassas ja kliendid pidid kaarti tõmbama (või sisestama) kaks korda: üks kord deposiidi maksmiseks ja üks kord kaardi loa loomiseks järgmiste tellimuste täitmiseks. Kui omnikanali loa loomise funktsioon on sisse lülitatud, peavad kliendid kaarti tõmbama ainult ühe korra nii deposiidi maksmiseks kui ka summa autoriseerimiseks, mis tuleb tasuda hiljem täidetavate tellimuste eest. Täitmise ajal hõivatakse autoriseeritud maksevahendid. Enne omnikanali loa lubamise funktsiooni juurutamist loodi järgmise tellimuse täitmiseks korduv kaardiluba. Seetõttu ei autoriseeritud ootelolevate täitmiste maksevahendeid ja kuna neid maksevahendeid ei hoitud selle konkreetse ostu jaoks, oli vähem tõenäoline, et neid saab hiljem hõivata.

> [!NOTE]
> Ühekordset kaarditõmmet ei toeta Retaili versioon 8.1.3. Klienditellimused versioonis 8.1.3 kasutavad sama voogu, mida kasutati enne omnikanali loa lubamise funktsiooni juurutamist. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Kaardid, mis ei anna välja korduvaid kaardilubasid

Mõnda kaarti ei saa kasutada omnikanali maksete jaoks, kuna need ei toeta korduvate kaardilubade väljaandmist. Kui kassas luuakse tellimus ja deposiidi eest makstakse kaardiga, mis ei toeta korduvaid kaardilubasid, kasutatakse eelmist kaardi loa loomise voogu. Seetõttu peab klient, kes soovib teha makse, mida kasutatakse järgmise tellimuse täitmiseks, esitama teise kaardi. Kui teine kaart ei toeta korduvaid kaardilubasid, lükatakse loa loomise toiming tagasi ja kassapidajal palutakse öelda kliendile, et kasutada tuleb teist kaarti. 

### <a name="using-a-different-card"></a>Teise kaardi kasutamine

Kauplusesse tellimuse järele tulev klient saab kasutada teist kaarti. Kui kassapidaja saab tellimuse kättesaamisel viiba **Saadaoleva makseviisi kasutamine**, saab ta kliendilt küsida, kas ta soovib kasutada sama kaarti. Kui klient on tellimuse loomiseks kasutatud kaardi ära kaotanud ja soovib maksta tellimuse eest teise kaardiga, saab kassapidaja valida suvandi **Kasutage muud makseviisi**. Kui klient tuleb hiljem tagasi järele sama tellimuse teistele kaupadele ja algne kaardi autoriseerimine kehtib endiselt, võib kassapidaja uuesti küsida, kas klient soovib kasutada seda kaarti.

### <a name="invalid-authorizations"></a>Kehtetud autoriseerimised

Kui tellimuse loomiseks kasutatud kaart ei ole enam kehtiv ja kättesaamiseks valitakse tooted, siis makse hõivamise taotlus nurjub. Kassa maksekonnektor üritab seejärel luua uue autoriseerimise ja hõivamise samu kaardi üksikasju kasutades. Kui uus autoriseerimine või hõivamine nurjub, teavitatakse kassapidajat, et makset ei saanud töödelda. Kassapidaja peab siis saama kliendilt uue makse. 

### <a name="multiple-available-payments"></a>Mitu saadaolevat makset

Kui järele minnakse tellimusele, millel on mitu maksevahendid ja mitu rida, esitatakse kassapidajale kõigepealt viip **Saadaoleva makseviisi kasutamine**. Kui kaarte on mitu ja kassapidaja valib suvandi **Saadaoleva makseviisi kasutamine**, hõivatakse saadaoleva kaardi read, kuni saldo vastab parasjagu kättesaadavatele kaupadele. Kassapidajal puudub võimalus valida kaart, mida kasutada kättesaadavate kaupade eest maksmiseks. 

## <a name="related-topics"></a>Seotud dokumendid

- [Maksete KKK](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
