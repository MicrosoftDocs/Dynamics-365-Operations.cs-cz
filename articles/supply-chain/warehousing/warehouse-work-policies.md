---
title: Zásady práce
description: Toto téma vysvětluje, jak nastavit pracovní zásady.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 08c04caeace7b8ced40915ace1561d817426cba3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424224"
---
# <a name="work-policies"></a>Zásady práce

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit systém a aplikaci skladu tak, aby podporovaly pracovní zásady. Tuto funkci můžete použít k rychlé registraci zásob bez vytvoření práce odložení, když obdržíte objednávky nákupu nebo převodu nebo když dokončíte výrobní procesy. Toto téma obsahuje obecné informace. Podrobné informace týkající se přijímání registračních značek viz [Příjem registrační značky prostřednictvím aplikace skladu](warehousing-mobile-device-app-license-plate-receiving.md).

Zásady práce určují, zda je práce ve skladu vytvořena, když je vyrobená položka nahlášena jako dokončená nebo když je zboží přijato pomocí aplikace skladu. Každé zásady práce nastavíte definováním podmínek, ve kterých platí: typy a procesy pracovní objednávky, umístění zásob a (volitelně) produkty. Například objednávka produktu *A0001* musí být přijata na místě *RECV* ve skladu *24*. Později se produkt spotřebuje v jiném procesu na místě *RECV*. V takovém případě můžete nastavit pracovní zásadu, která zabrání tomu, aby v případě, že pracovník ohlásí produkt *A0001* jako přijatý do skladu *RECV*, nebyla vytvořena práce odložení.

> [!NOTE]
> - Aby byly zásady práce aktivní, musíte pro ně definovat nejméně jedno místo na pevné záložce **Skladovací místa** na stránce **Zásady práce**. 
> - Nemůžete zadat stejné umístění pro více pracovních zásad.
> - Možnost **Tisk štítku** pro mobilní zařízení s aplikací Warehousing nevytisknou registrační štítek bez vytvoření práce.

## <a name="activate-the-features-in-your-system"></a>Aktivace funkcí v systému

