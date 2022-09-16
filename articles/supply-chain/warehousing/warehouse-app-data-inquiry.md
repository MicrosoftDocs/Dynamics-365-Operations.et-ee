---
title: Andmepäringud Warehouse Managementi mobiilirakenduse kõrvalepõigete kaudu
description: See artikkel kirjeldab, kuidas konfigureerida andmepäringu mobiilse seadme menüü-üksuseid ja kasutada neid dekrüptimisosana.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 39677ebfb9babeb7246ece4d27ab1813435ca12e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427844"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Andmepäringud Warehouse Managementi mobiilirakenduse kõrvalepõigete kaudu

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Funktsiooni sissejuhatus

Vöötkoodide skannimise võimaluse pakkumisega annab laohalduse mobiilirakendus teile lihtsa ja täpse viisi andmete hõivamiseks osana laoprotsessidest. Vöötkoodid on mõnikord kahjustatud ja muutuvad loetamatuks või ei pruugi teie äriprotsessi voogudes vöötkoodina olla vajalikku teavet. Sellisel juhul võib andmete käsitsi sisestamine võtta palju aega ning põhjustada isegi valede andmete hõivamise. Tulemused võivad vähendada mõjusust ja madalamat teenusetaset.

Paindliku andmepäringu protsessi abil saavad töötajad hõlpsalt otsida nõutud teavet manustatud laohalduse mobiilirakenduste voogude osana ja rakendada filtreerimisvalikuid nii, et kuvataks ainult asjakohased andmed. Seetõttu on käsitsi valimine kiirem ja täpsem.

Näiteks ostutellimuse vastuvõtuvoos on saabuva kaubavaru vastendamiseks vajalik ostutellimuse number. Selle protsessi osana saate hõlpsalt konfigureerida menüü-üksuseid, et pakkuda kaardiloendi kuva vastavate ostutellimuste numbrite kohta. Nii saate vastuvõtuvoogu jätkata, kasutades kiireid valikuid. See artikkel annab näidisstsenaariume, kuid funktsiooni saab kasutada ka mis tahes või kõigi laohalduse mobiilirakenduste voogude piires.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Lülitage sisse andmepäringu voo funktsioon ja selle eeltingimused.

Enne kui saate kasutada selles artiklis kirjeldatud funktsioone, peate nõutavate funktsioonide sisse lülitamiseks sooritama järgmise protseduuri.

