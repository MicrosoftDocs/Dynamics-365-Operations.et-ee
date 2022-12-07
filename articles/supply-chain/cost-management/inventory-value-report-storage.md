---
title: Laoväärtuse aruanded
description: See artikkel selgitab, kuidas laoväärtuse aruandeid seadistada, luua ja kasutada. Need aruanded annavad üksikasju teie varude füüsiliste ja finantskoguste ja -summade kohta.
author: JennySong-SH
ms.date: 11/28/2022
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup, InventValueExecutionHistory, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6b21f6a7856526863914aac73d50e5c3a70605e8
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806402"
---
# <a name="inventory-value-reports"></a>Laoväärtuse aruanded

[!include [banner](../includes/banner.md)]

Laoväärtuse aruanded annavad üksikasju teie varude füüsiliste ja finantskoguste ja -summade kohta. Aruandeid saate vaadata mitmel viisil. Näiteks saate kuvada kogusummasid või kandeid või filtreerida kaupu või ajavahemikku. Saate vaadata müüdud kaupade kulu (COGS) väärtusi või lõpetamata toodangu (WIP) väärtusi ja seadistada teisi valikuid.

Laoväärtuse aruannete abil saate teha järgmisi toiminguid:

- Tehke pearaamatu ja lao vastavusseviimine.
- Saate vaadata vaba kaubavaru ja kindla perioodi väärtusi.
- Looge aruande konfiguratsioonid, mis on kohandatud konkreetsele eesmärgile.
- Saate salvestada aruande konfiguratsioone, et neid saaks mitu korda kasutada.
- Aruande käivitamisel saate andmete filtreerimiseks lisada vahemikke.

## <a name="types-of-inventory-value-report"></a>Varude väärtuse aruande tüübid

Laoväärtuse aruannet on kahte tüüpi: laoväärtus **·**  (standardaruanne) ja laoväärtuse **aruande ladustamine**.

### <a name="standard-inventory-value-report"></a>Standardne laoväärtuse aruanne

Standardne **varude väärtuse** aruanne on lihtne aruanne, mis võimaldab teil valida kaasatud teabe ja seejärel näitab seda teavet ekraanil. See ei salvesta tulemusi. Samuti ei paku see interaktiivseid funktsioone filtreerimiseks, süvitsiminekuks, sirvimiseks või eksportimiseks. Seepärast soovitame enamikel juhtudel kasutada **laoväärtuse aruande** ladustamisaruannet.

### <a name="inventory-value-report-storage-report"></a>Laoväärtuse aruande ladustamisaruanne

Laoväärtuse **aruande ladustamisaruanne** esitab väljundi kas Microsofti interaktiivse leheküljena Dynamics 365 Supply Chain Management või eksporditud dokumendina mitmes vormingus.

Aruande brauseris vaatamisel reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt teie konfigureeritud paigutusest. Saate sortida tulemusi, filtreerida neid, minna andmetesse süvitsi ja muud.

Aruande tulemused talletatakse andmeüksuses **Varude väärtus**. Seetõttu saate tulemusi filtreerida ja eksportida eri vormingutesse, näiteks komaeraldusega (CSV) fail või Microsoft Exceli vorming.

Laoväärtuse **aruande ladustamisaruanne on** kasulik, kui väljund sisaldab palju ridu. Näiteks on teil 50 000 kaupa ja ladudeks määratud 300 kauplust. Sel juhul sisaldab väljund palju ridu, kui taotlete varude lõppsaldosid kauba, asukoha ja lao kaupa.