Chcete-li zpřístupnit všechny funkce popsané v tomto tématu ve vašem systému, zapněte v systému dvě následující funkce [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Rozšíření příjmu registrační značky
- Vylepšení zásad práce pro příchozí práci

## <a name="the-work-policies-page"></a>Stránka Zásady práce

Chcete-li nastavit zásady práce, přejděte na **Řízení skladu \> Nastavení \> Práce \> Zásady práce**. Poté na každé pevné záložce nastavte pole, jak je popsáno v následujících pododdílech.

### <a name="the-work-order-types-fasttab"></a>Pevná záložka Typy pracovního příkazu

Na pevné záložce **Typy pracovních příkazů** přidejte všechny typy pracovních příkazů a související pracovní procesy, na které se pracovní zásady vztahují. Pro pracovní zásady jsou podporovány následující typy pracovních příkazů a související pracovní procesy.

| Typ pořadí pracovních činností | Proces práce |
|---|---|
| Výdej suroviny| Všechny související procesy |
| Vyskladnění vedlejšího produktu | Všechny související procesy |
| Výdej dokončeného zboží | Všechny související procesy |
| Příjem převodu | Přijetí (a odložení) registrační značky |
| Nákupní objednávky | <ul><li>Přijetí (a odložení) registrační značky</li><li>Přijetí (a odložení) položky nákladu</li><li>Přijetí řádku nákupní objednávky (a odložení)</li><li>Přijetí zboží nákupní objednávky (a odložení)</li></ul> |

Chcete-li nastavit pracovní zásady tak, aby se vztahovaly na několik pracovních procesů stejného typu pracovního příkazu, přidejte do mřížky samostatný řádek pro každý pracovní proces.

Pro každý řádek v mřížce nastavte pole **Metodu tvorby práce** na jednu z následujících hodnot:

- **Nikdy** - Tato hodnota značí, že pracovní zásada zabrání vytvoření práce ve skladu pro vybraný typ pracovního příkazu a souvisejícího pracovního procesu.
- **Cross docking** - Zásady práce vytvoří křížové dokovací práce pomocí zásady, kterou vyberete v poli **Název zásady cross dockingu**.

### <a name="the-inventory-locations-fasttab"></a>Pevná záložka Umístění zásob

Na pevné záložce **Umístění zásob** přidejte všechna umístění, kde by se měly tyto pracovní zásady použít. Pokud žádné umístění není přidruženo k zásadám práce, zásady práce se nepoužijí na žádný proces.

Nemůžete zadat stejné umístění pro více pracovních zásad.

Je možné použít umístění skladu, které je přiřazeno k profilu místa, kde není volba **Použít sledování registrační značky** vypnutá. V takovém případě pracovníci zaregistrují zásoby na skladě.

### <a name="the-products-fasttab"></a>Pevná záložka Produkty

Na kartě **Produkty** nastavte pole **Výběr produktu** na řízení, na které produkty by se zásady měly vztahovat:

- **Vše** - Zásady by se měly vztahovat na všechny produkty.
- **Vybrané** - Zásady by se měly vztahovat pouze na produkty, které jsou uvedeny v tabulce. Použijte panel nástrojů na pevné záložce **Produkty** pro přidání produktů do mřížky nebo jejich odstranění z mřížky.

## <a name="default-and-custom-to-locations"></a>Výchozí a vlastní umístění „do“

> [!NOTE]
> Abyste zpřístupnili funkce popsané v této části ve vašem systému, musíte zapnout funkce *Vylepšení příjmu poznávací značky* a *Vylepšení pracovních zásad pro příchozí práci* v okně [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Dříve systém podporoval příjem pouze ve výchozím umístění, které je definováno pro každý sklad. Položky nabídky mobilního zařízení, které používají následující procesy vytváření práce, však nyní poskytují volbu **Použít výchozí data**. Tato možnost umožňuje přiřadit vlastní volbu „do“ místa k jedné nebo více položkám nabídky. (Tato možnost již byla k dispozici pro některé jiné typy položek nabídky.)

- Přijetí (a odložení) registrační značky
- Přijetí (a odložení) položky nákladu
- Přijetí řádku nákupní objednávky (a odložení)
- Přijetí zboží nákupní objednávky (a odložení)

Nastavení **Do místa** pro položku nabídky přepíše výchozí umístění příjmu do skladu, pro všechny objednávky, které jsou zpracovány pomocí této položky nabídky.

Chcete-li nastavit položku nabídky mobilního zařízení na podporu příjmu do vlastního místa, postupujte takto.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. Vyberte nebo vytvořte položku nabídky, která používá jeden z procesů vytváření práce, které jsou uvedeny dříve v této části.
1. Na pevné záložce **Obecné** nastavte možnost **Použít výchozí data** na **Ano**.
1. V podokně akcí vyberte **výchozí data**.
1. Na stránce **Výchozí data** nastavte následující hodnoty:

    - **Výchozí datové pole:** Nastavte toto pole na *Do místa*.
    - **Sklad:** Vyberte cílový sklad, který chcete použít s touto položkou nabídky.
    - **Umístění:** Toto pole uvádí všechna ID umístění, která jsou k dispozici pro vybraný sklad. Nastavení tohoto pole však ve skutečnosti nemá žádný účinek. Proto je nemůžete nechat prázdné. Seznam však můžete použít k potvrzení ID, které musíte zadat do pole **Pevně zakódovaná hodnota**.
    - **Pevně zakódovaná hodnota:** Zadejte ID místa pro přijímající umístění, které se vztahuje na tuto položku nabídky.

> [!TIP]
> Pracovní zásadu lze použít, pouze pokud jsou všechna místa pro příjem uvedena v příslušném nastavení zásad práce. Tento požadavek platí bez ohledu na to, zda používáte výchozí umístění pro příjem skladu nebo vlastní umístění „do“.

## <a name="example-scenario-warehouse-receiving"></a>Příklad scénáře: Příjem skladu

Všechny produkty, které obdrží proces *Přijetí zboží nákupní objednávky (a odložení)* musí být registrován v místě *FL-001* a musí být k dispozici ve skladu *24*. Práce by však neměla být vytvořena. Produkty, které jsou přijímány jakýmkoli jiným procesem (tj. pomocí jiných položek nabídky mobilního zařízení), by měly být zaregistrovány ve výchozím umístění pro příjem skladu (*RECV*) a práce by měla být vytvořena jako obvykle. (Tento scénář nezobrazuje výchozí nastavení příjmu.)

Tento scénář vyžaduje následující prvky:

- Zásady práce pro proces *Přijetí zboží nákupní objednávky (a odložení)* v místě *FL-001*, pro všechny produkty
- Položka nabídky mobilního zařízení, která má výchozí data a nastavuje pole **Na místo** na hodnotu *FL-001*

### <a name="prerequisites"></a>Předpoklady

Abyste zpřístupnili funkce popsané v tomto scénáři ve vašem systému, musíte zapnout funkce *Vylepšení příjmu registrační značky* a *Vylepšení pracovních zásad pro příchozí práci* v okně [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tento scénář používá standardní ukázková data. Proto, chcete-li s tímto scénářem pracovat pomocí hodnot zde poskytnutých, musíte používat prostředí, ve kterém jsou nainstalována ukázková data. Dále musíte vybrat právnickou osobu **USMF**.

### <a name="set-up-a-work-policy"></a>Nastavení zásady práce

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Práce \> Pracovní zásady**.
1. Zvolte **Nové**.
1. Do pole **Název zásady práce** zadejte *Žádná odložená práce nákupní položky*.
1. Zvolte **Uložit**.
1. Na pevné záložce **Typy pracovních příkazů** vyberte **Přidat** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:

    - **Typ pracovního příkazu:** *Nákupní objednávky*
    - **Proces tvorby práce:** *Příjem (a odložení) řádku nákupní objednávky*
    - **Metoda tvorby práce:** *Nikdy*
    - **Název zásad cross dockingu:** Toto pole nechte prázdné.

1. Na pevné záložce **Skladová místa** vyberte **Přidat** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:

    - **Sklad:** *24*
    - **Umístění:** *FL-001*

1. Na pevné záložce **Produkty**, nastavte pole **Výběr produktu** na *Vše*.
1. Zvolte **Uložit**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Nastavení položky nabídky na mobilním zařízení na registraci přijatých položek

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V levém podokně vyberte existující položku nabídky **Příjem nákupu**.
1. Na pevné záložce **Obecné** nastavte možnost **Použít výchozí data** na *Ano*.
1. Zvolte **Uložit**.
1. V podokně akcí vyberte **výchozí data**.
1. Na pevné záložce **Výchozí data** vyberte **Nový** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:

    - **Výchozí datové pole:** *Do místa*
    - **Sklad:** *24*
    - **Místo:** Toto pole nechte prázdné.
    - **Pevně zakódovaná hodnota:** *FL-001*

1. Zvolte **Uložit**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Příjem nákupní objednávky bez vytvoření práce

Příklad v této části ukazuje, jak přijímat položku objednávky, ale bez vytvoření práce, na místě, které se liší od výchozího přijímacího místa, které je nastaveno na sklad. Tento příklad používá zásady práce a položku mobilního zařízení, které jste vytvořili dříve v tomto scénáři.

#### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Zvolte **Nové**.
1. V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:

    - **Účet dodavatele:** *US-101*
    - **Lokalita:** *2*
    - **Sklad:** *24*

1. Vyberte **OK** - nová prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Na pevné záložce **Řádky objednávek** nastavte následující hodnoty pro prázdný řádek:

    - **Číslo položky:** *A0001*
    - **Množství:** *1*

1. Zvolte **Uložit**.
1. Poznamenejte si číslo nákupní objednávky.

#### <a name="receive-a-purchase-order"></a>Příjem nákupní objednávky

1. Na mobilním zařízení se přihlaste ke skladu *24* a jako ID uživatele zadejte *24* a jako heslo *1*.
1. Vyberte **Příchozí**.
1. Vyberte **Příjem nákupu**. Pole **Umístění** by mělo být nastaveno na *FL-001*.
1. Zadejte číslo objednávky pro objednávku, kterou jste vytvořili v předchozím postupu.
1. V poli **Číslo zboží** zadejte *A0001*.
1. Vyberte **OK**.
1. Do pole **Množství** zadejte *1*.
1. Vyberte **OK**.

Nákupní objednávka je nyní přijata, ale není s ní spojena žádná práce. Byl aktualizován soupis zásob a množství *1* položky *A0001* je nyní k dispozici v místě *FL-001*.

## <a name="example-scenario-manufacturing"></a>Příklad scénáře: Výroba

V následujícím příkladu jsou dvě výrobní zakázky, *PROD-001* a *PROD-002*. Výrobní zakázka *PROD-001* má operaci s názvem *Sestavení*, kde produkt *SC1* je hlášen jako dokončený v místě *001*. Výrobní zakázka *PROD-002* má operaci, která se nazývá *Lakování* a spotřebovává produkt *SC1* z umístění *001*. Výrobní zakázka *PROD-002* také spotřebovává suroviny *RM1* 1 z umístění *001*. Surovina *RM1* je uložena ve skladu *BULK-001* a bude vyskladněno v umístění *001* během práce ve skladu pro výdej surovin. Pro uvolnění výroby *PROD-002* je generována práce vyskladnění.

[![Zásady práce ve skladu](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Při plánování konfigurace zásad práce ve skladu pro tento scénář je třeba zvážit následujících body:

- Práce ve skladu pro výdej dokončeného zboží není vyžadována, když vykážete produkt *SC1* jako dokončený z výrobní zakázky *PROD-001* do umístění *001*. Důvodem je, že operace *Lakování* pro výrobní zakázku *PROD-002* spotřebovává *SC1* na stejném místě.
- Práce ve skladu pro vyzvednutí surovin je požadována pro účely přesunutí surovin *RM1* z umístění ve skladu *BULK-001* do umístění *001*.

Toto je příklad zásad práce, které můžete nastavit na základě těchto důvodů:

- **Název pracovních zásad:** *Žádná odložená práce*
- **Typy pracovních příkazů:** *Výdej dokončeného zboží* a *Vyskladnění vedlejšího produktu*
- **Skladová místa:** Sklad *51* a místa *001*
- **Produkty:** *SC1*

Následující ukázkové scénáře obsahují podrobné pokyny ke způsobu nastavení zásad pracovního skladu pro tento scénář.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Ukázkový scénář: Vykázání jako dokončeného v místě, které není řízeno registrační značkou

Tento scénář ukazuje příklad, kdy je výrobní příkaz vykázán jako dokončený v místě, které nemá licenční kód.

Tento scénář používá standardní ukázková data. Proto, chcete-li s tímto scénářem pracovat pomocí hodnot zde poskytnutých, musíte používat prostředí, ve kterém jsou nainstalována ukázková data. Dále musíte vybrat právnickou osobu **USMF**.

### <a name="set-up-a-warehouse-work-policy"></a>Nastavení zásady práce ve skladu

Skladové procesy ne vždy zahrnují skladovou práci. Definováním zásad práce můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Práce \> Pracovní zásady**.
1. Zvolte **Nové**.
1. Do pole **Název zásady práce** zadejte *Žádná odložená práce*.
1. V podokně akcí vyberte **Uložit**.
1. Na pevné záložce **Typy pracovních příkazů** vyberte **Přidat** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:

    - **Typ pracovního příkazu:** *Výdej dokončeného zboží*
    - **Pracovní proces:** *Všechny související pracovní procesy*
    - **Metoda tvorby práce:** *Nikdy*
    - **Název zásad cross dockingu:** Toto pole nechte prázdné.

1. Na pevné záložce Skladová místa znovu vyberte **Přidat** pro přidání druhého řádku do mřížky a nastavení následujících hodnot pro nový řádek:

    - V poli **Typ pracovního příkazu:** *Vyskladnění vedlejšího produktu*
    - **Pracovní proces:** *Všechny související pracovní procesy*
    - **Metoda tvorby práce:** *Nikdy*
    - **Název zásad cross dockingu:** Toto pole nechte prázdné.

1. Na pevné záložce **Skladová místa** vyberte **Přidat** pro přidání řádek do mřížky a nastavení následujících hodnot pro nový řádek:

    - **Sklad:** *51*
    - **Místo:** *001*

1. Na pevné záložce **Produkty**, nastavte pole **Výběr produktu** na *Vybrané*.
1. Na pevné záložce **Produkty** přidejte řádek do mřížky výběrem možnosti **Přidat**.
1. V novém řádku nastavte pole **Číslo položky** na *L0101*.
1. V podokně akcí vyberte **Uložit**.

### <a name="set-up-an-output-location"></a>Nastavení výstupního umístění

1. Přejděte na **Správa organizace \> Zdroje \> Skupiny zdrojů.**
1. V levém podokně vyberte skupinu zdrojů **5102**.
1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Výstupní sklad:** *51*
    - **Výstupní umístění:** *001*

1. V podokně akcí vyberte **Uložit**.

> [!NOTE]
> Umístění *001* není umístění řízené registrační značkou. Umístění výstupu, které není řízeno registrační značkou, můžete nastavit pouze v případě, že pro umístění existuje příslušné pracovní pravidlo.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Vytvoření výrobní zakázky a její ohlášení jako dokončené

1. Přejděte na **Řízení výroby \> Výrobní zakázky \> Všechny výrobní zakázky**.
1. V podokně akcí vyberte možnost **Nová výrobní zakázka**.
1. V dialogovém okně **Vytvoření výrobní zakázky** nastavte pole **Číslo položky** na *L0101*.
1. Vyberte **Vytvořit**, prodejní objednávka se vytvoří a dialogové okno se zavře.

    Nová výrobní zakázka je přidána do mřížky na stránce **Všechny výrobní objednávky**.

    Nechte vybranou novou výrobní zakázku.

1. V podokně akcí na kartě **Výrobní objednávka** ve skupině **Proces** zvolte **Odhad**.
1. V dialogovém okně **Odhad** si přečtěte odhad a poté výběrem **OK** zavřete dialogové okno.
1. V podokně akcí na kartě **Výrobní objednávka** ve skupině **Proces** zvolte **Start**.
1. V dialogovém okně **Start** na kartě **Obecné** nastavte hodnotu pole **Automatická spotřeba kusovníku** na *Nikdy*.
1. Volbou **OK** uložte svá nastavení a zavřete dialogové okno.
1. V podokně akcí na kartě **Výrobní objednávka** ve skupině **Proces** zvolte **Vykázat jako dokončené**.
1. V dialogovém okně **Vykázat jako dokončené** na kartě **Obecné** nastavte možnost **Chyba přijetí** na *Ano*.
1. Volbou **OK** uložte svá nastavení a zavřete dialogové okno.
1. V podokně akcí na kartě **Sklad** ve skupině **Obecné** vyberte **Podrobnosti práce**.

Pokud byla výrobní zakázka ohlášena jako dokončená, žádná práce nebyla pro vyskladnění vytvořena. K tomuto chování dochází, protože jsou definovány zásady práce, které brání generování práce, když je produkt *L0101* ohlášen za dokončený v umístění *001*.

## <a name="more-information"></a>Další informace

Další informace o položkách nabídky mobilního zařízení naleznete v tématu [Nastavení mobilních zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md).

Další informace týkající se přijímání registračních značek a zásad práce získáte v tématu [Příjem registrační značky prostřednictvím aplikace skladu](warehousing-mobile-device-app-license-plate-receiving.md).

Další informace o správě příchozího vytížení získáte v části [Skladová manipulace s příchozím zatížením pro nákupní objednávky](inbound-load-handling.md).