1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**. (Lisateavet selle kohta, kuidas kasutada **Funktsioonihalduse** tööruum, vt funktsioonihalduse [ülevaadet](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Kui käitate tarneahela halduse versiooni 10.0.28 või varem, lülitage sisse funktsioon, mis on loetletud järgmisel viisil:

    - **Moodul:** *laohaldus*
    - **Funktsiooni nimi:** *laorakenduse etapiviisilised juhised*

    See funktsioon on laohalduse rakenduse andmete *päringuvoo funktsiooni eeltingimus*. Tarneahela halduse versiooni 10.0.29 puhul on see kohustuslik ja seda ei saa välja lülitada. Funktsiooni *Laorakenduse toimingujuhised* kohta lisateabe saamiseks vaadake jaotist [Warehouse Management mobiilirakenduse etappide pealkirjade ja juhiste kohandamine](mobile-app-titles-instructions.md).

1. Lülitage sisse järgmisel viisil loetletud funktsioon:

    - **Moodul:** *laohaldus*
    - **Funktsiooni nimi:** *Warehouse management rakenduse ümbersuunamised*

    See funktsioon on laohalduse rakenduse andmete *päringuvoo funktsiooni eeltingimus*. Tarneahela halduse versiooni 10.0.29 puhul on see vaikimisi sisse lülitatud. Lisateavet laohalduse rakenduse *taastlemisfunktsiooni* kohta vt mobiilse [seadme menüü-üksuste etappide konfigureerimisest](warehouse-app-detours.md).

1. Kui laohalduse *rakenduse de pööramise funktsioon ei olnud juba sisse lülitatud, värskendage laohalduse mobiilirakenduse väljanimesid,* **\>\> häälestage laohalduse häälestuse \> mobiilse seadme rakenduse väljanimed** ja valige käsk **Loo vaikehäälestus.** Korrake seda sammu iga juriidilise isiku (ettevõtte) puhul, kus te kasutate laohalduse mobiilirakendust. Lisateavet vt [Mobiilirakenduse Warehouse Management väljade konfigureerimine](configure-app-field-names-priorities-warehouse.md).
1. Lülitage sisse järgmisel viisil loetletud funktsioon:

    - **Moodul:** *laohaldus*
    - **Funktsiooni nimi: laohalduse** *rakenduse andmete päringuvoog*

    See funktsioon on see, mida kirjeldatakse selles artiklis.

## <a name="example-scenarios"></a>Näidisstsenaariumid

See artikkel kasutab näidestsenaariume, et näidata, kuidas saate kasutada *laohalduse rakenduse andmepäringu voo* funktsiooni ostu sissetuleku voo parandamiseks. Stsenaariumid kasutavad standardseid näidisandmeid, mis sisaldavad voogu nimega Ostu *saamine*. See voog algab, paludes töötajatel määrata ostutellimuse numbri, mille suhtes nad saavad. Selleks, et aidata töötajatel lihtsam ostutellimust tuvastada, täiustate voo esimest lehekülge järgmiste uute päringuvalikute lisamisega [:](warehouse-app-detours.md)

- **Ostu loendisse otsige** hankija kaupa – avage leht, mis palub töötajatel sisestada hankija nime või osa hankija nimest. Kasutada saab metamärke. Näiteks, kui *töötaja ootab täna hankijalt sissetulevat tarnet, mille nimes sisaldub Enamjaoks Tassepin*, saab ta **sisestada kaartide komplekti avatud ostutellimustele, \*** mis seda teksti sisaldavad. Igal kaardil on mitu välja, mis annavad teavet iga ostutellimuse kohta. Lisaks hankija nimele saate kujundada kaarte nii, et need näitaksid hankija kontonumbrit, tarnekuupäeva ja dokumendi olekut.
- **Vaadake tänast POS-i** – avage leht, mis ei vii töötajatelt andmeid sisestama, vaid näitab hoopis eelkonfigureeritud filtreid (nt tänane kuupäev). Seejärel kuvab lehekülg kaartide komplekti, mis filtriga sobivad. Töötajad jätkavad, valides kaardi ostutellimusele, mille jaoks nad soovivad registreerida lao kaubad.
- **POS-i mine** kauba alusel – avage leht, mis palub töötajatel skannida saabunud laovarude mis tahes kauba vöötkoodi. Seejärel loetleb voog kõik avatud ostutellimused, mis sisaldavad skannitud kaubakoodi ridu. Et katta olukordi, kus vöötkoodi ei saa lugeda, saate lisada sellele leheküljele teise otsingu, mis lubab töötajatel otsida kaubakoode kindlal ostutellimusel.

Igal juhul tuvastab töötaja ostutellimuse, valides kaardi ja seejärel tagastatakse esimesele leheküljele, mis näitab valitud ostutellimuse numbrit. Töötaja saab sissetulevat laokauba registreerimisvoogu jätkata.

## <a name="enable-sample-data"></a>Luba näidisandmed

Selles artiklis kirjeldatud näidisstsenaariumide läbimiseks peate olema süsteemis, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Lisaks peate enne alustamist valima *USMF-i* juriidilise isiku (ettevõtte).

## <a name="configure-the-mobile-device-menu-items"></a>Mobiilse seadme menüü-üksuste konfigureerimine

Kõigi uute päringuvalikute loomiseks, mille peate voo esimesele leheküljele lisama, peate selle seadistama mobiilse seadme menüü-üksusena. Hiljem teete päringuvalikud kättesaadavaks ostu vastuvõtuvoo *dekoostena*.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Menüükäsu "Otsi ostukaod hankija kaupa" loomine

Järgmiste sammude **abil looge hankija menüü** üksuse alusel valik Otsi ostukaod.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Tegevuspaanil valige mobiilse **seadme** menüü-üksuse lisamiseks uus.
1. Seadke uuele menüükäsule järgmised väärtused:

    - **Menüükäsu nimi:** *ostude otsimine hankija järgi*
    - **Pealkiri:** *ostude/ostude otsimine hankija alusel*
    - **Režiim:** *Kaudne*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Tegevuse kood:** *andmete päring*
    - **Kasuta protsessijuhendit:** *Jah* (see väärtus valitakse automaatselt.)
    - **Tabeli nimi:** *PurchTable* (soovite otsida selle tabeli ostutellimuse numbreid.)

1. Valitud alustabelil **(sellisel** juhul ostutellimuste tabelis) põhineva päringu määratlemiseks valige tegevuspaanil suvand Redigeeri päringut.
1. Lisage päringuredaktori vahekaardil **Vahemik** ruudustikku järgmised read.

    | Tabel | Tuletatud tabel | Väli | Kriteerium |
    |---|---|---|---|
    | Ostutellimused | Ostutellimused | Ostutellimuse olek | Avatud tellimus |
    | Ostutellimused | Ostutellimused | Tarnekuupäev | (dayRange (-10,10)) |
    | Ostutellimused | Ostutellimused | Hankija nimi | |

1. Valige nupp **OK**.

    Selles näites on uus menüükäsk konfigureeritud nii, et otsitakse avatud ostutellimused, mis peaksid saabuma igal ajal 10 päeva jooksul möödunud kuni 10 päeva pärast.

    Päringu hankija nime **kriteeriumiveerg** *jäeti* tühjaks. Seetõttu saavad töötajad selle väärtuse määrata laohalduse mobiilirakenduse kasutamisel.

    Kui soovite määrata loendi sortimisjärjestuse, saate sortimise seadistada **vahekaardil Sortimine**.

1. Lisaks päringu määratlemisele tuleb valida, milliseid välju kuvatakse päringuloendi lehel kaartidel. Seepärast valige tegevuspaanil **väljaloend**.
1. **Seadke loendilehel** Väljad järgmised väärtused:

    - **Kuva väli 1:** *PurchId* (see väli kuvatakse iga kaardi päisena.)
    - **Kuva väli 2:** *PurchStatus*
    - **Kuva väli 3:** *PurchName*
    - **Kuva väli 4:** *OrderAccount*
    - **Kuva väli 5:** *deliverydate*
    - **Kuva väli 6:** *displayDocumentStatus()* (see väärtus on kuvamismeetod, nagu lõpus "()" näitab.)

1. Valige toimingupaanil nupp **Salvesta**. Seejärel sulgege leht.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Menüü üksuse "Otsi tänane objektid" loomine

Järgmiste sammude **abil looge tänase menüü üksuse** jaoks valik Otsi POS-i.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Tegevuspaanil valige mobiilse **seadme** menüü-üksuse lisamiseks uus.
1. Seadke uuele kaubale järgmised väärtused:

    - **Menüükäsu nimi:** *vaadake tänast POS-i*
    - **Pealkiri:** *otsitakse tänane kp.<a1/&.*
    - **Režiim:** *Kaudne*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Tegevuse kood:** *andmete päring*
    - **Kasuta protsessijuhendit:** *Jah* (see väärtus valitakse automaatselt.)
    - **Tabeli nimi:** *PurchTable* (soovite otsida selle tabeli ostutellimuse numbreid.)

1. Valitud alustabelil **(sellisel** juhul ostutellimuste tabelis) põhineva päringu määratlemiseks valige tegevuspaanil suvand Redigeeri päringut.
1. Lisage päringuredaktori vahekaardil **Vahemik** ruudustikku järgmised read.

    | Tabel | Tuletatud tabel | Väli | Kriteerium |
    |---|---|---|---|
    | Ostutellimus | Ostutellimus | Ostutellimuse olek | Avatud tellimus |
    | Ostutellimus | Ostutellimus | Tarnekuupäev | (Päev (0)) |

1. Valige nupp **OK**.

    Selles näites on uus menüükäsk konfigureeritud leidma avatud ostutellimusi, mis saabuvad täna.

    Kui soovite määrata loendi sortimisjärjestuse, saate sortimise seadistada **vahekaardil Sortimine**.

1. Lisaks päringu määratlemisele tuleb valida, milliseid välju kuvatakse päringuloendi lehel kaartidel. Seepärast valige tegevuspaanil **väljaloend**.
1. **Seadke loendilehel** Väljad järgmised väärtused:

    - **Kuva väli 1:** *PurchName* (see väli kuvatakse iga kaardi päisena.)
    - **Kuva väli 2:** *PurchId*
    - **Kuva väli 3:** *PurchStatus*
    - **Kuva väli 4:** *DlvMode*
    - **Kuva väli 5:** *DlvTerm*
    - **Kuva väli 6:** *OrderAccount*
    - **Kuva väli 7:** *VendorName()* (See väärtus on kuvamismeetod, nagu lõpus näitab "()".)

1. Valige toimingupaanil nupp **Salvesta**. Seejärel sulgege leht.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Menüükäsu "Otsi kpi-sid üksuse kaupa" loomine

Järgmiste sammude **abil looge menüükäsk** Otsi POS-i.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Tegevuspaanil valige mobiilse **seadme** menüü-üksuse lisamiseks uus.
1. Seadke uuele kaubale järgmised väärtused:

    - **Menüükäsu nimi:** *POS-i üksuse järgi lookamine*
    - **Pealkiri:** *otsitakse POS-i üksuse alusel*
    - **Režiim:** *Kaudne*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Tegevuse kood:** *andmete päring*
    - **Kasuta protsessijuhendit:** *Jah* (see väärtus valitakse automaatselt.)
    - **Tabeli nimi:** *PurchLine* (soovite otsida kaubakoodil põhinevaid ostutellimuse koode reaandmete kaudu.)

1. Valitud alustabelil **põhineva** päringu määratlemiseks valige tegevuspaanil suvand Redigeeri päringut (sel juhul ostutellimuse ridade tabel, *kuid saate kasutada päisega seotud väärtusi PurchTable’iga ühendamise kaudu*).
1. Lisage päringuredaktori vahekaardil **Vahemik** ruudustikku järgmised read.

    | Tabel | Tuletatud tabel | Väli | Kriteerium |
    |---|---|---|---|
    | Ostutellimuse read | Ostutellimuse read | Rea olek | Avatud tellimus |
    | Ostutellimuse read | Ostutellimuse read | Tarnekuupäev | (dayRange (-10,10)) |
    | Ostutellimuse read | Ostutellimuse read | Kaubakood | |

1. Valige nupp **OK**.

    Selles näites on uus menüükäsk konfigureeritud nii, et otsitakse avatud ostutellimuse read, mis saabuvad igal ajal 10 päeva jooksul möödunud kuni 10 päeva jooksul.

    Päringus on kaubakoodi **veerg** *Kriteeriumid* jäetud tühjaks. Seetõttu saavad töötajad määrata selle väärtuse ajal, kui nad kasutavad laohalduse mobiilirakendust.

    Kui soovite määrata loendi sortimisjärjestuse, saate sortimise seadistada **vahekaardil Sortimine**.

1. Lisaks päringu määratlemisele tuleb valida, milliseid välju kuvatakse päringuloendi lehel kaartidel. Seepärast valige tegevuspaanil **väljaloend**.
1. **Seadke loendilehel** Väljad järgmised väärtused:

    - **Kuva väli 1:** *PurchId* (selle välja väärtust kasutatakse iga kaardi päisena.)
    - **Kuva väli 2:** *VendAccount*
    - **Kuva väli 3:** *PurchQty*
    - **Kuva väli 4:** *PurchUnit*
    - **Kuva väli 5:** *PurchStatus*

1. Valige toimingupaanil nupp **Salvesta**. Seejärel sulgege leht.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Lisa uued mobiilse seadme menüü-üksused menüüsse

Teie kolm uut mobiilse seadme menüükäsku on nüüd valmis mobiilse seadme menüüsse lisama. See ülesanne tuleb täita enne, kui menüükäske saab kasutada dekrüptimisprotsessi osana. Selles näites saate luua uue alammenüü ja lisada sellele uusi menüükäske.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige toimingupaanil nupp **Uus**.
1. Seadke uue kirje päisesse järgmised väärtused:

    - **Nimi:** *esitatud*
    - **Kirjeldus:** *esitatud*

1. Valige loendis **Saadaolevad menüüd ja** menüü üksused esimene mobiilse seadme menüükäsk, mille äsja lõite. Seejärel valige paremnoolenupp, et teisaldada see üksus menüüstruktuuri **loendisse**.
1. Korrake eelmise sammu ülejäänud kahe uue menüükäsu puhul.
1. Valige vasakul loendipaanil **peamenüü**.
1. Liikuge loendis **Saadaolevad menüüd ja** menüü üksused jaotiseni **Menüüd ja** valige oma uus **menüü Sees**. Seejärel valige paremnoolenupp, et teisaldada see üksus menüüstruktuuri **loendisse**.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Detiiside konfigureerimine mobiilse seadme sammudes

Häälestuse lõpetamiseks peate nüüd kasutama **derakenduskonfiguratsiooni** *mobiilse seadme sammude lehel, et lisada kolme uut mobiilse seadme menüükäsku ostu vastuvõtuvoos olemasolevale ostutellimuse identimissammele*.

1. Minge laohalduse **häälestusprogrammi \> > mobiilse seadme \> sammudele**.
1. Sisestage **väljale** Filter ostutellimuse *nr*. Seejärel valige *ripploendist Sammu ID:* "PONum".
1. Kui ruudustikust valitakse leitav kirje, valige tegevuspaanil **suvand** Lisa etapi konfiguratsioon. Kuvatavas ripploendis seadke menüükäsu välja **väärtuseks** Ostu *vastuvõtt*. Seejärel valige **dialoogiakna sulgemiseks OK**.
1. Uue etapi konfiguratsiooni üksikasjade lehel (**Ostu vastuvõtu: PONum**) **valige kiirkaardil Saadaolevad eemaldajad (menüü-üksused)** tööriistaribal **suvand** Lisa.
1. Dialoogiboksis Lisa **detiikontei** valige **ja** otsitakse eelnevalt loodud hankija menüü üksuse ostukaod.
1. Valige **OK**, et sulgeda dialoogiboks ja lisada valitud menüükäsk de lisamisloendisse.
1. Valige uus kirjeldus ja seejärel valige käsk **Vali tööriistaribal saatmiseks** väljad.
1. Dialoogiboksis Vali **väljad** **saatmiseks** ärge lisage midagi jaotisse Ostu vastuvõtust saatmine, sest te ei soovi menüüelemendile de lisaväärtusi edastada. Siiski seadke **jaotises Too tagasi POS-id** hankija alusel tühjale reale, mis on juba lisatud, järgmine väärtus:

    - **Kopeeri ostutellimuste otsimiselt hankija järgi:** *ostutellimus*
    - **Kleebi ostu vastuvõtusse:** *ostutellimus*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Korrake samme 4 kuni 9 ülejäänud kahe uue menüükäsu puhul (**vaadake tänast POS-i** **ja otsige POS-i kauba alusel**). Hankija menüü-üksuse **puhul** ei soovi te ostutellimuste otsimiseks andmeid saata, kuid soovite tagastada ostutellimuse numbri.
1. Sulgege leht.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Proovi ostu vastuvõtuvoogu, mille andmepäring on osa detamis

Järgige neid samme, et testida oma uut mobiilirakenduse häälestust.

1. Looge mitu ostutellimust, mille read on laole 51.
1. Minge mobiilsesse seadmesse või emulaatorisse, milles töötab mobiilirakendus Warehouse Management, ja logige sisse lattu 51, kasutades kasutaja ID-d *51* ja parooli *1*.
1. Valige mobiilirakenduse menüüst Sissetulev **ja** seejärel Ostutellimus **võta vastu**.

    Peaksite nägema järgmist lehekülge, mis sisaldab kolme uut menüükäsku.

    ![Ostu vastuvõtmine ostutellimuse numbriga.](media/wma-purchase-receive-po-num-with-detours.png "Ostu vastuvõtmine ostutellimuse numbriga")

1. Proovige erinevaid võimalusi ja pange tähele, et saate saata ostutellimuse numbri tagasi, valides loendist ühe kaardi.

    ![Ostu vastuvõtmine ostutellimuse otsingu abil hankija kaupa, näide 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Ostu vastuvõtmine ostutellimuse otsingu abil hankija järgi, näide 1")

    ![Ostu vastuvõtmine ostutellimuse otsingu kaudu hankija kaupa, näide 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Ostu vastuvõtmine ostutellimuse otsingu kaudu hankija järgi, näide 2")

> [!TIP]
> **Selle** asemel, et käivitada vastuvõtuvoog ostu vastuvõtu menüükäsu kaudu, saate alustada päringuvoost (**\>\> Peamine päring POS-ide otsimine hankija** alusel) ja kutsuda soovitud voo käivitamiseks deebeti, valides loendist ühe kaardi. Selle lähenemise kasutamiseks saate määrata deritta mobiilse seadme sammude lehel, mille sammu ID **väärtus** on **·** *GenericDataInquiryList*. [*Kui laohalduse mobiilirakenduse mitmetasemeline dekrüptimine*](warehouse-app-detours.md) on teie süsteemi jaoks sisse lülitatud, saate vajadusel lisada ka täiendava lahtiütlemise (see funktsioon lisab toe kuni kahele eemaldamistasemele ja seda saab kohandada lisatasemete toetamiseks).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