> [!NOTE]
> Laoväärtuse **aruande talletusaruanne** ei sisalda aruande paigutuses määratletud vahesummasid. See ei sisalda ka pearaamatu saldosid, isegi kui need saldod on aruande kavandis määratletud. Vastavusseviimine pearaamatuga tuleb teha proovibilansside abil. Standardne laoväärtuse **aruanne sisaldab** siiski neid vahesummasid ja saldosid.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Laoväärtuse aruande talletusfunktsiooni sisse- või väljalülitamine

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.25 puhul lülitatakse funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*  [vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse tööruumis laoväärtuse aruande talletusfunktsiooni.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a> Määratlege laoväärtuse aruande konfiguratsioonid.

Kasutage lehte **Laoväärtuse** aruanded, et seadistada sisu, mis kaasatakse erinevat tüüpi varude väärtuse aruandesse. Saate määratleda mis tahes arvu aruandetüüpe. Iga kord, kui te loote laoväärtuse aruande tüübi, valite aruande tüübi.

1. Minge kuluhalduse **varude raamatupidamispoliitikate \> häälestuse laoväärtuse \> aruannetele**.
1. Järgige üht neist sammudest.

    - Olemasoleva aruande redigeerimiseks valige see loendipaanil ja seejärel valige tegevuspaanil **redigeeri**.
    - Uue aruande loomiseks valige tegevuspaanil **väärtus** Uus.

1. Seadke uue või valitud aruande päises järgmised väljad:

    - **ID** – sisestage aruande lühike identifikaator. See väärtus peab olema kõigi laoväärtuse aruande konfiguratsioonide seas kordumatu. Seda ei saa pärast uue konfiguratsiooni salvestamist redigeerida.
    - **Nimi** : sisestage aruande kirjeldav nimi.

1. Kui loote uue aruandekonfiguratsiooni, valige tegevuspaanil **salvestamine**, et teha ülejäänud väljad kättesaadavaks.
1. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Kuupäevaintervall** – valige eelmääratletud kuupäevavahemik. Te saate selle kuupäevaintervalli aruande käivitamisel alistada.
    - **Vahemik**: valige *sisestuskuupäev*  *või kande* kellaaeg, sõltuvalt kuupäevast ja kellaajast, mida tuleks kasutada kirjete toomisel aruande jaoks.
    - **Dimensioonikomplekt** – valige dimensioonide kogum, mille jaoks andmeid käitada. (Dimensioonid määratletakse pearaamatus.) Näiteks võite käivitada andmed põhikonto või *põhikonto*  *+ äriüksuse jaoks*. Valitud dimensioonikogumil ei tohi olla rohkem kui kaks dimensiooni. Lisateavet vt teemast [Finantsdimensioonikomplektid](../../finance/general-ledger/financial-dimension-sets.md).

1. Seadke kiirkaardil **Columns** (Veerud) järgmised väljad. Need väljad kontrollivad teie aruande veerge ja andmetüüpe, mida need veerud sisaldavad.

    - **Ladu**– laoväärtuse näitamiseks *määrake* selle valiku väärtuseks Jah. Seejärel saate need väärtused pearaamatukonto saldodega vastavusse viia.
    - **Lõpetamata**  toodangu väärtuse näitamiseks *määrake* selle suvandi väärtuseks Jah. Seejärel saate viia need väärtused vastavusse pearaamatu lõpetamata toodangu konto saldodega. Kui seate valikuks *Jah*, kuvatakse aruandes ainult lõpetamata toodangu olekuga varude füüsilised kogused ja summad. Tootmistellimused, mille olek on Lõpetamata toodang, on komplekteeritud või lõpetatuna kinnitatud, kuid need pole veel lõpetatud.
    - **Edasi lükatud COGS** – seadke see suvand *suvandile* Jah, et kuvada veerg, mis näitab edasilükatud COGS-i füüsilisi koguseid ja laosummasid. Edasilükatud COGS-i näidatakse, kasutades füüsilisi koguseid ja summasid, sest see tasakaalustab saatelehe kogused ja summad.
    - **COGS** – seadke selle suvandi väärtuseks *Jah,* et kuvada veerg, mis näitab COGS-i finantskoguseid ja summasid. COGS-i näidatakse finantskoguste ja -summade kasutamisel, sest see tasakaalustab arve kogused ja summad.
    - **Kasum ja kahjum**  – seadistage see valik *valikule* Jah, et kuvada veerg, mis näitab varude tulu ja kulu kontodele sisestatud finantssummat.
    - **Prindi võrdluse kumulatiivsed kontoväärtused** – määrake selle suvandi väärtuseks *Jah*, et kuvada veerg, mis näitab pearaamatukonto saldot. Sel viisil ei pea te kontrollima jälje saldot. See valik töötab ainult standardse laoväärtuse **aruandega**, mitte laoväärtuse **aruande ladustamisaruandega** . Pärast valiku Jah seadmist *peate* kasutama järgmisi välju iga pearaamatukonto määramiseks, mida soovite loendisse seada, **sõltuvalt** teie lubatud rahalise positsiooni suvanditest.

        > [!NOTE]
        > Kui valite *mõne* välja jaoks summakonto, kuvatakse nii iga kogusumma konto summa kui ka kogusumma konto summa.

        - **Laokonto** – määrake pearaamatukonto, mille laoteavet soovite kuvada. (Mõlemad **Varude** suvand ja prindi **kumulatiivsed kontoväärtused võrdluseks** peavad olema seatud väärtusele *Jah*.)
        - **Lõpetamata toodangu konto** – määrake pearaamatukonto, mille kohta lõpetamata toodangu teavet kuvada. (Mõlemad **Lõpetamata** toodangu suvand ja **prindi kumulatiivsed kontoväärtused võrdluseks** tuleb seada suvandile *Jah*.)
        - **Edasilükatud COGS-konto** – määrake pearaamatukonto, mille edasilükatud COGS-i teavet näidata. (Mõlemad **Edasilükatud COGS-i** suvand ja **võrdluse kumulatiivsete kontoväärtuste printimine** peab olema seatud väärtusele *Jah*.)
        - **COGS-konto** – määrake pearaamatukonto, mille COGS-i teavet kuvada. (Mõlemad **COGS-i** suvand ja **prindi võrdluseks kumulatiivsed kontoväärtused** peavad olema seatud väärtusele *Jah*.)

    - **Füüsiliste ja finantsväärtuste summeerimine** – *seadke* see valik valikule Jah, et kuvada veerg, mis näitab kogu laokogust ja laosummat (nii füüsiliste kui ka finantsilisi laovarude väärtuste kokkuvõtet). Kui see valik on seatud valikule *Ei*, kuvatakse aruandes nii füüsilise kui finantsilise laovaru väärtused.
    - **Kaasa pearaamatusse sisestamata** – määrake selle *suvandi* väärtuseks Jah, et kuvada veerg, milles kuvatakse kanded, mida pole kunagi pearaamatusse sisestatud. Kanded järgmist tüüpi kaupade kohta ei pruugita pearaamatusse sisestada:

        - Saadud ja veel arveldamata kaubad, kui vastava **kauba mudeligrupi** suvand Sisesta füüsiline ladu on tühjendatud.
        - Saadud ja veel arveldamata kaubad, kui suvand Sisesta toote sissetulek pearaamatusse **on**  **·**  **tühjendatud toote sissetuleku kiirkaardil ostureskontro parameetrite lehe vahekaardil Üldine (Ostureskontro**  **·**  ostureskontro häälestus **ostureskontro parameetrid). \>  \>**

    - **Arvuta keskmine ühiku kulu**  – määrake selle suvandi väärtuseks *Jah*, et kuvada veerg, milles kuvatakse keskmine ühiku hind. Keskmine ühikukulu on kogusumma jagatud kogusummaga.
    - **Kogus ja väärtus kokku** – *seadke* see valik valikule Jah, et kuvada veerud, mis näitavad füüsiliste varude (ja finantskoguste) kogust ning füüsiliste varude (ja finantssummade) kogusummat. Saate seada selle suvandi väärtuseks Jah *ainult* siis, kui suvand **Füüsiliste ja finantsväärtuste summeerimine** on seatud valikule *Ei*.
    - **Varude dimensioonid**  – märkige selles ruudustikus **ruut Kuva** iga dimensiooni puhul, mida soovite aruandes kuvada. Aruandes kuvatakse väärtused ainult **nende dimensioonide** puhul, kus suvand Finantsladu on lubatud. Teised dimensioonid kuvavad ainult tühjad veerud. Nende dimensioonide puhul, mida soovite kuvada, saate ka **kogusummade kaasamiseks** valida märkeruudu Kokku.
    - **Ressursi ID** – määrake suvandi **Kuva väärtuseks**  *Jah,* et kuvada veerg, mis identifitseerib iga rea kauba. Seadke suvandi **Kokku väärtuseks**  *Jah,* et kaasata ka kogusummad. Sõltuvalt iga rea loendis olevast kauba tüübist kuvatakse veerus üks järgmistest teabe tüüpidest:

        - **Materjal**  – veerus kuvatakse vastava `ItemID` materjalikirje väljaväärtus.
        - **Tööjõud**  – veerg näitab välja `WorkCenterID` väärtust vastava töökirje jaoks.
        - **Kaudne**  kulu – veerus kuvatakse `CodeID` vastava kulukirje väljaväärtus.

        Kui vaate **suvand**  *·*  **on määratud olekusse Ei nii ressursi ID**  **välja kui ka välja Ressursigrupp** puhul, näete ainult kogu laoväärtust, mis põhineb teie valitud varude dimensioonil.

    - **Ressursigrupp**  – määrake suvandi **Kuva** väärtuseks *Jah,* et kuvada veerg, mis identifitseerib iga rea ressursigrupi. Seadke suvandi **Kokku väärtuseks**  *Jah,* et kaasata ka kogusummad. Sõltuvalt iga rea loendis olevast kauba tüübist kuvatakse veerus üks järgmistest teabe tüüpidest:

        - **Materjal**  – veerus kuvatakse vastava `ItemGroup` materjalikirje väljaväärtus.
        - **Tööjõud**  – veerg näitab välja `WorkcenterGroup` väärtust vastava töökirje jaoks.
        - **Kaudne**  kulu – veerus kuvatakse `CostGroup` vastava kulukirje väljaväärtus. (Väärtus `CostGroupType` peab olema *Kaudne*.)

        Kui vaate **suvand**  *·*  **on määratud olekusse Ei nii ressursi ID**  **välja kui ka välja Ressursigrupp** puhul, näete ainult kogu laoväärtust, mis põhineb teie valitud varude dimensioonil.

1.  **Seadke kiirkaardil** Rows järgmised väljad. Need väljad lasevad teil aruandesse lisada vastavaid lõpetamata toodanguga seotud alamjaotisi või neid eemaldada.

    - **Materjal**  – materjaliteabe näitamiseks *määrake* selle valiku väärtuseks Jah. *Materjal* on vaikimisi ressursitüüp, sest materjalid tuleb kaasata kõigisse aruande konfiguratsioonidesse, et luua töökindel väljund.
    - **Tööjõud**  – määrake see valik väärtusele *Jah*, et näidata WIP-i töökulusid.
    - **Kaudne**  kulu – määrake selle suvandi väärtuseks *Jah*, et näidata WIP kaudseid kulusid.
    - **Otse väljast tellimine** – määrake selle valiku väärtuseks *Jah,* et näidata WIP-i otseseid välisteenuse kulusid. See teave on vajalik allhanke puhul.
    - **Üksikasjade tase** – valige aruandele kuvamissuvand:

        - *Kanded* – saate vaadata kõiki aruande asjakohaseid kandeid. Võite esineda jõudluse probleeme, kui vaatate aruandeid, mis sisaldavad suurt hulka kandeid. Seetõttu, kui soovite kasutada seda kuvamissuvandi, soovitame kasutada varude **väärtuse aruande ladustamisaruannet** .
        - *Kogusummad*  – vaadake kogutulemust.

    - **Algsaldo**  kaasamine – algsaldo näitamiseks *seadke* see valik väärtusele Jah. See valik on saadaval ainult siis, kui välja **Üksikasjade tase** väärtuseks on määratud *Kanded*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Varude väärtuse aruande salvestusaruande loomine

Järgige neid samme varude väärtuse aruande talletusaruande **loomiseks ja salvestamiseks** .

1. Avage **Kuluhaldus \> Päringud ja aruanded \> Varude väärtuse aruande talletus**.
1. Valige toimingupaanil nupp **Uus**.
1.  **Seadke dialoogiboksi Varude** väärtus kiirkaardil **Parameetrid** järgmised väljad:

    - **Nimi** : sisestage aruande kordumatu nimi.
    - **ID** : valige [aruandes kasutamiseks laoväärtuse](#report-configuration) aruande konfiguratsioon. Konfiguratsioon määrab suvandid veergude ja ridade jaoks, mis teie aruandesse kaasatakse.
    - **Kuupäevaintervall** – kasutage käesoleva jaotise välju, et määratleda, millised kirjed aruandesse kaasatakse. Kuupäevaintervalli määratlemiseks saate valida eelseadistatud vahemiku (aruande loomise kuupäeva põhjal) väljal **Kuupäevaintervalli kood** või valida kindlad kuupäevad väljadel **Alguskuupäev** ja **Lõppkuupäev**.

1. Kiirkaarti **kaasadel** kirjetes seadistage filtrid ja piirangud, et määratleda, millised andmed aruandesse kaasatakse. Valige **filter**, et avada standardpäringu redaktori dialoog, kus saate määratleda valikukriteeriumid, sortimiskriteeriumid ja liitmised. Väljad töötavad samamoodi nagu muudel päringutüüpidel Supply Chain Management puhul. Kõiki neid filtreid rakendatakse laokannetele, kuid mitte pearaamatu saldole. Pidage seda käitumist silmas, kui seadistate oma filtrid. Vastasel juhul võite näha lahknevust varude ja pearaamatu vahel.
1. Määrake kiirkaardil **Käivita taustal** kuidas, millal ja kui sageli aruanne luuakse. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.

    > [!NOTE]
    > See aruanne käivitatakse alati pakett-töö osana.

1. Valige **OK**, et rakendada oma sätted ja sulgeda dialoogiboks.

Pärast pakett-töö lõpetamist kuvatakse aruanne lehel **Varude väärtuse aruande talletus**. Aruande nägemiseks peate võib-olla lehte värskendama.

> [!IMPORTANT]
> Valitud laoväärtuse aruande konfiguratsioonis võib teil olla vale algsaldo, **·**  **kui valite sama kuupäeva nii väljal Alates kui ka väljal Kuni kuupäevani** ning **kui seate suvandi Kaasa**  *algsaldo väärtuseks Jah.*

## <a name="explore-an-inventory-value-report-storage-report"></a>Varude väärtuse aruande ladustamisaruande avastamine

Pärast aruande loomist saate igal ajal seda vaadata ja sellega tutvuda järgmisel viisil.

1. Avage **Kuluhaldus \> Päringud ja aruanded \> Varude väärtuse aruande talletus**.
1. Valige loendist aruanne. Lehel kuvatakse laoväärtuse aruande [konfiguratsiooni üksikasjad](#report-configuration) , mida kasutati valitud aruande loomiseks.
1. Tegevuspaanil valige aruande **sisu** kuvamiseks suvand Kuva üksikasjad.
1. Tutvuge aruandega mis tahes järgmist sammu järgides.

    - Nagu enamiku standardsete lehtede puhul Supply Chain Managementis saate valida peaaegu mis tahes veerupäise, et sortida või filtreerida ruudustikku selle veeru väärtuste järgi.
    - Kasutage välja **Filter**, et filtreerida aruannet mis tahes saadaoleva veeru väärtuse alusel.
    - Kasutage vaatemenüüd (välja **Filter** kohal), et salvestada ja laadida oma sortimise ning filtreerimise lemmikkombinatsioone.

## <a name="export-an-inventory-value-report-storage-report"></a><a name="export-stored-report"></a> Varude väärtuse aruande eksportimine ladustamisaruandena

Iga loodud aruanne talletatakse andmeüksuses **Varude väärtus**. Saate kasutada Supply Chain Managementi standardseid andmehaldusfunktsioone, et eksportida selle üksuse andmed mis tahes toetatud vormingusse, sh CSV või Exceli vorming.

Järgmine näide näitab, kuidas eksportida laoväärtuse **aruande ladustamisaruannet** .

1. Minge jaotisse **Süsteemihaldus \> Tööruumid \> Andmehaldus**.
1. Valige jaotises **Import/eksport** paan **Eksport**.
1.  **Kuvataval** ekspordilehel seadistage eksporditöö. Sisestage esimesena töö grupi nimi.
1. Valige jaotises **Valitud üksused** käsk **Lisa üksus**.
1. Määrake järgmised väljad kuvatavas dialoogiboksis.

    - **Üksuse nimi** – valige *Varude väärtus*.
    - **Sihtandmete vorming** – valige vorming, millesse andmed eksportida.

1. Valige käsk **Lisa**, et lisada uus rida, ja seejärel klõpsake nuppu **Sulge**, et sulgeda dialoogiboks.
1. Tavaliselt ekspordite korraga ühe aruande. Ühe aruande eksportimiseks seadistage selle rea filter, mille te just dialoogiboksis **Päringud** lisasite. Sel viisil saate määratleda, milline **Varude väärtuse** üksuse aruanne kaasatakse teie eksporti. Ühe aruande eksportimiseks seadke järgmised filtri valikud järgmisi samme järgides.

    1. Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida.
    2. Seadke välja **Tabel** väärtuseks *Varude väärtus*.
    3. Seadke välja **Tuletatud tabel** väärtuseks *Varude väärtus*.
    4. Määrake välja **Väli** väärtuseks väli, mille alusel soovite filtreerida. Tavaliselt kasutate täitmisnime **välja** ja/või täitmisaja **välja**.
    5. Seadke väli **Kriteeriumid** väärtusele, mida soovite valitud väljal otsida. (Kui valisite eelmises etapis välja **Käivitamise nimi**, on see väärtus aruande nimi. Kui valisite välja **Käivitamise aeg**, on see aruande loomise kellaaeg.)
    6. Vajadusel lisage tabelisse **Vahemik** veel ridu, kuni olete otsitava aruande üheselt identifitseerinud.

1. Valige **OK**, et salvestada oma sätted ja sulgeda dialoogiboks.
1. Oma ekspordi seadistuse salvestamiseks valige **Salvesta**.
1. Valige vahekaardil **Eksportimise suvandid** käsk **Ekspordi kohe**, et luua eksportimise fail.
1. Avanenud lehel **Käivitamise kokkuvõtte** saate vaadata oma ekspordi töö olekut ja eksporditud üksuste loendit. Valige jaotises **Üksuse töötlemise olek** loendist üksus **Varude väärtus** ja seejärel valige suvand **Laadi fail alla**, et laadida alla sellest üksusest eksporditud andmed.

Lisateavet andmete eksportimiseks andmehalduse kasutamise kohta vt [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="delete-stored-inventory-value-reports"></a>Talletatud laoväärtuse aruannete kustutamine

Kui talletatud laoväärtuse aruannete arv suureneb, võib juhtuda, et nad hakkavad lõpuks andmebaasis liiga palju ruumi enda alla võtma. See olukord võib mõjutada süsteemi jõudlust ja põhjustada kõrgemaid andmete talletuskulusid. Seetõttu on võimalik, et peate aruandeid aeg-ajalt puhastama, kustutades vanemad aruanded.

> [!IMPORTANT]
> Enne mõne eelnevalt loodud laoväärtuse [aruande](#export-stored-report) kustutamist soovitame tungivalt esmalt aruanded eksportida ja need väliselt talletada, sest te ei pruugi hiljem neid uuesti luua. Selline piirang on olemas, kuna laoväärtuse aruande loomisel töötab süsteem tänasest tagasi ja töötleb iga laokande kirjet töid vastupidises järjestuses. Kui proovite aruande loomisel liiga palju tagasi vaadata, võib töödeldavate kannete maht lõpuks saada nii suureks, et süsteem ei saa aruande loomise lõpule viia. Kaugus minevikust, mille kohta saate luua uusi aruandeid, sõltub laokannete arvust, mis teil on süsteemis vastava ajavahemiku jooksul.

### <a name="delete-one-report-at-a-time"></a>Ühe aruande kustutamine korraga

Järgige neid samme, et kustutada üks salvestatud aruanne korraga.

1. [Eksportige aruanne](#export-stored-report) , mida plaanite kustutada ja salvestada välisesse asukohta tulevaseks viiteks.
1. Avage **Kuluhaldus \> Päringud ja aruanded \> Varude väärtuse aruande talletus**.
1. Valige loendi paanil aruanne, mida soovite kustutada.
1. Valige tegumiribal suvand **Kustuta**.
1. Hoiatusteade tuletab teile meelde loodud aruandeid varundada. Valige **Jah**, kui olete kustutamise jätkamiseks valmis.

### <a name="delete-several-reports-at-the-same-time"></a>Mitme aruande üheaegne kustutamine

Järgige neid samme mitmete talletatud aruannete üheaegne kustutamiseks.

1. [Eksportige kõik aruanded](#export-stored-report) , mida plaanite kustutada ja ladustage need välisesse asukohta edasiseks viiteks.
1. Minge kuluhalduse **varude \> raamatupidamise laoväärtuse \> aruande \> andmete puhastamisele**.
1. Dialoogiboksis Laoväärtuse **aruande andmete**  **puhastamine** valige väljalt Laoväärtuse aruande kustutamine, mis käivitatud enne välja kuupäev, milleni tuleb kõik laoväärtuse aruanded kustutada.
1. Kiirkaarti **kaasamiskirjetes** saate määrata täiendavad filtritingimused, et piirata kustutamist vajaminev aruannete kogum. Valige **filter**, et avada standardne päringuredaktor, kus saate määrata kustutamisaruannete atribuudid.
1. Kiirkaardil **Käivita taustal** saate määrata, kuidas, millal ja kui sageli tuleks aruandeid kustutada. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul. Tavaliselt käivitate te seda tööd siiski iga kord käsitsi, kui seda vajatakse.
1. Määratud **aruannete kustutamiseks valige OK** .

## <a name="generate-a-standard-inventory-value-report"></a>Standardse varude väärtuse aruande loomine

Kasutage järgmist protseduuri standardse laoväärtuse **aruande loomiseks** .

1. Minge kuluhalduse päringute ja aruannetesse Laoarvestus **– olekuaruanded Laoväärtus \>  \> . \>**
1.  **Seadke dialoogiboksi Laoväärtuse** aruanne kiirkaardil **Parameetrid** järgmised väljad:

    - **Nimi** : sisestage aruande kordumatu nimi.
    - **ID** : valige [aruandes kasutamiseks laoväärtuse](#report-configuration) aruande konfiguratsioon. Konfiguratsioon loob suvandid veergude ja ridade jaoks, mis teie aruandesse kaasatakse.
    - **Kuupäevaintervall** – kasutage käesoleva jaotise välju, et määratleda, millised kirjed aruandesse kaasatakse. Kuupäevaintervalli määratlemiseks saate valida eelseadistatud vahemiku (aruande loomise kuupäeva põhjal) väljal **Kuupäevaintervalli kood** või valida kindlad kuupäevad väljadel **Alguskuupäev** ja **Lõppkuupäev**.

1. Kiirkaarti **kaasadel** kirjetes seadistage filtrid ja piirangud, et määratleda, millised andmed aruandesse kaasatakse. Valige **filter**, et avada standardpäringu redaktori dialoog, kus saate määratleda valikukriteeriumid, sortimiskriteeriumid ja liitmised. Väljad töötavad samamoodi nagu muudel päringutüüpidel Supply Chain Management puhul.
1. Määrake kiirkaardil **Käivita taustal** kuidas, millal ja kui sageli aruanne luuakse. Väljad töötavad samamoodi nagu muud tüüpi [taustatööl](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Management puhul.
1. Valige **OK**, et rakendada oma sätted ja sulgeda dialoogiboks. Kuvatakse aruanne.

## <a name="reading-inventory-value-reports"></a>Varude väärtuse aruannete lugemine

See jaotis annab mõningaid juhiseid, kuidas lugeda ja mõista laoväärtuse aruannet.

Tarneahela haldus toetab kaht järgmist varude olekuga seotud olulist kontseptsiooni:

- **Finantsilt**  uuendatud – see mõiste näitab, et laokanded on juba arveldatud. Tootmistellimuste puhul näitab see tootmistellimuse lõppu.
- **Füüsiliselt uuendatud**  – see mõiste näitab, et laokandeid pole veel arveldatud, kuid need on saadud või saadetud. Tootmistellimuste puhul näitab see, et materjal on komplekteeritud või tootmistellimus on lõpetatuna kinnitatud.

Kui mõistate neid kahte mõistet, peaks aruande väljundi järgnevaid veerge olema lihtne mõista:

- **Varud: rahaline**  kogus – finantsiliselt uuendatud kogus.
- **Varud: rahaline**  summa – finantsiliselt uuendatud laosumma väärtus.
- **Varud: füüsiline kogus on**  sisestatud – füüsiliselt uuendatud kogus.
- **Varud: sisestatud füüsiline**  summa – füüsiliselt uuendatud laosumma väärtus.
- **Varud: füüsiline kogus on sisestamata**  – kogus, mis on laokannetega, kuid mida pole pearaamatusse sisestatud. Näiteks on teil kauba **mudeligrupp**  **·**, kus tühjendatakse suvand Sisesta füüsiline ladu ja Sisesta finantsiline laovaru ning teil on kaup, mis on selle grupiga lingitud. Seejärel loote ostutellimuse, saate selle vastu ja arveldate. Kui vaatate üle kauba laoväärtuse aruande, näete, et ostutellimuse kogus ja väärtus kuvatakse **veergudes Ladu:**  **Sisestamata füüsiline kogus ja Ladu: füüsiline** summa.
- **Varud: füüsiline summa on sisestamata** – saate seadistada oma aruanded nii, et need kuvavad sisestamata summasid. Kuid kui kasutate varude vastavusseviimise aruannet, siis ärge seda väärtust kasutage. Vastasel juhul summat pearaamatusse ei sisestata.
- **Varud:**  kogus – aruande kõigi koguseveergude kogusumma.
- **Varud:**  summa – aruande kõigi summaveergude kogusumma. Kui teete varude vastavusseviimist, siis ärge kasutage **seda veergu, kui teie aruanne sisaldab veergu Varud: füüsiline summa on sisestamata** . Sellisel juhul tuleb kogusummast välja arvata **lao** füüsiline summa, mida pole sisestatud.
- **Keskmine ühikukulu**  – kogusumma jagatud kogusummaga.

Tavaliselt kasutate laoväärtuse aruannet laoväärtuse ja koguse vaatamiseks. Mõnikord siiski ei näidata aruandes kõiki asjakohaseid varude dimensioone. Kui te ei näe dimensioone, mida eeldate, kontrollige järgmisi sätteid:

- Vaadake üle kauba ladustamis- ja jälgimisdimensioonigrupid. Aruandes saab kuvada ainult **neid dimensioone**, kus suvand Finantsiline laovaru on lubatud.
- Minge kuluhalduse **\>  \>** varude raamatupidamispoliitikate häälestuse laoväärtuse aruannetesse, valige aruande loomiseks kasutatud aruande konfiguratsioon ja veenduge, et veerus Vaade on valitud vajalikud varude **dimensioonid.** 

Näiteks on teil kaup, mille kaubakood on *A0001*. Laoala dimensioonide grupis on finantsiline laovaru lubatud ainult laoala. Füüsilise lao puhul on nii sait kui ka ladu lubatud. Jälgimisdimensioonigrupis on partiinumber lubatud füüsilise laovaru jaoks, kuid mitte finantsilise laovaru jaoks. Seejärel kasutage aruande konfiguratsiooni, kus ala, ladu ja partii number on kõik valitud. Kui vaatate aruannet, näete väärtust ainult saidile. Lao veerud ja partiinumber on tühjad. Nagu see näide näitab, saavad laoväärtuse aruanded näidata ainult varude dimensioone, mis on finantsilise laovaru puhul lubatud.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
