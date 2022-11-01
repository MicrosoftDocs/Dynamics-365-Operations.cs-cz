---
title: Balení kontejnerů pro dodávku
description: Tento článek popisuje proces balení, který umožňuje ověřit skladové položky a zabalit je do kontejnerů.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708776"
---
# <a name="pack-containers-for-shipment"></a>Balení kontejnerů pro dodávku

[!include [banner](../../includes/banner.md)]

Proces balení kontejnerů umožňuje ověřit skladové položky a zabalit je do kontejnerů. Během tohoto procesu skladníci obvykle vybírají skladové položky z velkoobjemových skladovacích prostor a přesouvají je do balicí oblasti. Více skladníků tam kontroluje množství a typy položek a přiřazuje je k příslušným velikostem kontejnerů. Po plném zabalení kontejneru se uzavře a přesune do výstupního překladiště, kde je připraven k expedici.

Kontejnery představují fyzické struktury, do kterých jsou položky zabaleny, a vy můžete v systému sledovat informace o kontejnerech. Tyto informace mohou být užitečné při plánování přepravy, zejména pokud počítáte přepravní poplatky na základě kontejnerů. Před odesláním můžete zobrazit počet kontejnerů použitých v zásilce, typy kontejnerů, které se používají, a fyzické rozměry každého kontejneru (jako je celkový objem a hmotnost).

S kontejnery lze použít několik souvisejících funkcí odchozího skladu. Další informace naleznete v následujících článcích:

- [Kontejnerizace ve vlnách](wave-containerization.md)
- [Odchozí třídění](outbound-sorting.md)
- [Expedice malých balíků](small-parcel-shipping.md)
- [Potvrdit a převést](confirm-and-transfer.md)
- [Nastavení různých rozměrů pro balení a skladování](packing-vs-storage-dimensions.md)
- [Balicí práce pro balení odchozích kontejnerů a zpracování zásilek](packing-work.md)
- [Balení kontejnerů pomocí mobilní aplikace Warehouse Management](warehouse-app-packing-containers.md)
- [Příkladový scénář – Balení kontejnerů pomocí mobilní aplikace Warehouse Management](warehouse-app-pack-containers-scenario.md)
- [Vytisknout popisky kontejneru](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Nastavení skladu pro použití ručních operací balení

Existují dva základní způsoby, jak organizovat odchozí operace:

- **Tvorba a zpracování vln** – Pracovníci vybírají položky na základě práce odchozího skladu. Položky pak umístí přímo na místo odeslání, kde jsou připraveny k okamžité expedici. Další informace o nastavení a použití tohoto procesu naleznete v tématu [Vytváření a zpracování vln](wave-processing.md).
- **Ruční balení na balírnách** – Tento proces má další operaci mezi vychystáváním a expedicí. Místo vložení inventáře do *místa odeslání na nákladové bráně* ho pracovníci vloží do *místa balení*. Poté řídí proces balení na balicí stanici pomocí stránky **Balení** ve webovém klientovi. K umožnění tohoto procesu musíte nakonfigurovat systém podle popisu v této části.

### <a name="set-up-warehouse-locations-for-packing"></a>Nastavení skladových míst na balení

Musíte mít alespoň jedno balicí místo, kam budou pracovníci vkládat skladové položky, aby je bylo možné zabalit do kontejnerů. Další informace o vytváření skladových míst viz [Nastavení skladu a Konfigurace umístění ve skladu podporujícím WMS](tasks\configure-locations-wms-enabled-warehouse.md). Následující podsekce popisují, jak vytvořit a nastavit místa balení.

#### <a name="set-up-location-types-for-packing"></a>Nastavení typů míst pro balení

Musíte definovat *typ místa* pro místa balení. Typy skladových míst lze použít jako možnosti filtrování k řízení různých procesů správy skladu. Název každého typu místa obvykle popisuje, jak by se měl daný typ místa používat. Typ místa, který zde nastavíte, musí být přidružen ke každému místu, které se používá pro operace balení.

Chcete-li nastavit typ místa, postupujte podle následujících pokynů.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Typy umístění**.
1. V podokně Akce vyberte možnost **Nový** pro přidání typu místa do mřížky.
1. Nastavte následující pole pro nový typ místa:

    - **Typ místa** – Zadejte název typu místa. Každý název musí být jedinečný a měl by popisovat, jak má být typ místa použit.
    - **Popis** – zadejte krátký popis typu místa.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Informování systému o typu místa balení

Po vytvoření typu místa musíte nastavit systém tak, aby ho rozpoznal jako typ umístění, který se má použít pro operace balení.

Chcete-li nastavit typ místa, které se používá pro operace balení, postupujte podle těchto kroků.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**
2. Na kartě **Všeobecné** na pevné záložce **Typy míst** nastavte pole **Typ místa balení** na typ místa, které budete používat k identifikaci balíren.

> [!NOTE]
> Pokud upgradujete z verze Microsoft Dynamics AX, stav *Probíhá balení* byl odstraněn ze zásilek a nákladů, protože nefungoval konzistentně a způsoboval nadbytečná data. Proto jsou stránky seznamů **V dodávkách** a **Náklady v balení** zastaralé. Kontejnery, které musí být zabaleny, jsou sledovány na úrovni místa.
>
> V předchozích verzích jste definovali místo balení pomocí pole **ID profilu pro místo balení** na kartě **Balení** stránky **Parametry řízení skladu** k určení *profilu místa*. V aktuální verzi používáte **typ místa balení** na kartě **Všeobecné** stránky **Parametry řízení skladu** k určení *typu umístění*, jak je popsáno v tomto článku. Nové pole je lépe sladěno s procesem identifikace míst zastávek a konečných míst expedice.
>
> I když můžete nadále používat staré pole **ID profilu pro místo balení**, doporučujeme začít používat nové pole **Typ místa balení**, protože staré pole bude nakonec zastaralé.
>
> Pokud vymažete nastavení starého pole **ID profilu pro místo balení** a poté stránku uložíte, pole bude trvale zakázáno. Pro instalace, kde pole **ID profilu pro místo balení** nebylo nikdy použito, bude vždy zakázáno. Po vymazání nastavení pole **ID profilu pro místo balení** použijte nastavení popsaná v tomto článku k nastavení a identifikaci místa balení.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Nastavení profilů místa pro místa balení

Každý *profil místa* určuje informace a pravidla, která se vztahují na přidružená místa. Protože pro operace balení potřebujete alespoň jedno místo, musíte pro něj kromě typu místa vytvořit profil umístění. Každý profil lze použít na libovolném počtu míst. Místa, která se používají pro balení, musí být nastavena tak, aby sledovala registrační značky.

Chcete-li nastavit profil umístění pro místo balení, postupujte podle těchto kroků.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.
1. Buď vyberte existující profil v podokně seznamu, nebo vyberte v podokně akcí možnost **Nový** a vytvořte nový.
1. V záhlaví nového nebo vybraného profilu nastavte následující pole:

    - **ID profilu místa** – Zadejte jedinečné ID profilu.
    - **Název** – Zadejte popisný název profilu.

1. Na pevné záložce **Obecné** zadejte následující pole:

    - **Formát místa** – Vyberte formát místa, který se má použít pro aktuální místo. Formáty skladového místa představují systém pojmenování pro vytváření jedinečných a konzistentních názvů pro pozice přihrádky skladového místa používané ve skladu. Pokud ještě nemáte formát, který potřebujete, můžete ho vytvořit přechodem na **Správa skladu \> Nastavení \> Sklad \> Formáty místa**. Další informace viz [Konfigurace umístění ve skladu podporujícím WMS](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Typ místa** – Vyberte typ místa, který je nastaven jako typ místa balení na stránce **Parametry řízení skladu**, jak je popsáno dříve v tomto článku.
    - **Použít sledování registrační značky** – Pro místa balení nastavte tuto možnost na *Ano*. Systém musí být schopen sledovat ID registračních značek v místech balení, aby mohl řídit proces balení.
    - **Povolit negativní skladové zásoby** – Pro místa balení nastavte tuto možnost na *Ne*.
    - **Povolit smíšené položky** – Pro místa balení nastavte tuto možnost na *Ano*. Toto nastavení je vyžadováno, protože na balicí místa se obvykle dopravuje mnoho různých čísel položek současně.
    - **Povolit smíšené stavy skladu** – Pro místa balení nastavte tuto možnost na *Ano*. Toto nastavení je vyžadováno, protože na balicí místa se obvykle dopravují položky s různými stavy skladu současně.
    - **Povolit smíšené dávky skladu** – Pro místa balení nastavte tuto možnost na *Ano*. Tato možnost je automaticky nastavena na *Ano*, když je možnost **Povolit smíšené položky** nastavena na *Ano*.

#### <a name="set-up-packing-locations"></a>Nastavení míst balení

Musíte mít alespoň jedno *místo*, kam budou pracovníci vkládat skladové položky, které musí být zabaleny do kontejnerů.

K nastavení místa balení postupujte následovně.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění**.
1. V podokně Akce vyberte možnost **Nový** a přidejte místo.
1. Nastavte následující pole pro nové místo:

    - **Sklad** – Určete sklad, kde místo balení musí existovat.
    - **Místo** – Zadejte název nového místa.
    - **ID profilu místa** – Nezapomeňte zadat ID, které jste vytvořili v předchozí části.

## <a name="set-up-the-packing-process"></a>Nastavení procesu balení

Tato část popisuje, jak nakonfigurovat nastavení, která umožňují proces balení a umožňují pracovníkům zabalit skladové zásoby do kontejnerů.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Nastavení zásad balení kontejneru

Každé *zásady balení kontejnerů* definují, jak má být kontejner zpracován. Pokaždé, když vytvoříte nový kontejner, vyberete také zásady balení kontejneru, které se na něj vztahují.

Pokud chcete nastavit zásady balení kontejneru, postupujte následovně.

1. Přejděte na **Řízení skladu \> Nastavení \> Kontejnery \> Zásady balení kontejneru**.
1. Buď vyberte existující zásady v podokně seznamu, nebo vyberte v podokně akcí možnost **Nový** a vytvořte nové.
1. V záhlaví nové nebo vybrané zásady nastavte následující pole:

    - **Zásady balení kontejnerů** – Zadejte jedinečný název zásady.
    - **Popis** – Zadejte popisný název zásad.

1. Na kartě **Přehled** natavte následující pole. Tato pole vám umožňují určit, jaké akce mají být provedeny, když je kontejner uzavřen, zda pracovat s vytvářením práce, nebo bez a kdy by měl být kontejner uvolněn z balicí stanice.

    - **Sklad** – Vyberte sklad, kde zásady balení platí.
    - **Výchozí místo pro konečnou zásilku** – Určete preferované umístění kontejneru po jeho zavření. Toto pole je k dispozici jen, když je pole **Zásady uvolnění kontejneru** nastaveno na možnost *Zpřístupnit v konečném skladovém místě*.
    - **Výchozí místo pro třídění** – Toto pole se používá s funkcí [odchozí třídění](outbound-sorting.md).
    - **Jednotka hmotnosti** – Vyberte výchozí měrnou jednotku, která se použije, když je kontejner uzavřen a manifestován. Obvykle bude tato měrná jednotka měrnou jednotkou, kterou používá váha v balicí stanici. Toto pole se vztahuje na zásady s vytvořením práce nebo bez něj.
    - **Zásady uzavírání kontejnerů** – Vyberte jednu z následujících možností a definujte, co se má stát, když je kontejner uzavřen:

        - *Automatické uvolnění* – Kontejner bude považován za uvolněný z balicí stanice a akce, která je specifikována v poli **Zásady uvolňování kontejnerů** bude spuštěna.
        - *Zpožděné uvolnění* – Kontejner nebude okamžitě uvolněn z balicí stanice. Skladník ho musí později ručně uvolnit.
        - *Volitelné* – Zatímco pracovník zavírá kontejner, bude si moci vybrat, zda má být kontejner uvolněn.

        Pokud balicí stanice manipuluje převážně s jednotlivými kontejnery, které jsou expedovány přímo k zákazníkům, je nejpřirozenějším přístupem kontejnery okamžitě uvolnit. Pokud balicí stanice zpracovává zásilky, které se skládají z více kontejnerů, nebo dokonce palet, je pravděpodobně nejlepší odložit uvolnění, dokud nebude celá zásilka nebo paleta zabalena a připravena k vyzvednutí.

    - **Zásady uvolňování kontejnerů** – Vyberte jednu z následujících možností a definujte, co se má stát, když je kontejner uvolněn z balicí stanice:

        - *Zpřístupnit na konečném místě odeslání* – Aktualizujte kontejner na konečné místo odeslání. Pokud vyberete tuto možnost, použijte pole **Výchozí místo pro konečnou zásilku** k určení preferovaného umístění kontejneru po jeho zavření.
        - *Vytvořit práci na přesunutí kontejneru z balicí stanice* – Vytvořte práci na přesunutí kontejneru z balicí stanice do odkládacího prostoru nebo přímo k vykládacím dveřím. Použijte pole **Pracovní šablona** k určení pracovní šablony, která by měla být použita při vytvoření práce pro kontejner.
        - *Přiřaďte kontejner na výstupní třídicí pozici* – Tato možnost se používá s funkcí [odchozí třídění](outbound-sorting.md).

        Ve většině případů doporučujeme vytvořit práci pro přesun kontejnerů, protože tento přístup lépe reprezentuje skutečné ruční procesy ve skladu. Avšak pro jednoduché scénáře nebo situace, kdy je balicí stanice umístěna přímo v oblasti vykládacích dveří, může být vhodnější, aby byl kontejner okamžitě k dispozici na konečném místě odeslání.

    - **Pracovní šablona** – Vyberte pracovní šablonu, která má být použita při vytvoření práce pro kontejner. Toto pole je dostupné pouze tehdy, když je pole **Zásady uvolňování kontejnerů** nastaveno na *Vytvořit práci na přesunutí kontejneru z balicí stanice* a souvisí s typem pracovního příkazu, který je pojmenován *Vychystávání balených kontejnerů*. Další informace získáte v části [Pracovních šablony a směrnice místa](control-warehouse-location-directives.md).

    Ve zbývajících krocích nakonfigurujete nastavení, která se týkají *tvorby manifestu*. Tvorba manifestu je proces specifikování hmotnosti kontejneru, skupiny kontejnerů nebo zásilky spolu s ID sledování, které je obdrženo od poskytovatele přepravy. Dynamics 365 Supply Chain Management se neintegruje s externími systémy poskytovatelů dopravy. Místo toho musí skladníci vytisknout štítky, které obdrží od poskytovatele přepravy, a poté naskenovat sledovací číslo, když dokončí proceduru vytváření manifestu.

    Vzhledem k tomu, že požadavky manifestu se liší od zákazníka k zákazníkovi, a dokonce i od zásilky k zásilce, zásady balení umožňují značnou flexibilitu v pracovním postupu. Manifesty můžete nastavit pro kontejnery, skupiny kontejnerů a zásilky v libovolné kombinaci.

    Pokud používáte proceduru víceúrovňového manifestu, pracovníci musí vytvořit manifest pro všechny kontejnery předtím, než vytvoří manifest pro související skupinu kontejnerů, a musí vytvořit manifest pro všechny skupiny kontejnerů, než vytvoří manifest pro související zásilku.

1. Na záložce s náhledem **Manifest kontejneru** můžete nastavit následující pole:

    - **Automatické vytvoření manifestu při zavření kontejneru** – Nastavte tuto možnost na *Ano*, chcete-li použít informace manifestu jako součást procesu uzavírání kontejneru. Pokud nepoužíváte integraci dopravy, musí být informace zaznamenány ručně.
    - **Požadavky na manifest pro kontejner** – Vyberte jednu z následujících možností:

        - *Žádný* - Nebude použit žádný proces vytváření manifestu.
        - *Ruční* – Vytváření manifestu bude vyžadovat pracovní postup balení. Systém nedovolí uzavření nebo uvolnění kontejneru, dokud nebude vytváření manifestu dokončeno.
        - *Řízení dopravy* – Vytváření manifestu se bude provádět prostřednictvím nástrojů na výpočet přepravních sazeb pro řízení dopravy (TMS). Protože tato možnost vyžaduje vlastní vývoj k implementaci konkrétního modulu pro poskytovatele přepravy, nebude v aktuální verzi fungovat hned po vybalení.

    - **Vytisknout obsah kontejneru** – Nastavte tuto možnost na *Ano* pro automatický tisk sestavy obsahu kontejneru, když je kontejner registrován jako uzavřený. Sestavu lze také vytisknout na vyžádání.

1. Na pevné záložce **Manifest skupiny kontejnerů** v poli **Požadavky na manifest na skupinu kontejnerů** vyberte jednu z následujících možností:

    - *Žádný* – Manifest skupiny kontejnerů nebude zahrnut jako požadavek do pracovního postupu balení.
    - *Ruční* – Manifest skupiny kontejnerů bude zahrnut jako požadavek do pracovního postupu balení. Aby bylo možné vytvořit manifest skupiny, všechny kontejnery ve skupině musí být uzavřeny. Tuto možnost vyberte, pokud jste povinni vyplnit manifest pro každou skupinu kontejnerů, která je zabalena v balicí stanici. Tuto možnost obvykle vyberete, pokud jsou kontejnery baleny na paletě a je zobrazena celá paleta.

    > [!NOTE]
    > Aktuální verze nepodporuje sestavy manifestu pro skupiny kontejnerů a pro skupiny kontejnerů neexistuje podpora modulu TMS.

1. Na pevné záložce **Manifest zásilky** nastavte následující pole:

    - **Požadavky na manifest pro zásilku** – Vyberte jednu z následujících možností:

        - *Žádný* – Manifest zásilky nebude zahrnut jako požadavek do pracovního postupu balení.
        - *Ruční* – Manifest zásilky bude zahrnut jako požadavek do pracovního postupu balení. Žádné kontejnery pro zásilku nelze uvolnit, dokud není vytváření manifestu dokončeno.
        - *Řízení dopravy* – Vytváření manifestu se bude provádět prostřednictvím nástrojů na výpočet přepravních sazeb TMS. Protože tato možnost vyžaduje vlastní vývoj k implementaci konkrétního modulu pro poskytovatele přepravy, nebude v aktuální verzi fungovat hned po vybalení.

        Vytváření manifestu zásilky musí být povoleno, pokud jste povinni vyplnit manifest pro celou zásilku, která je zabalena v balicí stanici. Obvykle se používá, když je vyžadován jeden konsolidovaný manifest, i když se zásilka skládá z více kontejnerů nebo skupin kontejnerů.

    - **Tisk dodacího listu** – Nastavte tuto možnost na *Ano* pro automatický tisk dodacího list jako součásti manifestu zásilky. Dodací list lze také vytisknout na vyžádání.

### <a name="set-up-container-types"></a>Nastavení typů kontejneru

Během procesu ručního balení musí být kontejnery vytvořeny předtím, než do nich mohou být zabaleny položky. Každý kontejner musí být založen na *typu kontejneru*, který definuje maximální fyzický objem a nosnost kontejneru.

K nastavení typu kontejneru postupujte následovně.

1. Přejděte na **Řízení skladu \> Nastavení \> Kontejnery \> Typy kontejnerů**.
1. V podokně akcí vyberte možnost **Nový** pro přidání typu kontejneru.
1. Pro nový typ kontejneru nastavte následující pole:

    - **Kód typu kontejneru** – Zadejte jedinečné ID pro typ kontejneru.
    - **Popis** – zadejte popis nového typu kontejneru.
    - **Hmotnost obalu** – Zadejte skutečnou nebo odhadovanou hmotnost kontejneru.
    - **Maximální čistá hmotnost** – Zadejte maximální hmotnost, kterou může kontejner pojmout.

1. V části **Rozměry kontejneru** do polí **Délka**, **Šířka**, **Výška** a **Objem** zadejte fyzické rozměry samotného kontejneru.
1. V části **Maxima** do polí **Délka**, **Šířka**, **Výška** a **Objem** zadejte maximální fyzické rozměry, které kontejner pojme.
1. Můžete definovat další atributy pro typy kontejnerů, které jsou spojeny s jinými operacemi, které používají kontejnery. Další informace viz [Kontejnerizace](wave-containerization.md).

> [!NOTE]
> Pro proces ručního balení systém používá pouze hodnotu pole **Maximální čistá hmotnost** a hodnotu pole **Objem** v části **Maxima**.

### <a name="set-up-packing-profiles"></a>Nastavení profilů balení

*Balicí profily* jsou potřebné pro proces balení. Lze je vybrat nebo nastavit jako výchozí, když spustíte operaci balení na stránce **Balení**.

Chcete-li nastavit profil balení, postupujte následujícím způsobem:

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Profily balení**.
1. Buď vyberte existující profil v podokně seznamu, nebo vyberte v podokně akcí možnost **Nový** a vytvořte nový.
1. V záhlaví nového nebo vybraného profilu nastavte následující pole:

    - **ID profilu balení** – Zadejte krátké ID profilu.
    - **Popis** – Zadejte popis profilu balení.
    - **Zásady balení kontejnerů** – Vyberte zásady balení, které se vztahují na profil. Další informace naleznete v části [Nastavení zásad balení kontejnerů](#packing-policy) v tomto článku.
    - **Režim ID kontejneru** – Vyberte, zda ID kontejneru má být automaticky generováno při vytvoření kontejneru, nebo zda se vytváří ručně.
    - **Typ kontejneru** – Vyberte typ kontejneru, který použije jako výchozí při vytvoření nového kontejneru.
    - **Automaticky vytvořit kontejner při zavření kontejneru** – Zaškrtněte toto políčko, chcete-li automaticky vytvořit nový kontejner, pokud je předchozí kontejner uzavřen a v aktuální zásilce zůstane jeden nebo více řádků.

### <a name="set-up-warehouse-workers"></a>Nastavení pracovníku skladu

Každý uživatel nebo pracovník, který balí kontejnery pomocí stránky **Balení** webového klienta nebo aktivity *Balení* aktivity v mobilní aplikaci Warehouse Management, musí mít uživatelský účet spojený se záznamem *pracovník/osoba*, ke kterému jsou přiřazena požadovaná bezpečnostní přístupová práva. (Další informace o nastavení uživatelů naleznete v tématu [Vytváření nových uživatelů](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md).)

Postupujte pomocí následujících kroků pro nastavení záznamu *pracovník/osoba* pro proces balení.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Pracovník**.
1. V podokně Akce vyberte možnost **Nový** a přidejte uživatele pracovníka.
1. Nastavte pole **Pracovník** na existující záznam pracovníka, který je definován v modulu **Personální** modul pro uživatele, který bude provádět proces balení.
1. Na záložce **Profil** zadejte následující pole:

    - **Zásady balení kontejnerů** – Vyberte zásady balení kontejnerů, které definují, jak mají být kontejnery na balicí stanici zpracovávány. Zásady balení kontejnerů, které zde vyberete, budou pro pracovníka předem vybrány, když otevře balicí stanici. Další informace naleznete v následujícím příspěvku na blogu: [Vylepšená funkce balení](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **ID profilu balení** – Vyberte ID profilu balení, které definuje používané zásady balení a nastavení kontejneru. Pokud je vybrané ID profilu balení přidruženo k zásadám balení kontejneru, nebudete moci změnit nastavení pole **Zásady balení kontejnerů** na této stránce.

1. Na pevné záložce **Výchozí balicí stanice** vyberte výchozí pracoviště, sklad a místo, které se vztahují na pracovníka.
1. Pokud bude pracovník používat mobilní aplikaci Warehouse Management ke správě a registraci své práce na balení kontejnerů, na pevné kartě **Uživatelé** nastavte jeden nebo více účtů, které může pracovník použít k přihlášení do aplikace. Další informace naleznete v tématu [Nastavení uživatelských účtů mobilních zařízení](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Příklad

Tato část obsahuje příklad scénáře, který ukazuje, jak vytvořit objednávku a zabalit položky.

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

Tento scénář můžete také použít jako vodítko pro použití této funkce v produkčním systému. V takovém případě však musíte každé vlastní nastavení, které je zde popsáno, nahradit vlastními hodnotami.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Přihlaste se jako uživatel, který může dělat balicí práce

Přihlaste se do Supply Chain Management pomocí uživatelského účtu, který má oprávnění potřebná k balení kontejnerů. Uživatel *Julia Funderburková* je součástí ukázkových dat a má požadovaná oprávnění. Tento uživatel má ID uživatele *Admin*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Vytvoření prodejní objednávky a provedení práce

Chcete-li vytvořit prodejní objednávku a provést přesun objednaných položek na balicí stanici, postupujte podle těchto kroků.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu *US-005*.
1. Zvolte **OK** a zavřete dialogové okno.
1. Nová prodejní objednávka je otevřena a obsahuje jeden prázdný řádek na pevné záložce **Řádky prodejní objednávky**. Nastavte následující hodnoty pro nový řádek objednávky:

    - **Číslo položky:** *A0001*
    - **Množství:** *2*
    - **Lokalita:** *6*
    - **Sklad:** *62*

1. V době, kdy je vybrán řádek objednávky, vyberte na panelu nástrojů **Zásoby \> Rezervace** na pevné záložce **Řádky prodejní objednávky**.
1. Na stránce **Rezervace** v podokně Akce klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Zpráva zobrazuje ID zásilky a vlny pro objednávku.

1. V době, kdy je vybrán řádek objednávky na záložce s náhledem **Řádky prodejní objednávky**, vyberte na panelu nástrojů **Sklad** \> **Podrobnosti práce**. Pokud používáte ke spuštění svých vln dávkové zpracování, možná budete muset chvíli počkat, než se práce vytvoří.
1. V podokně akcí na kartě **Práce** na kartě **Práce** vyberte **Provést práci**.
1. Na stránce **Provedení práce** pole **ID uživatele** nastavte na *62*.
1. V podokně akcí vyberte možnost **Ověřit práci**.
1. Když obdržíte zprávu, že vaše práce je platná, vyberte **Provést práce** k dokončení procesu vybírání skladových položek a jejich umístění do místa *Balení*.
1. Poznamenejte si hodnotu **ID zásilky**, která je zobrazena pro práci v horní mřížce.

### <a name="pack-the-ordered-items-into-a-container"></a>Zabalte objednané zboží do kontejneru

Skladové položky byly nyní převezeny do balicí oblasti a jsou připraveny k zabalení do kontejnerů. Postupujte následujícím způsobem k vytvoření nového kontejneru v systému a jeho zabalení.

1. Přejděte na **Řízení skladu \> Balení a kontejnerizace \> Balení**.
1. V dialogovém okně **Vybrat balicí stanici** nastavte následující hodnoty:

    - **Lokalita:** *6*
    - **Sklad:** *62*
    - **Místo:** *balení*
    - **ID profilu balení:** *WH62*

1. Vyberte **OK**.
1. Na stránce **Balení** v poli **Registrační značka nebo zásilka** zadejte ID zásilky, které jste si předtím poznamenali. Nyní byste měli vidět zbývající rozbalené položky na pevné záložce **Otevřené řádky**.
1. V podokně Akce vyberte možnost **Nový kontejner** k vytvoření kontejneru v systému.
1. V dialogovém okně **ID nového kontejneru** nastavte pole **Typ kontejneru** na *SmallBox*.
1. Tlačítkem **OK** vytvořte kontejner.
1. Výběrem **OK** se vraťte na stránku **Balení**. Pevná záložka **Otevřené kontejnery** nyní zobrazuje hodnotu **ID kontejneru** kontejneru, který jste vytvořili.
1. Pro tento scénář si zatím zabalíte pouze jednu z objednaných položek. Na pevné záložce **Balení položky** proto nastavte následující hodnoty:

    - **Množství:** *1.00*
    - **Identifikátor:** *A0001*

    Ihned poté, co vyberete hodnotu **Identifikátor**, stránka aktualizuje pevné záložky **Otevřené řádky** a **Všechny řádky** označující, že jedna položka byla zabalena. Nyní byste měli zabalit jeden ze dvou kusů položky *A0001*.

1. V podokně akcí zvolte **Zavřít kontejner**.
1. V dialogovém okně **Zavřít kontejner** vyberte **Získat systémovou hmotnost**, aby se vyplnila hodnota **Celková hmotnost**.
1. Vyberte **OK** a kontejner zavřete.

> [!TIP]
> Existují různé způsoby zobrazení kontejnerů na základě kontextu. Když například balíte zásilku, je často užitečné zobrazit buď kontejnery, které jsou součástí zásilky, nebo všechny kontejnery, které jsou fyzicky na balicí stanici. Stránka **Balící stanice** obsahuje tlačítka, která můžete použít k zobrazení všech otevřených a uzavřených kontejnerů na balicí stanici. Tato zobrazení nejsou omezena na konkrétní zásilku. Mohou se hodit v situacích, kdy jeden pracovník balí kontejner a jiný pracovník vytváří manifest a uvolňuje kontejner.
>
> K dispozici je také konsolidovaný pohled na všechny kontejnery. Toto zobrazení je užitečné především pro uživatele, kteří pracují mimo kontext jedné balicí stanice. K zobrazení přejděte na **Řízení skladu \> Balení a kontejnerizace \> Kontejnery**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
